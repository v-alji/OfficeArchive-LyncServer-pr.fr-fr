---
title: 'Tableau Lync Server 2013 : AppSharingMetricsThreshold'
description: 'Tableau Lync Server 2013 : AppSharingMetricsThreshold'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppSharingMetricsThreshold table
ms:assetid: 782cfab9-01a6-4843-aea1-28f47b0b51f7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205018(v=OCS.15)
ms:contentKeyID: 48184556
ms.date: 12/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 092c7d08026e6b736b81043a71b4ecaabc4d5f1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439871"
---
# <a name="appsharingmetricsthreshold-table-in-lync-server-2013"></a><span data-ttu-id="982df-103">Table AppSharingMetricsThreshold dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="982df-103">AppSharingMetricsThreshold table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="982df-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="982df-104">

<span> </span></span></span>

<span data-ttu-id="982df-105">_**Dernière modification de la rubrique :** 2015-12-08_</span><span class="sxs-lookup"><span data-stu-id="982df-105">_**Topic Last Modified:** 2015-12-08_</span></span>

<span data-ttu-id="982df-106">La table AppSharingMetricsThreshold contient des valeurs optimales et acceptables pour la qualité de mesure d’utilisation utilisée avec le partage d’application.</span><span class="sxs-lookup"><span data-stu-id="982df-106">The AppSharingMetricsThreshold table contains optimal and acceptable values for the Quality of Experience metrics used with application sharing.</span></span> <span data-ttu-id="982df-107">Ces seuils sont utilisés pour déterminer si l’utilisation du partage d’application doit être considérée comme médiocre.</span><span class="sxs-lookup"><span data-stu-id="982df-107">These thresholds are used to determine if the application sharing experience should be classified as poor.</span></span>

