---
title: 'Affichage Lync Server 2013 : ErrorReport'
description: 'Affichage Lync Server 2013 : ErrorReport'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorReport view
ms:assetid: ca873f7e-b18b-4eaf-8db0-5f9d5a9b60a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721887(v=OCS.15)
ms:contentKeyID: 49733821
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 50fb0a362c71d8dfb5873157e7b1ed3d3eb680ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428523"
---
# <a name="errorreport-view-in-lync-server-2013"></a><span data-ttu-id="4ba2a-103">Affichage ErrorReport dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4ba2a-103">ErrorReport view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4ba2a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4ba2a-104">

<span> </span></span></span>

<span data-ttu-id="4ba2a-105">_**Dernière modification de la rubrique :** 2013-01-22_</span><span class="sxs-lookup"><span data-stu-id="4ba2a-105">_**Topic Last Modified:** 2013-01-22_</span></span>

<span data-ttu-id="4ba2a-106">Le mode ErrorReport stocke les informations sur les erreurs signalées.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-106">The ErrorReport view stores information about errors reported.</span></span> <span data-ttu-id="4ba2a-107">Chaque enregistrement correspond à une occurrence d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-107">Each record is one error occurrence.</span></span> <span data-ttu-id="4ba2a-108">Les erreurs sont capturées par l’agent CDR exécuté sur le serveur frontal ou envoyées par le client.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-108">The errors are captured either by the CDR agent running on the front-end server or sent from the client.</span></span> <span data-ttu-id="4ba2a-109">Cet affichage a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-109">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4ba2a-110">Colonne</span><span class="sxs-lookup"><span data-stu-id="4ba2a-110">Column</span></span></th>
<th><span data-ttu-id="4ba2a-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="4ba2a-111">Data Type</span></span></th>
<th><span data-ttu-id="4ba2a-112">Détails</span><span class="sxs-lookup"><span data-stu-id="4ba2a-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ba2a-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-114">DateHeure</span><span class="sxs-lookup"><span data-stu-id="4ba2a-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-115">L’heure de l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-115">Time of error occurred.</span></span> <span data-ttu-id="4ba2a-116">Utilisé conjointement avec ErrorReportSeq pour identifier de manière unique une erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-116">Used in conjunction with ErrorReportSeq to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ba2a-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-118">int</span><span class="sxs-lookup"><span data-stu-id="4ba2a-118">int</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-119">Numéro d’identification pour identifier l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-119">ID number to identify the error.</span></span> <span data-ttu-id="4ba2a-120">Utilisé conjointement avec ErrorTime pour identifier de manière unique une erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-120">Used in conjunction with ErrorTime to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ba2a-121"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-121"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-122">int</span><span class="sxs-lookup"><span data-stu-id="4ba2a-122">int</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-123">ID de diagnostic du rapport d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-123">Diagnostic ID for the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ba2a-124"><strong>FromUri</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-124"><strong>FromUri</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-125">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="4ba2a-125">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-126">URI de l’utilisateur à l’origine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-126">URI of the user who originated the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ba2a-127"><strong>FromUriType</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-127"><strong>FromUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="4ba2a-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-129">Type d’URI de l’utilisateur à l’origine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-129">Type of URI of the user who originated the error.</span></span> <span data-ttu-id="4ba2a-130">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="4ba2a-130">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ba2a-131"><strong>FromTenant</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-131"><strong>FromTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="4ba2a-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-133">Client de l’utilisateur à l’origine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-133">Tenant of the user who originated the error.</span></span> <span data-ttu-id="4ba2a-134">Pour plus d’informations, voir la <a href="lync-server-2013-tenants-table.md">table locataires dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="4ba2a-134">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ba2a-135"><strong>Visite guidée</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-135"><strong>ToUri</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-136">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="4ba2a-136">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-137">URI de l’utilisateur qui a été la cible du rapport d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-137">URI of the user who was the target of the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ba2a-138"><strong>ToUriType</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-138"><strong>ToUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-139">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="4ba2a-139">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-140">Type d’URI de l’utilisateur qui a ciblé le rapport d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-140">Type of URI of the user who target of the error report.</span></span> <span data-ttu-id="4ba2a-141">Pour plus d’informations, voir la table UriTypes.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-141">See the UriTypes Table for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ba2a-142"><strong>ToTenant</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-142"><strong>ToTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-143">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="4ba2a-143">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-144">Client de l’utilisateur qui cible le rapport d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-144">Tenant of the user who target of the error report.</span></span> <span data-ttu-id="4ba2a-145">Pour plus d’informations, voir la <a href="lync-server-2013-tenants-table.md">table locataires dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="4ba2a-145">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ba2a-146"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-146"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="4ba2a-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-148">URI de la Conférence qui était la cible du rapport d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-148">URI of the conference that was the target of the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ba2a-149"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-149"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="4ba2a-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-151">Type d’URI de la Conférence qui était la cible du rapport d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-151">URI type of the conference that was the target of the error report.</span></span> <span data-ttu-id="4ba2a-152">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="4ba2a-152">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ba2a-153"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-153"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-154">DateHeure</span><span class="sxs-lookup"><span data-stu-id="4ba2a-154">datetime</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-155">Durée de la demande de session à l’origine du rapport d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-155">Time of session request that originated the error report.</span></span> <span data-ttu-id="4ba2a-156">Utilisé conjointement avec SessionIdSeq pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-156">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="4ba2a-157">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="4ba2a-157">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ba2a-158"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-158"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-159">int</span><span class="sxs-lookup"><span data-stu-id="4ba2a-159">int</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-160">Numéro d’identification identifiant la demande de session à l’origine du rapport d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-160">ID number to identify the session request that originated the error report.</span></span> <span data-ttu-id="4ba2a-161">Utilisé conjointement avec SessionIdTime pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-161">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="4ba2a-162">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="4ba2a-162">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ba2a-163"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-163"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-164">varstring (LGA775)</span><span class="sxs-lookup"><span data-stu-id="4ba2a-164">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-165">ID de boîte de dialogue SIP de session à l’origine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-165">SIP dialog ID of session that originated the error.</span></span> <span data-ttu-id="4ba2a-166">Le format est le suivant :</span><span class="sxs-lookup"><span data-stu-id="4ba2a-166">The format is:</span></span></p>
<p><span data-ttu-id="4ba2a-167">boîte de dialogue ; à partir d’une balise</span><span class="sxs-lookup"><span data-stu-id="4ba2a-167">dialog;from-tag;to-tag</span></span></p>
<p><span data-ttu-id="4ba2a-168">Vous pouvez convertir ces données en format texte à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4ba2a-168">This data can be converted to text format by using this syntax:</span></span></p>
<p><span data-ttu-id="4ba2a-169">Cast (Cast (ExternalId) en tant que varchar (max))</span><span class="sxs-lookup"><span data-stu-id="4ba2a-169">cast(cast(ExternalId as varbinary(max)) as varchar(max))</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ba2a-170"><strong>ClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-170"><strong>ClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-171">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="4ba2a-171">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-172">Version du client utilisée par l’utilisateur à l’origine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-172">Version of client used by the user who originated the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ba2a-173"><strong>TypeClient</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-173"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-174">int</span><span class="sxs-lookup"><span data-stu-id="4ba2a-174">int</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-175">Client utilisé par l’utilisateur à l’origine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-175">Client used by the user who originated the error.</span></span> <span data-ttu-id="4ba2a-176">Pour plus d’informations, voir la <a href="lync-server-2013-useragentdef-table.md">table UserAgentDef dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="4ba2a-176">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ba2a-177"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-177"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-178">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="4ba2a-178">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-179">Nom de la catégorie du client utilisée par l’utilisateur à l’origine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-179">Name of the category of the client used by the user who originated the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ba2a-180"><strong>Source</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-180"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-181">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="4ba2a-181">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-182">Nom du serveur à l’origine de l’erreur (si le rapport a été envoyé à partir d’un composant serveur).</span><span class="sxs-lookup"><span data-stu-id="4ba2a-182">Name of server that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ba2a-183"><strong>Application</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-183"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-184">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="4ba2a-184">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-185">Nom de l’application à l’origine de l’erreur (si le rapport a été envoyé à partir d’un composant serveur).</span><span class="sxs-lookup"><span data-stu-id="4ba2a-185">Name of application that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ba2a-186"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-186"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-187">int</span><span class="sxs-lookup"><span data-stu-id="4ba2a-187">int</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-188">Code de réponse SIP à la session du message SIP contenant le rapport d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-188">SIP response code to the session of the SIP message containing the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ba2a-189"><strong>RequestType</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-189"><strong>RequestType</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-190">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="4ba2a-190">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-191">Type de requête ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-191">Type of request that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ba2a-192"><strong>Indiquez</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-192"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-193">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="4ba2a-193">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-194">Type de contenu de la requête qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-194">Content type of the request that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ba2a-195"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-195"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="4ba2a-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-197">Type de session.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-197">Type of session.</span></span> <span data-ttu-id="4ba2a-198">Pour plus d’informations, voir la <a href="lync-server-2013-calltype-table.md">table CallType dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="4ba2a-198">See the <a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ba2a-199"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-199"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-200">identificateur</span><span class="sxs-lookup"><span data-stu-id="4ba2a-200">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-201">Identifiant unique permettant de corréler les informations de connexion aux différents composants participant à une conférence.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-201">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ba2a-202"><strong>SetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-202"><strong>SetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-203">int</span><span class="sxs-lookup"><span data-stu-id="4ba2a-203">int</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-204">Durée (en millisecondes) requise pour un composant spécifique pour participer à une conférence.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-204">Time (in milliseconds) required for a specific component to join a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ba2a-205"><strong>IsCapturedByServer</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-205"><strong>IsCapturedByServer</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-206">bit</span><span class="sxs-lookup"><span data-stu-id="4ba2a-206">bit</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-207">Indique si le rapport d’erreur a été capturé par l’agent CDR exécuté sur le serveur frontal ou envoyé par le client.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-207">Indicates whether the error report was captured by the CDR agent running on the Front End server, or sent by the client.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ba2a-208"><strong>Indication</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-208"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-209">type</span><span class="sxs-lookup"><span data-stu-id="4ba2a-209">smallint</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-210">Réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-210">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ba2a-211"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-211"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-212">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="4ba2a-212">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-213">Informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-213">Additional information about the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ba2a-214"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-214"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-215">nvarchar</span><span class="sxs-lookup"><span data-stu-id="4ba2a-215">nvarchar</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-216">Nom de domaine complet du serveur frontal qui a soumis le rapport.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-216">Fully qualified domain name of the Front End server that submitted the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ba2a-217"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="4ba2a-217"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="4ba2a-218">nvarchar</span><span class="sxs-lookup"><span data-stu-id="4ba2a-218">nvarchar</span></span></p></td>
<td><p><span data-ttu-id="4ba2a-219">Nom de domaine complet du pool contenant le serveur frontal qui a soumis le rapport.</span><span class="sxs-lookup"><span data-stu-id="4ba2a-219">Fully qualified domain name of the pool containing the Front End server that submitted the report.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4ba2a-220">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4ba2a-220">


</div>

<span> </span>

</div>

</div>

</span></span></div>

