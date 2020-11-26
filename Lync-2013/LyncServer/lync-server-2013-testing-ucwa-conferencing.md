---
title: 'Lync Server 2013 : test des conférences UCWA'
description: 'Lync Server 2013 : test des conférences UCWA.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing UCWA conferencing
ms:assetid: 62b3866a-0759-4b1f-99ec-5a68d6a74f00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727306(v=OCS.15)
ms:contentKeyID: 63969610
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37f88a683abb67d55211422fc4dcf45fc1d5c966
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439736"
---
# <a name="testing-ucwa-conferencing-in-lync-server-2013"></a><span data-ttu-id="0d9ff-103">Test de la Conférence UCWA dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0d9ff-103">Testing UCWA conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0d9ff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0d9ff-104">

<span> </span></span></span>

<span data-ttu-id="0d9ff-105">_**Dernière modification de la rubrique :** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="0d9ff-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d9ff-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="0d9ff-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="0d9ff-107">Jour</span><span class="sxs-lookup"><span data-stu-id="0d9ff-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d9ff-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="0d9ff-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="0d9ff-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0d9ff-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d9ff-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="0d9ff-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="0d9ff-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="0d9ff-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande <strong>test-CsUcwaConference</strong> .</span><span class="sxs-lookup"><span data-stu-id="0d9ff-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsUcwaConference</strong> cmdlet.</span></span> <span data-ttu-id="0d9ff-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="0d9ff-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsUcwaConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="0d9ff-114">Description</span><span class="sxs-lookup"><span data-stu-id="0d9ff-114">Description</span></span>

<span data-ttu-id="0d9ff-115">L’applet de **contrôle test-CsUcwaConference** vérifie qu’un binôme d’utilisateurs de test peut planifier, rejoindre et diriger une conférence en ligne à l’aide de l’API Web Unified Communications Web (UCWA).</span><span class="sxs-lookup"><span data-stu-id="0d9ff-115">The **Test-CsUcwaConference** cmdlet verifies that a pair of test users can schedule, join, and then conduct an online conference using the Unified Communications Web API (UCWA).</span></span> <span data-ttu-id="0d9ff-116">Pour ce faire, le cmdlet utilise le service de ticket Web de Lync Server pour authentifier les deux utilisateurs test et les inscrire auprès de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-116">To do this, the cmdlet uses the Lync Server web ticket service to authenticate the two test users and register them with Lync Server.</span></span> <span data-ttu-id="0d9ff-117">L’applet de commande démarre alors une conférence à l’aide des informations d’identification de la classe Organizer et invite le participant à rejoindre la réunion.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-117">The cmdlet then starts a conference using the organizer credentials and invites the participant to join the meeting.</span></span> <span data-ttu-id="0d9ff-118">Une fois la réunion jointe, l’applet de **contrôle CsUcwaConference de test** vérifie que les utilisateurs peuvent effectuer des actions telles que les messages instantanés Exchange et les pools, puis déconnecter la Conférence et annuler l’enregistrement des deux utilisateurs test.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-118">After the meeting is joined, the **Test-CsUcwaConference** cmdlet verifies that the users can do such things as exchange instant message and conduct pools, then disconnects the conference and unregisters the two test users.</span></span> <span data-ttu-id="0d9ff-119">La conférence planifiée sera également supprimée une fois le test terminé.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-119">The scheduled conference will also be deleted when the test is finished.</span></span>

<span data-ttu-id="0d9ff-120">L’applet de **contrôle test-CsUcwaConference** peut également être utilisée pour déterminer si des utilisateurs anonymes peuvent participer à des conférences en ligne.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-120">The **Test-CsUcwaConference** cmdlet can also be used to determine whether anonymous users can join online conferences.</span></span>

