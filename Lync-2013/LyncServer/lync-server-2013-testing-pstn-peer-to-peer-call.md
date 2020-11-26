---
title: 'Lync Server 2013 : test de l’appel d’égal à égal PSTN'
description: 'Lync Server 2013 : test d’appel RTC d’égal à égal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing PSTN peer to peer call
ms:assetid: 7e128eef-9ada-49b4-940f-97d7d13f1e4a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690131(v=OCS.15)
ms:contentKeyID: 63969622
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8bf8726c46374e3a799b986e071566d0ae1de138
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439799"
---
# <a name="testing-pstn-peer-to-peer-call-in-lync-server-2013"></a><span data-ttu-id="e9084-103">Test de l’appel d’égal à égal RTC dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e9084-103">Testing PSTN peer to peer call in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e9084-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e9084-104">

<span> </span></span></span>

<span data-ttu-id="e9084-105">_**Dernière modification de la rubrique :** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="e9084-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9084-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="e9084-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="e9084-107">Jour</span><span class="sxs-lookup"><span data-stu-id="e9084-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9084-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="e9084-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="e9084-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e9084-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9084-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="e9084-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="e9084-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="e9084-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="e9084-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsPstnPeerToPeerCall.</span><span class="sxs-lookup"><span data-stu-id="e9084-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsPstnPeerToPeerCall cmdlet.</span></span> <span data-ttu-id="e9084-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="e9084-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPstnPeerToPeerCall&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="e9084-114">Description</span><span class="sxs-lookup"><span data-stu-id="e9084-114">Description</span></span>

<span data-ttu-id="e9084-115">L’applet de connexion Test-CsPstnPeerToPeerCall vérifie la possibilité pour une paire d’utilisateurs d’effectuer un appel d’égal à égal sur la passerelle RTC (réseau téléphonique commuté).</span><span class="sxs-lookup"><span data-stu-id="e9084-115">The Test-CsPstnPeerToPeerCall cmdlet verifies the ability a pair of users has to conduct a peer-to-peer call over the public switched telephone network (PSTN) gateway.</span></span> <span data-ttu-id="e9084-116">Lorsque vous appelez test-CsPstnPeerToPeerCall, l’applet de connexion tente d’abord de se connecter à deux utilisateurs de test sur Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e9084-116">When you call Test-CsPstnPeerToPeerCall, the cmdlet will first attempt to log on two test users to Lync Server.</span></span> <span data-ttu-id="e9084-117">En supposant que les ouvertures de session aboutissent, l’applet de connexion a alors une tentative d’appel de la part de l’utilisateur 2 par le biais de la passerelle RTC.</span><span class="sxs-lookup"><span data-stu-id="e9084-117">Assuming that the logons succeed, the cmdlet will then have user 1 attempt to call user 2 over the PSTN gateway.</span></span> <span data-ttu-id="e9084-118">Test-CsPstnPeerToPeerCall effectuera cet appel en utilisant le plan de numérotation, la stratégie vocale et d’autres paramètres de stratégie et de configuration attribués à l’utilisateur de test.</span><span class="sxs-lookup"><span data-stu-id="e9084-118">Test-CsPstnPeerToPeerCall will make this call using the dial plan, voice policy, and other policy and configuration settings assigned to the test user.</span></span> <span data-ttu-id="e9084-119">Si le test s’exécute comme prévu, l’applet de connexion vérifie que l’utilisateur 2 a pu répondre à l’appel, puis déconnecte les deux comptes de test du système.</span><span class="sxs-lookup"><span data-stu-id="e9084-119">If the test goes as planned, the cmdlet will verify that user 2 was able to answer the call, and then log off both test accounts from the system.</span></span>

<span data-ttu-id="e9084-120">Test-CsPstnPeerToPeerCall effectue un appel téléphonique réel et vérifie qu’il est possible d’établir une connexion et qu’elle transmet également des codes DTMF sur le réseau pour déterminer si le média peut être envoyé sur la connexion.</span><span class="sxs-lookup"><span data-stu-id="e9084-120">Test-CsPstnPeerToPeerCall makes an actual phone call, one that verifies that a connection can be made and that also transmits DTMF codes over the network to determine whether media can be sent over the connection.</span></span> <span data-ttu-id="e9084-121">L’appel est alors reçu par l’applet de demande et aucune terminaison manuelle de l’appel n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e9084-121">The call is answered by the cmdlet itself, and no manual termination of the call is necessary.</span></span> <span data-ttu-id="e9084-122">(Autrement dit, personne ne doit répondre et raccrocher le téléphone appelé.)</span><span class="sxs-lookup"><span data-stu-id="e9084-122">(That is, no one must answer and then hang up the phone that was called.)</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="e9084-123">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="e9084-123">Running the test</span></span>

