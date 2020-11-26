---
title: 'Lync Server 2013 : Table AudioStream'
description: 'Tableau Lync Server 2013 : AudioStream'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioStream table
ms:assetid: 49ccbbc3-2f73-45fc-80a6-e612535cbc10
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425961(v=OCS.15)
ms:contentKeyID: 48184077
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af2e622e14c54fa4f9a6313e1b0dae8f2483132
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438175"
---
# <a name="audiostream-table-in-lync-server-2013"></a><span data-ttu-id="24473-103">Table AudioStream dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="24473-103">AudioStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="24473-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="24473-104">

<span> </span></span></span>

<span data-ttu-id="24473-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="24473-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="24473-106">Chaque enregistrement représente un flux audio.</span><span class="sxs-lookup"><span data-stu-id="24473-106">Each record represents one audio stream.</span></span> <span data-ttu-id="24473-107">Une ligne de médias audio contient généralement deux flux audio.</span><span class="sxs-lookup"><span data-stu-id="24473-107">One audio media line usually contains two audio streams.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24473-108"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="24473-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="24473-109"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="24473-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="24473-110"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="24473-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="24473-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="24473-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24473-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="24473-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="24473-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="24473-114">Principal</span><span class="sxs-lookup"><span data-stu-id="24473-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="24473-115">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="24473-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="24473-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-117">int</span><span class="sxs-lookup"><span data-stu-id="24473-117">int</span></span></p></td>
<td><p><span data-ttu-id="24473-118">Principal</span><span class="sxs-lookup"><span data-stu-id="24473-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="24473-119">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="24473-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="24473-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="24473-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="24473-122">Principal</span><span class="sxs-lookup"><span data-stu-id="24473-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="24473-123">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="24473-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-124"><strong>StreamID</strong></span><span class="sxs-lookup"><span data-stu-id="24473-124"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-125">int</span><span class="sxs-lookup"><span data-stu-id="24473-125">int</span></span></p></td>
<td><p><span data-ttu-id="24473-126">Principal</span><span class="sxs-lookup"><span data-stu-id="24473-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="24473-127">IDENTIFIant unique dans une ligne de médias.</span><span class="sxs-lookup"><span data-stu-id="24473-127">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-128"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="24473-128"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-129">int</span><span class="sxs-lookup"><span data-stu-id="24473-129">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-130">Gigue réseau moyenne des statistiques de protocole RTCP (Real Time Control Protocol).</span><span class="sxs-lookup"><span data-stu-id="24473-130">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-131"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="24473-131"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-132">int</span><span class="sxs-lookup"><span data-stu-id="24473-132">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-133">Scintillement du réseau maximum lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="24473-133">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-134"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="24473-134"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-135">décimale (5 ; 4)</span><span class="sxs-lookup"><span data-stu-id="24473-135">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-136">Taux moyen de perte de paquets lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="24473-136">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-137"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="24473-137"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-138">décimale (5 ; 4)</span><span class="sxs-lookup"><span data-stu-id="24473-138">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-139">Perte de paquets maximum observée pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="24473-139">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-140"><strong>BurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="24473-140"><strong>BurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-141">décimale (9 ; 4)</span><span class="sxs-lookup"><span data-stu-id="24473-141">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-142">Densité moyenne de perte de paquets en rafales de pertes pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="24473-142">Average density of packet Loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-143"><strong>BurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="24473-143"><strong>BurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-144">int</span><span class="sxs-lookup"><span data-stu-id="24473-144">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-145">Durée moyenne de perte de paquets en rafales de pertes pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="24473-145">Average duration of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-146"><strong>BurstGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="24473-146"><strong>BurstGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-147">décimale (9 ; 4)</span><span class="sxs-lookup"><span data-stu-id="24473-147">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-148">Densité moyenne de perte de paquets lors de l’intervalle entre les pics de perte de paquets.</span><span class="sxs-lookup"><span data-stu-id="24473-148">Average density of packet loss during gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-149"><strong>BurstGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="24473-149"><strong>BurstGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-150">int</span><span class="sxs-lookup"><span data-stu-id="24473-150">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-151">Durée moyenne des espaces entre les pics de perte de paquets.</span><span class="sxs-lookup"><span data-stu-id="24473-151">Average duration of gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-152"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="24473-152"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-153">Ent</span><span class="sxs-lookup"><span data-stu-id="24473-153">Int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-154">Nombre de paquets pour le flux audio.</span><span class="sxs-lookup"><span data-stu-id="24473-154">Packet count for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-155"><strong>Bande passante</strong></span><span class="sxs-lookup"><span data-stu-id="24473-155"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-156">Ent</span><span class="sxs-lookup"><span data-stu-id="24473-156">Int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-157">Estimations de bande passante pour le flux audio.</span><span class="sxs-lookup"><span data-stu-id="24473-157">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-158"><strong>DegradationAvg</strong></span><span class="sxs-lookup"><span data-stu-id="24473-158"><strong>DegradationAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-159">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="24473-159">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-160">Baisse de la dégradation du réseau pour l’ensemble de l’appel.</span><span class="sxs-lookup"><span data-stu-id="24473-160">Network MOS Degradation for the whole call.</span></span> <span data-ttu-id="24473-161">La plage est 0,0 à 5,0.</span><span class="sxs-lookup"><span data-stu-id="24473-161">Range is 0.0 to 5.0.</span></span> <span data-ttu-id="24473-162">Cette mesure indique la somme que le coût du réseau a diminué en raison de la gigue et de la perte de paquets.</span><span class="sxs-lookup"><span data-stu-id="24473-162">This metric shows the amount the Network MOS was reduced because of jitter and packet loss.</span></span> <span data-ttu-id="24473-163">Pour une qualité acceptable, elle doit être inférieure à 0,5.</span><span class="sxs-lookup"><span data-stu-id="24473-163">For acceptable quality it should less than 0.5.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-164"><strong>DegradationMax</strong></span><span class="sxs-lookup"><span data-stu-id="24473-164"><strong>DegradationMax</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-165">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="24473-165">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-166">Dégradation du réseau maximal pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="24473-166">Maximum Network MOS degradation during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-167"><strong>DegradationJitterAvg</strong></span><span class="sxs-lookup"><span data-stu-id="24473-167"><strong>DegradationJitterAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-168">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="24473-168">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-169">Baisse de la dégradation du réseau à l’origine de gigue.</span><span class="sxs-lookup"><span data-stu-id="24473-169">Network MOS degradation caused by jitter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-170"><strong>DegradationPacketLossAvg</strong></span><span class="sxs-lookup"><span data-stu-id="24473-170"><strong>DegradationPacketLossAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-171">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="24473-171">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-172">Baisse de la dégradation du réseau à l’origine de la perte de paquets.</span><span class="sxs-lookup"><span data-stu-id="24473-172">Network MOS degradation caused by packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-173"><strong>AudioPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="24473-173"><strong>AudioPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-174">int</span><span class="sxs-lookup"><span data-stu-id="24473-174">int</span></span></p></td>
<td><p><span data-ttu-id="24473-175">Externes</span><span class="sxs-lookup"><span data-stu-id="24473-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="24473-176">Le codec audio utilisé pour l’appel, référencé à partir de la table PayloadDescription.</span><span class="sxs-lookup"><span data-stu-id="24473-176">The audio Codec used for the call, referenced from PayloadDescription Table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-177"><strong>AudioSampleRate</strong></span><span class="sxs-lookup"><span data-stu-id="24473-177"><strong>AudioSampleRate</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-178">int</span><span class="sxs-lookup"><span data-stu-id="24473-178">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-179">Taux d’échantillonnage pour le flux audio.</span><span class="sxs-lookup"><span data-stu-id="24473-179">Sampling rate for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-180"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="24473-180"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-181">int</span><span class="sxs-lookup"><span data-stu-id="24473-181">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-182">Durée de l’aller-retour des statistiques RTCP.</span><span class="sxs-lookup"><span data-stu-id="24473-182">Round trip time from RTCP statistics.</span></span> <span data-ttu-id="24473-183">Pour une qualité acceptable, il devrait être inférieur à 100 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="24473-183">For acceptable quality this should be less than 100ms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-184"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="24473-184"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-185">int</span><span class="sxs-lookup"><span data-stu-id="24473-185">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-186">Durée de l’aller-retour maximal pour le flux audio.</span><span class="sxs-lookup"><span data-stu-id="24473-186">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-187"><strong>OverallAvgNetworkMOS</strong></span><span class="sxs-lookup"><span data-stu-id="24473-187"><strong>OverallAvgNetworkMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-188">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="24473-188">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-189">MOS du réseau à bandes moyenne pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="24473-189">Average wideband Network MOS for the call.</span></span> <span data-ttu-id="24473-190">Cette métrique dépend du niveau de perte de paquets, de gigue et de codec utilisés.</span><span class="sxs-lookup"><span data-stu-id="24473-190">This metric depends on the packet loss, jitter, and codec used.</span></span> <span data-ttu-id="24473-191">La plage est [1,0 à 5,0].</span><span class="sxs-lookup"><span data-stu-id="24473-191">Range is [1.0 to 5.0].</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-192"><strong>OverallMinNetworkMOS</strong></span><span class="sxs-lookup"><span data-stu-id="24473-192"><strong>OverallMinNetworkMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-193">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="24473-193">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-194">Le réseau de bandes minimum pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="24473-194">The minimum wideband Network MOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-195"><strong>SendListenMOS</strong></span><span class="sxs-lookup"><span data-stu-id="24473-195"><strong>SendListenMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-196">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="24473-196">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-197">Le score d’écoute de la bande moyenne prédite pour le son envoyé, y compris le niveau de voix, le niveau de bruit et les caractéristiques de l’appareil de capture.</span><span class="sxs-lookup"><span data-stu-id="24473-197">The average predicted wideband Listening MOS score for audio sent, including speech level, noise level and capture device characteristics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-198"><strong>SendListenMOSMin</strong></span><span class="sxs-lookup"><span data-stu-id="24473-198"><strong>SendListenMOSMin</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-199">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="24473-199">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-200">Le minimum SendListenMOS pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="24473-200">The minimum SendListenMOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-201"><strong>RecvListenMOS</strong></span><span class="sxs-lookup"><span data-stu-id="24473-201"><strong>RecvListenMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-202">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="24473-202">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-203">Le score d’écoute de la bande moyenne prédite pour le son reçu du réseau, notamment le niveau de voix, le niveau sonore, le codec, les conditions du réseau et les caractéristiques de l’appareil de capture.</span><span class="sxs-lookup"><span data-stu-id="24473-203">The average predicted wideband Listening MOS score for audio received from the network including speech level, noise level, codec, network conditions and capture device characteristics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-204"><strong>RecvListenMOSMin</strong></span><span class="sxs-lookup"><span data-stu-id="24473-204"><strong>RecvListenMOSMin</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-205">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="24473-205">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-206">Le minimum RecvListenMOS pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="24473-206">The minimum RecvListenMOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-207"><strong>AudioFECUsed</strong></span><span class="sxs-lookup"><span data-stu-id="24473-207"><strong>AudioFECUsed</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-208">bit</span><span class="sxs-lookup"><span data-stu-id="24473-208">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-209">Indicateur indiquant si l’audio FEC a été utilisé pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="24473-209">Flag indicating if audio FEC was used for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-210"><strong>RatioConcealedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="24473-210"><strong>RatioConcealedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-211">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="24473-211">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-212">Taux moyen d’échantillons masqués générés par la correction audio sur des exemples classiques.</span><span class="sxs-lookup"><span data-stu-id="24473-212">Average ratio of concealed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-213"><strong>RatioStretchedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="24473-213"><strong>RatioStretchedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-214">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="24473-214">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-215">Taux moyen d’échantillons étirés générés par la correction audio sur des exemples classiques.</span><span class="sxs-lookup"><span data-stu-id="24473-215">Average ratio of stretched samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-216"><strong>RatioCompressedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="24473-216"><strong>RatioCompressedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-217">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="24473-217">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-218">Taux moyen d’échantillons compressés générés par la correction audio sur des exemples classiques.</span><span class="sxs-lookup"><span data-stu-id="24473-218">Average ratio of compressed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-219"><strong>Entrant</strong></span><span class="sxs-lookup"><span data-stu-id="24473-219"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-220">bit</span><span class="sxs-lookup"><span data-stu-id="24473-220">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-221">Des données de flux sur le côté du destinataire sont reçues.</span><span class="sxs-lookup"><span data-stu-id="24473-221">Stream data on receiver side is received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-222"><strong>Sortant</strong></span><span class="sxs-lookup"><span data-stu-id="24473-222"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-223">bit</span><span class="sxs-lookup"><span data-stu-id="24473-223">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-224">Les données du flux du côté de l’expéditeur sont reçues.</span><span class="sxs-lookup"><span data-stu-id="24473-224">Stream data on sender side is received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-225"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="24473-225"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-226">bit</span><span class="sxs-lookup"><span data-stu-id="24473-226">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="24473-227">1 signifie que le sens du flux provient de l’appelant vers l’appelant.</span><span class="sxs-lookup"><span data-stu-id="24473-227">1 means the stream direction is from the caller to the callee.</span></span></p>
<p><span data-ttu-id="24473-228">0 : le sens du flux provient de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="24473-228">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-229"><strong>JitterInterArrivalSD</strong></span><span class="sxs-lookup"><span data-stu-id="24473-229"><strong>JitterInterArrivalSD</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-230">float</span><span class="sxs-lookup"><span data-stu-id="24473-230">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-231">Écart type pour les heures d’arrivée de gigue.</span><span class="sxs-lookup"><span data-stu-id="24473-231">Standard deviation for jitter arrival times.</span></span></p>
<p><span data-ttu-id="24473-232">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-232">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-233"><strong>ConcealRatioMax</strong></span><span class="sxs-lookup"><span data-stu-id="24473-233"><strong>ConcealRatioMax</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-234">float</span><span class="sxs-lookup"><span data-stu-id="24473-234">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-235">Taux maximal de paquets masqués par la correction.</span><span class="sxs-lookup"><span data-stu-id="24473-235">Maximum ratio of packets concealed by the healer.</span></span></p>
<p><span data-ttu-id="24473-236">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-236">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-237"><strong>ConcealRatioSD</strong></span><span class="sxs-lookup"><span data-stu-id="24473-237"><strong>ConcealRatioSD</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-238">float</span><span class="sxs-lookup"><span data-stu-id="24473-238">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-239">Écart type pour le rapport de paquets masqués par la correction.</span><span class="sxs-lookup"><span data-stu-id="24473-239">Standard deviation for the ratio of packets concealed by the healer.</span></span></p>
<p><span data-ttu-id="24473-240">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-240">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-241"><strong>HealerPacketDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="24473-241"><strong>HealerPacketDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-242">float</span><span class="sxs-lookup"><span data-stu-id="24473-242">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-243">Taux de paquets rejetés par le taux de correction par rapport au nombre total de paquets reçus.</span><span class="sxs-lookup"><span data-stu-id="24473-243">Ratio of packets dropped by the healer compared to the total number of packets received.</span></span></p>
<p><span data-ttu-id="24473-244">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-244">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-245"><strong>HealerFECPacketUsedRatio</strong></span><span class="sxs-lookup"><span data-stu-id="24473-245"><strong>HealerFECPacketUsedRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-246">float</span><span class="sxs-lookup"><span data-stu-id="24473-246">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-247">Taux de paquets de correction d’erreur de transfert utilisés par rapport au nombre total de paquets reçus.</span><span class="sxs-lookup"><span data-stu-id="24473-247">Ratio of used forward error correction packets compared to the total number of packets received.</span></span></p>
<p><span data-ttu-id="24473-248">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-248">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-249"><strong>MaxCompressedSamples</strong></span><span class="sxs-lookup"><span data-stu-id="24473-249"><strong>MaxCompressedSamples</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-250">float</span><span class="sxs-lookup"><span data-stu-id="24473-250">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-251">Nombre maximal de paquets audio compressés par le cicatrisé.</span><span class="sxs-lookup"><span data-stu-id="24473-251">Maximum number of audio packets that were compressed by the healer.</span></span></p>
<p><span data-ttu-id="24473-252">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-252">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-253"><strong>LossCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="24473-253"><strong>LossCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-254">float</span><span class="sxs-lookup"><span data-stu-id="24473-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-255">Indique le pourcentage du temps pendant lequel l’appel a été dans un état de congestion de perte.</span><span class="sxs-lookup"><span data-stu-id="24473-255">Indicates the percentage of the time when the call was in a loss congestion state.</span></span></p>
<p><span data-ttu-id="24473-256">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-256">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-257"><strong>DelayCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="24473-257"><strong>DelayCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-258">float</span><span class="sxs-lookup"><span data-stu-id="24473-258">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-259">Indique le pourcentage de l’appel au cours duquel une congestion est causée par le retard de paquets réseau.</span><span class="sxs-lookup"><span data-stu-id="24473-259">Indicates the percentage of the call during which congestion was caused by the delayed arrival of network packets.</span></span></p>
<p><span data-ttu-id="24473-260">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-260">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-261"><strong>ContentionDetectedPercent</strong></span><span class="sxs-lookup"><span data-stu-id="24473-261"><strong>ContentionDetectedPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-262">float</span><span class="sxs-lookup"><span data-stu-id="24473-262">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-263">Indique le pourcentage de temps pendant lequel l’appel a été compétitif pour les ressources réseau.</span><span class="sxs-lookup"><span data-stu-id="24473-263">Indicates the percentage of the time when the call was competing for network resources.</span></span></p>
<p><span data-ttu-id="24473-264">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-264">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-265"><strong>BandwidthEstMin</strong></span><span class="sxs-lookup"><span data-stu-id="24473-265"><strong>BandwidthEstMin</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-266">int</span><span class="sxs-lookup"><span data-stu-id="24473-266">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-267">Quantité minimale d’estimation de la bande passante mesurée lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="24473-267">Minimum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="24473-268">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-268">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-269"><strong>BandwidthEstMax</strong></span><span class="sxs-lookup"><span data-stu-id="24473-269"><strong>BandwidthEstMax</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-270">int</span><span class="sxs-lookup"><span data-stu-id="24473-270">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-271">Quantité maximale d’estimation de la bande passante mesurée lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="24473-271">Maximum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="24473-272">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-272">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-273"><strong>BandwidthEstStdDev</strong></span><span class="sxs-lookup"><span data-stu-id="24473-273"><strong>BandwidthEstStdDev</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-274">int</span><span class="sxs-lookup"><span data-stu-id="24473-274">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-275">Écart type de l’estimation de la bande passante mesurée lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="24473-275">Standard deviation of the bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="24473-276">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-276">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-277"><strong>BandwidthEstAvge</strong></span><span class="sxs-lookup"><span data-stu-id="24473-277"><strong>BandwidthEstAvge</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-278">int</span><span class="sxs-lookup"><span data-stu-id="24473-278">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-279">Quantité moyenne d’estimation de bande passante mesurée lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="24473-279">Average amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="24473-280">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-280">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-281"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="24473-281"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-282">float</span><span class="sxs-lookup"><span data-stu-id="24473-282">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-283">Quantité totale de latence à sens unique.</span><span class="sxs-lookup"><span data-stu-id="24473-283">Total amount of one-way latency.</span></span> <span data-ttu-id="24473-284">Latence relative à sens unique, mesure du délai entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="24473-284">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="24473-285">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-285">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-286"><strong>Moyenne unidirectionnelle relative</strong></span><span class="sxs-lookup"><span data-stu-id="24473-286"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-287">float</span><span class="sxs-lookup"><span data-stu-id="24473-287">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-288">Quantité moyenne de latence à sens unique.</span><span class="sxs-lookup"><span data-stu-id="24473-288">Average amount of one-way latency.</span></span> <span data-ttu-id="24473-289">Latence relative à sens unique, mesure du délai entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="24473-289">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="24473-290">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-290">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-291"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="24473-291"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-292">float</span><span class="sxs-lookup"><span data-stu-id="24473-292">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-293">Quantité maximale de latence à sens unique.</span><span class="sxs-lookup"><span data-stu-id="24473-293">Maximum amount of one-way latency.</span></span> <span data-ttu-id="24473-294">Latence relative à sens unique, mesure du délai entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="24473-294">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="24473-295">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-295">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-296"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="24473-296"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-297">int</span><span class="sxs-lookup"><span data-stu-id="24473-297">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-298">Nombre total d’occurrences de rafales à sens unique.</span><span class="sxs-lookup"><span data-stu-id="24473-298">Total one-way burst occurrences.</span></span> <span data-ttu-id="24473-299">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendus plutôt qu’à un flux continu.</span><span class="sxs-lookup"><span data-stu-id="24473-299">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="24473-300">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="24473-300">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="24473-301">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-301">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-302"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="24473-302"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-303">float</span><span class="sxs-lookup"><span data-stu-id="24473-303">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-304">Densité du Burst total unidirectionnel.</span><span class="sxs-lookup"><span data-stu-id="24473-304">Total one-way burst density.</span></span> <span data-ttu-id="24473-305">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendus plutôt qu’à un flux continu.</span><span class="sxs-lookup"><span data-stu-id="24473-305">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="24473-306">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="24473-306">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="24473-307">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-307">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-308"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="24473-308"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-309">float</span><span class="sxs-lookup"><span data-stu-id="24473-309">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-310">Durée totale du Burst.</span><span class="sxs-lookup"><span data-stu-id="24473-310">Total one-way burst duration.</span></span> <span data-ttu-id="24473-311">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendus plutôt qu’à un flux continu.</span><span class="sxs-lookup"><span data-stu-id="24473-311">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="24473-312">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="24473-312">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="24473-313">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-313">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-314"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="24473-314"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-315">int</span><span class="sxs-lookup"><span data-stu-id="24473-315">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-316">Nombre total d’occurrences de l’espacement unidirectionnel.</span><span class="sxs-lookup"><span data-stu-id="24473-316">Total one-way gap occurrences.</span></span> <span data-ttu-id="24473-317">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendues au lieu d’un flux continu ; les intervalles indiquent les retards entre ces rafales.</span><span class="sxs-lookup"><span data-stu-id="24473-317">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="24473-318">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="24473-318">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="24473-319">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-319">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-320"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="24473-320"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-321">float</span><span class="sxs-lookup"><span data-stu-id="24473-321">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-322">Densité de l’intervalle total à sens unique.</span><span class="sxs-lookup"><span data-stu-id="24473-322">Total one-way gap density.</span></span> <span data-ttu-id="24473-323">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendues au lieu d’un flux continu ; les intervalles indiquent les retards entre ces rafales.</span><span class="sxs-lookup"><span data-stu-id="24473-323">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="24473-324">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="24473-324">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="24473-325">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-325">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-326"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="24473-326"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-327">float</span><span class="sxs-lookup"><span data-stu-id="24473-327">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-328">Durée totale de l’intervalle.</span><span class="sxs-lookup"><span data-stu-id="24473-328">Total one-way gap duration.</span></span> <span data-ttu-id="24473-329">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendues au lieu d’un flux continu ; les intervalles indiquent les retards entre ces rafales.</span><span class="sxs-lookup"><span data-stu-id="24473-329">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="24473-330">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="24473-330">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="24473-331">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-331">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-332"><strong>DecodeStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="24473-332"><strong>DecodeStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-333">float</span><span class="sxs-lookup"><span data-stu-id="24473-333">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-334">Pourcentage de l’appel décodé en stéréo.</span><span class="sxs-lookup"><span data-stu-id="24473-334">Percentage of the call decoded as stereo.</span></span></p>
<p><span data-ttu-id="24473-335">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-335">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-336"><strong>AecRenderStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="24473-336"><strong>AecRenderStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-337">float</span><span class="sxs-lookup"><span data-stu-id="24473-337">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-338">Pourcentage de l’appel rendu en stéréo par l’suppresseur d’écho acoustique.</span><span class="sxs-lookup"><span data-stu-id="24473-338">Percentage of the call rendered as stereo by the acoustic echo canceller.</span></span></p>
<p><span data-ttu-id="24473-339">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-339">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-340"><strong>AudioPostFECPLR</strong></span><span class="sxs-lookup"><span data-stu-id="24473-340"><strong>AudioPostFECPLR</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-341">float</span><span class="sxs-lookup"><span data-stu-id="24473-341">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-342">Taux de perte de paquets après application de la correction d’erreur de transfert.</span><span class="sxs-lookup"><span data-stu-id="24473-342">Packet loss rate after forward error correction has been applied.</span></span></p>
<p><span data-ttu-id="24473-343">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-343">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24473-344"><strong>EncodeStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="24473-344"><strong>EncodeStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-345">float</span><span class="sxs-lookup"><span data-stu-id="24473-345">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-346">Pourcentage de l’appel encodé en stéréo.</span><span class="sxs-lookup"><span data-stu-id="24473-346">Percentage of the call encoded as stereo.</span></span></p>
<p><span data-ttu-id="24473-347">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-347">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24473-348"><strong>AecCaptureStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="24473-348"><strong>AecCaptureStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="24473-349">float</span><span class="sxs-lookup"><span data-stu-id="24473-349">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="24473-350">Pourcentage de l’appel capturé comme stéréo par l’suppresseur d’écho acoustique.</span><span class="sxs-lookup"><span data-stu-id="24473-350">Percentage of the call captured as stereo by the acoustic echo canceller.</span></span></p>
<p><span data-ttu-id="24473-351">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24473-351">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="24473-352">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="24473-352">


</div>

<span> </span>

</div>

</div>

</span></span></div>

