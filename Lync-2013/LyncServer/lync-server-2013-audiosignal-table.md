---
title: 'Lync Server 2013 : table AudioSignal'
description: 'Tableau Lync Server 2013 : AudioSignal'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioSignal table
ms:assetid: 0013c8c6-cdf9-4d70-bc2a-cddd1560f66b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398064(v=OCS.15)
ms:contentKeyID: 48183217
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82f3b3119eaccfe56c4706cff07469bc3434461f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438205"
---
# <a name="audiosignal-table-in-lync-server-2013"></a><span data-ttu-id="34fbf-103">Table AudioSignal de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="34fbf-103">AudioSignal table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="34fbf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="34fbf-104">

<span> </span></span></span>

<span data-ttu-id="34fbf-105">_**Dernière modification de la rubrique :** 2013-11-12_</span><span class="sxs-lookup"><span data-stu-id="34fbf-105">_**Topic Last Modified:** 2013-11-12_</span></span>

<span data-ttu-id="34fbf-106">Chaque enregistrement représente les métriques du signal audio pour un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="34fbf-106">Each record represents audio signal metrics for one endpoint.</span></span> <span data-ttu-id="34fbf-107">En règle générale, chaque appel comporte deux enregistrements, l’un pour l’appelant et l’autre pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="34fbf-107">Usually, each call has two records, one is for caller, and one is for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34fbf-108"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="34fbf-109"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="34fbf-110"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="34fbf-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34fbf-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="34fbf-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="34fbf-114">Principal</span><span class="sxs-lookup"><span data-stu-id="34fbf-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="34fbf-115">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="34fbf-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34fbf-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-117">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-117">int</span></span></p></td>
<td><p><span data-ttu-id="34fbf-118">Principal</span><span class="sxs-lookup"><span data-stu-id="34fbf-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="34fbf-119">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="34fbf-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34fbf-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="34fbf-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="34fbf-122">Principal</span><span class="sxs-lookup"><span data-stu-id="34fbf-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="34fbf-123">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="34fbf-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34fbf-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-125">bit</span><span class="sxs-lookup"><span data-stu-id="34fbf-125">bit</span></span></p></td>
<td><p><span data-ttu-id="34fbf-126">Principal</span><span class="sxs-lookup"><span data-stu-id="34fbf-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="34fbf-127">0 : données du destinataire</span><span class="sxs-lookup"><span data-stu-id="34fbf-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="34fbf-128">1 : données de l’appelant</span><span class="sxs-lookup"><span data-stu-id="34fbf-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34fbf-129"><strong>SendSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-129"><strong>SendSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-130">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-130">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-131">Représente le niveau du signal audio après le contrôle du gain.</span><span class="sxs-lookup"><span data-stu-id="34fbf-131">Represents the Post-Analog Gain Control audio signal level.</span></span> <span data-ttu-id="34fbf-132">L’unité de cette métrique est dBmo.</span><span class="sxs-lookup"><span data-stu-id="34fbf-132">The unit for this metric is dBmo.</span></span> <span data-ttu-id="34fbf-133">Pour une qualité acceptable, il devrait représenter au moins 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="34fbf-133">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="34fbf-134">Cette métrique n’est pas communiquée par le serveur de conférence A/V ou les téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="34fbf-134">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34fbf-135"><strong>RecvSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-135"><strong>RecvSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-136">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-136">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-137">Voir SendSignalLevel.</span><span class="sxs-lookup"><span data-stu-id="34fbf-137">See SendSignalLevel.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34fbf-138"><strong>SendNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-138"><strong>SendNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-139">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-139">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-140">Représente le niveau de bruit sonore du contrôle post-analogue.</span><span class="sxs-lookup"><span data-stu-id="34fbf-140">Represents the Post-Analog Gain Control audio noise level.</span></span> <span data-ttu-id="34fbf-141">L’unité de cette métrique est dBmo.</span><span class="sxs-lookup"><span data-stu-id="34fbf-141">The unit for this metric is dBmo.</span></span> <span data-ttu-id="34fbf-142">Pour une qualité acceptable, elle doit être inférieure à 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="34fbf-142">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="34fbf-143">Cette métrique n’est pas communiquée par le serveur de conférence A/V ou les téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="34fbf-143">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34fbf-144"><strong>RecvNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-144"><strong>RecvNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-145">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-145">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-146">Voir SendNoiseLevel.</span><span class="sxs-lookup"><span data-stu-id="34fbf-146">See SendNoiseLevel.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34fbf-147"><strong>EchoReturn</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-147"><strong>EchoReturn</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-148">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-148">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-149">Métrique d’amélioration de retour d’écho.</span><span class="sxs-lookup"><span data-stu-id="34fbf-149">Echo Return Loss Enhancement metric.</span></span> <span data-ttu-id="34fbf-150">L’unité de cette métrique est dB.</span><span class="sxs-lookup"><span data-stu-id="34fbf-150">The unit for this metric is dB.</span></span> <span data-ttu-id="34fbf-151">Les valeurs inférieures représentent moins d’écho.</span><span class="sxs-lookup"><span data-stu-id="34fbf-151">Lower values represent less echo.</span></span> <span data-ttu-id="34fbf-152">Cette métrique n’est pas communiquée par le serveur de conférence A/V ou les téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="34fbf-152">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34fbf-153"><strong>AudioSpeakerGlitchRate</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-153"><strong>AudioSpeakerGlitchRate</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-154">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-154">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-155">Moyenne des problèmes par cinq minutes pour le rendu du haut-parleur.</span><span class="sxs-lookup"><span data-stu-id="34fbf-155">Average glitches per five minutes for the loudspeaker rendering.</span></span> <span data-ttu-id="34fbf-156">Pour une qualité optimale, cela devrait être inférieur à une par cinq minutes.</span><span class="sxs-lookup"><span data-stu-id="34fbf-156">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="34fbf-157">Non communiquées par des serveurs de conférence A/V, des serveurs de médiation ou des téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="34fbf-157">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34fbf-158"><strong>AudioMicGlitchRate</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-158"><strong>AudioMicGlitchRate</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-159">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-159">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-160">Moyenne des problèmes par cinq minutes pour la capture du micro.</span><span class="sxs-lookup"><span data-stu-id="34fbf-160">Average glitches per five minutes for the microphone capture.</span></span> <span data-ttu-id="34fbf-161">Pour une qualité optimale, il devrait être inférieur à une par cinq minutes.</span><span class="sxs-lookup"><span data-stu-id="34fbf-161">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="34fbf-162">Non communiquées par des serveurs de conférence A/V, des serveurs de médiation ou des téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="34fbf-162">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34fbf-163"><strong>AudioTimestampDriftRateMic</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-163"><strong>AudioTimestampDriftRateMic</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-164">décimale (9 ; 2)</span><span class="sxs-lookup"><span data-stu-id="34fbf-164">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-165">Taux d’horloge de l’horloge du périphérique microphone par rapport à l’horloge de l’UC.</span><span class="sxs-lookup"><span data-stu-id="34fbf-165">Microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34fbf-166"><strong>AudioTimestampDriftRateSpk</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-166"><strong>AudioTimestampDriftRateSpk</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-167">décimale (9 ; 2)</span><span class="sxs-lookup"><span data-stu-id="34fbf-167">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-168">Taux d’horloge du périphérique de haut-parleurs par rapport à l’horloge du processeur.</span><span class="sxs-lookup"><span data-stu-id="34fbf-168">Speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34fbf-169"><strong>AudioTimestampErrorMicMs</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-169"><strong>AudioTimestampErrorMicMs</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-170">décimale (9 ; 2)</span><span class="sxs-lookup"><span data-stu-id="34fbf-170">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-171">Taux d’horloge du périphérique de haut-parleurs par rapport à l’horloge du processeur.</span><span class="sxs-lookup"><span data-stu-id="34fbf-171">Speaker device clock drift rate, relative to CPU clock.</span></span></p>
<p><span data-ttu-id="34fbf-172">Erreur d’horodatage du flux de capture de microphone moyenne, en millisecondes, au cours des dernières 20 secondes de l’appel.</span><span class="sxs-lookup"><span data-stu-id="34fbf-172">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34fbf-173"><strong>AudioTimestampErrorSpkMs</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-173"><strong>AudioTimestampErrorSpkMs</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-174">décimale (9 ; 2)</span><span class="sxs-lookup"><span data-stu-id="34fbf-174">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-175">Erreur d’horodatage moyenne du flux de rendu du présentateur, en millisecondes, au cours des dernières 20 secondes de l’appel.</span><span class="sxs-lookup"><span data-stu-id="34fbf-175">Average speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34fbf-176"><strong>VsEntryCauses</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-176"><strong>VsEntryCauses</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-177">type</span><span class="sxs-lookup"><span data-stu-id="34fbf-177">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-178">Le commutateur vocal est un mode semi-duplex présentant une capacité d’interruption réduite.</span><span class="sxs-lookup"><span data-stu-id="34fbf-178">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="34fbf-179">Causes de l’entrée du commutateur vocal :</span><span class="sxs-lookup"><span data-stu-id="34fbf-179">Causes of voice switch entry:</span></span></p>
<p><span data-ttu-id="34fbf-180">ENTER_VS_BADTS 0x01</span><span class="sxs-lookup"><span data-stu-id="34fbf-180">ENTER_VS_BADTS 0x01</span></span></p>
<p><span data-ttu-id="34fbf-181">ENTER_VS_ECHO 0x02</span><span class="sxs-lookup"><span data-stu-id="34fbf-181">ENTER_VS_ECHO 0x02</span></span></p>
<p><span data-ttu-id="34fbf-182">ENTER_VS_FORCEORCONVERGENCE 0x04</span><span class="sxs-lookup"><span data-stu-id="34fbf-182">ENTER_VS_FORCEORCONVERGENCE 0x04</span></span></p>
<p><span data-ttu-id="34fbf-183">ENTER_VS_DNLP 0x08</span><span class="sxs-lookup"><span data-stu-id="34fbf-183">ENTER_VS_DNLP 0x08</span></span></p>
<p><span data-ttu-id="34fbf-184">La cause peut être une combinaison de ces causes individuelles.</span><span class="sxs-lookup"><span data-stu-id="34fbf-184">The cause can be a combination of those individual causes.</span></span> <span data-ttu-id="34fbf-185">ENTER_VS_FORCEORCONVERGENCE ne peut être activé qu’à l’aide de RegKey à des fins de test.</span><span class="sxs-lookup"><span data-stu-id="34fbf-185">ENTER_VS_FORCEORCONVERGENCE can only be enabled by regkey for test purpose.</span></span></p>
<p><span data-ttu-id="34fbf-186">Le type de données de cette colonne a été modifié dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="34fbf-186">The data type for this column was changed in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34fbf-187"><strong>EchoEventCauses</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-187"><strong>EchoEventCauses</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-188">tinyint</span><span class="sxs-lookup"><span data-stu-id="34fbf-188">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-189">Causes d’un événement ECHO :</span><span class="sxs-lookup"><span data-stu-id="34fbf-189">Causes of an echo event:</span></span></p>
<p><span data-ttu-id="34fbf-190">ECHO_EVENT_BAD_TIMESTAMP 0x01</span><span class="sxs-lookup"><span data-stu-id="34fbf-190">ECHO_EVENT_BAD_TIMESTAMP 0x01</span></span></p>
<p><span data-ttu-id="34fbf-191">ECHO_EVENT_POSTAEC_ECHO 0x02</span><span class="sxs-lookup"><span data-stu-id="34fbf-191">ECHO_EVENT_POSTAEC_ECHO 0x02</span></span></p>
<p><span data-ttu-id="34fbf-192">ECHO_EVENT_ANLP 0x04</span><span class="sxs-lookup"><span data-stu-id="34fbf-192">ECHO_EVENT_ANLP 0x04</span></span></p>
<p><span data-ttu-id="34fbf-193">ECHO_EVENT_DNLP 0x08</span><span class="sxs-lookup"><span data-stu-id="34fbf-193">ECHO_EVENT_DNLP 0x08</span></span></p>
<p><span data-ttu-id="34fbf-194">ECHO_EVENT_MIC_CLIPPING 0x10</span><span class="sxs-lookup"><span data-stu-id="34fbf-194">ECHO_EVENT_MIC_CLIPPING 0x10</span></span></p>
<p><span data-ttu-id="34fbf-195">ECHO_EVENT_BAD_STATE 0x20</span><span class="sxs-lookup"><span data-stu-id="34fbf-195">ECHO_EVENT_BAD_STATE 0x20</span></span></p>
<p><span data-ttu-id="34fbf-196">La cause peut être une combinaison de ces causes individuelles.</span><span class="sxs-lookup"><span data-stu-id="34fbf-196">The cause can be a combination of those individual causes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34fbf-197"><strong>EchoPercentMicIn</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-197"><strong>EchoPercentMicIn</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-198">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="34fbf-198">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-p109">Temps en pourcentage lors de la détection d’un écho dans le flux de capture du microphone. En règle générale, des valeurs faibles s’affichent pour les casques ou les combinés et des valeurs élevées pour les téléphones mains libres ou les haut-parleurs autonomes. Pour les appareils qui prennent en charge la suppression d’écho intégrée, des valeurs élevées indiquent une fuite d’écho. Pour les autres appareils, cette mesure ne doit pas être utilisée pour évaluer la qualité de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="34fbf-p109">Percentage of time when echo was detected in the microphone capture stream. Typically, values are low for headsets or handsets, and higher for speaker phones or stand-alone speakers. For devices that support on-board acoustic echo cancellation, high values indicate echo leak. For other devices, this metric should not be used to evaluate device quality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34fbf-203"><strong>EchoPercentSend</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-203"><strong>EchoPercentSend</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-204">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="34fbf-204">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="34fbf-205">Pourcentage de temps pendant lequel l’écho est détecté dans le flux envoyé.</span><span class="sxs-lookup"><span data-stu-id="34fbf-205">Percentage of time when echo is detected in sent stream.</span></span> <span data-ttu-id="34fbf-206">Pourcentage d’écho élevé dans les flux d’envoi indicateur de fuite d’écho.</span><span class="sxs-lookup"><span data-stu-id="34fbf-206">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34fbf-207"><strong>RxAGCSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-207"><strong>RxAGCSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-208">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-208">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-209">Reçu le niveau du signal sur le serveur de médiation de la passerelle ; Cela s’applique uniquement au serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="34fbf-209">Received signal level on the Mediation Server from the Gateway; this applies only to the Mediation Server.</span></span> <span data-ttu-id="34fbf-210">L’unité de cette valeur est dBoV.</span><span class="sxs-lookup"><span data-stu-id="34fbf-210">The unit of this metric is dBoV.</span></span> <span data-ttu-id="34fbf-211">Pour une qualité optimale, la plage acceptable doit être comprise entre [-30 et-18] dBoV.</span><span class="sxs-lookup"><span data-stu-id="34fbf-211">For good quality, the acceptable range should be [-30 to -18] dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34fbf-212"><strong>RxAGCNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-212"><strong>RxAGCNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-213">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-213">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-214">Reçu le niveau du signal sur le serveur de médiation de la passerelle.</span><span class="sxs-lookup"><span data-stu-id="34fbf-214">Received signal level on the Mediation Server from the Gateway.</span></span> <span data-ttu-id="34fbf-215">Cela s’applique uniquement au serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="34fbf-215">This applies only to the Mediation Server.</span></span> <span data-ttu-id="34fbf-216">L’unité de cette valeur est dBoV.</span><span class="sxs-lookup"><span data-stu-id="34fbf-216">The unit of this metric is dBoV.</span></span> <span data-ttu-id="34fbf-217">Pour une qualité optimale, la plage acceptable doit être inférieure à-50 dBoV.</span><span class="sxs-lookup"><span data-stu-id="34fbf-217">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34fbf-218"><strong>RxAvgAGCGain</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-218"><strong>RxAvgAGCGain</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-219">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-219">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-220">Contrôle automatique de gain sur le côté serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="34fbf-220">Automatic gain control (AGC) on the Mediation Server side.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34fbf-221"><strong>InitialSignalLevelRMS</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-221"><strong>InitialSignalLevelRMS</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-222">float</span><span class="sxs-lookup"><span data-stu-id="34fbf-222">float</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="34fbf-223">Le carré moyen racine (RMS) du signal entrant jusqu’aux 30 premières secondes de l’appel.</span><span class="sxs-lookup"><span data-stu-id="34fbf-223">The root mean square (RMS) of the incoming signal of up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34fbf-224"><strong>RecvSignalLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-224"><strong>RecvSignalLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-225">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-225">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="34fbf-226">Niveau du signal reçu sur le canal 1.</span><span class="sxs-lookup"><span data-stu-id="34fbf-226">Signal level as received on channel 1.</span></span></p>
<p><span data-ttu-id="34fbf-227">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="34fbf-227">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34fbf-228"><strong>RecvSignalLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-228"><strong>RecvSignalLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-229">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-229">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="34fbf-230">Niveau du signal reçu sur le canal 2.</span><span class="sxs-lookup"><span data-stu-id="34fbf-230">Signal level as received on channel 2.</span></span></p>
<p><span data-ttu-id="34fbf-231">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="34fbf-231">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34fbf-232"><strong>RecvNoiseLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-232"><strong>RecvNoiseLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-233">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-233">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="34fbf-234">Niveau sonore reçu sur canal 1.</span><span class="sxs-lookup"><span data-stu-id="34fbf-234">Noise level as received on channel 1.</span></span></p>
<p><span data-ttu-id="34fbf-235">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="34fbf-235">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34fbf-236"><strong>RecvNoiseLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-236"><strong>RecvNoiseLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-237">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-237">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="34fbf-238">Niveau sonore reçu sur canal 2.</span><span class="sxs-lookup"><span data-stu-id="34fbf-238">Noise level as received on channel 2.</span></span></p>
<p><span data-ttu-id="34fbf-239">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="34fbf-239">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34fbf-240"><strong>SendSignalLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-240"><strong>SendSignalLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-241">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-241">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="34fbf-242">Niveau du signal envoyé sur canal 1.</span><span class="sxs-lookup"><span data-stu-id="34fbf-242">Signal level as sent on channel 1.</span></span></p>
<p><span data-ttu-id="34fbf-243">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="34fbf-243">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34fbf-244"><strong>SendSignalLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-244"><strong>SendSignalLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-245">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-245">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="34fbf-246">Niveau du signal envoyé sur canal 2.</span><span class="sxs-lookup"><span data-stu-id="34fbf-246">Signal level as sent on channel 2.</span></span></p>
<p><span data-ttu-id="34fbf-247">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="34fbf-247">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34fbf-248"><strong>SendNoiseLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-248"><strong>SendNoiseLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-249">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-249">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="34fbf-250">Niveau sonore tel qu’il est envoyé sur canal 1.</span><span class="sxs-lookup"><span data-stu-id="34fbf-250">Noise level as sent on channel 1.</span></span></p>
<p><span data-ttu-id="34fbf-251">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="34fbf-251">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34fbf-252"><strong>SendNoiseLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="34fbf-252"><strong>SendNoiseLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="34fbf-253">int</span><span class="sxs-lookup"><span data-stu-id="34fbf-253">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="34fbf-254">Niveau sonore tel qu’il est envoyé sur canal 2.</span><span class="sxs-lookup"><span data-stu-id="34fbf-254">Noise level as sent on channel 2.</span></span></p>
<p><span data-ttu-id="34fbf-255">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="34fbf-255">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="34fbf-256">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="34fbf-256">


</div>

<span> </span>

</div>

</div>

</span></span></div>

