---
title: 'Lync Server 2013 : validation de l’accès au carnet d’adresses'
description: 'Lync Server 2013 : validation de l’accès au carnet d’adresses.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating address book access
ms:assetid: 630682c6-9262-46c5-9af1-6193db70374b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720916(v=OCS.15)
ms:contentKeyID: 63969611
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6da08e48be24b3325bc1f415b9baa3c9197717c3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438630"
---
# <a name="validating-address-book-access-in-lync-server-2013"></a><span data-ttu-id="c0aaa-103">Validation de l’accès au carnet d’adresses dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0aaa-103">Validating address book access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c0aaa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c0aaa-104">

<span> </span></span></span>

<span data-ttu-id="c0aaa-105">_**Dernière modification de la rubrique :** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="c0aaa-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0aaa-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="c0aaa-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="c0aaa-107">Jour</span><span class="sxs-lookup"><span data-stu-id="c0aaa-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0aaa-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="c0aaa-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="c0aaa-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0aaa-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0aaa-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="c0aaa-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="c0aaa-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="c0aaa-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsAddressBookService.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsAddressBookService cmdlet.</span></span> <span data-ttu-id="c0aaa-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="c0aaa-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsAddressBookService&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="c0aaa-114">Description</span><span class="sxs-lookup"><span data-stu-id="c0aaa-114">Description</span></span>

<span data-ttu-id="c0aaa-115">L’applet de connexion Test-CsAddressBookService permet de vérifier que l’utilisateur peut se connecter au service Web de téléchargement du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-115">The Test-CsAddressBookService cmdlet provides a way for you to verify that a user can connect to the Address Book Download Web service.</span></span> <span data-ttu-id="c0aaa-116">Lorsque vous exécutez l’applet de requête, Test-CsAddressBookService se connecte au service Web de téléchargement du carnet d’adresses sur le pool spécifié et demande l’emplacement des fichiers du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-116">When you run the cmdlet, Test-CsAddressBookService connects to the Address Book Download Web service on the specified pool and requests the location of the Address Book files.</span></span> <span data-ttu-id="c0aaa-117">Si le service Web de téléchargement de carnet d’adresses fournit cet emplacement, le test est considéré comme réussi.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-117">If the Address Book Download Web service supplies that location, the test is considered successful.</span></span> <span data-ttu-id="c0aaa-118">Si la requête est refusée, le test est considéré comme un échec.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-118">If the request is denied, then the test is considered a failure.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="c0aaa-119">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="c0aaa-119">Running the test</span></span>

<span data-ttu-id="c0aaa-120">Vous pouvez exécuter l’applet de contrôle Test-CsAddressBookService à l’aide d’un compte de test préconfiguré (voir Configuration de comptes de test pour exécuter des tests Lync Server) ou du compte d’un utilisateur qui a été activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-120">The Test-CsAddressBookService cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who has been enabled for Lync Server.</span></span> <span data-ttu-id="c0aaa-121">Pour exécuter cette recherche à l’aide d’un compte de test, il vous suffit de spécifier le nom de domaine complet (FQDN) du pool de serveurs Lync testé.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-121">To run this check using a test account, all you need to do is specify the fully qualified domain name (FQDN) of the Lync Server pool being tested.</span></span> <span data-ttu-id="c0aaa-122">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="c0aaa-122">For example:</span></span>

    Test-CsAddressBookService -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="c0aaa-123">Pour effectuer cette vérification à l’aide d’un compte d’utilisateur réel, vous devez d’abord créer un objet d’informations d’identification Windows PowerShell contenant le nom et le mot de passe du compte.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-123">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="c0aaa-124">Vous devez alors inclure cet objet Credential et l’adresse SIP attribuée au compte lors de l’appel de test-CsAddressBookService :</span><span class="sxs-lookup"><span data-stu-id="c0aaa-124">You must then include that credentials object and the SIP address assigned to the account when calling Test-CsAddressBookService:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsAddressBookService -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="c0aaa-125">Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsAddressBookService](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookService) .</span><span class="sxs-lookup"><span data-stu-id="c0aaa-125">For more information, see the Help documentation for the [Test-CsAddressBookService](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookService) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="c0aaa-126">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="c0aaa-126">Determining success or failure</span></span>

