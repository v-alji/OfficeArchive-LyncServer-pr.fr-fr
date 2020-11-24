---
title: 'Lync Server 2013 : règles de traduction'
description: 'Lync Server 2013 : règles de traduction.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Translation rules
ms:assetid: 6e067bd4-4931-4385-81ac-2acae45a16d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398520(v=OCS.15)
ms:contentKeyID: 48184460
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 65ee21459123ea09f54eb52e65a4d9ecba61c386
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393776"
---
# <a name="translation-rules-in-lync-server-2013"></a><span data-ttu-id="a16b6-103">Règles de traduction dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a16b6-103">Translation rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a16b6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a16b6-104">

<span> </span></span></span>

<span data-ttu-id="a16b6-105">_**Dernière modification de la rubrique :** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="a16b6-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="a16b6-106">Lync Server 2013 voix entreprise nécessite que toutes les chaînes de numérotation soient normalisées au format E. 164 pour pouvoir exécuter la recherche de numéro inverse (RNL).</span><span class="sxs-lookup"><span data-stu-id="a16b6-106">Lync Server 2013 Enterprise Voice requires that all dial strings be normalized to E.164 format for the purpose of performing reverse number lookup (RNL).</span></span> <span data-ttu-id="a16b6-107">Dans Microsoft Lync Server 2010, les règles de traduction sont uniquement prises en charge pour les numéros appelés.</span><span class="sxs-lookup"><span data-stu-id="a16b6-107">In Microsoft Lync Server 2010, translation rules are supported only for called numbers.</span></span> <span data-ttu-id="a16b6-108">Les règles de traduction suivantes sont également prises en charge dans Microsoft Lync Server 2013 pour les numéros d’appel.</span><span class="sxs-lookup"><span data-stu-id="a16b6-108">New in Microsoft Lync Server 2013, translation rules are also supported for calling numbers.</span></span> <span data-ttu-id="a16b6-109">L’*homologue de jonction* (c’est-à-dire la jonction de passerelle, PBX ou SIP associée) peut exiger que les numéros soient au format de numérotation local.</span><span class="sxs-lookup"><span data-stu-id="a16b6-109">The *trunk peer* (that is, the associated gateway, private branch exchange (PBX), or SIP trunk) may require that numbers be in a local dialing format.</span></span> <span data-ttu-id="a16b6-110">Pour convertir les numéros du format E.164 au format de numérotation local, vous pouvez définir une ou plusieurs règles de conversion pour manipuler l’URI demandé avant de l’acheminer vers l’homologue de jonction.</span><span class="sxs-lookup"><span data-stu-id="a16b6-110">To translate numbers from E.164 format to a local dialing format, you can define one or more translation rules to manipulate the request URI before you route it to the trunk peer.</span></span> <span data-ttu-id="a16b6-111">Par exemple, vous pouvez rédiger une règle pour supprimer la valeur « +44 » au début de la chaîne de numérotation et la remplacer par « 0144 ».</span><span class="sxs-lookup"><span data-stu-id="a16b6-111">For example, you could write a translation rule to remove +44 from the beginning of a dial string and replace it with 0144.</span></span>

<span data-ttu-id="a16b6-112">En effectuant une conversion de l’itinéraire sortant sur le serveur, vous pouvez réduire les exigences de configuration sur chaque homologue de jonction afin de convertir les numéros de téléphone dans un format de numérotation local.</span><span class="sxs-lookup"><span data-stu-id="a16b6-112">By performing outbound route translation on the server, you can reduce the configuration requirements on each individual trunk peer in order to translate phone numbers into a local dialing format.</span></span> <span data-ttu-id="a16b6-113">Lorsque vous planifiez les passerelles et le nombre de passerelles à associer à un cluster de serveurs de médiation spécifique, il est possible que les homologues de groupe puissent s’avérer utiles pour la numérotation locale.</span><span class="sxs-lookup"><span data-stu-id="a16b6-113">When you plan which gateways, and how many gateways, to associate with a specific Mediation Server cluster, it may be useful to group trunk peers with similar local dialing requirements.</span></span> <span data-ttu-id="a16b6-114">En effet, cela peut réduire le nombre de règles de conversion requises et le temps nécessaire pour les rédiger.</span><span class="sxs-lookup"><span data-stu-id="a16b6-114">This can reduce the number of required translation rules and the time it takes to write them.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a16b6-115">L’Association d’une ou plusieurs règles de traduction à une configuration de Trunk voix entreprise doit être utilisée comme alternative à la configuration de règles de traduction sur l’homologue de Trunk.</span><span class="sxs-lookup"><span data-stu-id="a16b6-115">Associating one or more translation rules with an Enterprise Voice trunk configuration should be used as an alternative to configuring translation rules on the trunk peer.</span></span> <span data-ttu-id="a16b6-116">N’associez pas de règles de traduction à une configuration de Trunk vocale d’entreprise si vous avez configuré des règles de traduction sur l’homologue de Trunk, car les deux règles peuvent entrer en conflit.</span><span class="sxs-lookup"><span data-stu-id="a16b6-116">Do not associate translation rules with an Enterprise Voice trunk configuration if you have configured translation rules on the trunk peer, because the two rules might conflict.</span></span>



</div>

<div>

