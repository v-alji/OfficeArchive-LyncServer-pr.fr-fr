---
title: 'Affichage Lync Server 2013 : ConferenceSessionDetails'
description: 'Affichage Lync Server 2013 : ConferenceSessionDetails'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceSessionDetails view
ms:assetid: 5858c84d-baed-421d-ad1d-3726e150e256
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688066(v=OCS.15)
ms:contentKeyID: 49733660
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d1c62f020413efecdbc0f909618256ccc7308d4f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434395"
---
# <a name="conferencesessiondetails-view-in-lync-server-2013"></a><span data-ttu-id="cac72-103">Affichage ConferenceSessionDetails dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cac72-103">ConferenceSessionDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cac72-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cac72-104">

<span> </span></span></span>

<span data-ttu-id="cac72-105">_**Dernière modification de la rubrique :** 2012-11-12_</span><span class="sxs-lookup"><span data-stu-id="cac72-105">_**Topic Last Modified:** 2012-11-12_</span></span>

<span data-ttu-id="cac72-106">Le mode ConferenceSessionDetails stocke les informations sur les sessions multiparties.</span><span class="sxs-lookup"><span data-stu-id="cac72-106">The ConferenceSessionDetails view stores information about multiparty sessions.</span></span> <span data-ttu-id="cac72-107">Chaque enregistrement représente une seule session de conférence, qui peut correspondre soit à la session ayant le focus, soit à la session associée à un serveur de conférence particulier.</span><span class="sxs-lookup"><span data-stu-id="cac72-107">Each record represents one conference session, which could be either the session with Focus or the session with a specific conferencing server.</span></span> <span data-ttu-id="cac72-108">Cet affichage a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cac72-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cac72-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="cac72-109">Column</span></span></th>
<th><span data-ttu-id="cac72-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="cac72-110">Data Type</span></span></th>
<th><span data-ttu-id="cac72-111">Détails</span><span class="sxs-lookup"><span data-stu-id="cac72-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cac72-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="cac72-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="cac72-114">Durée de la demande de session.</span><span class="sxs-lookup"><span data-stu-id="cac72-114">Time of session request.</span></span> <span data-ttu-id="cac72-115">Utilisé conjointement avec SessionIdSeq pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="cac72-115">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="cac72-116">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cac72-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-118">int</span><span class="sxs-lookup"><span data-stu-id="cac72-118">int</span></span></p></td>
<td><p><span data-ttu-id="cac72-119">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-119">ID number to identify the session.</span></span> <span data-ttu-id="cac72-120">Utilisé conjointement avec SessionIdTime pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="cac72-120">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="cac72-121">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cac72-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-122"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-122"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-123">DateHeure</span><span class="sxs-lookup"><span data-stu-id="cac72-123">datetime</span></span></p></td>
<td><p><span data-ttu-id="cac72-124">Heure de la première demande d’invitation.</span><span class="sxs-lookup"><span data-stu-id="cac72-124">Time of the first INVITE request.</span></span> <span data-ttu-id="cac72-125">Ce champ est généralement rempli par des données générées à partir du message d’invitation initial dans la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-125">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="cac72-126">S’il n’y a pas de message d’invitation, le champ est peuplé de la date et de l’heure du premier message SIP approprié (BYE, annuler, MESSAGE ou informations).</span><span class="sxs-lookup"><span data-stu-id="cac72-126">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-127"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-127"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-128">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="cac72-128">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="cac72-129">URI de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="cac72-129">URI of the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-130"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-130"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-131">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cac72-131">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cac72-132">URI du type de conférence.</span><span class="sxs-lookup"><span data-stu-id="cac72-132">Type of conference URI.</span></span> <span data-ttu-id="cac72-133">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cac72-133">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-134"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-134"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-135">identificateur</span><span class="sxs-lookup"><span data-stu-id="cac72-135">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="cac72-136">Identificateur qui différencie les instances des conférences périodiques.</span><span class="sxs-lookup"><span data-stu-id="cac72-136">Identifier that differentiates between instances of recurring conferences.</span></span> <span data-ttu-id="cac72-137">Chaque instance de conférence périodique a le même ConferenceURI mais une valeur ConfInstance différente.</span><span class="sxs-lookup"><span data-stu-id="cac72-137">Each recurring conference instance has the same ConferenceURI but a different ConfInstance value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-138"><strong>McuConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-138"><strong>McuConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="cac72-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="cac72-140">URI du serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="cac72-140">URI of the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-141"><strong>McuConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-141"><strong>McuConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-142">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cac72-142">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cac72-143">Type d’URI du serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="cac72-143">Type of conferencing server URI.</span></span> <span data-ttu-id="cac72-144">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cac72-144">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-145"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-145"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-146">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="cac72-146">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="cac72-147">URI de l’utilisateur impliqué dans la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-147">URI of the user involved in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-148"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-148"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-149">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cac72-149">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cac72-150">Type d’URI de l’utilisateur qui faisait partie de la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-150">Type of URI of the user whose was part of the session.</span></span> <span data-ttu-id="cac72-151">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cac72-151">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-152"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-152"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cac72-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cac72-154">Client de l’utilisateur qui faisait partie de la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-154">Tenant of the user whose was part of the session.</span></span> <span data-ttu-id="cac72-155">Pour plus d’informations, voir la <a href="lync-server-2013-tenants-table.md">table locataires dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cac72-155">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-156"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-156"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-157">identificateur</span><span class="sxs-lookup"><span data-stu-id="cac72-157">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="cac72-158">Identificateur unique de l’utilisateur dont vous participez à la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-158">Unique identifier of the user whose was part of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-159"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-159"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-160">DateHeure</span><span class="sxs-lookup"><span data-stu-id="cac72-160">datetime</span></span></p></td>
<td><p><span data-ttu-id="cac72-161">Heure de fin de la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-161">End time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-162"><strong>ConferenceClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-162"><strong>ConferenceClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-163">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cac72-163">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cac72-164">Version du serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="cac72-164">Version of conference server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-165"><strong>ConferenceClientType</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-165"><strong>ConferenceClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-166">int</span><span class="sxs-lookup"><span data-stu-id="cac72-166">int</span></span></p></td>
<td><p><span data-ttu-id="cac72-167">Type du serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="cac72-167">Type of conference server.</span></span> <span data-ttu-id="cac72-168">Pour plus d’informations, voir la <a href="lync-server-2013-useragentdef-table.md">table UserAgentDef dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cac72-168">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-169"><strong>ConferenceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-169"><strong>ConferenceCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-170">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="cac72-170">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="cac72-171">Catégorie de serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="cac72-171">Conference server category.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-172"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-172"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-173">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cac72-173">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cac72-174">Version du client utilisée par l’utilisateur ayant participé à la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-174">Version of client used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-175"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-175"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-176">int</span><span class="sxs-lookup"><span data-stu-id="cac72-176">int</span></span></p></td>
<td><p><span data-ttu-id="cac72-177">Client utilisé par l’utilisateur ayant participé à la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-177">Client used by the user who participated in the session.</span></span> <span data-ttu-id="cac72-178">Pour plus d’informations, voir la <a href="lync-server-2013-useragentdef-table.md">table UserAgentDef dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cac72-178">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-179"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-179"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-180">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="cac72-180">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="cac72-181">Nom de la catégorie du client utilisée par l’utilisateur qui faisait partie de la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-181">Name of the category of the client used by the user who was part of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-182"><strong>OnBehalfOfUri</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-182"><strong>OnBehalfOfUri</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-183">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="cac72-183">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="cac72-184">URI de l’utilisateur au nom duquel la session a été démarrée.</span><span class="sxs-lookup"><span data-stu-id="cac72-184">URI of the user on whose behalf the session was started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-185"><strong>OnBehalfOfUriType</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-185"><strong>OnBehalfOfUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-186">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cac72-186">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cac72-187">Type d’URI de l’utilisateur au nom duquel la session a démarré.</span><span class="sxs-lookup"><span data-stu-id="cac72-187">Type of URI of the user on whose behalf the session was started.</span></span> <span data-ttu-id="cac72-188">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cac72-188">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-189"><strong>OnBehalfOfTenant</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-189"><strong>OnBehalfOfTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-190">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cac72-190">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cac72-191">Client de l’utilisateur dont le nom est démarré.</span><span class="sxs-lookup"><span data-stu-id="cac72-191">Tenant of the user whose on behalf the session was started.</span></span> <span data-ttu-id="cac72-192">Pour plus d’informations, voir la <a href="lync-server-2013-tenants-table.md">table locataires dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cac72-192">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-193"><strong>ReferredByUri</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-193"><strong>ReferredByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-194">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="cac72-194">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="cac72-195">URI de l’utilisateur qui a expertisé la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-195">URI of the user who referred the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-196"><strong>ReferredByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-196"><strong>ReferredByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-197">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cac72-197">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cac72-198">Type d’URI de l’utilisateur qui a expertisé la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-198">Type of URI of the user who referred the session.</span></span> <span data-ttu-id="cac72-199">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cac72-199">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-200"><strong>ReferredByUriTenant</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-200"><strong>ReferredByUriTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-201">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cac72-201">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cac72-202">Client de l’utilisateur qui a fait appel à la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-202">Tenant of the user who referred the session.</span></span> <span data-ttu-id="cac72-203">Pour plus d’informations, voir la <a href="lync-server-2013-tenants-table.md">table locataires dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cac72-203">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-204"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-204"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-205">varstring (LGA775)</span><span class="sxs-lookup"><span data-stu-id="cac72-205">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="cac72-206">ID de boîte de dialogue SIP.</span><span class="sxs-lookup"><span data-stu-id="cac72-206">SIP dialog ID.</span></span> <span data-ttu-id="cac72-207">Le format est</span><span class="sxs-lookup"><span data-stu-id="cac72-207">The format is</span></span></p>
<p><span data-ttu-id="cac72-208">:d ialog ; from-tag ; to-tag</span><span class="sxs-lookup"><span data-stu-id="cac72-208">:dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-209"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-209"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-210">DateHeure</span><span class="sxs-lookup"><span data-stu-id="cac72-210">datetime</span></span></p></td>
<td><p><span data-ttu-id="cac72-211">Numéro d’identification identifiant la boîte de dialogue qui a été remplacée par la session actuelle.</span><span class="sxs-lookup"><span data-stu-id="cac72-211">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="cac72-212">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cac72-212">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-213"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-213"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-214">int</span><span class="sxs-lookup"><span data-stu-id="cac72-214">int</span></span></p></td>
<td><p><span data-ttu-id="cac72-215">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-215">ID number to identify the session.</span></span> <span data-ttu-id="cac72-216">Utilisé conjointement avec ReplaceDialogIdTime pour identifier de manière unique une session qui est remplacée par cette session.</span><span class="sxs-lookup"><span data-stu-id="cac72-216">Used in conjunction with ReplaceDialogIdTime to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="cac72-217">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cac72-217">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-218"><strong>ReplacesDialogId</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-218"><strong>ReplacesDialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-219">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="cac72-219">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="cac72-220">ID de boîte de dialogue SIP le remplacement de la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-220">SIP dialog ID the session replaces.</span></span> <span data-ttu-id="cac72-221">Le format de :</span><span class="sxs-lookup"><span data-stu-id="cac72-221">The format of the is:</span></span></p>
<p><span data-ttu-id="cac72-222">boîte de dialogue ; à partir d’une balise</span><span class="sxs-lookup"><span data-stu-id="cac72-222">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-223"><strong>IsStartedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-223"><strong>IsStartedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-224">bit</span><span class="sxs-lookup"><span data-stu-id="cac72-224">bit</span></span></p></td>
<td><p><span data-ttu-id="cac72-225">Indique si la session a été démarrée par le serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="cac72-225">Indicates whether the session was started by the conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-226"><strong>IsEndedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-226"><strong>IsEndedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-227">bit</span><span class="sxs-lookup"><span data-stu-id="cac72-227">bit</span></span></p></td>
<td><p><span data-ttu-id="cac72-228">Indique si la session a été terminée par le serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="cac72-228">Indicates whether the session was ended by the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-229"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-229"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-230">bit</span><span class="sxs-lookup"><span data-stu-id="cac72-230">bit</span></span></p></td>
<td><p><span data-ttu-id="cac72-231">Indique si l’utilisateur s’est connecté à partir du réseau interne.</span><span class="sxs-lookup"><span data-stu-id="cac72-231">Indicates whether the user logged on from the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-232"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-232"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-233">DateHeure</span><span class="sxs-lookup"><span data-stu-id="cac72-233">datetime</span></span></p></td>
<td><p><span data-ttu-id="cac72-234">Heure de la réponse au premier message d’invitation.</span><span class="sxs-lookup"><span data-stu-id="cac72-234">Time of the response to the first INVITE message.</span></span> <span data-ttu-id="cac72-235">Ce champ est généralement rempli par des données générées à partir du message d’invitation initial dans la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-235">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="cac72-236">S’il n’y a pas de message d’invitation, le champ est peuplé de la date et de l’heure du premier message SIP approprié (BYE, annuler, MESSAGE ou informations).</span><span class="sxs-lookup"><span data-stu-id="cac72-236">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-237"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-237"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-238">int</span><span class="sxs-lookup"><span data-stu-id="cac72-238">int</span></span></p></td>
<td><p><span data-ttu-id="cac72-239">Code de réponse SIP à l’invitation de la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-239">SIP response code to the session invitation.</span></span> <span data-ttu-id="cac72-240">Ce champ est généralement rempli par des données générées à partir du message d’invitation initial dans la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-240">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="cac72-241">S’il n’y a pas de message d’invitation, le champ est peuplé de la date et de l’heure du premier message SIP approprié (BYE, annuler, MESSAGE ou informations).</span><span class="sxs-lookup"><span data-stu-id="cac72-241">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-242"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-242"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-243">int</span><span class="sxs-lookup"><span data-stu-id="cac72-243">int</span></span></p></td>
<td><p><span data-ttu-id="cac72-244">ID de diagnostic capturé à partir d’en-têtes SIP de session.</span><span class="sxs-lookup"><span data-stu-id="cac72-244">Diagnostic ID captured from session SIP headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-245"><strong>Indiquez</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-245"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-246">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cac72-246">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cac72-247">Type de contenu de la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-247">Content type for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-248"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-248"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-249">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cac72-249">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cac72-250">Nom de domaine complet (FQDN) du serveur frontal qui a capturé les données de la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-250">FQDN of the Front End server that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-251"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-251"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-252">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cac72-252">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cac72-253">Nom de domaine complet (FQDN) du pool qui a capturé les données de la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-253">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-254"><strong>MediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-254"><strong>MediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-255">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cac72-255">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cac72-256">Serveur de médiation utilisé par l’utilisateur ayant participé à la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-256">Mediation Server used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-257"><strong>Passerelle</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-257"><strong>Gateway</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-258">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cac72-258">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cac72-259">Passerelle utilisée par l’utilisateur ayant participé à la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-259">Gateway used by the user who participated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-260"><strong>EdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-260"><strong>EdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-261">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cac72-261">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cac72-262">Nom de domaine complet (FQDN) du serveur Edge utilisé par l’utilisateur ayant participé à la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-262">FQDN of the Edge server used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac72-263"><strong>UserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-263"><strong>UserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-264">type</span><span class="sxs-lookup"><span data-stu-id="cac72-264">smallint</span></span></p></td>
<td><p><span data-ttu-id="cac72-265">Indique les attributs de l’utilisateur ayant participé à la session.</span><span class="sxs-lookup"><span data-stu-id="cac72-265">Indicates the attributes of the user who participated in the session.</span></span> <span data-ttu-id="cac72-266">Les définitions d’attribut suivantes sont autorisées :</span><span class="sxs-lookup"><span data-stu-id="cac72-266">The following attribute definitions allowed:</span></span></p>
<p><span data-ttu-id="cac72-267">0x01-intégré sur le téléphone de bureau</span><span class="sxs-lookup"><span data-stu-id="cac72-267">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac72-268"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="cac72-268"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="cac72-269">type</span><span class="sxs-lookup"><span data-stu-id="cac72-269">smallint</span></span></p></td>
<td><p><span data-ttu-id="cac72-270">Indique les attributs d’appel.</span><span class="sxs-lookup"><span data-stu-id="cac72-270">Indicates the call attributes.</span></span> <span data-ttu-id="cac72-271">Les définitions d’attribut suivantes sont autorisées :</span><span class="sxs-lookup"><span data-stu-id="cac72-271">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="cac72-272">0x01-nouvelle tentative de Session0</span><span class="sxs-lookup"><span data-stu-id="cac72-272">0x01 - Retried Session0</span></span></p>
<p><span data-ttu-id="cac72-273">x02 : appel passé par l’agent pour le compte d’un Response Group</span><span class="sxs-lookup"><span data-stu-id="cac72-273">x02 - A call made by agent on behalf of a Response Group</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="cac72-274">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cac72-274">


</div>

<span> </span>

</div>

</div>

</span></span></div>

