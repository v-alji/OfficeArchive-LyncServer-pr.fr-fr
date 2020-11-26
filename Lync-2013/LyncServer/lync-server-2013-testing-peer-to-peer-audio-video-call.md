---
title: 'Lync Server 2013 : test des appels audio et vidéo d’égal à égal'
description: 'Lync Server 2013 : test des appels audio et vidéo d’égal à égal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing peer to peer audio/video call
ms:assetid: 95eb3693-b866-4652-bc45-9b75fdb40b49
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743835(v=OCS.15)
ms:contentKeyID: 63969627
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 03bab69d926a99c091a510ce64b78dbf505d4cbc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439813"
---
# <a name="testing-peer-to-peer-audiovideo-call-in-lync-server-2013"></a><span data-ttu-id="ef8f6-103">Test de l’appel audio/vidéo d’égal à égal dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ef8f6-103">Testing peer to peer audio/video call in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ef8f6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ef8f6-104">

<span> </span></span></span>

<span data-ttu-id="ef8f6-105">_**Dernière modification de la rubrique :** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="ef8f6-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef8f6-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="ef8f6-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="ef8f6-107">Jour</span><span class="sxs-lookup"><span data-stu-id="ef8f6-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef8f6-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="ef8f6-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="ef8f6-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ef8f6-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef8f6-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="ef8f6-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="ef8f6-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="ef8f6-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsP2PAV.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsP2PAV cmdlet.</span></span> <span data-ttu-id="ef8f6-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="ef8f6-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsP2PAV&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="ef8f6-114">Description</span><span class="sxs-lookup"><span data-stu-id="ef8f6-114">Description</span></span>

<span data-ttu-id="ef8f6-115">Test-CsP2PAV est utilisé pour déterminer si un binôme d’utilisateurs de test peut participer à une conversation A/V d’égal à égal.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-115">Test-CsP2PAV is used to determine whether a pair of test users can participate in a peer-to-peer A/V conversation.</span></span> <span data-ttu-id="ef8f6-116">Pour tester ce scénario, l’applet de connexion démarre en se connectant aux deux utilisateurs de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-116">To test this scenario, the cmdlet starts off by logging on the two users to Lync Server.</span></span> <span data-ttu-id="ef8f6-117">En supposant que les deux ouvertures de session aboutissent, le premier utilisateur invite alors le second utilisateur à rejoindre un appel A/V.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-117">Assuming that the two logons succeed, the first user then invites the second user to join an A/V call.</span></span> <span data-ttu-id="ef8f6-118">Le deuxième utilisateur accepte l’appel, le lien entre les deux utilisateurs est testé, puis l’appel est terminé et les utilisateurs de test sont déconnectés du système.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-118">The second user accepts the call, the connection between the two users is tested, and then the call is ended and the test users are logged off from the system.</span></span>

<span data-ttu-id="ef8f6-119">Test-CsP2PAV n’effectue pas réellement d’appel A/V.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-119">Test-CsP2PAV does not actually conduct an A/V call.</span></span> <span data-ttu-id="ef8f6-120">Les informations multimédias ne sont pas échangées entre les utilisateurs test.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-120">Multimedia information is not exchanged between the test users.</span></span> <span data-ttu-id="ef8f6-121">Au lieu de cela, l’applet de demande vérifie simplement que les connexions appropriées peuvent être établies et que les deux utilisateurs peuvent effectuer un tel appel.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-121">Instead, the cmdlet merely verifies that the appropriate connections can be made and that the two users can conduct such a call.</span></span>

