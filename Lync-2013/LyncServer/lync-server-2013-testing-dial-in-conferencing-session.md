---
title: 'Lync Server 2013 : test de la session de conférence rendez-vous'
description: 'Lync Server 2013 : test de la session de conférence rendez-vous.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing dial-in conferencing session
ms:assetid: 6c505be5-5af7-450c-b3ca-10d9122bee5c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743834(v=OCS.15)
ms:contentKeyID: 63969613
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4d0c51b16df674dbf8bf7f0a2c6c4c93c2606d95
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394509"
---
# <a name="testing-dial-in-conferencing-session-in-lync-server-2013"></a><span data-ttu-id="6c483-103">Test de la session de conférence rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c483-103">Testing dial-in conferencing session in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6c483-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6c483-104">

<span> </span></span></span>

<span data-ttu-id="6c483-105">_**Dernière modification de la rubrique :** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="6c483-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c483-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="6c483-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="6c483-107">Jour</span><span class="sxs-lookup"><span data-stu-id="6c483-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c483-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="6c483-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="6c483-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6c483-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c483-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="6c483-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="6c483-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="6c483-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="6c483-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsDialInConferencing.</span><span class="sxs-lookup"><span data-stu-id="6c483-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsDialInConferencing cmdlet.</span></span> <span data-ttu-id="6c483-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="6c483-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsDialInConferencing&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="6c483-114">Description</span><span class="sxs-lookup"><span data-stu-id="6c483-114">Description</span></span>

<span data-ttu-id="6c483-115">L’applet de connexion Test-CsDialInConferencing vérifie si un utilisateur peut participer à une conférence rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="6c483-115">The Test-CsDialInConferencing cmdlet verifies whether a user can participate in a dial-in conference.</span></span> <span data-ttu-id="6c483-116">Test-CsDialInConferencing fonctionne en essayant de consigner un utilisateur de test sur le système.</span><span class="sxs-lookup"><span data-stu-id="6c483-116">Test-CsDialInConferencing works by trying to log a test user onto the system.</span></span> <span data-ttu-id="6c483-117">En cas de réussite de l’ouverture de session, l’applet de connexion utilise les informations d’identification et les autorisations de l’utilisateur pour essayer tous les numéros d’accès à la Conférence rendez-vous disponibles.</span><span class="sxs-lookup"><span data-stu-id="6c483-117">If the logon succeeds, the cmdlet will then use the user’s credentials and permissions to try all of the available dial-in conferencing access numbers.</span></span> <span data-ttu-id="6c483-118">Le succès ou l’échec de chaque tentative de connexion est noté, l’utilisateur de test sera déconnecté de Lync Server. test-CsDialInConferencing vérifie uniquement que les connexions appropriées peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="6c483-118">The success or failure of each dial-in try will be noted, then the test user will be logged off from Lync Server.Test-CsDialInConferencing only verifies that the appropriate connections can be made.</span></span> <span data-ttu-id="6c483-119">L’applet de connexion n’effectue aucun appel téléphonique ou ne crée pas de conférences rendez-vous que d’autres utilisateurs peuvent rejoindre.</span><span class="sxs-lookup"><span data-stu-id="6c483-119">The cmdlet does not actually make any phone calls or create any dial-in conferences that other users can join.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="6c483-120">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="6c483-120">Running the test</span></span>

<span data-ttu-id="6c483-121">Vous pouvez exécuter l’applet de contrôle Test-CsDialInConferencing à l’aide d’un compte de test préconfiguré (voir Configuration de comptes de test pour exécuter des tests Lync Server) ou du compte d’un utilisateur qui est activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6c483-121">The Test-CsDialInConferencing cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="6c483-122">Pour effectuer cette vérification à l’aide d’un compte de test, vous devez simplement spécifier le nom de domaine complet (FQDN) du pool de serveurs Lync testé.</span><span class="sxs-lookup"><span data-stu-id="6c483-122">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="6c483-123">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="6c483-123">For example:</span></span>

    Test-CsDialInConferencing -TargetFqdn "atl-cs-001.litwareinc.com" 

