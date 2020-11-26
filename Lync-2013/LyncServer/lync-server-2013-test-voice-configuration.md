---
title: 'Lync Server 2013 : test de la configuration vocale'
description: 'Lync Server 2013 : test de la configuration vocale.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test voice configuration
ms:assetid: 574794a3-cb30-4762-bb62-3a68574f05e9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725208(v=OCS.15)
ms:contentKeyID: 63969605
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4cc05286e5f534b4d469ef561d9ce009367e15be
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444181"
---
# <a name="test-voice-configuration-in-lync-server-2013"></a><span data-ttu-id="c0a0c-103">Test de la configuration vocale dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0a0c-103">Test voice configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c0a0c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c0a0c-104">

<span> </span></span></span>

<span data-ttu-id="c0a0c-105">_**Dernière modification de la rubrique :** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="c0a0c-105">_**Topic Last Modified:** 2014-05-20_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0a0c-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="c0a0c-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="c0a0c-107">Mois</span><span class="sxs-lookup"><span data-stu-id="c0a0c-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0a0c-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="c0a0c-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="c0a0c-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0a0c-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0a0c-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="c0a0c-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="c0a0c-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="c0a0c-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsVoiceTestConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsVoiceTestConfiguration cmdlet.</span></span> <span data-ttu-id="c0a0c-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="c0a0c-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsVoiceTestConfiguration&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="c0a0c-114">Description</span><span class="sxs-lookup"><span data-stu-id="c0a0c-114">Description</span></span>

<span data-ttu-id="c0a0c-115">Lync Server inclut plusieurs cmdlets Windows PowerShell (par exemple, Test-CsVoiceRoute et test-CsVoicePolicy, test-CsTrunkConfiguration) qui vous permettent de vérifier que les éléments individuels de votre infrastructure vocale d’entreprise (itinéraires vocaux, stratégies vocales, Trunks SIP) fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-115">Lync Server includes several Windows PowerShell cmdlets (such as Test-CsVoiceRoute and Test-CsVoicePolicy, Test-CsTrunkConfiguration) that enable you to verify that the individual pieces of your Enterprise Voice infrastructure – voice routes, voice policies, SIP trunks – are working as expected.</span></span>

<span data-ttu-id="c0a0c-116">S’il est important d’utiliser une voix entreprise pour tous les composants individuels : il est possible d’avoir un itinéraire vocal valide, une politique vocale valide et un Trunk SIP valide, mais les utilisateurs ne peuvent pas passer ou recevoir des appels téléphoniques.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-116">While it’s important with Enterprise Voice that all the individual pieces work: it’s possible to have a valid voice route, a valid voice policy, and a valid SIP trunk, but still have users unable to make or receive phone calls.</span></span> <span data-ttu-id="c0a0c-117">Pour cette raison, Lync Server vous permet également de créer des configurations de tests vocaux.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-117">Because of that, Lync Server also provides the ability to create voice test configurations.</span></span> <span data-ttu-id="c0a0c-118">Les configurations de tests vocaux représentent des scénarios d’entreprise vocaux communs : vous pouvez spécifier des éléments tels que les itinéraires vocaux, la politique vocale et un plan de numérotation, puis vérifier qu’ils sont en mesure de fonctionner ensemble afin de fournir un service téléphonique.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-118">Voice test configurations represent common Enterprise Voice scenarios: you can specify such things as a voice route, a voice policy, and a dial plan, and then verify that those individual items are work able to work together to provide phone service.</span></span> <span data-ttu-id="c0a0c-119">De plus, vous pouvez valider vos attentes dans un scénario donné.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-119">In addition, you can validate your expectations in a given scenario.</span></span> <span data-ttu-id="c0a0c-120">Par exemple, supposons que vous vous attendiez que la combinaison du plan de numérotation A et de la stratégie vocale A pour effet d’acheminer les appels sur le routage vocal C. Vous pouvez entrer l’itinéraire vocal C en tant que ExpectedRoute.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-120">For example, suppose that you expect that the combination of dial plan A and voice policy B would result in calls being routed over voice route C. You can enter voice route C as the ExpectedRoute.</span></span> <span data-ttu-id="c0a0c-121">Lors de l’exécution du test, si l’itinéraire vocal C n’est pas utilisé, le test sera marqué comme ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-121">When you run the test, if voice route C is not employed then the test will be marked as having failed.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="c0a0c-122">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="c0a0c-122">Running the test</span></span>

