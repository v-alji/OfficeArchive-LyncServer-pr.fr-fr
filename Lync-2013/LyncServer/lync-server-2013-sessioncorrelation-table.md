---
title: 'Lync Server 2013 : Table SessionCorrelation'
description: 'Tableau Lync Server 2013 : SessionCorrelation'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionCorrelation table
ms:assetid: 041705e1-7290-464f-95f8-96256cfa2e3e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398091(v=OCS.15)
ms:contentKeyID: 48183267
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 814b7e8539d89f87e7df60ceb03e70800553fb55
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424078"
---
# <a name="sessioncorrelation-table-in-lync-server-2013"></a><span data-ttu-id="e8272-103">Table SessionCorrelation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e8272-103">SessionCorrelation table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e8272-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e8272-104">

<span> </span></span></span>

<span data-ttu-id="e8272-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="e8272-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="e8272-106">La table SessionCorrelation est une table de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e8272-106">The SessionCorrelation table is a supporting table.</span></span> <span data-ttu-id="e8272-107">Chaque enregistrement représente une corrélation qui est utilisée pour mettre en corrélation plusieurs sessions.</span><span class="sxs-lookup"><span data-stu-id="e8272-107">Each record represents one CorrelationID which is used to correlate multiple sessions.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8272-108"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="e8272-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="e8272-109"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="e8272-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="e8272-110"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="e8272-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="e8272-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="e8272-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8272-112"><strong>1018</strong></span><span class="sxs-lookup"><span data-stu-id="e8272-112"><strong>Checksum</strong></span></span></p></td>
<td><p><span data-ttu-id="e8272-113">int</span><span class="sxs-lookup"><span data-stu-id="e8272-113">int</span></span></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8272-114"><strong>CorrelationKey</strong></span><span class="sxs-lookup"><span data-stu-id="e8272-114"><strong>CorrelationKey</strong></span></span></p></td>
<td><p><span data-ttu-id="e8272-115">int</span><span class="sxs-lookup"><span data-stu-id="e8272-115">int</span></span></p></td>
<td><p><span data-ttu-id="e8272-116">Principal</span><span class="sxs-lookup"><span data-stu-id="e8272-116">Primary</span></span></p></td>
<td><p><span data-ttu-id="e8272-117">Numéro unique identifiant ce serveur de conférence A/V.</span><span class="sxs-lookup"><span data-stu-id="e8272-117">Unique number identifying this A/V Conferencing Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8272-118"><strong>Corrélation</strong></span><span class="sxs-lookup"><span data-stu-id="e8272-118"><strong>CorrelationID</strong></span></span></p></td>
<td><p><span data-ttu-id="e8272-119">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="e8272-119">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e8272-120">Différent</span><span class="sxs-lookup"><span data-stu-id="e8272-120">Unique</span></span></p></td>
<td><p><span data-ttu-id="e8272-121">Les sessions corrélées auront le même ID de corrélation.</span><span class="sxs-lookup"><span data-stu-id="e8272-121">Sessions that are correlated will have the same correlation ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8272-122"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="e8272-122"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="e8272-123">DateHeure</span><span class="sxs-lookup"><span data-stu-id="e8272-123">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e8272-124">Pour un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="e8272-124">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e8272-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e8272-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

