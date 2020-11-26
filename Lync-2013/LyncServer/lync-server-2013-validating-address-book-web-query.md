---
title: 'Lync Server 2013 : validation de la requête Web du carnet d’adresses'
description: 'Lync Server 2013 : validation de la requête Web du carnet d’adresses.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating address book web query
ms:assetid: e6ae0a5a-e131-4cfe-9a33-6e611831072d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720925(v=OCS.15)
ms:contentKeyID: 63969662
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e73c39fc33f8d1851fc89d277333a94aaa137790
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438903"
---
# <a name="validating-address-book-web-query-in-lync-server-2013"></a><span data-ttu-id="fa83f-103">Validation de la requête Web du carnet d’adresses dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa83f-103">Validating address book web query in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fa83f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fa83f-104">

<span> </span></span></span>

<span data-ttu-id="fa83f-105">_**Dernière modification de la rubrique :** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="fa83f-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa83f-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="fa83f-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="fa83f-107">Jour</span><span class="sxs-lookup"><span data-stu-id="fa83f-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa83f-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="fa83f-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="fa83f-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa83f-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa83f-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="fa83f-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="fa83f-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="fa83f-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="fa83f-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsAddressBookWebQuery.</span><span class="sxs-lookup"><span data-stu-id="fa83f-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsAddressBookWebQuery cmdlet.</span></span> <span data-ttu-id="fa83f-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="fa83f-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsAddressBookWebQuery&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="fa83f-114">Description</span><span class="sxs-lookup"><span data-stu-id="fa83f-114">Description</span></span>

<span data-ttu-id="fa83f-115">Le cmdlet Test-CsAddressBookWebQuery permet aux administrateurs de vérifier que les utilisateurs peuvent utiliser le service de requête sur le carnet d’adresses pour rechercher un contact en particulier.</span><span class="sxs-lookup"><span data-stu-id="fa83f-115">The Test-CsAddressBookWebQuery cmdlet enables administrators to verify that users can use the Address Book Web Query service to search for a specific contact.</span></span> <span data-ttu-id="fa83f-116">Lorsque vous exécutez l’applet de connexion, Test-CsAddressBookWebQuery vous connecte pour la première fois au service de tickets Web.</span><span class="sxs-lookup"><span data-stu-id="fa83f-116">When you run the cmdlet, Test-CsAddressBookWebQuery will first connect to the Web Ticket service to be authenticated.</span></span> <span data-ttu-id="fa83f-117">Si l’authentification est réussie, l’applet de requête se connecte alors au service de requête sur le carnet d’adresses et recherche le contact spécifié.</span><span class="sxs-lookup"><span data-stu-id="fa83f-117">If authentication is successful, the cmdlet will then connect to the Address Book Web Query service and search for the specified contact.</span></span> <span data-ttu-id="fa83f-118">Si le contact est trouvé, l’applet de passe tente de renvoyer ces informations à l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="fa83f-118">If that contact is found, the cmdlet will attempt to return that information to the local computer.</span></span> <span data-ttu-id="fa83f-119">Le test sera marqué comme succès uniquement si toutes ces étapes peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="fa83f-119">The test will be marked a success only if all those steps can be completed.</span></span>

