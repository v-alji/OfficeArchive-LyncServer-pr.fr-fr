---
title: 'Lync Server 2013 : test du numéro de téléphone par rapport à un itinéraire vocal'
description: 'Lync Server 2013 : testez le numéro de téléphone en fonction d’une voie vocale.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test telephone number against a voice route
ms:assetid: 9a77ed6d-9394-4bef-9344-3d91b6959b97
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725211(v=OCS.15)
ms:contentKeyID: 63969631
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 789f4a538a992a72abf61f4c1fbdb98370f2e643
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444237"
---
# <a name="test-telephone-number-against-a-voice-route-in-lync-server-2013"></a><span data-ttu-id="1c24e-103">Testez le numéro de téléphone par rapport à un itinéraire vocal dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1c24e-103">Test telephone number against a voice route in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1c24e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1c24e-104">

<span> </span></span></span>

<span data-ttu-id="1c24e-105">_**Dernière modification de la rubrique :** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="1c24e-105">_**Topic Last Modified:** 2014-05-20_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c24e-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="1c24e-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="1c24e-107">Mois</span><span class="sxs-lookup"><span data-stu-id="1c24e-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c24e-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="1c24e-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="1c24e-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="1c24e-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c24e-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="1c24e-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="1c24e-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="1c24e-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="1c24e-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsVoiceRoute.</span><span class="sxs-lookup"><span data-stu-id="1c24e-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsVoiceRoute cmdlet.</span></span> <span data-ttu-id="1c24e-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="1c24e-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsVoiceRoute&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="1c24e-114">Description</span><span class="sxs-lookup"><span data-stu-id="1c24e-114">Description</span></span>

<span data-ttu-id="1c24e-115">Les itinéraires vocaux fonctionnent conjointement avec les politiques vocales pour vous permettre d’acheminer les appels voix entreprise vers le réseau PSTN.</span><span class="sxs-lookup"><span data-stu-id="1c24e-115">Voice routes work together with voice policies to help route Enterprise Voice calls to the PSTN network.</span></span> <span data-ttu-id="1c24e-116">Chaque itinéraire vocal inclut une expression régulière (un modèle de nombre) qui identifie les numéros de téléphone qui seront routés par le biais d’un itinéraire vocal donné : l’itinéraire sera en mesure de gérer les numéros de téléphone correspondant à cette expression régulière.</span><span class="sxs-lookup"><span data-stu-id="1c24e-116">Each voice route includes a regular expression (a number pattern) that identifies the phone numbers that will be routed through a given voice route: the route will be able to handle any phone numbers that match this regular expression.</span></span> <span data-ttu-id="1c24e-117">Par exemple, un itinéraire vocal peut avoir une expression régulière qui lui permet de gérer tout numéro à 10 chiffres.</span><span class="sxs-lookup"><span data-stu-id="1c24e-117">For example, a voice route might have a regular expression that enables it to handle any 10-digit number.</span></span> <span data-ttu-id="1c24e-118">Cela signifie que l’itinéraire peut gérer un numéro de téléphone tel que celui-ci :</span><span class="sxs-lookup"><span data-stu-id="1c24e-118">That means the route would be able to handle a phone number such as this:</span></span>

  - <span data-ttu-id="1c24e-119">2065551219</span><span class="sxs-lookup"><span data-stu-id="1c24e-119">2065551219</span></span>

<span data-ttu-id="1c24e-120">L’itinéraire ne peut pas gérer l’un ou l’autre des deux nombres suivants, aucun des deux chiffres :</span><span class="sxs-lookup"><span data-stu-id="1c24e-120">The route would not be able to handle either of the following two numbers, neither of which has 10 digits:</span></span>

  - <span data-ttu-id="1c24e-121">5551219</span><span class="sxs-lookup"><span data-stu-id="1c24e-121">5551219</span></span>

  - <span data-ttu-id="1c24e-122">12065551219</span><span class="sxs-lookup"><span data-stu-id="1c24e-122">12065551219</span></span>

