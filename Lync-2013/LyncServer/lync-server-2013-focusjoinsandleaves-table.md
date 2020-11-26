---
title: 'Lync Server 2013 : Table FocusJoinsAndLeaves'
description: 'Tableau Lync Server 2013 : FocusJoinsAndLeaves'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FocusJoinsAndLeaves table
ms:assetid: e6f0212c-67e9-4061-8720-d0296e855991
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399026(v=OCS.15)
ms:contentKeyID: 48185690
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5796de16ed204ce4f33935d937cbaa425d63a67f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428105"
---
# <a name="focusjoinsandleaves-table-in-lync-server-2013"></a><span data-ttu-id="56d0d-103">Table FocusJoinsAndLeaves dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="56d0d-103">FocusJoinsAndLeaves table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="56d0d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="56d0d-104">

<span> </span></span></span>

<span data-ttu-id="56d0d-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="56d0d-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="56d0d-106">Chaque enregistrement de cette table contient les informations CDR relatives à la jointure d’un utilisateur et laisse des informations pour une seule conférence.</span><span class="sxs-lookup"><span data-stu-id="56d0d-106">Each record in this table contains the CDR information about one user’s join and leave information for one conference.</span></span> <span data-ttu-id="56d0d-107">Chaque conférence est représentée dans ce tableau par un seul enregistrement pour chaque fois qu’un utilisateur rejoint et quitte la Conférence.</span><span class="sxs-lookup"><span data-stu-id="56d0d-107">Each conference is represented in this table by one record for each time a user joins and leaves the conference.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56d0d-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="56d0d-108">Column</span></span></th>
<th><span data-ttu-id="56d0d-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="56d0d-109">Data Type</span></span></th>
<th><span data-ttu-id="56d0d-110">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="56d0d-110">Key/Index</span></span></th>
<th><span data-ttu-id="56d0d-111">Détails</span><span class="sxs-lookup"><span data-stu-id="56d0d-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56d0d-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="56d0d-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="56d0d-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="56d0d-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="56d0d-114">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="56d0d-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="56d0d-115">Durée de l’instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="56d0d-115">Time of conference instance.</span></span> <span data-ttu-id="56d0d-116">Utilisé conjointement avec <strong>SessionIdSeq</strong> pour identifier de manière unique une instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="56d0d-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="56d0d-117">Pour plus d’informations, voir le <a href="lync-server-2013-conferences-table.md">tableau conférences dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56d0d-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56d0d-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="56d0d-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="56d0d-119">int</span><span class="sxs-lookup"><span data-stu-id="56d0d-119">int</span></span></p></td>
<td><p><span data-ttu-id="56d0d-120">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="56d0d-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="56d0d-121">Numéro d’identification pour identifier l’instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="56d0d-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="56d0d-122">Utilisé conjointement avec <strong>SessionIdTime</strong> pour identifier de manière unique une instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="56d0d-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="56d0d-123">Pour plus d’informations, voir le <a href="lync-server-2013-conferences-table.md">tableau conférences dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56d0d-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56d0d-124"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="56d0d-124"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="56d0d-125">DateHeure</span><span class="sxs-lookup"><span data-stu-id="56d0d-125">datetime</span></span></p></td>
<td><p><span data-ttu-id="56d0d-126">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="56d0d-126">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="56d0d-127">Durée de la demande de session.</span><span class="sxs-lookup"><span data-stu-id="56d0d-127">Time of session request.</span></span> <span data-ttu-id="56d0d-128">Utilisé conjointement avec <strong>SessionIdSeq</strong> pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="56d0d-128">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="56d0d-129">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56d0d-129">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56d0d-130"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="56d0d-130"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="56d0d-131">int</span><span class="sxs-lookup"><span data-stu-id="56d0d-131">int</span></span></p></td>
<td><p><span data-ttu-id="56d0d-132">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="56d0d-132">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="56d0d-133">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="56d0d-133">ID number to identify the session.</span></span> <span data-ttu-id="56d0d-134">Utilisé conjointement avec <strong>SessionIdTime</strong> pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="56d0d-134">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="56d0d-135">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56d0d-135">see the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56d0d-136"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="56d0d-136"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="56d0d-137">int</span><span class="sxs-lookup"><span data-stu-id="56d0d-137">int</span></span></p></td>
<td><p><span data-ttu-id="56d0d-138">Externes</span><span class="sxs-lookup"><span data-stu-id="56d0d-138">Foreign</span></span></p></td>
<td><p><span data-ttu-id="56d0d-139">Numéro unique identifiant cet utilisateur, référencé dans la <a href="lync-server-2013-users-table.md">table utilisateurs de Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="56d0d-139">Unique number identifying this user, referenced from the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56d0d-140"><strong>FocusUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="56d0d-140"><strong>FocusUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="56d0d-141">int</span><span class="sxs-lookup"><span data-stu-id="56d0d-141">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="56d0d-142">Si un utilisateur ouvre une session sur plusieurs ordinateurs ou appareils en même temps, <strong>UserInstance</strong> est utilisé pour identifier de façon unique la combinaison utilisateur/appareil.</span><span class="sxs-lookup"><span data-stu-id="56d0d-142">If a user is logged on at multiple computers or devices at the same time, <strong>UserInstance</strong> is used to uniquely identify the user/device combination.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56d0d-143"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="56d0d-143"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="56d0d-144">bit</span><span class="sxs-lookup"><span data-stu-id="56d0d-144">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="56d0d-145">Si l’utilisateur s’est connecté à partir d’une connexion interne ou non.</span><span class="sxs-lookup"><span data-stu-id="56d0d-145">Whether the user logged on from internal or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56d0d-146"><strong>UserRole</strong></span><span class="sxs-lookup"><span data-stu-id="56d0d-146"><strong>UserRole</strong></span></span></p></td>
<td><p><span data-ttu-id="56d0d-147">int</span><span class="sxs-lookup"><span data-stu-id="56d0d-147">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="56d0d-148">Le rôle de cet utilisateur dans la Conférence, comme le présentateur ou le participant.</span><span class="sxs-lookup"><span data-stu-id="56d0d-148">This user’s role in the conference, such as Presenter or Attendee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56d0d-149"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="56d0d-149"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="56d0d-150">DateHeure</span><span class="sxs-lookup"><span data-stu-id="56d0d-150">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="56d0d-151">Heure à laquelle l’utilisateur rejoint la Conférence.</span><span class="sxs-lookup"><span data-stu-id="56d0d-151">The time this user joins the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56d0d-152"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="56d0d-152"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="56d0d-153">DateHeure</span><span class="sxs-lookup"><span data-stu-id="56d0d-153">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="56d0d-154">Heure à laquelle l’utilisateur quitte la Conférence.</span><span class="sxs-lookup"><span data-stu-id="56d0d-154">The time this user leaves the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56d0d-155"><strong>ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="56d0d-155"><strong>ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="56d0d-156">int</span><span class="sxs-lookup"><span data-stu-id="56d0d-156">int</span></span></p></td>
<td><p><span data-ttu-id="56d0d-157">Externes</span><span class="sxs-lookup"><span data-stu-id="56d0d-157">Foreign</span></span></p></td>
<td><p><span data-ttu-id="56d0d-158">Version du logiciel client de l’utilisateur, référencée dans la <a href="lync-server-2013-clientversions-table.md">table ClientVersions dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="56d0d-158">Version of the user’s client software, referenced to the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56d0d-159"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="56d0d-159"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="56d0d-160">Identificateur</span><span class="sxs-lookup"><span data-stu-id="56d0d-160">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="56d0d-161">Identifiant unique global (GUID) du point de terminaison utilisé dans la Conférence.</span><span class="sxs-lookup"><span data-stu-id="56d0d-161">Globally unique identifier (GUID) of the endpoint used in the conference.</span></span></p>
<p><span data-ttu-id="56d0d-162">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="56d0d-162">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="56d0d-163">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="56d0d-163">


</div>

<span> </span>

</div>

</div>

</span></span></div>

