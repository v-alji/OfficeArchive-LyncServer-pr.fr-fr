---
title: 'Lync Server 2013 : tblEnumAttribute'
description: 'Lync Server 2013 : tblEnumAttribute.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblEnumAttribute
ms:assetid: 17f8b87e-36a6-4f6a-8630-7c76b61a7595
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558617(v=OCS.15)
ms:contentKeyID: 48183523
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ca979a68e758ad47b691ac704f24c68c1841938a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423539"
---
# <a name="tblenumattribute-in-lync-server-2013"></a><span data-ttu-id="07a15-103">tblEnumAttribute dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="07a15-103">tblEnumAttribute in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="07a15-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="07a15-104">

<span> </span></span></span>

<span data-ttu-id="07a15-105">_**Dernière modification de la rubrique :** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="07a15-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="07a15-106">tblEnumAttribute est une table codée en dur qui contient les attributs de visibilité et de comportement qui sont utilisés dans la table de nœud.</span><span class="sxs-lookup"><span data-stu-id="07a15-106">tblEnumAttribute is a hardcoded table that contains the Visibility and Behavior attributes that are used in the Node table.</span></span>

### <a name="columns"></a><span data-ttu-id="07a15-107">Celles</span><span class="sxs-lookup"><span data-stu-id="07a15-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="07a15-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="07a15-108">Column</span></span></th>
<th><span data-ttu-id="07a15-109">Type</span><span class="sxs-lookup"><span data-stu-id="07a15-109">Type</span></span></th>
<th><span data-ttu-id="07a15-110">Description</span><span class="sxs-lookup"><span data-stu-id="07a15-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07a15-111">attributeID</span><span class="sxs-lookup"><span data-stu-id="07a15-111">attributeID</span></span></p></td>
<td><p><span data-ttu-id="07a15-112">smallint, pas null</span><span class="sxs-lookup"><span data-stu-id="07a15-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="07a15-113">ID de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="07a15-113">ID of the attribute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07a15-114">attributeName</span><span class="sxs-lookup"><span data-stu-id="07a15-114">attributeName</span></span></p></td>
<td><p><span data-ttu-id="07a15-115">nvarchar (256), pas null</span><span class="sxs-lookup"><span data-stu-id="07a15-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="07a15-116">Nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="07a15-116">Name of the attribute.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="07a15-117">Clé</span><span class="sxs-lookup"><span data-stu-id="07a15-117">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="07a15-118">Colonne</span><span class="sxs-lookup"><span data-stu-id="07a15-118">Column</span></span></th>
<th><span data-ttu-id="07a15-119">Description</span><span class="sxs-lookup"><span data-stu-id="07a15-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07a15-120">attributeID</span><span class="sxs-lookup"><span data-stu-id="07a15-120">attributeID</span></span></p></td>
<td><p><span data-ttu-id="07a15-121">Clé primaire.</span><span class="sxs-lookup"><span data-stu-id="07a15-121">Primary key.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-values"></a><span data-ttu-id="07a15-122">Valeurs de table</span><span class="sxs-lookup"><span data-stu-id="07a15-122">Table Values</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="07a15-123">attributeID</span><span class="sxs-lookup"><span data-stu-id="07a15-123">attributeID</span></span></th>
<th><span data-ttu-id="07a15-124">attributeName</span><span class="sxs-lookup"><span data-stu-id="07a15-124">attributeName</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07a15-125">1</span><span class="sxs-lookup"><span data-stu-id="07a15-125">1</span></span></p></td>
<td><p><span data-ttu-id="07a15-126">Notoriété.</span><span class="sxs-lookup"><span data-stu-id="07a15-126">Visibility.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07a15-127">2</span><span class="sxs-lookup"><span data-stu-id="07a15-127">2</span></span></p></td>
<td><p><span data-ttu-id="07a15-128">Fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="07a15-128">Behavior.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="07a15-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07a15-129">See Also</span></span>


[<span data-ttu-id="07a15-130">tblNode dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="07a15-130">tblNode in Lync Server 2013</span></span>](lync-server-2013-tblnode.md)  
  

<span data-ttu-id="07a15-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="07a15-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

