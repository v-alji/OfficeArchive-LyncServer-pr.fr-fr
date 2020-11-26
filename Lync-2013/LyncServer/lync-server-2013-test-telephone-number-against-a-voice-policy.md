---
title: 'Lync Server 2013 : testez le numéro de téléphone en fonction de la politique vocale'
description: 'Lync Server 2013 : testez le numéro de téléphone en fonction de la politique vocale.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test telephone number against a voice policy
ms:assetid: 30c51700-17c6-4c57-891a-8d5ec30b50ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725207(v=OCS.15)
ms:contentKeyID: 63969596
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5a6523e7657bd4c30c23909bb02e2569b6067298
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441220"
---
# <a name="test-telephone-number-against-a-voice-policy-in-lync-server-2013"></a><span data-ttu-id="0aba4-103">Testez le numéro de téléphone en fonction de la politique vocale dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0aba4-103">Test telephone number against a voice policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0aba4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0aba4-104">

<span> </span></span></span>

<span data-ttu-id="0aba4-105">_**Dernière modification de la rubrique :** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="0aba4-105">_**Topic Last Modified:** 2014-05-20_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0aba4-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="0aba4-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="0aba4-107">Mois</span><span class="sxs-lookup"><span data-stu-id="0aba4-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0aba4-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="0aba4-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="0aba4-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0aba4-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0aba4-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="0aba4-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="0aba4-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="0aba4-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="0aba4-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsVoicePolicy.</span><span class="sxs-lookup"><span data-stu-id="0aba4-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsVoicePolicy cmdlet.</span></span> <span data-ttu-id="0aba4-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="0aba4-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsVoicePolicy&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="0aba4-114">Description</span><span class="sxs-lookup"><span data-stu-id="0aba4-114">Description</span></span>

<span data-ttu-id="0aba4-115">Possibilité pour les utilisateurs d’entreprise Voice de passer des appels sortants par le biais des charnières de réseau téléphonique commuté (RTC), en grande partie, sur les trois points suivants :</span><span class="sxs-lookup"><span data-stu-id="0aba4-115">The ability of Enterprise Voice users to make outgoing phone calls over the Public Switched Telephone network (PSTN) hinges, in large part, on three things:</span></span>

  - <span data-ttu-id="0aba4-116">La stratégie vocale affectée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0aba4-116">The voice policy assigned to the user.</span></span>

  - <span data-ttu-id="0aba4-117">Les itinéraires vocaux utilisés pour acheminer les appels de Lync Server vers le réseau PSTN.</span><span class="sxs-lookup"><span data-stu-id="0aba4-117">The voice routes used to route calls from Lync Server to the PSTN network.</span></span>

  - <span data-ttu-id="0aba4-118">L’utilisation RTC, propriété serveur Lync qui connecte une stratégie vocale à un itinéraire vocal.</span><span class="sxs-lookup"><span data-stu-id="0aba4-118">The PSTN usage, a Lync Server property that connects a voice policy to a voice route.</span></span>

<span data-ttu-id="0aba4-119">L’utilisation RTC est particulièrement importante : il s’agit de la propriété qui connecte une stratégie vocale à un itinéraire vocal.</span><span class="sxs-lookup"><span data-stu-id="0aba4-119">The PSTN usage is especially important: it’s the property that connects a voice policy to a voice route.</span></span> <span data-ttu-id="0aba4-120">(Une stratégie vocale et un itinéraire vocal sont considérés comme étant connectés s’ils ont au moins une utilisation PSTN en commun.) Les stratégies vocales peuvent être configurées sans spécifier d’utilisation PSTN.</span><span class="sxs-lookup"><span data-stu-id="0aba4-120">(A voice policy and a voice route are said to be connected if they have at least one PSTN usage in common.) Voice policies can be configured without specifying a PSTN usage.</span></span> <span data-ttu-id="0aba4-121">Dans ce cas, les utilisateurs qui ont été affectés à cette stratégie ne seront pas en mesure de passer des appels sortants sur le réseau PSTN.</span><span class="sxs-lookup"><span data-stu-id="0aba4-121">In that case, users who were assigned that policy won't be able to make outgoing calls over the PSTN network.</span></span> <span data-ttu-id="0aba4-122">De même, les itinéraires vocaux qui n’ont pas au moins une utilisation RTC spécifiée ne seront pas en mesure d’acheminer les appels vers le réseau PSTN.</span><span class="sxs-lookup"><span data-stu-id="0aba4-122">Likewise, voice routes that do not have at least one specified PSTN usage will be unable to route calls to the PSTN network.</span></span>

