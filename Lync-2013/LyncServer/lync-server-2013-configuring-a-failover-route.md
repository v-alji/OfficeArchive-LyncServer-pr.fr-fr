---
title: 'Lync Server 2013 : Configuration d’un itinéraire de basculement'
description: 'Lync Server 2013 : configuration d’un itinéraire de basculement.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a failover route
ms:assetid: 76e48df4-3b78-4fb7-b1f7-c1e604b81bad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398581(v=OCS.15)
ms:contentKeyID: 48184542
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7cfc45276931685a2d42103b1b7f1d5015dcd7e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433520"
---
# <a name="configuring-a-failover-route-in-lync-server-2013"></a><span data-ttu-id="d7976-103">Configuration d’un itinéraire de basculement dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7976-103">Configuring a failover route in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d7976-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d7976-104">

<span> </span></span></span>

<span data-ttu-id="d7976-105">_**Dernière modification de la rubrique :** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="d7976-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="d7976-p101">L’exemple suivant montre comment un administrateur peut définir un itinéraire de basculement à utiliser en cas de maintenance ou d’indisponibilité de Dallas-GW1. Les tableaux suivants illustrent la modification de configuration requise.</span><span class="sxs-lookup"><span data-stu-id="d7976-p101">The following example shows how an administrator can define a failover route for use if the Dallas-GW1 is down for maintenance or is otherwise unavailable. The following tables illustrate the required configuration change.</span></span>

