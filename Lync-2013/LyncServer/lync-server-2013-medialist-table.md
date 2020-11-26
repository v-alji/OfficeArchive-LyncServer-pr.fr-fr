---
title: 'Lync Server 2013 : Table MediaList'
description: 'Lync Server 2013 : table de médiane.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaList table
ms:assetid: 1f440590-c1bc-483e-b7bc-6cc763847768
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398279(v=OCS.15)
ms:contentKeyID: 48183579
ms.date: 07/12/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e54535cd4a081657e7dcd59446cf65aaa3af7cd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445924"
---
# <a name="medialist-table-in-lync-server-2013"></a><span data-ttu-id="c9c5a-103">Table MediaList dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c9c5a-103">MediaList table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c9c5a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c9c5a-104">

<span> </span></span></span>

<span data-ttu-id="c9c5a-105">_**Dernière modification de la rubrique :** 2016-07-12_</span><span class="sxs-lookup"><span data-stu-id="c9c5a-105">_**Topic Last Modified:** 2016-07-12_</span></span>

<span data-ttu-id="c9c5a-106">La table MediaList est une table statique qui stocke la liste de divers types de médias.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-106">The MediaList table is a static table that stores the list of various media types.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9c5a-107">Colonne</span><span class="sxs-lookup"><span data-stu-id="c9c5a-107">Column</span></span></th>
<th><span data-ttu-id="c9c5a-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="c9c5a-108">Data Type</span></span></th>
<th><span data-ttu-id="c9c5a-109">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="c9c5a-109">Key/Index</span></span></th>
<th><span data-ttu-id="c9c5a-110">Détails</span><span class="sxs-lookup"><span data-stu-id="c9c5a-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9c5a-111"><strong>MediaId</strong></span><span class="sxs-lookup"><span data-stu-id="c9c5a-111"><strong>MediaId</strong></span></span></p></td>
<td><p><span data-ttu-id="c9c5a-112">tinyint</span><span class="sxs-lookup"><span data-stu-id="c9c5a-112">tinyint</span></span></p></td>
<td><p><span data-ttu-id="c9c5a-113">Principal</span><span class="sxs-lookup"><span data-stu-id="c9c5a-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="c9c5a-114">Valeur : 1-7</span><span class="sxs-lookup"><span data-stu-id="c9c5a-114">Values: 1-7</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9c5a-115"><strong>Media</strong></span><span class="sxs-lookup"><span data-stu-id="c9c5a-115"><strong>Media</strong></span></span></p></td>
<td><p><span data-ttu-id="c9c5a-116">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c9c5a-116">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9c5a-117">Mappage statique de MediaID et des valeurs média :</span><span class="sxs-lookup"><span data-stu-id="c9c5a-117">Static mapping of MediaID and Media values:</span></span></p>
<ul>
<li><p><span data-ttu-id="c9c5a-118">1-MESSAGE INSTANTANÉ</span><span class="sxs-lookup"><span data-stu-id="c9c5a-118">1 – IM</span></span></p></li>
<li><p><span data-ttu-id="c9c5a-119">2 – Transfert de fichiers</span><span class="sxs-lookup"><span data-stu-id="c9c5a-119">2 – File Transfer</span></span></p></li>
<li><p><span data-ttu-id="c9c5a-120">3 – Assistance à distance</span><span class="sxs-lookup"><span data-stu-id="c9c5a-120">3 – Remote Assistance</span></span></p></li>
<li><p><span data-ttu-id="c9c5a-121">4 – Partage d’application</span><span class="sxs-lookup"><span data-stu-id="c9c5a-121">4 – Application Sharing</span></span></p></li>
<li><p><span data-ttu-id="c9c5a-122">5-audio</span><span class="sxs-lookup"><span data-stu-id="c9c5a-122">5 – Audio</span></span></p></li>
<li><p><span data-ttu-id="c9c5a-123">6-vidéo</span><span class="sxs-lookup"><span data-stu-id="c9c5a-123">6 – Video</span></span></p></li>
<li><p><span data-ttu-id="c9c5a-124">7 – Invitation d’application</span><span class="sxs-lookup"><span data-stu-id="c9c5a-124">7 – App Invite</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c9c5a-125">Si vous tentez de déterminer le type de modalité pour les valeurs dans LcsCDR.SessionDetailsView.MediaTypes, vous devrez utiliser l’extrait de Joindre suivant : </span><span class="sxs-lookup"><span data-stu-id="c9c5a-125">If you are trying to determine the modality type for the values in LcsCDR.SessionDetailsView.MediaTypes, then you need to use the following Join snippet:</span></span>

    LEFT JOIN on Media.MediaId = MediaList.MediaId

<span data-ttu-id="c9c5a-126"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c9c5a-126"></div>

<span> </span>

</div>

</div>

</span></span></div>

