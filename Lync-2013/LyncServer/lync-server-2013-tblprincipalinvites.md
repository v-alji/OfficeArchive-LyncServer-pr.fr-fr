---
title: 'Lync Server 2013 : tblPrincipalInvites'
description: 'Lync Server 2013 : tblPrincipalInvites.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalInvites
ms:assetid: 548ec156-4d1a-469d-a804-62cff226e5c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558650(v=OCS.15)
ms:contentKeyID: 48184141
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d30d741864ed2a3cfbec8329215be33c21b3b262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423504"
---
# <a name="tblprincipalinvites-in-lync-server-2013"></a><span data-ttu-id="193ab-103">tblPrincipalInvites dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="193ab-103">tblPrincipalInvites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="193ab-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="193ab-104">

<span> </span></span></span>

<span data-ttu-id="193ab-105">_**Dernière modification de la rubrique :** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="193ab-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="193ab-106">tblPrincipalInvites contient des invitations pour tous les utilisateurs approvisionnés pour tous les nœuds avec l’invitation automatique activé.</span><span class="sxs-lookup"><span data-stu-id="193ab-106">tblPrincipalInvites contains invitations for all provisioned users for all nodes with auto-invite on.</span></span>

### <a name="columns"></a><span data-ttu-id="193ab-107">Celles</span><span class="sxs-lookup"><span data-stu-id="193ab-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="193ab-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="193ab-108">Column</span></span></th>
<th><span data-ttu-id="193ab-109">Type</span><span class="sxs-lookup"><span data-stu-id="193ab-109">Type</span></span></th>
<th><span data-ttu-id="193ab-110">Description</span><span class="sxs-lookup"><span data-stu-id="193ab-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="193ab-111">prinID</span><span class="sxs-lookup"><span data-stu-id="193ab-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="193ab-112">ent, non null</span><span class="sxs-lookup"><span data-stu-id="193ab-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="193ab-113">ID du principal.</span><span class="sxs-lookup"><span data-stu-id="193ab-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="193ab-114">invID</span><span class="sxs-lookup"><span data-stu-id="193ab-114">invID</span></span></p></td>
<td><p><span data-ttu-id="193ab-115">ent, non null</span><span class="sxs-lookup"><span data-stu-id="193ab-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="193ab-116">Numéro séquentiel unique (par ID principal) généré à partir de la table tblLastInviteId.</span><span class="sxs-lookup"><span data-stu-id="193ab-116">Unique sequential number (per principal ID) generated from tblLastInviteId table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="193ab-117">ID</span><span class="sxs-lookup"><span data-stu-id="193ab-117">nodeID</span></span></p></td>
<td><p><span data-ttu-id="193ab-118">ent, non null</span><span class="sxs-lookup"><span data-stu-id="193ab-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="193ab-119">ID de nœud (salle de conversation uniquement).</span><span class="sxs-lookup"><span data-stu-id="193ab-119">Node ID (chat room only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="193ab-120">Created</span><span class="sxs-lookup"><span data-stu-id="193ab-120">createdOn</span></span></p></td>
<td><p><span data-ttu-id="193ab-121">DATEHEURE, pas null</span><span class="sxs-lookup"><span data-stu-id="193ab-121">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="193ab-122">Heure de création</span><span class="sxs-lookup"><span data-stu-id="193ab-122">Time of creation.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="193ab-123">Permettent</span><span class="sxs-lookup"><span data-stu-id="193ab-123">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="193ab-124">Colonne</span><span class="sxs-lookup"><span data-stu-id="193ab-124">Column</span></span></th>
<th><span data-ttu-id="193ab-125">Description</span><span class="sxs-lookup"><span data-stu-id="193ab-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="193ab-126">&lt;prinID, nodeID&gt;</span><span class="sxs-lookup"><span data-stu-id="193ab-126">&lt;prinID, nodeID&gt;</span></span></p></td>
<td><p><span data-ttu-id="193ab-127">Clé primaire.</span><span class="sxs-lookup"><span data-stu-id="193ab-127">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="193ab-128">prinID</span><span class="sxs-lookup"><span data-stu-id="193ab-128">prinID</span></span></p></td>
<td><p><span data-ttu-id="193ab-129">Clé étrangère avec recherche dans la table tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="193ab-129">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="193ab-130">ID</span><span class="sxs-lookup"><span data-stu-id="193ab-130">nodeID</span></span></p></td>
<td><p><span data-ttu-id="193ab-131">Clé étrangère avec recherche dans la table tblNode. nodeID.</span><span class="sxs-lookup"><span data-stu-id="193ab-131">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="193ab-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="193ab-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

