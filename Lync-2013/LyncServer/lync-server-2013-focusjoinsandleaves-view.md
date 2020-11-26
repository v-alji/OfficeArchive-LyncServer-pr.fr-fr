---
title: 'Affichage Lync Server 2013 : FocusJoinsAndLeaves'
description: 'Affichage Lync Server 2013 : FocusJoinsAndLeaves'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FocusJoinsAndLeaves view
ms:assetid: 226460ef-766f-4d61-80cb-f332b65a210d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687992(v=OCS.15)
ms:contentKeyID: 49733582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c6f68c44461e378e9ebedce1305ee6b384a7a8a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428106"
---
# <a name="focusjoinsandleaves-view-in-lync-server-2013"></a><span data-ttu-id="20de6-103">Affichage FocusJoinsAndLeaves dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20de6-103">FocusJoinsAndLeaves view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20de6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20de6-104">

<span> </span></span></span>

<span data-ttu-id="20de6-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="20de6-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="20de6-106">Le mode FocusJoinsAndLeaves stocke des informations sur la participation et la conservation des informations pour une conférence.</span><span class="sxs-lookup"><span data-stu-id="20de6-106">The FocusJoinsAndLeaves view stores information about join and leave information for one conference.</span></span> <span data-ttu-id="20de6-107">Chaque conférence est représentée dans cette vue par un enregistrement écrit chaque fois qu’un utilisateur rejoint et quitte la Conférence.</span><span class="sxs-lookup"><span data-stu-id="20de6-107">Each conference is represented in this view by a record written each time a user joins and leaves the conference.</span></span> <span data-ttu-id="20de6-108">Cet affichage a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="20de6-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20de6-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="20de6-109">Column</span></span></th>
<th><span data-ttu-id="20de6-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="20de6-110">Data Type</span></span></th>
<th><span data-ttu-id="20de6-111">Détails</span><span class="sxs-lookup"><span data-stu-id="20de6-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20de6-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="20de6-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="20de6-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="20de6-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="20de6-114">Durée de l’instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="20de6-114">Time of conference instance.</span></span> <span data-ttu-id="20de6-115">Utilisé conjointement avec SessionIdSeq pour identifier de manière unique une instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="20de6-115">Used in conjunction with SessionIdSeq to uniquely identify a conference instance.</span></span> <span data-ttu-id="20de6-116">Pour plus d’informations, voir le <a href="lync-server-2013-conferences-table.md">tableau conférences dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="20de6-116">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20de6-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="20de6-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="20de6-118">int</span><span class="sxs-lookup"><span data-stu-id="20de6-118">int</span></span></p></td>
<td><p><span data-ttu-id="20de6-119">Numéro d’identification pour identifier l’instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="20de6-119">ID number to identify the conference instance.</span></span> <span data-ttu-id="20de6-120">Utilisé conjointement avec SessionIdTime pour identifier de manière unique une instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="20de6-120">Used in conjunction with SessionIdTime to uniquely identify a conference instance.</span></span> <span data-ttu-id="20de6-121">Pour plus d’informations, voir le <a href="lync-server-2013-conferences-table.md">tableau conférences dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="20de6-121">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20de6-122"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="20de6-122"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="20de6-123">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="20de6-123">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="20de6-124">URI de l’utilisateur qui a capturé les informations de conférence jointes.</span><span class="sxs-lookup"><span data-stu-id="20de6-124">URI of the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20de6-125"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="20de6-125"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="20de6-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="20de6-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="20de6-127">Type d’URI de l’utilisateur qui a capturé les informations de conférence jointes.</span><span class="sxs-lookup"><span data-stu-id="20de6-127">Type of URI of the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="20de6-128">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="20de6-128">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20de6-129"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="20de6-129"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="20de6-130">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="20de6-130">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="20de6-131">Client de l’utilisateur qui a capturé des informations de conférence jointes.</span><span class="sxs-lookup"><span data-stu-id="20de6-131">Tenant of the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="20de6-132">Pour plus d’informations, voir la <a href="lync-server-2013-tenants-table.md">table locataires dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="20de6-132">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20de6-133"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="20de6-133"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="20de6-134">identificateur</span><span class="sxs-lookup"><span data-stu-id="20de6-134">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="20de6-135">Identificateur unique de l’utilisateur qui a capturé les informations de conférence jointes.</span><span class="sxs-lookup"><span data-stu-id="20de6-135">Unique identifier of the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20de6-136"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="20de6-136"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="20de6-137">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="20de6-137">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="20de6-138">Version du client utilisée par l’utilisateur et qui a capturé les informations de conférence jointes.</span><span class="sxs-lookup"><span data-stu-id="20de6-138">Version of client used by the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20de6-139"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="20de6-139"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="20de6-140">int</span><span class="sxs-lookup"><span data-stu-id="20de6-140">int</span></span></p></td>
<td><p><span data-ttu-id="20de6-141">Client utilisé par l’utilisateur et qui a capturé des informations de conférence jointes.</span><span class="sxs-lookup"><span data-stu-id="20de6-141">Client used by the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="20de6-142">Pour plus d’informations, voir <a href="lync-server-2013-useragentdef-table.md">table UserAgentDef dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="20de6-142">See <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20de6-143"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="20de6-143"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="20de6-144">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="20de6-144">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="20de6-145">Nom de la catégorie du client utilisée par l’utilisateur et ayant capturé des informations de conférence.</span><span class="sxs-lookup"><span data-stu-id="20de6-145">Name of the category of the client used by the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20de6-146"><strong>FocusUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="20de6-146"><strong>FocusUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="20de6-147">int</span><span class="sxs-lookup"><span data-stu-id="20de6-147">int</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20de6-148"><strong>IsuserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="20de6-148"><strong>IsuserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="20de6-149">bit</span><span class="sxs-lookup"><span data-stu-id="20de6-149">bit</span></span></p></td>
<td><p><span data-ttu-id="20de6-150">Bit qui indique si l’utilisateur est ou non un utilisateur interne.</span><span class="sxs-lookup"><span data-stu-id="20de6-150">Bit that represents whether the user is an internal user or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20de6-151"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="20de6-151"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="20de6-152">DateHeure</span><span class="sxs-lookup"><span data-stu-id="20de6-152">datetime</span></span></p></td>
<td><p><span data-ttu-id="20de6-153">Durée de la demande de session.</span><span class="sxs-lookup"><span data-stu-id="20de6-153">Time of session request.</span></span> <span data-ttu-id="20de6-154">Utilisé conjointement avec SessionIdSeq pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="20de6-154">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="20de6-155">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="20de6-155">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20de6-156"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="20de6-156"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="20de6-157">int</span><span class="sxs-lookup"><span data-stu-id="20de6-157">int</span></span></p></td>
<td><p><span data-ttu-id="20de6-158">Si un utilisateur ouvre une session sur plusieurs ordinateurs ou appareils en même temps, UserInstance est utilisé pour identifier de façon unique la combinaison utilisateur/appareil.</span><span class="sxs-lookup"><span data-stu-id="20de6-158">If a user is logged on at multiple computers or devices at the same time, UserInstance is used to uniquely identify the user/device combination.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20de6-159"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="20de6-159"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="20de6-160">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="20de6-160">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="20de6-161">ID de la boîte de dialogue SIP de la session.</span><span class="sxs-lookup"><span data-stu-id="20de6-161">SIP dialog ID of the session.</span></span> <span data-ttu-id="20de6-162">Le format est : boîte de dialogue ; de-balise ; à balise.</span><span class="sxs-lookup"><span data-stu-id="20de6-162">The format is: dialog;from-tag;to-tag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20de6-163"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="20de6-163"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="20de6-164">DateHeure</span><span class="sxs-lookup"><span data-stu-id="20de6-164">datetime</span></span></p></td>
<td><p><span data-ttu-id="20de6-165">Temps pendant lequel l’utilisateur a rejoint la Conférence.</span><span class="sxs-lookup"><span data-stu-id="20de6-165">Time that the user joined the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20de6-166"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="20de6-166"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="20de6-167">DateHeure</span><span class="sxs-lookup"><span data-stu-id="20de6-167">datetime</span></span></p></td>
<td><p><span data-ttu-id="20de6-168">Temps pendant lequel l’utilisateur a quitté la Conférence.</span><span class="sxs-lookup"><span data-stu-id="20de6-168">Time that the user left the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20de6-169"><strong>UserRole</strong></span><span class="sxs-lookup"><span data-stu-id="20de6-169"><strong>UserRole</strong></span></span></p></td>
<td><p><span data-ttu-id="20de6-170">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="20de6-170">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="20de6-171">Le rôle de l’utilisateur dans la Conférence, tel que le présentateur ou le participant.</span><span class="sxs-lookup"><span data-stu-id="20de6-171">User’s role in the conference, such as Presenter or Attendee.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="20de6-172">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20de6-172">


</div>

<span> </span>

</div>

</div>

</span></span></div>

