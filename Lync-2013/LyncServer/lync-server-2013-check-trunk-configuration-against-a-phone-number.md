---
title: 'Lync Server 2013 : vérifier la configuration de Trunk par rapport à un numéro de téléphone'
description: 'Lync Server 2013 : Vérifiez la configuration de Trunk par rapport à un numéro de téléphone.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Check trunk configuration against a phone number
ms:assetid: 0800d7a3-fc35-482b-a9a4-203d890bfa45
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725206(v=OCS.15)
ms:contentKeyID: 63969574
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7cdfe1a2a9c5c87310ad561464960c5a01fea7b5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434983"
---
# <a name="check-trunk-configuration-against-a-phone-number-in-lync-server-2013"></a><span data-ttu-id="cbecc-103">Vérifier la configuration de Trunk par rapport à un numéro de téléphone dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cbecc-103">Check trunk configuration against a phone number in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cbecc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cbecc-104">

<span> </span></span></span>

<span data-ttu-id="cbecc-105">_**Dernière modification de la rubrique :** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="cbecc-105">_**Topic Last Modified:** 2014-05-20_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cbecc-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="cbecc-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="cbecc-107">Mois</span><span class="sxs-lookup"><span data-stu-id="cbecc-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbecc-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="cbecc-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="cbecc-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="cbecc-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbecc-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="cbecc-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="cbecc-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="cbecc-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="cbecc-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsTrunkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cbecc-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsTrunkConfiguration cmdlet.</span></span> <span data-ttu-id="cbecc-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="cbecc-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsTrunkConfiguration&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="cbecc-114">Description</span><span class="sxs-lookup"><span data-stu-id="cbecc-114">Description</span></span>

<span data-ttu-id="cbecc-115">Les ISL SIP connectent le réseau d’entreprise voix interne de Lync Server à l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="cbecc-115">SIP trunks connect the Lync Server internal Enterprise Voice network to any of the following:</span></span>

  - <span data-ttu-id="cbecc-116">Le réseau téléphonique public commuté (RTC).</span><span class="sxs-lookup"><span data-stu-id="cbecc-116">The Public Switched Telephone network (PSTN).</span></span>

  - <span data-ttu-id="cbecc-117">Un échange de succursale public IP (PBX).</span><span class="sxs-lookup"><span data-stu-id="cbecc-117">An IP-public branch exchange (PBX).</span></span>

  - <span data-ttu-id="cbecc-118">Contrôleur de bordure de session (SBC).</span><span class="sxs-lookup"><span data-stu-id="cbecc-118">A Session Border Controller (SBC).</span></span>

<span data-ttu-id="cbecc-119">L’applet de connexion Test-CsTrunkConfiguration vérifie qu’un numéro de téléphone (tel qu’un appel) peut être converti en réseau E. 164 et routé sur une ligne SIP spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cbecc-119">The Test-CsTrunkConfiguration cmdlet verifies that a phone number (as dialed by a user) can be converted to the E.164 network and routed over a specified SIP trunk.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="cbecc-120">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="cbecc-120">Running the test</span></span>

<span data-ttu-id="cbecc-121">Pour exécuter l’applet de Get-CsTrunkConfiguration Test-CsTrunkConfiguration vous devez d’abord utiliser l’applet de cmdlet pour récupérer une instance de vos paramètres de configuration de Trunk SIP. cette instance est alors canalisée vers test-CsTrunkConfiguration :</span><span class="sxs-lookup"><span data-stu-id="cbecc-121">To run the Test-CsTrunkConfiguration cmdlet you must first use the Get-CsTrunkConfiguration cmdlet to retrieve an instance of your SIP trunk configuration settings; that instance is then piped to Test-CsTrunkConfiguration:</span></span>

`Get-CsTrunkConfiguration -Identity "Global" | Test-CsTrunkConfiguration -DialedNumber "12065551219"`

<span data-ttu-id="cbecc-122">L’exécution d' Test-CsTrunkConfiguration sans avoir d’exécution Get-CsTrunkConfiguration ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="cbecc-122">Running Test-CsTrunkConfiguration without first running Get-CsTrunkConfiguration won't work.</span></span> <span data-ttu-id="cbecc-123">Par exemple, cette commande échoue sans renvoyer de données :</span><span class="sxs-lookup"><span data-stu-id="cbecc-123">For example, this command will fail without returning any data:</span></span>

`Test-CsTrunkConfiguration -DialedNumber "12065551219" -TrunkConfiguration "Global"`

<span data-ttu-id="cbecc-124">Si vous avez plusieurs collections de paramètres de configuration de Trunk SIP, vous pouvez utiliser une commande similaire à celle qui suit pour tester chaque collection sur le même numéro de téléphone :</span><span class="sxs-lookup"><span data-stu-id="cbecc-124">If you have multiple collections of SIP trunk configuration settings, you can use a command similar to the following to at the same time test each collection against the same phone number:</span></span>

`Get-CsTrunkConfiguration | Test-CsTrunkConfiguration -DialedNumber "12065551219"`

<span data-ttu-id="cbecc-125">Pour plus d’informations, consultez la documentation d’aide de l’applet de Test-CsTrunkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cbecc-125">For more information, see the Help documentation for the Test-CsTrunkConfiguration cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="cbecc-126">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="cbecc-126">Determining success or failure</span></span>

