---
title: 'Lync Server 2013 : test de conversation permanente'
description: 'Lync Server 2013 : test de conversation permanente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing persistent chat
ms:assetid: d351b6f2-bc31-42e0-9e8d-c347713d6b4a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727313(v=OCS.15)
ms:contentKeyID: 63969651
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8b1dc4eef1870f1287dacdc1852ab1e24edd169
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440996"
---
# <a name="testing-persistent-chat-in-lync-server-2013"></a><span data-ttu-id="9b726-103">Test de conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9b726-103">Testing persistent chat in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9b726-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9b726-104">

<span> </span></span></span>

<span data-ttu-id="9b726-105">_**Dernière modification de la rubrique :** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="9b726-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b726-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="9b726-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="9b726-107">Jour</span><span class="sxs-lookup"><span data-stu-id="9b726-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b726-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="9b726-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="9b726-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9b726-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b726-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="9b726-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="9b726-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="9b726-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="9b726-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande <strong>test-CsPersistentChatMessage</strong> .</span><span class="sxs-lookup"><span data-stu-id="9b726-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsPersistentChatMessage</strong> cmdlet.</span></span> <span data-ttu-id="9b726-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="9b726-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPersistentChatMessage&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="9b726-114">Description</span><span class="sxs-lookup"><span data-stu-id="9b726-114">Description</span></span>

<span data-ttu-id="9b726-115">L’applet de **contrôle test-CsPersistentChatMessage** vérifie qu’une paire d’utilisateurs de test peut échanger des messages à l’aide du service Chat permanent.</span><span class="sxs-lookup"><span data-stu-id="9b726-115">The **Test-CsPersistentChatMessage** cmdlet verifies that a pair of test users can exchange messages using the Persistent Chat service.</span></span> <span data-ttu-id="9b726-116">Pour ce faire, l’applet de connexion enregistre les deux utilisateurs sur Lync Server 2013, connecte les utilisateurs à une salle de conversation permanente, échange une paire de messages, puis quitte la salle de conversation et déconnecte les deux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9b726-116">To do this, the cmdlet logs the two users on to Lync Server 2013, connects the users to a persistent Chat room, exchanges a pair of messages, then exits the chat room and logs off the two users.</span></span> <span data-ttu-id="9b726-117">Notez que les appels à cette applet de contrôle échoueront si vous n’avez pas créé de salles de conversation ou si les deux comptes d’utilisateurs test ne disposent pas d’une stratégie de discussion persistante lui permettant d’accéder au service de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="9b726-117">Note that calls to this cmdlet will fail if you have not created any chat rooms or if the two test user accounts are not assigned a Persistent Chat policy that gives them access to the Persistent Chat service.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="9b726-118">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="9b726-118">Running the test</span></span>

<span data-ttu-id="9b726-119">Les commandes indiquées dans l’exemple suivant testent la capacité d’une paire d’utilisateurs (litwareinc \\ Pilar et litwareinc \\ kenmyer) à se connecter à Lync Server 2013, puis échangent des messages à l’aide du service Chat permanent.</span><span class="sxs-lookup"><span data-stu-id="9b726-119">The commands shown in the following example test the ability of a pair of users (litwareinc\\pilar and litwareinc\\kenmyer) to log on to Lync Server 2013 and then exchange messages using the Persistent Chat service.</span></span> <span data-ttu-id="9b726-120">Pour cela, la première commande de l’exemple utilise l’applet de commande **Get-Credential** pour créer un objet d’information d’interface de ligne de commande Windows PowerShell contenant le nom et le mot de passe de l’utilisateur Pilar Arès.</span><span class="sxs-lookup"><span data-stu-id="9b726-120">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credential object that contains the name and password of the user Pilar Ackerman.</span></span> <span data-ttu-id="9b726-121">(Dans la mesure où le nom de connexion, litwareinc \\ Pilar, a été inclus en tant que paramètre, la boîte de dialogue demande d’informations d’identification Windows PowerShell n’exige que l’administrateur entre le mot de passe du compte Arès Pilar.) L’objet Credentials obtenu est ensuite stocké dans une variable nommée $cred 1.</span><span class="sxs-lookup"><span data-stu-id="9b726-121">(Because the logon name, litwareinc\\pilar, was included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Pilar Ackerman account.) The resulting credentials object is then stored in a variable named $cred1.</span></span> <span data-ttu-id="9b726-122">La deuxième commande effectue la même opération en renvoyant alors un objet Credential pour le compte Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="9b726-122">The second command does the same thing, this time returning a credential object for the Ken Myer account.</span></span>

