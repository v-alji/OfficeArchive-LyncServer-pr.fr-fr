---
title: 'Lync Server 2013 : Table Conference'
description: 'Lync Server 2013 : table de conférences.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference table
ms:assetid: 2a2c327c-4719-42dc-a3bb-6dbc0864d9af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425762(v=OCS.15)
ms:contentKeyID: 48183700
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 565725b527399cb3be55c649dfd74d8bcb5f13a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434465"
---
# <a name="conference-table-in-lync-server-2013"></a><span data-ttu-id="fc464-103">Table Conference dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc464-103">Conference table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fc464-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fc464-104">

<span> </span></span></span>

<span data-ttu-id="fc464-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="fc464-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="fc464-106">La table Conference est une table de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fc464-106">The Conference table is a supporting table.</span></span> <span data-ttu-id="fc464-107">Chaque enregistrement représente une conférence ou une session d’égal à égal.</span><span class="sxs-lookup"><span data-stu-id="fc464-107">Each record represents one conference or peer-to-peer session.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc464-108"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="fc464-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="fc464-109"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="fc464-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="fc464-110"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="fc464-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="fc464-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="fc464-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc464-112"><strong>ConferenceKey</strong></span><span class="sxs-lookup"><span data-stu-id="fc464-112"><strong>ConferenceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="fc464-113">int</span><span class="sxs-lookup"><span data-stu-id="fc464-113">int</span></span></p></td>
<td><p><span data-ttu-id="fc464-114">Principal</span><span class="sxs-lookup"><span data-stu-id="fc464-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="fc464-115">Numéro unique identifiant cet enregistrement de conférence.</span><span class="sxs-lookup"><span data-stu-id="fc464-115">Unique number identifying this conference record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc464-116"><strong>ConfURI</strong></span><span class="sxs-lookup"><span data-stu-id="fc464-116"><strong>ConfURI</strong></span></span></p></td>
<td><p><span data-ttu-id="fc464-117">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="fc464-117">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="fc464-118">différent</span><span class="sxs-lookup"><span data-stu-id="fc464-118">unique</span></span></p></td>
<td><p><span data-ttu-id="fc464-119">URI de conférence s’il s’agit d’une conférence, ou DialogID s’il s’agit d’une session d’égal à égal.</span><span class="sxs-lookup"><span data-stu-id="fc464-119">Conference URI if this is a conference, or DialogID if this is a peer-to-peer session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc464-120"><strong>1018</strong></span><span class="sxs-lookup"><span data-stu-id="fc464-120"><strong>Checksum</strong></span></span></p></td>
<td><p><span data-ttu-id="fc464-121">int</span><span class="sxs-lookup"><span data-stu-id="fc464-121">int</span></span></p></td>
<td><p><span data-ttu-id="fc464-122">index</span><span class="sxs-lookup"><span data-stu-id="fc464-122">index</span></span></p></td>
<td><p><span data-ttu-id="fc464-123">Checksum de l’URI de conférence.</span><span class="sxs-lookup"><span data-stu-id="fc464-123">Checksum of the conference URI.</span></span> <span data-ttu-id="fc464-124">Cette opération est utilisée en interne.</span><span class="sxs-lookup"><span data-stu-id="fc464-124">This is used internally.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc464-125"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="fc464-125"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="fc464-126">DateHeure</span><span class="sxs-lookup"><span data-stu-id="fc464-126">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc464-127">Pour un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="fc464-127">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="fc464-128">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fc464-128">


</div>

<span> </span>

</div>

</div>

</span></span></div>

