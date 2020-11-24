---
title: 'Lync Server 2013 : tblScopePrincipal'
description: 'Lync Server 2013 : tblScopePrincipal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblScopePrincipal
ms:assetid: 422d6c7f-7ba7-4dd4-bacc-95ace47959ff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558639(v=OCS.15)
ms:contentKeyID: 48184009
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63315f8525e5c2f05fe54a0f9ed9e8a97b9e8bce
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393905"
---
# <a name="tblscopeprincipal-in-lync-server-2013"></a><span data-ttu-id="d48cb-103">tblScopePrincipal dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d48cb-103">tblScopePrincipal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d48cb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d48cb-104">

<span> </span></span></span>

<span data-ttu-id="d48cb-105">_**Dernière modification de la rubrique :** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="d48cb-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="d48cb-106">tblScopePrincipal contient les étendues attribuées aux nœuds.</span><span class="sxs-lookup"><span data-stu-id="d48cb-106">tblScopePrincipal contains scopes assigned to nodes.</span></span>

### <a name="columns"></a><span data-ttu-id="d48cb-107">Celles</span><span class="sxs-lookup"><span data-stu-id="d48cb-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d48cb-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="d48cb-108">Column</span></span></th>
<th><span data-ttu-id="d48cb-109">Type</span><span class="sxs-lookup"><span data-stu-id="d48cb-109">Type</span></span></th>
<th><span data-ttu-id="d48cb-110">Description</span><span class="sxs-lookup"><span data-stu-id="d48cb-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d48cb-111">scopeNodeID</span><span class="sxs-lookup"><span data-stu-id="d48cb-111">scopeNodeID</span></span></p></td>
<td><p><span data-ttu-id="d48cb-112">ent, non null</span><span class="sxs-lookup"><span data-stu-id="d48cb-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="d48cb-113">ID du nœud auquel s’applique l’étendue.</span><span class="sxs-lookup"><span data-stu-id="d48cb-113">Node ID that the scope applies to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d48cb-114">scopePrinID</span><span class="sxs-lookup"><span data-stu-id="d48cb-114">scopePrinID</span></span></p></td>
<td><p><span data-ttu-id="d48cb-115">ent, non null</span><span class="sxs-lookup"><span data-stu-id="d48cb-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="d48cb-116">ID du principal.</span><span class="sxs-lookup"><span data-stu-id="d48cb-116">Principal ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d48cb-117">scopeIsDenied</span><span class="sxs-lookup"><span data-stu-id="d48cb-117">scopeIsDenied</span></span></p></td>
<td><p><span data-ttu-id="d48cb-118">bit, pas null</span><span class="sxs-lookup"><span data-stu-id="d48cb-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="d48cb-119">True si le type d’étendue est Deny ; False si Allow.</span><span class="sxs-lookup"><span data-stu-id="d48cb-119">True if type of scope is Deny; False if Allow.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d48cb-120">scopeUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="d48cb-120">scopeUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="d48cb-121">ent, non null</span><span class="sxs-lookup"><span data-stu-id="d48cb-121">int, not null</span></span></p></td>
<td><p><span data-ttu-id="d48cb-122">ID de l’élément principal qui a mis à jour cette entrée.</span><span class="sxs-lookup"><span data-stu-id="d48cb-122">ID of the principal that last updated this entry.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="d48cb-123">Permettent</span><span class="sxs-lookup"><span data-stu-id="d48cb-123">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d48cb-124">Colonne</span><span class="sxs-lookup"><span data-stu-id="d48cb-124">Column</span></span></th>
<th><span data-ttu-id="d48cb-125">Description</span><span class="sxs-lookup"><span data-stu-id="d48cb-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d48cb-126">&lt;scopeNodeID, scopePrinID&gt;</span><span class="sxs-lookup"><span data-stu-id="d48cb-126">&lt;scopeNodeID, scopePrinID&gt;</span></span></p></td>
<td><p><span data-ttu-id="d48cb-127">Clé primaire.</span><span class="sxs-lookup"><span data-stu-id="d48cb-127">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d48cb-128">scopeNodeID</span><span class="sxs-lookup"><span data-stu-id="d48cb-128">scopeNodeID</span></span></p></td>
<td><p><span data-ttu-id="d48cb-129">Clé étrangère avec recherche dans la table tblNode. nodeID.</span><span class="sxs-lookup"><span data-stu-id="d48cb-129">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d48cb-130">scopePrinID</span><span class="sxs-lookup"><span data-stu-id="d48cb-130">scopePrinID</span></span></p></td>
<td><p><span data-ttu-id="d48cb-131">Clé étrangère avec recherche dans la table tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="d48cb-131">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d48cb-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d48cb-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

