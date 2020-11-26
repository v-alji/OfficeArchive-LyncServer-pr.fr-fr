---
title: 'Lync Server 2013 : test de la connexion utilisateur à la messagerie vocale de la messagerie unifiée Exchange'
description: 'Lync Server 2013 : test de la connexion utilisateur à la messagerie vocale de la messagerie unifiée Exchange.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing user connection to Exchange UM voicemail
ms:assetid: 574da104-8823-4061-9fb6-353639f1884d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727305(v=OCS.15)
ms:contentKeyID: 63969604
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b887b5b0df02a5864e0a39f2b62893d20105a86a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439711"
---
# <a name="testing-user-connection-to-exchange-um-voicemail-in-lync-server-2013"></a><span data-ttu-id="2ba6b-103">Test de la connexion utilisateur à la messagerie vocale de messagerie unifiée Exchange dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ba6b-103">Testing user connection to Exchange UM voicemail in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2ba6b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2ba6b-104">

<span> </span></span></span>

<span data-ttu-id="2ba6b-105">_**Dernière modification de la rubrique :** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="2ba6b-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ba6b-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="2ba6b-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="2ba6b-107">Jour</span><span class="sxs-lookup"><span data-stu-id="2ba6b-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ba6b-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="2ba6b-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="2ba6b-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2ba6b-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ba6b-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="2ba6b-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="2ba6b-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="2ba6b-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande <strong>test-CsExUMVoiceMail</strong> .</span><span class="sxs-lookup"><span data-stu-id="2ba6b-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsExUMVoiceMail</strong> cmdlet.</span></span> <span data-ttu-id="2ba6b-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="2ba6b-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsExUMVoiceMail&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="2ba6b-114">Description</span><span class="sxs-lookup"><span data-stu-id="2ba6b-114">Description</span></span>

<span data-ttu-id="2ba6b-115">L’applet de **contrôle test-CsExUMVoiceMail** permet aux administrateurs de vérifier qu’un utilisateur peut accéder au service de messagerie unifiée Microsoft Exchange Server 2013 et l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-115">The **Test-CsExUMVoiceMail** cmdlet enables administrators to verify that a user can access and use the Microsoft Exchange Server 2013 unified messaging service.</span></span> <span data-ttu-id="2ba6b-116">Pour ce faire, l’applet de connexion se connecte au service de messagerie unifiée et quitte un message vocal dans la boîte aux lettres spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-116">To do this, the cmdlet connects to the unified messaging service and leaves a voice mail in the specified mailbox.</span></span> <span data-ttu-id="2ba6b-117">Il peut s’agir d’une messagerie vocale fournie par le système ou d’un message personnalisé. Fichier WAV enregistré vous-même.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-117">This can be a system-supplied voice mail, or it can be a custom .WAV file that you have recorded yourself.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="2ba6b-118">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="2ba6b-118">Running the test</span></span>

<span data-ttu-id="2ba6b-119">L’exemple suivant teste la connectivité de messagerie vocale Exchange Unified Messaging pour le pool atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-119">The following example tests Exchange Unified Messaging voice mail connectivity for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="2ba6b-120">Cette commande ne fonctionnera que si les utilisateurs de test étaient définis pour le pool atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-120">This command will work only if test users were defined for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="2ba6b-121">Si tel est le cas, la commande détermine si le premier utilisateur du test peut utiliser la messagerie vocale de la messagerie unifiée.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-121">If they have, then the command will determine whether the first test user can use Unified Messaging voice mail.</span></span> <span data-ttu-id="2ba6b-122">Si les utilisateurs test n’ont pas été configurés pour le pool, la commande échoue.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-122">If test users were not configured for the pool then the command will fail.</span></span>

    Test-CsExUMVoiceMail -TargetFqdn "atl-cs-001.litwareinc.com" -ReceiverSipAddress "sip:kenmyer@litwareinc.com" 

