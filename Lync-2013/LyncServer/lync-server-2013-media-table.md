---
title: 'Lync Server 2013 : Table Media'
description: 'Tableau Lync Server 2013 : Media.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media table
ms:assetid: 1e1b427f-59b5-4564-bde5-1002a80439ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398268(v=OCS.15)
ms:contentKeyID: 48183568
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31e30d1f91c59b8e3aa7915fc0d513618d0f709f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425674"
---
# <a name="media-table-in-lync-server-2013"></a><span data-ttu-id="f264a-103">Table Media dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f264a-103">Media table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f264a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f264a-104">

<span> </span></span></span>

<span data-ttu-id="f264a-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="f264a-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="f264a-106">Chaque enregistrement représente un type de média utilisé dans une session d’égal à égal.</span><span class="sxs-lookup"><span data-stu-id="f264a-106">Each record represents one media type used in a peer-to-peer session.</span></span> <span data-ttu-id="f264a-107">Une session serait représentée par plusieurs enregistrements dans la table, si plusieurs types de média sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="f264a-107">One session would be represented by multiple records in the table, if more than one media type is used.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f264a-108">La table multimédia ne doit pas être utilisée pour calculer la durée du média pour une session.</span><span class="sxs-lookup"><span data-stu-id="f264a-108">The Media table should not be used to calculate the media duration for a session.</span></span> <span data-ttu-id="f264a-109">Ce tableau contient les détails de signalisation d’échange de médias dans une session.</span><span class="sxs-lookup"><span data-stu-id="f264a-109">This table contains the signaling details of media exchange in a session.</span></span> <span data-ttu-id="f264a-110">L’échange de média est effectué par la demande d’invitation, et la durée de StartTime indique l’heure d’envoi de l’invitation. La durée d’invitation ne correspond pas nécessairement à l’heure de début du média, car le contenu multimédia ne démarre qu’après que la session de la session a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="f264a-110">Media exchange is done by the INVITE request, and StartTime indicates the time that the INVITE was sent out. The invite time does not necessarily mean the media start time, because media starts only after the sessionee accepts the session.</span></span> <span data-ttu-id="f264a-111">Le heure_fin correspond généralement à l’heure de fin de la session.</span><span class="sxs-lookup"><span data-stu-id="f264a-111">The EndTime usually means the end time of this session.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f264a-112">Colonne</span><span class="sxs-lookup"><span data-stu-id="f264a-112">Column</span></span></th>
<th><span data-ttu-id="f264a-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="f264a-113">Data Type</span></span></th>
<th><span data-ttu-id="f264a-114">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="f264a-114">Key/Index</span></span></th>
<th><span data-ttu-id="f264a-115">Détails</span><span class="sxs-lookup"><span data-stu-id="f264a-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f264a-116"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="f264a-116"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f264a-117">DateHeure</span><span class="sxs-lookup"><span data-stu-id="f264a-117">datetime</span></span></p></td>
<td><p><span data-ttu-id="f264a-118">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="f264a-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="f264a-119">Durée de la demande de session.</span><span class="sxs-lookup"><span data-stu-id="f264a-119">Time of session request.</span></span> <span data-ttu-id="f264a-120">Utilisé conjointement avec <strong>SessionIdSeq</strong> pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="f264a-120">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="f264a-121">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f264a-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f264a-122"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="f264a-122"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="f264a-123">int</span><span class="sxs-lookup"><span data-stu-id="f264a-123">int</span></span></p></td>
<td><p><span data-ttu-id="f264a-124">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="f264a-124">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="f264a-125">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="f264a-125">ID number to identify the session.</span></span> <span data-ttu-id="f264a-126">Utilisé conjointement avec <strong>SessionIdTime</strong> pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="f264a-126">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="f264a-127">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f264a-127">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f264a-128"><strong>MediaId</strong></span><span class="sxs-lookup"><span data-stu-id="f264a-128"><strong>MediaId</strong></span></span></p></td>
<td><p><span data-ttu-id="f264a-129">tinyint</span><span class="sxs-lookup"><span data-stu-id="f264a-129">tinyint</span></span></p></td>
<td><p><span data-ttu-id="f264a-130">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="f264a-130">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="f264a-131">Numéro unique identifiant ce type de média.</span><span class="sxs-lookup"><span data-stu-id="f264a-131">Unique number identifying this media type.</span></span> <span data-ttu-id="f264a-132">Pour plus d’informations, reportez-vous <a href="lync-server-2013-medialist-table.md">à la table de médiane dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f264a-132">See the <a href="lync-server-2013-medialist-table.md">MediaList table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f264a-133"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="f264a-133"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f264a-134">DateHeure</span><span class="sxs-lookup"><span data-stu-id="f264a-134">datetime</span></span></p></td>
<td><p><span data-ttu-id="f264a-135">Principal</span><span class="sxs-lookup"><span data-stu-id="f264a-135">Primary</span></span></p></td>
<td><p><span data-ttu-id="f264a-136">Il s’agit du temps d’envoi d’une demande de média et non de l’heure de début réelle du média.</span><span class="sxs-lookup"><span data-stu-id="f264a-136">This is the time that a media request was sent out, not the real media start time.</span></span> <span data-ttu-id="f264a-137"><strong>StartTime</strong> inclut le temps de configuration de la session.</span><span class="sxs-lookup"><span data-stu-id="f264a-137"><strong>StartTime</strong> includes the session setup time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f264a-138"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="f264a-138"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f264a-139">DateHeure</span><span class="sxs-lookup"><span data-stu-id="f264a-139">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f264a-140">Il s’agit de l’heure de fin de la session.</span><span class="sxs-lookup"><span data-stu-id="f264a-140">This is the end time of the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f264a-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f264a-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

