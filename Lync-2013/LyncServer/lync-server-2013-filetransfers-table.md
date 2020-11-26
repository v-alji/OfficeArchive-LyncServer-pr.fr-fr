---
title: 'Lync Server 2013 : Table FileTransfers'
description: 'Tableau Lync Server 2013 : FileTransfers'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FileTransfers table
ms:assetid: 5368e67c-d8a9-43a1-9472-a839950dedb3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398353(v=OCS.15)
ms:contentKeyID: 48184118
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ccde45fa3743a809499273676d567846ef292ecc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428166"
---
# <a name="filetransfers-table-in-lync-server-2013"></a><span data-ttu-id="9d0ce-103">Table FileTransfers dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9d0ce-103">FileTransfers table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9d0ce-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9d0ce-104">

<span> </span></span></span>

<span data-ttu-id="9d0ce-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="9d0ce-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="9d0ce-106">Chaque enregistrement représente une session de transfert de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9d0ce-106">Each record represents one file transfer session.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d0ce-107">Colonne</span><span class="sxs-lookup"><span data-stu-id="9d0ce-107">Column</span></span></th>
<th><span data-ttu-id="9d0ce-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="9d0ce-108">Data Type</span></span></th>
<th><span data-ttu-id="9d0ce-109">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="9d0ce-109">Key/Index</span></span></th>
<th><span data-ttu-id="9d0ce-110">Détails</span><span class="sxs-lookup"><span data-stu-id="9d0ce-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d0ce-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="9d0ce-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9d0ce-112">DateHeure</span><span class="sxs-lookup"><span data-stu-id="9d0ce-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="9d0ce-113">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="9d0ce-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d0ce-114">Durée de la demande de session.</span><span class="sxs-lookup"><span data-stu-id="9d0ce-114">Time of session request.</span></span> <span data-ttu-id="9d0ce-115">Utilisé conjointement avec <strong>SessionIdSeq</strong> pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="9d0ce-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="9d0ce-116">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9d0ce-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d0ce-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="9d0ce-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="9d0ce-118">int</span><span class="sxs-lookup"><span data-stu-id="9d0ce-118">int</span></span></p></td>
<td><p><span data-ttu-id="9d0ce-119">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="9d0ce-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d0ce-120">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="9d0ce-120">ID number to identify the session.</span></span> <span data-ttu-id="9d0ce-121">Utilisé conjointement avec <strong>SessionIdTime</strong> pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="9d0ce-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="9d0ce-122">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9d0ce-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d0ce-123"><strong>Nom de fichier</strong></span><span class="sxs-lookup"><span data-stu-id="9d0ce-123"><strong>File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="9d0ce-124">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9d0ce-124">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d0ce-125">Nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="9d0ce-125">Name of the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d0ce-126"><strong>FileIdentity</strong></span><span class="sxs-lookup"><span data-stu-id="9d0ce-126"><strong>FileIdentity</strong></span></span></p></td>
<td><p><span data-ttu-id="9d0ce-127">identificateur</span><span class="sxs-lookup"><span data-stu-id="9d0ce-127">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d0ce-128">Identificateur unique permettant de faire la distinction entre les transferts de fichiers impliquant le même nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="9d0ce-128">Unique identifier to distinguish between file transfers involving the same file name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d0ce-129"><strong>Sans</strong></span><span class="sxs-lookup"><span data-stu-id="9d0ce-129"><strong>Cookie</strong></span></span></p></td>
<td><p><span data-ttu-id="9d0ce-130">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="9d0ce-130">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="9d0ce-131">Principal</span><span class="sxs-lookup"><span data-stu-id="9d0ce-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="9d0ce-132">Permet de détecter chaque message de suivi associé à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="9d0ce-132">Used to identify every follow-up message as being associated with this one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d0ce-133"><strong>Valide</strong></span><span class="sxs-lookup"><span data-stu-id="9d0ce-133"><strong>Accept</strong></span></span></p></td>
<td><p><span data-ttu-id="9d0ce-134">bit</span><span class="sxs-lookup"><span data-stu-id="9d0ce-134">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d0ce-135">Peut être vrai ou nul.</span><span class="sxs-lookup"><span data-stu-id="9d0ce-135">Can be TRUE or NULL.</span></span> <span data-ttu-id="9d0ce-136">Si vrai, l’argument refuser et annuler est nul.</span><span class="sxs-lookup"><span data-stu-id="9d0ce-136">If TRUE, then Reject and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d0ce-137"><strong>Rejeter</strong></span><span class="sxs-lookup"><span data-stu-id="9d0ce-137"><strong>Reject</strong></span></span></p></td>
<td><p><span data-ttu-id="9d0ce-138">bit</span><span class="sxs-lookup"><span data-stu-id="9d0ce-138">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d0ce-139">Peut être vrai ou nul.</span><span class="sxs-lookup"><span data-stu-id="9d0ce-139">Can be TRUE or NULL.</span></span> <span data-ttu-id="9d0ce-140">Si vrai, l’argument accepter et annuler est nul.</span><span class="sxs-lookup"><span data-stu-id="9d0ce-140">If TRUE, then Accept and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d0ce-141"><strong>Annuler</strong></span><span class="sxs-lookup"><span data-stu-id="9d0ce-141"><strong>Cancel</strong></span></span></p></td>
<td><p><span data-ttu-id="9d0ce-142">bit</span><span class="sxs-lookup"><span data-stu-id="9d0ce-142">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d0ce-143">Peut être vrai ou nul.</span><span class="sxs-lookup"><span data-stu-id="9d0ce-143">Can be TRUE or NULL.</span></span> <span data-ttu-id="9d0ce-144">Si vrai, l’argument accepter et refuser est nul.</span><span class="sxs-lookup"><span data-stu-id="9d0ce-144">If TRUE, then Accept and Reject will be NULL.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9d0ce-145">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9d0ce-145">


</div>

<span> </span>

</div>

</div>

</span></span></div>