<span data-ttu-id="ef8f6-122">Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsP2PAV](https://docs.microsoft.com/powershell/module/skype/Test-CsP2PAV) .</span><span class="sxs-lookup"><span data-stu-id="ef8f6-122">For more information, see the Help documentation for the [Test-CsP2PAV](https://docs.microsoft.com/powershell/module/skype/Test-CsP2PAV) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="ef8f6-123">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="ef8f6-123">Running the test</span></span>

<span data-ttu-id="ef8f6-124">Vous pouvez exécuter l’applet de cmdlet Test-CsP2PAV à l’aide d’une paire de comptes de test préconfigurés (voir Configuration de comptes de test pour exécuter des tests Lync Server) ou les comptes de tous les utilisateurs qui sont activés pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-124">The Test-CsP2PAV cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="ef8f6-125">Pour exécuter cette vérification à l’aide de comptes de test, vous devez simplement spécifier le nom de domaine complet (FQDN) du pool de serveurs Lync testé.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-125">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="ef8f6-126">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="ef8f6-126">For example:</span></span>

    Test-CsP2PAV -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="ef8f6-127">Pour exécuter cette vérification à l’aide de comptes d’utilisateurs réels, vous devez créer deux objets d’informations d’identification Lync Server (objets contenant le nom de compte et le mot de passe) pour chaque compte.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-127">To run this check using actual user accounts, you must create two Lync Server credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="ef8f6-128">Vous devez alors inclure ces objets d’informations d’identification et les adresses SIP des deux comptes lors de l’appel de test-CsP2PAV :</span><span class="sxs-lookup"><span data-stu-id="ef8f6-128">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsP2PAV:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsP2PAV -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="ef8f6-129">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="ef8f6-129">Determining success or failure</span></span>

<span data-ttu-id="ef8f6-130">Si les deux utilisateurs de test peuvent effectuer un appel A/V d’égal à égal, vous recevrez une sortie semblable à ce qui suit avec la propriété Result marquée comme **réussie :**</span><span class="sxs-lookup"><span data-stu-id="ef8f6-130">If the two test users can complete a peer-to-peer A/V call, then you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="ef8f6-131">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ef8f6-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="ef8f6-132">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="ef8f6-132">Result : Success</span></span>

<span data-ttu-id="ef8f6-133">Latence : 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="ef8f6-133">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="ef8f6-134">Error</span><span class="sxs-lookup"><span data-stu-id="ef8f6-134">Error :</span></span>

<span data-ttu-id="ef8f6-135">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="ef8f6-135">Diagnosis :</span></span>

<span data-ttu-id="ef8f6-136">Si les utilisateurs ne parviennent pas à effectuer l’appel, le résultat est affiché en tant qu’échec et des informations supplémentaires sont enregistrées dans les propriétés d’erreur et de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="ef8f6-136">If the test users can't complete the call, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="ef8f6-137">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ef8f6-137">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="ef8f6-138">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="ef8f6-138">Result : Failure</span></span>

<span data-ttu-id="ef8f6-139">Latence : 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ef8f6-139">Latency : 00:00:00</span></span>

<span data-ttu-id="ef8f6-140">Erreur : 480, temporairement indisponible</span><span class="sxs-lookup"><span data-stu-id="ef8f6-140">Error : 480, Temporarily Unavailable</span></span>

<span data-ttu-id="ef8f6-141">Diagnostic : codeerreur = 15030, source = ATL-CS-001. litwareinc. com ; raison = échec</span><span class="sxs-lookup"><span data-stu-id="ef8f6-141">Diagnosis : ErrorCode=15030,Source=atl-cs-001.litwareinc.com,Reason=Failed</span></span>

<span data-ttu-id="ef8f6-142">pour acheminer vers Exchange Server</span><span class="sxs-lookup"><span data-stu-id="ef8f6-142">to route to Exchange Server</span></span>

<span data-ttu-id="ef8f6-143">Microsoft. RTC. signalisation. DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="ef8f6-143">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="ef8f6-144">Par exemple, la sortie précédente indique que le test a échoué, car le serveur Microsoft Exchange n’a pas pu être contacté.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-144">For example, the previous output states that the test failed because the Microsoft Exchange Server couldn't be contacted.</span></span> <span data-ttu-id="ef8f6-145">Ce message d’erreur indique généralement un problème de configuration de la messagerie unifiée Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-145">This error message typically indicates a problem the configuration of Exchange Unified Messaging.</span></span>

<span data-ttu-id="ef8f6-146">Si Test-CsP2PAV échoue, vous souhaiterez peut-être réexécuter le test, cette fois-ci, y compris le paramètre Verbose :</span><span class="sxs-lookup"><span data-stu-id="ef8f6-146">If Test-CsP2PAV fails then you might want to rerun the test, this time including the Verbose parameter:</span></span>

<span data-ttu-id="ef8f6-147">Test-CsP2PAV-TargetFqdn "atl-cs-001.litwareinc.com"-détails</span><span class="sxs-lookup"><span data-stu-id="ef8f6-147">Test-CsP2PAV -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose</span></span>

<span data-ttu-id="ef8f6-148">Lorsque le paramètre Verbose est inclus, Test-CsP2PAV renvoie un compte étape par étape de chaque action qu’il a effectuée lors de la vérification de la capacité de l’utilisateur spécifié à se connecter à Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-148">When the Verbose parameter is included, Test-CsP2PAV will return a step-by-step account of each action it tried as it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="ef8f6-149">Par exemple, supposons que votre test ait échoué avec le diagnostic suivant :</span><span class="sxs-lookup"><span data-stu-id="ef8f6-149">For example, suppose that your test failed with the following Diagnosis:</span></span>

<span data-ttu-id="ef8f6-150">Codeerreur = 6003, source = ATL-CS-001. litwareinc. com ; raison = non prise en charge d’une demande de boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="ef8f6-150">ErrorCode=6003,Source=atl-cs-001.litwareinc.com,Reason=Unsupported out of dialog request</span></span>

<span data-ttu-id="ef8f6-151">Si vous réexécutez Test-CsP2PAV et incluez le paramètre Verbose, vous obtiendrez une sortie semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="ef8f6-151">If you rerun Test-CsP2PAV and include the Verbose parameter, you'll get output similar to this:</span></span>

<span data-ttu-id="ef8f6-152">DÉTAILLÉ : activité de’Register’démarrée.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-152">VERBOSE: 'Register' activity started.</span></span>

<span data-ttu-id="ef8f6-153">Envoi de la demande d’inscription :</span><span class="sxs-lookup"><span data-stu-id="ef8f6-153">Sending Registration request:</span></span>

<span data-ttu-id="ef8f6-154">Nom de domaine complet cible = atl-cs-011.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ef8f6-154">Target Fqdn = atl-cs-011.litwareinc.com</span></span>

<span data-ttu-id="ef8f6-155">Adresse SIP de l’utilisateur = sip :kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="ef8f6-155">User Sip Address = sip:kenmyer@litwareinc.com</span></span>

<span data-ttu-id="ef8f6-156">Port du Bureau d’enregistrement = 5062.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-156">Registrar Port = 5062.</span></span>

<span data-ttu-id="ef8f6-157">Le type d’authentification « IWA » est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-157">Auth Type 'IWA' is selected.</span></span>

<span data-ttu-id="ef8f6-158">Exception «le point de terminaison n’a pas pu s’inscrire.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-158">An exception 'The endpoint was unable to register.</span></span> <span data-ttu-id="ef8f6-159">Voir le code d’après pour une raison spécifique. '</span><span class="sxs-lookup"><span data-stu-id="ef8f6-159">See the ErrorCode for specific reason.'</span></span> <span data-ttu-id="ef8f6-160">Il s’est produit lors de l’exécution du flux de travail Microsoft. RTC. SyntheticTransactions. flux de travail. STP2PAVWorkflow.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-160">occurred during workflow Microsoft.Rtc.SyntheticTransactions.Workflows.STP2PAVWorkflow execution.</span></span>

<span data-ttu-id="ef8f6-161">Même si vous examinez soigneusement la sortie, il est possible que vous voyiez un port de Registre incorrect (port 5062).</span><span class="sxs-lookup"><span data-stu-id="ef8f6-161">Although it might not be immediately obvious, if you examine the output carefully you’ll see that an incorrect Registrar port (port 5062) was specified.</span></span> <span data-ttu-id="ef8f6-162">À son tour, cela a entraîné l’échec du test.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-162">In turn, that caused the test to fail.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="ef8f6-163">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="ef8f6-163">Reasons why the test might have failed</span></span>

<span data-ttu-id="ef8f6-164">Voici quelques raisons courantes pour lesquelles Test-CsP2PAV risque d’échouer :</span><span class="sxs-lookup"><span data-stu-id="ef8f6-164">Here are some common reasons why Test-CsP2PAV might fail:</span></span>

  - <span data-ttu-id="ef8f6-165">Vous avez spécifié un compte d’utilisateur qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-165">You specified a user account that is not valid.</span></span> <span data-ttu-id="ef8f6-166">Vous pouvez vérifier qu’un compte d’utilisateur existe en exécutant une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="ef8f6-166">You can verify that a user account exists by running a command similar to this:</span></span>
    
    <span data-ttu-id="ef8f6-167">Get-CsUser « sip :kenmyer@litwareinc.com »</span><span class="sxs-lookup"><span data-stu-id="ef8f6-167">Get-CsUser "sip:kenmyer@litwareinc.com"</span></span>

  - <span data-ttu-id="ef8f6-168">Le compte d’utilisateur est valide, mais le compte n’est pas activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-168">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="ef8f6-169">Pour vérifier qu’un compte d’utilisateur est activé pour Lync Server, exécutez une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="ef8f6-169">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="ef8f6-170">Si la propriété Enabled est définie sur false, cela signifie que l’utilisateur n’est actuellement pas activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ef8f6-170">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

<span data-ttu-id="ef8f6-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ef8f6-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