<span data-ttu-id="9b726-123">Avec les objets d’information d’identification disponibles, la troisième commande détermine si ces deux utilisateurs peuvent se connecter à Lync Server 2013 et échanger des messages à l’aide d’une conversation permanente.</span><span class="sxs-lookup"><span data-stu-id="9b726-123">With the credential objects in hand, the third command determines whether these two users can log on to Lync Server 2013 and exchange messages using Persistent Chat.</span></span> <span data-ttu-id="9b726-124">Pour effectuer cette tâche, l’applet de commande **test-CsPersistentChatMessage** est appelée en utilisant les paramètres suivants : TargetFqdn (nom de domaine complet (FQDN) du pool d’inscriptions); SenderSipAddress (adresse SIP pour le premier utilisateur test); SenderCredential (objet Windows PowerShell contenant les informations d’identification pour ce même utilisateur); ReceiverSipAddress (adresse SIP de l’autre utilisateur du test); et ReceiverCredential (objet Windows PowerShell contenant les informations d’identification pour l’autre utilisateur de test).</span><span class="sxs-lookup"><span data-stu-id="9b726-124">To perform this task, the **Test-CsPersistentChatMessage** cmdlet is called using the following parameters: TargetFqdn (the FQDN of the Registrar pool); SenderSipAddress (the SIP address for the first test user); SenderCredential (the Windows PowerShell object that contains the credentials for this same user); ReceiverSipAddress (the SIP address for the other test user); and ReceiverCredential (the Windows PowerShell object that contains the credentials for the other test user).</span></span>

    $cred1 = Get-Credential "litwareinc\pilar"
    $cred2 = Get-Credential "litwareinc\kenmyer"
    
    Test-CsPersistentChatMessage -TargetFqdn atl-persistentchat-001.litwareinc.com -SenderSipAddress "sip:pilar@litwareinc.com" -SenderCredential $cred1 -ReceiverSipAddress "sip:kenmyer@litwareinc.com" -ReceiverCredential $cred2

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="9b726-125">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="9b726-125">Determining success or failure</span></span>

<span data-ttu-id="9b726-126">Si l’utilisateur spécifié dispose d’une stratégie d’emplacement valide, vous recevrez une sortie semblable à ce qui suit, avec la propriété Result marquée comme **réussie**:</span><span class="sxs-lookup"><span data-stu-id="9b726-126">If the specified user has a valid location policy, then you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="9b726-127">Nom de domaine complet (FQDN) cible : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="9b726-127">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="9b726-128">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="9b726-128">Result : Success</span></span>

<span data-ttu-id="9b726-129">Latence : 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9b726-129">Latency : 00:00:00</span></span>

<span data-ttu-id="9b726-130">Message d’erreur :</span><span class="sxs-lookup"><span data-stu-id="9b726-130">Error Message :</span></span>

<span data-ttu-id="9b726-131">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="9b726-131">Diagnosis :</span></span>

<span data-ttu-id="9b726-132">Si les utilisateurs spécifiés ne peuvent pas échanger de messages à l’aide du service de chat permanent, le résultat s’affichera en **panne** et des informations supplémentaires seront enregistrées dans les propriétés d’erreur et de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="9b726-132">If the specified users can't exchange messages using the Persistent Chat service, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="9b726-133">AVERTISSEMENT : impossible de lire le numéro de port du Bureau d’enregistrement pour le nom complet fourni</span><span class="sxs-lookup"><span data-stu-id="9b726-133">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="9b726-134">nom de domaine (FQDN).</span><span class="sxs-lookup"><span data-stu-id="9b726-134">domain name (FQDN).</span></span> <span data-ttu-id="9b726-135">Utilisation du numéro de port de bureau par défaut.</span><span class="sxs-lookup"><span data-stu-id="9b726-135">Using default Registrar port number.</span></span> <span data-ttu-id="9b726-136">Sauf</span><span class="sxs-lookup"><span data-stu-id="9b726-136">Exception:</span></span>