<span data-ttu-id="1c24e-123">L’applet de l’applet de Test-CsVoiceRoute vérifie si un itinéraire vocal donné peut acheminer un numéro de téléphone spécifié.</span><span class="sxs-lookup"><span data-stu-id="1c24e-123">The Test-CsVoiceRoute cmdlet verifies whether a given voice route can route a specified phone number.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="1c24e-124">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="1c24e-124">Running the test</span></span>

<span data-ttu-id="1c24e-125">Le processus en deux étapes permet de vérifier que la capacité d’un itinéraire vocal est d’acheminer un numéro de téléphone spécifié.</span><span class="sxs-lookup"><span data-stu-id="1c24e-125">Verifying the ability of a voice route to route a specified phone number is a two-step process.</span></span> <span data-ttu-id="1c24e-126">Tout d’abord, vous devez utiliser l’applet de contrôle Get-CsVoiceRoute pour renvoyer une instance de cet itinéraire, puis vous devez utiliser l’applet de contrôle Test-CsVoiceRoute pour vérifier la capacité de l’itinéraire à gérer le numéro de téléphone cible.</span><span class="sxs-lookup"><span data-stu-id="1c24e-126">First you have to use the Get-CsVoiceRoute cmdlet to return an instance of that voice route, and then you have to use the Test-CsVoiceRoute cmdlet to verify the ability of that route to handle the target phone number.</span></span> <span data-ttu-id="1c24e-127">Par exemple, si vous avez la possibilité de vérifier si l’itinéraire vocal de RedmondVoiceRoute peut acheminer le numéro de téléphone 2065551219 :</span><span class="sxs-lookup"><span data-stu-id="1c24e-127">For example, this command verifies whether the RedmondVoiceRoute voice route can route the phone number 2065551219:</span></span>

`Get-CsVoiceRoute -Identity "RedmondVoiceRoute" | Test-CsVoiceRoute -TargetNumber "2065551219"`

<span data-ttu-id="1c24e-128">Notez que le numéro de téléphone doit être tapé pour que les utilisateurs puissent composer ce numéro.</span><span class="sxs-lookup"><span data-stu-id="1c24e-128">Note that the phone number should be typed as you expect users to dial that number.</span></span> <span data-ttu-id="1c24e-129">Par exemple, si vous ne pensez pas que les utilisateurs incluent l’indicatif du pays et l’indicatif de la région lorsque vous composez, utilisez une syntaxe semblable à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="1c24e-129">For example, if you do not expect users to include the country code and area code when dialing, then use syntax similar to this:</span></span>

`-TargetNumber "5551219"`

<span data-ttu-id="1c24e-130">Dans le cas présent, le numéro de la cible quitte le code de pays et l’indicatif de la région.</span><span class="sxs-lookup"><span data-stu-id="1c24e-130">In this case, the target number leaves out both the country code and the area code.</span></span>

<span data-ttu-id="1c24e-131">Pour utiliser une seule commande pour tester tous les itinéraires vocaux sur un numéro cible spécifié, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="1c24e-131">To use a single command to test all the voice routes against a specified target number, use syntax such as the following:</span></span>

`Get-CsVoiceRoute | Test-CsVoiceRoute -TargetNumber "2065551219"`

<span data-ttu-id="1c24e-132">Pour plus d’informations, consultez la documentation d’aide de l’applet de Test-CsVoiceRoute.</span><span class="sxs-lookup"><span data-stu-id="1c24e-132">For more information, see the Help documentation for the Test-CsVoiceRoute cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="1c24e-133">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="1c24e-133">Determining success or failure</span></span>

<span data-ttu-id="1c24e-134">Si l’itinéraire vocal peut acheminer le numéro de téléphone cible, la cmdlet Test-CsVoiceRoute renvoie simplement la valeur true :</span><span class="sxs-lookup"><span data-stu-id="1c24e-134">If the voice route can route the target phone number the Test-CsVoiceRoute cmdlet just returns the value True:</span></span>

