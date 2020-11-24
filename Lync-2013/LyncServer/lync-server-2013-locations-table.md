---
title: 'Lync Server 2013 : Table Locations'
description: 'Tableau Lync Server 2013 : emplacements.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Locations table
ms:assetid: 78dc1b14-5394-4f8e-89d3-4ba593272a04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398596(v=OCS.15)
ms:contentKeyID: 48184579
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9d07b6d3d3820f4efb3310adf0734a7e10c53e6d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395081"
---
# <a name="locations-table-in-lync-server-2013"></a><span data-ttu-id="9c0d6-103">Table Locations dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c0d6-103">Locations table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9c0d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9c0d6-104">

<span> </span></span></span>

<span data-ttu-id="9c0d6-105">_**Dernière modification de la rubrique :** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="9c0d6-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="9c0d6-106">Chaque enregistrement représente une référence d’emplacement dans un appel d’urgence, par exemple un appel E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-106">Each record represents one location reference in an emergency call, like an E9-1-1 call.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c0d6-107">Colonne</span><span class="sxs-lookup"><span data-stu-id="9c0d6-107">Column</span></span></th>
<th><span data-ttu-id="9c0d6-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="9c0d6-108">Data Type</span></span></th>
<th><span data-ttu-id="9c0d6-109">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="9c0d6-109">Key/Index</span></span></th>
<th><span data-ttu-id="9c0d6-110">Détails</span><span class="sxs-lookup"><span data-stu-id="9c0d6-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c0d6-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="9c0d6-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9c0d6-112">DateHeure</span><span class="sxs-lookup"><span data-stu-id="9c0d6-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="9c0d6-113">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="9c0d6-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="9c0d6-114">Durée de la demande de session.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-114">Time of session request.</span></span> <span data-ttu-id="9c0d6-115">Utilisé conjointement avec <strong>SessionIdSeq</strong> pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="9c0d6-116">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9c0d6-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c0d6-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="9c0d6-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="9c0d6-118">int</span><span class="sxs-lookup"><span data-stu-id="9c0d6-118">int</span></span></p></td>
<td><p><span data-ttu-id="9c0d6-119">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="9c0d6-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="9c0d6-120">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-120">ID number to identify the session.</span></span> <span data-ttu-id="9c0d6-121">Utilisé conjointement avec <strong>SessionIdTime</strong> pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="9c0d6-122">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9c0d6-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c0d6-123"><strong>Emplacement</strong></span><span class="sxs-lookup"><span data-stu-id="9c0d6-123"><strong>Location</strong></span></span></p></td>
<td><p><span data-ttu-id="9c0d6-124">nvarchar (max)</span><span class="sxs-lookup"><span data-stu-id="9c0d6-124">nvarchar(max)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9c0d6-125">Emplacement de l’appel d’urgence.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-125">Location of emergency call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9c0d6-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9c0d6-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