<span data-ttu-id="c0aaa-127">Si l’utilisateur spécifié est en mesure de se connecter au service de carnet d’adresses, vous obtiendrez une sortie similaire à celle-ci, avec la propriété Result marquée comme **réussie**:</span><span class="sxs-lookup"><span data-stu-id="c0aaa-127">If the specified user is able to connect to the Address Book Service you will get back output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="c0aaa-128">TargetUri https://lync-se.fabrikam.com:443/abs/handler</span><span class="sxs-lookup"><span data-stu-id="c0aaa-128">TargetUri : https://lync-se.fabrikam.com:443/abs/handler</span></span>

<span data-ttu-id="c0aaa-129">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c0aaa-129">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="c0aaa-130">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="c0aaa-130">Result : Success</span></span>

<span data-ttu-id="c0aaa-131">Latence : 00:00:06.2260399</span><span class="sxs-lookup"><span data-stu-id="c0aaa-131">Latency : 00:00:06.2260399</span></span>

<span data-ttu-id="c0aaa-132">Error</span><span class="sxs-lookup"><span data-stu-id="c0aaa-132">Error :</span></span>

<span data-ttu-id="c0aaa-133">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="c0aaa-133">Diagnosis :</span></span>

<span data-ttu-id="c0aaa-134">Si l’utilisateur spécifié ne peut pas établir cette connexion, le résultat est affiché en tant qu’échec et des informations supplémentaires sont enregistrées dans les propriétés d’erreur et de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="c0aaa-134">If the specified user is not able to make this connection, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="c0aaa-135">TargetUri</span><span class="sxs-lookup"><span data-stu-id="c0aaa-135">TargetUri :</span></span>

<span data-ttu-id="c0aaa-136">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c0aaa-136">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="c0aaa-137">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="c0aaa-137">Result : Failure</span></span>

<span data-ttu-id="c0aaa-138">Latence : 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c0aaa-138">Latency : 00:00:00</span></span>

<span data-ttu-id="c0aaa-139">Diagnostic : codeerreur = 4005, source = ATL-CS-001.litwareinc.com,</span><span class="sxs-lookup"><span data-stu-id="c0aaa-139">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="c0aaa-140">Raison = URI de destination non activé pour le SIP ou non</span><span class="sxs-lookup"><span data-stu-id="c0aaa-140">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="c0aaa-141">Il.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-141">exist.</span></span>

<span data-ttu-id="c0aaa-142">Microsoft. RTC. signalisation. DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="c0aaa-142">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="c0aaa-143">Par exemple, la sortie précédente indique qu’un test a échoué, car l’utilisateur spécifié (autrement dit, l’URI de destination) n’existe pas ou n’a pas été activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-143">For example, the preceding output states that the test failed because the specified user (that is, the “Destination URI”) either does not exist or has not been enabled for Lync Server.</span></span> <span data-ttu-id="c0aaa-144">Vous pouvez vérifier qu’un compte d’utilisateur est valide ou non et que vous avez fourni l’adresse SIP correcte en exécutant une commande semblable à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="c0aaa-144">You can verify whether or not a user account is valid, and verify that you supplied the correct SIP address, by running a command like this one:</span></span>

<span data-ttu-id="c0aaa-145">Get-CsUser-identité « sip :kenmyer@litwareinc.com » | Select-Object SipAddress activé</span><span class="sxs-lookup"><span data-stu-id="c0aaa-145">Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, Enabled</span></span>

<span data-ttu-id="c0aaa-146">Si Test-CsAddressBookService échoue, vous souhaiterez peut-être réexécuter le test, cette fois-ci, y compris le paramètre Verbose :</span><span class="sxs-lookup"><span data-stu-id="c0aaa-146">If Test-CsAddressBookService fails then you might want to rerun the test, this time including the Verbose parameter:</span></span>

