---
title: 'Affichage Lync Server 2013 : AudioStreamDetail'
description: 'Affichage Lync Server 2013 : AudioStreamDetail'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioStreamDetail view
ms:assetid: b6a435b3-103c-41c4-96ed-33c3784534c0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721859(v=OCS.15)
ms:contentKeyID: 49733792
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92c4c9bbb4f126e242e28d835222f6ba2af89d8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438161"
---
# <a name="audiostreamdetail-view-in-lync-server-2013"></a><span data-ttu-id="790ec-103">Affichage AudioStreamDetail dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="790ec-103">AudioStreamDetail view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="790ec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="790ec-104">

<span> </span></span></span>

<span data-ttu-id="790ec-105">_**Dernière modification de la rubrique :** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="790ec-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="790ec-106">Le mode AudioStreamDetail stocke les informations relatives à chaque flux audio dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="790ec-106">The AudioStreamDetail View stores information about each audio stream in the database.</span></span> <span data-ttu-id="790ec-107">Cet affichage a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="790ec-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="790ec-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="790ec-108">Column</span></span></th>
<th><span data-ttu-id="790ec-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="790ec-109">Data Type</span></span></th>
<th><span data-ttu-id="790ec-110">Détails</span><span class="sxs-lookup"><span data-stu-id="790ec-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="790ec-111">SessionTime</span><span class="sxs-lookup"><span data-stu-id="790ec-111">SessionTime</span></span></p></td>
<td><p><span data-ttu-id="790ec-112">DateHeure</span><span class="sxs-lookup"><span data-stu-id="790ec-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="790ec-113">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="790ec-113">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-114">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="790ec-114">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="790ec-115">int</span><span class="sxs-lookup"><span data-stu-id="790ec-115">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-116">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="790ec-116">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-117">StreamId</span><span class="sxs-lookup"><span data-stu-id="790ec-117">StreamId</span></span></p></td>
<td><p><span data-ttu-id="790ec-118">int</span><span class="sxs-lookup"><span data-stu-id="790ec-118">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-119">IDENTIFIant unique dans une ligne de médias.</span><span class="sxs-lookup"><span data-stu-id="790ec-119">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-120">StartTime</span><span class="sxs-lookup"><span data-stu-id="790ec-120">StartTime</span></span></p></td>
<td><p><span data-ttu-id="790ec-121">DateHeure</span><span class="sxs-lookup"><span data-stu-id="790ec-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="790ec-122">Heure de début de la session.</span><span class="sxs-lookup"><span data-stu-id="790ec-122">Start time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-123">EndTime</span><span class="sxs-lookup"><span data-stu-id="790ec-123">EndTime</span></span></p></td>
<td><p><span data-ttu-id="790ec-124">DateHeure</span><span class="sxs-lookup"><span data-stu-id="790ec-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="790ec-125">Heure de fin de la session.</span><span class="sxs-lookup"><span data-stu-id="790ec-125">End time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-126">DialogCategory</span><span class="sxs-lookup"><span data-stu-id="790ec-126">DialogCategory</span></span></p></td>
<td><p><span data-ttu-id="790ec-127">bit</span><span class="sxs-lookup"><span data-stu-id="790ec-127">bit</span></span></p></td>
<td><p><span data-ttu-id="790ec-128">Catégorie de boîte de dialogue : 0 est le serveur Lync en jambes du serveur de médiation ; 1 est le serveur de médiation pour le tronçon de passerelle PSTN.</span><span class="sxs-lookup"><span data-stu-id="790ec-128">Dialog category: 0 is the Lync Server to Mediation Server leg; 1 is the Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-129">MediationServerBypassFlag</span><span class="sxs-lookup"><span data-stu-id="790ec-129">MediationServerBypassFlag</span></span></p></td>
<td><p><span data-ttu-id="790ec-130">bit</span><span class="sxs-lookup"><span data-stu-id="790ec-130">bit</span></span></p></td>
<td><p><span data-ttu-id="790ec-131">Indicateur indiquant si l’appel a été ignoré ou non.</span><span class="sxs-lookup"><span data-stu-id="790ec-131">Flag indicating if the call was bypassed or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-132">MediaBypassWarningFlag</span><span class="sxs-lookup"><span data-stu-id="790ec-132">MediaBypassWarningFlag</span></span></p></td>
<td><p><span data-ttu-id="790ec-133">int</span><span class="sxs-lookup"><span data-stu-id="790ec-133">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-134">Le cas échéant, indique pourquoi un appel n’a pas été ignoré, même si les ID de contournement correspondent.</span><span class="sxs-lookup"><span data-stu-id="790ec-134">If present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="790ec-135">Une seule valeur est définie :</span><span class="sxs-lookup"><span data-stu-id="790ec-135">Only one value is defined:</span></span></p>
<p><span data-ttu-id="790ec-136">0x0001-ID de contournement inconnu pour la carte réseau par défaut.</span><span class="sxs-lookup"><span data-stu-id="790ec-136">0x0001 – Unknown bypass ID for Default network adapter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-137">CallPriority</span><span class="sxs-lookup"><span data-stu-id="790ec-137">CallPriority</span></span></p></td>
<td><p><span data-ttu-id="790ec-138">int</span><span class="sxs-lookup"><span data-stu-id="790ec-138">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-139">Priorité de l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-139">Priority of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-140">CallerPool</span><span class="sxs-lookup"><span data-stu-id="790ec-140">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="790ec-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="790ec-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="790ec-142">Nom de domaine complet du pool d’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-142">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-143">CalleePool</span><span class="sxs-lookup"><span data-stu-id="790ec-143">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="790ec-144">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="790ec-144">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="790ec-145">Nom de domaine complet (FQDN) du pool d’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-145">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-146">Appelant</span><span class="sxs-lookup"><span data-stu-id="790ec-146">Caller</span></span></p></td>
<td><p><span data-ttu-id="790ec-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="790ec-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="790ec-148">URI de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-148">Caller’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-149">Appelé</span><span class="sxs-lookup"><span data-stu-id="790ec-149">Callee</span></span></p></td>
<td><p><span data-ttu-id="790ec-150">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="790ec-150">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="790ec-151">URI de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-151">Callee’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-152">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="790ec-152">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="790ec-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="790ec-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="790ec-154">Chaîne de l’agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-154">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-155">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="790ec-155">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="790ec-156">type</span><span class="sxs-lookup"><span data-stu-id="790ec-156">smallint</span></span></p></td>
<td><p><span data-ttu-id="790ec-157">Type de l’agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-157">Type of the caller’s user agent.</span></span> <span data-ttu-id="790ec-158">Pour plus d’informations, voir la <a href="lync-server-2013-useragent-table.md">table UserAgent dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="790ec-158">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-159">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="790ec-159">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="790ec-160">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="790ec-160">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="790ec-161">Catégorie de l’agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-161">Category of the caller’s user agent.</span></span> <span data-ttu-id="790ec-162">Pour plus d’informations, reportez-vous <a href="lync-server-2013-useragentdef-table-qoe.md">à la table UserAgentDef (QoE) dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="790ec-162">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-163">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="790ec-163">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="790ec-164">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="790ec-164">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="790ec-165">Chaîne de l’agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-165">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-166">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="790ec-166">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="790ec-167">type</span><span class="sxs-lookup"><span data-stu-id="790ec-167">smallint</span></span></p></td>
<td><p><span data-ttu-id="790ec-168">Type de l’agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-168">Type of callee’s user agent.</span></span> <span data-ttu-id="790ec-169">Pour plus d’informations, voir la <a href="lync-server-2013-useragent-table.md">table UserAgent dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="790ec-169">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-170">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="790ec-170">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="790ec-171">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="790ec-171">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="790ec-172">Catégorie de l’agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-172">Category of callee’s user agent.</span></span> <span data-ttu-id="790ec-173">Pour plus d’informations, reportez-vous <a href="lync-server-2013-useragentdef-table-qoe.md">à la table UserAgentDef (QoE) dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="790ec-173">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-174">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="790ec-174">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="790ec-175">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="790ec-175">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="790ec-176">Nom du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-176">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-177">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="790ec-177">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="790ec-178">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="790ec-178">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="790ec-179">Nom du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-179">Callee’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-180">Appelant</span><span class="sxs-lookup"><span data-stu-id="790ec-180">CallerOS</span></span></p></td>
<td><p><span data-ttu-id="790ec-181">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="790ec-181">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="790ec-182">Système d’exploitation (se) du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-182">Operating system (OS) of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-183">CalleeOS</span><span class="sxs-lookup"><span data-stu-id="790ec-183">CalleeOS</span></span></p></td>
<td><p><span data-ttu-id="790ec-184">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="790ec-184">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="790ec-185">Système d’exploitation (se) du point de terminaison de l’appelé.</span><span class="sxs-lookup"><span data-stu-id="790ec-185">Operating system (OS) of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-186">CallerCPUName</span><span class="sxs-lookup"><span data-stu-id="790ec-186">CallerCPUName</span></span></p></td>
<td><p><span data-ttu-id="790ec-187">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="790ec-187">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="790ec-188">Nom de l’UC du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-188">CPU name of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-189">CalleeCPUName</span><span class="sxs-lookup"><span data-stu-id="790ec-189">CalleeCPUName</span></span></p></td>
<td><p><span data-ttu-id="790ec-190">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="790ec-190">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="790ec-191">Nom de l’UC du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-191">CPU name of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-192">CallerCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="790ec-192">CallerCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="790ec-193">type</span><span class="sxs-lookup"><span data-stu-id="790ec-193">smallint</span></span></p></td>
<td><p><span data-ttu-id="790ec-194">Nombre de cœurs d’UC du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-194">Number of CPU cores in the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-195">CalleeCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="790ec-195">CalleeCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="790ec-196">type</span><span class="sxs-lookup"><span data-stu-id="790ec-196">smallint</span></span></p></td>
<td><p><span data-ttu-id="790ec-197">Nombre de cœurs d’UC du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-197">Number of CPU cores in the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-198">CallerCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="790ec-198">CallerCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="790ec-199">int</span><span class="sxs-lookup"><span data-stu-id="790ec-199">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-200">Vitesse de processeur de l’UC du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-200">CPU processor speed of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-201">CalleeCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="790ec-201">CalleeCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="790ec-202">int</span><span class="sxs-lookup"><span data-stu-id="790ec-202">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-203">Vitesse de processeur de l’UC du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-203">CPU processor speed of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-204">CallerVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="790ec-204">CallerVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="790ec-205">tinyint</span><span class="sxs-lookup"><span data-stu-id="790ec-205">tinyint</span></span></p></td>
<td><p><span data-ttu-id="790ec-206">Indique si le système de l’appelant s’exécute dans un environnement virtualisé.</span><span class="sxs-lookup"><span data-stu-id="790ec-206">Indicates whether the caller’s system is running in a virtualized environment.</span></span> <span data-ttu-id="790ec-207">Pour plus d’informations, voir la <a href="lync-server-2013-endpoint-table.md">table Endpoint dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="790ec-207">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-208">CalleeVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="790ec-208">CalleeVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="790ec-209">tinyint</span><span class="sxs-lookup"><span data-stu-id="790ec-209">tinyint</span></span></p></td>
<td><p><span data-ttu-id="790ec-210">Indique si le système de l’appelant s’exécute dans un environnement virtualisé.</span><span class="sxs-lookup"><span data-stu-id="790ec-210">Indicates whether the callee’s system is running in a virtualized environment.</span></span> <span data-ttu-id="790ec-211">Pour plus d’informations, voir la <a href="lync-server-2013-endpoint-table.md">table Endpoint dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="790ec-211">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-212">CorrelationKey</span><span class="sxs-lookup"><span data-stu-id="790ec-212">CorrelationKey</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="790ec-213">Clé de corrélation.</span><span class="sxs-lookup"><span data-stu-id="790ec-213">Correlation key.</span></span> <span data-ttu-id="790ec-214">Fait référence à partir de la <a href="lync-server-2013-sessioncorrelation-table.md">table SessionCorrelation dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="790ec-214">Referenced from the <a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-215">ConnectivityIce</span><span class="sxs-lookup"><span data-stu-id="790ec-215">ConnectivityIce</span></span></p></td>
<td><p><span data-ttu-id="790ec-216">tinyint</span><span class="sxs-lookup"><span data-stu-id="790ec-216">tinyint</span></span></p></td>
<td><p><span data-ttu-id="790ec-217">Des informations sur le chemin multimédia, par exemple direct ou relayé.</span><span class="sxs-lookup"><span data-stu-id="790ec-217">Information about the media path, such as direct or relayed.</span></span> <span data-ttu-id="790ec-218">Pour plus d’informations, voir la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="790ec-218">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-219">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="790ec-219">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="790ec-220">int</span><span class="sxs-lookup"><span data-stu-id="790ec-220">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-221">Informations sur le processus de création d’une connexion interactive (ICE) décrite dans les indicateurs bits pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-221">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="790ec-222">Pour plus d’informations, reportez-vous à la spécification relative au protocole serveur pour le contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="790ec-222">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-223">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="790ec-223">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="790ec-224">int</span><span class="sxs-lookup"><span data-stu-id="790ec-224">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-225">Informations sur le processus de création d’une connexion interactive (ICE) décrite dans les indicateurs bits pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-225">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="790ec-226">Pour plus d’informations, reportez-vous à la spécification relative au protocole serveur pour le contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="790ec-226">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-227">Transport</span><span class="sxs-lookup"><span data-stu-id="790ec-227">Transport</span></span></p></td>
<td><p><span data-ttu-id="790ec-228">tinyint</span><span class="sxs-lookup"><span data-stu-id="790ec-228">tinyint</span></span></p></td>
<td><p><span data-ttu-id="790ec-229">Le type de transport : 0 correspond au protocole UDP ; 1 est le protocole TCP.</span><span class="sxs-lookup"><span data-stu-id="790ec-229">Transport type: 0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-230">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="790ec-230">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="790ec-231">var (50)</span><span class="sxs-lookup"><span data-stu-id="790ec-231">var(50)</span></span></p></td>
<td><p><span data-ttu-id="790ec-232">Adresse IP de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-232">IP address of the caller.</span></span> <span data-ttu-id="790ec-233">Il peut s’agir d’une adresse IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="790ec-233">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-234">CallerPort</span><span class="sxs-lookup"><span data-stu-id="790ec-234">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="790ec-235">int</span><span class="sxs-lookup"><span data-stu-id="790ec-235">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-236">Port utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-236">Port used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-237">CallerInside</span><span class="sxs-lookup"><span data-stu-id="790ec-237">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="790ec-238">bit</span><span class="sxs-lookup"><span data-stu-id="790ec-238">bit</span></span></p></td>
<td><p><span data-ttu-id="790ec-239">Indique si l’appelant se trouve à l’intérieur du réseau intervalle : 1 désigne l’appelant à l’intérieur du réseau d’entreprise, 0 indique que l’appelant se trouve hors du réseau.</span><span class="sxs-lookup"><span data-stu-id="790ec-239">Indicates whether the caller is inside the interval network: 1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-240">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="790ec-240">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="790ec-241">var (50)</span><span class="sxs-lookup"><span data-stu-id="790ec-241">var(50)</span></span></p></td>
<td><p><span data-ttu-id="790ec-242">Adresse IP de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-242">IP address of the callee.</span></span> <span data-ttu-id="790ec-243">Il peut s’agir d’une adresse IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="790ec-243">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-244">CalleePort</span><span class="sxs-lookup"><span data-stu-id="790ec-244">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="790ec-245">int</span><span class="sxs-lookup"><span data-stu-id="790ec-245">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-246">Port utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-246">Port used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-247">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="790ec-247">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="790ec-248">bit</span><span class="sxs-lookup"><span data-stu-id="790ec-248">bit</span></span></p></td>
<td><p><span data-ttu-id="790ec-249">Indique si l’appelant se trouve à l’intérieur de l’intervalle réseau : 1 signifie que l’appelant se trouve à l’intérieur du réseau d’entreprise, 0 indique que l’appelant se trouve hors du réseau.</span><span class="sxs-lookup"><span data-stu-id="790ec-249">Indicates whether the callee is inside the interval network: 1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-250">CallerUserSite</span><span class="sxs-lookup"><span data-stu-id="790ec-250">CallerUserSite</span></span></p></td>
<td><p><span data-ttu-id="790ec-251">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="790ec-251">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="790ec-252">Nom du site de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-252">Name of the caller’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-253">CallerRegion</span><span class="sxs-lookup"><span data-stu-id="790ec-253">CallerRegion</span></span></p></td>
<td><p><span data-ttu-id="790ec-254">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="790ec-254">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="790ec-255">Nom du pays/de la région du site de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-255">Name of the country/region of the caller’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-256">CalleeUserSite</span><span class="sxs-lookup"><span data-stu-id="790ec-256">CalleeUserSite</span></span></p></td>
<td><p><span data-ttu-id="790ec-257">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="790ec-257">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="790ec-258">Nom du site du ou des appelants.</span><span class="sxs-lookup"><span data-stu-id="790ec-258">Name of the callee’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-259">CalleeRegion</span><span class="sxs-lookup"><span data-stu-id="790ec-259">CalleeRegion</span></span></p></td>
<td><p><span data-ttu-id="790ec-260">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="790ec-260">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="790ec-261">Nom du pays/de la région du site de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-261">Name of the country/region of the callee’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-262">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="790ec-262">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="790ec-263">var (50)</span><span class="sxs-lookup"><span data-stu-id="790ec-263">var(50)</span></span></p></td>
<td><p><span data-ttu-id="790ec-264">Adresse IP du service Edge A/V utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-264">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="790ec-265">Pour plus d’informations, consultez la <a href="lync-server-2013-ipaddress-table.md">table IPAddress dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="790ec-265">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-266">CallerRelayPort</span><span class="sxs-lookup"><span data-stu-id="790ec-266">CallerRelayPort</span></span></p></td>
<td><p><span data-ttu-id="790ec-267">int</span><span class="sxs-lookup"><span data-stu-id="790ec-267">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-268">Port utilisé sur le service Edge A/V utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-268">Port used on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-269">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="790ec-269">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="790ec-270">var (50)</span><span class="sxs-lookup"><span data-stu-id="790ec-270">var(50)</span></span></p></td>
<td><p><span data-ttu-id="790ec-271">Clé d’adresse IP du service Edge A/V utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-271">IP Address key of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="790ec-272">Pour plus d’informations, consultez la <a href="lync-server-2013-ipaddress-table.md">table IPAddress dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="790ec-272">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-273">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="790ec-273">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="790ec-274">int</span><span class="sxs-lookup"><span data-stu-id="790ec-274">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-275">Port utilisé sur le service Edge A/V utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-275">Port used on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-276">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="790ec-276">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="790ec-277">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="790ec-277">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="790ec-278">Nom de l’appareil de capture de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-278">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-279">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="790ec-279">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="790ec-280">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="790ec-280">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="790ec-281">Nom de l’appareil de rendu de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-281">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-282">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="790ec-282">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="790ec-283">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="790ec-283">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="790ec-284">Nom du pilote de périphérique de capture de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-284">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-285">CallerRenderDriver</span><span class="sxs-lookup"><span data-stu-id="790ec-285">CallerRenderDriver</span></span></p></td>
<td><p><span data-ttu-id="790ec-286">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="790ec-286">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="790ec-287">Nom du pilote de périphérique de rendu de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-287">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-288">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="790ec-288">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="790ec-289">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="790ec-289">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="790ec-290">Nom de l’appareil de capture du destinataire.</span><span class="sxs-lookup"><span data-stu-id="790ec-290">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-291">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="790ec-291">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="790ec-292">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="790ec-292">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="790ec-293">Nom de l’appareil de rendu de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-293">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-294">CalleeCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="790ec-294">CalleeCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="790ec-295">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="790ec-295">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="790ec-296">Nom du pilote de l’appareil de capture du appelé.</span><span class="sxs-lookup"><span data-stu-id="790ec-296">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-297">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="790ec-297">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="790ec-298">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="790ec-298">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="790ec-299">Nom du pilote du périphérique de rendu de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-299">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-300">CallerNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="790ec-300">CallerNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="790ec-301">tinyint</span><span class="sxs-lookup"><span data-stu-id="790ec-301">tinyint</span></span></p></td>
<td><p><span data-ttu-id="790ec-302">Type de connexion réseau de l’appelant : 0 est filaire, 1 est un réseau sans fil.</span><span class="sxs-lookup"><span data-stu-id="790ec-302">Caller’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-303">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="790ec-303">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="790ec-304">bit</span><span class="sxs-lookup"><span data-stu-id="790ec-304">bit</span></span></p></td>
<td><p><span data-ttu-id="790ec-305">Indique si l’appelant s’est connecté via un réseau privé virtuel : 1 est un réseau privé virtuel (VPN), 0 est non VPN.</span><span class="sxs-lookup"><span data-stu-id="790ec-305">Indicates whether the caller connected over a virtual private network: 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-306">CallerLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="790ec-306">CallerLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="790ec-307">décimale (18, 0)</span><span class="sxs-lookup"><span data-stu-id="790ec-307">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="790ec-308">Vitesse de liaison réseau pour le point de terminaison de l’appelant en bps.</span><span class="sxs-lookup"><span data-stu-id="790ec-308">Network link speed for the caller's endpoint in bps.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-309">CalleeNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="790ec-309">CalleeNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="790ec-310">tinyint</span><span class="sxs-lookup"><span data-stu-id="790ec-310">tinyint</span></span></p></td>
<td><p><span data-ttu-id="790ec-311">Type de connexion réseau du ou du destinataire : 0 est filaire, 1 est un téléphone sans fil.</span><span class="sxs-lookup"><span data-stu-id="790ec-311">Callee’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-312">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="790ec-312">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="790ec-313">bit</span><span class="sxs-lookup"><span data-stu-id="790ec-313">bit</span></span></p></td>
<td><p><span data-ttu-id="790ec-314">Indique si l’appelant s’est connecté via un réseau privé virtuel : 1 est un réseau privé virtuel (VPN), 0 est non VPN.</span><span class="sxs-lookup"><span data-stu-id="790ec-314">Indicates whether the caller connected over a virtual private network: 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-315">CalleeLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="790ec-315">CalleeLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="790ec-316">décimale (18, 0)</span><span class="sxs-lookup"><span data-stu-id="790ec-316">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="790ec-317">Vitesse de liaison réseau pour le point de terminaison de l’appelant en bps.</span><span class="sxs-lookup"><span data-stu-id="790ec-317">Network link speed for the callee's endpoint in bps.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-318">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="790ec-318">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="790ec-319">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-319">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-320">La fonction de conversation à bande étroite des sessions audio (en fonction des deux flux audio).</span><span class="sxs-lookup"><span data-stu-id="790ec-320">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-321">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="790ec-321">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="790ec-322">int</span><span class="sxs-lookup"><span data-stu-id="790ec-322">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-323">Bande passante réelle appliquée au flux d’envoi indiqué en fonction de différents paramètres de stratégie (TURN, API, SDP, serveur de stratégie, etc.).</span><span class="sxs-lookup"><span data-stu-id="790ec-323">Actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="790ec-324">Ce problème ne doit pas être confondu avec la bande passante effective, car il peut y avoir une bande passante effective plus faible en fonction de l’estimation de bande passante.</span><span class="sxs-lookup"><span data-stu-id="790ec-324">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="790ec-325">Il s’agit essentiellement de la bande passante maximale que le flux d’envoi peut prendre en limitant l’estimation de la bande passante.</span><span class="sxs-lookup"><span data-stu-id="790ec-325">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-326">JitterInterArrival</span><span class="sxs-lookup"><span data-stu-id="790ec-326">JitterInterArrival</span></span></p></td>
<td><p><span data-ttu-id="790ec-327">int</span><span class="sxs-lookup"><span data-stu-id="790ec-327">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-328">Gigue réseau moyenne des statistiques de protocole RTCP (Real Time Control Protocol).</span><span class="sxs-lookup"><span data-stu-id="790ec-328">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-329">JitterInterArrivalMax</span><span class="sxs-lookup"><span data-stu-id="790ec-329">JitterInterArrivalMax</span></span></p></td>
<td><p><span data-ttu-id="790ec-330">int</span><span class="sxs-lookup"><span data-stu-id="790ec-330">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-331">Scintillement du réseau maximum lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-331">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-332">PacketLossRate</span><span class="sxs-lookup"><span data-stu-id="790ec-332">PacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="790ec-333">décimale (5 ; 4)</span><span class="sxs-lookup"><span data-stu-id="790ec-333">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="790ec-334">Taux moyen de perte de paquets lors de l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-334">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-335">PacketLossRateMax</span><span class="sxs-lookup"><span data-stu-id="790ec-335">PacketLossRateMax</span></span></p></td>
<td><p><span data-ttu-id="790ec-336">décimale (5 ; 4)</span><span class="sxs-lookup"><span data-stu-id="790ec-336">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="790ec-337">Perte de paquets maximum observée pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-337">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-338">BurstDensity</span><span class="sxs-lookup"><span data-stu-id="790ec-338">BurstDensity</span></span></p></td>
<td><p><span data-ttu-id="790ec-339">décimale (9 ; 4)</span><span class="sxs-lookup"><span data-stu-id="790ec-339">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="790ec-340">Densité moyenne de perte de paquets en rafales de pertes pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-340">Average density of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-341">BurstDuration</span><span class="sxs-lookup"><span data-stu-id="790ec-341">BurstDuration</span></span></p></td>
<td><p><span data-ttu-id="790ec-342">int</span><span class="sxs-lookup"><span data-stu-id="790ec-342">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-343">Durée moyenne de perte de paquets en rafales de pertes pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-343">Average duration of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-344">BurstGapDensity</span><span class="sxs-lookup"><span data-stu-id="790ec-344">BurstGapDensity</span></span></p></td>
<td><p><span data-ttu-id="790ec-345">décimale (9 ; 4)</span><span class="sxs-lookup"><span data-stu-id="790ec-345">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="790ec-346">Densité moyenne de perte de paquets lors de l’intervalle entre les pics de perte de paquets.</span><span class="sxs-lookup"><span data-stu-id="790ec-346">Average density of packet loss during gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-347">BurstGapDuration</span><span class="sxs-lookup"><span data-stu-id="790ec-347">BurstGapDuration</span></span></p></td>
<td><p><span data-ttu-id="790ec-348">int</span><span class="sxs-lookup"><span data-stu-id="790ec-348">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-349">Durée moyenne des espaces entre les pics de perte de paquets.</span><span class="sxs-lookup"><span data-stu-id="790ec-349">Average duration of gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-350">PacketUtilization</span><span class="sxs-lookup"><span data-stu-id="790ec-350">PacketUtilization</span></span></p></td>
<td><p><span data-ttu-id="790ec-351">int</span><span class="sxs-lookup"><span data-stu-id="790ec-351">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-352">Nombre de paquets pour le flux audio.</span><span class="sxs-lookup"><span data-stu-id="790ec-352">Packet count for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-353">Bande passante</span><span class="sxs-lookup"><span data-stu-id="790ec-353">BandwidthEst</span></span></p></td>
<td><p><span data-ttu-id="790ec-354">int</span><span class="sxs-lookup"><span data-stu-id="790ec-354">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-355">Estimations de bande passante pour le flux audio.</span><span class="sxs-lookup"><span data-stu-id="790ec-355">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-356">DegradationAvg</span><span class="sxs-lookup"><span data-stu-id="790ec-356">DegradationAvg</span></span></p></td>
<td><p><span data-ttu-id="790ec-357">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-357">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-358">Baisse de la dégradation du réseau pour l’ensemble de l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-358">Network MOS Degradation for the whole call.</span></span> <span data-ttu-id="790ec-359">La plage est 0,0 à 5,0.</span><span class="sxs-lookup"><span data-stu-id="790ec-359">Range is 0.0 to 5.0.</span></span> <span data-ttu-id="790ec-360">Cette mesure indique la somme que le coût du réseau a diminué en raison de la gigue et de la perte de paquets.</span><span class="sxs-lookup"><span data-stu-id="790ec-360">This metric shows the amount the Network MOS was reduced because of jitter and packet loss.</span></span> <span data-ttu-id="790ec-361">Pour une qualité acceptable, elle doit être inférieure à 0,5.</span><span class="sxs-lookup"><span data-stu-id="790ec-361">For acceptable quality it should less than 0.5.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-362">DegradationMax</span><span class="sxs-lookup"><span data-stu-id="790ec-362">DegradationMax</span></span></p></td>
<td><p><span data-ttu-id="790ec-363">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-363">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-364">Dégradation du réseau maximal pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-364">Maximum Network MOS degradation during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-365">DegradationJitterAvg</span><span class="sxs-lookup"><span data-stu-id="790ec-365">DegradationJitterAvg</span></span></p></td>
<td><p><span data-ttu-id="790ec-366">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-366">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-367">Baisse de la dégradation du réseau à l’origine de gigue.</span><span class="sxs-lookup"><span data-stu-id="790ec-367">Network MOS degradation caused by jitter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-368">DegradationPacketLossAvg</span><span class="sxs-lookup"><span data-stu-id="790ec-368">DegradationPacketLossAvg</span></span></p></td>
<td><p><span data-ttu-id="790ec-369">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-369">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-370">Baisse de la dégradation du réseau à l’origine de la perte de paquets.</span><span class="sxs-lookup"><span data-stu-id="790ec-370">Network MOS degradation caused by packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-371">PayloadDescription</span><span class="sxs-lookup"><span data-stu-id="790ec-371">PayloadDescription</span></span></p></td>
<td><p><span data-ttu-id="790ec-372">int</span><span class="sxs-lookup"><span data-stu-id="790ec-372">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-373">Le codec audio utilisé pour l’appel, référencé à partir de la <a href="lync-server-2013-payloaddescription-table.md">table PayloadDescription dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="790ec-373">The audio codec used for the call, referenced from the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-374">AudioSampleRate</span><span class="sxs-lookup"><span data-stu-id="790ec-374">AudioSampleRate</span></span></p></td>
<td><p><span data-ttu-id="790ec-375">int</span><span class="sxs-lookup"><span data-stu-id="790ec-375">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-376">Taux d’échantillonnage pour le flux audio.</span><span class="sxs-lookup"><span data-stu-id="790ec-376">Sampling rate for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-377">CallerSendSignalLevel</span><span class="sxs-lookup"><span data-stu-id="790ec-377">CallerSendSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="790ec-378">int</span><span class="sxs-lookup"><span data-stu-id="790ec-378">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-379">Le niveau du signal audio après le contrôle de gain analogique pour le son envoyé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-379">Post-Analog Gain Control audio signal level for the audio the caller sent.</span></span> <span data-ttu-id="790ec-380">L’unité de cette métrique est dBmo.</span><span class="sxs-lookup"><span data-stu-id="790ec-380">The unit for this metric is dBmo.</span></span> <span data-ttu-id="790ec-381">Pour une qualité acceptable, il devrait représenter au moins 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="790ec-381">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="790ec-382">Cette métrique n’est pas communiquée par le serveur de conférence A/V ou les téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="790ec-382">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-383">CallerRecvSignalLevel</span><span class="sxs-lookup"><span data-stu-id="790ec-383">CallerRecvSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="790ec-384">int</span><span class="sxs-lookup"><span data-stu-id="790ec-384">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-385">Niveau du signal audio de l’appelant reçu.</span><span class="sxs-lookup"><span data-stu-id="790ec-385">Audio signal level for the audio the caller received.</span></span> <span data-ttu-id="790ec-386">L’unité de cette métrique est dBmo.</span><span class="sxs-lookup"><span data-stu-id="790ec-386">The unit for this metric is dBmo.</span></span> <span data-ttu-id="790ec-387">Pour une qualité acceptable, il devrait représenter au moins 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="790ec-387">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="790ec-388">Cette métrique n’est pas communiquée par le serveur de conférence A/V ou les téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="790ec-388">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-389">CallerSendNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="790ec-389">CallerSendNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="790ec-390">int</span><span class="sxs-lookup"><span data-stu-id="790ec-390">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-391">Le niveau sonore de contrôle du bruit de l’appelant envoyé.</span><span class="sxs-lookup"><span data-stu-id="790ec-391">Post-Analog Gain Control audio noise level for the audio the caller sent.</span></span> <span data-ttu-id="790ec-392">L’unité de cette métrique est dBmo.</span><span class="sxs-lookup"><span data-stu-id="790ec-392">The unit for this metric is dBmo.</span></span> <span data-ttu-id="790ec-393">Pour une qualité acceptable, elle doit être inférieure à 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="790ec-393">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="790ec-394">Cette métrique n’est pas communiquée par le serveur de conférence A/V ou les téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="790ec-394">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-395">CallerRecvNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="790ec-395">CallerRecvNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="790ec-396">int</span><span class="sxs-lookup"><span data-stu-id="790ec-396">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-397">Le niveau de bruit audio de contrôle de gain analogique pour le son reçu par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-397">Post-Analog Gain Control audio noise level for the audio the caller received.</span></span> <span data-ttu-id="790ec-398">L’unité de cette métrique est dBmo.</span><span class="sxs-lookup"><span data-stu-id="790ec-398">The unit for this metric is dBmo.</span></span> <span data-ttu-id="790ec-399">Pour une qualité acceptable, elle doit être inférieure à 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="790ec-399">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="790ec-400">Cette métrique n’est pas communiquée par le serveur de conférence A/V ou les téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="790ec-400">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-401">CallerEchoReturn</span><span class="sxs-lookup"><span data-stu-id="790ec-401">CallerEchoReturn</span></span></p></td>
<td><p><span data-ttu-id="790ec-402">int</span><span class="sxs-lookup"><span data-stu-id="790ec-402">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-403">Amélioration de la perte d’écho pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-403">Echo Return Loss Enhancement for the caller.</span></span> <span data-ttu-id="790ec-404">L’unité de cette métrique est dB.</span><span class="sxs-lookup"><span data-stu-id="790ec-404">The unit for this metric is dB.</span></span> <span data-ttu-id="790ec-405">Les valeurs inférieures représentent moins d’écho.</span><span class="sxs-lookup"><span data-stu-id="790ec-405">Lower values represent less echo.</span></span> <span data-ttu-id="790ec-406">Cette métrique n’est pas communiquée par le serveur de conférence A/V ou les téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="790ec-406">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-407">CallerSpeakerGlitchRate</span><span class="sxs-lookup"><span data-stu-id="790ec-407">CallerSpeakerGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="790ec-408">int</span><span class="sxs-lookup"><span data-stu-id="790ec-408">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-409">Moyenne des problèmes par cinq minutes pour le rendu du haut-parleur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-409">Average glitches per five minutes for the caller’s loudspeaker rendering.</span></span> <span data-ttu-id="790ec-410">Pour une qualité optimale, cela devrait être inférieur à une par cinq minutes.</span><span class="sxs-lookup"><span data-stu-id="790ec-410">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="790ec-411">Non communiquées par des serveurs de conférence A/V, des serveurs de médiation ou des téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="790ec-411">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-412">CallerMicGlitchRate</span><span class="sxs-lookup"><span data-stu-id="790ec-412">CallerMicGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="790ec-413">int</span><span class="sxs-lookup"><span data-stu-id="790ec-413">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-414">Moyenne des problèmes par cinq minutes pour la capture du micro de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-414">Average glitches per five minutes for the caller’s microphone capture.</span></span> <span data-ttu-id="790ec-415">Pour une qualité optimale, il devrait être inférieur à une par cinq minutes.</span><span class="sxs-lookup"><span data-stu-id="790ec-415">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="790ec-416">Non communiquées par des serveurs de conférence A/V, des serveurs de médiation ou des téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="790ec-416">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-417">CallerTimestampDriftRateMic</span><span class="sxs-lookup"><span data-stu-id="790ec-417">CallerTimestampDriftRateMic</span></span></p></td>
<td><p><span data-ttu-id="790ec-418">décimale (9 ; 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-418">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-419">Taux d’utilisation de l’horloge du périphérique microphone de l’appelant par rapport à l’horloge de l’UC.</span><span class="sxs-lookup"><span data-stu-id="790ec-419">Caller’s microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-420">CallerTimestampDriftRateSpk</span><span class="sxs-lookup"><span data-stu-id="790ec-420">CallerTimestampDriftRateSpk</span></span></p></td>
<td><p><span data-ttu-id="790ec-421">décimale (9 ; 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-421">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-422">Taux d’horloge des périphériques de haut-parleurs de l’appelant par rapport à l’horloge de l’UC.</span><span class="sxs-lookup"><span data-stu-id="790ec-422">Caller’s speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-423">CallerTimestampErrorMicMs</span><span class="sxs-lookup"><span data-stu-id="790ec-423">CallerTimestampErrorMicMs</span></span></p></td>
<td><p><span data-ttu-id="790ec-424">décimale (9 ; 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-424">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-425">Erreur d’horodatage du flux de capture de microphone moyenne, en millisecondes, au cours des dernières 20 secondes de l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-425">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-426">CallerTimestampErrorSpkMs</span><span class="sxs-lookup"><span data-stu-id="790ec-426">CallerTimestampErrorSpkMs</span></span></p></td>
<td><p><span data-ttu-id="790ec-427">décimale (9 ; 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-427">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-428">Moyenne de l’erreur d’horodatage du flux de haut-parleur de l’appelant, en millisecondes, au cours des dernières 20 secondes de l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-428">Average of the caller’s speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-429">CallerVsEntryCauses</span><span class="sxs-lookup"><span data-stu-id="790ec-429">CallerVsEntryCauses</span></span></p></td>
<td><p><span data-ttu-id="790ec-430">type</span><span class="sxs-lookup"><span data-stu-id="790ec-430">smallint</span></span></p></td>
<td><p><span data-ttu-id="790ec-431">Le commutateur vocal est un mode semi-duplex présentant une capacité d’interruption réduite.</span><span class="sxs-lookup"><span data-stu-id="790ec-431">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="790ec-432">Pour plus d’informations, voir la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="790ec-432">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-433">CallerEchoEventCauses</span><span class="sxs-lookup"><span data-stu-id="790ec-433">CallerEchoEventCauses</span></span></p></td>
<td><p><span data-ttu-id="790ec-434">tinyint</span><span class="sxs-lookup"><span data-stu-id="790ec-434">tinyint</span></span></p></td>
<td><p><span data-ttu-id="790ec-435">Causes d’un événement ECHO pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-435">Causes of an echo event for the caller.</span></span> <span data-ttu-id="790ec-436">Pour plus d’informations, voir la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="790ec-436">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-437">CallerEchoPercentMicIn</span><span class="sxs-lookup"><span data-stu-id="790ec-437">CallerEchoPercentMicIn</span></span></p></td>
<td><p><span data-ttu-id="790ec-438">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-438">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-439">Pourcentage de temps pendant lequel l’écho est détecté dans le flux de capture du microphone de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-439">Percentage of time when echo is detected in the caller’s microphone capture stream.</span></span> <span data-ttu-id="790ec-440">Si le casque est utilisé, la valeur doit être faible.</span><span class="sxs-lookup"><span data-stu-id="790ec-440">If headset is used, the value should be low.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-441">CallerEchoPercentSend</span><span class="sxs-lookup"><span data-stu-id="790ec-441">CallerEchoPercentSend</span></span></p></td>
<td><p><span data-ttu-id="790ec-442">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-442">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-443">Pourcentage de temps pendant lequel l’écho est détecté dans le flux envoyé de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-443">Percentage of time when echo is detected in the caller’s sent stream.</span></span> <span data-ttu-id="790ec-444">Pourcentage d’écho élevé dans les flux d’envoi indicateur de fuite d’écho.</span><span class="sxs-lookup"><span data-stu-id="790ec-444">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-445">CallerRxAGCSignalLevel</span><span class="sxs-lookup"><span data-stu-id="790ec-445">CallerRxAGCSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="790ec-446">int</span><span class="sxs-lookup"><span data-stu-id="790ec-446">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-447">Reçu le niveau du signal sur le serveur de médiation de la passerelle pour le son de l’appelant ; Cela s’applique uniquement au serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="790ec-447">Received signal level on the Mediation Server from the Gateway for the caller’s audio; this applies only to the Mediation Server.</span></span> <span data-ttu-id="790ec-448">L’unité de cette valeur est dBoV.</span><span class="sxs-lookup"><span data-stu-id="790ec-448">The unit of this metric is dBoV.</span></span> <span data-ttu-id="790ec-449">Pour une qualité optimale, la plage acceptable doit être comprise entre-30 et-18 dBoV.</span><span class="sxs-lookup"><span data-stu-id="790ec-449">For good quality, the acceptable range should be -30 to -18 dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-450">CallerRxAGCNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="790ec-450">CallerRxAGCNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="790ec-451">int</span><span class="sxs-lookup"><span data-stu-id="790ec-451">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-452">Reçu le niveau du signal sur le serveur de médiation de la passerelle pour le son de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-452">Received signal level on the Mediation Server from the Gateway for the caller’s audio.</span></span> <span data-ttu-id="790ec-453">Cela s’applique uniquement au serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="790ec-453">This applies only to the Mediation Server.</span></span> <span data-ttu-id="790ec-454">L’unité de cette valeur est dBoV.</span><span class="sxs-lookup"><span data-stu-id="790ec-454">The unit of this metric is dBoV.</span></span> <span data-ttu-id="790ec-455">Pour une qualité optimale, la plage acceptable doit être inférieure à-50 dBoV.</span><span class="sxs-lookup"><span data-stu-id="790ec-455">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-456">CallerRxAGCGain</span><span class="sxs-lookup"><span data-stu-id="790ec-456">CallerRxAGCGain</span></span></p></td>
<td><p><span data-ttu-id="790ec-457">int</span><span class="sxs-lookup"><span data-stu-id="790ec-457">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-458">Contrôle automatique de gain sur le côté du serveur de médiation appliqué au son de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-458">Automatic gain control (AGC) on the Mediation Server side applied to the caller’s audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-459">CallerInitialSignalLevelRMS</span><span class="sxs-lookup"><span data-stu-id="790ec-459">CallerInitialSignalLevelRMS</span></span></p></td>
<td><p><span data-ttu-id="790ec-460">float</span><span class="sxs-lookup"><span data-stu-id="790ec-460">float</span></span></p></td>
<td><p><span data-ttu-id="790ec-461">Moyenne quadratique (quadratique) du signal entrant à l’appelant pour les 30 premières secondes de l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-461">Root mean square (RMS) of the incoming signal to the caller for up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-462">CalleeSendSignalLevel</span><span class="sxs-lookup"><span data-stu-id="790ec-462">CalleeSendSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="790ec-463">int</span><span class="sxs-lookup"><span data-stu-id="790ec-463">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-464">Représente le niveau du signal audio du contrôle du gain sur le son de l’appel envoyé.</span><span class="sxs-lookup"><span data-stu-id="790ec-464">Represents the Post-Analog Gain Control audio signal level for the audio the callee sent.</span></span> <span data-ttu-id="790ec-465">L’unité de cette métrique est dBmo.</span><span class="sxs-lookup"><span data-stu-id="790ec-465">The unit for this metric is dBmo.</span></span> <span data-ttu-id="790ec-466">Pour une qualité acceptable, il devrait représenter au moins 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="790ec-466">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="790ec-467">Cette métrique n’est pas communiquée par le serveur de conférence A/V ou les téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="790ec-467">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-468">CalleeRecvSignalLevel</span><span class="sxs-lookup"><span data-stu-id="790ec-468">CalleeRecvSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="790ec-469">int</span><span class="sxs-lookup"><span data-stu-id="790ec-469">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-470">Niveau du signal audio pour le son de l’appelant reçu.</span><span class="sxs-lookup"><span data-stu-id="790ec-470">Audio signal level for the audio the callee received.</span></span> <span data-ttu-id="790ec-471">L’unité de cette métrique est dBmo.</span><span class="sxs-lookup"><span data-stu-id="790ec-471">The unit for this metric is dBmo.</span></span> <span data-ttu-id="790ec-472">Pour une qualité acceptable, il devrait représenter au moins 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="790ec-472">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="790ec-473">Cette métrique n’est pas communiquée par le serveur de conférence A/V ou les téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="790ec-473">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-474">CalleeSendNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="790ec-474">CalleeSendNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="790ec-475">int</span><span class="sxs-lookup"><span data-stu-id="790ec-475">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-476">Le niveau sonore de contrôle du bruit d’après-analogue pour le son de l’appel envoyé.</span><span class="sxs-lookup"><span data-stu-id="790ec-476">Post-Analog Gain Control audio noise level for the audio the callee sent.</span></span> <span data-ttu-id="790ec-477">L’unité de cette métrique est dBmo.</span><span class="sxs-lookup"><span data-stu-id="790ec-477">The unit for this metric is dBmo.</span></span> <span data-ttu-id="790ec-478">Pour une qualité acceptable, elle doit être inférieure à 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="790ec-478">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="790ec-479">Cette métrique n’est pas communiquée par le serveur de conférence A/V ou les téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="790ec-479">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-480">CalleeRecvNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="790ec-480">CalleeRecvNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="790ec-481">int</span><span class="sxs-lookup"><span data-stu-id="790ec-481">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-482">Le niveau sonore du contrôle du bruit de la fonction de gain analogique pour le son de l’appelant reçu.</span><span class="sxs-lookup"><span data-stu-id="790ec-482">Post-Analog Gain Control audio noise level for the audio the callee received.</span></span> <span data-ttu-id="790ec-483">L’unité de cette métrique est dBmo.</span><span class="sxs-lookup"><span data-stu-id="790ec-483">The unit for this metric is dBmo.</span></span> <span data-ttu-id="790ec-484">Pour une qualité acceptable, elle doit être inférieure à 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="790ec-484">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="790ec-485">Cette métrique n’est pas communiquée par le serveur de conférence A/V ou les téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="790ec-485">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-486">CalleeEchoReturn</span><span class="sxs-lookup"><span data-stu-id="790ec-486">CalleeEchoReturn</span></span></p></td>
<td><p><span data-ttu-id="790ec-487">int</span><span class="sxs-lookup"><span data-stu-id="790ec-487">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-488">Extension du retour de l’écho pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-488">Echo Return Loss Enhancement for the callee.</span></span> <span data-ttu-id="790ec-489">L’unité de cette métrique est dB.</span><span class="sxs-lookup"><span data-stu-id="790ec-489">The unit for this metric is dB.</span></span> <span data-ttu-id="790ec-490">Les valeurs inférieures représentent moins d’écho.</span><span class="sxs-lookup"><span data-stu-id="790ec-490">Lower values represent less echo.</span></span> <span data-ttu-id="790ec-491">Cette métrique n’est pas communiquée par le serveur de conférence A/V ou les téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="790ec-491">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-492">CalleeSpeakerGlitchRate</span><span class="sxs-lookup"><span data-stu-id="790ec-492">CalleeSpeakerGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="790ec-493">int</span><span class="sxs-lookup"><span data-stu-id="790ec-493">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-494">Moyenne des problèmes par cinq minutes pour le rendu du haut-parleur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-494">Average glitches per five minutes for the callee’s loudspeaker rendering.</span></span> <span data-ttu-id="790ec-495">Pour une qualité optimale, cela devrait être inférieur à une par cinq minutes.</span><span class="sxs-lookup"><span data-stu-id="790ec-495">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="790ec-496">Non communiquées par des serveurs de conférence A/V, des serveurs de médiation ou des téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="790ec-496">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-497">CalleeMicGlitchRate</span><span class="sxs-lookup"><span data-stu-id="790ec-497">CalleeMicGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="790ec-498">int</span><span class="sxs-lookup"><span data-stu-id="790ec-498">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-499">Moyenne des problèmes par cinq minutes pour la capture du micro de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-499">Average glitches per five minutes for the callee’s microphone capture.</span></span> <span data-ttu-id="790ec-500">Pour une qualité optimale, il devrait être inférieur à une par cinq minutes.</span><span class="sxs-lookup"><span data-stu-id="790ec-500">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="790ec-501">Non communiquées par des serveurs de conférence A/V, des serveurs de médiation ou des téléphones IP.</span><span class="sxs-lookup"><span data-stu-id="790ec-501">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-502">CalleeTimestampDriftRateMic</span><span class="sxs-lookup"><span data-stu-id="790ec-502">CalleeTimestampDriftRateMic</span></span></p></td>
<td><p><span data-ttu-id="790ec-503">décimale (9 ; 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-503">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-504">Taux d’utilisation de l’horloge du périphérique du micro du destinataire, par rapport à l’horloge de l’UC.</span><span class="sxs-lookup"><span data-stu-id="790ec-504">Callee’s microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-505">CalleeTimestampDriftRateSpk</span><span class="sxs-lookup"><span data-stu-id="790ec-505">CalleeTimestampDriftRateSpk</span></span></p></td>
<td><p><span data-ttu-id="790ec-506">décimale (9 ; 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-506">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-507">Taux d’horloge de l’horloge du périphérique du présentateur, par rapport à l’horloge du processeur.</span><span class="sxs-lookup"><span data-stu-id="790ec-507">Callee’s speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-508">CalleeTimestampErrorMicMs</span><span class="sxs-lookup"><span data-stu-id="790ec-508">CalleeTimestampErrorMicMs</span></span></p></td>
<td><p><span data-ttu-id="790ec-509">décimale (9 ; 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-509">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-510">Erreur d’horodatage du flux de capture de microphone moyenne, en millisecondes, au cours des dernières 20 secondes de l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-510">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-511">CalleeTimestampErrorSpkMs</span><span class="sxs-lookup"><span data-stu-id="790ec-511">CalleeTimestampErrorSpkMs</span></span></p></td>
<td><p><span data-ttu-id="790ec-512">décimale (9 ; 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-512">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-513">Moyenne de l’erreur d’horodatage du flux de rendu du haut-parleur de l’appelant, en millisecondes, au cours des dernières 20 secondes de l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-513">Average of the callee’s speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-514">CalleeVsEntryCauses</span><span class="sxs-lookup"><span data-stu-id="790ec-514">CalleeVsEntryCauses</span></span></p></td>
<td><p><span data-ttu-id="790ec-515">type</span><span class="sxs-lookup"><span data-stu-id="790ec-515">smallint</span></span></p></td>
<td><p><span data-ttu-id="790ec-516">Le commutateur vocal est un mode semi-duplex présentant une capacité d’interruption réduite.</span><span class="sxs-lookup"><span data-stu-id="790ec-516">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="790ec-517">Pour plus d’informations, voir la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="790ec-517">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-518">CalleeEchoEventCauses</span><span class="sxs-lookup"><span data-stu-id="790ec-518">CalleeEchoEventCauses</span></span></p></td>
<td><p><span data-ttu-id="790ec-519">tinyint</span><span class="sxs-lookup"><span data-stu-id="790ec-519">tinyint</span></span></p></td>
<td><p><span data-ttu-id="790ec-520">Causes d’un événement ECHO pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-520">Causes of an echo event for the callee.</span></span> <span data-ttu-id="790ec-521">Pour plus d’informations, voir la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="790ec-521">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-522">CalleeEchoPercentMicIn</span><span class="sxs-lookup"><span data-stu-id="790ec-522">CalleeEchoPercentMicIn</span></span></p></td>
<td><p><span data-ttu-id="790ec-523">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-523">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-524">Pourcentage de temps pendant lequel l’écho est détecté dans le flux de capture du micro de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-524">Percentage of time when echo is detected in the callee’s microphone capture stream.</span></span> <span data-ttu-id="790ec-525">Si le casque est utilisé, la valeur doit être faible.</span><span class="sxs-lookup"><span data-stu-id="790ec-525">If headset is used, the value should be low.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-526">CalleeEchoPercentSend</span><span class="sxs-lookup"><span data-stu-id="790ec-526">CalleeEchoPercentSend</span></span></p></td>
<td><p><span data-ttu-id="790ec-527">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-527">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-528">Pourcentage de temps pendant lequel l’écho est détecté dans le flux envoyé du destinataire du appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-528">Percentage of time when echo is detected in the callee’s sent stream.</span></span> <span data-ttu-id="790ec-529">Pourcentage d’écho élevé dans les flux d’envoi indicateur de fuite d’écho.</span><span class="sxs-lookup"><span data-stu-id="790ec-529">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-530">CalleeRxAGCSignalLevel</span><span class="sxs-lookup"><span data-stu-id="790ec-530">CalleeRxAGCSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="790ec-531">int</span><span class="sxs-lookup"><span data-stu-id="790ec-531">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-532">Reçu le niveau du signal sur le serveur de médiation de la passerelle pour le son de l’appelant ; Cela s’applique uniquement au serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="790ec-532">Received signal level on the Mediation Server from the Gateway for the callee’s audio; this applies only to the Mediation Server.</span></span> <span data-ttu-id="790ec-533">L’unité de cette valeur est dBoV.</span><span class="sxs-lookup"><span data-stu-id="790ec-533">The unit of this metric is dBoV.</span></span> <span data-ttu-id="790ec-534">Pour une qualité optimale, la plage acceptable doit être comprise entre [-30 et-18] dBoV.</span><span class="sxs-lookup"><span data-stu-id="790ec-534">For good quality, the acceptable range should be [-30 to -18] dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-535">CalleeRxAGCNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="790ec-535">CalleeRxAGCNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="790ec-536">int</span><span class="sxs-lookup"><span data-stu-id="790ec-536">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-537">Reçu le niveau du signal sur le serveur de médiation de la passerelle pour le son de l’appelé.</span><span class="sxs-lookup"><span data-stu-id="790ec-537">Received signal level on the Mediation Server from the Gateway for the callee’s audio.</span></span> <span data-ttu-id="790ec-538">Cela s’applique uniquement au serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="790ec-538">This applies only to the Mediation Server.</span></span> <span data-ttu-id="790ec-539">L’unité de cette valeur est dBoV.</span><span class="sxs-lookup"><span data-stu-id="790ec-539">The unit of this metric is dBoV.</span></span> <span data-ttu-id="790ec-540">Pour une qualité optimale, la plage acceptable doit être inférieure à-50 dBoV.</span><span class="sxs-lookup"><span data-stu-id="790ec-540">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-541">CalleeRxAGCGain</span><span class="sxs-lookup"><span data-stu-id="790ec-541">CalleeRxAGCGain</span></span></p></td>
<td><p><span data-ttu-id="790ec-542">int</span><span class="sxs-lookup"><span data-stu-id="790ec-542">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-543">Contrôle automatique de gain sur le côté du serveur de médiation appliqué au son de l’appelé.</span><span class="sxs-lookup"><span data-stu-id="790ec-543">Automatic gain control (AGC) on the Mediation Server side applied to the callee’s audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-544">CalleeInitialSignalLevelRMS</span><span class="sxs-lookup"><span data-stu-id="790ec-544">CalleeInitialSignalLevelRMS</span></span></p></td>
<td><p><span data-ttu-id="790ec-545">float</span><span class="sxs-lookup"><span data-stu-id="790ec-545">float</span></span></p></td>
<td><p><span data-ttu-id="790ec-546">Moyenne quadratique (quadratique) du signal entrant à l’appelant pour les 30 premières secondes de l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-546">Root mean square (RMS) of the incoming signal to the callee for up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-547">RatioConcealedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="790ec-547">RatioConcealedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="790ec-548">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-548">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-549">Taux moyen d’échantillons masqués générés par la correction audio sur des exemples classiques.</span><span class="sxs-lookup"><span data-stu-id="790ec-549">Average ratio of concealed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-550">RatioStretchedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="790ec-550">RatioStretchedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="790ec-551">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-551">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-552">Taux moyen d’échantillons étirés générés par la correction audio sur des exemples classiques.</span><span class="sxs-lookup"><span data-stu-id="790ec-552">Average ratio of stretched samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-553">RatioCompressedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="790ec-553">RatioCompressedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="790ec-554">décimale (5 ; 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-554">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-555">Taux moyen d’échantillons compressés générés par la correction audio sur des exemples classiques.</span><span class="sxs-lookup"><span data-stu-id="790ec-555">Average ratio of compressed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-556">RoundTrip</span><span class="sxs-lookup"><span data-stu-id="790ec-556">RoundTrip</span></span></p></td>
<td><p><span data-ttu-id="790ec-557">int</span><span class="sxs-lookup"><span data-stu-id="790ec-557">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-558">Durée de l’aller-retour des statistiques RTCP.</span><span class="sxs-lookup"><span data-stu-id="790ec-558">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-559">RoundTripMax</span><span class="sxs-lookup"><span data-stu-id="790ec-559">RoundTripMax</span></span></p></td>
<td><p><span data-ttu-id="790ec-560">int</span><span class="sxs-lookup"><span data-stu-id="790ec-560">int</span></span></p></td>
<td><p><span data-ttu-id="790ec-561">Durée de l’aller-retour maximal pour le flux audio.</span><span class="sxs-lookup"><span data-stu-id="790ec-561">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-562">OverallAvgNetworkMOS</span><span class="sxs-lookup"><span data-stu-id="790ec-562">OverallAvgNetworkMOS</span></span></p></td>
<td><p><span data-ttu-id="790ec-563">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-563">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-564">MOS du réseau à bandes moyenne pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-564">Average wideband Network MOS for the call.</span></span> <span data-ttu-id="790ec-565">Cette métrique dépend du niveau de perte de paquets, de gigue et de codec utilisés.</span><span class="sxs-lookup"><span data-stu-id="790ec-565">This metric depends on the packet loss, jitter, and codec used.</span></span> <span data-ttu-id="790ec-566">La plage est 1,0 à 5,0.</span><span class="sxs-lookup"><span data-stu-id="790ec-566">Range is 1.0 to 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-567">OverallMinNetworkMOS</span><span class="sxs-lookup"><span data-stu-id="790ec-567">OverallMinNetworkMOS</span></span></p></td>
<td><p><span data-ttu-id="790ec-568">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-568">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-569">Débit du réseau à large bande minimum pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-569">Minimum wideband Network MOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-570">SendListenMOS</span><span class="sxs-lookup"><span data-stu-id="790ec-570">SendListenMOS</span></span></p></td>
<td><p><span data-ttu-id="790ec-571">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-571">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-572">Score d’écoute de la bande moyenne prédite pour le son envoyé, avec les caractéristiques de niveau de voix, de niveau de bruit et de périphérique de capture.</span><span class="sxs-lookup"><span data-stu-id="790ec-572">Average predicted wideband Listening MOS score for audio sent, including speech level, noise level and capture device characteristics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-573">SendListenMOSMin</span><span class="sxs-lookup"><span data-stu-id="790ec-573">SendListenMOSMin</span></span></p></td>
<td><p><span data-ttu-id="790ec-574">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-574">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-575">SendListenMOS minimum pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-575">Minimum SendListenMOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-576">RecvListenMOS</span><span class="sxs-lookup"><span data-stu-id="790ec-576">RecvListenMOS</span></span></p></td>
<td><p><span data-ttu-id="790ec-577">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-577">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-578">Score d’écoute de la bande moyenne prédite pour le son reçu du réseau, y compris le niveau de synthèse vocale, le niveau sonore, le codec, les conditions du réseau et les caractéristiques de l’appareil de capture.</span><span class="sxs-lookup"><span data-stu-id="790ec-578">Average predicted wideband Listening MOS score for audio received from the network including speech level, noise level, codec, network conditions and capture device characteristics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-579">RecvListenMOSMin</span><span class="sxs-lookup"><span data-stu-id="790ec-579">RecvListenMOSMin</span></span></p></td>
<td><p><span data-ttu-id="790ec-580">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="790ec-580">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="790ec-581">RecvListenMOS minimum pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-581">Minimum RecvListenMOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="790ec-582">AudioFECUsed</span><span class="sxs-lookup"><span data-stu-id="790ec-582">AudioFECUsed</span></span></p></td>
<td><p><span data-ttu-id="790ec-583">bit</span><span class="sxs-lookup"><span data-stu-id="790ec-583">bit</span></span></p></td>
<td><p><span data-ttu-id="790ec-584">Indique si l’audio FEC a été utilisé pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="790ec-584">Indicates whether audio FEC was used for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="790ec-585">SenderIsCallerPAI</span><span class="sxs-lookup"><span data-stu-id="790ec-585">SenderIsCallerPAI</span></span></p></td>
<td><p><span data-ttu-id="790ec-586">bit</span><span class="sxs-lookup"><span data-stu-id="790ec-586">bit</span></span></p></td>
<td><p><span data-ttu-id="790ec-587">Indique la direction des informations d’identification par le biais de la déclaration p ; 1 signifie que le sens du flux provient de l’appelant vers l’appelant ; 0 : le sens du flux provient de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="790ec-587">Indicates direction of the p-asserted identify information; 1 means the stream direction is from the caller to the callee; 0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="790ec-588">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="790ec-588">


</div>

<span> </span>

</div>

</div>

</span></span></div>

