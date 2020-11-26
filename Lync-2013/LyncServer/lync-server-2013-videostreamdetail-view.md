---
title: 'Affichage Lync Server 2013 : VideoStreamDetail'
description: 'Affichage Lync Server 2013 : VideoStreamDetail'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoStreamDetail view
ms:assetid: ec8c45e1-307d-40ec-a75e-6083306105f2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721928(v=OCS.15)
ms:contentKeyID: 49733863
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3f420c292627d15fd0d54f2eba01c565a49a72d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443425"
---
# <a name="videostreamdetail-view-in-lync-server-2013"></a><span data-ttu-id="7cb41-103">Affichage VideoStreamDetail dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7cb41-103">VideoStreamDetail view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7cb41-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7cb41-104">

<span> </span></span></span>

<span data-ttu-id="7cb41-105">_**Dernière modification de la rubrique :** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="7cb41-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="7cb41-106">Le mode VideoStreamDetail stocke les informations relatives à chaque flux vidéo dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="7cb41-106">The VideoStreamDetail View stores information about each video stream in the database.</span></span> <span data-ttu-id="7cb41-107">Cet affichage a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7cb41-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cb41-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="7cb41-108">Column</span></span></th>
<th><span data-ttu-id="7cb41-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="7cb41-109">Data Type</span></span></th>
<th><span data-ttu-id="7cb41-110">Description</span><span class="sxs-lookup"><span data-stu-id="7cb41-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-111">SessionTime</span><span class="sxs-lookup"><span data-stu-id="7cb41-111">SessionTime</span></span></p></td>
<td><p><span data-ttu-id="7cb41-112">DateHeure</span><span class="sxs-lookup"><span data-stu-id="7cb41-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="7cb41-113">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="7cb41-113">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-114">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="7cb41-114">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="7cb41-115">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-115">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-116">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="7cb41-116">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-117">MediaLineLabel</span><span class="sxs-lookup"><span data-stu-id="7cb41-117">MediaLineLabel</span></span></p></td>
<td><p><span data-ttu-id="7cb41-118">tinyint</span><span class="sxs-lookup"><span data-stu-id="7cb41-118">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7cb41-119">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="7cb41-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-120">StreamId</span><span class="sxs-lookup"><span data-stu-id="7cb41-120">StreamId</span></span></p></td>
<td><p><span data-ttu-id="7cb41-121">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-121">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-122">IDENTIFIant unique dans une ligne de médias.</span><span class="sxs-lookup"><span data-stu-id="7cb41-122">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-123">StartTime</span><span class="sxs-lookup"><span data-stu-id="7cb41-123">StartTime</span></span></p></td>
<td><p><span data-ttu-id="7cb41-124">DateHeure</span><span class="sxs-lookup"><span data-stu-id="7cb41-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="7cb41-125">Heure de début de la session.</span><span class="sxs-lookup"><span data-stu-id="7cb41-125">Start time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-126">EndTime</span><span class="sxs-lookup"><span data-stu-id="7cb41-126">EndTime</span></span></p></td>
<td><p><span data-ttu-id="7cb41-127">DateHeure</span><span class="sxs-lookup"><span data-stu-id="7cb41-127">datetime</span></span></p></td>
<td><p><span data-ttu-id="7cb41-128">Heure de fin de la session.</span><span class="sxs-lookup"><span data-stu-id="7cb41-128">End time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-129">CallPriority</span><span class="sxs-lookup"><span data-stu-id="7cb41-129">CallPriority</span></span></p></td>
<td><p><span data-ttu-id="7cb41-130">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-130">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-131">Priorité de l’appel.</span><span class="sxs-lookup"><span data-stu-id="7cb41-131">Priority of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-132">CallerPool</span><span class="sxs-lookup"><span data-stu-id="7cb41-132">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="7cb41-133">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7cb41-133">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-134">Nom de domaine complet du pool d’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-134">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-135">CalleePool</span><span class="sxs-lookup"><span data-stu-id="7cb41-135">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="7cb41-136">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7cb41-136">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-137">Nom de domaine complet (FQDN) du pool d’appel.</span><span class="sxs-lookup"><span data-stu-id="7cb41-137">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-138">Appelant</span><span class="sxs-lookup"><span data-stu-id="7cb41-138">Caller</span></span></p></td>
<td><p><span data-ttu-id="7cb41-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="7cb41-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-140">URI de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-140">Caller’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-141">Appelé</span><span class="sxs-lookup"><span data-stu-id="7cb41-141">Callee</span></span></p></td>
<td><p><span data-ttu-id="7cb41-142">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="7cb41-142">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-143">URI de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-143">Callee’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-144">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="7cb41-144">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="7cb41-145">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7cb41-145">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-146">Chaîne de l’agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-146">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-147">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="7cb41-147">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="7cb41-148">type</span><span class="sxs-lookup"><span data-stu-id="7cb41-148">smallint</span></span></p></td>
<td><p><span data-ttu-id="7cb41-149">Type de l’agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-149">Type of caller’s user agent.</span></span> <span data-ttu-id="7cb41-150">Pour plus d’informations, voir la <a href="lync-server-2013-useragent-table.md">table UserAgent dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7cb41-150">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-151">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="7cb41-151">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="7cb41-152">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="7cb41-152">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-153">Catégorie de l’agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-153">Category of caller’s user agent.</span></span> <span data-ttu-id="7cb41-154">Pour plus d’informations, reportez-vous <a href="lync-server-2013-useragentdef-table-qoe.md">à la table UserAgentDef (QoE) dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7cb41-154">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-155">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="7cb41-155">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="7cb41-156">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7cb41-156">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-157">Chaîne de l’agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-157">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-158">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="7cb41-158">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="7cb41-159">type</span><span class="sxs-lookup"><span data-stu-id="7cb41-159">smallint</span></span></p></td>
<td><p><span data-ttu-id="7cb41-160">Type de l’agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-160">Type of callee’s user agent.</span></span> <span data-ttu-id="7cb41-161">Pour plus d’informations, voir la <a href="lync-server-2013-useragent-table.md">table UserAgent dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7cb41-161">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-162">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="7cb41-162">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="7cb41-163">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="7cb41-163">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-164">Catégorie de l’agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-164">Category of callee’s user agent.</span></span> <span data-ttu-id="7cb41-165">Pour plus d’informations, reportez-vous <a href="lync-server-2013-useragentdef-table-qoe.md">à la table UserAgentDef (QoE) dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7cb41-165">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-166">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cb41-166">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="7cb41-167">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7cb41-167">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-168">Nom du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-168">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-169">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cb41-169">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="7cb41-170">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7cb41-170">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-171">Nom du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-171">Callee’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-172">Appelant</span><span class="sxs-lookup"><span data-stu-id="7cb41-172">CallerOS</span></span></p></td>
<td><p><span data-ttu-id="7cb41-173">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="7cb41-173">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-174">Système d’exploitation (se) du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-174">Operating system (OS) of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-175">CalleeOS</span><span class="sxs-lookup"><span data-stu-id="7cb41-175">CalleeOS</span></span></p></td>
<td><p><span data-ttu-id="7cb41-176">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="7cb41-176">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-177">Système d’exploitation (se) du point de terminaison de l’appelé.</span><span class="sxs-lookup"><span data-stu-id="7cb41-177">Operating system (OS) of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-178">CallerCPUName</span><span class="sxs-lookup"><span data-stu-id="7cb41-178">CallerCPUName</span></span></p></td>
<td><p><span data-ttu-id="7cb41-179">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="7cb41-179">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-180">Nom de l’UC du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-180">CPU name of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-181">CalleeCPUName</span><span class="sxs-lookup"><span data-stu-id="7cb41-181">CalleeCPUName</span></span></p></td>
<td><p><span data-ttu-id="7cb41-182">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="7cb41-182">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-183">Nom de l’UC du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-183">CPU name of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-184">CallerCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="7cb41-184">CallerCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="7cb41-185">type</span><span class="sxs-lookup"><span data-stu-id="7cb41-185">smallint</span></span></p></td>
<td><p><span data-ttu-id="7cb41-186">Nombre de cœurs d’UC du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-186">Number of CPU cores of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-187">CalleeCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="7cb41-187">CalleeCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="7cb41-188">type</span><span class="sxs-lookup"><span data-stu-id="7cb41-188">smallint</span></span></p></td>
<td><p><span data-ttu-id="7cb41-189">Nombre de cœurs d’UC du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-189">Number of CPU cores of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-190">CallerCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="7cb41-190">CallerCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="7cb41-191">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-191">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-192">Vitesse de processeur de l’UC du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-192">CPU processor speed of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-193">CalleeCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="7cb41-193">CalleeCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="7cb41-194">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-194">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-195">Vitesse de processeur de l’UC du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-195">CPU processor speed of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-196">CallerVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="7cb41-196">CallerVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="7cb41-197">tinyint</span><span class="sxs-lookup"><span data-stu-id="7cb41-197">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7cb41-198">Indique si le système de l’appelant s’exécute dans un environnement virtualisé.</span><span class="sxs-lookup"><span data-stu-id="7cb41-198">Indicates whether the caller’s system is running in a virtualized environment.</span></span> <span data-ttu-id="7cb41-199">Pour plus d’informations, voir la <a href="lync-server-2013-endpoint-table.md">table Endpoint dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7cb41-199">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-200">CalleeVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="7cb41-200">CalleeVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="7cb41-201">tinyint</span><span class="sxs-lookup"><span data-stu-id="7cb41-201">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7cb41-202">Indique si le système de l’appelant s’exécute dans un environnement virtualisé.</span><span class="sxs-lookup"><span data-stu-id="7cb41-202">Indicates whether the callee’s system is running in a virtualized environment.</span></span> <span data-ttu-id="7cb41-203">Pour plus d’informations, voir la <a href="lync-server-2013-endpoint-table.md">table Endpoint dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7cb41-203">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-204">ConnectivityIce</span><span class="sxs-lookup"><span data-stu-id="7cb41-204">ConnectivityIce</span></span></p></td>
<td><p><span data-ttu-id="7cb41-205">tinyint</span><span class="sxs-lookup"><span data-stu-id="7cb41-205">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7cb41-206">Des informations sur le chemin multimédia, par exemple direct ou relayé.</span><span class="sxs-lookup"><span data-stu-id="7cb41-206">Information about media path, such as direct or relayed.</span></span> <span data-ttu-id="7cb41-207">Pour plus d’informations, voir la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7cb41-207">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-208">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="7cb41-208">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="7cb41-209">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-209">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-210">Informations sur le processus de création d’une connexion interactive (ICE) décrite dans les indicateurs bits pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-210">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="7cb41-211">Pour plus d’informations, reportez-vous à la spécification relative au protocole serveur pour le contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="7cb41-211">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-212">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="7cb41-212">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="7cb41-213">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-213">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-214">Informations sur le processus de création d’une connexion interactive (ICE) décrite dans les indicateurs bits pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-214">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="7cb41-215">Pour plus d’informations, reportez-vous à la spécification relative au protocole serveur pour le contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="7cb41-215">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-216">Transport</span><span class="sxs-lookup"><span data-stu-id="7cb41-216">Transport</span></span></p></td>
<td><p><span data-ttu-id="7cb41-217">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-217">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-218">Le type de transport : 0 correspond au protocole UDP ; 1 est le protocole TCP.</span><span class="sxs-lookup"><span data-stu-id="7cb41-218">Transport type: 0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-219">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="7cb41-219">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="7cb41-220">var (50)</span><span class="sxs-lookup"><span data-stu-id="7cb41-220">var(50)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-221">Adresse IP de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-221">IP address of the caller.</span></span> <span data-ttu-id="7cb41-222">Il peut s’agir d’une adresse IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="7cb41-222">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-223">CallerPort</span><span class="sxs-lookup"><span data-stu-id="7cb41-223">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="7cb41-224">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-224">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-225">Port utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-225">Port used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-226">CallerInside</span><span class="sxs-lookup"><span data-stu-id="7cb41-226">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="7cb41-227">bit</span><span class="sxs-lookup"><span data-stu-id="7cb41-227">bit</span></span></p></td>
<td><p><span data-ttu-id="7cb41-228">Indique si l’appelant se trouve au sein du réseau de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="7cb41-228">Indicates whether the caller is inside the organization network.</span></span> <span data-ttu-id="7cb41-229">1 désigne l’appelant à l’intérieur du réseau d’entreprise, 0 indique que l’appelant se trouve hors du réseau.</span><span class="sxs-lookup"><span data-stu-id="7cb41-229">1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-230">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="7cb41-230">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="7cb41-231">var (50)</span><span class="sxs-lookup"><span data-stu-id="7cb41-231">var(50)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-232">Adresse IP de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-232">IP address of the callee.</span></span> <span data-ttu-id="7cb41-233">Il peut s’agir d’une adresse IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="7cb41-233">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-234">CalleePort</span><span class="sxs-lookup"><span data-stu-id="7cb41-234">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="7cb41-235">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-235">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-236">Port utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-236">Port used by the callee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-237">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="7cb41-237">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="7cb41-238">bit</span><span class="sxs-lookup"><span data-stu-id="7cb41-238">bit</span></span></p></td>
<td><p><span data-ttu-id="7cb41-239">Indique si l’appelant se trouve à l’intérieur du réseau de l’organisation. 1 signifie que l’appelant se trouve à l’intérieur du réseau d’entreprise, 0 indique que l’appel se trouve hors du réseau.</span><span class="sxs-lookup"><span data-stu-id="7cb41-239">Indicates whether the caller is inside the organization network.1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-240">CallerUserSite</span><span class="sxs-lookup"><span data-stu-id="7cb41-240">CallerUserSite</span></span></p></td>
<td><p><span data-ttu-id="7cb41-241">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="7cb41-241">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-242">Nom du site de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-242">Name of the caller’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-243">CallerRegion</span><span class="sxs-lookup"><span data-stu-id="7cb41-243">CallerRegion</span></span></p></td>
<td><p><span data-ttu-id="7cb41-244">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="7cb41-244">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-245">Nom du pays/de la région du site de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-245">Name of the country/region of the caller’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-246">CalleeUserSite</span><span class="sxs-lookup"><span data-stu-id="7cb41-246">CalleeUserSite</span></span></p></td>
<td><p><span data-ttu-id="7cb41-247">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="7cb41-247">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-248">Nom du site du ou des appelants.</span><span class="sxs-lookup"><span data-stu-id="7cb41-248">Name of the callee’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-249">CalleeRegion</span><span class="sxs-lookup"><span data-stu-id="7cb41-249">CalleeRegion</span></span></p></td>
<td><p><span data-ttu-id="7cb41-250">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="7cb41-250">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-251">Nom du pays/de la région du site de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-251">Name of the country/region of the callee’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-252">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="7cb41-252">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="7cb41-253">var (50)</span><span class="sxs-lookup"><span data-stu-id="7cb41-253">var(50)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-254">Adresse IP du service Edge A/V utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-254">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="7cb41-255">Pour plus d’informations, consultez la <a href="lync-server-2013-ipaddress-table.md">table IPAddress dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7cb41-255">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-256">CallerRelayPort</span><span class="sxs-lookup"><span data-stu-id="7cb41-256">CallerRelayPort</span></span></p></td>
<td><p><span data-ttu-id="7cb41-257">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-257">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-258">Port sur le service Edge A/V utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-258">Port on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-259">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="7cb41-259">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="7cb41-260">var (50)</span><span class="sxs-lookup"><span data-stu-id="7cb41-260">var(50)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-261">Clé d’adresse IP du service Edge A/V utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-261">IP Address key of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="7cb41-262">Pour plus d’informations, consultez la <a href="lync-server-2013-ipaddress-table.md">table IPAddress dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="7cb41-262">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-263">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="7cb41-263">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="7cb41-264">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-264">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-265">Port sur le service Edge A/V utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-265">Port on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-266">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="7cb41-266">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="7cb41-267">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="7cb41-267">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-268">Nom de l’appareil de capture de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-268">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-269">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="7cb41-269">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="7cb41-270">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="7cb41-270">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-271">Nom de l’appareil de rendu de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-271">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-272">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="7cb41-272">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="7cb41-273">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="7cb41-273">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-274">Nom du pilote de périphérique de capture de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-274">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-275">CallerRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="7cb41-275">CallerRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="7cb41-276">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="7cb41-276">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-277">Nom du pilote de périphérique de rendu de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-277">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-278">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="7cb41-278">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="7cb41-279">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="7cb41-279">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-280">Nom de l’appareil de capture du destinataire.</span><span class="sxs-lookup"><span data-stu-id="7cb41-280">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-281">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="7cb41-281">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="7cb41-282">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="7cb41-282">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-283">Nom de l’appareil de rendu de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-283">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-284">CalleCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="7cb41-284">CalleCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="7cb41-285">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="7cb41-285">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-286">Nom du pilote de l’appareil de capture du appelé.</span><span class="sxs-lookup"><span data-stu-id="7cb41-286">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-287">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="7cb41-287">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="7cb41-288">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="7cb41-288">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-289">Nom du pilote du périphérique de rendu de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-289">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-290">CallerNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="7cb41-290">CallerNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="7cb41-291">tinyint</span><span class="sxs-lookup"><span data-stu-id="7cb41-291">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7cb41-292">Type de connexion réseau de l’appelant : 0 est filaire, 1 est un réseau sans fil.</span><span class="sxs-lookup"><span data-stu-id="7cb41-292">Caller’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-293">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="7cb41-293">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="7cb41-294">bit</span><span class="sxs-lookup"><span data-stu-id="7cb41-294">bit</span></span></p></td>
<td><p><span data-ttu-id="7cb41-295">Indique si l’appelant s’est connecté via un réseau privé virtuel.</span><span class="sxs-lookup"><span data-stu-id="7cb41-295">Indicates whether or not the caller connected over a virtual private network.</span></span> <span data-ttu-id="7cb41-296">1 est un réseau privé virtuel (VPN), 0 est non VPN.</span><span class="sxs-lookup"><span data-stu-id="7cb41-296">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-297">CallerLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="7cb41-297">CallerLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="7cb41-298">décimale (18)</span><span class="sxs-lookup"><span data-stu-id="7cb41-298">decimal(18,)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-299">Vitesse de liaison réseau pour le point de terminaison de l’appelant en bps.</span><span class="sxs-lookup"><span data-stu-id="7cb41-299">Network link speed for the caller's endpoint in bps.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-300">CalleeNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="7cb41-300">CalleeNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="7cb41-301">tinyint</span><span class="sxs-lookup"><span data-stu-id="7cb41-301">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7cb41-302">Type de connexion réseau du ou du destinataire : 0 est filaire, 1 est un téléphone sans fil.</span><span class="sxs-lookup"><span data-stu-id="7cb41-302">Callee’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-303">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="7cb41-303">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="7cb41-304">bit</span><span class="sxs-lookup"><span data-stu-id="7cb41-304">bit</span></span></p></td>
<td><p><span data-ttu-id="7cb41-305">Indique si l’appelant est connecté via un réseau privé virtuel.</span><span class="sxs-lookup"><span data-stu-id="7cb41-305">Indicates whether or not the callee connected over a virtual private network.</span></span> <span data-ttu-id="7cb41-306">1 est un réseau privé virtuel (VPN), 0 est non VPN.</span><span class="sxs-lookup"><span data-stu-id="7cb41-306">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-307">CalleeLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="7cb41-307">CalleeLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="7cb41-308">décimale (18, 0)</span><span class="sxs-lookup"><span data-stu-id="7cb41-308">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-309">Vitesse de liaison réseau pour le point de terminaison de l’appelant (en BPS).</span><span class="sxs-lookup"><span data-stu-id="7cb41-309">Network link speed for the callee’s endpoint (in bps).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-310">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="7cb41-310">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="7cb41-311">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="7cb41-311">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-312">La fonction de conversation à bande étroite des sessions audio (en fonction des deux flux audio).</span><span class="sxs-lookup"><span data-stu-id="7cb41-312">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-313">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="7cb41-313">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="7cb41-314">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-314">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-315">Bande passante réelle appliquée au flux d’envoi indiqué en fonction de différents paramètres de stratégie (TURN, API, SDP, serveur de stratégie, etc.).</span><span class="sxs-lookup"><span data-stu-id="7cb41-315">Actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="7cb41-316">Ce problème ne doit pas être confondu avec la bande passante effective, car il peut y avoir une bande passante effective plus faible en fonction de l’estimation de bande passante.</span><span class="sxs-lookup"><span data-stu-id="7cb41-316">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="7cb41-317">Il s’agit essentiellement de la bande passante maximale que le flux d’envoi peut prendre en limitation par l’estimation de bande passante.</span><span class="sxs-lookup"><span data-stu-id="7cb41-317">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-318">JitterInterArrival</span><span class="sxs-lookup"><span data-stu-id="7cb41-318">JitterInterArrival</span></span></p></td>
<td><p><span data-ttu-id="7cb41-319">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-319">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-320">Gigue réseau moyenne des statistiques de protocole RTCP (Real Time Control Protocol).</span><span class="sxs-lookup"><span data-stu-id="7cb41-320">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-321">JitterInterArrivalMax</span><span class="sxs-lookup"><span data-stu-id="7cb41-321">JitterInterArrivalMax</span></span></p></td>
<td><p><span data-ttu-id="7cb41-322">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-322">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-323">Scintillement du réseau maximum lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="7cb41-323">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-324">RoundTrip</span><span class="sxs-lookup"><span data-stu-id="7cb41-324">RoundTrip</span></span></p></td>
<td><p><span data-ttu-id="7cb41-325">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-325">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-326">Durée de l’aller-retour des statistiques RTCP.</span><span class="sxs-lookup"><span data-stu-id="7cb41-326">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-327">RoundTripMax</span><span class="sxs-lookup"><span data-stu-id="7cb41-327">RoundTripMax</span></span></p></td>
<td><p><span data-ttu-id="7cb41-328">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-328">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-329">Durée de l’aller-retour maximal pour le flux audio.</span><span class="sxs-lookup"><span data-stu-id="7cb41-329">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-330">PacketLossRate</span><span class="sxs-lookup"><span data-stu-id="7cb41-330">PacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="7cb41-331">décimale (5 ; 4)</span><span class="sxs-lookup"><span data-stu-id="7cb41-331">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-332">Taux moyen de perte de paquets lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="7cb41-332">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-333">PacketLossRateMax</span><span class="sxs-lookup"><span data-stu-id="7cb41-333">PacketLossRateMax</span></span></p></td>
<td><p><span data-ttu-id="7cb41-334">décimale (5 ; 4)</span><span class="sxs-lookup"><span data-stu-id="7cb41-334">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-335">Perte de paquets maximum observée pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="7cb41-335">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-336">PacketUtilization</span><span class="sxs-lookup"><span data-stu-id="7cb41-336">PacketUtilization</span></span></p></td>
<td><p><span data-ttu-id="7cb41-337">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-337">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-338">Nombre de paquets pour le flux vidéo (Real Time Transport Protocol, RTP).</span><span class="sxs-lookup"><span data-stu-id="7cb41-338">Packet count for the video stream (Real Time Transport Protocol, RTP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-339">Bande passante</span><span class="sxs-lookup"><span data-stu-id="7cb41-339">BandwidthEst</span></span></p></td>
<td><p><span data-ttu-id="7cb41-340">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-340">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-341">Estimations de bande passante pour le flux audio.</span><span class="sxs-lookup"><span data-stu-id="7cb41-341">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-342">PayloadDescription</span><span class="sxs-lookup"><span data-stu-id="7cb41-342">PayloadDescription</span></span></p></td>
<td><p><span data-ttu-id="7cb41-343">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-343">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-344">Codec audio utilisé pour l’appel, référencé à partir de la <a href="lync-server-2013-payloaddescription-table.md">table PayloadDescription dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="7cb41-344">Audio codec used for the call, referenced from the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-345">VideoResolution</span><span class="sxs-lookup"><span data-stu-id="7cb41-345">VideoResolution</span></span></p></td>
<td><p><span data-ttu-id="7cb41-346">car (9)</span><span class="sxs-lookup"><span data-stu-id="7cb41-346">char(9)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-347">Résolution de la vidéo, en pixels, de largeur multipliée par la hauteur en pixels.</span><span class="sxs-lookup"><span data-stu-id="7cb41-347">Resolution of the video in pixels width multiplied by pixels height.</span></span> <span data-ttu-id="7cb41-348">Signalée en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="7cb41-348">Reported as a string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-349">VideoBitRateAvg</span><span class="sxs-lookup"><span data-stu-id="7cb41-349">VideoBitRateAvg</span></span></p></td>
<td><p><span data-ttu-id="7cb41-350">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-350">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-351">Vitesse de transmission moyenne du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="7cb41-351">Average bit rate of the video stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-352">InboundVideoFrameRateAvg</span><span class="sxs-lookup"><span data-stu-id="7cb41-352">InboundVideoFrameRateAvg</span></span></p></td>
<td><p><span data-ttu-id="7cb41-353">décimale (9 ; 4)</span><span class="sxs-lookup"><span data-stu-id="7cb41-353">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-354">Fréquence d’images de la vidéo reçue.</span><span class="sxs-lookup"><span data-stu-id="7cb41-354">Frame rate of video received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-355">OutboundVideoFrameRateAvg</span><span class="sxs-lookup"><span data-stu-id="7cb41-355">OutboundVideoFrameRateAvg</span></span></p></td>
<td><p><span data-ttu-id="7cb41-356">décimale (9 ; 4)</span><span class="sxs-lookup"><span data-stu-id="7cb41-356">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-357">Fréquence d’images de la vidéo envoyée.</span><span class="sxs-lookup"><span data-stu-id="7cb41-357">Frame rate of video sent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-358">ViideoBitRateMax</span><span class="sxs-lookup"><span data-stu-id="7cb41-358">ViideoBitRateMax</span></span></p></td>
<td><p><span data-ttu-id="7cb41-359">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-359">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-360">Débit vidéo maximum lors de la session vidéo.</span><span class="sxs-lookup"><span data-stu-id="7cb41-360">Maximum video bit rate during the video session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-361">Cause du taux</span><span class="sxs-lookup"><span data-stu-id="7cb41-361">VideoPacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="7cb41-362">décimale (9 ; 4)</span><span class="sxs-lookup"><span data-stu-id="7cb41-362">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-363">Taux d’interruption des paquets vidéo.</span><span class="sxs-lookup"><span data-stu-id="7cb41-363">Rate at which video packets were lost.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-364">VideoFrameLossRate</span><span class="sxs-lookup"><span data-stu-id="7cb41-364">VideoFrameLossRate</span></span></p></td>
<td><p><span data-ttu-id="7cb41-365">décimale (9.4)</span><span class="sxs-lookup"><span data-stu-id="7cb41-365">decimal(9.4)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-366">Pourcentage du nombre total de trames vidéo perdues.</span><span class="sxs-lookup"><span data-stu-id="7cb41-366">Percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-367">VideoFEC</span><span class="sxs-lookup"><span data-stu-id="7cb41-367">VideoFEC</span></span></p></td>
<td><p><span data-ttu-id="7cb41-368">bit</span><span class="sxs-lookup"><span data-stu-id="7cb41-368">bit</span></span></p></td>
<td><p><span data-ttu-id="7cb41-369">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="7cb41-369">Not used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-370">VideoAllocateBWAvg</span><span class="sxs-lookup"><span data-stu-id="7cb41-370">VideoAllocateBWAvg</span></span></p></td>
<td><p><span data-ttu-id="7cb41-371">int</span><span class="sxs-lookup"><span data-stu-id="7cb41-371">int</span></span></p></td>
<td><p><span data-ttu-id="7cb41-372">Quantité moyenne de bande passante allouée pour la vidéo.</span><span class="sxs-lookup"><span data-stu-id="7cb41-372">Average amount of bandwidth allocated for video.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb41-373">VideoLocalFrameLossPercentageAvg</span><span class="sxs-lookup"><span data-stu-id="7cb41-373">VideoLocalFrameLossPercentageAvg</span></span></p></td>
<td><p><span data-ttu-id="7cb41-374">décimale (9.4)</span><span class="sxs-lookup"><span data-stu-id="7cb41-374">decimal(9.4)</span></span></p></td>
<td><p><span data-ttu-id="7cb41-375">Pourcentage du nombre total de trames vidéo perdues.</span><span class="sxs-lookup"><span data-stu-id="7cb41-375">Percentage of total video frames that were lost.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb41-376">SenderIsCallerPAI</span><span class="sxs-lookup"><span data-stu-id="7cb41-376">SenderIsCallerPAI</span></span></p></td>
<td><p><span data-ttu-id="7cb41-377">bit</span><span class="sxs-lookup"><span data-stu-id="7cb41-377">bit</span></span></p></td>
<td><p><span data-ttu-id="7cb41-378">Direction du flux pour les informations d’identité affirmées p.</span><span class="sxs-lookup"><span data-stu-id="7cb41-378">Stream direction for p-asserted identity information.</span></span> <span data-ttu-id="7cb41-379">1 signifie que le sens du flux provient de l’appelant vers l’appelant ; 0 : le sens du flux provient de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7cb41-379">1 means the stream direction is from the caller to the callee; 0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7cb41-380">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7cb41-380">


</div>

<span> </span>

</div>

</div>

</span></span></div>

