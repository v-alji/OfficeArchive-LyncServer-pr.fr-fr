---
title: 'Lync Server 2013 : Table ConferenceSessionDetails'
description: 'Tableau Lync Server 2013 : ConferenceSessionDetails'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceSessionDetails table
ms:assetid: 9eae6a54-69fd-4966-aa17-7ecee1297ad8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412741(v=OCS.15)
ms:contentKeyID: 48184925
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d101eb1607e366ab814e60acaeee80820fe87c5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434416"
---
# <a name="conferencesessiondetails-table-in-lync-server-2013"></a><span data-ttu-id="a89bb-103">Table ConferenceSessionDetails dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a89bb-103">ConferenceSessionDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a89bb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a89bb-104">

<span> </span></span></span>

<span data-ttu-id="a89bb-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="a89bb-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="a89bb-106">Chaque enregistrement représente une seule session de conférence, qui peut correspondre soit à la session ayant le focus, soit à la session associée à un serveur de conférence particulier.</span><span class="sxs-lookup"><span data-stu-id="a89bb-106">Each record represents one conference session, which could be either the session with Focus or the session with a specific conferencing server.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a89bb-107">Colonne</span><span class="sxs-lookup"><span data-stu-id="a89bb-107">Column</span></span></th>
<th><span data-ttu-id="a89bb-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="a89bb-108">Data Type</span></span></th>
<th><span data-ttu-id="a89bb-109">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="a89bb-109">Key/Index</span></span></th>
<th><span data-ttu-id="a89bb-110">Détails</span><span class="sxs-lookup"><span data-stu-id="a89bb-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a89bb-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="a89bb-112">Datetime</span></span></p></td>
<td><p><span data-ttu-id="a89bb-113">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="a89bb-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-114">Durée de la demande de session ; utilisé conjointement avec <strong>SessionIdSeq</strong> pour identifier de manière unique une session de conférence.</span><span class="sxs-lookup"><span data-stu-id="a89bb-114">Time of session request; used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference session.</span></span> <span data-ttu-id="a89bb-115">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a89bb-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89bb-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-117">int</span><span class="sxs-lookup"><span data-stu-id="a89bb-117">int</span></span></p></td>
<td><p><span data-ttu-id="a89bb-118">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="a89bb-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-119">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="a89bb-119">ID number to identify the session.</span></span> <span data-ttu-id="a89bb-120">Utilisé conjointement avec <strong>SessionIdTime</strong> pour identifier de manière unique une session de conférence.</span><span class="sxs-lookup"><span data-stu-id="a89bb-120">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference session.</span></span> <span data-ttu-id="a89bb-121">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a89bb-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span> *</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a89bb-122"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-122"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-123">int</span><span class="sxs-lookup"><span data-stu-id="a89bb-123">int</span></span></p></td>
<td><p><span data-ttu-id="a89bb-124">Externes</span><span class="sxs-lookup"><span data-stu-id="a89bb-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-125">URI de conférence Focus liée à cette session.</span><span class="sxs-lookup"><span data-stu-id="a89bb-125">Focus conference URI related to this session.</span></span> <span data-ttu-id="a89bb-126">Pour plus d’informations, voir la <a href="lync-server-2013-conferenceuris-table.md">table ConferenceUris dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a89bb-126">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="a89bb-127">Cet URI est un URI de conférence en fonction du focus.</span><span class="sxs-lookup"><span data-stu-id="a89bb-127">This URI is a Focus-based conference URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89bb-128"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-128"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-129">Identificateur</span><span class="sxs-lookup"><span data-stu-id="a89bb-129">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a89bb-130">Identificateur qui différencie les instances des conférences périodiques.</span><span class="sxs-lookup"><span data-stu-id="a89bb-130">Identifier that differentiates between instances of recurring conferences.</span></span> <span data-ttu-id="a89bb-131">Chaque instance de conférence périodique a le même ConferenceURI mais une valeur ConfInstance différente.</span><span class="sxs-lookup"><span data-stu-id="a89bb-131">Each recurring conference instance has the same ConferenceURI but a different ConfInstance value.</span></span></p>
<p><span data-ttu-id="a89bb-132">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a89bb-132">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a89bb-133"><strong>McuConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-133"><strong>McuConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-134">int</span><span class="sxs-lookup"><span data-stu-id="a89bb-134">int</span></span></p></td>
<td><p><span data-ttu-id="a89bb-135">Externes</span><span class="sxs-lookup"><span data-stu-id="a89bb-135">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-136">URI de la Conférence Server Conferencing liée à cette session.</span><span class="sxs-lookup"><span data-stu-id="a89bb-136">Conferencing server conference URI related to this session.</span></span> <span data-ttu-id="a89bb-137">Pour plus d’informations, voir la <a href="lync-server-2013-conferenceuris-table.md">table ConferenceUris dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a89bb-137">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="a89bb-138">Cet URI est l’URI de conférence basée sur le serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="a89bb-138">This URI is the conferencing server-based conference URI.</span></span> <span data-ttu-id="a89bb-139">Pour les sessions de conférence au focus, cette colonne a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="a89bb-139">For Focus conference sessions, this column will be null.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89bb-140"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-140"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-141">int</span><span class="sxs-lookup"><span data-stu-id="a89bb-141">int</span></span></p></td>
<td><p><span data-ttu-id="a89bb-142">Externes</span><span class="sxs-lookup"><span data-stu-id="a89bb-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-143">ID d’un utilisateur dans la session de conférence.</span><span class="sxs-lookup"><span data-stu-id="a89bb-143">ID of one user in the conference session.</span></span> <span data-ttu-id="a89bb-144">Pour plus d’informations, consultez le <a href="lync-server-2013-users-table.md">tableau utilisateurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a89bb-144">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a89bb-145"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-145"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-146">identificateur</span><span class="sxs-lookup"><span data-stu-id="a89bb-146">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a89bb-147">GUID permettant d’identifier l’instance de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="a89bb-147">A GUID to identify the instance of endpoint.</span></span> <span data-ttu-id="a89bb-148">Par exemple, si un utilisateur ouvre une session sur d’autres ordinateurs avec le même compte, chaque ordinateur aura un ID de point de terminaison différent.</span><span class="sxs-lookup"><span data-stu-id="a89bb-148">For example, if one user logs on to different machines with the same account, then each machine will have a different endpoint ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89bb-149"><strong>OnBehalfOfId</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-149"><strong>OnBehalfOfId</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-150">int</span><span class="sxs-lookup"><span data-stu-id="a89bb-150">int</span></span></p></td>
<td><p><span data-ttu-id="a89bb-151">Externes</span><span class="sxs-lookup"><span data-stu-id="a89bb-151">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-152">Indique l’IDENTIFIant de l’utilisateur pour lequel l’appelant a son nom.</span><span class="sxs-lookup"><span data-stu-id="a89bb-152">Indicates the ID of the user of who the caller is on behalf.</span></span> <span data-ttu-id="a89bb-153">Pour plus d’informations, consultez le <a href="lync-server-2013-users-table.md">tableau utilisateurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a89bb-153">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a89bb-154"><strong>ReferredById</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-154"><strong>ReferredById</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-155">int</span><span class="sxs-lookup"><span data-stu-id="a89bb-155">int</span></span></p></td>
<td><p><span data-ttu-id="a89bb-156">Externes</span><span class="sxs-lookup"><span data-stu-id="a89bb-156">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-157">ID de l’utilisateur avec lequel l’appel est soumis.</span><span class="sxs-lookup"><span data-stu-id="a89bb-157">ID of the user by who the call is referred.</span></span> <span data-ttu-id="a89bb-158">Pour plus d’informations, consultez le <a href="lync-server-2013-users-table.md">tableau utilisateurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a89bb-158">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89bb-159"><strong>UserClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-159"><strong>UserClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-160">int</span><span class="sxs-lookup"><span data-stu-id="a89bb-160">int</span></span></p></td>
<td><p><span data-ttu-id="a89bb-161">Externes</span><span class="sxs-lookup"><span data-stu-id="a89bb-161">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-162">Version du client utilisée par l’utilisateur de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="a89bb-162">Client version used by the conference user.</span></span> <span data-ttu-id="a89bb-163">Pour plus d’informations, voir la <a href="lync-server-2013-clientversions-table.md">table ClientVersions dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a89bb-163">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a89bb-164"><strong>ConfClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-164"><strong>ConfClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-165">int</span><span class="sxs-lookup"><span data-stu-id="a89bb-165">int</span></span></p></td>
<td><p><span data-ttu-id="a89bb-166">Externes</span><span class="sxs-lookup"><span data-stu-id="a89bb-166">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-167">Version du client utilisée par le serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="a89bb-167">Client version used by the conference server.</span></span> <span data-ttu-id="a89bb-168">Pour plus d’informations, voir la <a href="lync-server-2013-clientversions-table.md">table ClientVersions dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a89bb-168">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89bb-169"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-169"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-170">DateHeure</span><span class="sxs-lookup"><span data-stu-id="a89bb-170">datetime</span></span></p></td>
<td><p><span data-ttu-id="a89bb-171">Externes</span><span class="sxs-lookup"><span data-stu-id="a89bb-171">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-172">Numéro d’identification identifiant la boîte de dialogue qui a été remplacée par la session actuelle.</span><span class="sxs-lookup"><span data-stu-id="a89bb-172">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="a89bb-173">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a89bb-173">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a89bb-174"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-174"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-175">int</span><span class="sxs-lookup"><span data-stu-id="a89bb-175">int</span></span></p></td>
<td><p><span data-ttu-id="a89bb-176">Externes</span><span class="sxs-lookup"><span data-stu-id="a89bb-176">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-177">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="a89bb-177">ID number to identify the session.</span></span> <span data-ttu-id="a89bb-178">Utilisé conjointement avec <strong>ReplacesDialogIdTime</strong> pour identifier de manière unique une session qui est remplacée par cette session.</span><span class="sxs-lookup"><span data-stu-id="a89bb-178">Used in conjunction with <strong>ReplacesDialogIdTime</strong> to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="a89bb-179">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a89bb-179">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89bb-180"><strong>IsStartedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-180"><strong>IsStartedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-181">bit</span><span class="sxs-lookup"><span data-stu-id="a89bb-181">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a89bb-182">Indique si la session a démarré par le serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="a89bb-182">Indicates if the session started by the conferencing Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a89bb-183"><strong>IsEndedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-183"><strong>IsEndedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-184">bit</span><span class="sxs-lookup"><span data-stu-id="a89bb-184">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a89bb-185">Indique si la session a été terminée par le serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="a89bb-185">Indicates if the session ended by the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89bb-186"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-186"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-187">bit</span><span class="sxs-lookup"><span data-stu-id="a89bb-187">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a89bb-188">Si l’utilisateur est connecté à partir d’un emplacement interne ou non.</span><span class="sxs-lookup"><span data-stu-id="a89bb-188">Whether user is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a89bb-189"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-189"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-190">int</span><span class="sxs-lookup"><span data-stu-id="a89bb-190">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a89bb-191">Code de réponse SIP (Session Initiation Protocol) à l’invitation à la session.</span><span class="sxs-lookup"><span data-stu-id="a89bb-191">Session Initiation Protocol (SIP) response code to the session invitation.</span></span> <span data-ttu-id="a89bb-192">Ce champ est généralement rempli par des données générées à partir du message d’invitation initial dans la session.</span><span class="sxs-lookup"><span data-stu-id="a89bb-192">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="a89bb-193">S’il n’y a pas de message d’invitation, le champ est peuplé de la date et de l’heure du premier message SIP approprié (BYE, annuler, MESSAGE ou informations).</span><span class="sxs-lookup"><span data-stu-id="a89bb-193">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89bb-194"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-194"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-195">int</span><span class="sxs-lookup"><span data-stu-id="a89bb-195">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a89bb-196">ID de diagnostic capturé à partir de l’en-tête SIP.</span><span class="sxs-lookup"><span data-stu-id="a89bb-196">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a89bb-197"><strong>ServerId</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-197"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-198">int</span><span class="sxs-lookup"><span data-stu-id="a89bb-198">int</span></span></p></td>
<td><p><span data-ttu-id="a89bb-199">Externes</span><span class="sxs-lookup"><span data-stu-id="a89bb-199">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-200">ID du serveur frontal utilisé pour cette session.</span><span class="sxs-lookup"><span data-stu-id="a89bb-200">ID of the front-end server used for this session.</span></span> <span data-ttu-id="a89bb-201">Pour plus d’informations, voir le <a href="lync-server-2013-servers-table.md">tableau des serveurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a89bb-201">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89bb-202"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-202"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-203">int</span><span class="sxs-lookup"><span data-stu-id="a89bb-203">int</span></span></p></td>
<td><p><span data-ttu-id="a89bb-204">Externes</span><span class="sxs-lookup"><span data-stu-id="a89bb-204">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-205">ID du pool dans lequel la session a été capturée.</span><span class="sxs-lookup"><span data-stu-id="a89bb-205">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="a89bb-206">Pour plus d’informations, voir la <a href="lync-server-2013-pools-table.md">table pools dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a89bb-206">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a89bb-207"><strong>MediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-207"><strong>MediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-208">int</span><span class="sxs-lookup"><span data-stu-id="a89bb-208">int</span></span></p></td>
<td><p><span data-ttu-id="a89bb-209">Externes</span><span class="sxs-lookup"><span data-stu-id="a89bb-209">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-210">Serveur de médiation utilisé par l’appel.</span><span class="sxs-lookup"><span data-stu-id="a89bb-210">The Mediation Server the call is using.</span></span> <span data-ttu-id="a89bb-211">Pour plus d’informations, voir la <a href="lync-server-2013-mediationservers-table.md">table MediationServers dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a89bb-211">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89bb-212"><strong>GatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-212"><strong>GatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-213">int</span><span class="sxs-lookup"><span data-stu-id="a89bb-213">int</span></span></p></td>
<td><p><span data-ttu-id="a89bb-214">Externes</span><span class="sxs-lookup"><span data-stu-id="a89bb-214">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-215">Passerelle utilisée par l’appel.</span><span class="sxs-lookup"><span data-stu-id="a89bb-215">The gateway the call is using.</span></span> <span data-ttu-id="a89bb-216">Pour plus d’informations, voir le <a href="lync-server-2013-gateways-table.md">tableau passerelles dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a89bb-216">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a89bb-217"><strong>EdgeServerId</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-217"><strong>EdgeServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-218">int</span><span class="sxs-lookup"><span data-stu-id="a89bb-218">int</span></span></p></td>
<td><p><span data-ttu-id="a89bb-219">Externes</span><span class="sxs-lookup"><span data-stu-id="a89bb-219">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-220">Serveur Edge utilisé par l’appel.</span><span class="sxs-lookup"><span data-stu-id="a89bb-220">The Edge Server the call is using.</span></span> <span data-ttu-id="a89bb-221">Pour plus d’informations, voir la <a href="lync-server-2013-edgeservers-table.md">table EdgeServers dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a89bb-221">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89bb-222"><strong>ContentTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-222"><strong>ContentTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-223">int</span><span class="sxs-lookup"><span data-stu-id="a89bb-223">int</span></span></p></td>
<td><p><span data-ttu-id="a89bb-224">Externes</span><span class="sxs-lookup"><span data-stu-id="a89bb-224">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-225">Type de contenu utilisé dans la session.</span><span class="sxs-lookup"><span data-stu-id="a89bb-225">Content type used in the session.</span></span> <span data-ttu-id="a89bb-226">Pour plus d’informations, voir la <a href="lync-server-2013-contenttypes-table.md">table ContentTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="a89bb-226">See the <a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a89bb-227"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-227"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-228">DateHeure</span><span class="sxs-lookup"><span data-stu-id="a89bb-228">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a89bb-229">Heure de la première demande d’invitation.</span><span class="sxs-lookup"><span data-stu-id="a89bb-229">The time of the first INVITE request.</span></span> <span data-ttu-id="a89bb-230">Ce champ est généralement rempli par des données générées à partir du message d’invitation initial dans la session.</span><span class="sxs-lookup"><span data-stu-id="a89bb-230">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="a89bb-231">S’il n’y a pas de message d’invitation, le champ est peuplé de la date et de l’heure du premier message SIP approprié (BYE, annuler, MESSAGE ou informations).</span><span class="sxs-lookup"><span data-stu-id="a89bb-231">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89bb-232"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-232"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-233">DateHeure</span><span class="sxs-lookup"><span data-stu-id="a89bb-233">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a89bb-234">Heure de la première réponse SIP.</span><span class="sxs-lookup"><span data-stu-id="a89bb-234">Time of the first SIP RESPONSE.</span></span> <span data-ttu-id="a89bb-235">Ce champ est généralement rempli par des données générées à partir du message d’invitation initial dans la session.</span><span class="sxs-lookup"><span data-stu-id="a89bb-235">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="a89bb-236">S’il n’y a pas de message d’invitation, le champ est peuplé de la date et de l’heure du premier message SIP approprié (BYE, annuler, MESSAGE ou informations).</span><span class="sxs-lookup"><span data-stu-id="a89bb-236">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a89bb-237"><strong>SessionEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-237"><strong>SessionEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-238">DateHeure</span><span class="sxs-lookup"><span data-stu-id="a89bb-238">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a89bb-239">Heure de fin de la session.</span><span class="sxs-lookup"><span data-stu-id="a89bb-239">The time when the session is ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89bb-240"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-240"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-241">tinyint</span><span class="sxs-lookup"><span data-stu-id="a89bb-241">tinyint</span></span></p></td>
<td><p><span data-ttu-id="a89bb-242">Externes</span><span class="sxs-lookup"><span data-stu-id="a89bb-242">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a89bb-243">Contient la valeur du type d’URI MCU de la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="a89bb-243">Contains the MCU URI type value from the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a>.</span></span> <span data-ttu-id="a89bb-244">Ce champ permet d’améliorer les performances de requête.</span><span class="sxs-lookup"><span data-stu-id="a89bb-244">This field is used for improving query performance.</span></span></p>
<p><span data-ttu-id="a89bb-245">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a89bb-245">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a89bb-246"><strong>UserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-246"><strong>UserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-247">type</span><span class="sxs-lookup"><span data-stu-id="a89bb-247">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a89bb-248">Un ensemble de bits indiquant les attributs de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a89bb-248">A bit set that indicates the user attributes.</span></span> <span data-ttu-id="a89bb-249">Les définitions d’attribut suivantes apparaissent :</span><span class="sxs-lookup"><span data-stu-id="a89bb-249">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="a89bb-250">Intégré au téléphone de bureau-1</span><span class="sxs-lookup"><span data-stu-id="a89bb-250">Integrated with desktop phone - 1</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89bb-251"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="a89bb-251"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="a89bb-252">type</span><span class="sxs-lookup"><span data-stu-id="a89bb-252">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a89bb-253">Un ensemble de bits qui indique les attributs d’appel.</span><span class="sxs-lookup"><span data-stu-id="a89bb-253">A bit set that indicates the call attributes.</span></span> <span data-ttu-id="a89bb-254">Les définitions d’attribut suivantes apparaissent :</span><span class="sxs-lookup"><span data-stu-id="a89bb-254">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="a89bb-255">Nouvelle tentative de session-1</span><span class="sxs-lookup"><span data-stu-id="a89bb-255">Retried Session - 1</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a89bb-256">\* Pour la plupart des sessions, SessionIdSeq aura la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="a89bb-256">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="a89bb-257">S’il s’agit d’une session à partir de la même heure, le SessionIdSeq de l’une sera 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="a89bb-257">If multiple sessions start at exactly the same time, the SessionIdSeq for one will be 1, for another will be 2, and so on.</span></span>

<span data-ttu-id="a89bb-258"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a89bb-258"></div>

<span> </span>

</div>

</div>

</span></span></div>

