---
title: 'Tableau Lync Server 2013 : ErrorCategory'
description: 'Tableau Lync Server 2013 : ErrorCategory'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorCategory table
ms:assetid: 0fde3b73-9a2f-44dd-b8dc-6df512303ff1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204675(v=OCS.15)
ms:contentKeyID: 48183425
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8154c73f33b5dad62a338335a960553cfc06ec13
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428565"
---
# <a name="errorcategory-table-in-lync-server-2013"></a><span data-ttu-id="ac5d4-103">Table ErrorCategory dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ac5d4-103">ErrorCategory table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ac5d4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ac5d4-104">

<span> </span></span></span>

<span data-ttu-id="ac5d4-105">_**Dernière modification de la rubrique :** 2012-08-20_</span><span class="sxs-lookup"><span data-stu-id="ac5d4-105">_**Topic Last Modified:** 2012-08-20_</span></span>

<span data-ttu-id="ac5d4-106">La table ErrorCategory contient le nom convivial de chaque classification de diagnostic Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ac5d4-106">The ErrorCategory table contains the friendly name for each Microsoft Lync Server 2013 diagnostic classification.</span></span> <span data-ttu-id="ac5d4-107">Par défaut, Lync Server 2013 utilise les classifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="ac5d4-107">By default, Lync Server 2013 uses the following classifications:</span></span>

  - <span data-ttu-id="ac5d4-108">0--succès</span><span class="sxs-lookup"><span data-stu-id="ac5d4-108">0 -- Success</span></span>

  - <span data-ttu-id="ac5d4-109">1-échec imprévu</span><span class="sxs-lookup"><span data-stu-id="ac5d4-109">1 -- Expected failure</span></span>

  - <span data-ttu-id="ac5d4-110">2-échec inattendu</span><span class="sxs-lookup"><span data-stu-id="ac5d4-110">2 – Unexpected failure</span></span>

<span data-ttu-id="ac5d4-111">Ce tableau a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ac5d4-111">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ac5d4-112">Colonne</span><span class="sxs-lookup"><span data-stu-id="ac5d4-112">Column</span></span></th>
<th><span data-ttu-id="ac5d4-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="ac5d4-113">Data Type</span></span></th>
<th><span data-ttu-id="ac5d4-114">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="ac5d4-114">Key/Index</span></span></th>
<th><span data-ttu-id="ac5d4-115">Détails</span><span class="sxs-lookup"><span data-stu-id="ac5d4-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac5d4-116"><strong>RéfCatégorie</strong></span><span class="sxs-lookup"><span data-stu-id="ac5d4-116"><strong>CategoryId</strong></span></span></p></td>
<td><p><span data-ttu-id="ac5d4-117">tinyint</span><span class="sxs-lookup"><span data-stu-id="ac5d4-117">tinyint</span></span></p></td>
<td><p><span data-ttu-id="ac5d4-118">Principal</span><span class="sxs-lookup"><span data-stu-id="ac5d4-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="ac5d4-119">Identificateur unique de la classification.</span><span class="sxs-lookup"><span data-stu-id="ac5d4-119">Unique identifier for the classification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac5d4-120"><strong>Nom</strong></span><span class="sxs-lookup"><span data-stu-id="ac5d4-120"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ac5d4-121">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="ac5d4-121">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ac5d4-122">Valeur et nom convivial attribués à la classification.</span><span class="sxs-lookup"><span data-stu-id="ac5d4-122">Value and friendly name assigned to the classification.</span></span> <span data-ttu-id="ac5d4-123">Les valeurs autorisées sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ac5d4-123">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="ac5d4-124">0--succès</span><span class="sxs-lookup"><span data-stu-id="ac5d4-124">0 -- Success</span></span></p></li>
<li><p><span data-ttu-id="ac5d4-125">1-échec imprévu</span><span class="sxs-lookup"><span data-stu-id="ac5d4-125">1 -- Expected failure</span></span></p></li>
<li><p><span data-ttu-id="ac5d4-126">2-échec inattendu</span><span class="sxs-lookup"><span data-stu-id="ac5d4-126">2 – Unexpected failure</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="ac5d4-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ac5d4-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

