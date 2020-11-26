---
title: 'Lync Server 2013 : tblEnumValue'
description: 'Lync Server 2013 : tblEnumValue.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblEnumValue
ms:assetid: a33df20c-d19d-4f5c-b012-29dab8fb9200
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615025(v=OCS.15)
ms:contentKeyID: 48185040
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 159f90bb96c367fcb3e11725a582a9993080d3fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444447"
---
# <a name="tblenumvalue-in-lync-server-2013"></a><span data-ttu-id="9e2c0-103">tblEnumValue dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e2c0-103">tblEnumValue in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9e2c0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9e2c0-104">

<span> </span></span></span>

<span data-ttu-id="9e2c0-105">_**Dernière modification de la rubrique :** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="9e2c0-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="9e2c0-106">tblEnumValue est une table codée en dur qui contient les valeurs de visibilité et de comportement des attributs qui sont utilisés dans la table de nœud.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-106">tblEnumValue is a hardcoded table that contains the Visibility and Behavior values of the attributes that are used in the Node table.</span></span>

### <a name="columns"></a><span data-ttu-id="9e2c0-107">Celles</span><span class="sxs-lookup"><span data-stu-id="9e2c0-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e2c0-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="9e2c0-108">Column</span></span></th>
<th><span data-ttu-id="9e2c0-109">Type</span><span class="sxs-lookup"><span data-stu-id="9e2c0-109">Type</span></span></th>
<th><span data-ttu-id="9e2c0-110">Description</span><span class="sxs-lookup"><span data-stu-id="9e2c0-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e2c0-111">valueID</span><span class="sxs-lookup"><span data-stu-id="9e2c0-111">valueID</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-112">smallint, pas null</span><span class="sxs-lookup"><span data-stu-id="9e2c0-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-113">ID de la valeur.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-113">ID of the value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e2c0-114">attributeID</span><span class="sxs-lookup"><span data-stu-id="9e2c0-114">attributeID</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-115">smallint, pas null</span><span class="sxs-lookup"><span data-stu-id="9e2c0-115">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-116">ID de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-116">ID of the attribute.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e2c0-117">attributeValue</span><span class="sxs-lookup"><span data-stu-id="9e2c0-117">attributeValue</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-118">nvarchar (256), pas null</span><span class="sxs-lookup"><span data-stu-id="9e2c0-118">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-119">Nom de la valeur.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-119">Name of the value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="9e2c0-120">Permettent</span><span class="sxs-lookup"><span data-stu-id="9e2c0-120">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e2c0-121">Colonne</span><span class="sxs-lookup"><span data-stu-id="9e2c0-121">Column</span></span></th>
<th><span data-ttu-id="9e2c0-122">Description</span><span class="sxs-lookup"><span data-stu-id="9e2c0-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e2c0-123">valueID</span><span class="sxs-lookup"><span data-stu-id="9e2c0-123">valueID</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-124">Clé primaire.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-124">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e2c0-125">attributeID</span><span class="sxs-lookup"><span data-stu-id="9e2c0-125">attributeID</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-126">Clé étrangère avec recherche dans la table tblEnumAttribute. attributeID.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-126">Foreign key with lookup in tblEnumAttribute.attributeID table.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-values"></a><span data-ttu-id="9e2c0-127">Valeurs de table</span><span class="sxs-lookup"><span data-stu-id="9e2c0-127">Table Values</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e2c0-128">valueID</span><span class="sxs-lookup"><span data-stu-id="9e2c0-128">valueID</span></span></th>
<th><span data-ttu-id="9e2c0-129">attributeID</span><span class="sxs-lookup"><span data-stu-id="9e2c0-129">attributeID</span></span></th>
<th><span data-ttu-id="9e2c0-130">attributeValue</span><span class="sxs-lookup"><span data-stu-id="9e2c0-130">attributeValue</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e2c0-131">2</span><span class="sxs-lookup"><span data-stu-id="9e2c0-131">2</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-132">1</span><span class="sxs-lookup"><span data-stu-id="9e2c0-132">1</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-133">privé</span><span class="sxs-lookup"><span data-stu-id="9e2c0-133">private</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e2c0-134">3</span><span class="sxs-lookup"><span data-stu-id="9e2c0-134">3</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-135">1</span><span class="sxs-lookup"><span data-stu-id="9e2c0-135">1</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-136">hors</span><span class="sxs-lookup"><span data-stu-id="9e2c0-136">scope</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e2c0-137">4</span><span class="sxs-lookup"><span data-stu-id="9e2c0-137">4</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-138">2</span><span class="sxs-lookup"><span data-stu-id="9e2c0-138">2</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-139">normalement</span><span class="sxs-lookup"><span data-stu-id="9e2c0-139">normal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e2c0-140">5</span><span class="sxs-lookup"><span data-stu-id="9e2c0-140">5</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-141">2</span><span class="sxs-lookup"><span data-stu-id="9e2c0-141">2</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-142">Conférence</span><span class="sxs-lookup"><span data-stu-id="9e2c0-142">auditorium</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e2c0-143">6</span><span class="sxs-lookup"><span data-stu-id="9e2c0-143">6</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-144">1</span><span class="sxs-lookup"><span data-stu-id="9e2c0-144">1</span></span></p></td>
<td><p><span data-ttu-id="9e2c0-145">ouvre</span><span class="sxs-lookup"><span data-stu-id="9e2c0-145">open</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="9e2c0-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e2c0-146">See Also</span></span>


[<span data-ttu-id="9e2c0-147">tblNode dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e2c0-147">tblNode in Lync Server 2013</span></span>](lync-server-2013-tblnode.md)  
  

<span data-ttu-id="9e2c0-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9e2c0-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