<span data-ttu-id="e9084-124">Vous pouvez exécuter l’applet de cmdlet Test-CsPstnPeerToPeerCall à l’aide d’une paire de comptes de test préconfigurés (voir Configuration de comptes de test pour exécuter des tests Lync Server) ou les comptes de tous les utilisateurs qui sont activés pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e9084-124">The Test-CsPstnPeerToPeerCall cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="e9084-125">Pour exécuter cette vérification à l’aide de comptes de test, vous devez simplement spécifier le nom de domaine complet (FQDN) du pool de serveurs Lync testé.</span><span class="sxs-lookup"><span data-stu-id="e9084-125">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="e9084-126">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e9084-126">For example:</span></span>

`Test-CsPstnPeerToPeerCall -TargetFqdn "atl-cs-001.litwareinc.com"`

<span data-ttu-id="e9084-127">Pour exécuter ce contrôle à l’aide de comptes d’utilisateurs réels, vous devez créer deux objets d’informations d’identification Windows PowerShell (objets contenant le nom de compte et le mot de passe) pour chaque compte.</span><span class="sxs-lookup"><span data-stu-id="e9084-127">To run this check using actual user accounts, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="e9084-128">Vous devez alors inclure ces objets d’informations d’identification et les adresses SIP des deux comptes lors de l’appel de test-CsPstnPeerToPeerCall :</span><span class="sxs-lookup"><span data-stu-id="e9084-128">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsPstnPeerToPeerCall:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsPstnPeerToPeerCall -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

<span data-ttu-id="e9084-129">Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsPstnPeerToPeerCall](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnPeerToPeerCall) .</span><span class="sxs-lookup"><span data-stu-id="e9084-129">For more information, see the Help documentation for the [Test-CsPstnPeerToPeerCall](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnPeerToPeerCall) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="e9084-130">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="e9084-130">Determining success or failure</span></span>

<span data-ttu-id="e9084-131">Si les utilisateurs spécifiés peuvent effectuer un appel d’égal à égal, vous recevrez une sortie semblable à celle-ci, avec la propriété Result marquée comme **réussie :**</span><span class="sxs-lookup"><span data-stu-id="e9084-131">If the specified users can complete a peer-to-peer call, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="e9084-132">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="e9084-132">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="e9084-133">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="e9084-133">Result : Success</span></span>

<span data-ttu-id="e9084-134">Latence : 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="e9084-134">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="e9084-135">Error</span><span class="sxs-lookup"><span data-stu-id="e9084-135">Error :</span></span>

<span data-ttu-id="e9084-136">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="e9084-136">Diagnosis :</span></span>

<span data-ttu-id="e9084-137">Si les utilisateurs spécifiés ne parviennent pas à effectuer un appel d’égal à égal, le résultat est affiché en tant qu’échec et des informations supplémentaires seront enregistrées dans les propriétés d’erreur et de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="e9084-137">If the specified users can't complete a peer-to-peer call, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="e9084-138">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="e9084-138">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="e9084-139">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="e9084-139">Result : Failure</span></span>

<span data-ttu-id="e9084-140">Latence : 00:00:0182361</span><span class="sxs-lookup"><span data-stu-id="e9084-140">Latency : 00:00:0182361</span></span>

<span data-ttu-id="e9084-141">Erreur : 403, interdit</span><span class="sxs-lookup"><span data-stu-id="e9084-141">Error : 403, Forbidden</span></span>

<span data-ttu-id="e9084-142">Diagnostic : codeerreur = 12001, source = ATL-CS-001.litwareinc.com,</span><span class="sxs-lookup"><span data-stu-id="e9084-142">Diagnosis : ErrorCode=12001,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="e9084-143">Raison = la stratégie utilisateur ne contient pas l’utilisation de l’itinéraire du téléphone</span><span class="sxs-lookup"><span data-stu-id="e9084-143">Reason=User Policy does not contain phone route usage</span></span>

