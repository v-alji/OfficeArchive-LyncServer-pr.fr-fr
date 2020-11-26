---
title: 'Lync Server 2013 : Table Devices'
description: 'Tableau Lync Server 2013 : Devices.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Devices table
ms:assetid: 532e2280-4bbc-4a6c-93da-45d9f80a30a0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398351(v=OCS.15)
ms:contentKeyID: 48184169
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 763e1788e2874f9f9831c089ffe8fa077621b030
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429338"
---
# <a name="devices-table-in-lync-server-2013"></a><span data-ttu-id="0adaf-103">Table Devices dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0adaf-103">Devices table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0adaf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0adaf-104">

<span> </span></span></span>

<span data-ttu-id="0adaf-105">_**Dernière modification de la rubrique :** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="0adaf-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="0adaf-106">Le tableau appareils est une table de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0adaf-106">The Devices table is a supporting table.</span></span> <span data-ttu-id="0adaf-107">Chaque enregistrement stocke des informations sur un appareil (téléphone de bureau).</span><span class="sxs-lookup"><span data-stu-id="0adaf-107">Each record stores information about one device (desk phone).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0adaf-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="0adaf-108">Column</span></span></th>
<th><span data-ttu-id="0adaf-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="0adaf-109">Data Type</span></span></th>
<th><span data-ttu-id="0adaf-110">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="0adaf-110">Key/Index</span></span></th>
<th><span data-ttu-id="0adaf-111">Détails</span><span class="sxs-lookup"><span data-stu-id="0adaf-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0adaf-112"><strong>DeviceId</strong></span><span class="sxs-lookup"><span data-stu-id="0adaf-112"><strong>DeviceId</strong></span></span></p></td>
<td><p><span data-ttu-id="0adaf-113">int</span><span class="sxs-lookup"><span data-stu-id="0adaf-113">int</span></span></p></td>
<td><p><span data-ttu-id="0adaf-114">Principal</span><span class="sxs-lookup"><span data-stu-id="0adaf-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="0adaf-115">Numéro unique identifiant cette version matérielle.</span><span class="sxs-lookup"><span data-stu-id="0adaf-115">Unique number identifying this hardware version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0adaf-116"><strong>ManufacturerId</strong></span><span class="sxs-lookup"><span data-stu-id="0adaf-116"><strong>ManufacturerId</strong></span></span></p></td>
<td><p><span data-ttu-id="0adaf-117">int</span><span class="sxs-lookup"><span data-stu-id="0adaf-117">int</span></span></p></td>
<td><p><span data-ttu-id="0adaf-118">Externes</span><span class="sxs-lookup"><span data-stu-id="0adaf-118">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0adaf-119">Fabricant de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="0adaf-119">Manufacturer of this device.</span></span> <span data-ttu-id="0adaf-120">Pour plus d’informations, reportez-vous <a href="lync-server-2013-manufacturers-table.md">à la table fabricants dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0adaf-120">See the <a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0adaf-121"><strong>HardwareVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="0adaf-121"><strong>HardwareVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="0adaf-122">int</span><span class="sxs-lookup"><span data-stu-id="0adaf-122">int</span></span></p></td>
<td><p><span data-ttu-id="0adaf-123">Externes</span><span class="sxs-lookup"><span data-stu-id="0adaf-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0adaf-124">Version matérielle de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="0adaf-124">Hardware version of this device.</span></span> <span data-ttu-id="0adaf-125">Pour plus d’informations, voir la <a href="lync-server-2013-hardwareversions-table.md">table HardwareVersions dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0adaf-125">See the <a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0adaf-126"><strong>MacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="0adaf-126"><strong>MacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="0adaf-127">bigint</span><span class="sxs-lookup"><span data-stu-id="0adaf-127">bigint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0adaf-128">Adresse MAC</span><span class="sxs-lookup"><span data-stu-id="0adaf-128">MAC Address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0adaf-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0adaf-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

