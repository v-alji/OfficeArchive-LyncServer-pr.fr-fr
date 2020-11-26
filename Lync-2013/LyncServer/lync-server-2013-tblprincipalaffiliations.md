---
title: 'Lync Server 2013 : tblPrincipalAffiliations'
description: 'Lync Server 2013 : tblPrincipalAffiliations.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalAffiliations
ms:assetid: 45fd8484-5837-44d2-85bb-45c83546607c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558642(v=OCS.15)
ms:contentKeyID: 48183993
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01c373147a58300e64f22e60e989a777c59b2653
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441367"
---
# <a name="tblprincipalaffiliations-in-lync-server-2013"></a><span data-ttu-id="74cee-103">tblPrincipalAffiliations dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74cee-103">tblPrincipalAffiliations in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="74cee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="74cee-104">

<span> </span></span></span>

<span data-ttu-id="74cee-105">_**Dernière modification de la rubrique :** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="74cee-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="74cee-106">tblPrincipalAffiliations contient les affiliations principales qui décrivent les appartenances aux emplacements, y compris les groupes de sécurité des services de domaine Active Directory (AD FS) dans les conteneurs Active Directory, dans les domaines.</span><span class="sxs-lookup"><span data-stu-id="74cee-106">tblPrincipalAffiliations contains the principal affiliations that describe memberships in locations, including Active Directory Domain Services security groups, in Active Directory containers, in domains.</span></span>

### <a name="columns"></a><span data-ttu-id="74cee-107">Celles</span><span class="sxs-lookup"><span data-stu-id="74cee-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="74cee-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="74cee-108">Column</span></span></th>
<th><span data-ttu-id="74cee-109">Type</span><span class="sxs-lookup"><span data-stu-id="74cee-109">Type</span></span></th>
<th><span data-ttu-id="74cee-110">Description</span><span class="sxs-lookup"><span data-stu-id="74cee-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74cee-111">principalID</span><span class="sxs-lookup"><span data-stu-id="74cee-111">principalID</span></span></p></td>
<td><p><span data-ttu-id="74cee-112">ent, non null</span><span class="sxs-lookup"><span data-stu-id="74cee-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="74cee-113">ID du principal affilié.</span><span class="sxs-lookup"><span data-stu-id="74cee-113">ID of the affiliated principal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74cee-114">affiliationID</span><span class="sxs-lookup"><span data-stu-id="74cee-114">affiliationID</span></span></p></td>
<td><p><span data-ttu-id="74cee-115">ent, non null</span><span class="sxs-lookup"><span data-stu-id="74cee-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="74cee-116">ID de l’objet principal qui représente l’affiliation.</span><span class="sxs-lookup"><span data-stu-id="74cee-116">ID of the principal representing the affiliation.</span></span> <span data-ttu-id="74cee-117">Chaque identité (à l’exception des types d’utilisateur système) possède également une auto-affiliation.</span><span class="sxs-lookup"><span data-stu-id="74cee-117">Each principal (except system-user-types) has a self-affiliation as well.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74cee-118">index</span><span class="sxs-lookup"><span data-stu-id="74cee-118">index</span></span></p></td>
<td><p><span data-ttu-id="74cee-119">ent, non null</span><span class="sxs-lookup"><span data-stu-id="74cee-119">int, not null</span></span></p></td>
<td><p><span data-ttu-id="74cee-120">Index.</span><span class="sxs-lookup"><span data-stu-id="74cee-120">Index.</span></span> <span data-ttu-id="74cee-121">La valeur de auto-affiliations est-1, et pour les autres affiliations, elle augmente séquentiellement de 1 dans chaque &lt; principalID, &gt; compartiment affiliationId.</span><span class="sxs-lookup"><span data-stu-id="74cee-121">The value for self-affiliations is -1, and for the other affiliations it increases sequentially from 1 within each &lt;principalID, affiliationId&gt; bucket.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74cee-122">updatedBy</span><span class="sxs-lookup"><span data-stu-id="74cee-122">updatedBy</span></span></p></td>
<td><p><span data-ttu-id="74cee-123">ent, non null</span><span class="sxs-lookup"><span data-stu-id="74cee-123">int, not null</span></span></p></td>
<td><p><span data-ttu-id="74cee-124">Principal ayant effectué la dernière mise à jour.</span><span class="sxs-lookup"><span data-stu-id="74cee-124">Principal that did the latest update.</span></span> <span data-ttu-id="74cee-125">Il s’agit généralement de la méthode de synchronisation Active Directory.</span><span class="sxs-lookup"><span data-stu-id="74cee-125">This is usually 1, which means Active Directory Sync.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="74cee-126">Permettent</span><span class="sxs-lookup"><span data-stu-id="74cee-126">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="74cee-127">Celles</span><span class="sxs-lookup"><span data-stu-id="74cee-127">Columns</span></span></th>
<th><span data-ttu-id="74cee-128">Description</span><span class="sxs-lookup"><span data-stu-id="74cee-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74cee-129">&lt;principalID, index, affiliationID&gt;</span><span class="sxs-lookup"><span data-stu-id="74cee-129">&lt;principalID, index, affiliationID&gt;</span></span></p></td>
<td><p><span data-ttu-id="74cee-130">Clé primaire.</span><span class="sxs-lookup"><span data-stu-id="74cee-130">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74cee-131">principalID</span><span class="sxs-lookup"><span data-stu-id="74cee-131">principalID</span></span></p></td>
<td><p><span data-ttu-id="74cee-132">Clé étrangère avec recherche dans la table tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="74cee-132">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74cee-133">affiliationID</span><span class="sxs-lookup"><span data-stu-id="74cee-133">affiliationID</span></span></p></td>
<td><p><span data-ttu-id="74cee-134">Clé étrangère avec recherche dans la table tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="74cee-134">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="74cee-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="74cee-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