<span data-ttu-id="c0a0c-123">Avant de tester les collections de configurations vocales à l’aide de Windows PowerShell, vous devez d’abord utiliser l’applet de contrôle Get-CsVoiceTestConfiguration pour récupérer une instance de ces paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-123">Before testing Voice configuration collections using Windows PowerShell, you must first use the Get-CsVoiceTestConfiguration cmdlet to retrieve an instance of these configuration settings.</span></span> <span data-ttu-id="c0a0c-124">Cette instance doit alors être canalisée vers le test-CsVoiceTestConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-124">That instance must then be piped to the Test-CsVoiceTestConfiguration.</span></span> <span data-ttu-id="c0a0c-125">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="c0a0c-125">For example:</span></span>

`Get-CsVoiceTestConfiguration -Identity "RedmondVoiceTestConfiguration" | Test-CsVoiceTestConfiguration`

<span data-ttu-id="c0a0c-126">Pour valider l’ensemble des paramètres de configuration des tests vocaux en même temps, utilisez cette commande à la place :</span><span class="sxs-lookup"><span data-stu-id="c0a0c-126">To validate all the voice test configuration settings at the same time, use this command instead:</span></span>

`Get-CsVoiceTestConfiguration | Test-CsVoiceTestConfiguration`

<span data-ttu-id="c0a0c-127">Pour plus d’informations, consultez la documentation d’aide de l’applet de Test-CsVoiceTestConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-127">For more information, see the Help documentation for the Test-CsVoiceTestConfiguration cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="c0a0c-128">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="c0a0c-128">Determining success or failure</span></span>

<span data-ttu-id="c0a0c-129">L’applet de commande Test-CsVoiceTestConfiguration signale la réussite ou l’échec d’un test, et fournit des informations supplémentaires sur les tests réussis tels que la règle de traduction, l’itinéraire vocal et l’utilisation RTC utilisée pour effectuer la tâche :</span><span class="sxs-lookup"><span data-stu-id="c0a0c-129">The Test-CsVoiceTestConfiguration cmdlet reports whether a test failed or succeeded, and provides additional information about each successful test, such as the translation rule, voice route, and PSTN usage used to complete the task:</span></span>

<span data-ttu-id="c0a0c-130">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="c0a0c-130">Result:             Success</span></span>

<span data-ttu-id="c0a0c-131">TranslatedNumber : + 15551234</span><span class="sxs-lookup"><span data-stu-id="c0a0c-131">TranslatedNumber:   +15551234</span></span>

<span data-ttu-id="c0a0c-132">MatchingRule : description =; Pattern = ^ ( \\ d {4} ) $; Traduction = + 1 \\ d ; nom = test ; IsInternalExtension = false</span><span class="sxs-lookup"><span data-stu-id="c0a0c-132">MatchingRule:       Description=;Pattern=^(\\d{4})$;Translation=+1\\d;Name=Test;IsInternalExtension=False</span></span>

<span data-ttu-id="c0a0c-133">FirstMatchingRoute : site : Redmond</span><span class="sxs-lookup"><span data-stu-id="c0a0c-133">FirstMatchingRoute: site:Redmond</span></span>

<span data-ttu-id="c0a0c-134">MatchingUsage : local</span><span class="sxs-lookup"><span data-stu-id="c0a0c-134">MatchingUsage:      Local</span></span>

<span data-ttu-id="c0a0c-135">Si le test échoue, le résultat est alors signalé comme Fail :</span><span class="sxs-lookup"><span data-stu-id="c0a0c-135">If the test fails then the result is reported as Fail:</span></span>

<span data-ttu-id="c0a0c-136">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="c0a0c-136">Result:             Fail</span></span>

<span data-ttu-id="c0a0c-137">TranslatedNumber:</span><span class="sxs-lookup"><span data-stu-id="c0a0c-137">TranslatedNumber:</span></span>   

<span data-ttu-id="c0a0c-138">FirstMatchingRoute:</span><span class="sxs-lookup"><span data-stu-id="c0a0c-138">FirstMatchingRoute:</span></span>

<span data-ttu-id="c0a0c-139">MatchingUsage:</span><span class="sxs-lookup"><span data-stu-id="c0a0c-139">MatchingUsage:</span></span>      

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="c0a0c-140">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="c0a0c-140">Reasons why the test might have failed</span></span>

<span data-ttu-id="c0a0c-141">Dans la mesure où le test de configuration de tests vocaux teste plusieurs éléments différents (politiques vocales, plans de numérotation, itinéraires vocaux, etc.), plusieurs facteurs peuvent entraîner l’échec d’un test.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-141">Because voice test configuration testing tests several different items – including voice policies, dial plans, voice routes, and so on – there are several different factors that could result in a failed test.</span></span> <span data-ttu-id="c0a0c-142">En cas d’échec d’un test, vous devez commencer par passer en revue les paramètres de configuration en utilisant l’applet de contrôle Get-CsVoiceTestConfiguration :</span><span class="sxs-lookup"><span data-stu-id="c0a0c-142">If a test fails, your first step should be to review the configuration settings themselves by using the Get-CsVoiceTestConfiguration cmdlet:</span></span>

