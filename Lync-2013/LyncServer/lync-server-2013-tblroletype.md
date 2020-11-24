---
title: 'Lync Server 2013 : tblRoleType'
description: 'Lync Server 2013 : tblRoleType.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblRoleType
ms:assetid: 1eac3a54-656a-40ac-b771-edfc64d6e34b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558623(v=OCS.15)
ms:contentKeyID: 48183577
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f458259acaee7821d5f6a7339b993c70fe65f595
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393912"
---
# <a name="tblroletype-in-lync-server-2013"></a><span data-ttu-id="c66e4-103">tblRoleType dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c66e4-103">tblRoleType in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c66e4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c66e4-104">

<span> </span></span></span>

<span data-ttu-id="c66e4-105">_**Dernière modification de la rubrique :** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="c66e4-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="c66e4-106">tblRoleType est une table de recherche statique avec les types de rôles et leurs jeux d’autorisations associés.</span><span class="sxs-lookup"><span data-stu-id="c66e4-106">tblRoleType is a static lookup table with role types and their associated permission sets.</span></span>

### <a name="columns"></a><span data-ttu-id="c66e4-107">Celles</span><span class="sxs-lookup"><span data-stu-id="c66e4-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c66e4-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="c66e4-108">Column</span></span></th>
<th><span data-ttu-id="c66e4-109">Type</span><span class="sxs-lookup"><span data-stu-id="c66e4-109">Type</span></span></th>
<th><span data-ttu-id="c66e4-110">Description</span><span class="sxs-lookup"><span data-stu-id="c66e4-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c66e4-111">rtypeID</span><span class="sxs-lookup"><span data-stu-id="c66e4-111">rtypeID</span></span></p></td>
<td><p><span data-ttu-id="c66e4-112">ent, non null</span><span class="sxs-lookup"><span data-stu-id="c66e4-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="c66e4-113">ID du type de rôle.</span><span class="sxs-lookup"><span data-stu-id="c66e4-113">Role type ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c66e4-114">rtypeDesc</span><span class="sxs-lookup"><span data-stu-id="c66e4-114">rtypeDesc</span></span></p></td>
<td><p><span data-ttu-id="c66e4-115">nvarchar (256), pas null</span><span class="sxs-lookup"><span data-stu-id="c66e4-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="c66e4-116">Description du type de rôle.</span><span class="sxs-lookup"><span data-stu-id="c66e4-116">Role type description.</span></span> <span data-ttu-id="c66e4-117">Il existe quatre rôles disponibles :</span><span class="sxs-lookup"><span data-stu-id="c66e4-117">There are four available roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="c66e4-118">Membre : membres de salle de conversation</span><span class="sxs-lookup"><span data-stu-id="c66e4-118">Member: Chat room member</span></span></p></li>
<li><p><span data-ttu-id="c66e4-119">Manager : gestionnaire de salle de conversation</span><span class="sxs-lookup"><span data-stu-id="c66e4-119">Manager: Chat room manager</span></span></p></li>
<li><p><span data-ttu-id="c66e4-120">Voix : présentateur pour une salle de conversation Auditorium</span><span class="sxs-lookup"><span data-stu-id="c66e4-120">Voiced: Presenter for an auditorium chat room</span></span></p></li>
<li><p><span data-ttu-id="c66e4-121">Créateur : peut créer des salles de conversation</span><span class="sxs-lookup"><span data-stu-id="c66e4-121">Creator: Can create chat rooms</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c66e4-122">rtypeAllowedPermSet</span><span class="sxs-lookup"><span data-stu-id="c66e4-122">rtypeAllowedPermSet</span></span></p></td>
<td><p><span data-ttu-id="c66e4-123">bigint, pas null</span><span class="sxs-lookup"><span data-stu-id="c66e4-123">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="c66e4-124">Autorisation définie pour le rôle.</span><span class="sxs-lookup"><span data-stu-id="c66e4-124">Permission set for the role.</span></span> <span data-ttu-id="c66e4-125">Les bits utilisés sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="c66e4-125">The used bits are:</span></span></p>
<ul>
<li><p><span data-ttu-id="c66e4-126">2 : true si le rôle peut gérer des nœuds.</span><span class="sxs-lookup"><span data-stu-id="c66e4-126">2: True if the role can manage nodes.</span></span></p></li>
<li><p><span data-ttu-id="c66e4-127">4 : true si le rôle peut créer des nœuds enfants.</span><span class="sxs-lookup"><span data-stu-id="c66e4-127">4: True if the role can create children nodes.</span></span></p></li>
<li><p><span data-ttu-id="c66e4-128">7 : true si le rôle peut rejoindre une salle de conversation (ou des salles de conversation enfant d’une catégorie).</span><span class="sxs-lookup"><span data-stu-id="c66e4-128">7: True if the role can join a chat room (or children chat rooms of a category).</span></span></p></li>
<li><p><span data-ttu-id="c66e4-129">8 : true si le rôle peut discuter dans une salle de conversation (ou dans des salles de conversation enfant d’une catégorie).</span><span class="sxs-lookup"><span data-stu-id="c66e4-129">8: True if the role can chat in a chat room (or in children chat rooms of a category).</span></span></p></li>
<li><p><span data-ttu-id="c66e4-130">10 : true si le rôle peut lire l’historique des conversations même en l’absence de participation à une salle de conversation.</span><span class="sxs-lookup"><span data-stu-id="c66e4-130">10: True if the role can read chat history even when not joined to a chat room.</span></span></p></li>
<li><p><span data-ttu-id="c66e4-131">11 : true si le rôle peut voir la salle de conversation.</span><span class="sxs-lookup"><span data-stu-id="c66e4-131">11: True if the role can see the chat room.</span></span> <span data-ttu-id="c66e4-132">(Cette valeur est améliorée par des facteurs tels que Scope et Visibility.)</span><span class="sxs-lookup"><span data-stu-id="c66e4-132">(This is further refined by factors such as scope and visibility.)</span></span></p></li>
<li><p><span data-ttu-id="c66e4-133">12 : true si le rôle peut discuter dans une salle de conversation Auditorium.</span><span class="sxs-lookup"><span data-stu-id="c66e4-133">12: True if the role can chat in an auditorium chat room.</span></span></p></li>
<li><p><span data-ttu-id="c66e4-134">13 : true si le rôle peut ignorer les règles de visibilité lors de la consultation des nœuds.</span><span class="sxs-lookup"><span data-stu-id="c66e4-134">13: True if the role can bypass visibility rules when viewing nodes.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="c66e4-135">Clé</span><span class="sxs-lookup"><span data-stu-id="c66e4-135">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c66e4-136">Colonne</span><span class="sxs-lookup"><span data-stu-id="c66e4-136">Column</span></span></th>
<th><span data-ttu-id="c66e4-137">Description</span><span class="sxs-lookup"><span data-stu-id="c66e4-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c66e4-138">rtypeID</span><span class="sxs-lookup"><span data-stu-id="c66e4-138">rtypeID</span></span></p></td>
<td><p><span data-ttu-id="c66e4-139">Clé primaire.</span><span class="sxs-lookup"><span data-stu-id="c66e4-139">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c66e4-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c66e4-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