<span data-ttu-id="2ba6b-123">Les commandes indiquées dans l’exemple suivant testent la connectivité de la messagerie vocale de la messagerie unifiée Exchange pour l’utilisateur litwareinc \\ kenmyer.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-123">The commands shown in the next example test Exchange Unified Messaging voice mail connectivity for the user litwareinc\\kenmyer.</span></span> <span data-ttu-id="2ba6b-124">Pour ce faire, la première commande de l’exemple utilise l’applet de commande **Get-Credential** pour créer un objet d’information d’identification d’interface de ligne de commande Windows PowerShell pour l’utilisateur litwareinc \\ kenmyer.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-124">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credentials object for the user litwareinc\\kenmyer.</span></span> <span data-ttu-id="2ba6b-125">Notez que vous devez fournir le mot de passe de ce compte pour créer un objet d’informations d’identification valide et garantir que l’applet de contrôle **CsExUMVoiceMail** puisse exécuter sa vérification.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-125">Note that you must supply the password for this account to create a valid credentials object and to ensure that the **Test-CsExUMVoiceMail** cmdlet can run its check.</span></span>

<span data-ttu-id="2ba6b-126">La deuxième commande de l’exemple utilise l’objet Credentials fourni ($x) et l’adresse SIP de l’utilisateur litwareinc \\ kenmyer pour déterminer si l’utilisateur peut se connecter à la messagerie vocale de la messagerie unifiée Exchange.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-126">The second command in the example uses the supplied credentials object ($x) and the SIP address of the user litwareinc\\kenmyer to determine whether or this user can connect to Exchange Unified Messaging voice mail.</span></span>

    $credential = Get-Credential "litwareinc\pilar" 
    
    Test-CsExUMVoiceMail -TargetFqdn "atl-cs-001.litwareinc.com" -ReceiverSipAddress "sip:kenmyer@litwareinc.com" -SenderSipAddress "sip:pilar@litwareinc.com" -SenderCredential $credential 

<span data-ttu-id="2ba6b-127">Dans l’exemple qui suit, la commande est une variante de la commande affichée dans l’exemple 1 ; dans ce cas, le paramètre OutLoggerVariable est inclus pour générer un journal détaillé de chaque étape réalisée par le **test-CsExUMVoiceMail** cmdletand le succès ou l’échec de chacune de ces étapes.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-127">The command shown in the next example is a variation of the command shown in Example 1; in this case, the OutLoggerVariable parameter is included to generate a detailed log of every step done by the **Test-CsExUMVoiceMail** cmdletand the success or failure of each of those steps.</span></span> <span data-ttu-id="2ba6b-128">Pour ce faire, le paramètre OutLoggerVariable est ajouté à côté de la valeur de paramètre ExumText ; les informations de journalisation détaillées sont alors stockées dans une variable nommée $ExumTest.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-128">To do this, the OutLoggerVariable parameter is added alongside the parameter value ExumText; that causes detailed logging information to be stored in a variable named $ExumTest.</span></span> <span data-ttu-id="2ba6b-129">Dans la commande final de l’exemple, la méthode ToXML () est utilisée pour convertir les informations du journal au format XML.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-129">In the final command in the example, the ToXML() method is used to convert the log information to XML format.</span></span> <span data-ttu-id="2ba6b-130">Ces données XML sont alors écrites dans un fichier nommé C : \\ LogsVoicemailTest.xml à \\ l’aide de l’applet de Out-File cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-130">That XML data is then written to a file that is named C:\\Logs\\VoicemailTest.xml by using the Out-File cmdlet.</span></span>

    Test-CsExUMVoiceMail -TargetFqdn "atl-cs-001.litwareinc.com" -ReceiverSipAddress "sip:kenmyer@litwareinc.com" -OutLoggerVariable VoicemailTest 
     
    $VoicemailTest.ToXML() | Out-File C:\Logs\VoicemailTest.xml

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="2ba6b-131">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="2ba6b-131">Determining success or failure</span></span>

<span data-ttu-id="2ba6b-132">Si l’intégration Exchange est correctement configurée, vous recevrez une sortie similaire à celle-ci, avec la propriété Result marquée comme **réussie**:</span><span class="sxs-lookup"><span data-stu-id="2ba6b-132">If Exchange integration is correctly configured, you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="2ba6b-133">Nom de domaine complet (FQDN) cible : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="2ba6b-133">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="2ba6b-134">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="2ba6b-134">Result : Success</span></span>

<span data-ttu-id="2ba6b-135">Latence : 00:00:02.9911345</span><span class="sxs-lookup"><span data-stu-id="2ba6b-135">Latency : 00:00:02.9911345</span></span>

<span data-ttu-id="2ba6b-136">Message d’erreur :</span><span class="sxs-lookup"><span data-stu-id="2ba6b-136">Error Message :</span></span>

<span data-ttu-id="2ba6b-137">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="2ba6b-137">Diagnosis :</span></span>

