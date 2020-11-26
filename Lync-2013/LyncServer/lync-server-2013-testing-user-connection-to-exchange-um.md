---
title: 'Lync Server 2013 : test de la connexion utilisateur à la messagerie unifiée Exchange'
description: 'Lync Server 2013 : test de la connexion utilisateur à la messagerie unifiée Exchange.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing user connection to Exchange UM
ms:assetid: 0b83fbf4-e124-4efd-a0a9-202eb849af82
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727300(v=OCS.15)
ms:contentKeyID: 63969573
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ea6f7d446fe3fd98db67bab4ffee9cc976202689
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440933"
---
# <a name="testing-user-connection-to-exchange-um-in-lync-server-2013"></a><span data-ttu-id="27775-103">Test de la connexion utilisateur à la messagerie unifiée Exchange dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27775-103">Testing user connection to Exchange UM in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="27775-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="27775-104">

<span> </span></span></span>

<span data-ttu-id="27775-105">_**Dernière modification de la rubrique :** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="27775-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27775-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="27775-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="27775-107">Jour</span><span class="sxs-lookup"><span data-stu-id="27775-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27775-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="27775-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="27775-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="27775-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27775-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="27775-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="27775-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="27775-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="27775-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande <strong>test-CsExUMConnectivity</strong> .</span><span class="sxs-lookup"><span data-stu-id="27775-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsExUMConnectivity</strong> cmdlet.</span></span> <span data-ttu-id="27775-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="27775-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsExUMConnectivity&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="27775-114">Description</span><span class="sxs-lookup"><span data-stu-id="27775-114">Description</span></span>