<span data-ttu-id="e9084-144">La sortie précédente indique que le test a échoué, car la stratégie vocale affectée à au moins un des utilisateurs spécifiés n’inclut pas une utilisation du téléphone.</span><span class="sxs-lookup"><span data-stu-id="e9084-144">The previous output states that the test failed because the voice policy assigned to at least one of the specified users does not include a phone usage.</span></span> <span data-ttu-id="e9084-145">(Les utilisations du téléphone lient les politiques vocales aux itinéraires vocaux.</span><span class="sxs-lookup"><span data-stu-id="e9084-145">(Phone usages tie voice policies to voice routes.</span></span> <span data-ttu-id="e9084-146">Sans qu’il s’agissait d’une stratégie vocale et d’un itinéraire vocal correspondant, vous ne pouvez pas passer d’appels sur PSTN.)</span><span class="sxs-lookup"><span data-stu-id="e9084-146">Without both a voice policy and a corresponding voice route, you can't make calls over the PSTN.)</span></span>

<span data-ttu-id="e9084-147">Si Test-CsPstnPeerToPeerCall échoue, il est possible que vous souhaitiez réexécuter le test, cette fois-ci, y compris le paramètre Verbose :</span><span class="sxs-lookup"><span data-stu-id="e9084-147">If Test-CsPstnPeerToPeerCall fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsPstnPeerToPeerCall -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="e9084-148">Lorsque le paramètre Verbose est inclus, Test-CsPstnPeerToPeerCall renvoie un compte étape par étape de chaque action qu’il a effectuée lors de la vérification de la capacité de l’utilisateur spécifié à se connecter à Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e9084-148">When the Verbose parameter is included, Test-CsPstnPeerToPeerCall will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="e9084-149">Par exemple, cette sortie indique que des problèmes réseau empêchent une connexion avec le RTC :</span><span class="sxs-lookup"><span data-stu-id="e9084-149">For example, this output indicates that network problems are preventing a connection with the PSTN:</span></span>

<span data-ttu-id="e9084-150">Etablissement d’un appel vidéo audio sur’SIP : + 12065551219@litwareinc. com ; utilisateur = téléphone'.</span><span class="sxs-lookup"><span data-stu-id="e9084-150">Establishing Audio Video call to 'sip:+12065551219@litwareinc.com;user=phone'.</span></span>

<span data-ttu-id="e9084-151">Une exception «une 404 (non trouvée) a été reçue du réseau et l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="e9084-151">An exception 'A 404 (Not Found) response was received from the network and the operation failed.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="e9084-152">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="e9084-152">Reasons why the test might have failed</span></span>

<span data-ttu-id="e9084-153">Voici quelques raisons courantes pour lesquelles Test-CsPstnPeerToPeerCall risque d’échouer :</span><span class="sxs-lookup"><span data-stu-id="e9084-153">Here are some common reasons why Test-CsPstnPeerToPeerCall might fail:</span></span>

  - <span data-ttu-id="e9084-154">Vous avez spécifié un compte d’utilisateur qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e9084-154">You specified a user account that is not valid.</span></span> <span data-ttu-id="e9084-155">Vous pouvez vérifier qu’un compte d’utilisateur existe en exécutant une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="e9084-155">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="e9084-156">Le compte d’utilisateur est valide, mais le compte n’est pas activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e9084-156">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="e9084-157">Pour vérifier qu’un compte d’utilisateur est activé pour Lync Server, exécutez une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="e9084-157">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="e9084-158">Si la propriété Enabled est définie sur false, cela signifie que l’utilisateur n’est actuellement pas activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e9084-158">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="e9084-159">La stratégie vocale attribuée à l’utilisateur spécifié ne dispose pas d’une utilisation PSTN valide.</span><span class="sxs-lookup"><span data-stu-id="e9084-159">The voice policy assigned to the specified user does not have a valid PSTN usage.</span></span> <span data-ttu-id="e9084-160">Vous pouvez déterminer la politique vocale affectée à un utilisateur à l’aide d’une commande similaire à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="e9084-160">You can determine the voice policy that is assigned to a user by using a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object VoicePolicy
    
    <span data-ttu-id="e9084-161">Vous pouvez ensuite déterminer les utilisations RTC qui sont affectées à cette stratégie à l’aide d’une commande similaire à ce qui suit, qui extrait des informations sur le RedmondVoicePolicy de stratégie vocale par utilisateur :</span><span class="sxs-lookup"><span data-stu-id="e9084-161">And then you can determine the PSTN usages (if any) that are assigned to that policy by using a command similar to the following, which retrieves information about the per-user voice policy RedmondVoicePolicy:</span></span>
    
        Get-CsVoicePolicy -Identity "RedmondVoicePolicy"

<span data-ttu-id="e9084-162"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e9084-162"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

