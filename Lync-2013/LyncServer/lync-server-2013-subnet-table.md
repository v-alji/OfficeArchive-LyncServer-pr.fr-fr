---
title: 'Lync Server 2013 : Table Subnet'
description: 'Lync Server 2013 : table de sous-réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Subnet table
ms:assetid: 76f5c995-96c8-4aa3-bc30-1d74991d7c42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398582(v=OCS.15)
ms:contentKeyID: 48184544
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d30c04ddf897e0a62551709b30211ba724a75cbf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393944"
---
# <a name="subnet-table-in-lync-server-2013"></a><span data-ttu-id="5d982-103">Table Subnet dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d982-103">Subnet table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d982-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d982-104">

<span> </span></span></span>

<span data-ttu-id="5d982-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="5d982-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="5d982-106">La table de sous-réseau est une table de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5d982-106">The Subnet table is a supporting table.</span></span> <span data-ttu-id="5d982-107">Chaque enregistrement représente un sous-réseau défini dans les paramètres de configuration du réseau.</span><span class="sxs-lookup"><span data-stu-id="5d982-107">Each record represents one subnet defined in network configuration setting.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5d982-108"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="5d982-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="5d982-109"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="5d982-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="5d982-110"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="5d982-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="5d982-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="5d982-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d982-112"><strong>SubnetIP</strong></span><span class="sxs-lookup"><span data-stu-id="5d982-112"><strong>SubnetIP</strong></span></span></p></td>
<td><p><span data-ttu-id="5d982-113">int</span><span class="sxs-lookup"><span data-stu-id="5d982-113">int</span></span></p></td>
<td><p><span data-ttu-id="5d982-114">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="5d982-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="5d982-115">Représentation entière de l’adresse IP du sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="5d982-115">Integer representation for the subnet IP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d982-116"><strong>Masque_sous_réseau</strong></span><span class="sxs-lookup"><span data-stu-id="5d982-116"><strong>SubnetMask</strong></span></span></p></td>
<td><p><span data-ttu-id="5d982-117">int</span><span class="sxs-lookup"><span data-stu-id="5d982-117">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5d982-118">Masque de sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="5d982-118">Subnet mask.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d982-119"><strong>UserSiteKey</strong></span><span class="sxs-lookup"><span data-stu-id="5d982-119"><strong>UserSiteKey</strong></span></span></p></td>
<td><p><span data-ttu-id="5d982-120">int</span><span class="sxs-lookup"><span data-stu-id="5d982-120">int</span></span></p></td>
<td><p><span data-ttu-id="5d982-121">Externes</span><span class="sxs-lookup"><span data-stu-id="5d982-121">Foreign</span></span></p></td>
<td><p><span data-ttu-id="5d982-122">Fait référence à partir de la <a href="lync-server-2013-usersite-table.md">table UserSite dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="5d982-122">Referenced from the <a href="lync-server-2013-usersite-table.md">UserSite table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d982-123"><strong>SubnetDescription</strong></span><span class="sxs-lookup"><span data-stu-id="5d982-123"><strong>SubnetDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="5d982-124">nvarchar</span><span class="sxs-lookup"><span data-stu-id="5d982-124">nvarchar(512)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5d982-125">Description du sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="5d982-125">The description for the subnet.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5d982-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d982-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