<span data-ttu-id="0aba4-123">L’applet de commande Test-CsVoicePolicy vérifie qu’une stratégie vocale donnée a une utilisation PSTN et que l’utilisation est partagée par au moins un itinéraire vocal.</span><span class="sxs-lookup"><span data-stu-id="0aba4-123">The Test-CsVoicePolicy cmdlet verifies that a given voice policy has a PSTN usage and that the usage is shared by at least one voice route.</span></span> <span data-ttu-id="0aba4-124">Si la vérification exécutée par Test-CsVoicePolicy réussit, l’applet de commande renvoie le nom du premier itinéraire vocal valide qu’il recherche, ainsi que le nom de l’utilisation RTC qui connecte la stratégie à l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="0aba4-124">If the verification run by Test-CsVoicePolicy succeeds, the cmdlet will report back the name of the first valid voice route it finds, and also the name of the PSTN usage that connects the policy to the route.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="0aba4-125">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="0aba4-125">Running the test</span></span>

<span data-ttu-id="0aba4-126">Pour exécuter l’applet de Get-CsVoicePolicy Test-CsVoicePolicy vous devez d’abord utiliser l’applet de pour récupérer une instance de la stratégie vocale à tester. cette instance doit alors être canalisée vers test-CsVoicePolicy.</span><span class="sxs-lookup"><span data-stu-id="0aba4-126">To run the Test-CsVoicePolicy cmdlet you must first use the Get-CsVoicePolicy cmdlet retrieve an instance of the voice policy to be tested; that instance must then be piped to Test-CsVoicePolicy.</span></span> <span data-ttu-id="0aba4-127">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="0aba4-127">For example:</span></span>

`Get-CsVoicePolicy -Identity "Global" | Test-CsVoicePolicy -TargetNumber "+12065551219"`

<span data-ttu-id="0aba4-128">Notez que cette commande, qui n’utilise pas Get-CsVoicePolicy pour récupérer une instance de la stratégie vocale, ne peut pas :</span><span class="sxs-lookup"><span data-stu-id="0aba4-128">Note that this command, which does not use Get-CsVoicePolicy to retrieve a voice policy instance, will fail:</span></span>

`Test-CsVoicePolicy -TargetNumber "+12065551219" -VoicePolicy "Global"`

<span data-ttu-id="0aba4-129">Si vous voulez cocher toutes les stratégies vocales sur un numéro de téléphone spécifié, utilisez une commande semblable à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="0aba4-129">If you want to check all the voice policies against a specified phone number then use a command similar to this:</span></span>

`Get-CsVoicePolicy | Test-CsVoicePolicy -TargetNumber "+12065551219"`

<span data-ttu-id="0aba4-130">Notez que TargetNumber doit être spécifié en utilisant le format E. 164.</span><span class="sxs-lookup"><span data-stu-id="0aba4-130">Note that the TargetNumber must be specified by using the E.164 format.</span></span> <span data-ttu-id="0aba4-131">Test-CsVoicePolicy ne tente pas de normaliser ou de traduire des numéros de téléphone au format E. 164.</span><span class="sxs-lookup"><span data-stu-id="0aba4-131">Test-CsVoicePolicy won't attempt to normalize or translate phone numbers into the E.164 format.</span></span>

<span data-ttu-id="0aba4-132">Pour plus d’informations, consultez la documentation d’aide de l’applet de Test-CsVoicePolicy.</span><span class="sxs-lookup"><span data-stu-id="0aba4-132">For more information, see the Help documentation for the Test-CsVoicePolicy cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="0aba4-133">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="0aba4-133">Determining success or failure</span></span>

