---
title: 'Tableau Lync Server 2013 : VideoMetricsThreshold'
description: 'Tableau Lync Server 2013 : VideoMetricsThreshold'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoMetricsThreshold table
ms:assetid: 2e2f4711-35ba-48c6-b15b-5aba61c4eb75
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204778(v=OCS.15)
ms:contentKeyID: 48183736
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 93cdd6fb4c3c54ac1470499490f36fee87ba283d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438868"
---
# <a name="videometricsthreshold-table-in-lync-server-2013"></a><span data-ttu-id="709a6-103">Table VideoMetricsThreshold dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="709a6-103">VideoMetricsThreshold table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="709a6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="709a6-104">

<span> </span></span></span>

<span data-ttu-id="709a6-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="709a6-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="709a6-106">La table VideoMetricsThreshold contient des valeurs optimales et acceptables pour les métriques de qualité de l’utilisation des appels vidéo.</span><span class="sxs-lookup"><span data-stu-id="709a6-106">The VideoMetricsThreshold table contains optimal and acceptable values for the Quality of Experience metrics used with video calls.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="709a6-107"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-107"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="709a6-108"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-108"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="709a6-109"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-109"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="709a6-110"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-110"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="709a6-111"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-111"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="709a6-112">int</span><span class="sxs-lookup"><span data-stu-id="709a6-112">int</span></span></p></td>
<td><p><span data-ttu-id="709a6-113">Principal</span><span class="sxs-lookup"><span data-stu-id="709a6-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="709a6-114">Type d’appel placé.</span><span class="sxs-lookup"><span data-stu-id="709a6-114">Type of call that was placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709a6-115"><strong>VideoPostFECPLROptimal</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-115"><strong>VideoPostFECPLROptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="709a6-116">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="709a6-116">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="709a6-117">La valeur par défaut est 0,05.</span><span class="sxs-lookup"><span data-stu-id="709a6-117">The default value is 0.05.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709a6-118"><strong>VideoPostFECPLRAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-118"><strong>VideoPostFECPLRAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="709a6-119">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="709a6-119">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="709a6-120">La valeur par défaut est 0,10.</span><span class="sxs-lookup"><span data-stu-id="709a6-120">The default value is 0.10.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709a6-121"><strong>VideoLocalFrameLostPercentageAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-121"><strong>VideoLocalFrameLostPercentageAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="709a6-122">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="709a6-122">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="709a6-123">La valeur par défaut est 5,0.</span><span class="sxs-lookup"><span data-stu-id="709a6-123">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709a6-124"><strong>VideoLocalFrameLostPercentageAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-124"><strong>VideoLocalFrameLostPercentageAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="709a6-125">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="709a6-125">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="709a6-126">La valeur par défaut est 10,0.</span><span class="sxs-lookup"><span data-stu-id="709a6-126">The default value is 10.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709a6-127"><strong>RecvFrameRateAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-127"><strong>RecvFrameRateAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="709a6-128">décimale (9 ; 4)</span><span class="sxs-lookup"><span data-stu-id="709a6-128">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="709a6-129">La valeur par défaut est 12,0000.</span><span class="sxs-lookup"><span data-stu-id="709a6-129">The default value is 12.0000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709a6-130"><strong>RecvFramerateAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-130"><strong>RecvFramerateAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="709a6-131">décimale (9 ; 4)</span><span class="sxs-lookup"><span data-stu-id="709a6-131">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="709a6-132">La valeur par défaut est 7,0000.</span><span class="sxs-lookup"><span data-stu-id="709a6-132">The default value is 7.0000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709a6-133"><strong>LowFrameRateCallPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-133"><strong>LowFrameRateCallPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="709a6-134">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="709a6-134">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="709a6-135">La valeur par défaut est 5,0.</span><span class="sxs-lookup"><span data-stu-id="709a6-135">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709a6-136"><strong>LowFrameRateCallPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-136"><strong>LowFrameRateCallPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="709a6-137">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="709a6-137">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="709a6-138">La valeur par défaut est 10.0/</span><span class="sxs-lookup"><span data-stu-id="709a6-138">The default value is 10.0/</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709a6-139"><strong>LowResolutionCallPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-139"><strong>LowResolutionCallPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="709a6-140">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="709a6-140">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="709a6-141">La valeur par défaut est 5,0.</span><span class="sxs-lookup"><span data-stu-id="709a6-141">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709a6-142"><strong>LowResolutionCallPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-142"><strong>LowResolutionCallPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="709a6-143">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="709a6-143">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="709a6-144">La valeur par défaut est 10,0.</span><span class="sxs-lookup"><span data-stu-id="709a6-144">The default value is 10.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709a6-145"><strong>VideoPacketLossRateOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-145"><strong>VideoPacketLossRateOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="709a6-146">foat</span><span class="sxs-lookup"><span data-stu-id="709a6-146">foat</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="709a6-147">La valeur par défaut est 0,05.</span><span class="sxs-lookup"><span data-stu-id="709a6-147">The default value is 0.05.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709a6-148"><strong>VideoPacketLossRateAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-148"><strong>VideoPacketLossRateAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="709a6-149">float</span><span class="sxs-lookup"><span data-stu-id="709a6-149">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="709a6-150">La valeur par défaut est 0,10.</span><span class="sxs-lookup"><span data-stu-id="709a6-150">The default value is 0.10.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709a6-151"><strong>VideoFrameRateAvgOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-151"><strong>VideoFrameRateAvgOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="709a6-152">float</span><span class="sxs-lookup"><span data-stu-id="709a6-152">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="709a6-153">La valeur par défaut est 12.</span><span class="sxs-lookup"><span data-stu-id="709a6-153">The default value is 12.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709a6-154"><strong>VideoFrameRateAvgAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-154"><strong>VideoFrameRateAvgAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="709a6-155">float</span><span class="sxs-lookup"><span data-stu-id="709a6-155">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="709a6-156">La valeur par défaut est 7.</span><span class="sxs-lookup"><span data-stu-id="709a6-156">The default value is 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="709a6-157"><strong>DynamicCapabilityPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-157"><strong>DynamicCapabilityPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="709a6-158">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="709a6-158">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="709a6-159">La valeur par défaut est 5,00.</span><span class="sxs-lookup"><span data-stu-id="709a6-159">The default value is 5.00.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="709a6-160"><strong>DynamicCapabilityPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="709a6-160"><strong>DynamicCapabilityPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="709a6-161">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="709a6-161">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="709a6-162">La valeur par défaut est 10,00.</span><span class="sxs-lookup"><span data-stu-id="709a6-162">The default value is 10.00.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="709a6-163">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="709a6-163">


</div>

<span> </span>

</div>

</div>

</span></span></div>