`Get-CsVoiceTestConfiguration -Identity "RedmondVoiceTestConfiguration"`

<span data-ttu-id="c0a0c-143">Si les paramètres semblent être correctement configurés, exécutez de nouveau le test en incluant le paramètre Verbose :</span><span class="sxs-lookup"><span data-stu-id="c0a0c-143">If the settings seem to be configured correctly, re-run the test while including the Verbose parameter:</span></span>

`Get-CsVoiceTestConfiguration -Identity "RedmondVoiceTestConfiguration" | Test-CsVoiceTestConfiguration`

<span data-ttu-id="c0a0c-144">Le paramètre Verbose fournit un compte étape par étape de chaque action effectuée par Test-CsVoiceTestConfiguration comme illustré dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="c0a0c-144">The Verbose parameter will provide a step-by-step account of each action taken by Test-CsVoiceTestConfiguration as shown in this example:</span></span>

<span data-ttu-id="c0a0c-145">DÉTAILLÉ : Téléchargement d’un plan de numérotation : « global »</span><span class="sxs-lookup"><span data-stu-id="c0a0c-145">VERBOSE: Loading dial plan: "Global"</span></span>

<span data-ttu-id="c0a0c-146">DÉTAILLÉ : chargement de la stratégie vocale : « RedmondDialPlan »</span><span class="sxs-lookup"><span data-stu-id="c0a0c-146">VERBOSE: Loading voice policy: "RedmondDialPlan"</span></span>

<span data-ttu-id="c0a0c-147">Ce compte détaillé peut fournir un indice utile sur l’endroit où le test a réellement échoué.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-147">This step-by-step account might provide a useful clue as to where the test actually failed.</span></span> <span data-ttu-id="c0a0c-148">Si ce n’est pas le cas, vous pouvez utiliser d’autres cmdlets Windows PowerShell (par exemple, test-CsVoicePolicy) et procéder de manière méthodique pour vérifier les composants individuels inclus dans les paramètres de configuration des tests vocaux.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-148">If not, you can then use other Windows PowerShell cmdlets (such as Test-CsVoicePolicy) and methodically begin to verify the individual components that are included in the voice test configuration settings.</span></span>

<span data-ttu-id="c0a0c-149">Par ailleurs, n’ayez pas d’esprit qu’il est possible qu’un test soit en mesure d’acheminer un appel sans pour autant être marqué comme ayant échoué ; Cela peut se produire si vous entrez des valeurs pour ExpectedRoute, ExpectedTranslatedNumber et ExpectedUsage, et que ces attentes ne sont pas satisfaites.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-149">In addition to that, be aware that it’s possible for a test to be able to route a call and yet still be marked as a failure; that can occur if you enter values for ExpectedRoute, ExpectedTranslatedNumber, and ExpectedUsage, and any of those expectations are not met.</span></span> <span data-ttu-id="c0a0c-150">Par exemple, supposons que vous entriez l’itinéraire de la voix C comme prévu, mais que le test termine réellement l’appel à l’aide de l’itinéraire vocal D. Dans ce cas, le test sera marqué comme failed, car l’itinéraire vocal attendu n’a pas été utilisé.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-150">For example, suppose that you enter voice route C as your expected voice route, but the test actually completes the call using voice route D. In that case the test will be marked as Failed because the expected voice route was not used.</span></span> <span data-ttu-id="c0a0c-151">En cas d’échec d’un test, vous pouvez supprimer les valeurs pour ExpectedRoute, ExpectedTranslatedNumber et ExpectedUsage puis réexécuter le test.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-151">If a test fails, you might remove the values for ExpectedRoute, ExpectedTranslatedNumber, and ExpectedUsage and then re-run the test.</span></span> <span data-ttu-id="c0a0c-152">Cela vous aide à déterminer si l’appel n’a pas pu être effectué ou si vous attendez une seule personne et que vous en avez réellement reçu une.</span><span class="sxs-lookup"><span data-stu-id="c0a0c-152">That will help you determine whether the failure was because the call couldn't be completed, or because you expect one thing and actually received another.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c0a0c-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0a0c-153">See Also</span></span>


[<span data-ttu-id="c0a0c-154">Test-CsVoiceTestConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0a0c-154">Test-CsVoiceTestConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsVoiceTestConfiguration)  
  

<span data-ttu-id="c0a0c-155"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c0a0c-155"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

