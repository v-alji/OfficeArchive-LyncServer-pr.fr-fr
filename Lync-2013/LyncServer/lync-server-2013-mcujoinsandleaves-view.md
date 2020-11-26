---
title: 'Affichage Lync Server 2013 : McuJoinsAndLeaves'
description: 'Affichage Lync Server 2013 : McuJoinsAndLeaves'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: McuJoinsAndLeaves view
ms:assetid: 6f00b8e7-b8b6-4657-ac5e-d8a571806ae2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688088(v=OCS.15)
ms:contentKeyID: 49733687
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f7f2f51c340d5bd4824a6e8eff1a0da172a758c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425730"
---
# <a name="mcujoinsandleaves-view-in-lync-server-2013"></a><span data-ttu-id="367c7-103">Affichage McuJoinsAndLeaves dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="367c7-103">McuJoinsAndLeaves view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="367c7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="367c7-104">

<span> </span></span></span>

<span data-ttu-id="367c7-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="367c7-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="367c7-106">Le mode McuJoinsAndLeaves stocke les informations sur les utilisateurs qui rejoignent et laissent des informations pour un serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="367c7-106">The McuJoinsAndLeaves view stores information about users join and leave information for one conference server.</span></span> <span data-ttu-id="367c7-107">Chaque enregistrement de cette vue contient les détails de l’une des combinaisons d’un utilisateur qui rejoint ou quittent le serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="367c7-107">Each record in this view contains call details about one combination of a user join or leave and conferencing server.</span></span> <span data-ttu-id="367c7-108">Cet affichage a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="367c7-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="367c7-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="367c7-109">Column</span></span></th>
<th><span data-ttu-id="367c7-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="367c7-110">Data Type</span></span></th>
<th><span data-ttu-id="367c7-111">Détails</span><span class="sxs-lookup"><span data-stu-id="367c7-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="367c7-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="367c7-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="367c7-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="367c7-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="367c7-114">Durée de l’instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="367c7-114">Time of conference instance.</span></span> <span data-ttu-id="367c7-115">Utilisé conjointement avec SessionIdSeq pour identifier de manière unique une instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="367c7-115">Used in conjunction with SessionIdSeq to uniquely identify a conference instance.</span></span> <span data-ttu-id="367c7-116">Pour plus d’informations, voir le <a href="lync-server-2013-conferences-table.md">tableau conférences dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="367c7-116">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="367c7-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="367c7-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="367c7-118">int</span><span class="sxs-lookup"><span data-stu-id="367c7-118">int</span></span></p></td>
<td><p><span data-ttu-id="367c7-119">Numéro d’identification pour identifier l’instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="367c7-119">ID number to identify the conference instance.</span></span> <span data-ttu-id="367c7-120">Utilisé conjointement avec SessionIdTime pour identifier de manière unique une instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="367c7-120">Used in conjunction with SessionIdTime to uniquely identify a conference instance.</span></span> <span data-ttu-id="367c7-121">Pour plus d’informations, voir le <a href="lync-server-2013-conferences-table.md">tableau conférences dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="367c7-121">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="367c7-122"><strong>McuUri</strong></span><span class="sxs-lookup"><span data-stu-id="367c7-122"><strong>McuUri</strong></span></span></p></td>
<td><p><span data-ttu-id="367c7-123">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="367c7-123">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="367c7-124">URI du serveur de conférence auquel l’utilisateur s’est connecté.</span><span class="sxs-lookup"><span data-stu-id="367c7-124">The URI of the conferencing server that the user connected to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="367c7-125"><strong>McuUriType</strong></span><span class="sxs-lookup"><span data-stu-id="367c7-125"><strong>McuUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="367c7-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="367c7-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="367c7-127">URI du serveur de conférence auquel l’utilisateur s’est connecté.</span><span class="sxs-lookup"><span data-stu-id="367c7-127">The URI of the conferencing server that the user connected to.</span></span> <span data-ttu-id="367c7-128">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="367c7-128">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="367c7-129"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="367c7-129"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="367c7-130">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="367c7-130">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="367c7-131">URI de l’utilisateur qui a capturé les informations de jointure/conservation du serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="367c7-131">The URI of the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="367c7-132"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="367c7-132"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="367c7-133">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="367c7-133">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="367c7-134">Le type d’URI de l’utilisateur dont le serveur de conférence a été capturé.</span><span class="sxs-lookup"><span data-stu-id="367c7-134">The type of URI of the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="367c7-135">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="367c7-135">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="367c7-136"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="367c7-136"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="367c7-137">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="367c7-137">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="367c7-138">Le client de l’utilisateur qui a capturé les informations de jointure/conservation du serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="367c7-138">The tenant of the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="367c7-139">Pour plus d’informations, voir la <a href="lync-server-2013-tenants-table.md">table locataires dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="367c7-139">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="367c7-140"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="367c7-140"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="367c7-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="367c7-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="367c7-142">La version du client utilisée par l’utilisateur dont les informations de jointure/de conservation du serveur de conférence ont été capturées.</span><span class="sxs-lookup"><span data-stu-id="367c7-142">The version of client used by the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="367c7-143"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="367c7-143"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="367c7-144">int</span><span class="sxs-lookup"><span data-stu-id="367c7-144">int</span></span></p></td>
<td><p><span data-ttu-id="367c7-145">Le client utilisé par l’utilisateur qui a capturé les informations de jointure/conservation du serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="367c7-145">The client used by the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="367c7-146">Pour plus d’informations, voir la <a href="lync-server-2013-useragentdef-table.md">table UserAgentDef dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="367c7-146">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="367c7-147"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="367c7-147"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="367c7-148">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="367c7-148">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="367c7-149">Le nom de la catégorie du client utilisée par l’utilisateur dont les informations de jointure/conservation du serveur de conférence ont été capturées.</span><span class="sxs-lookup"><span data-stu-id="367c7-149">The name of the category of the client used by the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="367c7-150"><strong>McuUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="367c7-150"><strong>McuUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="367c7-151">int</span><span class="sxs-lookup"><span data-stu-id="367c7-151">int</span></span></p></td>
<td><p><span data-ttu-id="367c7-152">Identifie de manière unique la combinaison utilisateur/appareil pour les utilisateurs connectés simultanément à plusieurs appareils.</span><span class="sxs-lookup"><span data-stu-id="367c7-152">Uniquely identifies the user/device combination for users simultaneously logged on to multiple devices.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="367c7-153"><strong>IsUserFromPstn</strong></span><span class="sxs-lookup"><span data-stu-id="367c7-153"><strong>IsUserFromPstn</strong></span></span></p></td>
<td><p><span data-ttu-id="367c7-154">bit</span><span class="sxs-lookup"><span data-stu-id="367c7-154">bit</span></span></p></td>
<td><p><span data-ttu-id="367c7-155">Bit qui indique si l’utilisateur est ou non un utilisateur interne.</span><span class="sxs-lookup"><span data-stu-id="367c7-155">Bit that represents whether the user is an internal user or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="367c7-156"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="367c7-156"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="367c7-157">DateHeure</span><span class="sxs-lookup"><span data-stu-id="367c7-157">datetime</span></span></p></td>
<td><p><span data-ttu-id="367c7-158">Durée de la demande de session.</span><span class="sxs-lookup"><span data-stu-id="367c7-158">Time of session request.</span></span> <span data-ttu-id="367c7-159">Utilisé conjointement avec SessionIdSeq pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="367c7-159">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="367c7-160">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="367c7-160">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="367c7-161"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="367c7-161"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="367c7-162">int</span><span class="sxs-lookup"><span data-stu-id="367c7-162">int</span></span></p></td>
<td><p><span data-ttu-id="367c7-163">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="367c7-163">ID number to identify the session.</span></span> <span data-ttu-id="367c7-164">Utilisé conjointement avec SessionIdTime pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="367c7-164">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="367c7-165">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="367c7-165">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="367c7-166"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="367c7-166"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="367c7-167">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="367c7-167">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="367c7-168">ID de la boîte de dialogue SIP de la session.</span><span class="sxs-lookup"><span data-stu-id="367c7-168">SIP dialog ID of the session.</span></span> <span data-ttu-id="367c7-169">Le format est : boîte de dialogue ; de-balise ; à balise.</span><span class="sxs-lookup"><span data-stu-id="367c7-169">The format is: dialog;from-tag;to-tag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="367c7-170"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="367c7-170"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="367c7-171">DateHeure</span><span class="sxs-lookup"><span data-stu-id="367c7-171">datetime</span></span></p></td>
<td><p><span data-ttu-id="367c7-172">Temps pendant lequel l’utilisateur a rejoint le serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="367c7-172">Time the user joined the conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="367c7-173"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="367c7-173"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="367c7-174">DateHeure</span><span class="sxs-lookup"><span data-stu-id="367c7-174">datetime</span></span></p></td>
<td><p><span data-ttu-id="367c7-175">Temps pendant lequel l’utilisateur a quitté le serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="367c7-175">Time the user left the conferencing server.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="367c7-176">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="367c7-176">


</div>

<span> </span>

</div>

</div>

</span></span></div>