<span data-ttu-id="1c24e-135">MatchesPattern</span><span class="sxs-lookup"><span data-stu-id="1c24e-135">MatchesPattern</span></span>

\--------------

<span data-ttu-id="1c24e-136">Vrai</span><span class="sxs-lookup"><span data-stu-id="1c24e-136">True</span></span>

<span data-ttu-id="1c24e-137">Cela signifie que l’itinéraire peut gérer des nombres similaires au numéro cible.</span><span class="sxs-lookup"><span data-stu-id="1c24e-137">That means that route can handle numbers similar to the target number.</span></span> <span data-ttu-id="1c24e-138">Si l’itinéraire vocal ne peut pas gérer le numéro cible, Test-CsVoiceRoute renvoie la valeur false :</span><span class="sxs-lookup"><span data-stu-id="1c24e-138">If the voice route is can't handle the target number then Test-CsVoiceRoute returns the value False:</span></span>

<span data-ttu-id="1c24e-139">MatchesPattern</span><span class="sxs-lookup"><span data-stu-id="1c24e-139">MatchesPattern</span></span>

\--------------

<span data-ttu-id="1c24e-140">False</span><span class="sxs-lookup"><span data-stu-id="1c24e-140">False</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="1c24e-141">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="1c24e-141">Reasons why the test might have failed</span></span>

<span data-ttu-id="1c24e-142">Lors du test des itinéraires vocaux, « Failure » est un terme relatif.</span><span class="sxs-lookup"><span data-stu-id="1c24e-142">When testing voice routes, “failure” is a relative term.</span></span> <span data-ttu-id="1c24e-143">Dans ce cas, cela ne veut pas dire que l’itinéraire est quelque peu « rompu », ce qui signifie que l’itinéraire ne peut pas gérer le numéro cible.</span><span class="sxs-lookup"><span data-stu-id="1c24e-143">In this case, it doesn’t mean that the route is somehow “broken;” instead, it just means that the route can't handle the target number.</span></span> <span data-ttu-id="1c24e-144">Cela peut être dû au fait que l’itinéraire vocal a été configuré de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="1c24e-144">That could be because the voice route was configured incorrectly.</span></span> <span data-ttu-id="1c24e-145">Cela peut également signifier que l’itinéraire n’était jamais destiné à gérer des nombres à l’aide de ce modèle.</span><span class="sxs-lookup"><span data-stu-id="1c24e-145">It could also mean that the route was never intended to handle numbers using this pattern.</span></span> <span data-ttu-id="1c24e-146">Par exemple, si vous ne souhaitez pas acheminer les appels vers d’autres pays sur un itinéraire donné, il est possible que l’itinéraire soit configuré pour rejeter tous les numéros de téléphone incluant un code de pays.</span><span class="sxs-lookup"><span data-stu-id="1c24e-146">For example, if you do not want to route calls to other countries over a given route that route might be configured to reject all phone numbers that include a country code.</span></span> <span data-ttu-id="1c24e-147">Si Test-CsVoiceRoute renvoie faux lorsque vous attendiez qu’il retourne vrai, vérifiez que vous avez correctement tapé le numéro cible.</span><span class="sxs-lookup"><span data-stu-id="1c24e-147">If Test-CsVoiceRoute returns False when you expected it to return True, verify that you typed the target number in correctly.</span></span> <span data-ttu-id="1c24e-148">Si tel est le cas, utilisez une commande similaire à celle-ci pour afficher le NumberPattern configuré pour l’itinéraire :</span><span class="sxs-lookup"><span data-stu-id="1c24e-148">If you did, then use a command similar to this one to view the NumberPattern configured for the route:</span></span>

`Get-CsVoiceRoute -Identity "RedmondVoiceRoute" | Select-Object NumberPattern`

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1c24e-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c24e-149">See Also</span></span>


[<span data-ttu-id="1c24e-150">Test-CsVoiceRoute</span><span class="sxs-lookup"><span data-stu-id="1c24e-150">Test-CsVoiceRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsVoiceRoute)  
  

<span data-ttu-id="1c24e-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1c24e-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