## <a name="example-translation-rules"></a><span data-ttu-id="a16b6-117">Exemples de règles de conversion</span><span class="sxs-lookup"><span data-stu-id="a16b6-117">Example Translation Rules</span></span>

<span data-ttu-id="a16b6-118">Les exemples de règles de conversion suivantes vous montrent comment développer des règles sur le serveur pour convertir des numéros du format E.164 au format local pour un homologue de jonction.</span><span class="sxs-lookup"><span data-stu-id="a16b6-118">The following examples of translation rules show how you can develop rules on the server to translate numbers from E.164 format to a local format for the trunk peer.</span></span>

<span data-ttu-id="a16b6-119">Pour plus d’informations sur l’implémentation des règles de traduction, voir [définition des règles de traduction dans Lync Server 2013](lync-server-2013-defining-translation-rules.md) dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="a16b6-119">For details about how to implement translation rules, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>


<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a16b6-120">Description</span><span class="sxs-lookup"><span data-stu-id="a16b6-120">Description</span></span></th>
<th><span data-ttu-id="a16b6-121">Chiffres de début</span><span class="sxs-lookup"><span data-stu-id="a16b6-121">Starting Digits</span></span></th>
<th><span data-ttu-id="a16b6-122">Longueur</span><span class="sxs-lookup"><span data-stu-id="a16b6-122">Length</span></span></th>
<th><span data-ttu-id="a16b6-123">Chiffres à supprimer</span><span class="sxs-lookup"><span data-stu-id="a16b6-123">Digits to Remove</span></span></th>
<th><span data-ttu-id="a16b6-124">Chiffres à ajouter</span><span class="sxs-lookup"><span data-stu-id="a16b6-124">Digits to Add</span></span></th>
<th><span data-ttu-id="a16b6-125">Modèle de correspondance</span><span class="sxs-lookup"><span data-stu-id="a16b6-125">Matching Pattern</span></span></th>
<th><span data-ttu-id="a16b6-126">Conversion</span><span class="sxs-lookup"><span data-stu-id="a16b6-126">Translation</span></span></th>
<th><span data-ttu-id="a16b6-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="a16b6-127">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a16b6-128">Numérotation longue distance conventionnelle aux États-Unis</span><span class="sxs-lookup"><span data-stu-id="a16b6-128">Conventional long-distance dialing in U.S.</span></span></p>
<p><span data-ttu-id="a16b6-129">(supprimer le signe ’+’)</span><span class="sxs-lookup"><span data-stu-id="a16b6-129">(strip out the ‘+’)</span></span></p></td>
<td><p><span data-ttu-id="a16b6-130">+1</span><span class="sxs-lookup"><span data-stu-id="a16b6-130">+1</span></span></p></td>
<td><p><span data-ttu-id="a16b6-131">12 exactement</span><span class="sxs-lookup"><span data-stu-id="a16b6-131">Exactly 12</span></span></p></td>
<td><p><span data-ttu-id="a16b6-132">1</span><span class="sxs-lookup"><span data-stu-id="a16b6-132">1</span></span></p></td>
<td><p><span data-ttu-id="a16b6-133">0,4</span><span class="sxs-lookup"><span data-stu-id="a16b6-133">0</span></span></p></td>
<td><p><span data-ttu-id="a16b6-134">^\+(1 \ d {10} ) $</span><span class="sxs-lookup"><span data-stu-id="a16b6-134">^\+(1\d{10})$</span></span></p></td>
<td><p><span data-ttu-id="a16b6-135">$1</span><span class="sxs-lookup"><span data-stu-id="a16b6-135">$1</span></span></p></td>
<td><p><span data-ttu-id="a16b6-136">+14255551010 devient 14255551010</span><span class="sxs-lookup"><span data-stu-id="a16b6-136">+14255551010 becomes 14255551010</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a16b6-137">Numérotation longue distance internationale aux États-Unis</span><span class="sxs-lookup"><span data-stu-id="a16b6-137">U.S. international long-distance dialing</span></span></p>
<p><span data-ttu-id="a16b6-138">(supprimer le signe ’+’ et ajouter 011)</span><span class="sxs-lookup"><span data-stu-id="a16b6-138">(strip out ‘+’ and add 011)</span></span></p></td>
<td><p>+</p></td>
<td><p><span data-ttu-id="a16b6-139">11 au moins</span><span class="sxs-lookup"><span data-stu-id="a16b6-139">At least 11</span></span></p></td>
<td><p><span data-ttu-id="a16b6-140">1</span><span class="sxs-lookup"><span data-stu-id="a16b6-140">1</span></span></p></td>
<td><p><span data-ttu-id="a16b6-141">011</span><span class="sxs-lookup"><span data-stu-id="a16b6-141">011</span></span></p></td>
<td><p><span data-ttu-id="a16b6-142">^\+(\d {9} \d +) $</span><span class="sxs-lookup"><span data-stu-id="a16b6-142">^\+(\d{9}\d+)$</span></span></p></td>
<td><p><span data-ttu-id="a16b6-143">011$1</span><span class="sxs-lookup"><span data-stu-id="a16b6-143">011$1</span></span></p></td>
<td><p><span data-ttu-id="a16b6-144">+441235551010 devient 011441235551010</span><span class="sxs-lookup"><span data-stu-id="a16b6-144">+441235551010 becomes 011441235551010</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a16b6-145">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a16b6-145">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