### <a name="table-1-user-policy"></a><span data-ttu-id="d7976-p102">Tableau 1. Stratégie utilisateur</span><span class="sxs-lookup"><span data-stu-id="d7976-p102">Table 1. User Policy</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7976-110">Stratégie utilisateur</span><span class="sxs-lookup"><span data-stu-id="d7976-110">User policy</span></span></th>
<th><span data-ttu-id="d7976-111">Utilisation téléphonique</span><span class="sxs-lookup"><span data-stu-id="d7976-111">Phone usage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7976-112">Default Calling Policy</span><span class="sxs-lookup"><span data-stu-id="d7976-112">Default Calling Policy</span></span></p></td>
<td><p><span data-ttu-id="d7976-113">Local</span><span class="sxs-lookup"><span data-stu-id="d7976-113">Local</span></span></p>
<p><span data-ttu-id="d7976-114">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="d7976-114">GlobalPSTNHopoff</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7976-115">Redmond Local Policy</span><span class="sxs-lookup"><span data-stu-id="d7976-115">Redmond Local Policy</span></span></p></td>
<td><p><span data-ttu-id="d7976-116">RedmondLocal</span><span class="sxs-lookup"><span data-stu-id="d7976-116">RedmondLocal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7976-117">Dallas Calling Policy</span><span class="sxs-lookup"><span data-stu-id="d7976-117">Dallas Calling Policy</span></span></p></td>
<td><p><span data-ttu-id="d7976-118">DallasUsers</span><span class="sxs-lookup"><span data-stu-id="d7976-118">DallasUsers</span></span></p>
<p><span data-ttu-id="d7976-119">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="d7976-119">GlobalPSTNHopoff</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-2-routes"></a><span data-ttu-id="d7976-p103">Tableau 2. Itinéraires</span><span class="sxs-lookup"><span data-stu-id="d7976-p103">Table 2. Routes</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7976-122">Nom de l’itinéraire</span><span class="sxs-lookup"><span data-stu-id="d7976-122">Route name</span></span></th>
<th><span data-ttu-id="d7976-123">Type de numéro</span><span class="sxs-lookup"><span data-stu-id="d7976-123">Number pattern</span></span></th>
<th><span data-ttu-id="d7976-124">Utilisation téléphonique</span><span class="sxs-lookup"><span data-stu-id="d7976-124">Phone usage</span></span></th>
<th><span data-ttu-id="d7976-125">Jonction</span><span class="sxs-lookup"><span data-stu-id="d7976-125">Trunk</span></span></th>
<th><span data-ttu-id="d7976-126">Passerelle</span><span class="sxs-lookup"><span data-stu-id="d7976-126">Gateway</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7976-127">Redmond Local Route</span><span class="sxs-lookup"><span data-stu-id="d7976-127">Redmond Local Route</span></span></p></td>
<td><p><span data-ttu-id="d7976-128">^\+1 (425 | 206 | 253) (\d {7} ) $</span><span class="sxs-lookup"><span data-stu-id="d7976-128">^\+1(425|206|253)(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="d7976-129">Local</span><span class="sxs-lookup"><span data-stu-id="d7976-129">Local</span></span></p>
<p><span data-ttu-id="d7976-130">RedmondLocal</span><span class="sxs-lookup"><span data-stu-id="d7976-130">RedmondLocal</span></span></p></td>
<td><p><span data-ttu-id="d7976-131">Trunk1</span><span class="sxs-lookup"><span data-stu-id="d7976-131">Trunk1</span></span></p>
<p><span data-ttu-id="d7976-132">Trunk2</span><span class="sxs-lookup"><span data-stu-id="d7976-132">Trunk2</span></span></p></td>
<td><p><span data-ttu-id="d7976-133">Red-GW1</span><span class="sxs-lookup"><span data-stu-id="d7976-133">Red-GW1</span></span></p>
<p><span data-ttu-id="d7976-134">Red-GW2</span><span class="sxs-lookup"><span data-stu-id="d7976-134">Red-GW2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7976-135">Dallas Local Route</span><span class="sxs-lookup"><span data-stu-id="d7976-135">Dallas Local Route</span></span></p></td>
<td><p><span data-ttu-id="d7976-136">^\+1 (972 | 214 | 469) (\d {7} ) $</span><span class="sxs-lookup"><span data-stu-id="d7976-136">^\+1(972|214|469)(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="d7976-137">Local</span><span class="sxs-lookup"><span data-stu-id="d7976-137">Local</span></span></p></td>
<td><p><span data-ttu-id="d7976-138">Trunk3</span><span class="sxs-lookup"><span data-stu-id="d7976-138">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="d7976-139">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="d7976-139">Dallas-GW1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7976-140">Universal Route</span><span class="sxs-lookup"><span data-stu-id="d7976-140">Universal Route</span></span></p></td>
<td><p><span data-ttu-id="d7976-141">^\+? (\d \*) $</span><span class="sxs-lookup"><span data-stu-id="d7976-141">^\+?(\d\*)$</span></span></p></td>
<td><p><span data-ttu-id="d7976-142">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="d7976-142">GlobalPSTNHopoff</span></span></p></td>
<td><p><span data-ttu-id="d7976-143">Trunk1</span><span class="sxs-lookup"><span data-stu-id="d7976-143">Trunk1</span></span></p>
<p><span data-ttu-id="d7976-144">Trunk2</span><span class="sxs-lookup"><span data-stu-id="d7976-144">Trunk2</span></span></p>
<p><span data-ttu-id="d7976-145">Trunk3</span><span class="sxs-lookup"><span data-stu-id="d7976-145">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="d7976-146">Red-GW1</span><span class="sxs-lookup"><span data-stu-id="d7976-146">Red-GW1</span></span></p>
<p><span data-ttu-id="d7976-147">Red-GW2</span><span class="sxs-lookup"><span data-stu-id="d7976-147">Red-GW2</span></span></p>
<p><span data-ttu-id="d7976-148">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="d7976-148">Dallas-GW1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7976-149">Dallas Users Route</span><span class="sxs-lookup"><span data-stu-id="d7976-149">Dallas Users Route</span></span></p></td>
<td><p><span data-ttu-id="d7976-150">^\+? (\d \*) $</span><span class="sxs-lookup"><span data-stu-id="d7976-150">^\+?(\d\*)$</span></span></p></td>
<td><p><span data-ttu-id="d7976-151">DallasUsers</span><span class="sxs-lookup"><span data-stu-id="d7976-151">DallasUsers</span></span></p></td>
<td><p><span data-ttu-id="d7976-152">Trunk3</span><span class="sxs-lookup"><span data-stu-id="d7976-152">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="d7976-153">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="d7976-153">Dallas-GW1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d7976-p104">Dans le tableau 1, une utilisation téléphonique GlobalPSTNHopoff est ajoutée après l’utilisation téléphonique DallasUsers dans la stratégie Dallas Calling Policy. Cela permet aux appels dotés de la stratégie Dallas Calling Policy d’utiliser des itinéraires configurés pour l’utilisation téléphonique GlobalPSTNHopoff, lorsqu’aucun itinéraire n’est disponible pour l’utilisation téléphonique DallasUsers.</span><span class="sxs-lookup"><span data-stu-id="d7976-p104">In Table 1, a phone usage of GlobalPSTNHopoff is added after the DallasUsers phone usage in the Dallas Calling Policy. This enables calls with the Dallas Calling policy to use routes that are configured for the GlobalPSTNHopoff phone usage if a route for the DallasUsers phone usage is unavailable.</span></span>

<span data-ttu-id="d7976-156"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d7976-156"></div>

<span> </span>

</div>

</div>

</span></span></div>

