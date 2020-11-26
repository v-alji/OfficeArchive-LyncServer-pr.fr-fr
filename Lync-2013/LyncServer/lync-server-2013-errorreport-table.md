---
title: 'Lync Server 2013 : Table ErrorReport'
description: 'Tableau Lync Server 2013 : ErrorReport'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorReport table
ms:assetid: ae0287b4-e8ca-4f8c-84ef-502897dcaa2a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412826(v=OCS.15)
ms:contentKeyID: 48185129
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c1cc65c396c16dc137255438f7ef7c32b2d0b78
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428516"
---
# <a name="errorreport-table-in-lync-server-2013"></a><span data-ttu-id="f9db2-103">Table ErrorReport dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9db2-103">ErrorReport table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f9db2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f9db2-104">

<span> </span></span></span>

<span data-ttu-id="f9db2-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="f9db2-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="f9db2-106">La table ErrorReport stocke des informations sur les erreurs qui se sont produites.</span><span class="sxs-lookup"><span data-stu-id="f9db2-106">The ErrorReport table stores information about errors that have occurred.</span></span> <span data-ttu-id="f9db2-107">Chaque enregistrement correspond à une occurrence d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f9db2-107">Each record is one error occurrence.</span></span> <span data-ttu-id="f9db2-108">Les erreurs sont capturées par l’agent CDR exécuté sur le serveur frontal ou envoyées par le client.</span><span class="sxs-lookup"><span data-stu-id="f9db2-108">The errors are captured either by the CDR agent running on the front-end server or sent from the client.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9db2-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="f9db2-109">Column</span></span></th>
<th><span data-ttu-id="f9db2-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="f9db2-110">Data Type</span></span></th>
<th><span data-ttu-id="f9db2-111">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="f9db2-111">Key/Index</span></span></th>
<th><span data-ttu-id="f9db2-112">Détails</span><span class="sxs-lookup"><span data-stu-id="f9db2-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9db2-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-114">DateHeure</span><span class="sxs-lookup"><span data-stu-id="f9db2-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="f9db2-115">Principal</span><span class="sxs-lookup"><span data-stu-id="f9db2-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="f9db2-116">Date et heure auxquelles l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f9db2-116">Date and time the error occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9db2-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-118">int</span><span class="sxs-lookup"><span data-stu-id="f9db2-118">int</span></span></p></td>
<td><p><span data-ttu-id="f9db2-119">Principal</span><span class="sxs-lookup"><span data-stu-id="f9db2-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="f9db2-120">Numéro d’identification pour identifier le rapport d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f9db2-120">ID number to identify the error report.</span></span> <span data-ttu-id="f9db2-121">Utilisé conjointement avec <strong>ErrorTime</strong> pour identifier de manière unique un rapport d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f9db2-121">Used in conjunction with <strong>ErrorTime</strong> to uniquely identify an error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9db2-122"><strong>ErrorId</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-122"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-123">int</span><span class="sxs-lookup"><span data-stu-id="f9db2-123">int</span></span></p></td>
<td><p><span data-ttu-id="f9db2-124">Externes</span><span class="sxs-lookup"><span data-stu-id="f9db2-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f9db2-125">ID unique du type d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f9db2-125">Unique ID of the error type.</span></span> <span data-ttu-id="f9db2-126">Pour plus d’informations, voir la <a href="lync-server-2013-errordef-table.md">table ErrorDef dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f9db2-126">See the <a href="lync-server-2013-errordef-table.md">ErrorDef table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9db2-127"><strong>FromUserId</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-127"><strong>FromUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-128">int</span><span class="sxs-lookup"><span data-stu-id="f9db2-128">int</span></span></p></td>
<td><p><span data-ttu-id="f9db2-129">Externes</span><span class="sxs-lookup"><span data-stu-id="f9db2-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f9db2-130">Utilisateur à l’origine de la demande à l’origine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="f9db2-130">User who originated the request that caused the error.</span></span> <span data-ttu-id="f9db2-131">Pour plus d’informations, consultez le <a href="lync-server-2013-users-table.md">tableau utilisateurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f9db2-131">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9db2-132"><strong>ToUserId</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-132"><strong>ToUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-133">int</span><span class="sxs-lookup"><span data-stu-id="f9db2-133">int</span></span></p></td>
<td><p><span data-ttu-id="f9db2-134">Externes</span><span class="sxs-lookup"><span data-stu-id="f9db2-134">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f9db2-135">Utilisateur de destination pour la requête à l’origine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="f9db2-135">Destination user for the request that caused the error.</span></span> <span data-ttu-id="f9db2-136">Pour plus d’informations, consultez le <a href="lync-server-2013-users-table.md">tableau utilisateurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f9db2-136">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9db2-137"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-137"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-138">int</span><span class="sxs-lookup"><span data-stu-id="f9db2-138">int</span></span></p></td>
<td><p><span data-ttu-id="f9db2-139">Externes</span><span class="sxs-lookup"><span data-stu-id="f9db2-139">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f9db2-140">URI de la conférence liée à l’erreur.</span><span class="sxs-lookup"><span data-stu-id="f9db2-140">Conference URI related to the error.</span></span> <span data-ttu-id="f9db2-141">Pour plus d’informations, voir la <a href="lync-server-2013-conferenceuris-table.md">table ConferenceUris dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f9db2-141">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="f9db2-142">En règle générale, si ConferenceUriId n’est pas null, FromUserId ou ToUserId seront NULL.</span><span class="sxs-lookup"><span data-stu-id="f9db2-142">Typically, if ConferenceUriId is not null, then either FromUserId or ToUserId will be null.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9db2-143"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-143"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-144">DateHeure</span><span class="sxs-lookup"><span data-stu-id="f9db2-144">datetime</span></span></p></td>
<td><p><span data-ttu-id="f9db2-145">Externes</span><span class="sxs-lookup"><span data-stu-id="f9db2-145">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f9db2-146">Utilisé conjointement avec <strong>SessionIdSeq</strong> pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="f9db2-146">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="f9db2-147">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f9db2-147">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9db2-148"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-148"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-149">int</span><span class="sxs-lookup"><span data-stu-id="f9db2-149">int</span></span></p></td>
<td><p><span data-ttu-id="f9db2-150">Externes</span><span class="sxs-lookup"><span data-stu-id="f9db2-150">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f9db2-151">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="f9db2-151">ID number to identify the session.</span></span> <span data-ttu-id="f9db2-152">Utilisé conjointement avec <strong>SessionIdTime</strong> pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="f9db2-152">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="f9db2-153">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f9db2-153">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9db2-154"><strong>SourceId</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-154"><strong>SourceId</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-155">int</span><span class="sxs-lookup"><span data-stu-id="f9db2-155">int</span></span></p></td>
<td><p><span data-ttu-id="f9db2-156">Externes</span><span class="sxs-lookup"><span data-stu-id="f9db2-156">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f9db2-157">Serveur ayant envoyé le rapport d’erreur (si le rapport est envoyé à partir d’un composant serveur).</span><span class="sxs-lookup"><span data-stu-id="f9db2-157">Server that sent the error report (if the report is being sent from a server component).</span></span> <span data-ttu-id="f9db2-158">Pour plus d’informations, voir le <a href="lync-server-2013-servers-table.md">tableau des serveurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f9db2-158">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="f9db2-159">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f9db2-159">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9db2-160"><strong>ApplicationId</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-160"><strong>ApplicationId</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-161">int</span><span class="sxs-lookup"><span data-stu-id="f9db2-161">int</span></span></p></td>
<td><p><span data-ttu-id="f9db2-162">Externes</span><span class="sxs-lookup"><span data-stu-id="f9db2-162">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f9db2-163">Serveur ayant envoyé le rapport d’erreur (si le rapport est envoyé à partir d’un composant serveur).</span><span class="sxs-lookup"><span data-stu-id="f9db2-163">Server that sent the error report (if the report is being sent from a server component).</span></span> <span data-ttu-id="f9db2-164">Pour plus d’informations, consultez le <a href="lync-server-2013-application-table.md">tableau de l’application dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f9db2-164">See the <a href="lync-server-2013-application-table.md">Application table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="f9db2-165">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f9db2-165">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9db2-166"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-166"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-167">image</span><span class="sxs-lookup"><span data-stu-id="f9db2-167">image</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f9db2-168">Plus d’informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="f9db2-168">More information about the error.</span></span></p>
<p><span data-ttu-id="f9db2-169">Vous pouvez convertir ces données en format texte à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="f9db2-169">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(Detail as varbinary(max)) as varchar(max)) </code></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9db2-170"><strong>ClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-170"><strong>ClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-171">int</span><span class="sxs-lookup"><span data-stu-id="f9db2-171">int</span></span></p></td>
<td><p><span data-ttu-id="f9db2-172">Externes</span><span class="sxs-lookup"><span data-stu-id="f9db2-172">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f9db2-173">Version du client de point de terminaison qui envoie le rapport d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f9db2-173">The client version of endpoint that sends the error report.</span></span> <span data-ttu-id="f9db2-174">Pour plus d’informations, voir la <a href="lync-server-2013-clientversions-table.md">table ClientVersions dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f9db2-174">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9db2-175"><strong>IsCapturedByServer</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-175"><strong>IsCapturedByServer</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-176">bit</span><span class="sxs-lookup"><span data-stu-id="f9db2-176">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f9db2-177">Est le rapport d’erreur capturé par l’agent CDR exécuté sur le serveur frontal ou envoyé par le client.</span><span class="sxs-lookup"><span data-stu-id="f9db2-177">Is the error report captured by the CDR agent running on the front-end server, or sent by the client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9db2-178"><strong>Indication</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-178"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-179">type</span><span class="sxs-lookup"><span data-stu-id="f9db2-179">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f9db2-180">Réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f9db2-180">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9db2-181"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-181"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-182">Identificateur</span><span class="sxs-lookup"><span data-stu-id="f9db2-182">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f9db2-183">Identifiant unique permettant de corréler les informations de connexion aux différents composants participant à une conférence.</span><span class="sxs-lookup"><span data-stu-id="f9db2-183">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p>
<p><span data-ttu-id="f9db2-184">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f9db2-184">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9db2-185"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-185"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-186">int</span><span class="sxs-lookup"><span data-stu-id="f9db2-186">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f9db2-187">Durée (en millisecondes) requise pour un composant spécifique pour participer à une conférence.</span><span class="sxs-lookup"><span data-stu-id="f9db2-187">Time (in milliseconds) required for a specific component to join a conference.</span></span></p>
<p><span data-ttu-id="f9db2-188">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f9db2-188">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9db2-189"><strong>ServerId</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-189"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-190">int</span><span class="sxs-lookup"><span data-stu-id="f9db2-190">int</span></span></p></td>
<td><p><span data-ttu-id="f9db2-191">Externes</span><span class="sxs-lookup"><span data-stu-id="f9db2-191">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f9db2-192">Représente le nom de domaine complet du serveur qui a généré le rapport d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f9db2-192">Represents the fully qualified domain name of the server that generated the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9db2-193"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="f9db2-193"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="f9db2-194">int</span><span class="sxs-lookup"><span data-stu-id="f9db2-194">int</span></span></p></td>
<td><p><span data-ttu-id="f9db2-195">Externes</span><span class="sxs-lookup"><span data-stu-id="f9db2-195">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f9db2-196">Représente le nom de domaine complet du pool dans lequel le rapport d’erreur a été généré.</span><span class="sxs-lookup"><span data-stu-id="f9db2-196">Represents the fully qualified domain name of the pool where the error report was generated.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f9db2-197">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f9db2-197">


</div>

<span> </span>

</div>

</div>

</span></span></div>

