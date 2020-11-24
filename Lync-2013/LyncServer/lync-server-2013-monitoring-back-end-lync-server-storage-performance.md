---
title: 'Lync Server 2013 : surveillance des performances du stockage principal de Lync Server'
description: 'Lync Server 2013 : surveillance des performances du stockage principal de Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring back end Lync Server 2013 storage performance
ms:assetid: 71627c70-1953-4ac2-afbe-f3ad85be0f44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720917(v=OCS.15)
ms:contentKeyID: 63969619
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7501418d3589b941b7e92d2b414492c1d27a3ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394172"
---
# <a name="monitoring-back-end-lync-server-2013-storage-performance"></a><span data-ttu-id="93348-103">Surveiller les performances de stockage de Lync Server 2013 en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="93348-103">Monitoring back end Lync Server 2013 storage performance</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="93348-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="93348-104">

<span> </span></span></span>

<span data-ttu-id="93348-105">_**Dernière modification de la rubrique :** 2014-05-02_</span><span class="sxs-lookup"><span data-stu-id="93348-105">_**Topic Last Modified:** 2014-05-02_</span></span>

<span data-ttu-id="93348-106">Les bases de données principales de Lync Server 2013 constituent un élément essentiel du déploiement de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="93348-106">The Lync Server 2013 back-end databases are a very important part of the Lync Server 2013 deployment.</span></span> <span data-ttu-id="93348-107">Nous vous recommandons de surveiller en permanence les bases de données et les journaux de transactions correspondants pour vous assurer que le serveur Lync Server 2013 fonctionne de façon optimale.</span><span class="sxs-lookup"><span data-stu-id="93348-107">We recommend constantly monitoring the databases and respective transaction logs to help to make sure that the Lync Server 2013 back end is performing optimally.</span></span>

<span data-ttu-id="93348-108">Le tableau suivant identifie les compteurs de performance qui doivent être surveillés pour en savoir plus sur les performances de stockage.</span><span class="sxs-lookup"><span data-stu-id="93348-108">The following table identifies performance counters that should be monitored to learn information about Storage Performance.</span></span> <span data-ttu-id="93348-109">Les valeurs de référence de ces compteurs doivent d’abord être définies (lorsque le système se trouve à sa normale, charge attendue) pour comprendre les changements de performance lorsque le système est surchargé.</span><span class="sxs-lookup"><span data-stu-id="93348-109">The baseline values for these counters must be determined first (when system is at its normal, expected load) to understand the performance changes when system is stressed.</span></span>

### <a name="performance-counters-to-be-monitored"></a><span data-ttu-id="93348-110">Compteurs de performance à surveiller</span><span class="sxs-lookup"><span data-stu-id="93348-110">Performance counters to be monitored</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93348-111">Compteur de performance</span><span class="sxs-lookup"><span data-stu-id="93348-111">Performance Counter</span></span></th>
<th><span data-ttu-id="93348-112">Seuils de référence</span><span class="sxs-lookup"><span data-stu-id="93348-112">Baseline thresholds</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93348-113">Transactions/s (RTC)</span><span class="sxs-lookup"><span data-stu-id="93348-113">Transactions/sec (RTC)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93348-114">Transactions/s (RTCDyn)</span><span class="sxs-lookup"><span data-stu-id="93348-114">Transactions/sec (rtcdyn)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93348-115">Transactions/s (tempdb)</span><span class="sxs-lookup"><span data-stu-id="93348-115">Transactions/sec (tempdb)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93348-116">Vidages du journal/s (RTC)</span><span class="sxs-lookup"><span data-stu-id="93348-116">Log Flushes/sec (RTC)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93348-117">Vidages du journal/s (RTCDyn)</span><span class="sxs-lookup"><span data-stu-id="93348-117">Log Flushes/sec (rtcdyn)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93348-118">Vidages du journal/s (tempdb)</span><span class="sxs-lookup"><span data-stu-id="93348-118">Log Flushes/sec (tempdb)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93348-119">Transferts de disque/s (lecture + écriture)-RTC DB</span><span class="sxs-lookup"><span data-stu-id="93348-119">Disk Transfers/sec (read+write) - RTC db</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93348-120">Transferts de disque/s-journal RTC</span><span class="sxs-lookup"><span data-stu-id="93348-120">Disk Transfers/sec - RTC log</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93348-121">Transferts de disque/s-RTCDyn DB</span><span class="sxs-lookup"><span data-stu-id="93348-121">Disk Transfers/sec - rtcdyn db</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93348-122">Transfert de disque/s-journal de RTCDyn</span><span class="sxs-lookup"><span data-stu-id="93348-122">Disk Transfers/sec - rtcdyn log</span></span></p></td>
<td></td>
</tr>
</tbody>
</table><span data-ttu-id="93348-123">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="93348-123">


</div>

<span> </span>

</div>

</div>

</span></span></div>

