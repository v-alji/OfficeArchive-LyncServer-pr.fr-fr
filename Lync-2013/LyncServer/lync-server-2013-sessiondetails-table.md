---
title: 'Lync Server 2013 : Table SessionDetails'
description: 'Tableau Lync Server 2013 : SessionDetails'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionDetails table
ms:assetid: 783d2508-e31f-4b54-be0c-63aa5ec21c04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398589(v=OCS.15)
ms:contentKeyID: 48184559
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd927f784fb0f2a835c896824105fe8bb112c7a1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444776"
---
# <a name="sessiondetails-table-in-lync-server-2013"></a><span data-ttu-id="efd10-103">Table SessionDetails dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="efd10-103">SessionDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="efd10-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="efd10-104">

<span> </span></span></span>

<span data-ttu-id="efd10-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="efd10-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="efd10-106">Chaque enregistrement représente une session d’égal à égal, qui peut être un appel téléphonique VoIP-VoIP, une session de messagerie instantanée à deux parties ou tout autre type de session.</span><span class="sxs-lookup"><span data-stu-id="efd10-106">Each record represents one peer-to-peer session, which could be a VoIP-VoIP phone call, two-party IM session, or other type of session.</span></span> <span data-ttu-id="efd10-107">Vous pouvez effectuer une jointure de tableau avec le [tableau multimédia dans Lync Server 2013](lync-server-2013-media-table.md) pour trouver les détails de chaque média impliqué dans cette session.</span><span class="sxs-lookup"><span data-stu-id="efd10-107">You can perform a table join with the [Media table in Lync Server 2013](lync-server-2013-media-table.md) to find the details of each media involved in this session.</span></span>

