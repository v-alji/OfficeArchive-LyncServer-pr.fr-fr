---
title: 'Lync Server 2013 : test du plan de numérotation'
description: 'Lync Server 2013 : test du plan de numérotation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing the dial plan
ms:assetid: 70eec03c-aca3-4106-86a7-77ae96b53779
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690130(v=OCS.15)
ms:contentKeyID: 63969616
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a0ef2e3fce9d1fbbb0186b1b7aef608834145d3e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395308"
---
# <a name="testing-the-dial-plan-in-lync-server-2013"></a><span data-ttu-id="8d0cd-103">Test du plan de numérotation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8d0cd-103">Testing the dial plan in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8d0cd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8d0cd-104">

<span> </span></span></span>

<span data-ttu-id="8d0cd-105">_**Dernière modification de la rubrique :** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="8d0cd-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d0cd-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="8d0cd-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="8d0cd-107">Jour</span><span class="sxs-lookup"><span data-stu-id="8d0cd-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0cd-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="8d0cd-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="8d0cd-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8d0cd-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0cd-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="8d0cd-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="8d0cd-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="8d0cd-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="8d0cd-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsDialPlan.</span><span class="sxs-lookup"><span data-stu-id="8d0cd-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsDialPlan cmdlet.</span></span> <span data-ttu-id="8d0cd-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="8d0cd-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsDialPlan&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="8d0cd-114">Description</span><span class="sxs-lookup"><span data-stu-id="8d0cd-114">Description</span></span>

<span data-ttu-id="8d0cd-115">L’applet de requête Test-CsDialPlan vous permet d’afficher les résultats de l’application d’un plan de numérotation à un numéro de téléphone donné.</span><span class="sxs-lookup"><span data-stu-id="8d0cd-115">The Test-CsDialPlan cmdlet enables you to see the results of applying a dial plan to a given telephone number.</span></span> <span data-ttu-id="8d0cd-116">Les plans de numérotation fournissent des informations, telles que les règles de normalisation, requises pour permettre aux utilisateurs d’entreprise Voice d’effectuer des appels téléphoniques.</span><span class="sxs-lookup"><span data-stu-id="8d0cd-116">Dial plans provide information, such as how normalization rules are applied, required to enable Enterprise Voice users to make telephone calls.</span></span> <span data-ttu-id="8d0cd-117">À partir d’un numéro composé et d’un plan de numérotation, cette applet de contrôle vérifie quelle règle de normalisation du plan de numérotation sera appliquée et quel sera le numéro traduit.</span><span class="sxs-lookup"><span data-stu-id="8d0cd-117">Given a dialed number and a dial plan, this cmdlet will verify which normalization rule within the dial plan will be applied and what the translated number will be.</span></span>

<span data-ttu-id="8d0cd-118">Vous pouvez utiliser cette cmdlet pour résoudre les problèmes liés aux traductions de nombres ou pour vérifier l’application de règles à certains numéros.</span><span class="sxs-lookup"><span data-stu-id="8d0cd-118">You can use this cmdlet for troubleshooting issues with number translations, or for verifying how to apply rules against certain numbers.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="8d0cd-119">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="8d0cd-119">Running the test</span></span>

