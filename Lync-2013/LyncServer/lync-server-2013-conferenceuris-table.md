---
title: 'Lync Server 2013 : Table ConferenceUris'
description: 'Tableau Lync Server 2013 : ConferenceUris'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceUris table
ms:assetid: b1721d52-3c65-45ea-8997-06af8fef93fc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412854(v=OCS.15)
ms:contentKeyID: 48185160
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a142aa9ad1fe4d3ae92aa3e21aa9eee505457cbe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434388"
---
# <a name="conferenceuris-table-in-lync-server-2013"></a><span data-ttu-id="c95f9-103">Table ConferenceUris dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c95f9-103">ConferenceUris table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c95f9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c95f9-104">

<span> </span></span></span>

<span data-ttu-id="c95f9-105">_**Dernière modification de la rubrique :** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="c95f9-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="c95f9-106">La table ConfereneUris est une table qui contient une liste des différents URI de conférence ayant participé à des sessions de conférence enregistrées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="c95f9-106">The ConfereneUris table is a supporting table that stores a list of the various conference URIs that have participated in conference sessions recorded in the database.</span></span> <span data-ttu-id="c95f9-107">Chaque enregistrement de la table représente un URI de conférence.</span><span class="sxs-lookup"><span data-stu-id="c95f9-107">Each record in the table represents one conference URI.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c95f9-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="c95f9-108">Column</span></span></th>
<th><span data-ttu-id="c95f9-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="c95f9-109">Data Type</span></span></th>
<th><span data-ttu-id="c95f9-110">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="c95f9-110">Key/Index</span></span></th>
<th><span data-ttu-id="c95f9-111">Détails</span><span class="sxs-lookup"><span data-stu-id="c95f9-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c95f9-112"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="c95f9-112"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="c95f9-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="c95f9-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="c95f9-114">Principal</span><span class="sxs-lookup"><span data-stu-id="c95f9-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="c95f9-115">Date et heure d’utilisation internes.</span><span class="sxs-lookup"><span data-stu-id="c95f9-115">Time stamp, Internal used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c95f9-116"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="c95f9-116"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="c95f9-117">int</span><span class="sxs-lookup"><span data-stu-id="c95f9-117">int</span></span></p></td>
<td><p><span data-ttu-id="c95f9-118">Principal</span><span class="sxs-lookup"><span data-stu-id="c95f9-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="c95f9-119">Numéro unique identifiant cet URI de conférence.</span><span class="sxs-lookup"><span data-stu-id="c95f9-119">Unique number identifying this conference URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c95f9-120"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="c95f9-120"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="c95f9-121">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="c95f9-121">nvarchar(450)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c95f9-122">URI de conférence.</span><span class="sxs-lookup"><span data-stu-id="c95f9-122">Conference URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c95f9-123"><strong>1018</strong></span><span class="sxs-lookup"><span data-stu-id="c95f9-123"><strong>Checksum</strong></span></span></p></td>
<td><p><span data-ttu-id="c95f9-124">int</span><span class="sxs-lookup"><span data-stu-id="c95f9-124">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c95f9-125">Checksum de ConferenceUri.</span><span class="sxs-lookup"><span data-stu-id="c95f9-125">Checksum of ConferenceUri.</span></span> <span data-ttu-id="c95f9-126">Permet d’augmenter la vitesse de recherche de la base de données.</span><span class="sxs-lookup"><span data-stu-id="c95f9-126">Used to increases the speed of database searches.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c95f9-127"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="c95f9-127"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="c95f9-128">int</span><span class="sxs-lookup"><span data-stu-id="c95f9-128">int</span></span></p></td>
<td><p><span data-ttu-id="c95f9-129">Externes</span><span class="sxs-lookup"><span data-stu-id="c95f9-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c95f9-130">Type d’URI (par exemple, conf : chat pour une conférence par messagerie instantanée, ou conf : audio-vidéo pour les conférences audio/vidéo).</span><span class="sxs-lookup"><span data-stu-id="c95f9-130">URI type, such as conf:chat for IM conference, or conf:audio-video for audio/video conference.</span></span> <span data-ttu-id="c95f9-131">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans la table Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="c95f9-131">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> table for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c95f9-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c95f9-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

