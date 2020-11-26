---
title: 'Lync Server 2013 : Table Session'
description: 'Lync Server 2013 : table de sessions.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Session table
ms:assetid: 7f05529c-794d-41ed-bca4-2e85b87b2dec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398635(v=OCS.15)
ms:contentKeyID: 48184626
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1a52813dfea808253cc934f71a9d4c846c2dbbd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441815"
---
# <a name="session-table-in-lync-server-2013"></a><span data-ttu-id="ce0c1-103">Table Session dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce0c1-103">Session table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ce0c1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ce0c1-104">

<span> </span></span></span>

<span data-ttu-id="ce0c1-105">_**Dernière modification de la rubrique :** 2013-09-09_</span><span class="sxs-lookup"><span data-stu-id="ce0c1-105">_**Topic Last Modified:** 2013-09-09_</span></span>

<span data-ttu-id="ce0c1-106">Chaque enregistrement représente une session qui implique du son, de l’audio et de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-106">Each record represents one session which involves audio or audio and video.</span></span> <span data-ttu-id="ce0c1-107">Il contient des informations générales sur la session.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-107">It contains overall information about the session.</span></span> <span data-ttu-id="ce0c1-108">Une session est définie comme une boîte de dialogue SIP (Session Initiation Protocol) audio ou vidéo entre deux points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-108">A session is defined as an audio or video Session Initiation Protocol (SIP) dialog between two endpoints.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce0c1-109"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="ce0c1-110"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="ce0c1-111"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="ce0c1-112"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce0c1-113"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-113"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-114">DateHeure</span><span class="sxs-lookup"><span data-stu-id="ce0c1-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-115">Principal</span><span class="sxs-lookup"><span data-stu-id="ce0c1-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-116">Fait référence à partir de la <a href="lync-server-2013-dialog-table.md">table boîte de dialogue dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-116">Referenced from the <a href="lync-server-2013-dialog-table.md">Dialog table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0c1-117"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-117"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-118">int</span><span class="sxs-lookup"><span data-stu-id="ce0c1-118">int</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-119">Principal</span><span class="sxs-lookup"><span data-stu-id="ce0c1-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-120">Fait référence à partir de la <a href="lync-server-2013-dialog-table.md">table boîte de dialogue dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-120">Referenced from the <a href="lync-server-2013-dialog-table.md">Dialog table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0c1-121"><strong>ConferenceKey</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-121"><strong>ConferenceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-122">int</span><span class="sxs-lookup"><span data-stu-id="ce0c1-122">int</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-123">Externes</span><span class="sxs-lookup"><span data-stu-id="ce0c1-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-124">Clé de conférence.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-124">Conference key.</span></span> <span data-ttu-id="ce0c1-125">Référence à partir de la <a href="lync-server-2013-conference-table.md">table Conference dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-125">Referenced from the <a href="lync-server-2013-conference-table.md">Conference table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0c1-126"><strong>CorrelationKey</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-126"><strong>CorrelationKey</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-127">int</span><span class="sxs-lookup"><span data-stu-id="ce0c1-127">int</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-128">Externes</span><span class="sxs-lookup"><span data-stu-id="ce0c1-128">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-129">Clé de corrélation.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-129">Correlation key.</span></span> <span data-ttu-id="ce0c1-130">Fait référence à partir de la <a href="lync-server-2013-sessioncorrelation-table.md">table SessionCorrelation dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-130">Referenced from the <a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0c1-131"><strong>DialogCategory</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-131"><strong>DialogCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-132">bit</span><span class="sxs-lookup"><span data-stu-id="ce0c1-132">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ce0c1-133">Catégorie de boîte de dialogue. 0 est Lync Server to Mediation Server leg ; 1 est un serveur de médiation en tronçon de passerelle PSTN.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-133">Dialog category; 0 is Lync Server to Mediation Server leg; 1 is Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0c1-134"><strong>MediationServerBypassFlag</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-134"><strong>MediationServerBypassFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-135">bit</span><span class="sxs-lookup"><span data-stu-id="ce0c1-135">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ce0c1-136">Indicateur indiquant si l’appel a été ignoré ou non.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-136">Flag indicating if the call was bypassed or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0c1-137"><strong>MediaBypassWarningFlag</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-137"><strong>MediaBypassWarningFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-138">int</span><span class="sxs-lookup"><span data-stu-id="ce0c1-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ce0c1-139">Ce champ, s’il est présent, indique pourquoi un appel n’a pas été ignoré, même si les ID de contournement correspondent.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-139">This field, if present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="ce0c1-140">Pour Lync Server, une seule valeur est définie.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-140">For Lync Server, only one value is defined.</span></span></p>
<p><span data-ttu-id="ce0c1-141">0x0001-ID de contournement inconnu pour la carte réseau par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-141">0x0001 – Unknown bypass ID for Default network adapter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0c1-142"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-142"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-143">DateHeure</span><span class="sxs-lookup"><span data-stu-id="ce0c1-143">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ce0c1-144">Heure de début de l’appel.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-144">Call start time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0c1-145"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-145"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-146">DateHeure</span><span class="sxs-lookup"><span data-stu-id="ce0c1-146">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ce0c1-147">Heure de fin de l’appel.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-147">Call end time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0c1-148"><strong>CallerPool</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-148"><strong>CallerPool</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-149">int</span><span class="sxs-lookup"><span data-stu-id="ce0c1-149">int</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-150">Externes</span><span class="sxs-lookup"><span data-stu-id="ce0c1-150">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-151">Le pool de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-151">The pool of the caller.</span></span> <span data-ttu-id="ce0c1-152">Fait référence à partir de la <a href="lync-server-2013-pool-table.md">table de réserve dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-152">Referenced from the <a href="lync-server-2013-pool-table.md">Pool table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0c1-153"><strong>CalleePool</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-153"><strong>CalleePool</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-154">int</span><span class="sxs-lookup"><span data-stu-id="ce0c1-154">int</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-155">Externes</span><span class="sxs-lookup"><span data-stu-id="ce0c1-155">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-156">Le regroupement du destinataire de l’appel.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-156">The pool of the call receiver.</span></span> <span data-ttu-id="ce0c1-157">Fait référence à partir de la <a href="lync-server-2013-pool-table.md">table de réserve dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-157">Referenced from the <a href="lync-server-2013-pool-table.md">Pool table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0c1-158"><strong>CalleePAI</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-158"><strong>CalleePAI</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-159">int</span><span class="sxs-lookup"><span data-stu-id="ce0c1-159">int</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-160">Externes</span><span class="sxs-lookup"><span data-stu-id="ce0c1-160">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-161">URI SIP dans l’identité SIP p-assertion (PAI) du point de terminaison de réception.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-161">SIP URI in the SIP p-asserted identity (PAI) of the receiving endpoint.</span></span> <span data-ttu-id="ce0c1-162">Référence à partir de la <a href="lync-server-2013-user-table.md">table utilisateur dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-162">Referenced from the <a href="lync-server-2013-user-table.md">User table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0c1-163"><strong>CallerURI</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-163"><strong>CallerURI</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-164">int</span><span class="sxs-lookup"><span data-stu-id="ce0c1-164">int</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-165">Externes</span><span class="sxs-lookup"><span data-stu-id="ce0c1-165">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-166">URI de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-166">Caller’s URI.</span></span> <span data-ttu-id="ce0c1-167">Référence à partir de la <a href="lync-server-2013-user-table.md">table utilisateur dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-167">Referenced from the <a href="lync-server-2013-user-table.md">User table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0c1-168"><strong>CallerEndpoint</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-168"><strong>CallerEndpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-169">int</span><span class="sxs-lookup"><span data-stu-id="ce0c1-169">int</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-170">Externes</span><span class="sxs-lookup"><span data-stu-id="ce0c1-170">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-171">Point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-171">Caller’s endpoint.</span></span> <span data-ttu-id="ce0c1-172">Référence à partir de la <a href="lync-server-2013-endpoint-table.md">table de points de terminaison dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-172">Referenced from the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0c1-173"><strong>CallerUserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-173"><strong>CallerUserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-174">bit</span><span class="sxs-lookup"><span data-stu-id="ce0c1-174">bit</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-175">Externes</span><span class="sxs-lookup"><span data-stu-id="ce0c1-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-176">Agent utilisateur de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-176">Caller’s user agent.</span></span> <span data-ttu-id="ce0c1-177">Référence à partir de la <a href="lync-server-2013-useragent-table.md">table UserAgent dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-177">Referenced from the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0c1-178"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-178"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-179">type</span><span class="sxs-lookup"><span data-stu-id="ce0c1-179">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ce0c1-180">Priorité de cet appel.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-180">The priority of this call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0c1-181"><strong>ClassifiedPoorCall</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-181"><strong>ClassifiedPoorCall</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-182">bit</span><span class="sxs-lookup"><span data-stu-id="ce0c1-182">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ce0c1-183">Cette colonne a été déconseillée et n’est pas utilisée dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-183">This column has been deprecated and is not used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="ce0c1-184">À la place, ces informations sont communiquées sur une base de lignes par média.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-184">Instead, this information is reported on a per-media line bases.</span></span> <span data-ttu-id="ce0c1-185">Pour plus d’informations, reportez-vous à la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="ce0c1-185">Refer to the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0c1-186"><strong>CallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-186"><strong>CallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-187">int</span><span class="sxs-lookup"><span data-stu-id="ce0c1-187">int</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-188">Externes</span><span class="sxs-lookup"><span data-stu-id="ce0c1-188">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-189">P-assertion-identité de l’utilisateur qui a placé l’appel.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-189">P-Asserted-Identity of the user who placed the call.</span></span> <span data-ttu-id="ce0c1-190">Le P-assertion-Identity (PAI) est utilisé pour transmettre la véritable identité de l’utilisateur qui a placé l’appel.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-190">The P-Asserted-Identity (PAI) is used to convey the true identity of the user who placed the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0c1-191"><strong>CalleeEndpoint</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-191"><strong>CalleeEndpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-192">int</span><span class="sxs-lookup"><span data-stu-id="ce0c1-192">int</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-193">Externes</span><span class="sxs-lookup"><span data-stu-id="ce0c1-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-194">Point de terminaison ayant reçu l’appel.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-194">Endpoint that received the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce0c1-195"><strong>CalleeUserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-195"><strong>CalleeUserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-196">int</span><span class="sxs-lookup"><span data-stu-id="ce0c1-196">int</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-197">Externes</span><span class="sxs-lookup"><span data-stu-id="ce0c1-197">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-198">Agent utilisateur utilisé par l’utilisateur qui a reçu l’appel.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-198">User agent employed by the user who received the call.</span></span> <span data-ttu-id="ce0c1-199">Les agents utilisateurs représentent l’appareil de point de terminaison client.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-199">User agents represent the client endpoint device.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce0c1-200"><strong>CalleeUri</strong></span><span class="sxs-lookup"><span data-stu-id="ce0c1-200"><strong>CalleeUri</strong></span></span></p></td>
<td><p><span data-ttu-id="ce0c1-201">int</span><span class="sxs-lookup"><span data-stu-id="ce0c1-201">int</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-202">Externes</span><span class="sxs-lookup"><span data-stu-id="ce0c1-202">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ce0c1-203">URI SIP de l’utilisateur qui a reçu l’appel.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-203">SIP URI of the user who received the call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ce0c1-204">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ce0c1-204">


</div>

<span> </span>

</div>

</div>

</span></span></div>