<span data-ttu-id="9b726-137">System. InvalidOperationException : aucun cluster correspondant détecté dans la topologie.</span><span class="sxs-lookup"><span data-stu-id="9b726-137">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="9b726-138">dès</span><span class="sxs-lookup"><span data-stu-id="9b726-138">at</span></span>

<span data-ttu-id="9b726-139">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="9b726-139">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="9b726-140">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="9b726-140">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="9b726-141">Nom de domaine complet (FQDN) cible : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="9b726-141">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="9b726-142">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="9b726-142">Result : Failure</span></span>

<span data-ttu-id="9b726-143">Latence : 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9b726-143">Latency : 00:00:00</span></span>

<span data-ttu-id="9b726-144">Message d’erreur : 10060, une tentative de connexion a échoué car la partie connectée</span><span class="sxs-lookup"><span data-stu-id="9b726-144">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="9b726-145">ne répond pas correctement après un certain temps, ou</span><span class="sxs-lookup"><span data-stu-id="9b726-145">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="9b726-146">échec de la connexion établie, car l’hôte connecté a</span><span class="sxs-lookup"><span data-stu-id="9b726-146">established connection failed because connected host has</span></span>

<span data-ttu-id="9b726-147">échec de la réponse à \[ 2001:4898 : E8 : f39e : 5c9a : ad83:81b3:9944 \] : 5061</span><span class="sxs-lookup"><span data-stu-id="9b726-147">failed to respond \[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="9b726-148">Exception interne : une tentative de connexion a échoué, car le</span><span class="sxs-lookup"><span data-stu-id="9b726-148">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="9b726-149">la fête connectée ne répond pas correctement après un délai de</span><span class="sxs-lookup"><span data-stu-id="9b726-149">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="9b726-150">heure ou échec de la connexion en raison d’un hôte connecté</span><span class="sxs-lookup"><span data-stu-id="9b726-150">time, or established connection failed because connected host</span></span>

<span data-ttu-id="9b726-151">échec de la réponse</span><span class="sxs-lookup"><span data-stu-id="9b726-151">has failed to respond</span></span>

<span data-ttu-id="9b726-152">\[2001:4898 : E8 : f39e : 5c9a : ad83:81b3:9944 \] : 5061</span><span class="sxs-lookup"><span data-stu-id="9b726-152">\[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="9b726-153">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="9b726-153">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="9b726-154">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="9b726-154">Reasons why the test might have failed</span></span>

<span data-ttu-id="9b726-155">Voici quelques raisons courantes pour lesquelles **les tests-CsPersistentChatMessage** peuvent échouer :</span><span class="sxs-lookup"><span data-stu-id="9b726-155">Here are some common reasons why **Test-CsPersistentChatMessage** might fail:</span></span>

  - <span data-ttu-id="9b726-156">Une valeur de paramètre incorrecte a été fournie.</span><span class="sxs-lookup"><span data-stu-id="9b726-156">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="9b726-157">Il est possible que les comptes de test requis n’existent pas ou aient été créés correctement.</span><span class="sxs-lookup"><span data-stu-id="9b726-157">The required test accounts may not exist or have been correctly created.</span></span>

  - <span data-ttu-id="9b726-158">Il est possible qu’il y ait un problème réseau entraînant un délai inattendu qui a entraîné le test.</span><span class="sxs-lookup"><span data-stu-id="9b726-158">There may have been a network issue causing an unexpected delay which timed out the test.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9b726-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b726-159">See Also</span></span>


[<span data-ttu-id="9b726-160">Grant-CsPersistentChatPolicy</span><span class="sxs-lookup"><span data-stu-id="9b726-160">Grant-CsPersistentChatPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Grant-CsPersistentChatPolicy)  
[<span data-ttu-id="9b726-161">New-CsPersistentChatPolicy</span><span class="sxs-lookup"><span data-stu-id="9b726-161">New-CsPersistentChatPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsPersistentChatPolicy)  
[<span data-ttu-id="9b726-162">Set-CsPersistentChatPolicy</span><span class="sxs-lookup"><span data-stu-id="9b726-162">Set-CsPersistentChatPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsPersistentChatPolicy)  
  

<span data-ttu-id="9b726-163"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9b726-163"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

