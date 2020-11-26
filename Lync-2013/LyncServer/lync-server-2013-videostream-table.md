---
title: 'Lync Server 2013 : Table VideoStream'
description: 'Tableau Lync Server 2013 : VideoStream'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoStream table
ms:assetid: 4275ede7-5467-4a97-b8c8-a4b00917bf32
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425928(v=OCS.15)
ms:contentKeyID: 48184014
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d741478e1f6290685181bff471f143e41ce9ca1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444125"
---
# <a name="videostream-table-in-lync-server-2013"></a><span data-ttu-id="0ae79-103">Table VideoStream dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ae79-103">VideoStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0ae79-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0ae79-104">

<span> </span></span></span>

<span data-ttu-id="0ae79-105">_**Dernière modification de la rubrique :** 2013-12-13_</span><span class="sxs-lookup"><span data-stu-id="0ae79-105">_**Topic Last Modified:** 2013-12-13_</span></span>

<span data-ttu-id="0ae79-106">Chaque enregistrement représente un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="0ae79-106">Each record represents one video stream.</span></span> <span data-ttu-id="0ae79-107">Une ligne de média vidéo contient généralement deux flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="0ae79-107">One video media line usually contains two video streams.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ae79-108"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="0ae79-109"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="0ae79-110"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="0ae79-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="0ae79-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="0ae79-114">Principal</span><span class="sxs-lookup"><span data-stu-id="0ae79-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="0ae79-115">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="0ae79-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-117">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-117">int</span></span></p></td>
<td><p><span data-ttu-id="0ae79-118">Principal</span><span class="sxs-lookup"><span data-stu-id="0ae79-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="0ae79-119">R référencé à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="0ae79-119">R Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="0ae79-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="0ae79-122">Principal</span><span class="sxs-lookup"><span data-stu-id="0ae79-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="0ae79-123">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="0ae79-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-124"><strong>StreamID</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-124"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-125">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-125">int</span></span></p></td>
<td><p><span data-ttu-id="0ae79-126">Principal</span><span class="sxs-lookup"><span data-stu-id="0ae79-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="0ae79-127">IDENTIFIant unique dans une ligne de médias.</span><span class="sxs-lookup"><span data-stu-id="0ae79-127">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-128"><strong>VideoPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-128"><strong>VideoPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-129">type</span><span class="sxs-lookup"><span data-stu-id="0ae79-129">smallint</span></span></p></td>
<td><p><span data-ttu-id="0ae79-130">Étranger, primaire</span><span class="sxs-lookup"><span data-stu-id="0ae79-130">Foreign, Primary</span></span></p></td>
<td><p><span data-ttu-id="0ae79-131">Description de la charge utile.</span><span class="sxs-lookup"><span data-stu-id="0ae79-131">Payload description.</span></span> <span data-ttu-id="0ae79-132">Pour plus d’informations, voir la <a href="lync-server-2013-payloaddescription-table.md">table PayloadDescription dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ae79-132">See the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-133"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-133"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-134">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-134">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-135">Gigue réseau moyenne des statistiques de protocole RTCP (Real Time Control Protocol).</span><span class="sxs-lookup"><span data-stu-id="0ae79-135">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-136"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-136"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-137">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-137">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-138">Scintillement du réseau maximum lors de la session vidéo.</span><span class="sxs-lookup"><span data-stu-id="0ae79-138">Maximum network jitter during the video session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-139"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-139"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-140">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-140">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-141">Durée de l’aller-retour des statistiques RTCP.</span><span class="sxs-lookup"><span data-stu-id="0ae79-141">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-142"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-142"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-143">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-143">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-144">Durée de l’aller-retour maximal pour le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="0ae79-144">Maximum round trip time for the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-145"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-145"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-146">décimale (5 ; 4)</span><span class="sxs-lookup"><span data-stu-id="0ae79-146">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-147">Taux moyen de perte de paquets lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="0ae79-147">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-148"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-148"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-149">décimale (5 ; 4)</span><span class="sxs-lookup"><span data-stu-id="0ae79-149">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-150">Perte de paquets maximum observée pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="0ae79-150">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-151"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-151"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-152">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-152">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-153">Nombre de paquets pour le flux vidéo (Real Time Transport Protocol, RTP).</span><span class="sxs-lookup"><span data-stu-id="0ae79-153">Packet count for the video stream (Real Time Transport Protocol, RTP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-154"><strong>Bande passante</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-154"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-155">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-155">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-156">Estimations de bande passante pour le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="0ae79-156">Bandwidth estimates for the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-157"><strong>VideoResolution</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-157"><strong>VideoResolution</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-158">car (9)</span><span class="sxs-lookup"><span data-stu-id="0ae79-158">char(9)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-159">Résolution de la vidéo, en pixels, de largeur multipliée par la hauteur en pixels.</span><span class="sxs-lookup"><span data-stu-id="0ae79-159">Resolution of the video in pixels width multiplied by pixels height.</span></span> <span data-ttu-id="0ae79-160">Signalée en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="0ae79-160">Reported as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-161"><strong>VideoBitRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-161"><strong>VideoBitRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-162">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-162">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-163">Vitesse de transmission moyenne du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="0ae79-163">Average bit rate of the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-164"><strong>InboundVideoFrameRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-164"><strong>InboundVideoFrameRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-165">décimale (9 ; 4)</span><span class="sxs-lookup"><span data-stu-id="0ae79-165">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-166">Fréquence d’images vidéo reçues.</span><span class="sxs-lookup"><span data-stu-id="0ae79-166">The video frame rate received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-167"><strong>OutboundVideoFrameRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-167"><strong>OutboundVideoFrameRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-168">décimale (9 ; 4)</span><span class="sxs-lookup"><span data-stu-id="0ae79-168">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-169">Fréquence d’images vidéo envoyées.</span><span class="sxs-lookup"><span data-stu-id="0ae79-169">The video frame rate sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-170"><strong>VideoBitRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-170"><strong>VideoBitRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-171">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-171">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-172">Débit vidéo maximum lors de la session vidéo.</span><span class="sxs-lookup"><span data-stu-id="0ae79-172">The maximum video bit rate during the video session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-173"><strong>VideoFrameLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-173"><strong>VideoFrameLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-174">décimale (9 ; 4)</span><span class="sxs-lookup"><span data-stu-id="0ae79-174">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-175">Pourcentage du nombre total de trames vidéo perdues.</span><span class="sxs-lookup"><span data-stu-id="0ae79-175">The percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-176"><strong>VideoFEC</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-176"><strong>VideoFEC</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-177">bit</span><span class="sxs-lookup"><span data-stu-id="0ae79-177">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-178">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="0ae79-178">Not available.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-179"><strong>VideoLocalFrameLossPercentageAvg</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-179"><strong>VideoLocalFrameLossPercentageAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-180">décimale (9 ; 4)</span><span class="sxs-lookup"><span data-stu-id="0ae79-180">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-181">Pourcentage du nombre total de trames vidéo perdues.</span><span class="sxs-lookup"><span data-stu-id="0ae79-181">The percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-182"><strong>CIFQualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-182"><strong>CIFQualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-183">tinyint</span><span class="sxs-lookup"><span data-stu-id="0ae79-183">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-184">Pourcentage de l’appel à la résolution CAF (Common Interchange Format).</span><span class="sxs-lookup"><span data-stu-id="0ae79-184">The percentage of the call that was at the Common Interchange Format (CIF) resolution.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-185"><strong>VGAQualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-185"><strong>VGAQualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-186">tinyint</span><span class="sxs-lookup"><span data-stu-id="0ae79-186">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-187">Pourcentage de l’appel à la résolution VGA.</span><span class="sxs-lookup"><span data-stu-id="0ae79-187">The percentage of the call that was at VGA resolution.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-188"><strong>HD720QualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-188"><strong>HD720QualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-189">tinyint</span><span class="sxs-lookup"><span data-stu-id="0ae79-189">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-190">Pourcentage de l’appel passé à la résolution HD720.</span><span class="sxs-lookup"><span data-stu-id="0ae79-190">The percentage of the call that was at HD720 resolution.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-191"><strong>NoneDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-191"><strong>NoneDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-192">tinyint</span><span class="sxs-lookup"><span data-stu-id="0ae79-192">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-193">Pourcentage de la durée de l’appel sans cadre.</span><span class="sxs-lookup"><span data-stu-id="0ae79-193">Percentage of call duration with no frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-194"><strong>BDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-194"><strong>BDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-195">tinyint</span><span class="sxs-lookup"><span data-stu-id="0ae79-195">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-196">Pourcentage de la durée de l’appel avec la dépose de l’image B.</span><span class="sxs-lookup"><span data-stu-id="0ae79-196">Percentage of call duration with B frame drop.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-197"><strong>BPDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-197"><strong>BPDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-198">tinyint</span><span class="sxs-lookup"><span data-stu-id="0ae79-198">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-199">Pourcentage de la durée de l’appel avec la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="0ae79-199">Percentage of call duration with BP frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-200"><strong>BPSPDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-200"><strong>BPSPDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-201">tinyint</span><span class="sxs-lookup"><span data-stu-id="0ae79-201">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-202">Pourcentage de la durée de l’appel avec BPSP Frame.</span><span class="sxs-lookup"><span data-stu-id="0ae79-202">Percentage of call duration with BPSP frame drop.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-203"><strong>BPSPIDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-203"><strong>BPSPIDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-204">tinyint</span><span class="sxs-lookup"><span data-stu-id="0ae79-204">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-205">Pourcentage de la durée de l’appel avec BPSPI Frame.</span><span class="sxs-lookup"><span data-stu-id="0ae79-205">Percentage of call duration with BPSPI frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-206"><strong>Entrant</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-206"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-207">bit</span><span class="sxs-lookup"><span data-stu-id="0ae79-207">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-208">Des données de flux sur le côté du destinataire sont reçues.</span><span class="sxs-lookup"><span data-stu-id="0ae79-208">Stream data on receiver side is received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-209"><strong>Sortant</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-209"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-210">bit</span><span class="sxs-lookup"><span data-stu-id="0ae79-210">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-211">Les données du flux du côté de l’expéditeur sont reçues.</span><span class="sxs-lookup"><span data-stu-id="0ae79-211">Stream data on sender side is received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-212"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-212"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-213">bit</span><span class="sxs-lookup"><span data-stu-id="0ae79-213">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0ae79-214">1 signifie que le sens du flux provient de l’appelant vers l’appel.</span><span class="sxs-lookup"><span data-stu-id="0ae79-214">1 means the stream direction is from the caller to callee.</span></span></p>
<p><span data-ttu-id="0ae79-215">0 : le sens du flux provient de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="0ae79-215">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-216"><strong>LossCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-216"><strong>LossCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-217">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-217">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-218">Indique le pourcentage du temps pendant lequel l’appel a été dans un état de congestion de perte.</span><span class="sxs-lookup"><span data-stu-id="0ae79-218">Indicates the percentage of the time when the call was in a loss congestion state.</span></span></p>
<p><span data-ttu-id="0ae79-219">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-219">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-220"><strong>DelayCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-220"><strong>DelayCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-221">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-221">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-222">Indique le pourcentage de l’appel au cours duquel une congestion est causée par le retard de paquets réseau.</span><span class="sxs-lookup"><span data-stu-id="0ae79-222">Indicates the percentage of the call during which congestion was caused by the delayed arrival of network packets.</span></span></p>
<p><span data-ttu-id="0ae79-223">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-223">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-224"><strong>ContentionDetectedPercent</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-224"><strong>ContentionDetectedPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-225">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-225">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-226">Indique le pourcentage de temps pendant lequel l’appel a été compétitif pour les ressources réseau.</span><span class="sxs-lookup"><span data-stu-id="0ae79-226">Indicates the percentage of the time when the call was competing for network resources.</span></span></p>
<p><span data-ttu-id="0ae79-227">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-227">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-228"><strong>BandwidthEstMin</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-228"><strong>BandwidthEstMin</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-229">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-229">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-230">Quantité minimale d’estimation de la bande passante mesurée lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="0ae79-230">Minimum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="0ae79-231">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-231">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-232"><strong>BandwidthEstMax</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-232"><strong>BandwidthEstMax</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-233">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-233">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-234">Quantité maximale d’estimation de la bande passante mesurée lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="0ae79-234">Maximum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="0ae79-235">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-235">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-236"><strong>BandwidthEstStdDev</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-236"><strong>BandwidthEstStdDev</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-237">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-237">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-238">Écart type de l’estimation de la bande passante mesurée lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="0ae79-238">Standard deviation of the bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="0ae79-239">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-239">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-240"><strong>BandwidthEstAvge</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-240"><strong>BandwidthEstAvge</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-241">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-241">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-242">Quantité moyenne d’estimation de bande passante mesurée lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="0ae79-242">Average amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="0ae79-243">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-243">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-244"><strong>LowBandwidthForMultiview</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-244"><strong>LowBandwidthForMultiview</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-245">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-245">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-246">Pourcentage de l’appel où le point de terminaison a déterminé que la connexion réseau n’a pas pu prendre en charge la vidéo multivue.</span><span class="sxs-lookup"><span data-stu-id="0ae79-246">Percentage of the call where the endpoint determined that the network connection could not support multiview video.</span></span></p>
<p><span data-ttu-id="0ae79-247">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-247">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-248"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-248"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-249">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-249">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-250">Quantité totale de latence à sens unique.</span><span class="sxs-lookup"><span data-stu-id="0ae79-250">Total amount of one-way latency.</span></span> <span data-ttu-id="0ae79-251">Latence relative à sens unique, mesure du délai entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="0ae79-251">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="0ae79-252">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-252">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-253"><strong>Moyenne unidirectionnelle relative</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-253"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-254">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-255">Quantité moyenne de latence à sens unique.</span><span class="sxs-lookup"><span data-stu-id="0ae79-255">Average amount of one-way latency.</span></span> <span data-ttu-id="0ae79-256">Latence relative à sens unique, mesure du délai entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="0ae79-256">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="0ae79-257">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-257">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-258"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-258"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-259">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-259">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-260">Quantité maximale de latence à sens unique.</span><span class="sxs-lookup"><span data-stu-id="0ae79-260">Maximum amount of one-way latency.</span></span> <span data-ttu-id="0ae79-261">Latence relative à sens unique, mesure du délai entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="0ae79-261">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="0ae79-262">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-262">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-263"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-263"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-264">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-264">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-265">Nombre total d’occurrences de rafales à sens unique.</span><span class="sxs-lookup"><span data-stu-id="0ae79-265">Total one-way burst occurrences.</span></span> <span data-ttu-id="0ae79-266">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendus plutôt qu’à un flux continu.</span><span class="sxs-lookup"><span data-stu-id="0ae79-266">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="0ae79-267">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="0ae79-267">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="0ae79-268">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-268">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-269"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-269"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-270">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-270">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-271">Densité du Burst total unidirectionnel.</span><span class="sxs-lookup"><span data-stu-id="0ae79-271">Total one-way burst density.</span></span> <span data-ttu-id="0ae79-272">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendus plutôt qu’à un flux continu.</span><span class="sxs-lookup"><span data-stu-id="0ae79-272">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="0ae79-273">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="0ae79-273">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="0ae79-274">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-274">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-275"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-275"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-276">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-276">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-277">Durée totale du Burst.</span><span class="sxs-lookup"><span data-stu-id="0ae79-277">Total one-way burst duration.</span></span> <span data-ttu-id="0ae79-278">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendus plutôt qu’à un flux continu.</span><span class="sxs-lookup"><span data-stu-id="0ae79-278">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="0ae79-279">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="0ae79-279">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="0ae79-280">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-280">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-281"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-281"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-282">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-282">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-283">Nombre total d’occurrences de l’espacement unidirectionnel.</span><span class="sxs-lookup"><span data-stu-id="0ae79-283">Total one-way gap occurrences.</span></span> <span data-ttu-id="0ae79-284">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendues au lieu d’un flux continu ; les intervalles indiquent les retards entre ces rafales.</span><span class="sxs-lookup"><span data-stu-id="0ae79-284">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="0ae79-285">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="0ae79-285">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="0ae79-286">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-286">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-287"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-287"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-288">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-288">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-289">Densité de l’intervalle total à sens unique.</span><span class="sxs-lookup"><span data-stu-id="0ae79-289">Total one-way gap density.</span></span> <span data-ttu-id="0ae79-290">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendues au lieu d’un flux continu ; les intervalles indiquent les retards entre ces rafales.</span><span class="sxs-lookup"><span data-stu-id="0ae79-290">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="0ae79-291">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="0ae79-291">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="0ae79-292">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-292">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-293"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-293"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-294">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-294">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-295">Durée totale de l’intervalle.</span><span class="sxs-lookup"><span data-stu-id="0ae79-295">Total one-way gap duration.</span></span> <span data-ttu-id="0ae79-296">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendues au lieu d’un flux continu ; les intervalles indiquent les retards entre ces rafales.</span><span class="sxs-lookup"><span data-stu-id="0ae79-296">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="0ae79-297">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="0ae79-297">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="0ae79-298">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-298">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-299"><strong>Cause du taux</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-299"><strong>VideoPacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-300">décimale (9 ; 4)</span><span class="sxs-lookup"><span data-stu-id="0ae79-300">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-301">Taux d’interruption des paquets vidéo.</span><span class="sxs-lookup"><span data-stu-id="0ae79-301">Rate at which video packets were lost.</span></span></p>
<p><span data-ttu-id="0ae79-302">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-302">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-303"><strong>VideoAllocateBWAvg</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-303"><strong>VideoAllocateBWAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-304">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-304">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-305">Quantité moyenne de bande passante allouée pour la vidéo.</span><span class="sxs-lookup"><span data-stu-id="0ae79-305">Average amount of bandwidth allocated for video.</span></span></p>
<p><span data-ttu-id="0ae79-306">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-306">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-307"><strong>SendCodecTypes</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-307"><strong>SendCodecTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-308">type</span><span class="sxs-lookup"><span data-stu-id="0ae79-308">smallint</span></span></p></td>
<td><p><span data-ttu-id="0ae79-309">Externes</span><span class="sxs-lookup"><span data-stu-id="0ae79-309">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ae79-310">Type de codecs vidéo utilisés par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="0ae79-310">Type of video codecs used by the sender.</span></span> <span data-ttu-id="0ae79-311">Pour plus d’informations, voir la <a href="lync-server-2013-codecdescription-table.md">table CodecDescription dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ae79-311">See the <a href="lync-server-2013-codecdescription-table.md">CodecDescription table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="0ae79-312">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-312">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-313"><strong>SendResolutionWidth</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-313"><strong>SendResolutionWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-314">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-314">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-315">Largeur de résolution utilisée par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="0ae79-315">Resolution width used by the sender.</span></span></p>
<p><span data-ttu-id="0ae79-316">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-316">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-317"><strong>SendResolutionHeight</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-317"><strong>SendResolutionHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-318">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-318">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-319">Hauteur de résolution utilisée par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="0ae79-319">Resolution height used by the sender.</span></span></p>
<p><span data-ttu-id="0ae79-320">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-320">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-321"><strong>SendFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-321"><strong>SendFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-322">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-322">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-323">Transmission moyenne de la fréquence d’images vidéo utilisée par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="0ae79-323">Average video frame rate transmission used by the sender.</span></span></p>
<p><span data-ttu-id="0ae79-324">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-324">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-325"><strong>SendBitRateMaximum</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-325"><strong>SendBitRateMaximum</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-326">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-326">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-327">Taux de bits maximal pour l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="0ae79-327">Maximum bit rate for the sender.</span></span></p>
<p><span data-ttu-id="0ae79-328">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-328">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-329"><strong>SendBitRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-329"><strong>SendBitRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-330">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-330">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-331">Taux de bits moyen pour l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="0ae79-331">Average bit rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-332"><strong>SendVideoStreamsMax</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-332"><strong>SendVideoStreamsMax</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-333">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-333">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-334">Nombre maximal de flux vidéo utilisés par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="0ae79-334">Maximum number of video streams used by the sender.</span></span></p>
<p><span data-ttu-id="0ae79-335">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-335">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-336"><strong>RecvCodecTypes</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-336"><strong>RecvCodecTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-337">type</span><span class="sxs-lookup"><span data-stu-id="0ae79-337">smallint</span></span></p></td>
<td><p><span data-ttu-id="0ae79-338">Externes</span><span class="sxs-lookup"><span data-stu-id="0ae79-338">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ae79-339">Codes vidéo utilisés par le destinataire.</span><span class="sxs-lookup"><span data-stu-id="0ae79-339">Video codes used by the receiver.</span></span> <span data-ttu-id="0ae79-340">Pour plus d’informations, voir la <a href="lync-server-2013-codecdescription-table.md">table CodecDescription dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ae79-340">See the <a href="lync-server-2013-codecdescription-table.md">CodecDescription table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="0ae79-341">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-341">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-342"><strong>RecvResolutionWidth</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-342"><strong>RecvResolutionWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-343">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-343">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-344">Largeur de résolution utilisée par le destinataire.</span><span class="sxs-lookup"><span data-stu-id="0ae79-344">Resolution width used by the receiver.</span></span></p>
<p><span data-ttu-id="0ae79-345">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-345">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-346"><strong>RecvResolutionHeight</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-346"><strong>RecvResolutionHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-347">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-347">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-348">Hauteur de résolution utilisée par le destinataire.</span><span class="sxs-lookup"><span data-stu-id="0ae79-348">Resolution height used by the receiver.</span></span></p>
<p><span data-ttu-id="0ae79-349">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-349">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-350"><strong>Cause reçues</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-350"><strong>RecvFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-351">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-351">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-352">Fréquence d’images vidéo moyenne utilisée par le destinataire.</span><span class="sxs-lookup"><span data-stu-id="0ae79-352">Average video frame rate used by the receiver.</span></span></p>
<p><span data-ttu-id="0ae79-353">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-353">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-354"><strong>RecvBitRateMaximum</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-354"><strong>RecvBitRateMaximum</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-355">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-355">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-356">Vitesse de transmission maximale du destinataire.</span><span class="sxs-lookup"><span data-stu-id="0ae79-356">Maximum bit rate for the receiver.</span></span></p>
<p><span data-ttu-id="0ae79-357">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-357">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-358"><strong>RecvBitRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-358"><strong>RecvBitRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-359">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-359">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-360">Taux de bits moyen pour le destinataire.</span><span class="sxs-lookup"><span data-stu-id="0ae79-360">Average bit rate for the receiver.</span></span></p>
<p><span data-ttu-id="0ae79-361">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-361">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-362"><strong>RecvVideoStreamsMax</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-362"><strong>RecvVideoStreamsMax</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-363">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-363">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-364">Flux vidéo maximal pour le destinataire.</span><span class="sxs-lookup"><span data-stu-id="0ae79-364">Maximum video streams for the receiver.</span></span></p>
<p><span data-ttu-id="0ae79-365">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-365">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-366"><strong>RecvVideoStreamsMin</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-366"><strong>RecvVideoStreamsMin</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-367">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-367">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-368">Flux vidéo minimal pour le destinataire.</span><span class="sxs-lookup"><span data-stu-id="0ae79-368">Minimum video streams for the receiver.</span></span></p>
<p><span data-ttu-id="0ae79-369">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-369">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-370"><strong>RecvVideoStreamsMode</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-370"><strong>RecvVideoStreamsMode</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-371">int</span><span class="sxs-lookup"><span data-stu-id="0ae79-371">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-372">Mode vidéo (par exemple, Galerie ou flux unique) pour le destinataire.</span><span class="sxs-lookup"><span data-stu-id="0ae79-372">Video mode (for example, gallery or single stream) for the receiver.</span></span></p>
<p><span data-ttu-id="0ae79-373">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-373">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-374"><strong>VideoPostFECPLR</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-374"><strong>VideoPostFECPLR</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-375">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-375">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-376">Taux de perte de paquets après application de la correction d’erreur de transfert.</span><span class="sxs-lookup"><span data-stu-id="0ae79-376">Packet loss rate after forward error correction has been applied.</span></span></p>
<p><span data-ttu-id="0ae79-377">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-377">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-378"><strong>Cause du pourcentage</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-378"><strong>DynamicCapabilityPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-379">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-379">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-380">Pourcentage de temps pendant lequel l’indicateur de capacité dynamique a été actif.</span><span class="sxs-lookup"><span data-stu-id="0ae79-380">Percentage of time that the dynamic capability flag was active.</span></span></p>
<p><span data-ttu-id="0ae79-381">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-381">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-382"><strong>ResolutionMin</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-382"><strong>ResolutionMin</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-383">car (9)</span><span class="sxs-lookup"><span data-stu-id="0ae79-383">char(9)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-384">Résolution minimale mesurée lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="0ae79-384">Minimum resolution measured during the call.</span></span></p>
<p><span data-ttu-id="0ae79-385">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-385">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-386"><strong>LowBitRateCallPercent</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-386"><strong>LowBitRateCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-387">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-387">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-388">Pourcentage de l’appel inférieur au seuil de faible taux de bits (70 kilobits par seconde).</span><span class="sxs-lookup"><span data-stu-id="0ae79-388">Percentage of the call below the low bit rate threshold (70 kilobits per second).</span></span></p>
<p><span data-ttu-id="0ae79-389">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-389">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-390"><strong>Cause du pourcentage</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-390"><strong>LowFrameRateCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-391">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-391">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-392">Pourcentage de l’appel inférieur au seuil de fréquence d’images faible (7,5 images par seconde, entrant).</span><span class="sxs-lookup"><span data-stu-id="0ae79-392">Percentage of the call below the low frame rate threshold (7.5 frames per second, inbound).</span></span></p>
<p><span data-ttu-id="0ae79-393">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-393">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-394"><strong>Cause du pourcentage</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-394"><strong>LowResolutionCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-395">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-395">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-396">Pourcentage de l’appel qui s’est produit à la résolution la plus basse.</span><span class="sxs-lookup"><span data-stu-id="0ae79-396">Percentage of the call that occurred at the lowest resolution.</span></span></p>
<p><span data-ttu-id="0ae79-397">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-397">This column was introduced in Microsoft Lync Server 2013.</span></span></p>
<p><span data-ttu-id="0ae79-398">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-398">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae79-399"><strong>DurationSeconds</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-399"><strong>DurationSeconds</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-400">float</span><span class="sxs-lookup"><span data-stu-id="0ae79-400">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-401">Durée de l’appel en secondes.</span><span class="sxs-lookup"><span data-stu-id="0ae79-401">Length of the call in seconds.</span></span></p>
<p><span data-ttu-id="0ae79-402">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-402">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae79-403"><strong>IsAggregatedData</strong></span><span class="sxs-lookup"><span data-stu-id="0ae79-403"><strong>IsAggregatedData</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae79-404">bit</span><span class="sxs-lookup"><span data-stu-id="0ae79-404">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ae79-405">Indique si les données ont été agrégées à partir de plusieurs appels.</span><span class="sxs-lookup"><span data-stu-id="0ae79-405">Indicates whether the data has been aggregated from multiple calls.</span></span></p>
<p><span data-ttu-id="0ae79-406">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae79-406">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0ae79-407">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0ae79-407">


</div>

<span> </span>

</div>

</div>

</span></span></div>

