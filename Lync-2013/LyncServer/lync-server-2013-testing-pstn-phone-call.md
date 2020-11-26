---
title: 'Lync Server 2013 : test d’appel téléphonique PSTN'
description: 'Lync Server 2013 : test d’appel téléphonique PSTN.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing PSTN phone call
ms:assetid: dc7d319d-a627-45b6-a978-6111901251e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690133(v=OCS.15)
ms:contentKeyID: 63969656
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b42ea6dd46145961a34386d704f8f44e9b7909ad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439764"
---
# <a name="testing-pstn-phone-call-in-lync-server-2013"></a><span data-ttu-id="36fa3-103">Test de l’appel téléphonique PSTN dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36fa3-103">Testing PSTN phone call in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="36fa3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="36fa3-104">

<span> </span></span></span>

<span data-ttu-id="36fa3-105">_**Dernière modification de la rubrique :** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="36fa3-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36fa3-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="36fa3-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="36fa3-107">Jour</span><span class="sxs-lookup"><span data-stu-id="36fa3-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36fa3-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="36fa3-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="36fa3-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="36fa3-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36fa3-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="36fa3-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="36fa3-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="36fa3-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="36fa3-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsRegistration.</span><span class="sxs-lookup"><span data-stu-id="36fa3-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsRegistration cmdlet.</span></span> <span data-ttu-id="36fa3-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="36fa3-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPstnOutboundCall&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="36fa3-114">Description</span><span class="sxs-lookup"><span data-stu-id="36fa3-114">Description</span></span>

<span data-ttu-id="36fa3-115">L’applet de passe Test-CsPstnOutboundCall teste la possibilité pour un utilisateur de passer un appel vers un numéro de téléphone situé sur le RTC.</span><span class="sxs-lookup"><span data-stu-id="36fa3-115">The Test-CsPstnOutboundCall cmdlet tests the ability of a user to make a call to a phone number located on the PSTN.</span></span> <span data-ttu-id="36fa3-116">Lorsque vous exécutez test-CsPstnOutboundCall, l’applet de connexion tente d’abord de consigner l’utilisateur de test sur Lync Server.</span><span class="sxs-lookup"><span data-stu-id="36fa3-116">When you run Test-CsPstnOutboundCall, the cmdlet first attempts to log the test user on to Lync Server.</span></span> <span data-ttu-id="36fa3-117">En cas de réussite de l’ouverture de session, l’applet de passe tente alors d’effectuer un appel téléphonique via la passerelle RTC.</span><span class="sxs-lookup"><span data-stu-id="36fa3-117">If the logon succeeds, the cmdlet will then try to make a phone call across the PSTN gateway.</span></span> <span data-ttu-id="36fa3-118">Cet appel téléphonique sera réalisé à l’aide du plan de numérotation, de la politique vocale et d’autres stratégies et paramètres attribués au compte de test.</span><span class="sxs-lookup"><span data-stu-id="36fa3-118">This phone call will be made using the dial plan, voice policy, and other policies and settings assigned to the test account.</span></span> <span data-ttu-id="36fa3-119">Lorsque l’appel est reçu, l’applet de connexion envoie des codes à deux tonalités (DTMF) sur le réseau pour vérifier la connectivité multimédia.</span><span class="sxs-lookup"><span data-stu-id="36fa3-119">When the call is answered, the cmdlet sends dual-tone multi-frequency (DTMF) codes over the network to verify media connectivity.</span></span>

<span data-ttu-id="36fa3-120">Lors de ses tests, Test-CsPstnOutboundCall effectue un appel réel : le téléphone cible sonne et répond au succès du test.</span><span class="sxs-lookup"><span data-stu-id="36fa3-120">When conducting its test, Test-CsPstnOutboundCall will make an actual phone call: the target phone will ring and must be answered for the test to succeed.</span></span> <span data-ttu-id="36fa3-121">Cet appel doit également être arrêté manuellement par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="36fa3-121">This call must also be manually ended by the administrator.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="36fa3-122">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="36fa3-122">Running the test</span></span>

