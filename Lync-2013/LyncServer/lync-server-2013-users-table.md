---
title: 'Lync Server 2013 : Table Users'
description: 'Tableau Lync Server 2013 : utilisateurs.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Users table
ms:assetid: a8d71373-4b57-4245-9f02-f7fc0d9fcd3c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412791(v=OCS.15)
ms:contentKeyID: 48185032
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b1418e162a04e46ee0dfeca082aa66b0665fc77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436180"
---
# <a name="users-table-in-lync-server-2013"></a><span data-ttu-id="78359-103">Table Users dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="78359-103">Users table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="78359-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="78359-104">

<span> </span></span></span>

<span data-ttu-id="78359-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="78359-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="78359-106">La table users est une table de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="78359-106">The Users table is a supporting table.</span></span> <span data-ttu-id="78359-107">Chaque enregistrement de la table stocke des informations relatives à un utilisateur impliqué dans des appels ou des sessions ayant des enregistrements dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="78359-107">Each record in the table stores information about one user involved in calls or sessions that have records in the database.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78359-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="78359-108">Column</span></span></th>
<th><span data-ttu-id="78359-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="78359-109">Data Type</span></span></th>
<th><span data-ttu-id="78359-110">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="78359-110">Key/Index</span></span></th>
<th><span data-ttu-id="78359-111">Détails</span><span class="sxs-lookup"><span data-stu-id="78359-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78359-112"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="78359-112"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="78359-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="78359-113">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78359-114">Horodatage pour un usage interne.</span><span class="sxs-lookup"><span data-stu-id="78359-114">Time stamp for internal use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78359-115"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="78359-115"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="78359-116">int</span><span class="sxs-lookup"><span data-stu-id="78359-116">int</span></span></p></td>
<td><p><span data-ttu-id="78359-117">Principal</span><span class="sxs-lookup"><span data-stu-id="78359-117">Primary</span></span></p></td>
<td><p><span data-ttu-id="78359-118">Numéro unique identifiant cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78359-118">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78359-119"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="78359-119"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="78359-120">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="78359-120">nvarchar(450)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="78359-121">URI de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78359-121">User URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78359-122"><strong>IDClient</strong></span><span class="sxs-lookup"><span data-stu-id="78359-122"><strong>TenantId</strong></span></span></p></td>
<td><p><span data-ttu-id="78359-123">int</span><span class="sxs-lookup"><span data-stu-id="78359-123">int</span></span></p></td>
<td><p><span data-ttu-id="78359-124">Externes</span><span class="sxs-lookup"><span data-stu-id="78359-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78359-125">ID de client de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78359-125">This user’s Tenant ID.</span></span> <span data-ttu-id="78359-126">Pour plus d’informations, voir la <a href="lync-server-2013-tenants-table.md">table locataires dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78359-126">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78359-127"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="78359-127"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="78359-128">int</span><span class="sxs-lookup"><span data-stu-id="78359-128">int</span></span></p></td>
<td><p><span data-ttu-id="78359-129">Externes</span><span class="sxs-lookup"><span data-stu-id="78359-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78359-130">Type d’URI de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78359-130">This user’s URI type.</span></span> <span data-ttu-id="78359-131">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78359-131">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="78359-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="78359-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

