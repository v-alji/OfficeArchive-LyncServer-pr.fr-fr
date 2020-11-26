---
title: 'Lync Server 2013 : Table McuJoinsAndLeaves'
description: 'Tableau Lync Server 2013 : McuJoinsAndLeaves'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: McuJoinsAndLeaves table
ms:assetid: 4e073366-0b5d-45b4-a3f6-d63dd5fd9f25
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398316(v=OCS.15)
ms:contentKeyID: 48184115
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee7d9473892ac357dcefd80b0d52382c5dd7d930
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425751"
---
# <a name="mcujoinsandleaves-table-in-lync-server-2013"></a><span data-ttu-id="133bd-103">Table McuJoinsAndLeaves dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="133bd-103">McuJoinsAndLeaves table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="133bd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="133bd-104">

<span> </span></span></span>

<span data-ttu-id="133bd-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="133bd-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="133bd-106">Chaque enregistrement de cette table contient les détails de l’appel d’une combinaison d’une jointure utilisateur ou d’un serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="133bd-106">Each record in this table contains call details about one combination of a user join or leave and conferencing server.</span></span> <span data-ttu-id="133bd-107">Par exemple, si un utilisateur rejoint une conférence incluant des conférences Web et des éléments audio ou vidéo, un enregistrement sera créé pour la participation à la conférence Web de cet utilisateur et un autre enregistrement serait créé pour la participation de l’utilisateur à la conférence audio/vidéo.</span><span class="sxs-lookup"><span data-stu-id="133bd-107">For example, if a user joins a conference that includes web conferencing and audio/video elements, one record would be created for that user’s web conferencing join, and another record would be created for the user’s audio/video conferencing join.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="133bd-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="133bd-108">Column</span></span></th>
<th><span data-ttu-id="133bd-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="133bd-109">Data Type</span></span></th>
<th><span data-ttu-id="133bd-110">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="133bd-110">Key/Index</span></span></th>
<th><span data-ttu-id="133bd-111">Détails</span><span class="sxs-lookup"><span data-stu-id="133bd-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="133bd-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="133bd-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="133bd-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="133bd-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="133bd-114">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="133bd-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="133bd-115">Durée de l’instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="133bd-115">Time of conference instance.</span></span> <span data-ttu-id="133bd-116">Utilisé conjointement avec <strong>SessionIdSeq</strong> pour identifier de manière unique une instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="133bd-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="133bd-117">Pour plus d’informations, voir le <a href="lync-server-2013-conferences-table.md">tableau conférences dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="133bd-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="133bd-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="133bd-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="133bd-119">int</span><span class="sxs-lookup"><span data-stu-id="133bd-119">int</span></span></p></td>
<td><p><span data-ttu-id="133bd-120">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="133bd-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="133bd-121">Numéro d’identification pour identifier l’instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="133bd-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="133bd-122">Utilisé conjointement avec <strong>SessionIdTime</strong> pour identifier de manière unique une instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="133bd-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="133bd-123">Pour plus d’informations, voir le <a href="lync-server-2013-conferences-table.md">tableau conférences dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="133bd-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="133bd-124"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="133bd-124"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="133bd-125">int</span><span class="sxs-lookup"><span data-stu-id="133bd-125">int</span></span></p></td>
<td><p><span data-ttu-id="133bd-126">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="133bd-126">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="133bd-127">Numéro unique identifiant cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="133bd-127">Unique number identifying this user.</span></span> <span data-ttu-id="133bd-128">Pour plus d’informations, consultez le <a href="lync-server-2013-users-table.md">tableau utilisateurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="133bd-128">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="133bd-129"><strong>McuUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="133bd-129"><strong>McuUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="133bd-130">int</span><span class="sxs-lookup"><span data-stu-id="133bd-130">int</span></span></p></td>
<td><p><span data-ttu-id="133bd-131">Principal</span><span class="sxs-lookup"><span data-stu-id="133bd-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="133bd-132">Si un utilisateur ouvre une session sur plusieurs ordinateurs ou appareils en même temps, McuUserInstance identifie de façon unique la combinaison utilisateur/appareil.</span><span class="sxs-lookup"><span data-stu-id="133bd-132">If a user is logged on at multiple computers or devices at once, McuUserInstance uniquely identifies the user/device combination.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="133bd-133"><strong>IsFromPstn</strong></span><span class="sxs-lookup"><span data-stu-id="133bd-133"><strong>IsFromPstn</strong></span></span></p></td>
<td><p><span data-ttu-id="133bd-134">bit</span><span class="sxs-lookup"><span data-stu-id="133bd-134">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="133bd-135">Le fait que l’utilisateur se connecte à partir d’un réseau PSTN ou non.</span><span class="sxs-lookup"><span data-stu-id="133bd-135">Whether the user is joining from a PSTN or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="133bd-136"><strong>McuId</strong></span><span class="sxs-lookup"><span data-stu-id="133bd-136"><strong>McuId</strong></span></span></p></td>
<td><p><span data-ttu-id="133bd-137">int</span><span class="sxs-lookup"><span data-stu-id="133bd-137">int</span></span></p></td>
<td><p><span data-ttu-id="133bd-138">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="133bd-138">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="133bd-139">Numéro unique identifiant ce serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="133bd-139">Unique number identifying this conferencing server.</span></span> <span data-ttu-id="133bd-140">Pour plus d’informations, reportez-vous <a href="lync-server-2013-mcus-table.md">à la table MCU dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="133bd-140">See the <a href="lync-server-2013-mcus-table.md">Mcus table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="133bd-141"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="133bd-141"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="133bd-142">DateHeure</span><span class="sxs-lookup"><span data-stu-id="133bd-142">datetime</span></span></p></td>
<td><p><span data-ttu-id="133bd-143">Externes</span><span class="sxs-lookup"><span data-stu-id="133bd-143">Foreign</span></span></p></td>
<td><p><span data-ttu-id="133bd-144">Durée de la demande de session.</span><span class="sxs-lookup"><span data-stu-id="133bd-144">Time of session request.</span></span> <span data-ttu-id="133bd-145">Utilisé conjointement avec <strong>SessionIdSeq</strong> pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="133bd-145">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="133bd-146">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="133bd-146">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="133bd-147"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="133bd-147"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="133bd-148">int</span><span class="sxs-lookup"><span data-stu-id="133bd-148">int</span></span></p></td>
<td><p><span data-ttu-id="133bd-149">Externes</span><span class="sxs-lookup"><span data-stu-id="133bd-149">Foreign</span></span></p></td>
<td><p><span data-ttu-id="133bd-150">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="133bd-150">ID number to identify the session.</span></span> <span data-ttu-id="133bd-151">Utilisé conjointement avec <strong>SessionIdTime</strong> pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="133bd-151">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="133bd-152">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="133bd-152">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="133bd-153"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="133bd-153"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="133bd-154">DateHeure</span><span class="sxs-lookup"><span data-stu-id="133bd-154">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="133bd-155">Heure à laquelle l’utilisateur rejoint ce serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="133bd-155">The time this user joins this conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="133bd-156"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="133bd-156"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="133bd-157">DateHeure</span><span class="sxs-lookup"><span data-stu-id="133bd-157">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="133bd-158">Heure à laquelle l’utilisateur quitte ce serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="133bd-158">The time this user leaves this conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="133bd-159"><strong>ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="133bd-159"><strong>ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="133bd-160">int</span><span class="sxs-lookup"><span data-stu-id="133bd-160">int</span></span></p></td>
<td><p><span data-ttu-id="133bd-161">Externes</span><span class="sxs-lookup"><span data-stu-id="133bd-161">Foreign</span></span></p></td>
<td><p><span data-ttu-id="133bd-162">Identificateur spécifiant le numéro de version de l’utilisation du logiciel client dans la Conférence.</span><span class="sxs-lookup"><span data-stu-id="133bd-162">Identifier that specifies the version number of the client software use in the conference.</span></span> <span data-ttu-id="133bd-163">Pour plus d’informations, voir la <a href="lync-server-2013-clientversions-table.md">table ClientVersions dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="133bd-163">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="133bd-164">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="133bd-164">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="133bd-165">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="133bd-165">


</div>

<span> </span>

</div>

</div>

</span></span></div>

