---
title: 'Tableau Lync Server 2013 : AppSharingStream'
description: 'Tableau Lync Server 2013 : AppSharingStream'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppSharingStream table
ms:assetid: 391490cb-d7b8-44ca-b4d1-429600da909c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204808(v=OCS.15)
ms:contentKeyID: 48183852
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b530af5b489e090e5d0d00fbb01b2b950bafbe5a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440555"
---
# <a name="appsharingstream-table-in-lync-server-2013"></a><span data-ttu-id="ef5fa-103">Table AppSharingStream dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ef5fa-103">AppSharingStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ef5fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ef5fa-104">

<span> </span></span></span>

<span data-ttu-id="ef5fa-105">_**Dernière modification de la rubrique :** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="ef5fa-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="ef5fa-106">La table AppSharingStream contient des métriques de qualité d’utilisation pour les flux réseau utilisés pour le partage d’application.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-106">The AppSharingStream table contains Quality of Experience metrics for the network streams used for application sharing.</span></span> <span data-ttu-id="ef5fa-107">Ce tableau a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef5fa-108"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="ef5fa-109"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="ef5fa-110"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="ef5fa-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef5fa-113">dateTime</span></span></p></td>
<td><p><span data-ttu-id="ef5fa-114">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="ef5fa-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="ef5fa-115">Date et heure de démarrage de la session.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-115">Date and time that the session started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-117">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-117">int</span></span></p></td>
<td><p><span data-ttu-id="ef5fa-118">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="ef5fa-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="ef5fa-119">Identificateur séquentiel permettant de faire la distinction entre les sessions qui ont commencé à la même date et en même temps.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-119">Sequential identifier used to distinguish between sessions that started on the same date and at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="ef5fa-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="ef5fa-122">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="ef5fa-122">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="ef5fa-123">Représente le type de ligne vidéo utilisée lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-123">Represents the type of video line used in the call.</span></span> <span data-ttu-id="ef5fa-124">Les valeurs autorisées sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ef5fa-124">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="ef5fa-125">0-audio</span><span class="sxs-lookup"><span data-stu-id="ef5fa-125">0 – Audio</span></span></p></li>
<li><p><span data-ttu-id="ef5fa-126">1-vidéo</span><span class="sxs-lookup"><span data-stu-id="ef5fa-126">1 – Video</span></span></p></li>
<li><p><span data-ttu-id="ef5fa-127">2-vidéo panoramique</span><span class="sxs-lookup"><span data-stu-id="ef5fa-127">2 – Panoramic video</span></span></p></li>
<li><p><span data-ttu-id="ef5fa-128">3 – partage de bureau et d’application</span><span class="sxs-lookup"><span data-stu-id="ef5fa-128">3 –Application/Desktop Sharing</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-129"><strong>StreamID</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-129"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-130">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-130">int</span></span></p></td>
<td><p><span data-ttu-id="ef5fa-131">Principal</span><span class="sxs-lookup"><span data-stu-id="ef5fa-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="ef5fa-132">Identificateur unique du flux de partage d’application.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-132">Unique identifier of the application sharing stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-133"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-133"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-134">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-134">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-135">Gigue moyenne détectée entre les arrivées de paquets RTP.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-135">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="ef5fa-136">(Gigue est une mesure du &quot; shakiness &quot; d’un appel.) Les valeurs de gigue élevée sont généralement provoquées par une congestion ou un serveur multimédia surchargé, ce qui a pour effet de déformer ou de perdre du son.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-136">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-137"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-137"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-138">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-139">Scintillement maximal détecté entre les arrivées de Paquets RTP.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-139">Maximum jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="ef5fa-140">(Gigue est une mesure du &quot; shakiness &quot; d’un appel.) Les valeurs de gigue élevée sont généralement provoquées par une congestion ou un serveur multimédia surchargé, ce qui a pour effet de déformer ou de perdre du son.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-140">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-141"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-141"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-142">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-142">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-p105">Temps moyen (en millisecondes) nécessaire à un paquet RTP (Real-Time Transport Protocol) pour effectuer un aller-retour vers un autre système d’extrémité. Des boucles de 200 millisecondes ou moins sont considérées qualitativement acceptables.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-p105">Average amount of (in milliseconds) required for a Real-Time Transport Protocol packet to travel to another endpoint and then back. Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="ef5fa-p106">Des boucles de durée plus élevée peuvent être causées par le routage international des appels, une mauvaise configuration du routage ou un serveur multimédia surchargé. Les durées d’aller-retour élevées créent des difficultés dans le cadre de conversations audio bidirectionnelles réalisées en temps réel.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-p106">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-147"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-147"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-148">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-148">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-149">Le volume maximal de (en millisecondes) requis pour un paquet de protocole de transport Real-Time pour voyager à un autre point de terminaison, puis retour.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-149">Maximum amount of (in milliseconds) required for a Real-Time Transport Protocol packet to travel to another endpoint and then back.</span></span> <span data-ttu-id="ef5fa-150">Des boucles de 200 millisecondes ou moins sont considérées qualitativement acceptables.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-150">Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="ef5fa-p108">Des boucles de durée plus élevée peuvent être causées par le routage international des appels, une mauvaise configuration du routage ou un serveur multimédia surchargé. Les durées d’aller-retour élevées créent des difficultés dans le cadre de conversations audio bidirectionnelles réalisées en temps réel.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-p108">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-153"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-153"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-154">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-154">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-p109">Taux moyen de pertes de paquets RTP. (La perte de paquets survient lorsque des paquets RTP, protocole employé pour la transmission audio et vidéo sur Internet, n’atteignent pas leur point de destination.) Les valeurs de perte élevées peuvent provenir d’une congestion, d’un dépassement de la bande passante disponible, d’une congestion/interférence dans la liaison sans fil ou d’un serveur multimédia surchargé, ce qui se traduit par une distorsion ou une perte de l’audio.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-p109">Average rate of Real-Time Transport Protocol (RTP) packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-158"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-158"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-159">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-159">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-160">Taux maximal de perte de Paquets RTP (Real-Time Transport Protocol).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-160">Maximum rate of Real-Time Transport Protocol (RTP) packet loss.</span></span> <span data-ttu-id="ef5fa-161">(La perte de paquets se produit lorsque les paquets RTP, un protocole utilisé pour transmettre des contenus audio et vidéo sur Internet, n’a pas pu atteindre leur destination.) Les taux de perte élevés sont généralement causés par une congestion ; absence de bande passante ; encombrement ou interférence sans fil ; ou un serveur multimédia surchargé.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-161">(Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server.</span></span> <span data-ttu-id="ef5fa-162">La perte de paquets génère généralement une distorsion ou une perte de son.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-162">Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-163"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-163"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-164">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-164">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-165">Nombre de paquets envoyés.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-165">Number of packets sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-166"><strong>Bande passante</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-166"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-167">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-167">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-168">Durée de bande passante estimée disponible à la fin de la session.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-168">Estimated one-way bandwidth available at the end of the session.</span></span> <span data-ttu-id="ef5fa-169">État en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-169">Reported in bits per second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-170"><strong>AppSharingPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-170"><strong>AppSharingPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-171">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-171">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-172">Description de la charge utile de partage d’application.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-172">Description of the application sharing payload.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-173"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-173"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-174">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-174">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-175">Quantité totale de latence à sens unique.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-175">Total amount of one-way latency.</span></span> <span data-ttu-id="ef5fa-176">Latence relative à sens unique, mesure du délai entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-176">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-177"><strong>Moyenne unidirectionnelle relative</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-177"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-178">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-178">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-179">Quantité moyenne de latence à sens unique.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-179">Average amount of one-way latency.</span></span> <span data-ttu-id="ef5fa-180">Latence relative à sens unique, mesure du délai entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-180">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-181"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-181"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-182">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-182">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-183">Quantité maximale de latence à sens unique.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-183">Maximum amount of one-way latency.</span></span> <span data-ttu-id="ef5fa-184">Latence relative à sens unique, mesure du délai entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-184">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-185"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-185"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-186">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-186">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-187">Nombre total d’occurrences de rafales à sens unique.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-187">Total one-way burst occurrences.</span></span> <span data-ttu-id="ef5fa-188">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendus plutôt qu’à un flux continu.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-188">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="ef5fa-189">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-189">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-190"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-190"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-191">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-191">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-192">Densité du Burst total unidirectionnel.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-192">Total one-way burst density.</span></span> <span data-ttu-id="ef5fa-193">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendus plutôt qu’à un flux continu.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-193">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="ef5fa-194">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-194">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-195"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-195"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-196">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-196">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-197">Durée totale du Burst.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-197">Total one-way burst duration.</span></span> <span data-ttu-id="ef5fa-198">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendus plutôt qu’à un flux continu.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-198">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="ef5fa-199">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-199">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-200"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-200"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-201">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-201">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-202">Nombre total d’occurrences de l’espacement unidirectionnel.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-202">Total one-way gap occurrences.</span></span> <span data-ttu-id="ef5fa-203">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendues au lieu d’un flux continu ; les intervalles indiquent les retards entre ces rafales.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-203">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="ef5fa-204">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-204">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-205"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-205"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-206">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-206">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-207">Densité de l’intervalle total à sens unique.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-207">Total one-way gap density.</span></span> <span data-ttu-id="ef5fa-208">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendues au lieu d’un flux continu ; les intervalles indiquent les retards entre ces rafales.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-208">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="ef5fa-209">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-209">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-210"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-210"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-211">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-211">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-212">Durée totale de l’intervalle.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-212">Total one-way gap duration.</span></span> <span data-ttu-id="ef5fa-213">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendues au lieu d’un flux continu ; les intervalles indiquent les retards entre ces rafales.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-213">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="ef5fa-214">Cette métrique mesure le flux de données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-214">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-215"><strong>ApplicationSharingType</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-215"><strong>ApplicationSharingType</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-216">varChar (256)</span><span class="sxs-lookup"><span data-stu-id="ef5fa-216">varChar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-217">Rôle d’application (partage ou visionneuse) et type de contenu.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-217">Application role (Sharer or Viewer) and content type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-218"><strong>RDPTileProcessingLatencyTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-218"><strong>RDPTileProcessingLatencyTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-219">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-219">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-220">Durée totale du traitement des vignettes du protocole RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-220">Total processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ef5fa-221">Un total supérieur équivaut à un délai plus long dans l’interface d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-221">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-222"><strong>Vignettes RDP</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-222"><strong>RDPTileProcessingLatencyAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-223">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-223">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-224">Durée de traitement moyenne des vignettes du protocole RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-224">Average processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ef5fa-225">Un total supérieur équivaut à un délai plus long dans l’interface d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-225">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-226"><strong>RDPTileProcessingLatencyMax</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-226"><strong>RDPTileProcessingLatencyMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-227">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-227">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-228">Temps de traitement maximal pour les vignettes de protocole RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-228">Maximum processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ef5fa-229">Un total supérieur équivaut à un délai plus long dans l’interface d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-229">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-230"><strong>RDPTileProcessingLatencyBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-230"><strong>RDPTileProcessingLatencyBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-231">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-231">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-232">Des occurrences de Burst dans le temps de traitement des vignettes de protocole RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-232">Burst occurrences in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ef5fa-233">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendus plutôt qu’à un flux continu.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-233">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-234"><strong>RDPTileProcessingLatencyBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-234"><strong>RDPTileProcessingLatencyBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-235">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-235">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-236">Densité Burst du temps de traitement des vignettes du protocole RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-236">Burst density in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ef5fa-237">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendus plutôt qu’à un flux continu.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-237">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-238"><strong>RDPTileProcessingLatencyBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-238"><strong>RDPTileProcessingLatencyBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-239">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-239">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-240">Durée Burst du temps de traitement des vignettes de protocole RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-240">Burst duration in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ef5fa-241">Une transmission « Burst » est une transmission dans laquelle les données sont transmises en rafales inattendus plutôt qu’à un flux continu.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-241">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-242"><strong>RDPTileProcessingLatencyGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-242"><strong>RDPTileProcessingLatencyGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-243">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-243">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-244">Occurrences de l’espace dans le temps de traitement des vignettes de protocole RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-244">Gap occurrences in the processing time for remote desktop protocol (RDP) tiles.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-245"><strong>RDPTileProcessingLatencyGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-245"><strong>RDPTileProcessingLatencyGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-246">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-246">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-247">La densité de l’intervalle du temps de traitement des vignettes RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-247">Gap density in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ef5fa-248">La densité de faible interépaisseur correspond à une meilleure expérience d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-248">Low gap density equates to a better viewing experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-249"><strong>RDPTileProcessingLatencyGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-249"><strong>RDPTileProcessingLatencyGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-250">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-250">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-251">Durée de l’intervalle du temps de traitement des vignettes RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-251">Gap duration in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ef5fa-252">Les durées de faible intervalle sont assimilées à une meilleure expérience d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-252">Short gap durations equate to a better viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-253"><strong>CaptureTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-253"><strong>CaptureTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-254">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-255">Taux total de vignettes capturées (en mosaïques par seconde).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-255">Total rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-256"><strong>CaptureTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-256"><strong>CaptureTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-257">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-257">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-258">Taux moyen des vignettes capturées (en mosaïques par seconde).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-258">Average rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-259"><strong>CaptureTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-259"><strong>CaptureTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-260">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-260">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-261">Taux maximal de vignettes capturées (en mosaïques par seconde).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-261">Maximum rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-262"><strong>CaptureTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-262"><strong>CaptureTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-263">dans t</span><span class="sxs-lookup"><span data-stu-id="ef5fa-263">in t</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-264">Occurrences de Burst dans le taux de vignettes capturées (en mosaïques par seconde).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-264">Burst occurrences in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-265"><strong>CaptureTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-265"><strong>CaptureTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-266">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-266">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-267">Densité Burst dans le taux de vignettes capturées (en mosaïques par seconde).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-267">Burst density in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-268"><strong>CaptureTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-268"><strong>CaptureTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-269">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-269">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-270">Durée Burst dans le taux de vignettes capturées (en mosaïques par seconde).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-270">Burst duration in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-271"><strong>CaptureTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-271"><strong>CaptureTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-272">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-272">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-273">Occurrences de l’espace dans le taux de vignettes capturées (en mosaïques par seconde).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-273">Gap occurrences in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-274"><strong>CaptureTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-274"><strong>CaptureTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-275">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-275">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-276">Densité de l’intervalle dans le taux de vignettes capturées (en mosaïques par seconde).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-276">Gap density in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-277"><strong>CaptureTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-277"><strong>CaptureTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-278">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-278">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-279">Durée de l’intervalle en fonction du taux de vignettes capturées (en mosaïques par seconde).</span><span class="sxs-lookup"><span data-stu-id="ef5fa-279">Gap duration in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-280"><strong>Vignettes altérées</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-280"><strong>SpoiledTilePercentTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-281">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-281">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-282">Pourcentage total du contenu n’ayant pas atteint la visionneuse, mais qui a été ignoré et écrasé par le contenu actualisé.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-282">Total percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-283"><strong>SpoiledTilePercentAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-283"><strong>SpoiledTilePercentAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-284">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-284">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-285">Pourcentage moyen du contenu n’ayant pas atteint la visionneuse, mais qui a été ignoré et écrasé par le contenu actualisé.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-285">Average percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-286"><strong>SpoiledTilePercentMax</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-286"><strong>SpoiledTilePercentMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-287">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-287">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-288">Pourcentage maximal du contenu n’ayant pas atteint la visionneuse, mais a été ignoré et écrasé par le contenu actualisé.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-288">Maximum percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-289"><strong>SpoiledTilePercentBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-289"><strong>SpoiledTilePercentBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-290">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-290">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-291">Des occurrences de Burst pour le contenu n’ayant pas atteint la visionneuse, mais qui ont été ignorées et écrasées par le contenu fraîche.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-291">Burst occurrences for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-292"><strong>SpoiledTilePercentBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-292"><strong>SpoiledTilePercentBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-293">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-293">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-294">Densité Burst pour le contenu n’ayant pas atteint la visionneuse, mais qui a été ignoré et écrasé par le contenu actualisé.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-294">Burst density for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-295"><strong>SpoiledTilePercentBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-295"><strong>SpoiledTilePercentBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-296">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-296">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-297">Durée Burst pour le contenu n’ayant pas atteint la visionneuse, mais qui a été supprimée et écrasé par le contenu fraîche.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-297">Burst duration for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-298"><strong>SpoiledTilePercentGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-298"><strong>SpoiledTilePercentGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-299">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-299">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-300">Occurrences d’espace pour le contenu n’ayant pas atteint la visionneuse, mais qui ont été ignorées et écrasées par le contenu fraîche.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-300">Gap occurrences for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-301"><strong>SpoiledTilePercentGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-301"><strong>SpoiledTilePercentGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-302">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-302">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-303">Densité de l’intervalle pour le contenu n’ayant pas atteint la visionneuse, mais qui a été supprimée et écrasé par le contenu actualisé.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-303">Gap density for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-304"><strong>SpoiledTilePercentGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-304"><strong>SpoiledTilePercentGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-305">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-305">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-306">Durée de l’intervalle pour le contenu n’ayant pas atteint la visionneuse, mais qui a été annulée et écrasée par le contenu actualisé.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-306">Gap duration for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-307"><strong>ScrapingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-307"><strong>ScrapingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-308">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-308">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-309">Nombre total d’images abîmées à partir de la source graphique.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-309">Total number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-310"><strong>ScrapingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-310"><strong>ScrapingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-311">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-311">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-312">Nombre moyen de trames abîmées dans la source graphique.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-312">Average number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-313"><strong>ScrapingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-313"><strong>ScrapingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-314">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-314">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-315">Nombre maximal d’images abîmées dans la source graphique.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-315">Maximum number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-316"><strong>ScrapingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-316"><strong>ScrapingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-317">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-317">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-318">Des occurrences de Burst dans les trames abîmées à partir de la source graphique.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-318">Burst occurrences in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-319"><strong>ScrapingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-319"><strong>ScrapingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-320">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-320">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-321">Densité Burst dans les trames abîmées à partir de la source graphique.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-321">Burst density in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-322"><strong>ScrapingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-322"><strong>ScrapingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-323">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-323">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-324">Durée Burst dans les trames rachetées à partir de la source graphique.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-324">Burst duration in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-325"><strong>ScrapingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-325"><strong>ScrapingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-326">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-326">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-327">Occurrences de l’espace dans les trames abîmées dans la source graphique.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-327">Gap occurrences in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-328"><strong>ScrapingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-328"><strong>ScrapingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-329">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-329">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-330">Densité de l’intervalle dans les trames rachetées à partir de la source graphique.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-330">Gap density in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-331"><strong>ScrapingFrameRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-331"><strong>ScrapingFrameRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-332">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-332">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-333">Durée de l’intervalle dans les trames abîmées par la source graphique.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-333">Gap duration in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-334"><strong>IncomingTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-334"><strong>IncomingTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-335">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-335">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-336">Taux total d’images entrantes reçues par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-336">Total incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-337"><strong>IncomingTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-337"><strong>IncomingTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-338">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-338">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-339">Taux moyen d’images entrantes reçues par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-339">Average incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-340"><strong>IncomingTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-340"><strong>IncomingTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-341">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-341">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-342">Taux maximal de vignettes entrantes reçues par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-342">Maximum incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-343"><strong>IncomingTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-343"><strong>IncomingTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-344">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-344">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-345">Des occurrences de Burst dans le taux de vignettes entrantes reçues par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-345">Burst occurrences in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-346"><strong>IncomingTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-346"><strong>IncomingTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-347">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-347">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-348">Densité Burst dans le taux de vignette entrante tel qu’il est reçu par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-348">Burst density in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-349"><strong>IncomingTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-349"><strong>IncomingTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-350">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-350">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-351">Durée Burst dans le taux de vignette entrante tel qu’il est reçu par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-351">Burst duration in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-352"><strong>IncomingTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-352"><strong>IncomingTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-353">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-353">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-354">Occurrences de l’espace dans le taux de vignette entrantes reçues par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-354">Gap occurrences in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-355"><strong>IncomingTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-355"><strong>IncomingTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-356">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-356">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-357">Densité de l’intervalle dans le taux de vignette entrante tel qu’il est reçu par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-357">Gap density in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-358"><strong>IncomingTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-358"><strong>IncomingTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-359">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-359">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-360">Durée de l’intervalle dans le taux de vignette entrante tel qu’il est reçu par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-360">Gap duration in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-361"><strong>IncomingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-361"><strong>IncomingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-362">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-362">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-363">Taux total d’images entrantes reçues par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-363">Total incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-364"><strong>IncomingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-364"><strong>IncomingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-365">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-365">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-366">Taux moyen d’images entrantes reçues par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-366">Average incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-367"><strong>IncomingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-367"><strong>IncomingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-368">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-368">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-369">Taux maximal d’images entrantes reçues par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-369">Maximum incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-370"><strong>IncomingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-370"><strong>IncomingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-371">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-371">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-372">Des occurrences de Burst dans la fréquence d’images entrantes reçues par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-372">Burst occurrences in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-373"><strong>IncomingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-373"><strong>IncomingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-374">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-374">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-375">Densité Burst dans la fréquence d’images entrantes reçue par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-375">Burst density in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-376"><strong>IncomingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-376"><strong>IncomingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-377">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-377">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-378">Durée Burst dans la fréquence d’images entrantes reçue par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-378">Burst duration in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-379"><strong>IncomingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-379"><strong>IncomingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-380">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-380">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-381">Occurrences de l’espace dans la fréquence d’images entrantes reçues par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-381">Gap occurrences in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-382"><strong>IncomingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-382"><strong>IncomingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-383">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-383">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-384">Densité de l’intervalle dans la fréquence d’images entrantes reçue par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-384">Gap density in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-385"><strong>IncomingFrameRateDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-385"><strong>IncomingFrameRateDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-386">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-386">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-387">Durée de l’intervalle dans la fréquence d’images entrantes reçue par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-387">Gap duration in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-388"><strong>OutgoingTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-388"><strong>OutgoingTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-389">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-389">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-390">Taux total de vignettes sortantes de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-390">Total outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-391"><strong>OutgoingTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-391"><strong>OutgoingTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-392">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-392">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-393">Taux moyen d’une vignette sortante pour l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-393">Average outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-394"><strong>OutgoingTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-394"><strong>OutgoingTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-395">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-395">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-396">Taux de vignette sortante maximal pour l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-396">Maximum outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-397"><strong>OutgoingTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-397"><strong>OutgoingTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-398">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-398">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-399">Des occurrences de Burst dans le taux de vignette sortante pour l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-399">Burst occurrences in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-400"><strong>OutgoingTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-400"><strong>OutgoingTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-401">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-401">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-402">Densité Burst dans le taux de vignette sortante pour l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-402">Burst density in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-403"><strong>OutgoingTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-403"><strong>OutgoingTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-404">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-404">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-405">Durée Burst dans le taux de vignette sortante pour l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-405">Burst duration in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-406"><strong>OutgoingTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-406"><strong>OutgoingTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-407">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-407">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-408">Occurrences de l’espace dans le taux de vignette sortante de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-408">Gap occurrences in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-409"><strong>OutgoingTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-409"><strong>OutgoingTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-410">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-410">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-411">Densité de l’intervalle dans le taux de vignette sortante pour l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-411">Gap density in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-412"><strong>OutgoingTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-412"><strong>OutgoingTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-413">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-413">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-414">Durée de l’intervalle dans le taux de vignette sortante pour l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-414">Gap duration in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-415"><strong>OutgoingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-415"><strong>OutgoingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-416">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-416">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-417">Taux total d’images sortantes pour l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-417">Total outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-418"><strong>OutgoingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-418"><strong>OutgoingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-419">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-419">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-420">taux moyen d’images sortantes pour l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-420">average outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-421"><strong>OutgoingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-421"><strong>OutgoingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-422">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-422">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-423">Taux maximal d’images sortant pour l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-423">Maximum outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-424"><strong>OutgoingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-424"><strong>OutgoingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-425">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-425">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-426">Des occurrences de Burst dans le taux d’images sortant pour l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-426">Burst occurrences in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-427"><strong>OutgoingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-427"><strong>OutgoingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-428">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-428">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-429">Densité Burst dans le taux d’image sortant de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-429">Burst density in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-430"><strong>OutgoingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-430"><strong>OutgoingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-431">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-431">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-432">Durée Burst dans le taux d’images sortant de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-432">Burst duration in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-433"><strong>OutgoingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-433"><strong>OutgoingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-434">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-434">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-435">Occurrences de l’espace dans le taux d’image sortant de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-435">Gap occurrences in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-436"><strong>OutgoingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-436"><strong>OutgoingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-437">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-437">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-438">Densité de l’intervalle dans le taux d’image sortant de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-438">Gap density in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-439"><strong>OutgoingFrameRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-439"><strong>OutgoingFrameRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-440">float</span><span class="sxs-lookup"><span data-stu-id="ef5fa-440">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-441">Durée de l’intervalle dans le taux d’image sortant de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-441">Gap duration in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-442"><strong>AverageRectangleHeight</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-442"><strong>AverageRectangleHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-443">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-443">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-444">Hauteur moyenne de la résolution vidéo, en pixels.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-444">Average video resolution height, in pixels.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-445"><strong>AverageRectangleWidth</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-445"><strong>AverageRectangleWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-446">int</span><span class="sxs-lookup"><span data-stu-id="ef5fa-446">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-447">Largeur de résolution vidéo moyenne, en pixels.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-447">Average video resolution width, in pixels.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-448"><strong>Entrant</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-448"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-449">bit</span><span class="sxs-lookup"><span data-stu-id="ef5fa-449">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-450">Fréquence d’images moyenne (en images par seconde) pour les transmissions entrantes.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-450">Average frame rate (in frames per second) for inbound transmissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5fa-451"><strong>Sortant</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-451"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-452">bit</span><span class="sxs-lookup"><span data-stu-id="ef5fa-452">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-453">Fréquence d’images moyenne (en images par seconde) pour les transmissions sortantes.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-453">Average frame rate (in frames per second) for outbound transmissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5fa-454"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="ef5fa-454"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5fa-455">bit</span><span class="sxs-lookup"><span data-stu-id="ef5fa-455">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef5fa-456">1 signifie que le sens du flux provient de l’appelant vers l’appel.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-456">1 means the stream direction is from the caller to callee.</span></span></p>
<p><span data-ttu-id="ef5fa-457">0 : le sens du flux provient de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="ef5fa-457">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ef5fa-458">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ef5fa-458">


</div>

<span> </span>

</div>

</div>

</span></span></div>

