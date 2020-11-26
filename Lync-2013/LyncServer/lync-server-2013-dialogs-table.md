---
title: 'Lync Server 2013 : Table Dialogs'
description: 'Tableau Lync Server 2013 : boîtes de dialogue.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dialogs table
ms:assetid: 487a430b-af66-4ea6-b28e-4e33cfdb7f9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425954(v=OCS.15)
ms:contentKeyID: 48184001
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c2c9cf9ec59fc48f7f5ffc6232980e3f8aa68c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429181"
---
# <a name="dialogs-table-in-lync-server-2013"></a><span data-ttu-id="4157d-103">Table Dialogs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4157d-103">Dialogs table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4157d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4157d-104">

<span> </span></span></span>

<span data-ttu-id="4157d-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="4157d-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="4157d-106">Le tableau boîtes de dialogue est une table de prise en charge qui contient les informations sur DialogIDs pour les sessions d’égal à égal.</span><span class="sxs-lookup"><span data-stu-id="4157d-106">The Dialogs table is a supporting table that stores the information about DialogIDs for peer-to-peer sessions.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4157d-107">Colonne</span><span class="sxs-lookup"><span data-stu-id="4157d-107">Column</span></span></th>
<th><span data-ttu-id="4157d-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="4157d-108">Data Type</span></span></th>
<th><span data-ttu-id="4157d-109">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="4157d-109">Key/Index</span></span></th>
<th><span data-ttu-id="4157d-110">Détails</span><span class="sxs-lookup"><span data-stu-id="4157d-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4157d-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="4157d-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="4157d-112">DateHeure</span><span class="sxs-lookup"><span data-stu-id="4157d-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="4157d-113">Principal</span><span class="sxs-lookup"><span data-stu-id="4157d-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="4157d-114">Durée de la demande de session ; utilisé conjointement avec SessionIDSeq pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="4157d-114">Time of session request; used in conjunction with SessionIDSeq to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4157d-115"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="4157d-115"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="4157d-116">int</span><span class="sxs-lookup"><span data-stu-id="4157d-116">int</span></span></p></td>
<td><p><span data-ttu-id="4157d-117">Principal</span><span class="sxs-lookup"><span data-stu-id="4157d-117">Primary</span></span></p></td>
<td><p><span data-ttu-id="4157d-118">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="4157d-118">ID number to identify the session.</span></span> <span data-ttu-id="4157d-119">Utilisé conjointement avec SessionIDTime pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="4157d-119">Used in conjunction with SessionIDTime to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4157d-120"><strong>ExternalChecksum</strong></span><span class="sxs-lookup"><span data-stu-id="4157d-120"><strong>ExternalChecksum</strong></span></span></p></td>
<td><p><span data-ttu-id="4157d-121">int</span><span class="sxs-lookup"><span data-stu-id="4157d-121">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4157d-122">Checksum du ExternalID.</span><span class="sxs-lookup"><span data-stu-id="4157d-122">Checksum of the ExternalID.</span></span> <span data-ttu-id="4157d-123">Ce champ est utilisé pour augmenter la vitesse de recherche de la base de données.</span><span class="sxs-lookup"><span data-stu-id="4157d-123">This field is used to increase the speed of database searches.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4157d-124"><strong>ExternalId</strong></span><span class="sxs-lookup"><span data-stu-id="4157d-124"><strong>ExternalId</strong></span></span></p></td>
<td><p><span data-ttu-id="4157d-125">varbinary (LGA775)</span><span class="sxs-lookup"><span data-stu-id="4157d-125">varbinary(775)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4157d-126">ID de boîte de dialogue SIP, enregistré en tant que fichier binaire.</span><span class="sxs-lookup"><span data-stu-id="4157d-126">SIP dialog ID, stored as a binary.</span></span> <span data-ttu-id="4157d-127">Le format du binaire est le suivant :</span><span class="sxs-lookup"><span data-stu-id="4157d-127">The format of the binary is:</span></span></p>
<p><span data-ttu-id="4157d-128">boîte de dialogue ; à partir d’une balise</span><span class="sxs-lookup"><span data-stu-id="4157d-128">dialog;from-tag;to-tag</span></span></p>
<p><span data-ttu-id="4157d-129">Vous pouvez convertir ces données en format texte à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4157d-129">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(ExternalId as varbinary(max)) as varchar(max))</code></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4157d-130">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4157d-130">


</div>

<span> </span>

</div>

</div>

</span></span></div>