<span data-ttu-id="cbecc-127">Si Test-CsTrunkConfiguration pouvez passer un appel au numéro composé, le numéro de téléphone traduit (au format E. 164) et la règle utilisée pour traduire ce numéro de téléphone s’affichent à l’écran.</span><span class="sxs-lookup"><span data-stu-id="cbecc-127">If Test-CsTrunkConfiguration can place a call to the dialed number then the translated phone number (in the E.164 format) and the rule used to translate that phone number will both be displayed on screen:</span></span>

<span data-ttu-id="cbecc-128">TranslatedNumber MatchingRule</span><span class="sxs-lookup"><span data-stu-id="cbecc-128">TranslatedNumber MatchingRule</span></span>

<span data-ttu-id="cbecc-129">\---------------- ------------</span><span class="sxs-lookup"><span data-stu-id="cbecc-129">\---------------- ------------</span></span>

<span data-ttu-id="cbecc-130">\+12065551219 global/Redmond</span><span class="sxs-lookup"><span data-stu-id="cbecc-130">\+12065551219 Global/Redmond</span></span>

<span data-ttu-id="cbecc-131">Si le test échoue, Test-CsTrunkConfiguration renverra des valeurs de propriété vides :</span><span class="sxs-lookup"><span data-stu-id="cbecc-131">If the test fails, Test-CsTrunkConfiguration will return empty property values:</span></span>

<span data-ttu-id="cbecc-132">TranslatedNumber MatchingRule</span><span class="sxs-lookup"><span data-stu-id="cbecc-132">TranslatedNumber MatchingRule</span></span>

<span data-ttu-id="cbecc-133">\---------------- ------------</span><span class="sxs-lookup"><span data-stu-id="cbecc-133">\---------------- ------------</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="cbecc-134">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="cbecc-134">Reasons why the test might have failed</span></span>

<span data-ttu-id="cbecc-135">Si Test-CsTrunkConfiguration ne renvoie aucune correspondance qui signifie généralement que les paramètres de configuration de Trunk en cours de test ne disposent pas d’une règle de traduction d’un numéro de téléphone capable de convertir le numéro numéroté au format E. 164.</span><span class="sxs-lookup"><span data-stu-id="cbecc-135">If Test-CsTrunkConfiguration does not return a match that typically means that the trunk configuration settings being test do not have an outgoing calling number translation rule capable to converting the dialed number to the E.164 format.</span></span> <span data-ttu-id="cbecc-136">Pour récupérer les règles de traduction affectées à un ensemble de paramètres de configuration de Trunk, vous pouvez utiliser une syntaxe similaire à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="cbecc-136">To retrieve the translation rules assigned to a collection of trunk configuration settings, you can use syntax similar to this:</span></span>

`Get-CsTrunkConfiguration -Identity "global" | Select-Object -ExpandProperty OutboundTranslationRulesList`

<span data-ttu-id="cbecc-137">Cela renvoie des informations similaires à ce qui suit pour chaque règle de traduction :</span><span class="sxs-lookup"><span data-stu-id="cbecc-137">That returns information similar to this for each translation rule:</span></span>

<span data-ttu-id="cbecc-138">Description : numéros de téléphone sans code de pays ou indicatif régional.</span><span class="sxs-lookup"><span data-stu-id="cbecc-138">Description : Phone numbers without a country code or area code.</span></span>

<span data-ttu-id="cbecc-139">Modèle : ^ \\ + ( \\ d \* ) $</span><span class="sxs-lookup"><span data-stu-id="cbecc-139">Pattern : ^\\+(\\d\*)$</span></span>

`Translation : $1`

<span data-ttu-id="cbecc-140">Nom : NoAreaCode</span><span class="sxs-lookup"><span data-stu-id="cbecc-140">Name : NoAreaCode</span></span>

<span data-ttu-id="cbecc-141">À ce stade, vous vérifiez la valeur de la propriété Pattern (qui est une chaîne d' [expression régulière](https://go.microsoft.com/fwlink/?linkid=400464) ) pour vérifier si une des règles de traduction est configurée pour gérer le numéro numéroté.</span><span class="sxs-lookup"><span data-stu-id="cbecc-141">At that point, you check the value of the Pattern property (which is a [regular expression](https://go.microsoft.com/fwlink/?linkid=400464) string) to see whether any of the translation rules are configured to handle the dialed number.</span></span> <span data-ttu-id="cbecc-142">Si ce n’est pas le cas, vous devez modifier une des règles existantes (Set-CsOutboundTranslationRule) ou utiliser l’applet de l’applet de New-CsOutboundTranslationRule pour ajouter une nouvelle règle à la collection.</span><span class="sxs-lookup"><span data-stu-id="cbecc-142">If not, you'll either have to change one of the existing rules (Set-CsOutboundTranslationRule) or use the New-CsOutboundTranslationRule cmdlet to add a new rule to the collection.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="cbecc-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbecc-143">See Also</span></span>


[<span data-ttu-id="cbecc-144">Test-CsTrunkConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbecc-144">Test-CsTrunkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsTrunkConfiguration)  
  

<span data-ttu-id="cbecc-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cbecc-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

