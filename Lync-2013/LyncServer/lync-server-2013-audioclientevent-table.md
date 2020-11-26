---
title: 'Lync Server 2013 : Table AudioClientEvent'
description: 'Tableau Lync Server 2013 : AudioClientEvent'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioClientEvent table
ms:assetid: fef73d8f-7261-4e5b-9769-82435b007979
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413086(v=OCS.15)
ms:contentKeyID: 48185967
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2200cd9567bdd10ac4ad8f5c269062c2f5614dcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438209"
---
# <a name="audioclientevent-table-in-lync-server-2013"></a><span data-ttu-id="1ad2d-103">Table AudioClientEvent dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1ad2d-103">AudioClientEvent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1ad2d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1ad2d-104">

<span> </span></span></span>

<span data-ttu-id="1ad2d-105">_**Dernière modification de la rubrique :** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="1ad2d-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="1ad2d-106">Chaque enregistrement contient un événement client pour un point de terminaison dans un appel audio.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-106">Each record contains a client event for one endpoint in an audio call.</span></span> <span data-ttu-id="1ad2d-107">En règle générale, un appel possède deux enregistrements, un pour l’appelant et un pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-107">Usually, one call has two records, one for caller and one for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1ad2d-108"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="1ad2d-109"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="1ad2d-110"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="1ad2d-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ad2d-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="1ad2d-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="1ad2d-114">Principal</span><span class="sxs-lookup"><span data-stu-id="1ad2d-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="1ad2d-115">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ad2d-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-117">int</span><span class="sxs-lookup"><span data-stu-id="1ad2d-117">int</span></span></p></td>
<td><p><span data-ttu-id="1ad2d-118">Principal</span><span class="sxs-lookup"><span data-stu-id="1ad2d-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="1ad2d-119">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ad2d-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="1ad2d-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="1ad2d-122">Principal</span><span class="sxs-lookup"><span data-stu-id="1ad2d-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="1ad2d-123">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ad2d-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-125">bit</span><span class="sxs-lookup"><span data-stu-id="1ad2d-125">bit</span></span></p></td>
<td><p><span data-ttu-id="1ad2d-126">Principal</span><span class="sxs-lookup"><span data-stu-id="1ad2d-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="1ad2d-127">0 : données du destinataire</span><span class="sxs-lookup"><span data-stu-id="1ad2d-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="1ad2d-128">1 : données de l’appelant</span><span class="sxs-lookup"><span data-stu-id="1ad2d-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ad2d-129"><strong>NetworkSendQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-129"><strong>NetworkSendQualityEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-130">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="1ad2d-130">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1ad2d-131">Pourcentage de session de déclenchement de l’événement NetworkSendQuality pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-131">Percentage of session the NetworkSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="1ad2d-132">La qualité du réseau en termes de gigue ou de perte de paquets est sévère et a un impact sur la qualité du son envoyé.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-132">Network quality in terms of jitter or packet loss is severe and impacting the quality of audio being sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ad2d-133"><strong>NetworkReceiveQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-133"><strong>NetworkReceiveQualityEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-134">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="1ad2d-134">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1ad2d-135">Pourcentage de session de déclenchement de l’événement ReceiveSendQuality pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-135">Percentage of session the ReceiveSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="1ad2d-136">La qualité du réseau en termes de gigue ou de perte de paquets est sérieuse et a un impact sur la qualité du son reçu.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-136">Network quality in terms of jitter or packet loss is severe and impacting the quality of audio being received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ad2d-137"><strong>NetworkDelayEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-137"><strong>NetworkDelayEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-138">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="1ad2d-138">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1ad2d-139">Pourcentage de session le déclenchement de l’événement de temporisation a été déclenché pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-139">Percentage of session the Delay event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="1ad2d-140">La latence du réseau est sérieuse et a un impact sur l’interface en empêchant les communications interactives</span><span class="sxs-lookup"><span data-stu-id="1ad2d-140">Network latency is severe and impacting the experience by preventing interactive communication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ad2d-141"><strong>NetworkBandwidthLowEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-141"><strong>NetworkBandwidthLowEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-142">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="1ad2d-142">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1ad2d-143">Pourcentage de session de déclenchement de l’événement LowBandwidth pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-143">Percentage of session the LowBandwidth event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="1ad2d-144">La bande passante disponible est insuffisante pour obtenir une utilisation vocale acceptable.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-144">The available bandwidth is insufficient for an acceptable voice experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ad2d-145"><strong>CPUInsufficientEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-145"><strong>CPUInsufficientEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-146">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="1ad2d-146">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1ad2d-147">Pourcentage de session de l’événement UC insuffisant déclenché pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-147">Percentage of session the insufficient CPU event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="1ad2d-148">Il n’y a pas assez de cycles d’UC pour le traitement avec les modalités et applications en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-148">There are insufficient CPU cycles for processing with the current modalities and applications in use.</span></span> <span data-ttu-id="1ad2d-149">Cela entraîne une distorsion du canal audio.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-149">This causes distortions with the audio channel.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ad2d-150"><strong>DeviceHalfDuplexAECEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-150"><strong>DeviceHalfDuplexAECEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-151">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="1ad2d-151">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1ad2d-152">Pourcentage de session de déclenchement de l’événement DeviceHalfDuplexAEC pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-152">Percentage of session the DeviceHalfDuplexAEC event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="1ad2d-153">Afin d’éviter l’écho, le système a entré Half duplex.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-153">In order to prevent echo, the system has enter half duplex.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ad2d-154"><strong>DeviceRenderNotFunctioningEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-154"><strong>DeviceRenderNotFunctioningEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-155">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="1ad2d-155">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1ad2d-156">Pourcentage de session de déclenchement de l’événement DeviceRenderNotFunctioning pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-156">Percentage of session the DeviceRenderNotFunctioning event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="1ad2d-157">L’appareil de rendu actuellement utilisé pour la session ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-157">The render device currently being used for the session is not functioning correctly.</span></span> <span data-ttu-id="1ad2d-158">Cela peut entraîner des problèmes audio à sens unique.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-158">This can cause one-way audio issues.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ad2d-159"><strong>DeviceCaptureNotFunctioningEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-159"><strong>DeviceCaptureNotFunctioningEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-160">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="1ad2d-160">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1ad2d-161">Pourcentage de session de déclenchement de l’événement DeviceCaptureNotFunctioning pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-161">Percentage of session the DeviceCaptureNotFunctioning event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="1ad2d-162">L’appareil de capture actuellement utilisé pour la session ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-162">The capture device currently being used for the session is not functioning correctly.</span></span> <span data-ttu-id="1ad2d-163">Cela peut entraîner des problèmes audio à sens unique.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-163">This can cause one-way audio issues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ad2d-164"><strong>DeviceGlitchesEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-164"><strong>DeviceGlitchesEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-165">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="1ad2d-165">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1ad2d-166">Pourcentage de session de déclenchement de l’événement DeviceGlitches pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-166">Percentage of session the DeviceGlitches event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="1ad2d-167">Il y a des problèmes importants dans le rendu du son qui engendre des distorsions.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-167">There are severe glitches in the rendering of audio which is causing distortions.</span></span> <span data-ttu-id="1ad2d-168">Ces problèmes peuvent être causés par des problèmes de pilotes, des appels de procédures différées (DPC) Storm (pilotes) et une utilisation élevée de l’UC.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-168">These glitches can be caused by driver issues, deferred procedure calls (DPC) storm (drivers), and high CPU usage.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ad2d-169"><strong>DeviceLowSNREventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-169"><strong>DeviceLowSNREventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-170">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="1ad2d-170">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1ad2d-171">Pourcentage de session de déclenchement de l’événement DeviceLowSNR pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-171">Percentage of session the DeviceLowSNR event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="1ad2d-172">La qualité de la capture est très médiocre, qu’elle soit très bruyante ou que l’utilisateur parle trop loin du microphone.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-172">The capture quality is very poor, either very noisy or user is talking too far away from the microphone.</span></span> <span data-ttu-id="1ad2d-173">Cela entraînera une distorsion.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-173">This will cause distortions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ad2d-174"><strong>DeviceLowSpeechLevelEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-174"><strong>DeviceLowSpeechLevelEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-175">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="1ad2d-175">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1ad2d-176">Pourcentage de session de déclenchement de l’événement DeviceLowSpeechLevel pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-176">Percentage of session the DeviceLowSpeechLevel event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="1ad2d-177">Le niveau de voix de l’utilisateur est trop faible et le système ne peut plus l’augmenter.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-177">User‘s speech level is too low and the system cannot increase it any further.</span></span> <span data-ttu-id="1ad2d-178">Cela peut entraîner des distorsions ou une perception perçue comme un son à sens unique.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-178">This can either cause distortions or perceived as one-way audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ad2d-179"><strong>DeviceClippingEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-179"><strong>DeviceClippingEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-180">Décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="1ad2d-180">Decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1ad2d-181">Pourcentage de session de déclenchement de l’événement DeviceClipping pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-181">Percentage of session the DeviceClipping event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="1ad2d-182">Lorsque le son du microphone est proche de l’extrémité de la parole, la distorsion est audible en raison de l’écrêtage.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-182">When near-end speech clips the microphone, far-end hears distortion due to clipping.</span></span> <span data-ttu-id="1ad2d-183">Il est important d’éviter une capture du microphone proche de la fin.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-183">It is important to avoid near-end microphone clipping.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ad2d-184"><strong>DeviceEchoEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-184"><strong>DeviceEchoEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-185">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="1ad2d-185">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1ad2d-186">Pourcentage de session de déclenchement de l’événement DeviceEchoEvent pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-186">Percentage of session the DeviceEchoEvent event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="1ad2d-187">L’appareil ou la configuration entraîne un écho au-delà de la capacité du système à compenser.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-187">Device or setup is causing echo beyond the ability of the system to compensate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ad2d-188"><strong>DeviceNearEndToEchoRatioEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-188"><strong>DeviceNearEndToEchoRatioEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-189">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="1ad2d-189">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1ad2d-190">Pourcentage de session de déclenchement de l’événement DeviceNearEndToEchoRatio pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-190">Percentage of session the DeviceNearEndToEchoRatio event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="1ad2d-191">La parole de l’utilisateur est trop faible par rapport à l’écho capturé qui a un impact sur l’interface utilisateur, car il limite le niveau d’interruption d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-191">The user’s speech is too low compared to the echo being captured which impacts the users experience because it limits how easy it is to interrupt a user.</span></span> <span data-ttu-id="1ad2d-192">Réduire le volume des haut-parleurs, rapprochez le micro du contact.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-192">Reduce speaker volume, move the microphone closer to the talker.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ad2d-193"><strong>DeviceMultipleEndpointsEventCount</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-193"><strong>DeviceMultipleEndpointsEventCount</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-194">int</span><span class="sxs-lookup"><span data-stu-id="1ad2d-194">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1ad2d-195">Nombre de fois que l’événement DeviceMultipleEndpoints a été déclenché pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-195">Number of times during session the DeviceMultipleEndpoints event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="1ad2d-196">Plusieurs points de terminaison audio au sein de la même session détectés et le système a compensé en réduisant le volume de rendu.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-196">Multiple audio endpoints in the same session detected and the system has compensated by reducing render volume.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ad2d-197"><strong>DeviceHowlingEventCount</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-197"><strong>DeviceHowlingEventCount</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-198">int</span><span class="sxs-lookup"><span data-stu-id="1ad2d-198">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1ad2d-199">Nombre de fois que l’événement DeviceHowlingEvent a été déclenché pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-199">Number of times during session the DeviceHowlingEvent event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="1ad2d-200">Boucle de commentaires audio détectée (provoquée par plusieurs points de terminaison partageant le chemin audio).</span><span class="sxs-lookup"><span data-stu-id="1ad2d-200">Audio feedback loop detected (caused by multiple endpoints sharing audio path).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ad2d-201"><strong>DeviceRenderZeroVolumeEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-201"><strong>DeviceRenderZeroVolumeEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-202">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="1ad2d-202">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1ad2d-203">Pourcentage de session l’événement DeviceRenderZeroVolume a été déclenché pour être dans l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-203">Percentage of session the DeviceRenderZeroVolume event was fired for being in the “Bad’ state.</span></span> <span data-ttu-id="1ad2d-204">L’appareil de rendu a été défini sur le volume zéro.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-204">The render device was set to zero volume.</span></span></p>
<p><span data-ttu-id="1ad2d-205">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-205">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ad2d-206"><strong>DeviceRenderMuteEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="1ad2d-206"><strong>DeviceRenderMuteEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad2d-207">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="1ad2d-207">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1ad2d-208">Pourcentage de session l’événement DeviceRenderMute a été déclenché pour être dans l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="1ad2d-208">Percentage of session the DeviceRenderMute event was fired for being in the “Bad’ state.</span></span> <span data-ttu-id="1ad2d-209">L’appareil de rendu a été coupé.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-209">The render device was muted.</span></span></p>
<p><span data-ttu-id="1ad2d-210">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1ad2d-210">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1ad2d-211">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1ad2d-211">


</div>

<span> </span>

</div>

</div>

</span></span></div>

