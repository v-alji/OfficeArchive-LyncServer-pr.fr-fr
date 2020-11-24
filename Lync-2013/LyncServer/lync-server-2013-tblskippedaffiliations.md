---
title: 'Lync Server 2013 : tblSkippedAffiliations'
description: 'Lync Server 2013 : tblSkippedAffiliations.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblSkippedAffiliations
ms:assetid: 0b129b54-a7a8-42a6-9279-0e08410c06ec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558611(v=OCS.15)
ms:contentKeyID: 48183373
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31746cee7302d34a1d19b3059ca1da6beab9345d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395064"
---
# <a name="tblskippedaffiliations-in-lync-server-2013"></a><span data-ttu-id="a65e2-103">tblSkippedAffiliations dans Server 2013</span><span class="sxs-lookup"><span data-stu-id="a65e2-103">tblSkippedAffiliations in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a65e2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a65e2-104">

<span> </span></span></span>

<span data-ttu-id="a65e2-105">_**Dernière modification de la rubrique :** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="a65e2-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="a65e2-106">tblSkippedAffiliations contient les affiliations qui n’ont pas pu être lues (généralement en raison des erreurs d’accès aux services de domaine Active Directory).</span><span class="sxs-lookup"><span data-stu-id="a65e2-106">tblSkippedAffiliations contains the affiliations that could not be read (usually due to Active Directory Domain Services access errors).</span></span>

### <a name="columns"></a><span data-ttu-id="a65e2-107">Celles</span><span class="sxs-lookup"><span data-stu-id="a65e2-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a65e2-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="a65e2-108">Column</span></span></th>
<th><span data-ttu-id="a65e2-109">Type</span><span class="sxs-lookup"><span data-stu-id="a65e2-109">Type</span></span></th>
<th><span data-ttu-id="a65e2-110">Description</span><span class="sxs-lookup"><span data-stu-id="a65e2-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a65e2-111">prinID</span><span class="sxs-lookup"><span data-stu-id="a65e2-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="a65e2-112">ent, non null</span><span class="sxs-lookup"><span data-stu-id="a65e2-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="a65e2-113">ID du principal.</span><span class="sxs-lookup"><span data-stu-id="a65e2-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a65e2-114">affDescription</span><span class="sxs-lookup"><span data-stu-id="a65e2-114">affDescription</span></span></p></td>
<td><p><span data-ttu-id="a65e2-115">nvarchar (256), pas null</span><span class="sxs-lookup"><span data-stu-id="a65e2-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="a65e2-116">Chaîne identifiant l’affiliation.</span><span class="sxs-lookup"><span data-stu-id="a65e2-116">A string identifying the affiliation.</span></span></p>
<p><span data-ttu-id="a65e2-117">Le format est : GUID : {0} URI : {1} &gt; ID :{2}</span><span class="sxs-lookup"><span data-stu-id="a65e2-117">The format is: guid: {0} uri: {1}&gt; id: {2}</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a65e2-118">updatedBy</span><span class="sxs-lookup"><span data-stu-id="a65e2-118">updatedBy</span></span></p></td>
<td><p><span data-ttu-id="a65e2-119">ent, non null</span><span class="sxs-lookup"><span data-stu-id="a65e2-119">int, not null</span></span></p></td>
<td><p><span data-ttu-id="a65e2-120">ID de l’objet principal qui a mis à jour cette ligne.</span><span class="sxs-lookup"><span data-stu-id="a65e2-120">ID of the principal that updated this row.</span></span> <span data-ttu-id="a65e2-121">Il est toujours 1 (utilisateur système), car la synchronisation Active Directory est la seule source de ces entrées.</span><span class="sxs-lookup"><span data-stu-id="a65e2-121">It is always 1 (system user) because Active Directory Sync is the only source for these entries.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="a65e2-122">Permettent</span><span class="sxs-lookup"><span data-stu-id="a65e2-122">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a65e2-123">Colonne (s)</span><span class="sxs-lookup"><span data-stu-id="a65e2-123">Column(s)</span></span></th>
<th><span data-ttu-id="a65e2-124">Description</span><span class="sxs-lookup"><span data-stu-id="a65e2-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a65e2-125">&lt;prinID, affDescription&gt;</span><span class="sxs-lookup"><span data-stu-id="a65e2-125">&lt;prinID, affDescription&gt;</span></span></p></td>
<td><p><span data-ttu-id="a65e2-126">Clé primaire.</span><span class="sxs-lookup"><span data-stu-id="a65e2-126">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a65e2-127">prinID</span><span class="sxs-lookup"><span data-stu-id="a65e2-127">prinID</span></span></p></td>
<td><p><span data-ttu-id="a65e2-128">Clé étrangère avec recherche dans la table tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="a65e2-128">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a65e2-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a65e2-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

