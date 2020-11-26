---
title: 'Lync Server 2013 : Table Endpoint'
description: 'Tableau Lync Server 2013 : Endpoint.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Endpoint table
ms:assetid: 500f330d-4d7d-4e88-b1cc-fef9a9de6b5c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398327(v=OCS.15)
ms:contentKeyID: 48184098
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 614872eee41b5d8e56da4b96cf5bbe3a4a1cf4d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428677"
---
# <a name="endpoint-table-in-lync-server-2013"></a><span data-ttu-id="1c084-103">Table Endpoint dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1c084-103">Endpoint table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1c084-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1c084-104">

<span> </span></span></span>

<span data-ttu-id="1c084-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="1c084-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="1c084-106">La table Endpoint est une table qui contient des informations sur les points de terminaison ayant participé à des sessions enregistrées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="1c084-106">The Endpoint table is a supporting table that stores information about the endpoints that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="1c084-107">Chaque enregistrement de la table représente un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1c084-107">Each record in the table represents one endpoint.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c084-108"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="1c084-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="1c084-109"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="1c084-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="1c084-110"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="1c084-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="1c084-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="1c084-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c084-112"><strong>EndpointKey</strong></span><span class="sxs-lookup"><span data-stu-id="1c084-112"><strong>EndpointKey</strong></span></span></p></td>
<td><p><span data-ttu-id="1c084-113">int</span><span class="sxs-lookup"><span data-stu-id="1c084-113">int</span></span></p></td>
<td><p><span data-ttu-id="1c084-114">Principal</span><span class="sxs-lookup"><span data-stu-id="1c084-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="1c084-115">Numéro unique identifiant ce point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1c084-115">Unique number identifying this endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c084-116"><strong>Nom</strong></span><span class="sxs-lookup"><span data-stu-id="1c084-116"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="1c084-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1c084-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1c084-118">Différent</span><span class="sxs-lookup"><span data-stu-id="1c084-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="1c084-119">Nom du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1c084-119">Endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c084-120"><strong>OS</strong></span><span class="sxs-lookup"><span data-stu-id="1c084-120"><strong>OS</strong></span></span></p></td>
<td><p><span data-ttu-id="1c084-121">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="1c084-121">nvarchar(128)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1c084-122">Système d’exploitation (se) du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1c084-122">Operating system (OS) of the endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c084-123"><strong>CPUName</strong></span><span class="sxs-lookup"><span data-stu-id="1c084-123"><strong>CPUName</strong></span></span></p></td>
<td><p><span data-ttu-id="1c084-124">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="1c084-124">nvarchar(128)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1c084-125">Nom de l’UC du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1c084-125">CPU name of the endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c084-126"><strong>CPUNumberOfCores</strong></span><span class="sxs-lookup"><span data-stu-id="1c084-126"><strong>CPUNumberOfCores</strong></span></span></p></td>
<td><p><span data-ttu-id="1c084-127">type</span><span class="sxs-lookup"><span data-stu-id="1c084-127">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1c084-128">Nombre de cœurs d’UC du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1c084-128">Number of CPU cores of the endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c084-129"><strong>CPUProcessorSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="1c084-129"><strong>CPUProcessorSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="1c084-130">int</span><span class="sxs-lookup"><span data-stu-id="1c084-130">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1c084-131">Vitesse de processeur de l’UC du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1c084-131">CPU processor speed of the endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c084-132"><strong>VirtualizationFlag</strong></span><span class="sxs-lookup"><span data-stu-id="1c084-132"><strong>VirtualizationFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="1c084-133">tinyint</span><span class="sxs-lookup"><span data-stu-id="1c084-133">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1c084-134">Indicateur binaire indiquant si le système s’exécute dans un environnement virtualisé :</span><span class="sxs-lookup"><span data-stu-id="1c084-134">Bit flag that indicates if the system is running in a virtualized environment:</span></span></p>
<ul>
<li><p><span data-ttu-id="1c084-135">0x0000 – aucun</span><span class="sxs-lookup"><span data-stu-id="1c084-135">0x0000 – None</span></span></p></li>
<li><p><span data-ttu-id="1c084-136">0x0001 – HyperV</span><span class="sxs-lookup"><span data-stu-id="1c084-136">0x0001 – HyperV</span></span></p></li>
<li><p><span data-ttu-id="1c084-137">0x0002 – VMWare</span><span class="sxs-lookup"><span data-stu-id="1c084-137">0x0002 – VMWare</span></span></p></li>
<li><p><span data-ttu-id="1c084-138">0x0004 – PC virtuel</span><span class="sxs-lookup"><span data-stu-id="1c084-138">0x0004 – Virtual PC</span></span></p></li>
<li><p><span data-ttu-id="1c084-139">0x0008-Xen PC</span><span class="sxs-lookup"><span data-stu-id="1c084-139">0x0008 – Xen PC</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="1c084-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1c084-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