<span data-ttu-id="6c483-124">Pour effectuer cette vérification à l’aide d’un compte d’utilisateur réel, vous devez créer un objet d’informations d’identification Windows PowerShell contenant le nom et le mot de passe du compte.</span><span class="sxs-lookup"><span data-stu-id="6c483-124">To run this check using an actual user account, you must create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="6c483-125">Vous devez alors inclure cet objet Credential et le protocole SIP correspondant à l’appel de test-CsDialInConferencing :</span><span class="sxs-lookup"><span data-stu-id="6c483-125">You must then include that credentials object and the account SIP address the calling Test-CsDialInConferencing:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsDialInConferencing -TargetFqdn atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="6c483-126">Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsDialInConferencing](https://docs.microsoft.com/powershell/module/skype/Test-CsDialInConferencing) .</span><span class="sxs-lookup"><span data-stu-id="6c483-126">For more information, see the Help documentation for the [Test-CsDialInConferencing](https://docs.microsoft.com/powershell/module/skype/Test-CsDialInConferencing) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="6c483-127">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="6c483-127">Determining success or failure</span></span>

<span data-ttu-id="6c483-128">Si l’utilisateur spécifié peut se connecter à Lync Server et établir une connexion à l’aide de l’un des numéros d’accès pour les conférences rendez-vous disponibles, vous recevrez une sortie similaire à celle-ci, avec la propriété Result marquée comme **réussie :**</span><span class="sxs-lookup"><span data-stu-id="6c483-128">If the specified user can log on to Lync Server and then make a connection using one of the available dial-in conferencing access numbers, then you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="6c483-129">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="6c483-129">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="6c483-130">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="6c483-130">Result : Success</span></span>

<span data-ttu-id="6c483-131">Latence : 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="6c483-131">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="6c483-132">Error</span><span class="sxs-lookup"><span data-stu-id="6c483-132">Error :</span></span>

<span data-ttu-id="6c483-133">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="6c483-133">Diagnosis :</span></span>

<span data-ttu-id="6c483-134">Si l’utilisateur spécifié ne peut pas établir cette connexion, le résultat s’affichera en panne et des informations supplémentaires seront enregistrées dans les propriétés d’erreur et de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="6c483-134">If the specified user can't make this connection, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="6c483-135">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="6c483-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="6c483-136">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="6c483-136">Result : Failure</span></span>

<span data-ttu-id="6c483-137">Latence : 00:00:00</span><span class="sxs-lookup"><span data-stu-id="6c483-137">Latency : 00:00:00</span></span>

<span data-ttu-id="6c483-138">Erreur : la connexion a été refusée.</span><span class="sxs-lookup"><span data-stu-id="6c483-138">Error : The log on was denied.</span></span> <span data-ttu-id="6c483-139">Vérifiez que les informations d’identification appropriées sont</span><span class="sxs-lookup"><span data-stu-id="6c483-139">Check that the proper credentials are</span></span>

<span data-ttu-id="6c483-140">utilisé et le compte est actif.</span><span class="sxs-lookup"><span data-stu-id="6c483-140">being used and the account is active.</span></span>

<span data-ttu-id="6c483-141">Exception interne : NegotiateSecurityAssociation a échoué, erreur :-</span><span class="sxs-lookup"><span data-stu-id="6c483-141">Inner Exception:NegotiateSecurityAssociation failed, error: -</span></span>

<span data-ttu-id="6c483-142">2146893044</span><span class="sxs-lookup"><span data-stu-id="6c483-142">2146893044</span></span>

<span data-ttu-id="6c483-143">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="6c483-143">Diagnosis :</span></span>

<span data-ttu-id="6c483-144">La sortie précédente indique que l’utilisateur de test a été refusé d’accéder au serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="6c483-144">The previous output indicates that the test user was denied access to Lync Server itself.</span></span> <span data-ttu-id="6c483-145">En règle générale, cela signifie que les informations d’identification de l’utilisateur transmises à Test-CsDialInConferencing n’étaient pas valides.</span><span class="sxs-lookup"><span data-stu-id="6c483-145">This typically means that the user credentials passed to Test-CsDialInConferencing were not valid.</span></span> <span data-ttu-id="6c483-146">Ensuite, vous devez recréer l’objet des informations d’identification Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6c483-146">In turn, you should re-create the Windows PowerShell credentials object.</span></span> <span data-ttu-id="6c483-147">Même si vous pouvez récupérer le mot de passe du compte d’utilisateur, vous pouvez vérifier l’adresse SIP à l’aide d’une commande similaire à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="6c483-147">Although you can retrieve the password for the user account, you can verify the SIP address by using a command similar to this:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="6c483-148">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="6c483-148">Reasons why the test might have failed</span></span>

<span data-ttu-id="6c483-149">Voici quelques raisons courantes pour lesquelles Test-CsDialInConferencing risque d’échouer :</span><span class="sxs-lookup"><span data-stu-id="6c483-149">Here are some common reasons why Test-CsDialInConferencing might fail:</span></span>

  - <span data-ttu-id="6c483-150">Vous avez spécifié un compte d’utilisateur qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6c483-150">You specified a user account that is not valid.</span></span> <span data-ttu-id="6c483-151">Vous pouvez vérifier qu’un compte d’utilisateur existe en exécutant une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="6c483-151">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="6c483-152">Le compte d’utilisateur est valide, mais le compte n’est pas activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6c483-152">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="6c483-153">Pour vérifier qu’un compte d’utilisateur est activé pour Lync Server, exécutez une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="6c483-153">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="6c483-154">Si la propriété Enabled est définie sur false, cela signifie que l’utilisateur n’est actuellement pas activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6c483-154">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="6c483-155">Vous avez peut-être un numéro d’accès à une conférence rendez-vous incorrect.</span><span class="sxs-lookup"><span data-stu-id="6c483-155">You might have an incorrect dial-in conferencing access number.</span></span> <span data-ttu-id="6c483-156">Vous pouvez revenir à la liste actuelle des numéros d’accès aux conférences rendez-vous à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="6c483-156">You can return your currently-configured list of dial-in conferencing access numbers by using this command:</span></span>
    
        Get-CsDialConferencingAccessNumber

<span data-ttu-id="6c483-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6c483-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

