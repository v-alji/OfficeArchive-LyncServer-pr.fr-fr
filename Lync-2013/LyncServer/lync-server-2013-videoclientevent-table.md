---
title: 'Lync Server 2013 : Table VideoClientEvent'
description: 'Tableau Lync Server 2013 : VideoClientEvent'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoClientEvent table
ms:assetid: e8ab963b-fe1d-45b3-b9bd-66a5f44c1629
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399039(v=OCS.15)
ms:contentKeyID: 48185891
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ae73ac2548e838241febe60a2d31f80983b01de5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395192"
---
# <a name="videoclientevent-table-in-lync-server-2013"></a><span data-ttu-id="97c4e-103">Table VideoClientEvent dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97c4e-103">VideoClientEvent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="97c4e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="97c4e-104">

<span> </span></span></span>

<span data-ttu-id="97c4e-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="97c4e-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="97c4e-106">Chaque enregistrement contient un événement client pour un point de terminaison dans un appel vidéo.</span><span class="sxs-lookup"><span data-stu-id="97c4e-106">Each record contains client event for one endpoint in a video call.</span></span> <span data-ttu-id="97c4e-107">En règle générale, un appel possède deux enregistrements, un pour l’appelant et un pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="97c4e-107">Usually, one call has two records, one for caller and one for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="97c4e-108"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="97c4e-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="97c4e-109"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="97c4e-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="97c4e-110"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="97c4e-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="97c4e-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="97c4e-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97c4e-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="97c4e-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="97c4e-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="97c4e-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="97c4e-114">Principal</span><span class="sxs-lookup"><span data-stu-id="97c4e-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="97c4e-115">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="97c4e-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97c4e-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="97c4e-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="97c4e-117">int</span><span class="sxs-lookup"><span data-stu-id="97c4e-117">int</span></span></p></td>
<td><p><span data-ttu-id="97c4e-118">Principal</span><span class="sxs-lookup"><span data-stu-id="97c4e-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="97c4e-119">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="97c4e-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97c4e-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="97c4e-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="97c4e-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="97c4e-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="97c4e-122">Principal</span><span class="sxs-lookup"><span data-stu-id="97c4e-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="97c4e-123">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="97c4e-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97c4e-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="97c4e-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="97c4e-125">bit</span><span class="sxs-lookup"><span data-stu-id="97c4e-125">bit</span></span></p></td>
<td><p><span data-ttu-id="97c4e-126">Principal</span><span class="sxs-lookup"><span data-stu-id="97c4e-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="97c4e-127">0 : données du destinataire</span><span class="sxs-lookup"><span data-stu-id="97c4e-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="97c4e-128">1 : données de l’appelant</span><span class="sxs-lookup"><span data-stu-id="97c4e-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97c4e-129"><strong>NetworkBandwidthLowEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="97c4e-129"><strong>NetworkBandwidthLowEventRatio</strong></span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p><span data-ttu-id="97c4e-130">Pourcentage de session de déclenchement de l’événement LowBandwidth pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="97c4e-130">Percentage of session the LowBandwidth event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="97c4e-131">La bande passante disponible est insuffisante pour obtenir une utilisation vocale acceptable.</span><span class="sxs-lookup"><span data-stu-id="97c4e-131">The available bandwidth is insufficient for an acceptable voice experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97c4e-132"><strong>NetworkReceiveQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="97c4e-132"><strong>NetworkReceiveQualityEventRatio</strong></span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p><span data-ttu-id="97c4e-133">Pourcentage de session de déclenchement de l’événement ReceiveSendQuality pour l’état « incorrect ».</span><span class="sxs-lookup"><span data-stu-id="97c4e-133">Percentage of session the ReceiveSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="97c4e-134">La qualité du réseau en termes de gigue ou de perte de paquets est sévère et a un impact sur la qualité du son reçu.</span><span class="sxs-lookup"><span data-stu-id="97c4e-134">Network quality in terms of jitter or packet loss is severe and impacts the quality of audio being received.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="97c4e-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="97c4e-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