<span data-ttu-id="efd10-108">Notez que les champs IsUser1IntegratedWithDeskPhone et IsUser2IntegratedWithDeskPhone ont été déplacés de la table SessionDetails utilisée dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="efd10-108">Note that the IsUser1IntegratedWithDeskPhone and the IsUser2IntegratedWithDeskPhone fields have been dropped from the SessionDetails table used in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="efd10-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="efd10-109">Column</span></span></th>
<th><span data-ttu-id="efd10-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="efd10-110">Data Type</span></span></th>
<th><span data-ttu-id="efd10-111">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="efd10-111">Key/Index</span></span></th>
<th><span data-ttu-id="efd10-112">Détails</span><span class="sxs-lookup"><span data-stu-id="efd10-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="efd10-113"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-113"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-114">DateHeure</span><span class="sxs-lookup"><span data-stu-id="efd10-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="efd10-115">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="efd10-115">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-116">Durée de la demande de session.</span><span class="sxs-lookup"><span data-stu-id="efd10-116">Time of session request.</span></span> <span data-ttu-id="efd10-117">Utilisé conjointement avec <strong>SessionIdSeq</strong> pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="efd10-117">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="efd10-118">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-118">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-119"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-119"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-120">int</span><span class="sxs-lookup"><span data-stu-id="efd10-120">int</span></span></p></td>
<td><p><span data-ttu-id="efd10-121">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="efd10-121">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-122">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="efd10-122">ID number to identify the session.</span></span> <span data-ttu-id="efd10-123">Utilisé conjointement avec <strong>SessionIdTime</strong> pour identifier une session de manière unique. \* pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-123">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.\* See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-124"><strong>Corrélation</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-124"><strong>CorrelationId</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-125">identificateur</span><span class="sxs-lookup"><span data-stu-id="efd10-125">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="efd10-126">Un GUID pour corréler plusieurs sessions.</span><span class="sxs-lookup"><span data-stu-id="efd10-126">A GUID to correlate multiple sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-127"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-127"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-128">DateHeure</span><span class="sxs-lookup"><span data-stu-id="efd10-128">datetime</span></span></p></td>
<td><p><span data-ttu-id="efd10-129">Externes</span><span class="sxs-lookup"><span data-stu-id="efd10-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-130">Numéro d’identification identifiant la boîte de dialogue qui a été remplacée par la session actuelle.</span><span class="sxs-lookup"><span data-stu-id="efd10-130">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="efd10-131">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-131">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-132"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-132"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-133">int</span><span class="sxs-lookup"><span data-stu-id="efd10-133">int</span></span></p></td>
<td><p><span data-ttu-id="efd10-134">Externes</span><span class="sxs-lookup"><span data-stu-id="efd10-134">Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-135">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="efd10-135">ID number to identify the session.</span></span> <span data-ttu-id="efd10-136">Utilisé conjointement avec <strong>ReplacesDialogIdTime</strong> pour identifier de manière unique une session qui est remplacée par cette session.</span><span class="sxs-lookup"><span data-stu-id="efd10-136">Used in conjunction with <strong>ReplacesDialogIdTime</strong> to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="efd10-137">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-137">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-138"><strong>User1Id</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-138"><strong>User1Id</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-139">int</span><span class="sxs-lookup"><span data-stu-id="efd10-139">int</span></span></p></td>
<td><p><span data-ttu-id="efd10-140">Externes</span><span class="sxs-lookup"><span data-stu-id="efd10-140">Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-141">ID d’un utilisateur dans la session.</span><span class="sxs-lookup"><span data-stu-id="efd10-141">ID of one user in the session.</span></span> <span data-ttu-id="efd10-142">Pour plus d’informations, consultez le <a href="lync-server-2013-users-table.md">tableau utilisateurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-142">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-143"><strong>User2Id</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-143"><strong>User2Id</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-144">int</span><span class="sxs-lookup"><span data-stu-id="efd10-144">int</span></span></p></td>
<td><p><span data-ttu-id="efd10-145">Externes</span><span class="sxs-lookup"><span data-stu-id="efd10-145">Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-146">ID de l’autre utilisateur de la session.</span><span class="sxs-lookup"><span data-stu-id="efd10-146">ID of the other user in the session.</span></span> <span data-ttu-id="efd10-147">Pour plus d’informations, consultez le <a href="lync-server-2013-users-table.md">tableau utilisateurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-147">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-148"><strong>User1EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-148"><strong>User1EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-149">Identificateur</span><span class="sxs-lookup"><span data-stu-id="efd10-149">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="efd10-150">GUID identifiant le point de terminaison utilisé par le premier utilisateur de la session.</span><span class="sxs-lookup"><span data-stu-id="efd10-150">GUID that identifies the endpoint used by the first user in the session.</span></span></p>
<p><span data-ttu-id="efd10-151">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="efd10-151">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-152"><strong>User2EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-152"><strong>User2EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-153">Identificateur</span><span class="sxs-lookup"><span data-stu-id="efd10-153">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="efd10-154">GUID identifiant le point de terminaison utilisé par le second utilisateur de la session.</span><span class="sxs-lookup"><span data-stu-id="efd10-154">GUID that identifies the endpoint used by the second user in the session.</span></span></p>
<p><span data-ttu-id="efd10-155">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="efd10-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-156"><strong>TargetUserId</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-156"><strong>TargetUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-157">int</span><span class="sxs-lookup"><span data-stu-id="efd10-157">int</span></span></p></td>
<td><p><span data-ttu-id="efd10-158">Externes</span><span class="sxs-lookup"><span data-stu-id="efd10-158">Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-159">URI de l’utilisateur à l’origine de la demande SIP.</span><span class="sxs-lookup"><span data-stu-id="efd10-159">The original To user URI in the SIP request.</span></span> <span data-ttu-id="efd10-160">Pour plus d’informations, consultez le <a href="lync-server-2013-users-table.md">tableau utilisateurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-160">see the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-161"><strong>SessionStartedById</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-161"><strong>SessionStartedById</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-162">int</span><span class="sxs-lookup"><span data-stu-id="efd10-162">int</span></span></p></td>
<td><p><span data-ttu-id="efd10-163">Externes</span><span class="sxs-lookup"><span data-stu-id="efd10-163">Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-164">ID de l’utilisateur qui a démarré la session.</span><span class="sxs-lookup"><span data-stu-id="efd10-164">ID of the user who started the session.</span></span> <span data-ttu-id="efd10-165">Pour plus d’informations, consultez le <a href="lync-server-2013-users-table.md">tableau utilisateurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-165">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-166"><strong>OnBehalfOfId</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-166"><strong>OnBehalfOfId</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-167">int</span><span class="sxs-lookup"><span data-stu-id="efd10-167">int</span></span></p></td>
<td><p><span data-ttu-id="efd10-168">Externes</span><span class="sxs-lookup"><span data-stu-id="efd10-168">Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-169">Indique l’IDENTIFIant de l’utilisateur pour lequel l’appelant a son nom.</span><span class="sxs-lookup"><span data-stu-id="efd10-169">Indicates the ID of the user of who the caller is on behalf.</span></span> <span data-ttu-id="efd10-170">Pour plus d’informations, consultez le <a href="lync-server-2013-users-table.md">tableau utilisateurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-170">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-171"><strong>ReferredById</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-171"><strong>ReferredById</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-172">int</span><span class="sxs-lookup"><span data-stu-id="efd10-172">int</span></span></p></td>
<td><p><span data-ttu-id="efd10-173">Externes</span><span class="sxs-lookup"><span data-stu-id="efd10-173">Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-174">ID de l’utilisateur avec lequel l’appel est soumis.</span><span class="sxs-lookup"><span data-stu-id="efd10-174">ID of the user by who the call is referred.</span></span> <span data-ttu-id="efd10-175">Pour plus d’informations, consultez le <a href="lync-server-2013-users-table.md">tableau utilisateurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-175">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-176"><strong>ServerId</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-176"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-177">int</span><span class="sxs-lookup"><span data-stu-id="efd10-177">int</span></span></p></td>
<td><p><span data-ttu-id="efd10-178">Externes</span><span class="sxs-lookup"><span data-stu-id="efd10-178">Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-179">ID du serveur frontal utilisé pour cette session.</span><span class="sxs-lookup"><span data-stu-id="efd10-179">ID of the front-end server used for this session.</span></span> <span data-ttu-id="efd10-180">Pour plus d’informations, voir le <a href="lync-server-2013-servers-table.md">tableau des serveurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-180">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-181"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-181"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-182">int</span><span class="sxs-lookup"><span data-stu-id="efd10-182">int</span></span></p></td>
<td><p><span data-ttu-id="efd10-183">Externes</span><span class="sxs-lookup"><span data-stu-id="efd10-183">Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-184">ID du pool dans lequel la session a été capturée.</span><span class="sxs-lookup"><span data-stu-id="efd10-184">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="efd10-185">Pour plus d’informations, voir la <a href="lync-server-2013-pools-table.md">table pools dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-185">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-186"><strong>ContentTypeID</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-186"><strong>ContentTypeID</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-187">int</span><span class="sxs-lookup"><span data-stu-id="efd10-187">int</span></span></p></td>
<td><p><span data-ttu-id="efd10-188">Externes</span><span class="sxs-lookup"><span data-stu-id="efd10-188">Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-189">Type de contenu utilisé dans la session.</span><span class="sxs-lookup"><span data-stu-id="efd10-189">Content type used in the session.</span></span> <span data-ttu-id="efd10-190">Pour plus d’informations, voir la <a href="lync-server-2013-contenttypes-table.md">table ContentTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-190">See the <a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-191"><strong>User1ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-191"><strong>User1ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-192">int</span><span class="sxs-lookup"><span data-stu-id="efd10-192">int</span></span></p></td>
<td><p><span data-ttu-id="efd10-193">Externes</span><span class="sxs-lookup"><span data-stu-id="efd10-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-194">Version du client utilisée par user1.</span><span class="sxs-lookup"><span data-stu-id="efd10-194">Client version used by User1.</span></span> <span data-ttu-id="efd10-195">Pour plus d’informations, voir la <a href="lync-server-2013-clientversions-table.md">table ClientVersions dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-195">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-196"><strong>User2ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-196"><strong>User2ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-197">int</span><span class="sxs-lookup"><span data-stu-id="efd10-197">int</span></span></p></td>
<td><p><span data-ttu-id="efd10-198">Externes</span><span class="sxs-lookup"><span data-stu-id="efd10-198">Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-199">Version du client utilisée par utilisateur2.</span><span class="sxs-lookup"><span data-stu-id="efd10-199">Client version used by User2.</span></span> <span data-ttu-id="efd10-200">Pour plus d’informations, voir la <a href="lync-server-2013-clientversions-table.md">table ClientVersions dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-200">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-201"><strong>User1EdgeServerid</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-201"><strong>User1EdgeServerid</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-202">int</span><span class="sxs-lookup"><span data-stu-id="efd10-202">int</span></span></p></td>
<td><p><span data-ttu-id="efd10-203">Externes</span><span class="sxs-lookup"><span data-stu-id="efd10-203">Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-204">Serveur Edge utilisé par user1.</span><span class="sxs-lookup"><span data-stu-id="efd10-204">Edge Server used by User1.</span></span> <span data-ttu-id="efd10-205">Pour plus d’informations, voir la <a href="lync-server-2013-edgeservers-table.md">table EdgeServers dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-205">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-206"><strong>User2EdgeServerid</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-206"><strong>User2EdgeServerid</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-207">int</span><span class="sxs-lookup"><span data-stu-id="efd10-207">int</span></span></p></td>
<td><p><span data-ttu-id="efd10-208">Externes</span><span class="sxs-lookup"><span data-stu-id="efd10-208">Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-209">Serveur Edge utilisé par utilisateur2.</span><span class="sxs-lookup"><span data-stu-id="efd10-209">Edge Server used by User2.</span></span> <span data-ttu-id="efd10-210">Pour plus d’informations, voir la <a href="lync-server-2013-edgeservers-table.md">table EdgeServers dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-210">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-211"><strong>IsUser1Internal</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-211"><strong>IsUser1Internal</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-212">bit</span><span class="sxs-lookup"><span data-stu-id="efd10-212">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="efd10-213">Si User1 est connecté à partir d’une connexion interne ou non.</span><span class="sxs-lookup"><span data-stu-id="efd10-213">Whether User1 is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-214"><strong>IsUser2Internal</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-214"><strong>IsUser2Internal</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-215">bit</span><span class="sxs-lookup"><span data-stu-id="efd10-215">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="efd10-216">L’état d’une connexion interne ou non.</span><span class="sxs-lookup"><span data-stu-id="efd10-216">Whether User2 is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-217"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-217"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-218">DateHeure</span><span class="sxs-lookup"><span data-stu-id="efd10-218">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="efd10-219">Heure de la première demande d’invitation.</span><span class="sxs-lookup"><span data-stu-id="efd10-219">The time of the first INVITE request.</span></span> <span data-ttu-id="efd10-220">Ce champ est généralement rempli par des données générées à partir du message d’invitation initial dans la session.</span><span class="sxs-lookup"><span data-stu-id="efd10-220">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="efd10-221">S’il n’y a pas de message d’invitation, le champ est peuplé de la date et de l’heure du premier message SIP approprié (BYE, annuler, MESSAGE ou informations).</span><span class="sxs-lookup"><span data-stu-id="efd10-221">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span> <span data-ttu-id="efd10-222">Ce champ est généralement rempli par des données générées à partir du message d’invitation initial dans la session.</span><span class="sxs-lookup"><span data-stu-id="efd10-222">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="efd10-223">S’il n’y a pas de message d’invitation, le champ est peuplé de la date et de l’heure du premier message SIP approprié (BYE, annuler, MESSAGE ou informations).</span><span class="sxs-lookup"><span data-stu-id="efd10-223">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-224"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-224"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-225">DateHeure</span><span class="sxs-lookup"><span data-stu-id="efd10-225">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="efd10-226">Heure de la réponse au premier message d’invitation.</span><span class="sxs-lookup"><span data-stu-id="efd10-226">The time of the response to the first INVITE message.</span></span> <span data-ttu-id="efd10-227">Ce champ est généralement rempli par des données générées à partir du message d’invitation initial dans la session.</span><span class="sxs-lookup"><span data-stu-id="efd10-227">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="efd10-228">S’il n’y a pas de message d’invitation, le champ est peuplé de la date et de l’heure du premier message SIP approprié (BYE, annuler, MESSAGE ou informations).</span><span class="sxs-lookup"><span data-stu-id="efd10-228">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-229"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-229"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-230">int</span><span class="sxs-lookup"><span data-stu-id="efd10-230">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="efd10-231">Code de réponse SIP à l’invitation de la session.</span><span class="sxs-lookup"><span data-stu-id="efd10-231">SIP response code to the session invitation.</span></span> <span data-ttu-id="efd10-232">Ce champ est généralement rempli par des données générées à partir du message d’invitation initial dans la session.</span><span class="sxs-lookup"><span data-stu-id="efd10-232">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="efd10-233">S’il n’y a pas de message d’invitation, le champ est peuplé de la date et de l’heure du premier message SIP approprié (BYE, annuler, MESSAGE ou informations).</span><span class="sxs-lookup"><span data-stu-id="efd10-233">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-234"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-234"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-235">int</span><span class="sxs-lookup"><span data-stu-id="efd10-235">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="efd10-236">ID de diagnostic capturé à partir de l’en-tête SIP.</span><span class="sxs-lookup"><span data-stu-id="efd10-236">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-237"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-237"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-238">int</span><span class="sxs-lookup"><span data-stu-id="efd10-238">int</span></span></p></td>
<td><p><span data-ttu-id="efd10-239">Externes</span><span class="sxs-lookup"><span data-stu-id="efd10-239">Foreign</span></span></p></td>
<td><p><span data-ttu-id="efd10-240">Priorité de l’appel.</span><span class="sxs-lookup"><span data-stu-id="efd10-240">Call priority.</span></span> <span data-ttu-id="efd10-241">Pour plus d’informations, voir la <a href="lync-server-2013-callpriorities-table.md">table CallPriorities dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="efd10-241">See the <a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-242"><strong>User1MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-242"><strong>User1MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-243">int</span><span class="sxs-lookup"><span data-stu-id="efd10-243">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="efd10-244">Nombre de messages envoyés par user1 lors de la session.</span><span class="sxs-lookup"><span data-stu-id="efd10-244">Number of messages sent by User1 during the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-245"><strong>User2MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-245"><strong>User2MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-246">int</span><span class="sxs-lookup"><span data-stu-id="efd10-246">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="efd10-247">Nombre de messages envoyés par utilisateur2 lors de la session.</span><span class="sxs-lookup"><span data-stu-id="efd10-247">Number of messages sent by User2 during the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-248"><strong>SessionEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-248"><strong>SessionEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-249">DateHeure</span><span class="sxs-lookup"><span data-stu-id="efd10-249">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="efd10-250">Heure à la fin de la session.</span><span class="sxs-lookup"><span data-stu-id="efd10-250">Time at the end of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-251"><strong>MediaTypes</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-251"><strong>MediaTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-252">int</span><span class="sxs-lookup"><span data-stu-id="efd10-252">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="efd10-253">Un ensemble de bits qui indique le type de média de cette session.</span><span class="sxs-lookup"><span data-stu-id="efd10-253">A bit set that indicates the media type of this session.</span></span> <span data-ttu-id="efd10-254">Voici les définitions des types :</span><span class="sxs-lookup"><span data-stu-id="efd10-254">Listed are the definitions of the types:</span></span></p>
<h3 id="section-1"> </h3>
<div>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="efd10-255">MI</span><span class="sxs-lookup"><span data-stu-id="efd10-255">IM</span></span></p></td>
<td><p><span data-ttu-id="efd10-256">1</span><span class="sxs-lookup"><span data-stu-id="efd10-256">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-257">FILE_TRANSFER</span><span class="sxs-lookup"><span data-stu-id="efd10-257">FILE_TRANSFER</span></span></p></td>
<td><p><span data-ttu-id="efd10-258">2</span><span class="sxs-lookup"><span data-stu-id="efd10-258">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-259">REMOTE_ASSISTANCE</span><span class="sxs-lookup"><span data-stu-id="efd10-259">REMOTE_ASSISTANCE</span></span></p></td>
<td><p><span data-ttu-id="efd10-260">4</span><span class="sxs-lookup"><span data-stu-id="efd10-260">4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-261">APP_SHARING</span><span class="sxs-lookup"><span data-stu-id="efd10-261">APP_SHARING</span></span></p></td>
<td><p><span data-ttu-id="efd10-262">version8</span><span class="sxs-lookup"><span data-stu-id="efd10-262">8</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-263">AUDIO</span><span class="sxs-lookup"><span data-stu-id="efd10-263">AUDIO</span></span></p></td>
<td><p><span data-ttu-id="efd10-264">Seiz</span><span class="sxs-lookup"><span data-stu-id="efd10-264">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-265">CAMÉSCOPE</span><span class="sxs-lookup"><span data-stu-id="efd10-265">VIDEO</span></span></p></td>
<td><p><span data-ttu-id="efd10-266">32</span><span class="sxs-lookup"><span data-stu-id="efd10-266">32</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-267">APP_INVITE</span><span class="sxs-lookup"><span data-stu-id="efd10-267">APP_INVITE</span></span></p></td>
<td><p><span data-ttu-id="efd10-268">64</span><span class="sxs-lookup"><span data-stu-id="efd10-268">64</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-269"><strong>User1Flag</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-269"><strong>User1Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-270">type</span><span class="sxs-lookup"><span data-stu-id="efd10-270">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="efd10-271">Un ensemble de bits qui indique les attributs User1.</span><span class="sxs-lookup"><span data-stu-id="efd10-271">A bit set that indicates the User1 attributes.</span></span> <span data-ttu-id="efd10-272">Les définitions d’attribut suivantes apparaissent :</span><span class="sxs-lookup"><span data-stu-id="efd10-272">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="efd10-273">0x01-intégré sur le téléphone de bureau</span><span class="sxs-lookup"><span data-stu-id="efd10-273">0x01 - Integrated with desktop phone</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-274"><strong>User2Flag</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-274"><strong>User2Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-275">type</span><span class="sxs-lookup"><span data-stu-id="efd10-275">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="efd10-276">Un ensemble de bits qui indique les attributs utilisateur2.</span><span class="sxs-lookup"><span data-stu-id="efd10-276">A bit set that indicates the User2 attributes.</span></span> <span data-ttu-id="efd10-277">Les définitions d’attribut suivantes apparaissent :</span><span class="sxs-lookup"><span data-stu-id="efd10-277">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="efd10-278">0x01-intégré sur le téléphone de bureau</span><span class="sxs-lookup"><span data-stu-id="efd10-278">0x01 - Integrated with desktop phone</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efd10-279"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-279"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-280">type</span><span class="sxs-lookup"><span data-stu-id="efd10-280">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="efd10-281">Un ensemble de bits qui indique les attributs d’appel.</span><span class="sxs-lookup"><span data-stu-id="efd10-281">A bit set that indicates the call attributes.</span></span> <span data-ttu-id="efd10-282">Les définitions d’attribut suivantes apparaissent :</span><span class="sxs-lookup"><span data-stu-id="efd10-282">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="efd10-283">0x01-nouvelle tentative de session</span><span class="sxs-lookup"><span data-stu-id="efd10-283">0x01 - Retried Session</span></span></p></li>
<li><p><span data-ttu-id="efd10-284">0x02-appel émis par l’agent pour le compte d’un groupe de réponse</span><span class="sxs-lookup"><span data-stu-id="efd10-284">0x02 - A call made by agent on behalf of a response group</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efd10-285"><strong>Formé</strong></span><span class="sxs-lookup"><span data-stu-id="efd10-285"><strong>Processed</strong></span></span></p></td>
<td><p><span data-ttu-id="efd10-286">bit</span><span class="sxs-lookup"><span data-stu-id="efd10-286">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="efd10-287">Pour une utilisation interne par le service de surveillance.</span><span class="sxs-lookup"><span data-stu-id="efd10-287">For internal use by the Monitoring service.</span></span></p>
<p><span data-ttu-id="efd10-288">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="efd10-288">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="efd10-289">\* Pour la plupart des sessions, SessionIdSeq aura la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="efd10-289">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="efd10-290">S’il s’agit d’une session à partir de la même heure, le SessionIdSeq de l’une sera 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="efd10-290">If multiple sessions start at exactly the same time, the SessionIdSeq for one will be 1, for another will be 2, and so on.</span></span>

<span data-ttu-id="efd10-291"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="efd10-291"></div>

<span> </span>

</div>

</div>

</span></span></div>

