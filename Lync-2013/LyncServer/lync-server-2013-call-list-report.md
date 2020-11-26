---
title: 'Lync Server 2013 : rapport sur la liste d’appels'
description: 'Lync Server 2013 : rapport sur la liste d’appels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call List Report
ms:assetid: 9739f9f0-7a37-4844-91d5-f089d2011013
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615020(v=OCS.15)
ms:contentKeyID: 48184921
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5b08d4c5f3011facc9cd8d4f6b2800638f3cc896
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435753"
---
# <a name="call-list-report-in-lync-server-2013"></a><span data-ttu-id="62b20-103">Rapport de liste d’appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="62b20-103">Call List Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="62b20-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="62b20-104">

<span> </span></span></span>

<span data-ttu-id="62b20-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="62b20-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="62b20-106">Le rapport Liste des appels fournit des métriques de Qualité de l’expérience pour chaque appel émis et reçu dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="62b20-106">The Call List Report provides Quality of Experience (QoE) metrics for individual calls made and received in your organization.</span></span> <span data-ttu-id="62b20-107">Notez que les mesures réelles indiquées dépendent de la façon dont vous accédez au rapport Liste des appels.</span><span class="sxs-lookup"><span data-stu-id="62b20-107">Note that the actual metrics reported will depend on how you access the Call List report.</span></span> <span data-ttu-id="62b20-108">Par exemple, si vous ouvrez le rapport à partir du [rapport sur les appareils dans Lync Server 2013](lync-server-2013-device-report.md), vous verrez des indicateurs tels que les métriques suivantes qui sont également signalées sur le rapport sur les appareils :</span><span class="sxs-lookup"><span data-stu-id="62b20-108">For example, if you open the report from the [Device Report in Lync Server 2013](lync-server-2013-device-report.md), you'll see metrics such as the following, metrics that are also reported on the Device Report:</span></span>

  - <span data-ttu-id="62b20-109">Microphone de l’appelant</span><span class="sxs-lookup"><span data-stu-id="62b20-109">Caller's microphone</span></span>

  - <span data-ttu-id="62b20-110">Haut-parleur de l’appelant</span><span class="sxs-lookup"><span data-stu-id="62b20-110">Caller's speaker</span></span>

  - <span data-ttu-id="62b20-111">Microphone de l’appelé</span><span class="sxs-lookup"><span data-stu-id="62b20-111">Callee's microphone</span></span>

  - <span data-ttu-id="62b20-112">Haut-parleur de l’appelé</span><span class="sxs-lookup"><span data-stu-id="62b20-112">Callee's speaker</span></span>

  - <span data-ttu-id="62b20-113">Ratio de la durée du basculement vocal</span><span class="sxs-lookup"><span data-stu-id="62b20-113">Ratio of voice switch time</span></span>

<span data-ttu-id="62b20-114">Toutefois, si vous ouvrez le rapport liste d’appels [dans le rapport d’emplacements dans Lync Server 2013](lync-server-2013-location-report.md), vous ne verrez pas l’un de ces indicateurs. à la place, vous verrez des métriques comme celles-ci :</span><span class="sxs-lookup"><span data-stu-id="62b20-114">However, if you open the Call List Report from the [Location Report in Lync Server 2013](lync-server-2013-location-report.md), you won't see any of those metrics; instead, you'll see metrics like these:</span></span>

  - <span data-ttu-id="62b20-115">Boucle (ms)</span><span class="sxs-lookup"><span data-stu-id="62b20-115">Round trip (ms)</span></span>

  - <span data-ttu-id="62b20-116">Dégradation (MOS)</span><span class="sxs-lookup"><span data-stu-id="62b20-116">Degradation (MOS)</span></span>

  - <span data-ttu-id="62b20-117">Perte de paquets</span><span class="sxs-lookup"><span data-stu-id="62b20-117">Packet loss</span></span>

  - <span data-ttu-id="62b20-118">Gigue (ms)</span><span class="sxs-lookup"><span data-stu-id="62b20-118">Jitter (ms)</span></span>