<span data-ttu-id="36fa3-123">Vous pouvez exécuter l’applet de contrôle Test-CsPstnOutboundCall à l’aide d’un compte de test préconfiguré (voir Configuration de comptes de test pour exécuter des tests Lync Server) ou du compte d’un utilisateur qui est activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="36fa3-123">The Test-CsPstnOutboundCall cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="36fa3-124">Pour effectuer cette vérification à l’aide d’un compte de test, vous devez simplement spécifier le nom de domaine complet (FQDN) du pool de serveurs Lync testé et le numéro de téléphone RTC appelé.</span><span class="sxs-lookup"><span data-stu-id="36fa3-124">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested and the PSTN phone number being called.</span></span> <span data-ttu-id="36fa3-125">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="36fa3-125">For example:</span></span>

    Test-CsPstnOutboundCall -TargetFqdn "atl-cs-001.litwareinc.com" -TargetPstnPhoneNumber "+12065551219"

<span data-ttu-id="36fa3-126">Pour effectuer cette vérification à l’aide d’un compte d’utilisateur réel, vous devez d’abord créer un objet d’informations d’identification Windows PowerShell contenant le nom et le mot de passe du compte.</span><span class="sxs-lookup"><span data-stu-id="36fa3-126">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="36fa3-127">Vous devez alors inclure cet objet Credential et l’adresse SIP attribuée au compte lorsque vous appelez le test-CsPstnOutboundCall :</span><span class="sxs-lookup"><span data-stu-id="36fa3-127">You must then include that credentials object and the SIP address assigned to the account when you call Test-CsPstnOutboundCall:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsPstnOutboundCall -TargetFqdn "atl-cs-001.litwareinc.com" -TargetPstnPhoneNumber "+12065551219" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="36fa3-128">Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsPstnOutboundCall](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnOutboundCall) .</span><span class="sxs-lookup"><span data-stu-id="36fa3-128">For more information, see the Help documentation for the [Test-CsPstnOutboundCall](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnOutboundCall) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="36fa3-129">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="36fa3-129">Determining success or failure</span></span>

<span data-ttu-id="36fa3-130">Si l’utilisateur spécifié peut effectuer l’appel et si l’appel est reçu, vous recevrez une sortie semblable à ce qui suit, avec la propriété Result marquée comme **réussie :**</span><span class="sxs-lookup"><span data-stu-id="36fa3-130">If the specified user can make the call, and if the call is answered, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="36fa3-131">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="36fa3-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="36fa3-132">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="36fa3-132">Result : Success</span></span>

<span data-ttu-id="36fa3-133">Latence : 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="36fa3-133">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="36fa3-134">Error</span><span class="sxs-lookup"><span data-stu-id="36fa3-134">Error :</span></span>

<span data-ttu-id="36fa3-135">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="36fa3-135">Diagnosis :</span></span>

<span data-ttu-id="36fa3-136">Si l’utilisateur spécifié ne peut pas effectuer l’appel ou si l’appel n’a pas de réponse, le résultat s’affichera en tant qu’échec et des informations supplémentaires seront enregistrées dans les propriétés d’erreur et de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="36fa3-136">If the specified user can't make the call or if the call is not answered, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="36fa3-137">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="36fa3-137">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="36fa3-138">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="36fa3-138">Result : Failure</span></span>

<span data-ttu-id="36fa3-139">Latence : 00:00:0987365</span><span class="sxs-lookup"><span data-stu-id="36fa3-139">Latency : 00:00:0987365</span></span>

<span data-ttu-id="36fa3-140">Erreur : 403, interdit</span><span class="sxs-lookup"><span data-stu-id="36fa3-140">Error : 403, Forbidden</span></span>

<span data-ttu-id="36fa3-141">Diagnostic : codeerreur = 12001, source = ATL-CS-001. litwareinc. com, Reason = utilisateur</span><span class="sxs-lookup"><span data-stu-id="36fa3-141">Diagnosis : ErrorCode=12001,Source=atl-cs-001.litwareinc.com,Reason=User</span></span>

<span data-ttu-id="36fa3-142">La stratégie ne contient pas l’utilisation de l’itinéraire du téléphone</span><span class="sxs-lookup"><span data-stu-id="36fa3-142">Policy does not contain phone route usage</span></span>

