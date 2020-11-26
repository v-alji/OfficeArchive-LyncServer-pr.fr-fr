---
title: 'Lync Server 2013 : Table UserAgent'
description: 'Tableau Lync Server 2013 : UserAgent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserAgent table
ms:assetid: d6bda1c0-b053-457a-9ffa-2ae859788775
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398939(v=OCS.15)
ms:contentKeyID: 48185582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b701d8384313d0267dd566e0c32242f6cc077472
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439127"
---
# <a name="useragent-table-in-lync-server-2013"></a><span data-ttu-id="be3bd-103">Table UserAgent dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="be3bd-103">UserAgent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="be3bd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="be3bd-104">

<span> </span></span></span>

<span data-ttu-id="be3bd-105">_**Dernière modification de la rubrique :** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="be3bd-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="be3bd-106">La table UserAgent est une table qui contient une liste des différents agents utilisateurs ayant participé à des sessions enregistrées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="be3bd-106">The UserAgent table is a supporting table that stores a list of the various user agents that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="be3bd-107">Chaque enregistrement de la table représente un agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="be3bd-107">Each record in the table represents one user agent</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="be3bd-108"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="be3bd-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="be3bd-109"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="be3bd-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="be3bd-110"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="be3bd-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="be3bd-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="be3bd-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be3bd-112"><strong>UserAgentKey</strong></span><span class="sxs-lookup"><span data-stu-id="be3bd-112"><strong>UserAgentKey</strong></span></span></p></td>
<td><p><span data-ttu-id="be3bd-113">int</span><span class="sxs-lookup"><span data-stu-id="be3bd-113">int</span></span></p></td>
<td><p><span data-ttu-id="be3bd-114">Principal</span><span class="sxs-lookup"><span data-stu-id="be3bd-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="be3bd-115">Numéro unique identifiant cet agent utilisateur.</span><span class="sxs-lookup"><span data-stu-id="be3bd-115">Unique number identifying this user agent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be3bd-116"><strong>UserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="be3bd-116"><strong>UserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="be3bd-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="be3bd-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="be3bd-118">Différent</span><span class="sxs-lookup"><span data-stu-id="be3bd-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="be3bd-119">Chaîne de l’agent utilisateur.</span><span class="sxs-lookup"><span data-stu-id="be3bd-119">User Agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be3bd-120"><strong>UAType</strong></span><span class="sxs-lookup"><span data-stu-id="be3bd-120"><strong>UAType</strong></span></span></p></td>
<td><p><span data-ttu-id="be3bd-121">type</span><span class="sxs-lookup"><span data-stu-id="be3bd-121">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="be3bd-122">1 est un serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="be3bd-122">1 is Mediation Server.</span></span></p>
<p><span data-ttu-id="be3bd-123">2 est un serveur de conférence A/V.</span><span class="sxs-lookup"><span data-stu-id="be3bd-123">2 is A/V Conferencing Server.</span></span></p>
<p><span data-ttu-id="be3bd-124">4 est Lync.</span><span class="sxs-lookup"><span data-stu-id="be3bd-124">4 is Lync.</span></span></p>
<p><span data-ttu-id="be3bd-125">8 est le téléphone IP.</span><span class="sxs-lookup"><span data-stu-id="be3bd-125">8 is IP Phone.</span></span></p>
<p><span data-ttu-id="be3bd-126">16 est la console Live Meeting.</span><span class="sxs-lookup"><span data-stu-id="be3bd-126">16 is Live Meeting Console.</span></span></p>
<p><span data-ttu-id="be3bd-127">32 est l’outil de validation du déploiement (DVT).</span><span class="sxs-lookup"><span data-stu-id="be3bd-127">32 is Deployment Validation Tool (DVT).</span></span></p>
<p><span data-ttu-id="be3bd-128">64 est Lync sur les ordinateurs Macintosh.</span><span class="sxs-lookup"><span data-stu-id="be3bd-128">64 is Lync on Macintosh computers.</span></span></p>
<p><span data-ttu-id="be3bd-129">128 est Office Communications Server 2007 R2 attendant.</span><span class="sxs-lookup"><span data-stu-id="be3bd-129">128 is Office Communications Server 2007 R2 Attendant.</span></span></p>
<p><span data-ttu-id="be3bd-130">256 est le service d’annonce de conférence.</span><span class="sxs-lookup"><span data-stu-id="be3bd-130">256 is Conferencing Announcement service.</span></span></p>
<p><span data-ttu-id="be3bd-131">512 est le standard automatique de conférence.</span><span class="sxs-lookup"><span data-stu-id="be3bd-131">512 is Conferencing Auto Attendant.</span></span></p>
<p><span data-ttu-id="be3bd-132">1024 est une application de Response Group.</span><span class="sxs-lookup"><span data-stu-id="be3bd-132">1024 is Response Group application.</span></span></p>
<p><span data-ttu-id="be3bd-133">2048 est hors du contrôle vocal.</span><span class="sxs-lookup"><span data-stu-id="be3bd-133">2048 is Outside Voice Control.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="be3bd-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="be3bd-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

