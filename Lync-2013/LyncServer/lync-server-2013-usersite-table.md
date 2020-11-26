---
title: 'Lync Server 2013 : Table UserSite'
description: 'Tableau Lync Server 2013 : UserSite'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserSite table
ms:assetid: 1c2a3cf2-dc05-472e-8097-a31f3a1aafcb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398256(v=OCS.15)
ms:contentKeyID: 48183552
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e0fb3149b9378bbfd3f14da8176eed226e4f57f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436110"
---
# <a name="usersite-table-in-lync-server-2013"></a><span data-ttu-id="c6172-103">Table UserSite dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c6172-103">UserSite table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c6172-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c6172-104">

<span> </span></span></span>

<span data-ttu-id="c6172-105">_**Dernière modification de la rubrique :** 2010-11-09_</span><span class="sxs-lookup"><span data-stu-id="c6172-105">_**Topic Last Modified:** 2010-11-09_</span></span>

<span data-ttu-id="c6172-106">La table UserSite est une table de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c6172-106">The UserSite table is a supporting table.</span></span> <span data-ttu-id="c6172-107">Chaque enregistrement représente un site d’utilisateur défini dans les paramètres de configuration réseau.</span><span class="sxs-lookup"><span data-stu-id="c6172-107">Each record represents one user site defined in network configuration setting.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c6172-108"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="c6172-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="c6172-109"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="c6172-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="c6172-110"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="c6172-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="c6172-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="c6172-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6172-112"><strong>UserSiteKey</strong></span><span class="sxs-lookup"><span data-stu-id="c6172-112"><strong>UserSiteKey</strong></span></span></p></td>
<td><p><span data-ttu-id="c6172-113">int</span><span class="sxs-lookup"><span data-stu-id="c6172-113">int</span></span></p></td>
<td><p><span data-ttu-id="c6172-114">Principal</span><span class="sxs-lookup"><span data-stu-id="c6172-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="c6172-115">Numéro unique identifiant le site de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c6172-115">Unique number identifying the user site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6172-116"><strong>UserSiteName</strong></span><span class="sxs-lookup"><span data-stu-id="c6172-116"><strong>UserSiteName</strong></span></span></p></td>
<td><p><span data-ttu-id="c6172-117">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="c6172-117">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="c6172-118">Différent</span><span class="sxs-lookup"><span data-stu-id="c6172-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="c6172-119">Nom du site de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c6172-119">User site’s name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6172-120"><strong>RegionKey</strong></span><span class="sxs-lookup"><span data-stu-id="c6172-120"><strong>RegionKey</strong></span></span></p></td>
<td><p><span data-ttu-id="c6172-121">int</span><span class="sxs-lookup"><span data-stu-id="c6172-121">int</span></span></p></td>
<td><p><span data-ttu-id="c6172-122">Externes</span><span class="sxs-lookup"><span data-stu-id="c6172-122">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c6172-123">Référencé à partir de la <a href="lync-server-2013-region-table.md">table région dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="c6172-123">Referenced from <a href="lync-server-2013-region-table.md">Region table in Lync Server 2013</a>.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c6172-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c6172-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