<span data-ttu-id="c0aaa-147">Test-CsAddressBookService-TargetFqdn "atl-cs-001.litwareinc.com"-détails</span><span class="sxs-lookup"><span data-stu-id="c0aaa-147">Test-CsAddressBookService -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose</span></span>

<span data-ttu-id="c0aaa-148">Lorsque le paramètre Verbose est inclus Test-CsAddressBookService renvoie un compte étape par étape de chaque action lancée lors de la vérification de la capacité de l’utilisateur à se connecter à Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-148">When the Verbose parameter is included Test-CsAddressBookService will return a step-by-step account of each action it attempted when checking the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="c0aaa-149">Par exemple, cet exemple de sortie montre que test-CsAddressBookService, au moins dans cet exemple, a pu télécharger le fichier du carnet d’adresses :</span><span class="sxs-lookup"><span data-stu-id="c0aaa-149">For example, this sample output shows that Test-CsAddressBookService, at least in this example, was able to download the Address Book file:</span></span>

<span data-ttu-id="c0aaa-150">Envoi de la requête HTTP GET.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-150">Sending Http GET Request.</span></span>

<span data-ttu-id="c0aaa-151">Chemin d’accès du fichier = https://atl-cs-001.litwareinc.com:443/abs/handler/f-1299.lsabs</span><span class="sxs-lookup"><span data-stu-id="c0aaa-151">File Path = https://atl-cs-001.litwareinc.com:443/abs/handler/f-1299.lsabs</span></span>

<span data-ttu-id="c0aaa-152">Tentative de numérotation = 1</span><span class="sxs-lookup"><span data-stu-id="c0aaa-152">Attempt Number = 1</span></span>

<span data-ttu-id="c0aaa-153">Délai d’expiration (MS) = 60000</span><span class="sxs-lookup"><span data-stu-id="c0aaa-153">TimeOut (msec) = 60000</span></span>

<span data-ttu-id="c0aaa-154">Téléchargement du fichier ABS réussi https://atl-cs-001.litwareinc.com:443/abs/handler/f-1299.lsabs</span><span class="sxs-lookup"><span data-stu-id="c0aaa-154">Successfully Downloaded the ABS file https://atl-cs-001.litwareinc.com:443/abs/handler/f-1299.lsabs</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="c0aaa-155">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="c0aaa-155">Reasons why the test might have failed</span></span>

<span data-ttu-id="c0aaa-156">Voici quelques raisons courantes pour lesquelles Test-CsAddressBookService risque d’échouer :</span><span class="sxs-lookup"><span data-stu-id="c0aaa-156">Here are some common reasons why Test-CsAddressBookService might fail:</span></span>

  - <span data-ttu-id="c0aaa-157">Vous avez spécifié un compte d’utilisateur non valide.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-157">You specified an invalid user account.</span></span> <span data-ttu-id="c0aaa-158">Vous pouvez vérifier qu’un compte d’utilisateur existe en exécutant une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="c0aaa-158">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="c0aaa-159">Le compte d’utilisateur est valide, mais le compte n’est pas activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-159">The user account is valid, but the account is not currently enabled for Lync Server.</span></span> <span data-ttu-id="c0aaa-160">Pour vérifier qu’un compte d’utilisateur a été activé pour Lync Server, exécutez une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="c0aaa-160">To verify that a user account has been enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="c0aaa-161">Si la propriété Enabled est définie sur false, cela signifie que l’utilisateur n’est pas actuellement activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c0aaa-161">If the Enabled property is set to False that means that the user is not currently enabled for Lync Server.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c0aaa-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0aaa-162">See Also</span></span>


[<span data-ttu-id="c0aaa-163">Test-CsAddressBookService</span><span class="sxs-lookup"><span data-stu-id="c0aaa-163">Test-CsAddressBookService</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookService)  
  

<span data-ttu-id="c0aaa-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c0aaa-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