<span data-ttu-id="0aba4-134">Si la stratégie vocale peut trouver un itinéraire vocal correspondant et une utilisation RTC correspondante, l’itinéraire et l’utilisation seront affichés à l’écran :</span><span class="sxs-lookup"><span data-stu-id="0aba4-134">If the voice policy can find both a matching voice route and a matching PSTN usage, then both the route and the usage will be displayed on-screen:</span></span>

<span data-ttu-id="0aba4-135">FirstMatchingRoute MatchingUsage</span><span class="sxs-lookup"><span data-stu-id="0aba4-135">FirstMatchingRoute MatchingUsage</span></span>

<span data-ttu-id="0aba4-136">\------------------ -------------</span><span class="sxs-lookup"><span data-stu-id="0aba4-136">\------------------ -------------</span></span>

<span data-ttu-id="0aba4-137">RedmondVoiceRoute RedmondPstnUsage</span><span class="sxs-lookup"><span data-stu-id="0aba4-137">RedmondVoiceRoute RedmondPstnUsage</span></span>

<span data-ttu-id="0aba4-138">Si une voie vocale ou une utilisation PSTN appropriée est introuvable, les valeurs de propriété vides seront affichées à l’écran :</span><span class="sxs-lookup"><span data-stu-id="0aba4-138">If either an appropriate voice route or an appropriate PSTN usage cannot be found then blank property values will be displayed on-screen:</span></span>

<span data-ttu-id="0aba4-139">FirstMatchingRoute MatchingUsage</span><span class="sxs-lookup"><span data-stu-id="0aba4-139">FirstMatchingRoute MatchingUsage</span></span>

<span data-ttu-id="0aba4-140">\------------------ -------------</span><span class="sxs-lookup"><span data-stu-id="0aba4-140">\------------------ -------------</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="0aba4-141">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="0aba4-141">Reasons why the test might have failed</span></span>

<span data-ttu-id="0aba4-142">Si Test-CsVoicePolicy ne renvoie aucune correspondance qui peut signifier que la stratégie vocale ne partage pas d’utilisation RTC avec un itinéraire vocal.</span><span class="sxs-lookup"><span data-stu-id="0aba4-142">If Test-CsVoicePolicy does not return a match that could mean that the voice policy does not share a PSTN usage with a voice route.</span></span> <span data-ttu-id="0aba4-143">Pour le vérifier, utilisez une applet de commande similaire à celle qui suit pour vérifier que les utilisations RTC attribuées à la stratégie vocale :</span><span class="sxs-lookup"><span data-stu-id="0aba4-143">To verify that, use a cmdlet similar to the following to verify that PSTN usages assigned to the voice policy:</span></span>

`Get-CsVoicePolicy -Identity "Global" | Select-Object PstnUsages | Format-List`

<span data-ttu-id="0aba4-144">Ensuite, exécutez la commande suivante pour identifier les utilisations PSTN affectées à chacun de vos itinéraires vocaux :</span><span class="sxs-lookup"><span data-stu-id="0aba4-144">Next, run this command to determine the PSTN usages assign to each of your voice routes:</span></span>

`Get-CsVoiceRoute | Select-Object Identity, PstnUsages`

<span data-ttu-id="0aba4-145">Si vous voyez des correspondances (autrement dit, si vous voyez un ou plusieurs itinéraires vocaux qui partagent au moins une utilisation PSTN avec votre stratégie vocale), exécutez l’applet de commande Test-CsVoiceRoute pour vérifier que l’itinéraire vocal peut composer le numéro de téléphone fourni.</span><span class="sxs-lookup"><span data-stu-id="0aba4-145">If you see any matches (that is, if you see one or more voice routes that share at least one PSTN usage with your voice policy), you should then run the Test-CsVoiceRoute cmdlet to verify that the voice route can dial the supplied phone number.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0aba4-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0aba4-146">See Also</span></span>


[<span data-ttu-id="0aba4-147">Test-CsVoicePolicy</span><span class="sxs-lookup"><span data-stu-id="0aba4-147">Test-CsVoicePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsVoicePolicy)  
  

<span data-ttu-id="0aba4-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0aba4-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

