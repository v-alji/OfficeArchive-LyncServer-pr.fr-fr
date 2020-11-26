---
title: 'Lync Server 2013 : tblFileToken'
description: 'Lync Server 2013 : tblFileToken.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblFileToken
ms:assetid: 49e7dd79-1607-443c-818a-88c160e4ed06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558646(v=OCS.15)
ms:contentKeyID: 48184073
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c0a0465bd769cff5c23c00a98f79e2346232175
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423532"
---
# <a name="tblfiletoken-in-lync-server-2013"></a><span data-ttu-id="a0f5a-103">tblFileToken dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0f5a-103">tblFileToken in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0f5a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0f5a-104">

<span> </span></span></span>

<span data-ttu-id="a0f5a-105">_**Dernière modification de la rubrique :** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="a0f5a-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="a0f5a-106">tblFileToken contient des jetons temporaires aux fins de transfert de fichiers.</span><span class="sxs-lookup"><span data-stu-id="a0f5a-106">tblFileToken contains temporary tokens for file transfer purposes.</span></span>

### <a name="columns"></a><span data-ttu-id="a0f5a-107">Celles</span><span class="sxs-lookup"><span data-stu-id="a0f5a-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0f5a-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="a0f5a-108">Column</span></span></th>
<th><span data-ttu-id="a0f5a-109">Type</span><span class="sxs-lookup"><span data-stu-id="a0f5a-109">Type</span></span></th>
<th><span data-ttu-id="a0f5a-110">Description</span><span class="sxs-lookup"><span data-stu-id="a0f5a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0f5a-111">fileToken</span><span class="sxs-lookup"><span data-stu-id="a0f5a-111">fileToken</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-112">nvarchar (50), pas null</span><span class="sxs-lookup"><span data-stu-id="a0f5a-112">nvarchar (50), not null</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-113">Jeton unique (GUID).</span><span class="sxs-lookup"><span data-stu-id="a0f5a-113">Unique token (a GUID).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0f5a-114">fileTokenUserID</span><span class="sxs-lookup"><span data-stu-id="a0f5a-114">fileTokenUserID</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-115">ent, non null</span><span class="sxs-lookup"><span data-stu-id="a0f5a-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-116">ID du principal qui transfère le fichier.</span><span class="sxs-lookup"><span data-stu-id="a0f5a-116">ID of the principal that is transferring the file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0f5a-117">fileTokenChannelID</span><span class="sxs-lookup"><span data-stu-id="a0f5a-117">fileTokenChannelID</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-118">GUID, pas null</span><span class="sxs-lookup"><span data-stu-id="a0f5a-118">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-119">GUID du nœud de salle de conversation.</span><span class="sxs-lookup"><span data-stu-id="a0f5a-119">GUID of the chat room node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0f5a-120">fileTokenExpireDate</span><span class="sxs-lookup"><span data-stu-id="a0f5a-120">fileTokenExpireDate</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-121">DATEHEURE, pas null</span><span class="sxs-lookup"><span data-stu-id="a0f5a-121">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-122">Durée d’expiration.</span><span class="sxs-lookup"><span data-stu-id="a0f5a-122">Expiration time.</span></span> <span data-ttu-id="a0f5a-123">(Les jetons expirent au bout de 30 minutes, sauf s’ils sont épinglés (voir les descriptions suivies dans cette colonne).</span><span class="sxs-lookup"><span data-stu-id="a0f5a-123">(Tokens expire after 30 minutes, unless pinned (see the following descriptions in this column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0f5a-124">fileTokenComplianceFileUrl</span><span class="sxs-lookup"><span data-stu-id="a0f5a-124">fileTokenComplianceFileUrl</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-125">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="a0f5a-125">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-126">URL du fichier transféré (pour une utilisation du service de conformité).</span><span class="sxs-lookup"><span data-stu-id="a0f5a-126">URL of the transferred file (for Compliance service use).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0f5a-127">fileTokenComplianceThumbnailUrl</span><span class="sxs-lookup"><span data-stu-id="a0f5a-127">fileTokenComplianceThumbnailUrl</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="a0f5a-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-129">URL de la miniature du fichier transféré (pour une utilisation du service de conformité).</span><span class="sxs-lookup"><span data-stu-id="a0f5a-129">URL of the thumbnail for the transferred file (for Compliance service use).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0f5a-130">fileTokenComplianceTime</span><span class="sxs-lookup"><span data-stu-id="a0f5a-130">fileTokenComplianceTime</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-131">datetime2</span><span class="sxs-lookup"><span data-stu-id="a0f5a-131">datetime2</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-132">Horodatage de l’opération de transfert de fichiers réelle (pour l’utilisation du service de conformité).</span><span class="sxs-lookup"><span data-stu-id="a0f5a-132">Timestamp for the actual file transfer operation (for Compliance service use).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0f5a-133">fileTokenComplianceIsUpload</span><span class="sxs-lookup"><span data-stu-id="a0f5a-133">fileTokenComplianceIsUpload</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-134">bit</span><span class="sxs-lookup"><span data-stu-id="a0f5a-134">bit</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-135">True si Télécharger ; Faux si Télécharger (pour une utilisation du service de conformité).</span><span class="sxs-lookup"><span data-stu-id="a0f5a-135">True if upload; False if download (for Compliance service use).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0f5a-136">fileTokenCompliancePinned</span><span class="sxs-lookup"><span data-stu-id="a0f5a-136">fileTokenCompliancePinned</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-137">bit, pas null</span><span class="sxs-lookup"><span data-stu-id="a0f5a-137">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-138">True si le jeton est épinglé.</span><span class="sxs-lookup"><span data-stu-id="a0f5a-138">True if token is pinned.</span></span> <span data-ttu-id="a0f5a-139">Il est utilisé pour conserver le jeton dans le tableau jusqu’à ce que le service de conformité puisse récupérer les champs appropriés.</span><span class="sxs-lookup"><span data-stu-id="a0f5a-139">It’s used to keep the token in the table until Compliance service has a chance to retrieve the relevant fields from it.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="a0f5a-140">Permettent</span><span class="sxs-lookup"><span data-stu-id="a0f5a-140">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0f5a-141">Colonne</span><span class="sxs-lookup"><span data-stu-id="a0f5a-141">Column</span></span></th>
<th><span data-ttu-id="a0f5a-142">Description</span><span class="sxs-lookup"><span data-stu-id="a0f5a-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0f5a-143">fileToken</span><span class="sxs-lookup"><span data-stu-id="a0f5a-143">fileToken</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-144">Clé primaire.</span><span class="sxs-lookup"><span data-stu-id="a0f5a-144">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0f5a-145">fileTokenChannelID</span><span class="sxs-lookup"><span data-stu-id="a0f5a-145">fileTokenChannelID</span></span></p></td>
<td><p><span data-ttu-id="a0f5a-146">Clé étrangère avec recherche dans la table tblNode. nodeGuid.</span><span class="sxs-lookup"><span data-stu-id="a0f5a-146">Foreign key with lookup in tblNode.nodeGuid table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a0f5a-147">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0f5a-147">


</div>

<span> </span>

</div>

</div>

</span></span></div>