<span data-ttu-id="fa83f-120">Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) .</span><span class="sxs-lookup"><span data-stu-id="fa83f-120">For more information, see the Help documentation for the [Test-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="fa83f-121">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="fa83f-121">Running the test</span></span>

<span data-ttu-id="fa83f-122">Vous pouvez exécuter l’applet de contrôle Test-CsAddressBookWebQuery à l’aide d’un compte de test préconfiguré (voir Configuration de comptes de test pour exécuter des tests Lync Server) ou du compte d’un utilisateur qui est activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fa83f-122">The Test-CsAddressBookWebQuery cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="fa83f-123">Pour effectuer cette vérification à l’aide d’un compte de test, vous devez simplement spécifier le nom de domaine complet (FQDN) du pool de serveurs Lync et l’adresse SIP de l’utilisateur agissant en tant que cible de la recherche.</span><span class="sxs-lookup"><span data-stu-id="fa83f-123">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool and the SIP address of the user acting as the target of the search.</span></span> <span data-ttu-id="fa83f-124">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="fa83f-124">For example:</span></span>

    Test-CsAddressBookWebQuery -TargetFqdn "atl-cs-001.litwareinc.com" -TargetSipAddress "sip:davidlongmire@litwareinc.com"

<span data-ttu-id="fa83f-125">Pour effectuer cette vérification à l’aide d’un compte d’utilisateur réel, vous devez créer un objet d’informations d’identification Windows PowerShell contenant un nom d’utilisateur et un mot de passe valides.</span><span class="sxs-lookup"><span data-stu-id="fa83f-125">To run this check using an actual user account, you must create a Windows PowerShell credentials object that contains a valid user name and password.</span></span> <span data-ttu-id="fa83f-126">Vous devez alors inclure cet objet Credential et l’adresse SIP attribuée au compte lorsque le code appelle test-CsAddressBookWebQuery :</span><span class="sxs-lookup"><span data-stu-id="fa83f-126">You must then include that credentials object and the SIP address assigned to the account when the code calls Test-CsAddressBookWebQuery:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsAddressBookWebQuery -TargetFqdn "atl-cs-001.litwareinc.com" -TargetSipAddress "sip:davidlongmire@litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="fa83f-127">Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) .</span><span class="sxs-lookup"><span data-stu-id="fa83f-127">For more information, see the Help documentation for the [Test-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="fa83f-128">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="fa83f-128">Determining success or failure</span></span>

<span data-ttu-id="fa83f-129">Si l’utilisateur spécifié peut se connecter au service de carnet d’adresses et récupérer l’adresse utilisateur ciblée, vous renverra une sortie similaire à celle-ci avec la propriété Result marquée comme réussie :</span><span class="sxs-lookup"><span data-stu-id="fa83f-129">If the specified user can connect to the Address Book Service and retrieve the targeted user address, you'll return output similar to this with the Result property marked as Success:</span></span>

<span data-ttu-id="fa83f-130">TargetUri https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="fa83f-130">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="fa83f-131">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="fa83f-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="fa83f-132">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="fa83f-132">Result : Success</span></span>

<span data-ttu-id="fa83f-133">Latence : 00:00:06.2611356</span><span class="sxs-lookup"><span data-stu-id="fa83f-133">Latency : 00:00:06.2611356</span></span>

<span data-ttu-id="fa83f-134">Error</span><span class="sxs-lookup"><span data-stu-id="fa83f-134">Error :</span></span>

<span data-ttu-id="fa83f-135">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="fa83f-135">Diagnosis :</span></span>

<span data-ttu-id="fa83f-136">Si l’utilisateur spécifié ne peut pas se connecter ou si l’adresse de l’utilisateur cible ne peut pas être récupérée, le résultat s’affichera en tant qu’échec et des informations supplémentaires seront enregistrées dans les propriétés d’erreur et de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="fa83f-136">If the specified user can't connect or if the target user address cannot be retrieved, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="fa83f-137">TargetUri https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="fa83f-137">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="fa83f-138">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="fa83f-138">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="fa83f-139">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="fa83f-139">Result : Failure</span></span>

<span data-ttu-id="fa83f-140">Latence : 00:00:00</span><span class="sxs-lookup"><span data-stu-id="fa83f-140">Latency : 00:00:00</span></span>

<span data-ttu-id="fa83f-141">Erreur : le service Web du carnet d’adresses a échoué avec le code de réponse</span><span class="sxs-lookup"><span data-stu-id="fa83f-141">Error : Address Book Web service request has failed with response code</span></span>

<span data-ttu-id="fa83f-142">NoEntryFound.</span><span class="sxs-lookup"><span data-stu-id="fa83f-142">NoEntryFound.</span></span>

<span data-ttu-id="fa83f-143">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="fa83f-143">Diagnosis :</span></span>

<span data-ttu-id="fa83f-144">La sortie précédente indique que le test a échoué car l’utilisateur cible est introuvable.</span><span class="sxs-lookup"><span data-stu-id="fa83f-144">The previous output states that the test failed because the target user couldn't be found.</span></span> <span data-ttu-id="fa83f-145">Vous pouvez déterminer si une adresse SIP valide a été transmise à Test-CsAddressBookWebQuery en exécutant une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="fa83f-145">You can determine whether or not a valid SIP address was passed to Test-CsAddressBookWebQuery by running a command similar to the following:</span></span>

    Get-CsUser | Where-Object {$_.SipAddress -eq "sip:davidlongmire@litwareinc.com"

<span data-ttu-id="fa83f-146">Si Test-CsAddressBookWebQuery échoue, il est possible que vous souhaitiez réexécuter le test, cette fois-ci, y compris le paramètre Verbose :</span><span class="sxs-lookup"><span data-stu-id="fa83f-146">If Test-CsAddressBookWebQuery fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsAddressBookWebQuery -TargetFqdn "atl-cs-001.litwareinc.com" -TargetSipAddress "sip:davidlongmire@litwareinc.com" -Verbose

<span data-ttu-id="fa83f-147">Lorsque le paramètre Verbose est inclus, Test-CsAddressBookWebQuery renvoie un compte étape par étape de chaque action effectuée lors de la vérification de la capacité de l’utilisateur spécifié à se connecter à Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fa83f-147">When the Verbose parameter is included, Test-CsAddressBookWebQuery will return a step-by-step account of each action it tried while checking the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="fa83f-148">Par exemple, cette sortie indique que Test-CsAddressBookWebQuery a pu se connecter au service de carnet d’adresses, mais qu’il n’a pas été en mesure de localiser l’adresse SIP cible :</span><span class="sxs-lookup"><span data-stu-id="fa83f-148">For example, this output indicates that Test-CsAddressBookWebQuery was able to connect to the Address Book Service, but was not able to locate the target SIP address:</span></span>

<span data-ttu-id="fa83f-149">Activité « QueryAddressBookWebService » démarrée.</span><span class="sxs-lookup"><span data-stu-id="fa83f-149">'QueryAddressBookWebService' activity started.</span></span>

<span data-ttu-id="fa83f-150">Appel au service de requête sur le Web du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="fa83f-150">Calling Address Book Web Query Service.</span></span> <span data-ttu-id="fa83f-151">URL ABWS =</span><span class="sxs-lookup"><span data-stu-id="fa83f-151">ABWS URL =</span></span>

https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc

<span data-ttu-id="fa83f-152">Exception de requête dans le carnet d’adresses : échec de la demande de service Web du carnet d’adresses avec le code de réponse NoEntryFound.</span><span class="sxs-lookup"><span data-stu-id="fa83f-152">Address book query exception : Address Book Web service request has failed with response code NoEntryFound.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="fa83f-153">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="fa83f-153">Reasons Why the Test Might Have Failed</span></span>

<span data-ttu-id="fa83f-154">Voici quelques raisons courantes pour lesquelles Test-CsAddressBookWebQuery risque d’échouer :</span><span class="sxs-lookup"><span data-stu-id="fa83f-154">Here are some common reasons why Test-CsAddressBookWebQuery might fail:</span></span>

  - <span data-ttu-id="fa83f-155">Vous avez spécifié un compte d’utilisateur non valide.</span><span class="sxs-lookup"><span data-stu-id="fa83f-155">You specified an invalid user account.</span></span> <span data-ttu-id="fa83f-156">Vous pouvez vérifier qu’un compte d’utilisateur existe en exécutant une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="fa83f-156">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="fa83f-157">Le compte d’utilisateur est valide, mais le compte n’est pas activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fa83f-157">The user account is valid, but the account is not currently enabled for Lync Server.</span></span> <span data-ttu-id="fa83f-158">Pour vérifier qu’un compte d’utilisateur a été activé pour Lync Server, exécutez une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="fa83f-158">To verify that a user account has been enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="fa83f-159">Si la propriété Enabled est définie sur false, cela signifie que l’utilisateur n’est pas actuellement activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fa83f-159">If the Enabled property is set to False that means that the user is not currently enabled for Lync Server.</span></span>

  - <span data-ttu-id="fa83f-160">L’utilisateur cible n’est peut-être pas dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="fa83f-160">The target user might not be in the Address Book.</span></span>

  - <span data-ttu-id="fa83f-161">Le carnet d’adresses n’a peut-être pas été entièrement mis à jour et répliqué.</span><span class="sxs-lookup"><span data-stu-id="fa83f-161">The Address Book might not have fully updated and replicated.</span></span> <span data-ttu-id="fa83f-162">Vous pouvez forcer la mise à jour de tous les serveurs du carnet d’adresses de votre organisation en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="fa83f-162">You can force an update of all the Address Book Servers in your organization by running the following command:</span></span>
    
        Update-CsAddressBook

<span data-ttu-id="fa83f-163"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fa83f-163"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