<span data-ttu-id="62b20-p102">Il s’agit des mesures signalées dans le Rapport d’emplacement. Cependant, dans le rapport Liste des appels, vous pouvez toujours cliquer sur la mesure Détail pour fournir des informations de qualité de l’expérience complète pour n’importe quel appel.</span><span class="sxs-lookup"><span data-stu-id="62b20-p102">Those are the metrics reported on the Location Report. However, from the Call List Report you can always click the Detail metric to provide complete QoE information for any call.</span></span>

<div>

## <a name="accessing-the-call-list-report"></a><span data-ttu-id="62b20-121">Accès au rapport Liste des appels</span><span class="sxs-lookup"><span data-stu-id="62b20-121">Accessing the Call List Report</span></span>

<span data-ttu-id="62b20-122">Le rapport Liste des appels est accessible à partir des rapports suivants :</span><span class="sxs-lookup"><span data-stu-id="62b20-122">The Call List Report can be accessed from any of the following reports:</span></span>

  - <span data-ttu-id="62b20-123">Le [rapport d’emplacement dans Lync Server 2013](lync-server-2013-location-report.md) (en cliquant sur le volume des appels ou en utilisant une métrique de pourcentage médiocre)</span><span class="sxs-lookup"><span data-stu-id="62b20-123">The [Location Report in Lync Server 2013](lync-server-2013-location-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="62b20-124">[Rapport sur les appareils dans Lync Server 2013](lync-server-2013-device-report.md) (en cliquant sur le volume des appels ou en utilisant une métrique de pourcentage médiocre)</span><span class="sxs-lookup"><span data-stu-id="62b20-124">The [Device Report in Lync Server 2013](lync-server-2013-device-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="62b20-125">[Rapport synthèse sur la qualité multimédia dans Lync Server 2013](lync-server-2013-media-quality-summary-report.md) (en cliquant sur le volume des appels ou sur le pourcentage d’appels médiocre)</span><span class="sxs-lookup"><span data-stu-id="62b20-125">The [Media Quality Summary Report in Lync Server 2013](lync-server-2013-media-quality-summary-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="62b20-126">Rapport sur les [performances du serveur dans Lync Server 2013](lync-server-2013-server-performance-report.md) (en cliquant sur le volume des appels ou en utilisant une métrique de pourcentage médiocre)</span><span class="sxs-lookup"><span data-stu-id="62b20-126">The [Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

<span data-ttu-id="62b20-127">Dans le rapport de la liste d’appels, vous pouvez accéder au [rapport Détails des appels dans Lync Server 2013](lync-server-2013-call-detail-report.md) en cliquant sur la métrique de détail.</span><span class="sxs-lookup"><span data-stu-id="62b20-127">From within the Call List Report you can access the [Call Detail Report in Lync Server 2013](lync-server-2013-call-detail-report.md) by clicking the Detail metric.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-list-report"></a><span data-ttu-id="62b20-128">Utilisation optimale du rapport Liste des appels</span><span class="sxs-lookup"><span data-stu-id="62b20-128">Making the Best Use of the Call List Report</span></span>

<span data-ttu-id="62b20-129">Si vous ne vous souvenez pas de la signification de certaines des mesures du rapport Liste des appels (par exemple, Ratio de la durée du basculement vocal), maintenez le pointeur de la souris sur l’étiquette de la mesure ; une info-bulle s’affiche et fournit une brève description de la mesure.</span><span class="sxs-lookup"><span data-stu-id="62b20-129">If you can't remember what some of the Call List Report metrics (such as Ratio voice switch time) actually measure, hold your mouse over the metric label; a tool tip will then appear giving you a brief description of the metric.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="62b20-130">Filtres</span><span class="sxs-lookup"><span data-stu-id="62b20-130">Filters</span></span>

<span data-ttu-id="62b20-p103">Aucun. Il est impossible de filtrer le rapport de liste d’appels.</span><span class="sxs-lookup"><span data-stu-id="62b20-p103">None. You cannot filter the Call List Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="62b20-133">Mesures</span><span class="sxs-lookup"><span data-stu-id="62b20-133">Metrics</span></span>

<span data-ttu-id="62b20-134">Le tableau qui suit répertorie les informations fournies dans le rapport de liste d’appels pour chaque appel.</span><span class="sxs-lookup"><span data-stu-id="62b20-134">The following table lists the information provided in the Call List Report for each call.</span></span>

### <a name="call-list-report-metrics"></a><span data-ttu-id="62b20-135">Mesures du rapport de liste d’appels</span><span class="sxs-lookup"><span data-stu-id="62b20-135">Call List Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62b20-136">Nom</span><span class="sxs-lookup"><span data-stu-id="62b20-136">Name</span></span></th>
<th><span data-ttu-id="62b20-137">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="62b20-137">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="62b20-138">Description</span><span class="sxs-lookup"><span data-stu-id="62b20-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62b20-139"><strong>Détails</strong></span><span class="sxs-lookup"><span data-stu-id="62b20-139"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="62b20-140">Non</span><span class="sxs-lookup"><span data-stu-id="62b20-140">No</span></span></p></td>
<td><p><span data-ttu-id="62b20-141">Lorsque vous cliquez sur cet élément, le rapport affiche des informations supplémentaires sur l’appel.</span><span class="sxs-lookup"><span data-stu-id="62b20-141">When you click this item, the report shows additional information on the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62b20-142"><strong>Appelant</strong></span><span class="sxs-lookup"><span data-stu-id="62b20-142"><strong>Caller</strong></span></span></p></td>
<td><p><span data-ttu-id="62b20-143">Oui</span><span class="sxs-lookup"><span data-stu-id="62b20-143">Yes</span></span></p></td>
<td><p><span data-ttu-id="62b20-144">Adresse IP de la personne ayant initié l’appel.</span><span class="sxs-lookup"><span data-stu-id="62b20-144">SIP address of the person who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62b20-145"><strong>Appelé</strong></span><span class="sxs-lookup"><span data-stu-id="62b20-145"><strong>Callee</strong></span></span></p></td>
<td><p><span data-ttu-id="62b20-146">Oui</span><span class="sxs-lookup"><span data-stu-id="62b20-146">Yes</span></span></p></td>
<td><p><span data-ttu-id="62b20-147">Adresse IP de la personne qui a été appelée.</span><span class="sxs-lookup"><span data-stu-id="62b20-147">SIP address of the person who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62b20-148"><strong>Heure de début</strong></span><span class="sxs-lookup"><span data-stu-id="62b20-148"><strong>Start time</strong></span></span></p></td>
<td><p><span data-ttu-id="62b20-149">Oui</span><span class="sxs-lookup"><span data-stu-id="62b20-149">Yes</span></span></p></td>
<td><p><span data-ttu-id="62b20-150">Date et heure de début de l’appel.</span><span class="sxs-lookup"><span data-stu-id="62b20-150">Date and time that the call started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62b20-151"><strong>Heure de fin</strong></span><span class="sxs-lookup"><span data-stu-id="62b20-151"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="62b20-152">Oui</span><span class="sxs-lookup"><span data-stu-id="62b20-152">Yes</span></span></p></td>
<td><p><span data-ttu-id="62b20-153">Date et heure de fin de l’appel.</span><span class="sxs-lookup"><span data-stu-id="62b20-153">Date and time that the call ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62b20-154"><strong>Agent utilisateur de l’appelant</strong></span><span class="sxs-lookup"><span data-stu-id="62b20-154"><strong>Caller user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="62b20-155">Oui</span><span class="sxs-lookup"><span data-stu-id="62b20-155">Yes</span></span></p></td>
<td><p><span data-ttu-id="62b20-156">Logiciel utilisé par le point de terminaison de la personne ayant initié l’appel.</span><span class="sxs-lookup"><span data-stu-id="62b20-156">Software used by the endpoint of the person who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62b20-157"><strong>Agent utilisateur de l’appelé</strong></span><span class="sxs-lookup"><span data-stu-id="62b20-157"><strong>Callee user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="62b20-158">Oui</span><span class="sxs-lookup"><span data-stu-id="62b20-158">Yes</span></span></p></td>
<td><p><span data-ttu-id="62b20-159">Logiciel utilisé par le point de terminaison de la personne qui a été appelée.</span><span class="sxs-lookup"><span data-stu-id="62b20-159">Software used by the endpoint of the person who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62b20-160"><strong>Boucle (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="62b20-160"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="62b20-161">Oui</span><span class="sxs-lookup"><span data-stu-id="62b20-161">Yes</span></span></p></td>
<td><p><span data-ttu-id="62b20-p104">Temps moyen (en millisecondes) nécessaire à un package RTP (Real-Time Transport Protocol) pour effectuer un aller-retour vers un autre point de terminaison. Des boucles de 100 millisecondes ou moins sont considérées qualitativement acceptables.</span><span class="sxs-lookup"><span data-stu-id="62b20-p104">Average amount of (in milliseconds) required for a real-time transport protocol (RTP) packet to travel to another endpoint and then back. Round-trip times of 100 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="62b20-p105">Des boucles avec des temps plus élevés peuvent être causées par le routage international des appels, une mauvaise configuration du routage ou un serveur multimédia surchargé. Les temps d’aller-retour élevés créent des difficultés dans le cadre de conversations audio bidirectionnelles réalisées en temps réel.</span><span class="sxs-lookup"><span data-stu-id="62b20-p105">High round-trip values can be caused by international call routing, a routing misconfiguration, or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62b20-166"><strong>Dégradation (MOS)</strong></span><span class="sxs-lookup"><span data-stu-id="62b20-166"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="62b20-167">Oui</span><span class="sxs-lookup"><span data-stu-id="62b20-167">Yes</span></span></p></td>
<td><p><span data-ttu-id="62b20-168">Taux moyen de dégradation de la note moyenne d’opinion (MOS) observé au cours d’un appel.</span><span class="sxs-lookup"><span data-stu-id="62b20-168">Average amount of mean opinion score (MOS) degradation experienced during a call.</span></span> <span data-ttu-id="62b20-169">Les valeurs de dégradation peuvent aller de 0,0 (la plus faible) à 5,0 (la plus élevée).</span><span class="sxs-lookup"><span data-stu-id="62b20-169">Degradation values can range from a low of 0.0 to a high of 5.0.</span></span> <span data-ttu-id="62b20-170">Une valeur de 0,5 ou moins signifie une dégradation acceptable.</span><span class="sxs-lookup"><span data-stu-id="62b20-170">A value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="62b20-171">Traditionnellement, les notes moyennes d’opinion sont calculées en demandant aux utilisateurs d’évaluer la qualité d’un appel sur une échelle de 1 à 5.</span><span class="sxs-lookup"><span data-stu-id="62b20-171">Historically, mean options scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="62b20-172">Dans Lync Server, Lync Server utilise un ensemble d’algorithmes pour prévoir la façon dont les utilisateurs auraient noté un appel.</span><span class="sxs-lookup"><span data-stu-id="62b20-172">In Lync Server, Lync Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="62b20-p107">Les valeurs de dégradation élevées peuvent provenir d’une congestion, d’un dépassement de la bande passante disponible, d’une congestion/interférence dans la liaison sans fil ou bien d’un serveur multimédia ou d’un point de terminaison surchargé, ce qui se traduit par une distorsion ou une perte de l’audio.</span><span class="sxs-lookup"><span data-stu-id="62b20-p107">High degradation values can be caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62b20-175"><strong>Perte de paquets</strong></span><span class="sxs-lookup"><span data-stu-id="62b20-175"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="62b20-176">Oui</span><span class="sxs-lookup"><span data-stu-id="62b20-176">Yes</span></span></p></td>
<td><p><span data-ttu-id="62b20-p108">Taux moyen de pertes de paquets RTP. (La perte de paquets survient lorsque des paquets RTP, protocole employé pour la transmission audio et vidéo sur Internet, n’atteignent pas leur point de destination.) Les valeurs de perte élevées peuvent provenir d’une congestion, d’un dépassement de la bande passante disponible, d’une congestion/interférence dans la liaison sans fil ou d’un serveur multimédia surchargé, ce qui se traduit par une distorsion ou une perte de l’audio.</span><span class="sxs-lookup"><span data-stu-id="62b20-p108">Average rate of RTP packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62b20-180"><strong>Gigue</strong></span><span class="sxs-lookup"><span data-stu-id="62b20-180"><strong>Jitter</strong></span></span></p></td>
<td><p><span data-ttu-id="62b20-181">Oui</span><span class="sxs-lookup"><span data-stu-id="62b20-181">Yes</span></span></p></td>
<td><p><span data-ttu-id="62b20-182">Gigue moyenne détectée entre les arrivées de paquets RTP.</span><span class="sxs-lookup"><span data-stu-id="62b20-182">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="62b20-183">(Gigue est une mesure du &quot; shakiness &quot; d’un appel.) Les valeurs de gigue élevée sont généralement provoquées par une congestion ou un serveur multimédia surchargé, ce qui a pour effet de déformer ou de perdre du son.</span><span class="sxs-lookup"><span data-stu-id="62b20-183">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62b20-184"><strong>Taux de masquage de la réparation</strong></span><span class="sxs-lookup"><span data-stu-id="62b20-184"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="62b20-185">Oui</span><span class="sxs-lookup"><span data-stu-id="62b20-185">Yes</span></span></p></td>
<td><p><span data-ttu-id="62b20-p110">Ratio moyen d’échantillons audio masqués par rapport au nombre total d’échantillons. (Un échantillon audio masqué est une technique employée pour adoucir les effets de transition violents généralement causés par des paquets réseau perdus.) Des valeurs élevées indiquent des niveaux importants de masquage des pertes appliqués suite à la perte de paquets ou des phénomènes de gigue. Elles se traduisent par une distorsion ou une perte de l’audio.</span><span class="sxs-lookup"><span data-stu-id="62b20-p110">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62b20-188"><strong>Taux d’étirement de la réparation</strong></span><span class="sxs-lookup"><span data-stu-id="62b20-188"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="62b20-189">Oui</span><span class="sxs-lookup"><span data-stu-id="62b20-189">Yes</span></span></p></td>
<td><p><span data-ttu-id="62b20-p111">Ratio moyen d’échantillons audio étirés par rapport au nombre total d’échantillons. (Un échantillon audio étiré est un composant audio qui a été étendu dans le but de maintenir la qualité des appels lorsqu’un paquet réseau perdu est détecté.) Les valeurs élevées indiquent l’existence de niveaux importants d’étirement d’échantillons dus au phénomène de gigue, ce qui se traduit par un effet de robotisation ou de distorsion de l’audio.</span><span class="sxs-lookup"><span data-stu-id="62b20-p111">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62b20-192"><strong>Taux de compression de la réparation</strong></span><span class="sxs-lookup"><span data-stu-id="62b20-192"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="62b20-193">Oui</span><span class="sxs-lookup"><span data-stu-id="62b20-193">Yes</span></span></p></td>
<td><p><span data-ttu-id="62b20-p112">Ratio moyen d’échantillons audio compressés par rapport au nombre total d’échantillons. (Un échantillon audio compressé est un composant audio qui a été compressé dans le but de maintenir la qualité des appels lorsqu’un paquet réseau perdu est détecté.) Les valeurs élevées indiquent l’existence de niveaux importants de compression d’échantillons dus au phénomène de gigue, ce qui se traduit par un effet d’accélération ou de distorsion de l’audio.</span><span class="sxs-lookup"><span data-stu-id="62b20-p112">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62b20-196"><strong>Connectivité</strong></span><span class="sxs-lookup"><span data-stu-id="62b20-196"><strong>Connectivity</strong></span></span></p></td>
<td><p><span data-ttu-id="62b20-197">Oui</span><span class="sxs-lookup"><span data-stu-id="62b20-197">Yes</span></span></p></td>
<td><p><span data-ttu-id="62b20-p113">Type de liaison de communication sans fil. Il s’agit en général de l’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="62b20-p113">Type of wireless communication link. Typically, this is one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="62b20-200">Relais</span><span class="sxs-lookup"><span data-stu-id="62b20-200">Relay</span></span></p></li>
<li><p><span data-ttu-id="62b20-201">Direct</span><span class="sxs-lookup"><span data-stu-id="62b20-201">Direct</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="62b20-202">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="62b20-202">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

