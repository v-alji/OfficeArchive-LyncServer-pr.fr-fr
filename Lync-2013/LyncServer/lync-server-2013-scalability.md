---
title: Évolutivité de Lync Server 2013
description: Extensibilité de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scalability
ms:assetid: 46fa0cb5-1507-4a12-ad3f-ba64585e2dc4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg417160(v=OCS.15)
ms:contentKeyID: 48183995
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28cd5820755ffd1eb863ed6f2369b5756a7ae3f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442116"
---
# <a name="scalability-with-lync-server-2013"></a><span data-ttu-id="1d59f-103">Évolutivité avec Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1d59f-103">Scalability with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1d59f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1d59f-104">

<span> </span></span></span>

<span data-ttu-id="1d59f-105">_**Dernière modification de la rubrique :** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="1d59f-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="1d59f-106">Lync Server est disponible en deux éditions, Enterprise Edition et Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="1d59f-106">Lync Server is offered in two editions, Enterprise Edition and Standard Edition.</span></span> <span data-ttu-id="1d59f-107">Les différentes éditions sont principalement destinées aux différentes tailles d’organisations.</span><span class="sxs-lookup"><span data-stu-id="1d59f-107">The different editions are intended primarily for different sizes of organizations.</span></span> <span data-ttu-id="1d59f-108">Comme indiqué dans le tableau suivant, les deux éditions prennent en charge toutes les fonctionnalités de toutes les charges de travail, à l’exception de haute disponibilité et de récupération d’urgence.</span><span class="sxs-lookup"><span data-stu-id="1d59f-108">As shown in the following table, both editions support all functionality in all workloads, except for high availability and disaster recovery.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1d59f-109">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="1d59f-109">Feature</span></span></th>
<th><span data-ttu-id="1d59f-110">Prise en charge dans l’édition Enterprise ?</span><span class="sxs-lookup"><span data-stu-id="1d59f-110">Supported in Enterprise Edition?</span></span></th>
<th><span data-ttu-id="1d59f-111">Prise en charge dans les éditions standard ?</span><span class="sxs-lookup"><span data-stu-id="1d59f-111">Supported in Standard Edition?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d59f-112">Messagerie instantanée et présence</span><span class="sxs-lookup"><span data-stu-id="1d59f-112">Instant messaging (IM) and presence</span></span></p></td>
<td><p><span data-ttu-id="1d59f-113">Oui</span><span class="sxs-lookup"><span data-stu-id="1d59f-113">Yes</span></span></p></td>
<td><p><span data-ttu-id="1d59f-114">Oui</span><span class="sxs-lookup"><span data-stu-id="1d59f-114">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d59f-115">Conférence</span><span class="sxs-lookup"><span data-stu-id="1d59f-115">Conferencing</span></span></p></td>
<td><p><span data-ttu-id="1d59f-116">Oui</span><span class="sxs-lookup"><span data-stu-id="1d59f-116">Yes</span></span></p></td>
<td><p><span data-ttu-id="1d59f-117">Oui</span><span class="sxs-lookup"><span data-stu-id="1d59f-117">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d59f-118">Conférence A/V</span><span class="sxs-lookup"><span data-stu-id="1d59f-118">A/V conferencing</span></span></p></td>
<td><p><span data-ttu-id="1d59f-119">Oui</span><span class="sxs-lookup"><span data-stu-id="1d59f-119">Yes</span></span></p></td>
<td><p><span data-ttu-id="1d59f-120">Oui</span><span class="sxs-lookup"><span data-stu-id="1d59f-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d59f-121">Conférence rendez-vous</span><span class="sxs-lookup"><span data-stu-id="1d59f-121">Dial-in conferencing</span></span></p></td>
<td><p><span data-ttu-id="1d59f-122">Oui</span><span class="sxs-lookup"><span data-stu-id="1d59f-122">Yes</span></span></p></td>
<td><p><span data-ttu-id="1d59f-123">Oui</span><span class="sxs-lookup"><span data-stu-id="1d59f-123">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d59f-124">Voix Entreprise</span><span class="sxs-lookup"><span data-stu-id="1d59f-124">Enterprise Voice</span></span></p></td>
<td><p><span data-ttu-id="1d59f-125">Oui</span><span class="sxs-lookup"><span data-stu-id="1d59f-125">Yes</span></span></p></td>
<td><p><span data-ttu-id="1d59f-126">Oui</span><span class="sxs-lookup"><span data-stu-id="1d59f-126">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d59f-127">La virtualisation</span><span class="sxs-lookup"><span data-stu-id="1d59f-127">Virtualization</span></span></p></td>
<td><p><span data-ttu-id="1d59f-128">Oui</span><span class="sxs-lookup"><span data-stu-id="1d59f-128">Yes</span></span></p></td>
<td><p><span data-ttu-id="1d59f-129">Oui</span><span class="sxs-lookup"><span data-stu-id="1d59f-129">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d59f-130">Haute disponibilité, basculement et reprise après sinistre</span><span class="sxs-lookup"><span data-stu-id="1d59f-130">High availability, failover, and disaster recovery</span></span></p></td>
<td><p><span data-ttu-id="1d59f-131">Oui</span><span class="sxs-lookup"><span data-stu-id="1d59f-131">Yes</span></span></p></td>
<td><p><span data-ttu-id="1d59f-132">Non</span><span class="sxs-lookup"><span data-stu-id="1d59f-132">No</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1d59f-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1d59f-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