<span data-ttu-id="27775-115">L’applet de **contrôle test-CsExUMConnectivity** vérifie que l’utilisateur spécifié est en mesure de se connecter au service de messagerie unifiée Microsoft Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="27775-115">The **Test-CsExUMConnectivity** cmdlet verifies that the specified user can connect to the Microsoft Exchange Server 2013 unified messaging service.</span></span> <span data-ttu-id="27775-116">Notez que cette cmdlet vérifie uniquement qu’une connexion peut être établie au service.</span><span class="sxs-lookup"><span data-stu-id="27775-116">Note that this cmdlet only verifies that a connection can be made to the service.</span></span> <span data-ttu-id="27775-117">Le service proprement dit n’est pas testé.</span><span class="sxs-lookup"><span data-stu-id="27775-117">It does not test the service itself.</span></span> <span data-ttu-id="27775-118">Pour tester le service de messagerie unifiée (en exécutant une cmdlet de transaction synthétique qui quitte réellement un message de messagerie vocale dans la boîte aux lettres de l’utilisateur), utilisez l’applet de contrôle Test-CsExUMVoiceMail.</span><span class="sxs-lookup"><span data-stu-id="27775-118">To test the unified messaging service (by running a synthetic transaction cmdlet that actually leaves a voice mail message in a user's mailbox) use the Test-CsExUMVoiceMail cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="27775-119">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="27775-119">Running the test</span></span>

<span data-ttu-id="27775-120">L’exemple suivant teste la connectivité de messagerie unifiée Exchange pour le pool atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="27775-120">The following example tests Exchange Unified Messaging connectivity for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="27775-121">Cette commande ne fonctionnera que si les utilisateurs de test étaient définis pour le pool atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="27775-121">This command will work only if test users were defined for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="27775-122">Si tel est le cas, la commande détermine si le premier utilisateur de test peut se connecter à la messagerie unifiée.</span><span class="sxs-lookup"><span data-stu-id="27775-122">If they have, then the command will determine whether the first test user can connect to Unified Messaging.</span></span> <span data-ttu-id="27775-123">Si les utilisateurs test n’ont pas été configurés pour le pool, la commande échoue.</span><span class="sxs-lookup"><span data-stu-id="27775-123">If test users were not configured for the pool then the command will fail.</span></span>

    Test-CsExUMConnectivity -TargetFqdn "atl-cs-001.litwareinc.com" 

<span data-ttu-id="27775-124">Les commandes indiquées dans l’exemple suivant testent la connectivité de messagerie unifiée Exchange pour l’utilisateur litwareinc \\ kenmyer.</span><span class="sxs-lookup"><span data-stu-id="27775-124">The commands shown in the following example test Exchange Unified Messaging connectivity for the user litwareinc\\kenmyer.</span></span> <span data-ttu-id="27775-125">Pour ce faire, la première commande de l’exemple utilise l’applet de commande **Get-Credential** pour créer un objet d’information d’identification d’interface de ligne de commande Windows PowerShell pour l’utilisateur litwareinc \\ kenmyer.</span><span class="sxs-lookup"><span data-stu-id="27775-125">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credentials object for the user litwareinc\\kenmyer.</span></span> <span data-ttu-id="27775-126">Notez que vous devez fournir le mot de passe de ce compte pour créer un objet d’informations d’identification valide et garantir que l’applet de contrôle **CsExUMConnectivity** puisse exécuter sa vérification.</span><span class="sxs-lookup"><span data-stu-id="27775-126">Note that you must supply the password for this account to create a valid credentials object and to ensure that the **Test-CsExUMConnectivity** cmdlet can run its check.</span></span>

<span data-ttu-id="27775-127">La deuxième commande de l’exemple utilise l’objet Credentials fourni ($x) et l’adresse SIP de l’utilisateur litwareinc \\ kenmyer pour déterminer si l’utilisateur peut se connecter à la messagerie unifiée Exchange.</span><span class="sxs-lookup"><span data-stu-id="27775-127">The second command in the example uses the supplied credentials object ($x) and the SIP address of the user litwareinc\\kenmyer to determine whether or this user can connect to Exchange Unified Messaging.</span></span>

    $credential = Get-Credential "litwareinc\kenmyer" 
    Test-CsExUMConnectivity -TargetFqdn "atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="27775-128">Dans l’exemple qui suit, la commande est une variante de la commande qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="27775-128">The command shown in the next example is a variation of the command just shown.</span></span> <span data-ttu-id="27775-129">Dans ce cas, le paramètre OutLoggerVariable est inclus pour générer un journal détaillé de chaque étape réalisée par le **test-CsExUMConnectivity** cmdletand le succès ou l’échec de chacune de ces étapes.</span><span class="sxs-lookup"><span data-stu-id="27775-129">In this case, the OutLoggerVariable parameter is included to generate a detailed log of every step done by the **Test-CsExUMConnectivity** cmdletand the success or failure of each of those steps.</span></span> <span data-ttu-id="27775-130">Pour ce faire, le paramètre OutLoggerVariable est ajouté avec la valeur de paramètre ExumText ; les informations de journalisation détaillées sont alors stockées dans une variable nommée $ExumTest.</span><span class="sxs-lookup"><span data-stu-id="27775-130">To do this, the OutLoggerVariable parameter is added together with the parameter value ExumText; that causes detailed logging information to be stored in a variable named $ExumTest.</span></span> <span data-ttu-id="27775-131">Dans la commande final de l’exemple, la méthode ToXML () est utilisée pour convertir les informations du journal au format XML.</span><span class="sxs-lookup"><span data-stu-id="27775-131">In the final command in the example, the ToXML() method is used to convert the log information to XML format.</span></span> <span data-ttu-id="27775-132">Ces données XML sont alors écrites dans un fichier nommé C : \\ LogsExumTest.xml à \\ l’aide de l’applet de Out-File cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27775-132">That XML data is then written to a file that is named C:\\Logs\\ExumTest.xml by using the Out-File cmdlet.</span></span>

    $credential = Get-Credential "litwareinc\kenmyer" 
    Test-CsExUMConnectivity -TargetFqdn "atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential -OutLoggerVariable ExumTest 
    $ExumTest.ToXML() | Out-File C:\Logs\ExumTest.xml 

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="27775-133">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="27775-133">Determining success or failure</span></span>

<span data-ttu-id="27775-134">Si l’intégration Exchange est correctement configurée, vous recevrez une sortie similaire à celle-ci, avec la propriété Result marquée comme **réussie**:</span><span class="sxs-lookup"><span data-stu-id="27775-134">If Exchange integration is correctly configured, you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="27775-135">Nom de domaine complet (FQDN) cible : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="27775-135">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="27775-136">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="27775-136">Result : Success</span></span>

<span data-ttu-id="27775-137">Latence : 00:00:00</span><span class="sxs-lookup"><span data-stu-id="27775-137">Latency : 00:00:00</span></span>

<span data-ttu-id="27775-138">Message d’erreur :</span><span class="sxs-lookup"><span data-stu-id="27775-138">Error Message :</span></span>

<span data-ttu-id="27775-139">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="27775-139">Diagnosis :</span></span>

<span data-ttu-id="27775-140">Si l’utilisateur spécifié ne peut pas recevoir de notifications, le résultat est affiché en tant qu' **échec** et des informations supplémentaires sont enregistrées dans les propriétés d’erreur et de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="27775-140">If the specified user can't receive notifications, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="27775-141">Nom de domaine complet (FQDN) cible : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="27775-141">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="27775-142">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="27775-142">Result : Failure</span></span>

<span data-ttu-id="27775-143">Latence : 00:00:00</span><span class="sxs-lookup"><span data-stu-id="27775-143">Latency : 00:00:00</span></span>

<span data-ttu-id="27775-144">Message d’erreur : 10060, une tentative de connexion a échoué car la partie connectée</span><span class="sxs-lookup"><span data-stu-id="27775-144">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="27775-145">ne répond pas correctement après un certain temps, ou</span><span class="sxs-lookup"><span data-stu-id="27775-145">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="27775-146">échec de la connexion établie, car l’hôte connecté a</span><span class="sxs-lookup"><span data-stu-id="27775-146">established connection failed because connected host has</span></span>

<span data-ttu-id="27775-147">échec de la réponse à 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="27775-147">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="27775-148">Exception interne : une tentative de connexion a échoué, car le</span><span class="sxs-lookup"><span data-stu-id="27775-148">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="27775-149">la fête connectée ne répond pas correctement après un délai de</span><span class="sxs-lookup"><span data-stu-id="27775-149">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="27775-150">heure ou échec de la connexion en raison d’un hôte connecté</span><span class="sxs-lookup"><span data-stu-id="27775-150">time, or established connection failed because connected host</span></span>

<span data-ttu-id="27775-151">échec de la réponse à 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="27775-151">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="27775-152">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="27775-152">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="27775-153">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="27775-153">Reasons why the test might have failed</span></span>

<span data-ttu-id="27775-154">Voici quelques raisons courantes pour lesquelles **les tests-CsExUMConnectivity** peuvent échouer :</span><span class="sxs-lookup"><span data-stu-id="27775-154">Here are some common reasons why **Test-CsExUMConnectivity** might fail:</span></span>

  - <span data-ttu-id="27775-155">Une valeur de paramètre incorrecte a été fournie.</span><span class="sxs-lookup"><span data-stu-id="27775-155">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="27775-156">S’il est utilisé, les paramètres facultatifs doivent être correctement configurés ou le test échoue.</span><span class="sxs-lookup"><span data-stu-id="27775-156">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="27775-157">Réexécutez la commande sans les paramètres facultatifs et déterminez si l’opération aboutit.</span><span class="sxs-lookup"><span data-stu-id="27775-157">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="27775-158">Si le serveur Exchange n’est pas configuré correctement ou n’est pas encore déployé, cette commande échoue.</span><span class="sxs-lookup"><span data-stu-id="27775-158">This command will fail if the Exchange Server is misconfigured or not yet deployed.</span></span>

  - <span data-ttu-id="27775-159">Cette commande échoue si le serveur Exchange n’est pas joignable sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="27775-159">This command will fail if the Exchange Server is not reachable over your network.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="27775-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27775-160">See Also</span></span>


[<span data-ttu-id="27775-161">Test-CsExUMVoiceMail</span><span class="sxs-lookup"><span data-stu-id="27775-161">Test-CsExUMVoiceMail</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsExUMVoiceMail)  
  

<span data-ttu-id="27775-162"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="27775-162"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

