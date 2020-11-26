---
title: 'Lync Server 2013 : vue de session'
description: 'Lync Server 2013 : vue de session.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Session view
ms:assetid: 49e33f5b-45d0-4146-a5a4-76954d895a98
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688048(v=OCS.15)
ms:contentKeyID: 49733641
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ff4bc4abbd55e073006693d28f092f077698ef75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444790"
---
# <a name="session-view-in-lync-server-2013"></a><span data-ttu-id="da009-103">Affichage de session dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="da009-103">Session view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="da009-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="da009-104">

<span> </span></span></span>

<span data-ttu-id="da009-105">_**Dernière modification de la rubrique :** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="da009-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="da009-106">Le mode session stocke les informations sur les sessions contenant des enregistrements dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="da009-106">The Session View stores information about sessions that have records in the database.</span></span> <span data-ttu-id="da009-107">Cet affichage a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="da009-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="da009-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="da009-108">Column</span></span></th>
<th><span data-ttu-id="da009-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="da009-109">Data Type</span></span></th>
<th><span data-ttu-id="da009-110">Détails</span><span class="sxs-lookup"><span data-stu-id="da009-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da009-111">ConferenceDateTime</span><span class="sxs-lookup"><span data-stu-id="da009-111">ConferenceDateTime</span></span></p></td>
<td><p><span data-ttu-id="da009-112">DateHeure</span><span class="sxs-lookup"><span data-stu-id="da009-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="da009-113">Fait référence à partir de la table MediaLine.</span><span class="sxs-lookup"><span data-stu-id="da009-113">Referenced from the MediaLine Table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da009-114">ConferenceURI</span><span class="sxs-lookup"><span data-stu-id="da009-114">ConferenceURI</span></span></p></td>
<td><p><span data-ttu-id="da009-115">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="da009-115">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="da009-116">URI de conférence s’il s’agit d’une conférence, ou DialogID s’il s’agit d’une session d’égal à égal.</span><span class="sxs-lookup"><span data-stu-id="da009-116">Conference URI if this is a conference, or DialogID if this is a peer-to-peer session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da009-117">Correspondance</span><span class="sxs-lookup"><span data-stu-id="da009-117">Correlation</span></span></p></td>
<td><p><span data-ttu-id="da009-118">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="da009-118">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="da009-119">ID de corrélation de la session.</span><span class="sxs-lookup"><span data-stu-id="da009-119">Correlation ID of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da009-120">DialogCategory</span><span class="sxs-lookup"><span data-stu-id="da009-120">DialogCategory</span></span></p></td>
<td><p><span data-ttu-id="da009-121">bit</span><span class="sxs-lookup"><span data-stu-id="da009-121">bit</span></span></p></td>
<td><p><span data-ttu-id="da009-122">Catégorie de boîte de dialogue. 0 est Lync Server to Mediation Server leg ; 1 est un serveur de médiation en tronçon de passerelle PSTN.</span><span class="sxs-lookup"><span data-stu-id="da009-122">Dialog category; 0 is Lync Server to Mediation Server leg; 1 is Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da009-123">MediationServerBypassFlag</span><span class="sxs-lookup"><span data-stu-id="da009-123">MediationServerBypassFlag</span></span></p></td>
<td><p><span data-ttu-id="da009-124">bit</span><span class="sxs-lookup"><span data-stu-id="da009-124">bit</span></span></p></td>
<td><p><span data-ttu-id="da009-125">Indique si l’appel a été ignoré.</span><span class="sxs-lookup"><span data-stu-id="da009-125">Indicates whether or not the call was bypassed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da009-126">MediaBypassWarningFlag</span><span class="sxs-lookup"><span data-stu-id="da009-126">MediaBypassWarningFlag</span></span></p></td>
<td><p><span data-ttu-id="da009-127">int</span><span class="sxs-lookup"><span data-stu-id="da009-127">int</span></span></p></td>
<td><p><span data-ttu-id="da009-128">Ce champ, s’il est présent, indique pourquoi un appel n’a pas été ignoré, même si les ID de contournement correspondent.</span><span class="sxs-lookup"><span data-stu-id="da009-128">This field, if present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="da009-129">Pour Lync Server, une seule valeur est définie :</span><span class="sxs-lookup"><span data-stu-id="da009-129">For Lync Server, only one value is defined:</span></span></p>
<p><span data-ttu-id="da009-130">0x0001-ID de contournement inconnu pour la carte réseau par défaut</span><span class="sxs-lookup"><span data-stu-id="da009-130">0x0001 – Unknown bypass ID for Default network adapter</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da009-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="da009-131">StartTime</span></span></p></td>
<td><p><span data-ttu-id="da009-132">DateHeure</span><span class="sxs-lookup"><span data-stu-id="da009-132">datetime</span></span></p></td>
<td><p><span data-ttu-id="da009-133">Heure de début de l’appel.</span><span class="sxs-lookup"><span data-stu-id="da009-133">Call start time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da009-134">EndTime</span><span class="sxs-lookup"><span data-stu-id="da009-134">EndTime</span></span></p></td>
<td><p><span data-ttu-id="da009-135">DateHeure</span><span class="sxs-lookup"><span data-stu-id="da009-135">datetime</span></span></p></td>
<td><p><span data-ttu-id="da009-136">Heure de fin de l’appel.</span><span class="sxs-lookup"><span data-stu-id="da009-136">Call end time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da009-137">CallerPool</span><span class="sxs-lookup"><span data-stu-id="da009-137">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="da009-138">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="da009-138">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="da009-139">Nom de domaine complet du pool d’appelant.</span><span class="sxs-lookup"><span data-stu-id="da009-139">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da009-140">CalleePool</span><span class="sxs-lookup"><span data-stu-id="da009-140">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="da009-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="da009-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="da009-142">Nom de domaine complet (FQDN) du pool d’appel.</span><span class="sxs-lookup"><span data-stu-id="da009-142">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da009-143">CallerPAI</span><span class="sxs-lookup"><span data-stu-id="da009-143">CallerPAI</span></span></p></td>
<td><p><span data-ttu-id="da009-144">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="da009-144">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="da009-145">URI d’identité ayant une assertion p d’appelant.</span><span class="sxs-lookup"><span data-stu-id="da009-145">Caller’s p-asserted identity URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da009-146">CalleePAI</span><span class="sxs-lookup"><span data-stu-id="da009-146">CalleePAI</span></span></p></td>
<td><p><span data-ttu-id="da009-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="da009-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="da009-148">URI d’identité affirmée de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="da009-148">Callee’s p-asserted identity URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da009-149">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="da009-149">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="da009-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="da009-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="da009-151">Nom du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="da009-151">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da009-152">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="da009-152">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="da009-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="da009-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="da009-154">Nom du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="da009-154">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da009-155">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="da009-155">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="da009-156">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="da009-156">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="da009-157">Chaîne de l’agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="da009-157">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da009-158">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="da009-158">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="da009-159">type</span><span class="sxs-lookup"><span data-stu-id="da009-159">smallint</span></span></p></td>
<td><p><span data-ttu-id="da009-160">Type de l’agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="da009-160">Type of caller’s user agent.</span></span> <span data-ttu-id="da009-161">Pour plus d’informations, voir la <a href="lync-server-2013-useragent-table.md">table UserAgent dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="da009-161">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da009-162">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="da009-162">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="da009-163">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="da009-163">nvarchar (64)</span></span></p></td>
<td><p><span data-ttu-id="da009-164">Catégorie de l’agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="da009-164">Category of caller’s user agent.</span></span> <span data-ttu-id="da009-165">Pour plus d’informations, reportez-vous <a href="lync-server-2013-useragentdef-table-qoe.md">à la table UserAgentDef (QoE) dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="da009-165">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da009-166">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="da009-166">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="da009-167">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="da009-167">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="da009-168">Chaîne de l’agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="da009-168">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da009-169">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="da009-169">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="da009-170">type</span><span class="sxs-lookup"><span data-stu-id="da009-170">smallint</span></span></p></td>
<td><p><span data-ttu-id="da009-171">Type d’agent utilisateur pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="da009-171">Type of user agent for the callee.</span></span> <span data-ttu-id="da009-172">Pour plus d’informations, voir la <a href="lync-server-2013-useragent-table.md">table UserAgent dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="da009-172">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da009-173">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="da009-173">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="da009-174">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="da009-174">nvarchar (64)</span></span></p></td>
<td><p><span data-ttu-id="da009-175">Catégorie de l’agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="da009-175">User agent category for the callee.</span></span> <span data-ttu-id="da009-176">Pour plus d’informations, reportez-vous <a href="lync-server-2013-useragentdef-table-qoe.md">à la table UserAgentDef (QoE) dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="da009-176">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da009-177">CallerURI</span><span class="sxs-lookup"><span data-stu-id="da009-177">CallerURI</span></span></p></td>
<td><p><span data-ttu-id="da009-178">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="da009-178">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="da009-179">URI de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="da009-179">Caller’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da009-180">CalleeURI</span><span class="sxs-lookup"><span data-stu-id="da009-180">CalleeURI</span></span></p></td>
<td><p><span data-ttu-id="da009-181">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="da009-181">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="da009-182">URI de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="da009-182">Callee’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da009-183">CallPrioirty</span><span class="sxs-lookup"><span data-stu-id="da009-183">CallPrioirty</span></span></p></td>
<td><p><span data-ttu-id="da009-184">int</span><span class="sxs-lookup"><span data-stu-id="da009-184">int</span></span></p></td>
<td><p><span data-ttu-id="da009-185">Priorité de l’appel.</span><span class="sxs-lookup"><span data-stu-id="da009-185">Priority of the call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="da009-186">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="da009-186">


</div>

<span> </span>

</div>

</div>

</span></span></div>