<span data-ttu-id="0d9ff-121">Notez que l’applet de **contrôle test-CsUcwaConference** ne doit pas être exécutée sur un pool Microsoft Lync Server 2010, sauf si UCWA a été installé sur ce pool.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-121">Note that the **Test-CsUcwaConference** cmdlet should not be run against a Microsoft Lync Server 2010 pool unless UCWA was installed on that pool.</span></span> <span data-ttu-id="0d9ff-122">Si UCWA n’a pas été installé, l’appel à l’applet de **contrôle CsUcwaConference** échoue.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-122">If UCWA has not been installed then the call to the **Test-CsUcwaConference** cmdlet will fail.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="0d9ff-123">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="0d9ff-123">Running the test</span></span>

<span data-ttu-id="0d9ff-124">La commande décrite dans l’exemple 1 vérifie qu’un binôme d’utilisateurs de test peut participer à une conférence UCWA sur le pool atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-124">The command shown in Example 1 verifies that a pair of test users can participate in an UCWA conference on the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="0d9ff-125">Notez que cette commande échoue si vous n’avez pas prédéfini une paire de tests de configuration de l’analyse de l’état des utilisateurs pour atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-125">Note that this command will fail if you have not predefined a pair of health monitoring configuration test users for atl-cs-001.litwareinc.com.</span></span>

    Test-CsUcwaConference -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="0d9ff-126">Les commandes illustrées dans l’exemple 2 permettent de tester la capacité d’une paire d’utilisateurs (litwareinc \\ Pilar et litwareinc \\ kenmyer) de participer à une conférence UCWA.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-126">The commands shown in Example 2 test the ability of a pair of users (litwareinc\\pilar and litwareinc\\kenmyer) to participate in an UCWA conference.</span></span> <span data-ttu-id="0d9ff-127">Pour cela, la première commande de l’exemple utilise l’applet de commande Get-Credential pour créer un objet d’information d’interface de ligne de commande Windows PowerShell contenant le nom et le mot de passe de l’utilisateur Pilar Arès.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-127">To do this, the first command in the example uses the Get-Credential cmdlet to create a Windows PowerShell command-line interface credential object that contains the name and password of the user Pilar Ackerman.</span></span> <span data-ttu-id="0d9ff-128">(Dans la mesure où le nom de connexion, litwareinc \\ Pilar, a été inclus en tant que paramètre, la boîte de dialogue demande d’informations d’identification Windows PowerShell n’exige que l’administrateur entre le mot de passe du compte Arès Pilar.) L’objet Credentials obtenu est ensuite stocké dans une variable nommée $cred 1.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-128">(Because the logon name, litwareinc\\pilar, was included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Pilar Ackerman account.) The resulting credentials object is then stored in a variable named $cred1.</span></span> <span data-ttu-id="0d9ff-129">La deuxième commande effectue la même opération en renvoyant alors un objet Credential pour le compte Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-129">The second command does the same thing, this time returning a credential object for the Ken Myer account.</span></span>

<span data-ttu-id="0d9ff-130">À l’aide des deux objets d’information d’identification disponibles, la troisième commande de l’exemple détermine si les deux utilisateurs peuvent participer à une conférence UCWA.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-130">With the two credential objects in hand, the third command in the example determines whether the two users can participate in an UCWA conference.</span></span> <span data-ttu-id="0d9ff-131">Pour exécuter cette tâche, l’applet de commande **test-CsUcwaConference** est appelée, ainsi que les paramètres suivants : TargetFqdn (nom de domaine complet (FQDN) du pool d’inscriptions); OrganizerSipAddress (adresse SIP de l’organisateur de la réunion); OrganizerCredential (objet Windows PowerShell contenant les informations d’identification pour ce même utilisateur); ParticipantSipAddress (adresse SIP de l’autre utilisateur du test); et ParticipantCredential (l’objet d’interface de ligne de commande Windows PowerShell qui contient les informations d’identification pour l’autre utilisateur).</span><span class="sxs-lookup"><span data-stu-id="0d9ff-131">To run this task, the **Test-CsUcwaConference** cmdlet is called, together with the following parameters: TargetFqdn (the FQDN of the Registrar pool); OrganizerSipAddress (the SIP address for the meeting organizer); OrganizerCredential (the Windows PowerShell object that contains the credentials for this same user); ParticipantSipAddress (the SIP address for the other test user); and ParticipantCredential (the Windows PowerShell command-line interface object that contains the credentials for the other user).</span></span>

    $cred1 = Get-Credential "litwareinc\pilar"
    $cred2 = Get-Credential "litwareinc\kenmyer"
    Test-CsUcwaConference -TargetFqdn atl-cs-001.litwareinc.com -OrganizerSipAddress "sip:pilar@litwareinc.com" -OrganizerCredential $cred1 -ParticipantSipAddress "sip:kenmyer@litwareinc.com" -ParticipantCredential $cred2

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="0d9ff-132">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="0d9ff-132">Determining success or failure</span></span>

