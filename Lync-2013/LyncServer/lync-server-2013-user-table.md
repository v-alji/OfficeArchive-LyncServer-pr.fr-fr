---
title: 'Lync Server 2013 : Table User'
description: 'Lync Server 2013 : table utilisateur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User table
ms:assetid: 6b52047e-286d-47ab-b7bc-a9b266f62d82
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398505(v=OCS.15)
ms:contentKeyID: 48184437
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 15d1ac08a229f4afea35a2727ef1105a5f24b826
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444167"
---
# <a name="user-table-in-lync-server-2013"></a><span data-ttu-id="cd760-103">Table User dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd760-103">User table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cd760-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cd760-104">

<span> </span></span></span>

<span data-ttu-id="cd760-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="cd760-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="cd760-106">La table utilisateur est une table qui contient une liste des différents utilisateurs ayant participé à des sessions enregistrées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="cd760-106">The User table is a supporting table that stores a list of the various users who have participated in sessions recorded in the database.</span></span> <span data-ttu-id="cd760-107">Chaque enregistrement de la table représente un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cd760-107">Each record in the table represents one user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cd760-108"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="cd760-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="cd760-109"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="cd760-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="cd760-110"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="cd760-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="cd760-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="cd760-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd760-112"><strong>UserKey</strong></span><span class="sxs-lookup"><span data-stu-id="cd760-112"><strong>UserKey</strong></span></span></p></td>
<td><p><span data-ttu-id="cd760-113">int</span><span class="sxs-lookup"><span data-stu-id="cd760-113">int</span></span></p></td>
<td><p><span data-ttu-id="cd760-114">Principal</span><span class="sxs-lookup"><span data-stu-id="cd760-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="cd760-115">Numéro unique identifiant cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cd760-115">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd760-116"><strong>SPAMMEUR</strong></span><span class="sxs-lookup"><span data-stu-id="cd760-116"><strong>URI</strong></span></span></p></td>
<td><p><span data-ttu-id="cd760-117">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="cd760-117">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="cd760-118">Différent</span><span class="sxs-lookup"><span data-stu-id="cd760-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="cd760-119">Chaîne d’URI.</span><span class="sxs-lookup"><span data-stu-id="cd760-119">URI string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd760-120"><strong>URIType</strong></span><span class="sxs-lookup"><span data-stu-id="cd760-120"><strong>URIType</strong></span></span></p></td>
<td><p><span data-ttu-id="cd760-121">int</span><span class="sxs-lookup"><span data-stu-id="cd760-121">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="cd760-122">1 est un type d’URI inconnu.</span><span class="sxs-lookup"><span data-stu-id="cd760-122">1 is unknown URI type.</span></span></p>
<p><span data-ttu-id="cd760-123">2 est l’URI de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cd760-123">2 is user URI.</span></span></p>
<p><span data-ttu-id="cd760-124">4 est un URI de conférence.</span><span class="sxs-lookup"><span data-stu-id="cd760-124">4 is conference URI.</span></span></p>
<p><span data-ttu-id="cd760-125">8 est un URI de téléphone.</span><span class="sxs-lookup"><span data-stu-id="cd760-125">8 is phone URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd760-126"><strong>TenantKey</strong></span><span class="sxs-lookup"><span data-stu-id="cd760-126"><strong>TenantKey</strong></span></span></p></td>
<td><p><span data-ttu-id="cd760-127">int</span><span class="sxs-lookup"><span data-stu-id="cd760-127">int</span></span></p></td>
<td><p><span data-ttu-id="cd760-128">Externes</span><span class="sxs-lookup"><span data-stu-id="cd760-128">Foreign</span></span></p></td>
<td><p><span data-ttu-id="cd760-129">Client de l’utilisateur, référencé dans la table locataire.</span><span class="sxs-lookup"><span data-stu-id="cd760-129">Tenant of the user, referenced from tenant table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd760-130"><strong>LastPoorCallTime</strong></span><span class="sxs-lookup"><span data-stu-id="cd760-130"><strong>LastPoorCallTime</strong></span></span></p></td>
<td><p><span data-ttu-id="cd760-131">DateHeure</span><span class="sxs-lookup"><span data-stu-id="cd760-131">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="cd760-132">Horodatage le plus récent lorsque l’utilisateur avait un appel audio médiocre.</span><span class="sxs-lookup"><span data-stu-id="cd760-132">Latest time stamp when the user had a poor audio call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd760-133"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="cd760-133"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="cd760-134">DateHeure</span><span class="sxs-lookup"><span data-stu-id="cd760-134">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="cd760-135">Pour un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="cd760-135">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="cd760-136">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cd760-136">


</div>

<span> </span>

</div>

</div>

</span></span></div>

