---
title: 'Lync Server 2013 : le test de la fonctionnalité de messagerie instantanée de groupe'
description: 'Lync Server 2013 : possibilité de test de faire des conversations de groupe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to do group IM
ms:assetid: ca5545bc-51ac-490f-b96b-917bb742ad04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743839(v=OCS.15)
ms:contentKeyID: 63969652
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f6988a0c1a7ba569f7b4da098ae741beab5e14fa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441101"
---
# <a name="testing-ability-to-do-group-im-in-lync-server-2013"></a><span data-ttu-id="b2669-103">Possibilité de test de faire des conversations de groupe dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b2669-103">Testing ability to do group IM in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b2669-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b2669-104">

<span> </span></span></span>

<span data-ttu-id="b2669-105">_**Dernière modification de la rubrique :** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="b2669-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2669-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="b2669-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="b2669-107">Jour</span><span class="sxs-lookup"><span data-stu-id="b2669-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2669-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="b2669-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="b2669-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b2669-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2669-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="b2669-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="b2669-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="b2669-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="b2669-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsGroupIM.</span><span class="sxs-lookup"><span data-stu-id="b2669-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsGroupIM cmdlet.</span></span> <span data-ttu-id="b2669-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="b2669-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsGroupIM&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="b2669-114">Description</span><span class="sxs-lookup"><span data-stu-id="b2669-114">Description</span></span>

<span data-ttu-id="b2669-115">Le cmdlet Test-CsGroupIM vérifie que les utilisateurs de votre organisation peuvent animer des sessions de messagerie instantanée de groupe.</span><span class="sxs-lookup"><span data-stu-id="b2669-115">The Test-CsGroupIM cmdlet verifies that users in your organization can conduct group instant messaging sessions.</span></span> <span data-ttu-id="b2669-116">Lorsque vous exécutez test-CsGroupIM, l’applet de connexion tente de se connecter à un couple d’utilisateurs de test sur Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b2669-116">When you run Test-CsGroupIM, the cmdlet attempts to sign in a pair of test users to Lync Server.</span></span> <span data-ttu-id="b2669-117">En cas de succès, Test-CsGroupIM crée une nouvelle conférence à l’aide du premier utilisateur test, puis invite le second utilisateur à rejoindre la Conférence.</span><span class="sxs-lookup"><span data-stu-id="b2669-117">If successful, Test-CsGroupIM creates a new conference using the first test user, then invites the second user to join the conference.</span></span> <span data-ttu-id="b2669-118">Après un échange de messages, les deux utilisateurs sont alors déconnectés du système.</span><span class="sxs-lookup"><span data-stu-id="b2669-118">After an exchange of messages, both users are then disconnected from the system.</span></span> <span data-ttu-id="b2669-119">Notez que tout cela se produit sans aucune interaction utilisateur, sans affecter les utilisateurs réels.</span><span class="sxs-lookup"><span data-stu-id="b2669-119">Note that all of this happens without any user interaction, and without affecting any actual users.</span></span> <span data-ttu-id="b2669-120">Par exemple, supposons que le compte de test sip :kenmyer@litwareinc.com correspond à un utilisateur réel possédant un compte de serveur Lync réel.</span><span class="sxs-lookup"><span data-stu-id="b2669-120">For example, suppose that the test account sip:kenmyer@litwareinc.com corresponds to a real user who has a real Lync Server account.</span></span> <span data-ttu-id="b2669-121">Dans ce cas, le test sera mené sans interruption pour le véritable Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="b2669-121">In that case, the test will be conducted without any disruption to the real Ken Myer.</span></span> <span data-ttu-id="b2669-122">Par exemple, même lorsque le compte de test Ken Myer se déconnecte du système, Ken Myer la personne reste connectée.</span><span class="sxs-lookup"><span data-stu-id="b2669-122">For example, even when the Ken Myer test account logs off from the system, Ken Myer the person will remain logged on.</span></span> <span data-ttu-id="b2669-123">De même, le véritable Ken Myer ne recevra pas d’invitation à rejoindre la Conférence.</span><span class="sxs-lookup"><span data-stu-id="b2669-123">Likewise, the real Ken Myer won't receive an invitation to join the conference.</span></span> <span data-ttu-id="b2669-124">Cette invitation sera envoyée au compte de test et acceptée par celle-ci.</span><span class="sxs-lookup"><span data-stu-id="b2669-124">That invitation will be sent to, and accepted by, the test account.</span></span>