<span data-ttu-id="0d9ff-133">Si la Conférence est configurée correctement, vous recevrez une sortie semblable à celle-ci, avec la propriété Result marquée comme **réussie :**</span><span class="sxs-lookup"><span data-stu-id="0d9ff-133">If conferencing is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="0d9ff-134">Nom de domaine complet (FQDN) cible : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="0d9ff-134">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="0d9ff-135">URI cible : https://LyncTest-SE. LyncTest. SelfHost. Corp.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-135">Target Uri : https:// LyncTest-SE.LyncTest.SelfHost.Corp.</span></span>

<span data-ttu-id="0d9ff-136">Microsoft.com:443/CertProv/CertProvisiongService.svc</span><span class="sxs-lookup"><span data-stu-id="0d9ff-136">Microsoft.com:443/CertProv/CertProvisiongService.svc</span></span>

<span data-ttu-id="0d9ff-137">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="0d9ff-137">Result : Success</span></span>

<span data-ttu-id="0d9ff-138">Latence : 00:00:14.9862716</span><span class="sxs-lookup"><span data-stu-id="0d9ff-138">Latency : 00:00:14.9862716</span></span>

<span data-ttu-id="0d9ff-139">Message d’erreur :</span><span class="sxs-lookup"><span data-stu-id="0d9ff-139">Error Message :</span></span>

<span data-ttu-id="0d9ff-140">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="0d9ff-140">Diagnosis :</span></span>

<span data-ttu-id="0d9ff-141">Si les utilisateurs spécifiés ne peuvent pas utiliser les conférences, le résultat est affiché en tant qu' **échec** et des informations supplémentaires sont enregistrées dans les propriétés d’erreur et de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="0d9ff-141">If the specified users can't use conferencing, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="0d9ff-142">AVERTISSEMENT : impossible de lire le numéro de port du Bureau d’enregistrement pour le nom complet fourni</span><span class="sxs-lookup"><span data-stu-id="0d9ff-142">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="0d9ff-143">nom de domaine (FQDN).</span><span class="sxs-lookup"><span data-stu-id="0d9ff-143">domain name (FQDN).</span></span> <span data-ttu-id="0d9ff-144">Utilisation du numéro de port de bureau par défaut.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-144">Using default Registrar port number.</span></span> <span data-ttu-id="0d9ff-145">Sauf</span><span class="sxs-lookup"><span data-stu-id="0d9ff-145">Exception:</span></span>

<span data-ttu-id="0d9ff-146">System. InvalidOperationException : aucun cluster correspondant détecté dans la topologie.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-146">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="0d9ff-147">dès</span><span class="sxs-lookup"><span data-stu-id="0d9ff-147">at</span></span>

<span data-ttu-id="0d9ff-148">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="0d9ff-148">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="0d9ff-149">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="0d9ff-149">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="0d9ff-150">Test-CsUcwaConference : il n’y a aucun utilisateur de test affecté à</span><span class="sxs-lookup"><span data-stu-id="0d9ff-150">Test-CsUcwaConference : There is no test user assigned for</span></span>

<span data-ttu-id="0d9ff-151">\[LyncTest.SelfHost.Corp.Microsoft.com \] .</span><span class="sxs-lookup"><span data-stu-id="0d9ff-151">\[LyncTest.SelfHost.Corp.Microsoft.com\].</span></span> <span data-ttu-id="0d9ff-152">Vérifiez la configuration de l’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-152">Verify test user configuration.</span></span>

<span data-ttu-id="0d9ff-153">À la ligne : 1 car : 1</span><span class="sxs-lookup"><span data-stu-id="0d9ff-153">At line:1 char:1</span></span>