<span data-ttu-id="2ba6b-138">Si l’utilisateur spécifié ne peut pas se connecter à la boîte vocale, le résultat est affiché en **panne** et des informations supplémentaires sont enregistrées dans les propriétés d’erreur et de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="2ba6b-138">If the specified user can't connect to voicemail, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="2ba6b-139">AVERTISSEMENT : impossible de lire le numéro de port du Bureau d’enregistrement pour le nom complet fourni</span><span class="sxs-lookup"><span data-stu-id="2ba6b-139">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="2ba6b-140">nom de domaine (FQDN).</span><span class="sxs-lookup"><span data-stu-id="2ba6b-140">domain name (FQDN).</span></span> <span data-ttu-id="2ba6b-141">Utilisation du numéro de port de bureau par défaut.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-141">Using default Registrar port number.</span></span> <span data-ttu-id="2ba6b-142">Sauf</span><span class="sxs-lookup"><span data-stu-id="2ba6b-142">Exception:</span></span>

<span data-ttu-id="2ba6b-143">System. InvalidOperationException : aucun cluster correspondant détecté dans la topologie.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-143">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="2ba6b-144">dès</span><span class="sxs-lookup"><span data-stu-id="2ba6b-144">at</span></span>

<span data-ttu-id="2ba6b-145">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="2ba6b-145">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="2ba6b-146">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="2ba6b-146">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="2ba6b-147">Nom de domaine complet (FQDN) cible : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="2ba6b-147">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="2ba6b-148">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="2ba6b-148">Result : Failure</span></span>

<span data-ttu-id="2ba6b-149">Latence : 00:00:00</span><span class="sxs-lookup"><span data-stu-id="2ba6b-149">Latency : 00:00:00</span></span>

<span data-ttu-id="2ba6b-150">Message d’erreur : 10060, une tentative de connexion a échoué car la partie connectée</span><span class="sxs-lookup"><span data-stu-id="2ba6b-150">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="2ba6b-151">ne répond pas correctement après un certain temps, ou</span><span class="sxs-lookup"><span data-stu-id="2ba6b-151">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="2ba6b-152">échec de la connexion établie, car l’hôte connecté a</span><span class="sxs-lookup"><span data-stu-id="2ba6b-152">established connection failed because connected host has</span></span>

<span data-ttu-id="2ba6b-153">échec de la réponse à 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="2ba6b-153">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="2ba6b-154">Exception interne : une tentative de connexion a échoué, car le</span><span class="sxs-lookup"><span data-stu-id="2ba6b-154">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="2ba6b-155">la fête connectée ne répond pas correctement après un délai de</span><span class="sxs-lookup"><span data-stu-id="2ba6b-155">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="2ba6b-156">heure ou échec de la connexion en raison d’un hôte connecté</span><span class="sxs-lookup"><span data-stu-id="2ba6b-156">time, or established connection failed because connected host</span></span>

<span data-ttu-id="2ba6b-157">échec de la réponse à 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="2ba6b-157">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="2ba6b-158">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="2ba6b-158">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="2ba6b-159">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="2ba6b-159">Reasons why the test might have failed</span></span>

<span data-ttu-id="2ba6b-160">Voici quelques raisons courantes pour lesquelles **les tests-CsExUMVoiceMail** peuvent échouer :</span><span class="sxs-lookup"><span data-stu-id="2ba6b-160">Here are some common reasons why **Test-CsExUMVoiceMail** might fail:</span></span>

  - <span data-ttu-id="2ba6b-161">Une valeur de paramètre incorrecte a été fournie.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-161">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="2ba6b-162">S’il est utilisé, les paramètres facultatifs doivent être correctement configurés ou le test échoue.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-162">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="2ba6b-163">Réexécutez la commande sans les paramètres facultatifs et déterminez si l’opération aboutit.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-163">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="2ba6b-164">Si le serveur Exchange n’est pas configuré correctement ou n’est pas encore déployé, cette commande échoue.</span><span class="sxs-lookup"><span data-stu-id="2ba6b-164">This command will fail if the Exchange Server is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2ba6b-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ba6b-165">See Also</span></span>


[<span data-ttu-id="2ba6b-166">Test-CsExUMConnectivity</span><span class="sxs-lookup"><span data-stu-id="2ba6b-166">Test-CsExUMConnectivity</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsExUMConnectivity)  
  

<span data-ttu-id="2ba6b-167"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2ba6b-167"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