<span data-ttu-id="b2669-125">Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) .</span><span class="sxs-lookup"><span data-stu-id="b2669-125">For more information, see the Help documentation for the [Test-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="b2669-126">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="b2669-126">Running the test</span></span>

<span data-ttu-id="b2669-127">Vous pouvez exécuter l’applet de cmdlet Test-CsGroupIM à l’aide d’une paire de comptes de test préconfigurés (voir Configuration de comptes de test pour exécuter des tests Lync Server) ou les comptes de tous les utilisateurs qui sont activés pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b2669-127">The Test-CsGroupIM cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="b2669-128">Pour exécuter cette vérification à l’aide de comptes de test, vous devez simplement spécifier le nom de domaine complet (FQDN) du pool de serveurs Lync testé.</span><span class="sxs-lookup"><span data-stu-id="b2669-128">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="b2669-129">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b2669-129">For example:</span></span>

    Test-CsGroupIM -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="b2669-130">Pour exécuter cette vérification à l’aide de comptes d’utilisateurs réels, vous devez créer deux objets d’informations d’identification Lync Server Management Shell (objets contenant le nom de compte et le mot de passe) pour chaque compte.</span><span class="sxs-lookup"><span data-stu-id="b2669-130">To run this check using actual user accounts, you must create two Lync Server Management Shell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="b2669-131">Vous devez alors inclure ces objets d’informations d’identification et les adresses SIP des deux comptes lors de l’appel de test-CsGroupIM :</span><span class="sxs-lookup"><span data-stu-id="b2669-131">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsGroupIM:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsGroupIm -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

<span data-ttu-id="b2669-132">Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) .</span><span class="sxs-lookup"><span data-stu-id="b2669-132">For more information, see the Help documentation for the [Test-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="b2669-133">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="b2669-133">Determining Success or Failure</span></span>

<span data-ttu-id="b2669-134">Si les deux utilisateurs peuvent terminer une session de messagerie instantanée de groupe, vous recevrez une sortie similaire à celle-ci avec la propriété Result marquée comme **réussie :**</span><span class="sxs-lookup"><span data-stu-id="b2669-134">If the two users can complete a group instant messaging session, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="b2669-135">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="b2669-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="b2669-136">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="b2669-136">Result : Success</span></span>

<span data-ttu-id="b2669-137">Latence : 00:00:06.3812203</span><span class="sxs-lookup"><span data-stu-id="b2669-137">Latency : 00:00:06.3812203</span></span>

<span data-ttu-id="b2669-138">Error</span><span class="sxs-lookup"><span data-stu-id="b2669-138">Error :</span></span>

<span data-ttu-id="b2669-139">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="b2669-139">Diagnosis :</span></span>

<span data-ttu-id="b2669-140">Si les deux utilisateurs ne peuvent pas mettre fin à la session de messagerie instantanée, le résultat s’affichera en panne et des informations supplémentaires seront enregistrées dans les propriétés d’erreur et de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="b2669-140">If the two users can't able to complete the instant messaging session, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="b2669-141">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="b2669-141">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="b2669-142">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="b2669-142">Result : Failure</span></span>

<span data-ttu-id="b2669-143">Latence : 00:00:00</span><span class="sxs-lookup"><span data-stu-id="b2669-143">Latency : 00:00:00</span></span>

<span data-ttu-id="b2669-144">Erreur : 404, introuvable</span><span class="sxs-lookup"><span data-stu-id="b2669-144">Error : 404, Not Found</span></span>

<span data-ttu-id="b2669-145">Diagnostic : codeerreur = 4005, source = ATL-CS-001.litwareinc.com,</span><span class="sxs-lookup"><span data-stu-id="b2669-145">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="b2669-146">Raison = URI de destination non activé pour le SIP ou non</span><span class="sxs-lookup"><span data-stu-id="b2669-146">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="b2669-147">Il.</span><span class="sxs-lookup"><span data-stu-id="b2669-147">exist.</span></span>

<span data-ttu-id="b2669-148">Microsoft. RTC. signalisation. DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="b2669-148">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="b2669-149">La sortie précédente indique que le test a échoué car au moins un des comptes de test n’est pas valide, car le compte n’existe pas ou parce que l’utilisateur n’a pas été activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b2669-149">The previous output states that the test failed because at least one of the test accounts was not valid, either because the account does not exist or because the user has not been enabled for Lync Server.</span></span> <span data-ttu-id="b2669-150">Vous pouvez vérifier que le compte existe et que le compte a été activé pour nm-OCS-14-3e en exécutant une commande similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b2669-150">You can verify the account exists, and whether or not the account has been enabled for nm-ocs-14-3rd by running a command similar to this:</span></span>

    "Ken Myer", "David Longmire" | Get-CsUser | Select-Object SipAddress, Enabled

<span data-ttu-id="b2669-151">Si Test-CsGroupIM échoue, il est possible que vous souhaitiez réexécuter le test, cette fois-ci, y compris le paramètre Verbose :</span><span class="sxs-lookup"><span data-stu-id="b2669-151">If Test-CsGroupIM fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsGroupIM -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="b2669-152">Lorsque le paramètre Verbose est inclus, Test-CsGroupIM renvoie un compte étape par étape de chaque action qu’il a effectuée lors de la vérification de la capacité des utilisateurs spécifiés à participer à une session de messagerie instantanée de groupe.</span><span class="sxs-lookup"><span data-stu-id="b2669-152">When the Verbose parameter is included, Test-CsGroupIM will return a step-by-step account of each action it tried when it checked the ability of the specified users to participate in a group instant messaging sessions.</span></span> <span data-ttu-id="b2669-153">Par exemple, si vous constatez qu’un ou plusieurs comptes d’utilisateur ne sont pas valides, vous pouvez réexécuter le test en utilisant le paramètre Verbose et déterminer le compte d’utilisateur qui n’est pas valide :</span><span class="sxs-lookup"><span data-stu-id="b2669-153">For example, if your test fails and you are told that one or more of the user accounts is not valid, you can rerun the test using the Verbose parameter and determine which user account is not valid:</span></span>

<span data-ttu-id="b2669-154">Envoi de la demande d’inscription :</span><span class="sxs-lookup"><span data-stu-id="b2669-154">Sending Registration request:</span></span>

 <span data-ttu-id="b2669-155">Nom de domaine complet cible = atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="b2669-155">Target Fqdn      = atl-cs-001.litwareinc.com</span></span>

 <span data-ttu-id="b2669-156">Adresse SIP de l’utilisateur = sip :kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="b2669-156">User SIP Address = sip:kenmyer@litwareinc.com</span></span>

 <span data-ttu-id="b2669-157">Register port = 5061</span><span class="sxs-lookup"><span data-stu-id="b2669-157">Register Port    = 5061</span></span>

<span data-ttu-id="b2669-158">Le type d’authentification « IWA » est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b2669-158">Auth type 'IWA' is selected.</span></span>

<span data-ttu-id="b2669-159">Une exception’la connexion a été refusée.</span><span class="sxs-lookup"><span data-stu-id="b2669-159">An exception 'The log on was denied.</span></span> <span data-ttu-id="b2669-160">Vérifiez que les informations d’identification correctes sont utilisées et que le compte est actif'</span><span class="sxs-lookup"><span data-stu-id="b2669-160">Check that the correct credentials are being used and the account is active'</span></span>

<span data-ttu-id="b2669-161">Comme vous pouvez le voir dans cet exemple, l’utilisateur qui dispose de l’adresse SIP sip :kenmyer@litwareinc.com n’a pas réussi à se connecter.</span><span class="sxs-lookup"><span data-stu-id="b2669-161">As you can see, in this example the user who has the SIP address sip:kenmyer@litwareinc.com was not able to log on.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="b2669-162">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="b2669-162">Reasons why the test might have failed</span></span>

<span data-ttu-id="b2669-163">Voici quelques raisons courantes pour lesquelles Test-CsGroupIM risque d’échouer :</span><span class="sxs-lookup"><span data-stu-id="b2669-163">Here are some common reasons why Test-CsGroupIM might fail:</span></span>

  - <span data-ttu-id="b2669-164">Vous avez spécifié un compte d’utilisateur incorrect.</span><span class="sxs-lookup"><span data-stu-id="b2669-164">You specified an incorrect user account.</span></span> <span data-ttu-id="b2669-165">Vous pouvez vérifier qu’un compte d’utilisateur existe en exécutant une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b2669-165">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="b2669-166">Le compte d’utilisateur est valide, mais le compte n’est pas activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b2669-166">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="b2669-167">Pour vérifier qu’un compte d’utilisateur a été activé pour Lync Server, exécutez une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b2669-167">To verify that a user account was enabled for Lync Server, run a command similar to the following:</span></span>
    
    <span data-ttu-id="b2669-168">Get-CsUser « sip :kenmyer@litwareinc.com » | Select-Object activé</span><span class="sxs-lookup"><span data-stu-id="b2669-168">Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled</span></span>
    
    <span data-ttu-id="b2669-169">Si la propriété Enabled est définie sur false, cela signifie que l’utilisateur n’est actuellement pas activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b2669-169">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="b2669-170">Le service de messagerie instantanée n’est peut-être pas disponible.</span><span class="sxs-lookup"><span data-stu-id="b2669-170">The instant messaging service might not be available.</span></span> <span data-ttu-id="b2669-171">Lync Server vous permet de configurer le système de sorte que la messagerie instantanée ne soit pas disponible si vous n’êtes pas en mesure d’accéder à la base de données d’archivage.</span><span class="sxs-lookup"><span data-stu-id="b2669-171">With Lync Server, you can configure the system so that instant messaging is not available if the archiving database cannot be accessed.</span></span> <span data-ttu-id="b2669-172">Vous pouvez vérifier qu’en exécutant une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b2669-172">You can verify that by running a command similar to the following:</span></span>
    
        Get-CsArchivingConfiguration -Identity "atl-cs-001.litwareinc.com" | Select-Object BlockOnArchiveFailure
    
    <span data-ttu-id="b2669-173">Si BlockOnArchiveFailure est défini sur true, vous devez déterminer si la base de données d’archivage est disponible ou non.</span><span class="sxs-lookup"><span data-stu-id="b2669-173">If BlockOnArchiveFailure is set to True, then you should determine whether or not the archiving database is available.</span></span> <span data-ttu-id="b2669-174">Vous pouvez renvoyer les emplacements de vos bases de données d’archivage à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b2669-174">You can return the locations of your archiving databases by using the following command:</span></span>
    
        Get-CsService -ArchivingDatabase

  - <span data-ttu-id="b2669-175">Le serveur d’archivage n’est peut-être pas disponible.</span><span class="sxs-lookup"><span data-stu-id="b2669-175">The Archiving Server might not be available.</span></span> <span data-ttu-id="b2669-176">Vous pouvez récupérer le nom de domaine complet (FQDN) de vos serveurs d’archivage à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b2669-176">You can retrieve the FQDN of your Archiving Servers by using this command:</span></span>
    
        Get-CsService -ArchivingServer
    
    <span data-ttu-id="b2669-177">Vous pouvez ensuite exécuter une commande ping sur le serveur approprié pour vérifier qu’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="b2669-177">You can then ping the appropriate server to verify that it is available.</span></span> <span data-ttu-id="b2669-178">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b2669-178">For example:</span></span>
    
        ping atl-archiving-001.litwareinc.com

<span data-ttu-id="b2669-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b2669-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

