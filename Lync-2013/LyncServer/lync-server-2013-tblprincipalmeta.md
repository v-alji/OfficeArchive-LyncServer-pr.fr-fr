---
title: 'Lync Server 2013 : tblPrincipalMeta'
description: 'Lync Server 2013 : tblPrincipalMeta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalMeta
ms:assetid: 808490d4-7d6d-47a2-b8af-b5940d47073b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615009(v=OCS.15)
ms:contentKeyID: 48184648
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 899fd1e450dac52afa56c1ee1de86da82b2db309
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393932"
---
# <a name="tblprincipalmeta-in-lync-server-2013"></a><span data-ttu-id="99d5c-103">tblPrincipalMeta dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="99d5c-103">tblPrincipalMeta in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="99d5c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="99d5c-104">

<span> </span></span></span>

<span data-ttu-id="99d5c-105">_**Dernière modification de la rubrique :** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="99d5c-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="99d5c-106">tblPrincipalMeta contient les principaux qui doivent être actualisés à partir des services de domaine Active Directory (AD FS).</span><span class="sxs-lookup"><span data-stu-id="99d5c-106">tblPrincipalMeta contains the principals that have to be refreshed from Active Directory Domain Services.</span></span>

### <a name="columns"></a><span data-ttu-id="99d5c-107">Celles</span><span class="sxs-lookup"><span data-stu-id="99d5c-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="99d5c-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="99d5c-108">Column</span></span></th>
<th><span data-ttu-id="99d5c-109">Type</span><span class="sxs-lookup"><span data-stu-id="99d5c-109">Type</span></span></th>
<th><span data-ttu-id="99d5c-110">Description</span><span class="sxs-lookup"><span data-stu-id="99d5c-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99d5c-111">prinID</span><span class="sxs-lookup"><span data-stu-id="99d5c-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="99d5c-112">ent, non null</span><span class="sxs-lookup"><span data-stu-id="99d5c-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="99d5c-113">ID du principal.</span><span class="sxs-lookup"><span data-stu-id="99d5c-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99d5c-114">prinAffiliationsDirty</span><span class="sxs-lookup"><span data-stu-id="99d5c-114">prinAffiliationsDirty</span></span></p></td>
<td><p><span data-ttu-id="99d5c-115">bit, pas null</span><span class="sxs-lookup"><span data-stu-id="99d5c-115">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="99d5c-116">True si les affiliations principales doivent être actualisées.</span><span class="sxs-lookup"><span data-stu-id="99d5c-116">True if principal affiliations have to be refreshed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99d5c-117">prinAttributesDirty</span><span class="sxs-lookup"><span data-stu-id="99d5c-117">prinAttributesDirty</span></span></p></td>
<td><p><span data-ttu-id="99d5c-118">bit, pas null</span><span class="sxs-lookup"><span data-stu-id="99d5c-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="99d5c-119">True si les attributs principaux doivent être actualisés.</span><span class="sxs-lookup"><span data-stu-id="99d5c-119">True if principal attributes have to be refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99d5c-120">prinDeleted</span><span class="sxs-lookup"><span data-stu-id="99d5c-120">prinDeleted</span></span></p></td>
<td><p><span data-ttu-id="99d5c-121">bit, pas null</span><span class="sxs-lookup"><span data-stu-id="99d5c-121">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="99d5c-122">True si l’objet principal a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="99d5c-122">True if the principal has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99d5c-123">tryCount</span><span class="sxs-lookup"><span data-stu-id="99d5c-123">tryCount</span></span></p></td>
<td><p><span data-ttu-id="99d5c-124">int</span><span class="sxs-lookup"><span data-stu-id="99d5c-124">int</span></span></p></td>
<td><p><span data-ttu-id="99d5c-125">Nombre de tentatives d’actualisation du principal à partir d’AD DS qui est déjà en passe.</span><span class="sxs-lookup"><span data-stu-id="99d5c-125">Number of attempts to refresh the principal from AD DS that have happened so far.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99d5c-126">lastTry</span><span class="sxs-lookup"><span data-stu-id="99d5c-126">lastTry</span></span></p></td>
<td><p><span data-ttu-id="99d5c-127">DateHeure</span><span class="sxs-lookup"><span data-stu-id="99d5c-127">datetime</span></span></p></td>
<td><p><span data-ttu-id="99d5c-128">Horodatage de la dernière tentative d’actualisation du principal.</span><span class="sxs-lookup"><span data-stu-id="99d5c-128">Time stamp from the latest attempt to refresh the principal.</span></span> <span data-ttu-id="99d5c-129">Il peut s’agir de la valeur null s’il n’y a pas encore de tentative d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="99d5c-129">Can be null if no refresh has been attempted yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99d5c-130">nextTry</span><span class="sxs-lookup"><span data-stu-id="99d5c-130">nextTry</span></span></p></td>
<td><p><span data-ttu-id="99d5c-131">DateHeure</span><span class="sxs-lookup"><span data-stu-id="99d5c-131">datetime</span></span></p></td>
<td><p><span data-ttu-id="99d5c-132">Horodatage de la prochaine actualisation planifiée.</span><span class="sxs-lookup"><span data-stu-id="99d5c-132">Time stamp for the next scheduled refresh.</span></span> <span data-ttu-id="99d5c-133">Peut être null s’il n’y a pas de planification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="99d5c-133">Can be null if no further refresh has been scheduled.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="99d5c-134">Permettent</span><span class="sxs-lookup"><span data-stu-id="99d5c-134">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="99d5c-135">Colonne</span><span class="sxs-lookup"><span data-stu-id="99d5c-135">Column</span></span></th>
<th><span data-ttu-id="99d5c-136">Description</span><span class="sxs-lookup"><span data-stu-id="99d5c-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99d5c-137">prinID</span><span class="sxs-lookup"><span data-stu-id="99d5c-137">prinID</span></span></p></td>
<td><p><span data-ttu-id="99d5c-138">Clé primaire.</span><span class="sxs-lookup"><span data-stu-id="99d5c-138">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99d5c-139">prinID</span><span class="sxs-lookup"><span data-stu-id="99d5c-139">prinID</span></span></p></td>
<td><p><span data-ttu-id="99d5c-140">Clé étrangère avec recherche dans la table tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="99d5c-140">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="99d5c-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="99d5c-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