<span data-ttu-id="36fa3-143">La sortie précédente indique que le test a échoué, car la stratégie vocale affectée à l’utilisateur spécifié n’inclut pas une utilisation du téléphone.</span><span class="sxs-lookup"><span data-stu-id="36fa3-143">The previous output states that the test failed because the voice policy assigned to the specified user does not include a phone usage.</span></span> <span data-ttu-id="36fa3-144">(Les utilisations du téléphone lient les politiques vocales aux itinéraires vocaux.</span><span class="sxs-lookup"><span data-stu-id="36fa3-144">(Phone usages tie voice policies to voice routes.</span></span> <span data-ttu-id="36fa3-145">Sans qu’il s’agissait d’une stratégie vocale et d’un itinéraire vocal correspondant, vous ne pouvez pas passer d’appels sur PSTN.)</span><span class="sxs-lookup"><span data-stu-id="36fa3-145">Without both a voice policy and a corresponding voice route you can't make calls over the PSTN.)</span></span>

<span data-ttu-id="36fa3-146">Si Test-CsPstnOutboundCall échoue, vous souhaiterez peut-être réexécuter le test, cette fois-ci, y compris le paramètre Verbose :</span><span class="sxs-lookup"><span data-stu-id="36fa3-146">If Test-CsPstnOutboundCall fails then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsPstnOutboundCall -TargetFqdn "atl-cs-001.litwareinc.com" -TargetPstnPhoneNumber "+12065551219" -Verbose

<span data-ttu-id="36fa3-147">Lorsque le paramètre Verbose est inclus, Test-CsPstnOutboundCall renvoie un compte étape par étape de chaque action qu’il a effectuée lors de la vérification de la capacité de l’utilisateur spécifié à se connecter à Lync Server.</span><span class="sxs-lookup"><span data-stu-id="36fa3-147">When the Verbose parameter is included, Test-CsPstnOutboundCall will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="36fa3-148">Par exemple, cette sortie indique que des problèmes réseau empêchent une connexion avec le RTC :</span><span class="sxs-lookup"><span data-stu-id="36fa3-148">For example, this output indicates that network problems are preventing a connection with the PSTN:</span></span>

<span data-ttu-id="36fa3-149">Etablissement d’un appel vidéo audio sur’SIP : + 12065551219@litwareinc. com ; utilisateur = téléphone'.</span><span class="sxs-lookup"><span data-stu-id="36fa3-149">Establishing Audio Video call to 'sip:+12065551219@litwareinc.com;user=phone'.</span></span>

<span data-ttu-id="36fa3-150">Une exception «une 404 (non trouvée) a été reçue du réseau et l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="36fa3-150">An exception 'A 404 (Not Found) response was received from the network and the operation failed.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="36fa3-151">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="36fa3-151">Reasons why the test might have failed</span></span>

<span data-ttu-id="36fa3-152">Voici quelques raisons courantes pour lesquelles Test-CsPstnOutboundCall risque d’échouer :</span><span class="sxs-lookup"><span data-stu-id="36fa3-152">Here are some common reasons why Test-CsPstnOutboundCall might fail:</span></span>

  - <span data-ttu-id="36fa3-153">Vous avez spécifié un compte d’utilisateur non valide.</span><span class="sxs-lookup"><span data-stu-id="36fa3-153">You specified an invalid user account.</span></span> <span data-ttu-id="36fa3-154">Vous pouvez vérifier qu’un compte d’utilisateur existe en exécutant une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="36fa3-154">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="36fa3-155">Le compte d’utilisateur est valide, mais le compte n’est pas activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="36fa3-155">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="36fa3-156">Pour vérifier qu’un compte d’utilisateur est activé pour Lync Server, exécutez une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="36fa3-156">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="36fa3-157">Si la propriété Enabled est définie sur false, cela signifie que l’utilisateur n’est actuellement pas activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="36fa3-157">If the Enabled property is set to False that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="36fa3-158">La stratégie vocale attribuée à l’utilisateur spécifié ne dispose pas d’une utilisation PSTN valide.</span><span class="sxs-lookup"><span data-stu-id="36fa3-158">The voice policy assigned to the specified user does not have a valid PSTN usage.</span></span> <span data-ttu-id="36fa3-159">Vous pouvez déterminer la politique vocale affectée à un utilisateur à l’aide d’une commande similaire à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="36fa3-159">You can determine the voice policy that is assigned to a user by using a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object VoicePolicy
    
    <span data-ttu-id="36fa3-160">Vous pouvez ensuite déterminer les utilisations RTC qui sont affectées à cette stratégie à l’aide d’une commande similaire à ce qui suit, qui extrait des informations sur le RedmondVoicePolicy de stratégie vocale par utilisateur :</span><span class="sxs-lookup"><span data-stu-id="36fa3-160">And then you can determine the PSTN usages (if any) that are assigned to that policy by using a command similar to the following, which retrieves information about the per-user voice policy RedmondVoicePolicy:</span></span>
    
        Get-CsVoicePolicy -Identity "RedmondVoicePolicy"

<span data-ttu-id="36fa3-161"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="36fa3-161"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

