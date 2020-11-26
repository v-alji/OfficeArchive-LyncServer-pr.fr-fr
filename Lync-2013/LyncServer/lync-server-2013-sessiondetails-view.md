---
title: 'Affichage Lync Server 2013 : SessionDetails'
description: 'Affichage Lync Server 2013 : SessionDetails'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionDetails view
ms:assetid: ea328c6f-cf22-48dd-8f7f-f1666c9148c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721924(v=OCS.15)
ms:contentKeyID: 49733859
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c9f657257e54389defb805919be61adbdecad74
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424029"
---
# <a name="sessiondetails-view-in-lync-server-2013"></a><span data-ttu-id="9ce22-103">Affichage SessionDetails dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9ce22-103">SessionDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9ce22-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9ce22-104">

<span> </span></span></span>

<span data-ttu-id="9ce22-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="9ce22-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="9ce22-106">Le mode SessionDetails stocke les informations sur les sessions d’égal à égal, qui peuvent être un appel téléphonique VoIP-VoIP, une session de messagerie instantanée à deux participants ou un autre type de session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-106">The SessionDetails view stores information about peer-to-peer sessions, which could be a VoIP-VoIP phone call, two-party IM session, or other type of session.</span></span> <span data-ttu-id="9ce22-107">Cet affichage a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9ce22-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9ce22-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="9ce22-108">Column</span></span></th>
<th><span data-ttu-id="9ce22-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="9ce22-109">Data Type</span></span></th>
<th><span data-ttu-id="9ce22-110">Détails</span><span class="sxs-lookup"><span data-stu-id="9ce22-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-112">DateHeure</span><span class="sxs-lookup"><span data-stu-id="9ce22-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="9ce22-113">Durée de la demande de session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-113">Time of session request.</span></span> <span data-ttu-id="9ce22-114">Utilisé conjointement avec SessionIdSeq pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="9ce22-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="9ce22-115">Pour plus d’informations, consultez le <a href="lync-server-2013-dialogs-table.md">tableau de boîte de dialogue dans la table Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9ce22-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> Table for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-117">int</span><span class="sxs-lookup"><span data-stu-id="9ce22-117">int</span></span></p></td>
<td><p><span data-ttu-id="9ce22-118">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-118">ID number to identify the session.</span></span> <span data-ttu-id="9ce22-119">Utilisé conjointement avec SessionIdTime pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="9ce22-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="9ce22-120">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9ce22-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-121"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-121"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-122">DateHeure</span><span class="sxs-lookup"><span data-stu-id="9ce22-122">datetime</span></span></p></td>
<td><p><span data-ttu-id="9ce22-123">Heure de la première demande d’invitation.</span><span class="sxs-lookup"><span data-stu-id="9ce22-123">Time of the first INVITE request.</span></span> <span data-ttu-id="9ce22-124">Ce champ est généralement rempli par des données générées à partir du message d’invitation initial dans la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-124">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="9ce22-125">S’il n’y a pas de message d’invitation, le champ est peuplé de la date et de l’heure du premier message SIP approprié (BYE, annuler, MESSAGE ou informations).</span><span class="sxs-lookup"><span data-stu-id="9ce22-125">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span> <span data-ttu-id="9ce22-126">Ce champ est généralement rempli par des données générées à partir du message d’invitation initial dans la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-126">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="9ce22-127">S’il n’y a pas de message d’invitation, le champ est peuplé de la date et de l’heure du premier message SIP approprié (BYE, annuler, MESSAGE ou informations).</span><span class="sxs-lookup"><span data-stu-id="9ce22-127">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-128"><strong>FromUri</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-128"><strong>FromUri</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-129">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="9ce22-129">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-130">URI de l’utilisateur qui a démarré la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-130">URI of the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-131"><strong>Visite guidée</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-131"><strong>ToUri</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-132">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="9ce22-132">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-133">URI de l’utilisateur qui a rejoint la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-133">URI of the user who joined the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-134"><strong>FromUriType</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-134"><strong>FromUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-135">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9ce22-135">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-136">Type d’URI de l’utilisateur qui a démarré la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-136">Type of URI of the user who started the session.</span></span> <span data-ttu-id="9ce22-137">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9ce22-137">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-138"><strong>ToUriType</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-138"><strong>ToUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-139">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9ce22-139">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-140">Type d’URI de l’utilisateur qui a rejoint la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-140">Type of URI of the user who joined the session.</span></span> <span data-ttu-id="9ce22-141">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9ce22-141">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-142"><strong>FromTenant</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-142"><strong>FromTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-143">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="9ce22-143">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-144">Client de l’utilisateur qui a démarré la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-144">Tenant of the user who started the session.</span></span> <span data-ttu-id="9ce22-145">Pour plus d’informations, voir la <a href="lync-server-2013-tenants-table.md">table locataires dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9ce22-145">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-146"><strong>ToTenant</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-146"><strong>ToTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-147">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9ce22-147">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-148">Le client de l’utilisateur qui a rejoint la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-148">The tenant of the user who joined the session.</span></span> <span data-ttu-id="9ce22-149">Pour plus d’informations, voir la <a href="lync-server-2013-tenants-table.md">table locataires dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9ce22-149">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-150"><strong>FromEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-150"><strong>FromEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-151">identificateur</span><span class="sxs-lookup"><span data-stu-id="9ce22-151">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="9ce22-152">Identificateur unique du point de terminaison de l’utilisateur qui a démarré la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-152">Unique identifier of the endpoint of the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-153"><strong>ToEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-153"><strong>ToEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-154">identificateur</span><span class="sxs-lookup"><span data-stu-id="9ce22-154">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="9ce22-155">Identificateur unique du point de terminaison de l’utilisateur qui a rejoint la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-155">Unique identifier of the endpoint of the user who joined the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-156"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-156"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-157">DateHeure</span><span class="sxs-lookup"><span data-stu-id="9ce22-157">datetime</span></span></p></td>
<td><p><span data-ttu-id="9ce22-158">Heure de fin de la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-158">End time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-159"><strong>FromMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-159"><strong>FromMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-160">int</span><span class="sxs-lookup"><span data-stu-id="9ce22-160">int</span></span></p></td>
<td><p><span data-ttu-id="9ce22-161">Nombre de messages envoyés par l’utilisateur qui a démarré la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-161">Number of messages sent by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-162"><strong>ToMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-162"><strong>ToMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-163">int</span><span class="sxs-lookup"><span data-stu-id="9ce22-163">int</span></span></p></td>
<td><p><span data-ttu-id="9ce22-164">Nombre de messages envoyés par l’utilisateur ayant rejoint la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-164">Number of messages sent by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-165"><strong>FromClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-165"><strong>FromClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-166">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9ce22-166">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-167">Version du client utilisée par l’utilisateur qui a démarré la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-167">Version of client used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-168"><strong>FromClientType</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-168"><strong>FromClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-169">int</span><span class="sxs-lookup"><span data-stu-id="9ce22-169">int</span></span></p></td>
<td><p><span data-ttu-id="9ce22-170">Client utilisé par l’utilisateur qui a démarré la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-170">Client used by the user who started the session.</span></span> <span data-ttu-id="9ce22-171">Pour plus d’informations, voir la <a href="lync-server-2013-useragentdef-table.md">table UserAgentDef dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9ce22-171">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-172"><strong>FromClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-172"><strong>FromClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-173">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="9ce22-173">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-174">Nom de la catégorie du client utilisée par l’utilisateur qui a démarré la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-174">Name of the category of the client used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-175"><strong>ToClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-175"><strong>ToClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-176">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9ce22-176">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-177">Version du client utilisée par l’utilisateur ayant rejoint la session</span><span class="sxs-lookup"><span data-stu-id="9ce22-177">Version of client used by the user who joined the session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-178"><strong>ToClientType</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-178"><strong>ToClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-179">int</span><span class="sxs-lookup"><span data-stu-id="9ce22-179">int</span></span></p></td>
<td><p><span data-ttu-id="9ce22-180">Client utilisé par l’utilisateur ayant rejoint la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-180">Client used by the user who joined the session.</span></span> <span data-ttu-id="9ce22-181">Pour plus d’informations, voir la <a href="lync-server-2013-useragentdef-table.md">table UserAgentDef dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9ce22-181">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-182"><strong>ToClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-182"><strong>ToClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-183">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="9ce22-183">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-184">Nom de la catégorie du client utilisée par l’utilisateur ayant rejoint la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-184">Name of the category of the client used by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-185"><strong>TargetUri</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-185"><strong>TargetUri</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-186">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="9ce22-186">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-187">URI de l’utilisateur cible de la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-187">URI of the target user of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-188"><strong>TargetUriType</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-188"><strong>TargetUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-189">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="9ce22-189">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-190">Type d’URI de l’utilisateur cible pour la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-190">Type of URI of the target user for the session.</span></span> <span data-ttu-id="9ce22-191">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9ce22-191">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-192"><strong>OnBehalfOfUri</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-192"><strong>OnBehalfOfUri</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-193">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="9ce22-193">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-194">URI de l’utilisateur au nom duquel la session a été démarrée.</span><span class="sxs-lookup"><span data-stu-id="9ce22-194">URI of the user on whose behalf the session was started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-195"><strong>OnnnBehalfOfUriType</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-195"><strong>OnnnBehalfOfUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9ce22-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-197">Type d’URI de l’utilisateur au nom duquel la session a démarré.</span><span class="sxs-lookup"><span data-stu-id="9ce22-197">Type of URI of the user on whose behalf the session was started.</span></span> <span data-ttu-id="9ce22-198">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9ce22-198">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-199"><strong>OnBehalfOfTenant</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-199"><strong>OnBehalfOfTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-200">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9ce22-200">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-201">Client de l’utilisateur dont le nom est démarré.</span><span class="sxs-lookup"><span data-stu-id="9ce22-201">Tenant of the user whose on behalf the session was started.</span></span> <span data-ttu-id="9ce22-202">Pour plus d’informations, voir la <a href="lync-server-2013-tenants-table.md">table locataires dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9ce22-202">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-203"><strong>ReferredByUri</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-203"><strong>ReferredByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-204">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="9ce22-204">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-205">URI de l’utilisateur qui a expertisé la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-205">URI of the user who referred the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-206"><strong>ReferredByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-206"><strong>ReferredByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-207">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9ce22-207">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-208">Type d’URI de l’utilisateur qui a expertisé la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-208">Type of URI of the user who referred the session.</span></span> <span data-ttu-id="9ce22-209">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9ce22-209">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-210"><strong>ReferredByTenant</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-210"><strong>ReferredByTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-211">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9ce22-211">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-212">Client de l’utilisateur qui a fait appel à la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-212">Tenant of the user who referred the session.</span></span> <span data-ttu-id="9ce22-213">Pour plus d’informations, voir la <a href="lync-server-2013-tenants-table.md">table locataires dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9ce22-213">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-214"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-214"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-215">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="9ce22-215">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-216">ID de boîte de dialogue SIP.</span><span class="sxs-lookup"><span data-stu-id="9ce22-216">SIP dialog ID.</span></span> <span data-ttu-id="9ce22-217">Le format est le suivant :</span><span class="sxs-lookup"><span data-stu-id="9ce22-217">The format is:</span></span></p>
<p><span data-ttu-id="9ce22-218">boîte de dialogue ; à partir d’une balise</span><span class="sxs-lookup"><span data-stu-id="9ce22-218">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-219"><strong>Corrélation</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-219"><strong>CorrelationId</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-220">identificateur</span><span class="sxs-lookup"><span data-stu-id="9ce22-220">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="9ce22-221">GUID utilisé pour mettre en corrélation plusieurs sessions.</span><span class="sxs-lookup"><span data-stu-id="9ce22-221">GUID used to correlate multiple sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-222"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-222"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-223">DateHeure</span><span class="sxs-lookup"><span data-stu-id="9ce22-223">datetime</span></span></p></td>
<td><p><span data-ttu-id="9ce22-224">Heure de la boîte de dialogue qui a été remplacée par la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-224">Time of the dialog which was replaced by the session.</span></span> <span data-ttu-id="9ce22-225">Utilisé conjointement avec ReplaceDialogIdSeq pour identifier de façon unique une boîte de dialogue qui est remplacée par la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-225">Used in conjunction with ReplaceDialogIdSeq to uniquely identify a dialog that is replaced by the session.</span></span> <span data-ttu-id="9ce22-226">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9ce22-226">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-227"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-227"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-228">int</span><span class="sxs-lookup"><span data-stu-id="9ce22-228">int</span></span></p></td>
<td><p><span data-ttu-id="9ce22-229">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-229">ID number to identify the session.</span></span> <span data-ttu-id="9ce22-230">Utilisé conjointement avec ReplaceDialogIdTime pour identifier de façon unique une boîte de dialogue qui est remplacée par la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-230">Used in conjunction with ReplaceDialogIdTime to uniquely identify a dialog that is replaced by the session.</span></span> <span data-ttu-id="9ce22-231">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9ce22-231">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-232"><strong>ReplacesDialogId</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-232"><strong>ReplacesDialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-233">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="9ce22-233">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-234">ID de boîte de dialogue SIP le remplacement de la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-234">SIP dialog ID the session replaces.</span></span> <span data-ttu-id="9ce22-235">Le format est le suivant :</span><span class="sxs-lookup"><span data-stu-id="9ce22-235">The format is:</span></span></p>
<p><span data-ttu-id="9ce22-236">boîte de dialogue ; à partir d’une balise</span><span class="sxs-lookup"><span data-stu-id="9ce22-236">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-237"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-237"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-238">DateHeure</span><span class="sxs-lookup"><span data-stu-id="9ce22-238">datetime</span></span></p></td>
<td><p><span data-ttu-id="9ce22-239">Heure de la réponse au premier message d’invitation.</span><span class="sxs-lookup"><span data-stu-id="9ce22-239">Time of the response to the first INVITE message.</span></span> <span data-ttu-id="9ce22-240">Ce champ est généralement rempli par des données générées à partir du message d’invitation initial dans la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-240">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="9ce22-241">S’il n’y a pas de message d’invitation, le champ est peuplé de la date et de l’heure du premier message SIP approprié (BYE, annuler, MESSAGE ou informations).</span><span class="sxs-lookup"><span data-stu-id="9ce22-241">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-242"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-242"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-243">int</span><span class="sxs-lookup"><span data-stu-id="9ce22-243">int</span></span></p></td>
<td><p><span data-ttu-id="9ce22-244">Code de réponse SIP à l’invitation de la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-244">SIP response code to the session invitation.</span></span> <span data-ttu-id="9ce22-245">Ce champ est généralement rempli par des données générées à partir du message d’invitation initial dans la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-245">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="9ce22-246">S’il n’y a pas de message d’invitation, le champ est peuplé de la date et de l’heure du premier message SIP approprié (BYE, annuler, MESSAGE ou informations).</span><span class="sxs-lookup"><span data-stu-id="9ce22-246">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-247"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-247"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-248">int</span><span class="sxs-lookup"><span data-stu-id="9ce22-248">int</span></span></p></td>
<td><p><span data-ttu-id="9ce22-249">ID de diagnostic capturé à partir d’en-têtes SIP.</span><span class="sxs-lookup"><span data-stu-id="9ce22-249">Diagnostic ID captured from SIP headers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-250"><strong>Indiquez</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-250"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-251">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9ce22-251">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-252">Type de contenu de la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-252">Type of content for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-253"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-253"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-254">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9ce22-254">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-255">Nom de domaine complet (FQDN) du serveur frontal qui a capturé les données de la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-255">FQDN of the Front End server that captured the data for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-256"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-256"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-257">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9ce22-257">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-258">Nom de domaine complet (FQDN) du pool qui a capturé les données de la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-258">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-259"><strong>FromEdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-259"><strong>FromEdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-260">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9ce22-260">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-261">Nom de domaine complet (FQDN) du serveur Edge utilisé par l’utilisateur qui a démarré la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-261">FQDN of the Edge server used by the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-262"><strong>ToEdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-262"><strong>ToEdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-263">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9ce22-263">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-264">Nom de domaine complet du serveur Edge utilisé par l’utilisateur qui a démarré la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-264">FQDN of the Edge server used by the user who started the session</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-265"><strong>IsFromInternal</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-265"><strong>IsFromInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-266">bit</span><span class="sxs-lookup"><span data-stu-id="9ce22-266">bit</span></span></p></td>
<td><p><span data-ttu-id="9ce22-267">Indique si l’utilisateur qui a démarré la session s’est connecté à partir du réseau interne.</span><span class="sxs-lookup"><span data-stu-id="9ce22-267">Indicates whether the user who started the session logged on from the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-268"><strong>IsToInternal</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-268"><strong>IsToInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-269">bit</span><span class="sxs-lookup"><span data-stu-id="9ce22-269">bit</span></span></p></td>
<td><p><span data-ttu-id="9ce22-270">Indique si l’utilisateur ayant rejoint la session à partir du réseau interne.</span><span class="sxs-lookup"><span data-stu-id="9ce22-270">Indicates whether the user who joined the session logged on from the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-271"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-271"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-272">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9ce22-272">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-273">Priorité de la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-273">Call priority of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-274"><strong>FromUserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-274"><strong>FromUserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-275">type</span><span class="sxs-lookup"><span data-stu-id="9ce22-275">smallint</span></span></p></td>
<td><p><span data-ttu-id="9ce22-276">Indique les attributs de l’utilisateur qui a démarré la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-276">Indicates the attributes of the user who started the session.</span></span> <span data-ttu-id="9ce22-277">Les définitions d’attribut suivantes sont autorisées :</span><span class="sxs-lookup"><span data-stu-id="9ce22-277">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="9ce22-278">0x01-intégré sur le téléphone de bureau</span><span class="sxs-lookup"><span data-stu-id="9ce22-278">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-279"><strong>ToUserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-279"><strong>ToUserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-280">type</span><span class="sxs-lookup"><span data-stu-id="9ce22-280">smallint</span></span></p></td>
<td><p><span data-ttu-id="9ce22-281">Indique les attributs de l’utilisateur qui a démarré la session.</span><span class="sxs-lookup"><span data-stu-id="9ce22-281">Indicates the attributes of the user who started the session.</span></span> <span data-ttu-id="9ce22-282">Les définitions d’attribut suivantes sont autorisées :</span><span class="sxs-lookup"><span data-stu-id="9ce22-282">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="9ce22-283">0x01-intégré sur le téléphone de bureau</span><span class="sxs-lookup"><span data-stu-id="9ce22-283">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ce22-284"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-284"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-285">type</span><span class="sxs-lookup"><span data-stu-id="9ce22-285">smallint</span></span></p></td>
<td><p><span data-ttu-id="9ce22-286">Indique les attributs d’appel.</span><span class="sxs-lookup"><span data-stu-id="9ce22-286">Indicates the call attributes.</span></span> <span data-ttu-id="9ce22-287">Les définitions d’attribut suivantes sont autorisées :</span><span class="sxs-lookup"><span data-stu-id="9ce22-287">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="9ce22-288">0x01-nouvelle tentative de session</span><span class="sxs-lookup"><span data-stu-id="9ce22-288">0x01 - Retried Session</span></span></p>
<p><span data-ttu-id="9ce22-289">0x02-appel émis par l’agent pour le compte d’un groupe de réponse</span><span class="sxs-lookup"><span data-stu-id="9ce22-289">0x02 - A call made by agent on behalf of a Response Group</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ce22-290"><strong>Emplacement</strong></span><span class="sxs-lookup"><span data-stu-id="9ce22-290"><strong>Location</strong></span></span></p></td>
<td><p><span data-ttu-id="9ce22-291">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="9ce22-291">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="9ce22-292">Emplacement de l’appel d’urgence.</span><span class="sxs-lookup"><span data-stu-id="9ce22-292">Location of emergency call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9ce22-293">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9ce22-293">


</div>

<span> </span>

</div>

</div>

</span></span></div>

