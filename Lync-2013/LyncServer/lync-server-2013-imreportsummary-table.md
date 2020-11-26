---
title: 'Tableau Lync Server 2013 : IMReportSummary'
description: 'Tableau Lync Server 2013 : IMReportSummary'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IMReportSummary table
ms:assetid: 27ff9453-53f2-4fae-b637-70a086c9df96
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204753(v=OCS.15)
ms:contentKeyID: 48183673
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dfafa81d1605845b29a3627321fcbc0f72ca7ac7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427312"
---
# <a name="imreportsummary-table-in-lync-server-2013"></a><span data-ttu-id="5deef-103">Table IMReportSummary dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5deef-103">IMReportSummary table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5deef-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5deef-104">

<span> </span></span></span>

<span data-ttu-id="5deef-105">_**Dernière modification de la rubrique :** 2012-08-20_</span><span class="sxs-lookup"><span data-stu-id="5deef-105">_**Topic Last Modified:** 2012-08-20_</span></span>

<span data-ttu-id="5deef-106">Le IMReportSummaryTable fournit un rapport global sur les sessions de messagerie instantanée tenues au sein d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="5deef-106">The IMReportSummaryTable provides an overall report on the instant messaging sessions held in an organization.</span></span> <span data-ttu-id="5deef-107">Ce tableau a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5deef-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5deef-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="5deef-108">Column</span></span></th>
<th><span data-ttu-id="5deef-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="5deef-109">Data Type</span></span></th>
<th><span data-ttu-id="5deef-110">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="5deef-110">Key/Index</span></span></th>
<th><span data-ttu-id="5deef-111">Détails</span><span class="sxs-lookup"><span data-stu-id="5deef-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5deef-112"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="5deef-112"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5deef-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="5deef-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="5deef-114">Principal</span><span class="sxs-lookup"><span data-stu-id="5deef-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="5deef-115">Date et heure de début de la session de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="5deef-115">Date and time that the instant messaging session began.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5deef-116"><strong>TimePeriod</strong></span><span class="sxs-lookup"><span data-stu-id="5deef-116"><strong>TimePeriod</strong></span></span></p></td>
<td><p><span data-ttu-id="5deef-117">Char(1</span><span class="sxs-lookup"><span data-stu-id="5deef-117">char(1)</span></span></p></td>
<td><p><span data-ttu-id="5deef-118">Principal</span><span class="sxs-lookup"><span data-stu-id="5deef-118">Primary</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5deef-119"><strong>PoolFQDN</strong></span><span class="sxs-lookup"><span data-stu-id="5deef-119"><strong>PoolFQDN</strong></span></span></p></td>
<td><p><span data-ttu-id="5deef-120">nvarchar (257)</span><span class="sxs-lookup"><span data-stu-id="5deef-120">nvarchar(257)</span></span></p></td>
<td><p><span data-ttu-id="5deef-121">Principal</span><span class="sxs-lookup"><span data-stu-id="5deef-121">Primary</span></span></p></td>
<td><p><span data-ttu-id="5deef-122">Nom de domaine complet du pool hébergeant la session.</span><span class="sxs-lookup"><span data-stu-id="5deef-122">Fully qualified domain name of the pool hosting the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5deef-123"><strong>AuthType</strong></span><span class="sxs-lookup"><span data-stu-id="5deef-123"><strong>AuthType</strong></span></span></p></td>
<td><p><span data-ttu-id="5deef-124">int</span><span class="sxs-lookup"><span data-stu-id="5deef-124">int</span></span></p></td>
<td><p><span data-ttu-id="5deef-125">Principal</span><span class="sxs-lookup"><span data-stu-id="5deef-125">Primary</span></span></p></td>
<td><p><span data-ttu-id="5deef-126">Priorité (par exemple, urgent ou non urgent) de l’appel.</span><span class="sxs-lookup"><span data-stu-id="5deef-126">Priority (for example, urgent or non-urgent) of the call.</span></span> <span data-ttu-id="5deef-127">Les informations de priorité sont stockées dans la <a href="lync-server-2013-callpriorities-table.md">table CallPriorities dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="5deef-127">Priority information is stored in the <a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5deef-128"><strong>SessionCount</strong></span><span class="sxs-lookup"><span data-stu-id="5deef-128"><strong>SessionCount</strong></span></span></p></td>
<td><p><span data-ttu-id="5deef-129">bigint</span><span class="sxs-lookup"><span data-stu-id="5deef-129">bigint</span></span></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5deef-130"><strong>MsgCount</strong></span><span class="sxs-lookup"><span data-stu-id="5deef-130"><strong>MsgCount</strong></span></span></p></td>
<td><p><span data-ttu-id="5deef-131">bigint</span><span class="sxs-lookup"><span data-stu-id="5deef-131">bigint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5deef-132">Nombre total de messages instantanés échangés lors de la session.</span><span class="sxs-lookup"><span data-stu-id="5deef-132">Total number of instant messages exchanged during the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5deef-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5deef-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