<span data-ttu-id="0d9ff-154">\+ Test-CsUcwaConference-TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="0d9ff-154">\+ Test-CsUcwaConference -TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span></span>

\+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

<span data-ttu-id="0d9ff-155">\+ CategoryInfo : ResourceUnavailable : ( :) \[ Test-CsUcwaConference\]</span><span class="sxs-lookup"><span data-stu-id="0d9ff-155">\+ CategoryInfo : ResourceUnavailable: (:) \[Test-CsUcwaConference\]</span></span>

<span data-ttu-id="0d9ff-156">, InvalidOperationException</span><span class="sxs-lookup"><span data-stu-id="0d9ff-156">, InvalidOperationException</span></span>

<span data-ttu-id="0d9ff-157">\+ FullyQualifiedErrorId : NotFoundTestUsers, Microsoft. RTC. Management. synthé</span><span class="sxs-lookup"><span data-stu-id="0d9ff-157">\+ FullyQualifiedErrorId : NotFoundTestUsers,Microsoft.Rtc.Management.Synth</span></span>

<span data-ttu-id="0d9ff-158">eticTransactions.TestUcwaConferenceCmdlet</span><span class="sxs-lookup"><span data-stu-id="0d9ff-158">eticTransactions.TestUcwaConferenceCmdlet</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="0d9ff-159">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="0d9ff-159">Reasons why the test might have failed</span></span>

<span data-ttu-id="0d9ff-160">Voici quelques raisons courantes pour lesquelles **les tests-CsUcwaConference** peuvent échouer :</span><span class="sxs-lookup"><span data-stu-id="0d9ff-160">Here are some common reasons why **Test-CsUcwaConference** might fail:</span></span>

  - <span data-ttu-id="0d9ff-161">Une valeur de paramètre incorrecte a été fournie.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-161">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="0d9ff-162">S’il est utilisé, les paramètres facultatifs doivent être correctement configurés ou le test échoue.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-162">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="0d9ff-163">Réexécutez la commande sans les paramètres facultatifs et déterminez si l’opération aboutit.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-163">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="0d9ff-164">La possibilité d’organiser une conférence dépend de la stratégie de conférence qui a été affectée à l’utilisateur qui a organisé la Conférence (dans le cas de l’applet de **contrôle CsUcwaConference** , qui est le « sender »).</span><span class="sxs-lookup"><span data-stu-id="0d9ff-164">The ability to conduct a conference depends on the conferencing policy that has been assigned to the user who organized the conference (in the case of the **Test-CsUcwaConference** cmdlet, that is the "sender").</span></span> <span data-ttu-id="0d9ff-165">Si l’organisateur n’est pas autorisé à inclure des activités de collaboration dans sa réunion (par exemple, si sa propriété EnableDataCollaboration est définie sur false), l’applet de commande **test-CsUcwaConference** échoue.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-165">If the organizer is not allowed to include collaborative activities in his or her meeting (for example, if his or her conferencing policy has the EnableDataCollaboration property set to False) then the **Test-CsUcwaConference** cmdlet will fail.</span></span>

  - <span data-ttu-id="0d9ff-166">Cette commande échoue si le serveur de périphérie est mal configuré ou n’est pas encore déployé.</span><span class="sxs-lookup"><span data-stu-id="0d9ff-166">This command will fail if the Edge Server is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0d9ff-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d9ff-167">See Also</span></span>


[<span data-ttu-id="0d9ff-168">Test-CsASConference</span><span class="sxs-lookup"><span data-stu-id="0d9ff-168">Test-CsASConference</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsASConference)  
[<span data-ttu-id="0d9ff-169">Test-CsDataConference</span><span class="sxs-lookup"><span data-stu-id="0d9ff-169">Test-CsDataConference</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsDataConference)  
[<span data-ttu-id="0d9ff-170">Test-CsAVConference</span><span class="sxs-lookup"><span data-stu-id="0d9ff-170">Test-CsAVConference</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference)  
  

<span data-ttu-id="0d9ff-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0d9ff-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