<span data-ttu-id="982df-108">Ce tableau a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="982df-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="982df-109"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="982df-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="982df-110"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="982df-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="982df-111"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="982df-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="982df-112"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="982df-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="982df-113"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="982df-113"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="982df-114">int</span><span class="sxs-lookup"><span data-stu-id="982df-114">int</span></span></p></td>
<td><p><span data-ttu-id="982df-115">Principal</span><span class="sxs-lookup"><span data-stu-id="982df-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="982df-116">Type d’appel placé.</span><span class="sxs-lookup"><span data-stu-id="982df-116">Type of call that was placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="982df-117"><strong>AppliedBandwidthLimitOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="982df-117"><strong>AppliedBandwidthLimitOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="982df-118">int</span><span class="sxs-lookup"><span data-stu-id="982df-118">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="982df-119">Limite maximale de bande passante pour le partage d’application.</span><span class="sxs-lookup"><span data-stu-id="982df-119">Optimal bandwidth limitation for application sharing.</span></span> <span data-ttu-id="982df-120">La valeur par défaut est 1 million.</span><span class="sxs-lookup"><span data-stu-id="982df-120">The default value is 1000000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="982df-121"><strong>AppliedBandwidthLimitAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="982df-121"><strong>AppliedBandwidthLimitAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="982df-122">int</span><span class="sxs-lookup"><span data-stu-id="982df-122">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="982df-123">Limitation de bande passante acceptable pour le partage d’application.</span><span class="sxs-lookup"><span data-stu-id="982df-123">Acceptable bandwidth limitation for application sharing.</span></span> <span data-ttu-id="982df-124">La valeur par défaut est 500000.</span><span class="sxs-lookup"><span data-stu-id="982df-124">The default value is 500000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="982df-125"><strong>SpoiledTilePercentTotalOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="982df-125"><strong>SpoiledTilePercentTotalOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="982df-126">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="982df-126">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="982df-127">Taux de pourcentage optimal pour les vignettes « abîmées » permettant de classer une qualité de partage d’application.</span><span class="sxs-lookup"><span data-stu-id="982df-127">Optimal percentage rate for “spoiled” tiles for classifying an Application Sharing quality.</span></span> <span data-ttu-id="982df-128">Cette valeur correspond au pourcentage du contenu du partageur n’ayant pas atteint la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="982df-128">This value is the percentage of the content from the sharer that did not reach the viewer.</span></span> <span data-ttu-id="982df-129">Le contenu est susceptible d’être ignoré (ou abîmé) lorsque le partage annule les vignettes à partir de la source graphique ou que les vignettes ASMCU ignorent les vignettes du partage respectivement.</span><span class="sxs-lookup"><span data-stu-id="982df-129">Content may be discarded (or spoiled) when the sharer discards tiles from the graphics source or the ASMCU tiles discards tiles from Sharer respectively.</span></span> <span data-ttu-id="982df-130">La valeur par défaut est 11%.</span><span class="sxs-lookup"><span data-stu-id="982df-130">The default value is 11 percent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="982df-131"><strong>SpoiledTilePercentTotalAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="982df-131"><strong>SpoiledTilePercentTotalAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="982df-132">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="982df-132">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="982df-133">taux de cceptable pour les vignettes « abîmées » permettant de classer une qualité de partage d’application.</span><span class="sxs-lookup"><span data-stu-id="982df-133">cceptable percentage rate for “spoiled” tiles for classifying an Application Sharing quality.</span></span> <span data-ttu-id="982df-134">Cette valeur correspond au pourcentage du contenu du partageur n’ayant pas atteint la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="982df-134">This value is the percentage of the content from the sharer that did not reach the viewer.</span></span> <span data-ttu-id="982df-135">Le contenu est susceptible d’être ignoré (ou abîmé) lorsque le partage annule les vignettes à partir de la source graphique ou que les vignettes ASMCU ignorent les vignettes du partage respectivement.</span><span class="sxs-lookup"><span data-stu-id="982df-135">Content may be discarded (or spoiled) when the sharer discards tiles from the graphics source or the ASMCU tiles discards tiles from Sharer respectively.</span></span> <span data-ttu-id="982df-136">La valeur par défaut est 36%.</span><span class="sxs-lookup"><span data-stu-id="982df-136">The default value is 36 percent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="982df-137"><strong>JitterInterArrivalOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="982df-137"><strong>JitterInterArrivalOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="982df-138">int</span><span class="sxs-lookup"><span data-stu-id="982df-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="982df-139">Cette colonne n’est pas utilisée dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="982df-139">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="982df-140"><strong>JitterInterArrivalAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="982df-140"><strong>JitterInterArrivalAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="982df-141">int</span><span class="sxs-lookup"><span data-stu-id="982df-141">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="982df-142">Cette colonne n’est pas utilisée dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="982df-142">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="982df-143"><strong>RelativeOneWayBurstDensityOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="982df-143"><strong>RelativeOneWayBurstDensityOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="982df-144">float</span><span class="sxs-lookup"><span data-stu-id="982df-144">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="982df-145">Cette colonne n’est pas utilisée dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="982df-145">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="982df-146"><strong>RelativeOneWayBurstDensityAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="982df-146"><strong>RelativeOneWayBurstDensityAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="982df-147">float</span><span class="sxs-lookup"><span data-stu-id="982df-147">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="982df-148">Cette colonne n’est pas utilisée dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="982df-148">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="982df-149"><strong>RDPTileProcessingLatencyBurstDensityOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="982df-149"><strong>RDPTileProcessingLatencyBurstDensityOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="982df-150">float</span><span class="sxs-lookup"><span data-stu-id="982df-150">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="982df-151">Cette colonne n’est pas utilisée dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="982df-151">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="982df-152"><strong>RDPTileProcessingLatencyBurstDensityAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="982df-152"><strong>RDPTileProcessingLatencyBurstDensityAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="982df-153">float</span><span class="sxs-lookup"><span data-stu-id="982df-153">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="982df-154">Cette colonne n’est pas utilisée dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="982df-154">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="982df-155"><strong>RelativeOneWayAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="982df-155"><strong>RelativeOneWayAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="982df-156">float</span><span class="sxs-lookup"><span data-stu-id="982df-156">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="982df-157">Valeur optimale pour le retard relatif unidirectionnel entre les deux points de terminaison multimédias impliqués dans le partage d’application.</span><span class="sxs-lookup"><span data-stu-id="982df-157">Optimal value for the relative one-way delay between the two media endpoints involved in the application sharing.</span></span> <span data-ttu-id="982df-158">Il s’agit d’une mesure de latence sur un seul tronçon.</span><span class="sxs-lookup"><span data-stu-id="982df-158">This is a single-hop latency measure.</span></span> <span data-ttu-id="982df-159">La valeur par défaut est 1,0 secondes.</span><span class="sxs-lookup"><span data-stu-id="982df-159">The default value is 1.0 seconds.</span></span></p>
<p><span data-ttu-id="982df-160">La colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="982df-160">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="982df-161"><strong>RelativeOneWayAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="982df-161"><strong>RelativeOneWayAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="982df-162">float</span><span class="sxs-lookup"><span data-stu-id="982df-162">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="982df-163">Valeur optimale pour le retard relatif unidirectionnel entre les deux points de terminaison multimédias impliqués dans le partage d’application.</span><span class="sxs-lookup"><span data-stu-id="982df-163">Optimal value for the relative one-way delay between the two media endpoints involved in the application sharing.</span></span> <span data-ttu-id="982df-164">Il s’agit d’une mesure de latence sur un seul tronçon.</span><span class="sxs-lookup"><span data-stu-id="982df-164">This is a single-hop latency measure.</span></span> <span data-ttu-id="982df-165">La valeur par défaut est 1,75 secondes.</span><span class="sxs-lookup"><span data-stu-id="982df-165">The default value is 1.75 seconds.</span></span></p>
<p><span data-ttu-id="982df-166">La colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="982df-166">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="982df-167"><strong>RDPTileProcessingLatencyAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="982df-167"><strong>RDPTileProcessingLatencyAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="982df-168">float</span><span class="sxs-lookup"><span data-stu-id="982df-168">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="982df-169">Valeur optimale de la latence moyenne du traitement de vignettes RDP sur le serveur de conférence en tant que serveur de conférence en fonction de la durée de la session d’affichage.</span><span class="sxs-lookup"><span data-stu-id="982df-169">Optimal value of the average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session.</span></span> <span data-ttu-id="982df-170">La latence correspond au temps entre le moment où l’image de début est encodé sur le serveur (le partage ou la MCU en fonction du scénario) et la même image de démarrage est décodée sur la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="982df-170">Latency is the time difference between when the Start Frame is encoded on the server (sharer or MCU depending on the scenario) and the same Start Frame is decoded on the viewer.</span></span></p>
<p><span data-ttu-id="982df-171">Une moyenne élevée indique un délai plus long pour l’expérience de visionnage.</span><span class="sxs-lookup"><span data-stu-id="982df-171">A high average reflects a longer delay in the viewing experience.</span></span> <span data-ttu-id="982df-172">Un serveur de conférence surchargé peut rencontrer des délais moyens plus élevés.</span><span class="sxs-lookup"><span data-stu-id="982df-172">An overloaded conferencing server may experience higher average delays.</span></span> <span data-ttu-id="982df-173">La valeur par défaut est 200 millions.</span><span class="sxs-lookup"><span data-stu-id="982df-173">The default value is 200ms.</span></span></p>
<p><span data-ttu-id="982df-174">La colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="982df-174">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="982df-175"><strong>RDPTileProcessingLatencyAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="982df-175"><strong>RDPTileProcessingLatencyAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="982df-176">float</span><span class="sxs-lookup"><span data-stu-id="982df-176">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="982df-177">Valeur acceptable de la latence moyenne du traitement de vignettes RDP sur le serveur de conférence en tant que serveur de conférence en fonction de la durée de la session d’affichage.</span><span class="sxs-lookup"><span data-stu-id="982df-177">Acceptable value of the average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session.</span></span> <span data-ttu-id="982df-178">La latence correspond au temps entre le moment où l’image de début est encodé sur le serveur (le partage ou la MCU en fonction du scénario) et la même image de démarrage est décodée sur la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="982df-178">Latency is the time difference between when the Start Frame is encoded on the server (sharer or MCU depending on the scenario) and the same Start Frame is decoded on the viewer.</span></span></p>
<p><span data-ttu-id="982df-179">Une moyenne élevée indique un délai plus long pour l’expérience de visionnage.</span><span class="sxs-lookup"><span data-stu-id="982df-179">A high average reflects a longer delay in the viewing experience.</span></span> <span data-ttu-id="982df-180">Un serveur de conférence surchargé peut rencontrer des délais moyens plus élevés.</span><span class="sxs-lookup"><span data-stu-id="982df-180">An overloaded conferencing server may experience higher average delays.</span></span> <span data-ttu-id="982df-181">La valeur par défaut est 200 millions.</span><span class="sxs-lookup"><span data-stu-id="982df-181">The default value is 200ms.</span></span></p>
<p><span data-ttu-id="982df-182">La colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="982df-182">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="982df-183">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="982df-183">


</div>

<span> </span>

</div>

</div>

</span></span></div>

