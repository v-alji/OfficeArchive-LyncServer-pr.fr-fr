---
title: 'Lync Server 2013 : table TraceRoute'
description: 'Lync Server 2013 : table TraceRoute.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: TraceRoute table
ms:assetid: b9493cef-6ece-4f13-bf68-dbf132aab4f4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205205(v=OCS.15)
ms:contentKeyID: 48185242
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af33e572065fbab1eaaaef684997e7f95edaed9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440835"
---
# <a name="traceroute-table-in-lync-server-2013"></a><span data-ttu-id="19c52-103">Tableau TraceRoute dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="19c52-103">TraceRoute table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="19c52-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="19c52-104">

<span> </span></span></span>

<span data-ttu-id="19c52-105">_**Dernière modification de la rubrique :** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="19c52-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="19c52-106">La table TraceRoute contient les informations de routage des appels.</span><span class="sxs-lookup"><span data-stu-id="19c52-106">The TraceRoute table contains routing information from calls.</span></span> <span data-ttu-id="19c52-107">Ce tableau a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="19c52-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="19c52-108"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="19c52-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="19c52-109"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="19c52-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="19c52-110"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="19c52-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="19c52-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="19c52-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19c52-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="19c52-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="19c52-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="19c52-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="19c52-114">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="19c52-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="19c52-115">Date et heure de début de l’appel.</span><span class="sxs-lookup"><span data-stu-id="19c52-115">Date and time that the call began.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19c52-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="19c52-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="19c52-117">int</span><span class="sxs-lookup"><span data-stu-id="19c52-117">int</span></span></p></td>
<td><p><span data-ttu-id="19c52-118">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="19c52-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="19c52-119">Identificateur unique permettant de faire la distinction entre plusieurs appels qui pouvaient avoir commencé à la même date et en même temps.</span><span class="sxs-lookup"><span data-stu-id="19c52-119">Unique identifier used to distinguish between multiple calls that might have begun on the same date and at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19c52-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="19c52-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="19c52-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="19c52-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="19c52-122">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="19c52-122">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="19c52-123">Représente le type de ligne vidéo utilisée lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="19c52-123">Represents the type of video line used in the call.</span></span> <span data-ttu-id="19c52-124">Les valeurs autorisées sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="19c52-124">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="19c52-125">0-audio</span><span class="sxs-lookup"><span data-stu-id="19c52-125">0 – Audio</span></span></p></li>
<li><p><span data-ttu-id="19c52-126">1-vidéo</span><span class="sxs-lookup"><span data-stu-id="19c52-126">1 – Video</span></span></p></li>
<li><p><span data-ttu-id="19c52-127">2-vidéo panoramique</span><span class="sxs-lookup"><span data-stu-id="19c52-127">2 – Panoramic video</span></span></p></li>
<li><p><span data-ttu-id="19c52-128">3 – partage de bureau et d’application</span><span class="sxs-lookup"><span data-stu-id="19c52-128">3 – Application/Desktop sharing</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19c52-129"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="19c52-129"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="19c52-130">bit</span><span class="sxs-lookup"><span data-stu-id="19c52-130">bit</span></span></p></td>
<td><p><span data-ttu-id="19c52-131">Principal</span><span class="sxs-lookup"><span data-stu-id="19c52-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="19c52-132">Point de terminaison ayant placé l’appel.</span><span class="sxs-lookup"><span data-stu-id="19c52-132">Endpoint that placed the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19c52-133"><strong>Relais</strong></span><span class="sxs-lookup"><span data-stu-id="19c52-133"><strong>Hop</strong></span></span></p></td>
<td><p><span data-ttu-id="19c52-134">int</span><span class="sxs-lookup"><span data-stu-id="19c52-134">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="19c52-135">Tronçon réseau/</span><span class="sxs-lookup"><span data-stu-id="19c52-135">Network hop/</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19c52-136"><strong>IPAddressKey</strong></span><span class="sxs-lookup"><span data-stu-id="19c52-136"><strong>IPAddressKey</strong></span></span></p></td>
<td><p><span data-ttu-id="19c52-137">int</span><span class="sxs-lookup"><span data-stu-id="19c52-137">int</span></span></p></td>
<td><p><span data-ttu-id="19c52-138">Externes</span><span class="sxs-lookup"><span data-stu-id="19c52-138">Foreign</span></span></p></td>
<td><p><span data-ttu-id="19c52-139">Identificateur unique de l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="19c52-139">Unique identifier for the IP address.</span></span> <span data-ttu-id="19c52-140">Les informations d’adresse IP sont stockées dans la <a href="lync-server-2013-ipaddress-table.md">table IPAddress de Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="19c52-140">IP address information is stored in the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19c52-141"><strong>TEMPS</strong></span><span class="sxs-lookup"><span data-stu-id="19c52-141"><strong>RTT</strong></span></span></p></td>
<td><p><span data-ttu-id="19c52-142">int</span><span class="sxs-lookup"><span data-stu-id="19c52-142">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="19c52-143">Durée de l’aller-retour.</span><span class="sxs-lookup"><span data-stu-id="19c52-143">Roundtrip time.</span></span> <span data-ttu-id="19c52-144">Le temps d’aller-retour mesure la durée pendant laquelle un paquet vocal atteint sa destination et renvoie la notification de réception.</span><span class="sxs-lookup"><span data-stu-id="19c52-144">The roundtrip time measures the amount of time it takes for a voice packet to reach its destination and then send back notification that it was received.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="19c52-145">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="19c52-145">


</div>

<span> </span>

</div>

</div>

</span></span></div>

