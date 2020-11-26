---
title: 'Lync Server 2013 : Table Server'
description: 'Tableau Lync Server 2013 : serveur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server table
ms:assetid: 9af89d08-d35a-48e8-b56d-6df292f973cc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398801(v=OCS.15)
ms:contentKeyID: 48184890
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 00990a91aec64063480d96a16380171990913ad4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441850"
---
# <a name="server-table-in-lync-server-2013"></a><span data-ttu-id="ed148-103">Table Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ed148-103">Server table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ed148-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ed148-104">

<span> </span></span></span>

<span data-ttu-id="ed148-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="ed148-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="ed148-106">La table serveur est une table de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ed148-106">The Server table is a supporting table.</span></span> <span data-ttu-id="ed148-107">Chaque enregistrement représente un serveur.</span><span class="sxs-lookup"><span data-stu-id="ed148-107">Each record represents one server.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed148-108"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="ed148-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="ed148-109"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="ed148-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="ed148-110"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="ed148-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="ed148-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="ed148-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed148-112"><strong>ServerKey</strong></span><span class="sxs-lookup"><span data-stu-id="ed148-112"><strong>ServerKey</strong></span></span></p></td>
<td><p><span data-ttu-id="ed148-113">int</span><span class="sxs-lookup"><span data-stu-id="ed148-113">int</span></span></p></td>
<td><p><span data-ttu-id="ed148-114">Principal</span><span class="sxs-lookup"><span data-stu-id="ed148-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="ed148-115">Numéro unique identifiant le serveur.</span><span class="sxs-lookup"><span data-stu-id="ed148-115">Unique number identifying the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed148-116"><strong>FQDNOrIP</strong></span><span class="sxs-lookup"><span data-stu-id="ed148-116"><strong>FQDNOrIP</strong></span></span></p></td>
<td><p><span data-ttu-id="ed148-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="ed148-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ed148-118">index</span><span class="sxs-lookup"><span data-stu-id="ed148-118">index</span></span></p></td>
<td><p><span data-ttu-id="ed148-119">Chaîne d’adresses MAC.</span><span class="sxs-lookup"><span data-stu-id="ed148-119">MAC address string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed148-120"><strong>ServerType</strong></span><span class="sxs-lookup"><span data-stu-id="ed148-120"><strong>ServerType</strong></span></span></p></td>
<td><p><span data-ttu-id="ed148-121">int</span><span class="sxs-lookup"><span data-stu-id="ed148-121">int</span></span></p></td>
<td><p><span data-ttu-id="ed148-122">Externes</span><span class="sxs-lookup"><span data-stu-id="ed148-122">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ed148-123">1 : serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="ed148-123">1: Mediation Server</span></span></p>
<p><span data-ttu-id="ed148-124">2 : service de conférence a/V Server16394 : service32769 Edge A/V : passerelle</span><span class="sxs-lookup"><span data-stu-id="ed148-124">2: A/V Conferencing Server16394: A/V Edge service32769: Gateway</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed148-125"><strong>PoolName</strong></span><span class="sxs-lookup"><span data-stu-id="ed148-125"><strong>PoolName</strong></span></span></p></td>
<td><p><span data-ttu-id="ed148-126">nvarchar</span><span class="sxs-lookup"><span data-stu-id="ed148-126">nvarchar(512)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ed148-127">Regroupement auquel appartient le serveur.</span><span class="sxs-lookup"><span data-stu-id="ed148-127">Pool the server belongs to.</span></span> <span data-ttu-id="ed148-128">Applicable uniquement au serveur de conférence A/V.</span><span class="sxs-lookup"><span data-stu-id="ed148-128">Only applicable for the A/V Conferencing Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed148-129"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="ed148-129"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="ed148-130">DateHeure</span><span class="sxs-lookup"><span data-stu-id="ed148-130">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ed148-131">Pour un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="ed148-131">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ed148-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ed148-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