<span data-ttu-id="8d0cd-120">L’applet de l’applet de Test-CsDialPlan nécessite deux choses.</span><span class="sxs-lookup"><span data-stu-id="8d0cd-120">The Test-CsDialPlan cmdlet requires you to do two things.</span></span> <span data-ttu-id="8d0cd-121">Tout d’abord, vous devez obtenir une instance du plan de numérotation testé. vous pouvez effectuer cette opération à l’aide de l’applet de Get-CsDialPlan.</span><span class="sxs-lookup"><span data-stu-id="8d0cd-121">First, you must obtain an instance of the dial plan being tested; that can be done by using the Get-CsDialPlan cmdlet.</span></span> <span data-ttu-id="8d0cd-122">Deuxièmement, vous devez spécifier le numéro de téléphone qui doit être normalisé.</span><span class="sxs-lookup"><span data-stu-id="8d0cd-122">Second, you must specify the phone number that has to be normalized.</span></span> <span data-ttu-id="8d0cd-123">Le format utilisé pour le numéro de téléphone doit correspondre au numéro composé par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8d0cd-123">The format that is used for the phone number should match the number as dialed/entered by a user.</span></span> <span data-ttu-id="8d0cd-124">Par exemple, cette commande récupère une instance du plan de numérotation, RedmondDialPlan et vérifie si le numéro de téléphone 12065551219 peut être normalisé :</span><span class="sxs-lookup"><span data-stu-id="8d0cd-124">For example, this command retrieves an instance of the dial plan, RedmondDialPlan, and checks whether the phone number 12065551219 can be normalized:</span></span>

    Get-CsDialPlan -Identity "RedmondDialPlan" | Test-CsDialPlan -DialedNumber "12065551219" | Format-List

<span data-ttu-id="8d0cd-125">Si vous disposez d’une règle de normalisation qui ajoute automatiquement le code du pays (dans cet exemple, 1) et l’indicatif de la région (206), vous pouvez vérifier le numéro de téléphone 5551219 comme suit :</span><span class="sxs-lookup"><span data-stu-id="8d0cd-125">If you have a normalization rule that automatically adds the country code (in this example, 1) and the area code (206), then you might want to check the phone number 5551219, as follows:</span></span>

    Get-CsDialPlan -Identity "RedmondDialPlan" | Test-CsDialPlan -DialedNumber "5551219" | Format-List

