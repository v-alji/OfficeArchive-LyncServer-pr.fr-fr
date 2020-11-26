---
title: 'Lync Server 2013 : tblLastInviteId'
description: 'Lync Server 2013 : tblLastInviteId.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblLastInviteId
ms:assetid: 222b3508-5963-4ddc-b4f3-e8412767e61b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558625(v=OCS.15)
ms:contentKeyID: 48183608
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e5a13cfc7edc29ea20c95f7f4d587b0cfb84eb73
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444419"
---
# <a name="tbllastinviteid-in-lync-server-2013"></a><span data-ttu-id="a49b0-103">tblLastInviteId dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a49b0-103">tblLastInviteId in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a49b0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a49b0-104">

<span> </span></span></span>

<span data-ttu-id="a49b0-105">_**Dernière modification de la rubrique :** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="a49b0-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="a49b0-106">tblLastInviteId contient le dernier ID d’invitation généré (et utilisé dans la table tblPrincipalInvites) pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a49b0-106">tblLastInviteId contains the last invite ID that was generated (and used in the tblPrincipalInvites table) for each user.</span></span>

### <a name="columns"></a><span data-ttu-id="a49b0-107">Celles</span><span class="sxs-lookup"><span data-stu-id="a49b0-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a49b0-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="a49b0-108">Column</span></span></th>
<th><span data-ttu-id="a49b0-109">Type</span><span class="sxs-lookup"><span data-stu-id="a49b0-109">Type</span></span></th>
<th><span data-ttu-id="a49b0-110">Description</span><span class="sxs-lookup"><span data-stu-id="a49b0-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a49b0-111">prinID</span><span class="sxs-lookup"><span data-stu-id="a49b0-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="a49b0-112">ent, non null</span><span class="sxs-lookup"><span data-stu-id="a49b0-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="a49b0-113">ID du principal.</span><span class="sxs-lookup"><span data-stu-id="a49b0-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a49b0-114">lastInviteID</span><span class="sxs-lookup"><span data-stu-id="a49b0-114">lastInviteID</span></span></p></td>
<td><p><span data-ttu-id="a49b0-115">ent, non null</span><span class="sxs-lookup"><span data-stu-id="a49b0-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="a49b0-116">Dernier ID d’invitation utilisé.</span><span class="sxs-lookup"><span data-stu-id="a49b0-116">Last used invite ID.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="a49b0-117">Permettent</span><span class="sxs-lookup"><span data-stu-id="a49b0-117">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a49b0-118">Colonne</span><span class="sxs-lookup"><span data-stu-id="a49b0-118">Column</span></span></th>
<th><span data-ttu-id="a49b0-119">Description</span><span class="sxs-lookup"><span data-stu-id="a49b0-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a49b0-120">prinID</span><span class="sxs-lookup"><span data-stu-id="a49b0-120">prinID</span></span></p></td>
<td><p><span data-ttu-id="a49b0-121">Clé primaire.</span><span class="sxs-lookup"><span data-stu-id="a49b0-121">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a49b0-122">prinID</span><span class="sxs-lookup"><span data-stu-id="a49b0-122">prinID</span></span></p></td>
<td><p><span data-ttu-id="a49b0-123">Clé étrangère avec recherche dans la table tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="a49b0-123">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="a49b0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a49b0-124">See Also</span></span>


[<span data-ttu-id="a49b0-125">tblPrincipalInvites dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a49b0-125">tblPrincipalInvites in Lync Server 2013</span></span>](lync-server-2013-tblprincipalinvites.md)  
  

<span data-ttu-id="a49b0-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a49b0-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

