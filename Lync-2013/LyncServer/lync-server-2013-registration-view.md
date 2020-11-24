---
title: 'Lync Server 2013 : affichage d’inscription'
description: 'Lync Server 2013 : affichage d’inscription.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Registration view
ms:assetid: 8a42bc7d-3d4f-43c1-9e15-89b2ee419ade
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688120(v=OCS.15)
ms:contentKeyID: 49733718
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be169cafc324f89cacedda154ca49a8ff1ff39aa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394348"
---
# <a name="registration-view-in-lync-server-2013"></a><span data-ttu-id="c3806-103">Affichage inscription dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c3806-103">Registration view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c3806-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c3806-104">

<span> </span></span></span>

<span data-ttu-id="c3806-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="c3806-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="c3806-106">Le mode d’enregistrement enregistre des informations sur l’inscription des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c3806-106">The Registration view stores information about user registration.</span></span> <span data-ttu-id="c3806-107">Cet affichage a été présenté dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c3806-107">This view was introduced in Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3806-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="c3806-108">Column</span></span></th>
<th><span data-ttu-id="c3806-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="c3806-109">Data Type</span></span></th>
<th><span data-ttu-id="c3806-110">Détails</span><span class="sxs-lookup"><span data-stu-id="c3806-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3806-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-112">DateHeure</span><span class="sxs-lookup"><span data-stu-id="c3806-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="c3806-113">Durée de la demande de session.</span><span class="sxs-lookup"><span data-stu-id="c3806-113">Time of session request.</span></span> <span data-ttu-id="c3806-114">Utilisé conjointement avec SessionIdSeq pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="c3806-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="c3806-115">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="c3806-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3806-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-117">int</span><span class="sxs-lookup"><span data-stu-id="c3806-117">int</span></span></p></td>
<td><p><span data-ttu-id="c3806-118">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="c3806-118">ID number to identify the session.</span></span> <span data-ttu-id="c3806-119">Utilisé conjointement avec SessionIdTime pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="c3806-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="c3806-120">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="c3806-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3806-121"><strong>RegisterTime</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-121"><strong>RegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-122">DateHeure</span><span class="sxs-lookup"><span data-stu-id="c3806-122">datetime</span></span></p></td>
<td><p><span data-ttu-id="c3806-123">Heure à laquelle l’inscription s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c3806-123">Time at which registration occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3806-124"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-124"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-125">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="c3806-125">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="c3806-126">URI de l’utilisateur inscrit.</span><span class="sxs-lookup"><span data-stu-id="c3806-126">URI of the user who registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3806-127"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-127"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3806-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3806-129">Type d’URI de l’utilisateur inscrit.</span><span class="sxs-lookup"><span data-stu-id="c3806-129">Type of URI of the user who registered.</span></span> <span data-ttu-id="c3806-130">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="c3806-130">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3806-131"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-131"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3806-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3806-133">Client de l’utilisateur inscrit.</span><span class="sxs-lookup"><span data-stu-id="c3806-133">Tenant of the user who registered.</span></span> <span data-ttu-id="c3806-134">Pour plus d’informations, voir la <a href="lync-server-2013-tenants-table.md">table locataires dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="c3806-134">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3806-135"><strong>EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-135"><strong>EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-136">identificateur</span><span class="sxs-lookup"><span data-stu-id="c3806-136">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="c3806-137">Identificateur unique du point de terminaison de l’utilisateur enregistré avec.</span><span class="sxs-lookup"><span data-stu-id="c3806-137">Unique identifier of the endpoint of the user registered with.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3806-138"><strong>EndpointEra</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-138"><strong>EndpointEra</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-139">identificateur</span><span class="sxs-lookup"><span data-stu-id="c3806-139">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="c3806-140">Identificateur unique utilisé pour différencier les inscriptions qui impliquent le même utilisateur et le même point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="c3806-140">Unique identifier used to differentiate registrations that involve the same user and the same endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3806-141"><strong>DeRegisterType</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-141"><strong>DeRegisterType</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-142">DateHeure</span><span class="sxs-lookup"><span data-stu-id="c3806-142">datetime</span></span></p></td>
<td><p><span data-ttu-id="c3806-143">Heure à laquelle l’annulation de l’inscription s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c3806-143">Time at which deregistration occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3806-144"><strong>DeRegisterReason</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-144"><strong>DeRegisterReason</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-145">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3806-145">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3806-146">Raison de l’annulation de l’inscription.</span><span class="sxs-lookup"><span data-stu-id="c3806-146">Reason for deregistration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3806-147"><strong>ClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-147"><strong>ClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-148">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3806-148">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3806-149">Version du client utilisée par l’utilisateur inscrit.</span><span class="sxs-lookup"><span data-stu-id="c3806-149">Version of client used by the user who registered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3806-150"><strong>TypeClient</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-150"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-151">int</span><span class="sxs-lookup"><span data-stu-id="c3806-151">int</span></span></p></td>
<td><p><span data-ttu-id="c3806-152">Client utilisé par l’utilisateur inscrit.</span><span class="sxs-lookup"><span data-stu-id="c3806-152">Client used by the user who registered.</span></span> <span data-ttu-id="c3806-153">Pour plus d’informations, voir la <a href="lync-server-2013-useragentdef-table.md">table UserAgentDef dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="c3806-153">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3806-154"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-154"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-155">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="c3806-155">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="c3806-156">Catégorie du client utilisée par l’utilisateur qui est inscrit.</span><span class="sxs-lookup"><span data-stu-id="c3806-156">Category of the client used by the user who registered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3806-157"><strong>Grat</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-157"><strong>IpAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-158">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3806-158">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3806-159">Adresse IP de l’utilisateur avec lequel il a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="c3806-159">IP Address the user registered with.</span></span> <span data-ttu-id="c3806-160">Il s’agit éventuellement d’une adresse IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="c3806-160">This may be an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3806-161"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-161"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-162">varstring (LGA775)</span><span class="sxs-lookup"><span data-stu-id="c3806-162">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="c3806-163">ID de boîte de dialogue SIP.</span><span class="sxs-lookup"><span data-stu-id="c3806-163">SIP dialog ID.</span></span> <span data-ttu-id="c3806-164">Le format de :</span><span class="sxs-lookup"><span data-stu-id="c3806-164">The format of the is:</span></span></p>
<p><span data-ttu-id="c3806-165">boîte de dialogue ; à partir d’une balise</span><span class="sxs-lookup"><span data-stu-id="c3806-165">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3806-166"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-166"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-167">int</span><span class="sxs-lookup"><span data-stu-id="c3806-167">int</span></span></p></td>
<td><p><span data-ttu-id="c3806-168">Code de réponse SIP à l’invitation de la session.</span><span class="sxs-lookup"><span data-stu-id="c3806-168">SIP response code to the session invitation.</span></span> <span data-ttu-id="c3806-169">Ce champ est généralement rempli par des données générées à partir du message d’invitation initial dans la session.</span><span class="sxs-lookup"><span data-stu-id="c3806-169">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="c3806-170">S’il n’y a pas de message d’invitation, le champ est peuplé de la date et de l’heure du premier message SIP approprié (BYE, annuler, MESSAGE ou informations).</span><span class="sxs-lookup"><span data-stu-id="c3806-170">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3806-171"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-171"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-172">int</span><span class="sxs-lookup"><span data-stu-id="c3806-172">int</span></span></p></td>
<td><p><span data-ttu-id="c3806-173">ID de diagnostic capturé à partir de l’en-tête SIP.</span><span class="sxs-lookup"><span data-stu-id="c3806-173">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3806-174"><strong>serveur d’inscriptions</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-174"><strong>Registrar</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-175">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3806-175">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3806-176">Nom de domaine complet du Bureau d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c3806-176">FQDN of the Registrar.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3806-177"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-177"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-178">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3806-178">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3806-179">Nom de domaine complet (FQDN) du pool qui a capturé les données de la session.</span><span class="sxs-lookup"><span data-stu-id="c3806-179">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3806-180"><strong>EdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-180"><strong>EdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-181">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3806-181">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3806-182">Nom de domaine complet (FQDN) du serveur Edge utilisé par l’utilisateur qui est inscrit.</span><span class="sxs-lookup"><span data-stu-id="c3806-182">FQDN of the Edge Server used by the user who registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3806-183"><strong>IsInternal</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-183"><strong>IsInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-184">bit</span><span class="sxs-lookup"><span data-stu-id="c3806-184">bit</span></span></p></td>
<td><p><span data-ttu-id="c3806-185">Indique si l’utilisateur s’est connecté à partir du réseau interne.</span><span class="sxs-lookup"><span data-stu-id="c3806-185">Indicates whether the user logged on from the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3806-186"><strong>IsUserServiceAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-186"><strong>IsUserServiceAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-187">bit</span><span class="sxs-lookup"><span data-stu-id="c3806-187">bit</span></span></p></td>
<td><p><span data-ttu-id="c3806-188">Indique si l’UserService a été disponible au moment de l’inscription.</span><span class="sxs-lookup"><span data-stu-id="c3806-188">Indicates whether the UserService was available at registration time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3806-189"><strong>IsPrimaryRegistrar</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-189"><strong>IsPrimaryRegistrar</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-190">bit</span><span class="sxs-lookup"><span data-stu-id="c3806-190">bit</span></span></p></td>
<td><p><span data-ttu-id="c3806-191">Indique si l’inscription a été apportée au bureau d’enregistrement principal.</span><span class="sxs-lookup"><span data-stu-id="c3806-191">Indicates whether registration was with the primary Registrar.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3806-192"><strong>DeviceMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-192"><strong>DeviceMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-193">bigint</span><span class="sxs-lookup"><span data-stu-id="c3806-193">bigint</span></span></p></td>
<td><p><span data-ttu-id="c3806-194">Adresse MAC de l’appareil inscrit.</span><span class="sxs-lookup"><span data-stu-id="c3806-194">MAC Address of device registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3806-195"><strong>DeviceManufacturer</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-195"><strong>DeviceManufacturer</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3806-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3806-197">Fabricant de l’appareil inscrit.</span><span class="sxs-lookup"><span data-stu-id="c3806-197">Manufacturer of the device registered.</span></span> <span data-ttu-id="c3806-198">Pour plus d’informations, reportez-vous <a href="lync-server-2013-manufacturers-table.md">à la table fabricants dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="c3806-198">See the <a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3806-199"><strong>DeviceHardwareVersion</strong></span><span class="sxs-lookup"><span data-stu-id="c3806-199"><strong>DeviceHardwareVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="c3806-200">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3806-200">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3806-201">Version matérielle de l’appareil inscrit.</span><span class="sxs-lookup"><span data-stu-id="c3806-201">Hardware version of the device registered.</span></span> <span data-ttu-id="c3806-202">Pour plus d’informations, voir la <a href="lync-server-2013-hardwareversions-table.md">table HardwareVersions dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="c3806-202">See the <a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c3806-203">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c3806-203">


</div>

<span> </span>

</div>

</div>

</span></span></div>