<span data-ttu-id="8d0cd-126">Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsDialPlan](https://docs.microsoft.com/powershell/module/skype/Test-CsDialPlan) .</span><span class="sxs-lookup"><span data-stu-id="8d0cd-126">For more information, see the Help documentation for the [Test-CsDialPlan](https://docs.microsoft.com/powershell/module/skype/Test-CsDialPlan) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="8d0cd-127">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="8d0cd-127">Determining success or failure</span></span>

<span data-ttu-id="8d0cd-128">Test-CsDialPlan est différent de la plupart des cmdlets de test du serveur Lync, car il n’indique qu’un test a réussi ou échoué.</span><span class="sxs-lookup"><span data-stu-id="8d0cd-128">Test-CsDialPlan differs from many of the Lync Server test cmdlets because it only indirectly indicates whether a test succeeded or failed.</span></span> <span data-ttu-id="8d0cd-129">Lorsque vous utilisez Test-CsDialPlan vous ne recevez pas de sortie semblable à celle-ci avec le résultat libellé clairement :</span><span class="sxs-lookup"><span data-stu-id="8d0cd-129">When using Test-CsDialPlan you do not receive back output similar to this with the Result clearly labeled:</span></span>

<span data-ttu-id="8d0cd-130">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="8d0cd-130">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="8d0cd-131">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="8d0cd-131">Result : Success</span></span>

<span data-ttu-id="8d0cd-132">Latence : 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="8d0cd-132">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="8d0cd-133">Error</span><span class="sxs-lookup"><span data-stu-id="8d0cd-133">Error :</span></span>

<span data-ttu-id="8d0cd-134">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="8d0cd-134">Diagnosis :</span></span>

<span data-ttu-id="8d0cd-135">Au lieu de cela, si Test-CsDialPlan réussit, vous recevrez des informations sur la règle de normalisation qui a pu traduire et utiliser le numéro de téléphone spécifié.</span><span class="sxs-lookup"><span data-stu-id="8d0cd-135">Instead, if Test-CsDialPlan succeeds, then you'll receive information about the normalization rule that was able to successfully translate and use the specified phone number:</span></span>

<span data-ttu-id="8d0cd-136">TranslatedNumber : + 12065551219</span><span class="sxs-lookup"><span data-stu-id="8d0cd-136">TranslatedNumber : +12065551219</span></span>

<span data-ttu-id="8d0cd-137">MatchingRule : description =; Modèle = ^ ( \\ j (11)) $; Traduction = + $1 ;</span><span class="sxs-lookup"><span data-stu-id="8d0cd-137">MatchingRule : Description=;Pattern=^(\\d(11))$;Translation=+$1;</span></span>

<span data-ttu-id="8d0cd-138">Nom = tout préfixe ; IsInternalExtension = false</span><span class="sxs-lookup"><span data-stu-id="8d0cd-138">Name=Prefix All; IsInternalExtension=False</span></span>

<span data-ttu-id="8d0cd-139">Si Test-CsDialPlan échoue (autrement dit, si le plan de numérotation n’a pas de règle de normalisation qui peut traduire le numéro de téléphone spécifié), il vous suffit de recevoir la sortie « vider » comme suit :</span><span class="sxs-lookup"><span data-stu-id="8d0cd-139">If Test-CsDialPlan fails (that is, if the dial plan does not have a normalization rule that can translate the specified phone number), you'll just receive “empty” output as follows:</span></span>

<span data-ttu-id="8d0cd-140">TranslatedNumber :</span><span class="sxs-lookup"><span data-stu-id="8d0cd-140">TranslatedNumber :</span></span>

<span data-ttu-id="8d0cd-141">MatchingRule :</span><span class="sxs-lookup"><span data-stu-id="8d0cd-141">MatchingRule :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="8d0cd-142">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="8d0cd-142">Reasons why the test might have failed</span></span>

<span data-ttu-id="8d0cd-143">Voici quelques raisons courantes pour lesquelles Test-CsDialPlan risque d’échouer :</span><span class="sxs-lookup"><span data-stu-id="8d0cd-143">Here are some common reasons why Test-CsDialPlan might fail:</span></span>

  - <span data-ttu-id="8d0cd-144">Vous avez peut-être déjà utilisé un format incorrect lorsque vous spécifiez le numéro de téléphone.</span><span class="sxs-lookup"><span data-stu-id="8d0cd-144">You might have used an incorrect format when specifying the phone number.</span></span> <span data-ttu-id="8d0cd-145">Les plans de numérotation incluent des règles de normalisation qui permettent à Lync Server de traduire les numéros de téléphone numérotés ou entrés par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8d0cd-145">Dial plans include normalization rules that enable Lync Server to translate the phone numbers dialed or entered by a user.</span></span> <span data-ttu-id="8d0cd-146">Par conséquent, votre plan de numérotation doit être doté de règles de normalisation correspondant aux numéros que les utilisateurs peuvent composer.</span><span class="sxs-lookup"><span data-stu-id="8d0cd-146">Therefore, your dial plan should have normalization rules that match the numbers users are likely to dial.</span></span> <span data-ttu-id="8d0cd-147">Par exemple, si les utilisateurs peuvent composer le code de pays, l’indicatif régional et le numéro de téléphone lui-même, cela signifie que votre plan de numérotation doit être doté d’une règle de normalisation pour gérer les numéros de téléphone comme suit :</span><span class="sxs-lookup"><span data-stu-id="8d0cd-147">For example, if users might dial the country code, area code, and then the phone number itself, that means that your dial plan should have a normalization rule to handle phone numbers such as this:</span></span>
    
    <span data-ttu-id="8d0cd-148">12065551219</span><span class="sxs-lookup"><span data-stu-id="8d0cd-148">12065551219</span></span>
    
    <span data-ttu-id="8d0cd-149">Toutefois, si vous entrez un numéro de téléphone incorrect (par exemple, en ne disquittant pas le dernier chiffre), Test-CsDialPlan ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="8d0cd-149">However, if you enter an incorrect phone number (for example, leaving off the final digit), then Test-CsDialPlan will fail.</span></span> <span data-ttu-id="8d0cd-150">Ce n’est pas parce que le plan de numérotation est défectueux, car vous avez entré un numéro de téléphone qui ne peut pas être interprété.</span><span class="sxs-lookup"><span data-stu-id="8d0cd-150">That’s not because the dial plan is faulty but because you have entered a phone number than can’t be interpreted.</span></span>

<span data-ttu-id="8d0cd-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8d0cd-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

