---
title: 'Lync Server 2013 : Table MediaLine'
description: 'Tableau Lync Server 2013 : MediaLine'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaLine table
ms:assetid: 414b1d63-ae97-4c27-bac0-c9ad0f808ff0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425920(v=OCS.15)
ms:contentKeyID: 48183956
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2acea8e14ba0608d9ebf72a48f888bfc4501fae3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425618"
---
# <a name="medialine-table-in-lync-server-2013"></a><span data-ttu-id="f2ffb-103">Table MediaLine dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2ffb-103">MediaLine table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f2ffb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f2ffb-104">

<span> </span></span></span>

<span data-ttu-id="f2ffb-105">_**Dernière modification de la rubrique :** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="f2ffb-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="f2ffb-106">Chaque enregistrement représente une ligne multimédia.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-106">Each record represents one media line.</span></span> <span data-ttu-id="f2ffb-107">(Une session audio est généralement composée d’une seule ligne de média audio.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-107">(One audio session usually contains one audio media line.</span></span> <span data-ttu-id="f2ffb-108">Une session audio et vidéo (A/V) contient généralement une seule ligne de médias audio et une seule ligne de média vidéo, bien que la session puisse contenir deux lignes de média vidéo si un appareil de conférence est utilisé ou si la vue Galerie est utilisée.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-108">One audio and video (A/V) session usually contains one audio media line and one video media line, although the session might contain two video media lines if a conferencing device is used or if Gallery View is used.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2ffb-109"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="f2ffb-110"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="f2ffb-111"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="f2ffb-112"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-113"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-113"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-114">DateHeure</span><span class="sxs-lookup"><span data-stu-id="f2ffb-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-115">Principal</span><span class="sxs-lookup"><span data-stu-id="f2ffb-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-116">Fait référence à partir de la <a href="lync-server-2013-session-table.md">table de session dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-116">Referenced from the <a href="lync-server-2013-session-table.md">Session table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-117"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-117"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-118">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-118">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-119">Principal</span><span class="sxs-lookup"><span data-stu-id="f2ffb-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-120">Fait référence à partir de la <a href="lync-server-2013-session-table.md">table de session dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-120">Referenced from the <a href="lync-server-2013-session-table.md">Session table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-121"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-121"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-122">tinyint</span><span class="sxs-lookup"><span data-stu-id="f2ffb-122">tinyint</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-123">Principal</span><span class="sxs-lookup"><span data-stu-id="f2ffb-123">Primary</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-124">0 correspond au son principal, 1 correspond à la vidéo principale et 2 correspond à la vidéo panoramique, 3 au partage d’applications et de bureau.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-124">0 is main audio, 1 is main video, and 2 is panoramic video, 3 is Application/Desktop Sharing.</span></span> <span data-ttu-id="f2ffb-125">Cette étiquette doit être unique au sein d’une même session.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-125">This label must be unique within a single session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-126"><strong>ConnectivityIce</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-126"><strong>ConnectivityIce</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-127">tinyint</span><span class="sxs-lookup"><span data-stu-id="f2ffb-127">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f2ffb-128">Cette colonne est présente mais n’est pas utilisée dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-128">This column is present but not used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="f2ffb-129">Les informations relatives à la connectivité utilisée pour une ligne multimédia sont capturées dans les colonnes CallerConnectivityICE et CalleeConnectivityICE.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-129">Information about the connectivity used for a media line is captured in the CallerConnectivityICE and CalleeConnectivityICE columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-130"><strong>CallerIceWarningFlags</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-130"><strong>CallerIceWarningFlags</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-131">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-131">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f2ffb-132">Informations sur le processus de création d’une connexion interactive (ICE) décrite dans les indicateurs de bits.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-132">Information about Interactive Connectivity Establishment (ICE) process described in bits flags.</span></span> <span data-ttu-id="f2ffb-133">Pour plus d’informations, reportez-vous à la <em>spécification qualité de l’expérimentation du protocole serveur</em>, disponible au téléchargement.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-133">For details, refer to the <em>Quality of Experience Monitoring Server Protocol Specification</em>, available for download.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-134"><strong>CalleeIceWarningFlags</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-134"><strong>CalleeIceWarningFlags</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-135">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-135">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f2ffb-136">Identique à CallerIceWarningFlags, mais au côté de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-136">Same as CallerIceWarningFlags, but on the callee side.</span></span> <span data-ttu-id="f2ffb-137">Pour plus d’informations, reportez-vous à la <em>spécification qualité de l’expérimentation du protocole serveur</em>, disponible au téléchargement.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-137">For details, refer to the <em>Quality of Experience Monitoring Server Protocol Specification</em>, available for download.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-138"><strong>Sécurité</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-138"><strong>Security</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-139">tinyint</span><span class="sxs-lookup"><span data-stu-id="f2ffb-139">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f2ffb-140">Profil de sécurité utilisé.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-140">The security profile in use.</span></span> <span data-ttu-id="f2ffb-141">0 est aucun, 1 est SRTP, 2 est v1.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-141">0 is NONE, 1 is SRTP, 2 is V1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-142"><strong>Transport</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-142"><strong>Transport</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-143">tinyint</span><span class="sxs-lookup"><span data-stu-id="f2ffb-143">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f2ffb-144">0 correspond au protocole UDP, 1 au port TCP.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-144">0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-145"><strong>CallerIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-145"><strong>CallerIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-146">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-146">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-147">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-147">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-148">Adresse IP de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-148">IP Address of the caller.</span></span> <span data-ttu-id="f2ffb-149">Pour plus d’informations, consultez la <a href="lync-server-2013-ipaddress-table.md">table IPAddress dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f2ffb-149">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-150"><strong>CallerPort</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-150"><strong>CallerPort</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-151">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-151">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f2ffb-152">Port utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-152">Port used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-153"><strong>CallerSubnet</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-153"><strong>CallerSubnet</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-154">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-154">int</span></span></p></td>
<td><p> <span data-ttu-id="f2ffb-155">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-155">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-156">Sous-réseau de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-156">The subnet of the caller.</span></span> <span data-ttu-id="f2ffb-157">Pour plus d’informations, consultez la <a href="lync-server-2013-ipaddress-table.md">table IPAddress dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f2ffb-157">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-158"><strong>CallerInside</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-158"><strong>CallerInside</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-159">bit</span><span class="sxs-lookup"><span data-stu-id="f2ffb-159">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f2ffb-160">1 désigne l’appelant à l’intérieur du réseau d’entreprise, 0 indique que l’appelant se trouve hors du réseau.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-160">1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-161"><strong>CallerMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-161"><strong>CallerMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-162">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-162">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-163">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-163">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-164">Adresse MAC de l’appelant, référencée à partir de la <a href="lync-server-2013-macaddress-table.md">table MacAddress dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-164">Caller’s mac address, referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-165"><strong>CallerRelayIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-165"><strong>CallerRelayIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-166">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-166">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-167">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-167">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-168">Adresse IP du service Edge A/V du serveur Lync utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-168">IP Address of the Lync Server A/V Edge service used by the caller.</span></span> <span data-ttu-id="f2ffb-169">Pour plus d’informations, consultez la <a href="lync-server-2013-ipaddress-table.md">table IPAddress dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f2ffb-169">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-170"><strong>CallerRelayPort</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-170"><strong>CallerRelayPort</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-171">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-171">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f2ffb-172">Port utilisé par l’appelant sur le service Edge A/V.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-172">Port used on the A/V Edge service by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-173"><strong>CallerCaptureDev</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-173"><strong>CallerCaptureDev</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-174">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-174">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-175">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-176">Appareil de capture utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-176">Capture device used by the caller.</span></span> <span data-ttu-id="f2ffb-177">Fait référence à partir de la <a href="lync-server-2013-device-table.md">table de périphériques dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-177">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-178"><strong>CallerRenderDev</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-178"><strong>CallerRenderDev</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-179">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-179">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-180">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-180">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-181">Périphérique de rendu utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-181">Render device used by caller.</span></span> <span data-ttu-id="f2ffb-182">Fait référence à partir de la <a href="lync-server-2013-device-table.md">table de périphériques dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-182">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-183"><strong>CallerCaptureDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-183"><strong>CallerCaptureDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-184">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-184">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-185">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-185">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-186">Pilote pour l’appareil de capture de l’appelant, référencé à partir de la <a href="lync-server-2013-devicedriver-table.md">table DeviceDriver dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-186">Driver for the caller’s capture device, referenced from the <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-187"><strong>CallerRenderDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-187"><strong>CallerRenderDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-188">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-188">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-189">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-189">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-190">Pilote pour l’appareil de rendu de l’appelant, référencé à partir de la <a href="lync-server-2013-devicedriver-table.md">table DeviceDriver dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-190">Driver for the caller’s render device, referenced from the <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-191"><strong>CallerNetworkConnectionType</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-191"><strong>CallerNetworkConnectionType</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-192">tinyint</span><span class="sxs-lookup"><span data-stu-id="f2ffb-192">tinyint</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-193">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-194">Indique la manière dont l’appelant s’est connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-194">Indicates how the caller connected to the network.</span></span> <span data-ttu-id="f2ffb-195">Les valeurs sont obtenues à partir de la <a href="lync-server-2013-networkconnectiondetail-table.md">table NetworkConnectionDetail dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-195">Values are obtained from the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a>.</span></span> <span data-ttu-id="f2ffb-196">Les valeurs par défaut sont 0 pour une connexion câblée' 1 pour une connexion WiFi ; et 3 pour une connexion Ethernet.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-196">Typical values are 0 for a wired connection’ 1 for a WiFi connection; and 3 for an Ethernet connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-197"><strong>CallerBssid</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-197"><strong>CallerBssid</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-198">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-198">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-199">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-199">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-200">BSSID de l’appelant, si la technologie sans fil est utilisée.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-200">Caller’s BSSID if wireless is used.</span></span> <span data-ttu-id="f2ffb-201">Référencée à partir de la <a href="lync-server-2013-macaddress-table.md">table MacAddress dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-201">Referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-202"><strong>CallerVPN</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-202"><strong>CallerVPN</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-203">bit</span><span class="sxs-lookup"><span data-stu-id="f2ffb-203">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f2ffb-204">Le lien de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-204">The caller's link.</span></span> <span data-ttu-id="f2ffb-205">1 est un réseau privé virtuel (VPN), 0 est non VPN.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-205">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-206"><strong>CallerLinkSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-206"><strong>CallerLinkSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-207">décimale (18, 0)</span><span class="sxs-lookup"><span data-stu-id="f2ffb-207">decimal(18,0)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f2ffb-208">La vitesse de connexion du réseau, en BPS, pour le point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-208">The network link speed, in bps, for the caller's endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-209"><strong>CalleeIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-209"><strong>CalleeIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-210">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-210">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-211">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-211">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-212">Adresse IP du destinataire de l’appel.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-212">IP Address of the call receiver.</span></span> <span data-ttu-id="f2ffb-213">Pour plus d’informations, consultez la <a href="lync-server-2013-ipaddress-table.md">table IPAddress dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f2ffb-213">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-214"><strong>CalleePort</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-214"><strong>CalleePort</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-215">bit</span><span class="sxs-lookup"><span data-stu-id="f2ffb-215">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f2ffb-216">Port utilisé par le destinataire de l’appel.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-216">Port used by the call receiver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-217"><strong>CalleeSubnet</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-217"><strong>CalleeSubnet</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-218">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-218">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-219">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-219">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-220">Sous-réseau de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-220">Subnet of callee.</span></span> <span data-ttu-id="f2ffb-221">Pour plus d’informations, consultez la <a href="lync-server-2013-ipaddress-table.md">table IPAddress dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f2ffb-221">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-222"><strong>CalleeInside</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-222"><strong>CalleeInside</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-223">bit</span><span class="sxs-lookup"><span data-stu-id="f2ffb-223">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f2ffb-224">1 signifie que le destinataire de l’appel se trouve à l’intérieur du réseau d’entreprise, 0 correspond au destinataire de l’appel hors du réseau.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-224">1 means call receiver is inside the enterprise network, 0 means the call receiver is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-225"><strong>CalleeMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-225"><strong>CalleeMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-226">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-226">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-227">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-227">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-228">Adresse MAC du destinataire.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-228">Callee Mac address.</span></span> <span data-ttu-id="f2ffb-229">Fait référence à partir de la <a href="lync-server-2013-macaddress-table.md">table MacAddress dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-229">Referenced from the <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-230"><strong>CalleeRelayIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-230"><strong>CalleeRelayIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-231">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-231">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-232">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-232">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-233">Adresse IP du service Edge A/V utilisée par le destinataire de l’appel.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-233">IP Address of the A/V Edge service used by the call receiver.</span></span> <span data-ttu-id="f2ffb-234">Pour plus d’informations, consultez la <a href="lync-server-2013-ipaddress-table.md">table IPAddress dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f2ffb-234">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-235"><strong>CalleeRelayPort</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-235"><strong>CalleeRelayPort</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-236">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-236">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f2ffb-237">Port utilisé sur le service Edge A/V par le destinataire de l’appel.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-237">Port used on the A/V Edge Service by the call receiver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-238"><strong>CalleeCaptureDev</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-238"><strong>CalleeCaptureDev</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-239">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-239">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-240">externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-240">foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-241">Appareil de capture utilisé par le destinataire de l’appel.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-241">Capture device used by the call receiver.</span></span> <span data-ttu-id="f2ffb-242">Fait référence à partir de la <a href="lync-server-2013-device-table.md">table de périphériques dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-242">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-243"><strong>CalleeRenderDev</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-243"><strong>CalleeRenderDev</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-244">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-244">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-245">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-245">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-246">Périphérique de rendu utilisé par le destinataire de l’appel.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-246">Render device used by the call receiver.</span></span> <span data-ttu-id="f2ffb-247">Fait référence à partir de la <a href="lync-server-2013-device-table.md">table de périphériques dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-247">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-248"><strong>CalleeCaptureDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-248"><strong>CalleeCaptureDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-249">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-249">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-250">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-250">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-251">Pilote de l’appareil de capture du destinataire de l’appel.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-251">Driver for the call receiver’s capture device.</span></span> <span data-ttu-id="f2ffb-252">Référencé à partir de la <a href="lync-server-2013-devicedriver-table.md">table DeviceDriver dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-252">Referenced from <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-253"><strong>CalleeRenderDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-253"><strong>CalleeRenderDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-254">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="f2ffb-254">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-255">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-255">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-256">Pilote de l’appareil de rendu du destinataire de l’appel.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-256">Driver for the call receiver’s render device.</span></span> <span data-ttu-id="f2ffb-257">Référencé à partir de la <a href="lync-server-2013-devicedriver-table.md">table DeviceDriver dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-257">Referenced from <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-258"><strong>CalleeNetworkConnectionType</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-258"><strong>CalleeNetworkConnectionType</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-259">tinyint</span><span class="sxs-lookup"><span data-stu-id="f2ffb-259">tinyint</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-260">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-260">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-261">Indique la manière dont l’appelant s’est connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-261">Indicates how the callee connected to the network.</span></span> <span data-ttu-id="f2ffb-262">Les valeurs sont obtenues à partir de la <a href="lync-server-2013-networkconnectiondetail-table.md">table NetworkConnectionDetail dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-262">Values are obtained from the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a>.</span></span> <span data-ttu-id="f2ffb-263">Les valeurs par défaut sont 0 pour une connexion câblée' 1 pour une connexion WiFi ; et 3 pour une connexion Ethernet.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-263">Typical values are 0 for a wired connection’ 1 for a WiFi connection; and 3 for an Ethernet connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-264"><strong>CalleeBssid</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-264"><strong>CalleeBssid</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-265">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-265">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-266">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-266">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-267">Le BSSID de l’appelant si la technologie sans fil est utilisée.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-267">Callee’s BSSID if wireless is used.</span></span> <span data-ttu-id="f2ffb-268">Référencée à partir de la <a href="lync-server-2013-macaddress-table.md">table MacAddress dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-268">Referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-269"><strong>CalleeVPN</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-269"><strong>CalleeVPN</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-270">bit</span><span class="sxs-lookup"><span data-stu-id="f2ffb-270">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f2ffb-271">Le lien du destinataire de l’appel ; 1 est un réseau privé virtuel (VPN), 0 est non VPN.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-271">The call receiver’s link; 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-272"><strong>CalleeLinkSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-272"><strong>CalleeLinkSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-273">décimale (18, 0)</span><span class="sxs-lookup"><span data-stu-id="f2ffb-273">decimal(18,0)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f2ffb-274">La vitesse de connexion du réseau, en BPS, pour le point de terminaison du destinataire de l’appel.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-274">The network link speed, in bps, for the call receiver’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-275"><strong>ConversationalMOS</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-275"><strong>ConversationalMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-276">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="f2ffb-276">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f2ffb-277">La fonction de conversation à bande étroite des sessions audio (en fonction des deux flux audio).</span><span class="sxs-lookup"><span data-stu-id="f2ffb-277">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-278"><strong>AppliedBandwidthLimit</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-278"><strong>AppliedBandwidthLimit</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-279">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-279">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f2ffb-280">Il s’agit de la bande passante réelle appliquée au flux d’envoi indiqué en fonction de différents paramètres de stratégie (TURN, API, SDP, serveur de stratégie, etc.).</span><span class="sxs-lookup"><span data-stu-id="f2ffb-280">This is the actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="f2ffb-281">Ce problème ne doit pas être confondu avec la bande passante effective, car il peut y avoir une bande passante effective plus faible en fonction de l’estimation de bande passante.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-281">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="f2ffb-282">Il s’agit essentiellement de la bande passante maximale que le flux d’envoi peut prendre en limitation par l’estimation de bande passante.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-282">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-283"><strong>AppliedBandwidthSourceKey</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-283"><strong>AppliedBandwidthSourceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-284">type</span><span class="sxs-lookup"><span data-stu-id="f2ffb-284">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f2ffb-285">Il s’agit de la source de la bande passante qui est imposée.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-285">This is the source of the bandwidth cap being imposed.</span></span> <span data-ttu-id="f2ffb-286">Il décrit l’emplacement à partir duquel la limite de bande passante provient (« serveur de stratégie », « activer le serveur », « modalité », etc.).</span><span class="sxs-lookup"><span data-stu-id="f2ffb-286">It describes where the bandwidth limit is coming from (“Policy Server”, “TURN Server”, “Modality”, and so on).</span></span> <span data-ttu-id="f2ffb-287">Fait référence à partir de la <a href="lync-server-2013-appliedbandwidthsource-table.md">table AppliedBandwidthSource dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-287">Referenced from the <a href="lync-server-2013-appliedbandwidthsource-table.md">AppliedBandwidthSource table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-288"><strong>Appelant</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-288"><strong>Caller</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-289">bit</span><span class="sxs-lookup"><span data-stu-id="f2ffb-289">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f2ffb-290">Indique si les mesures de l’appelant ont été reçues ; 1 est oui, la valeur null est non.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-290">Indicates whether metrics from the caller were received; 1 is yes, a null value is no.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-291"><strong>Appelé</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-291"><strong>Callee</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-292">bit</span><span class="sxs-lookup"><span data-stu-id="f2ffb-292">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f2ffb-293">Indique si les mesures du destinataire de l’appel ont été reçues. 1 est oui, la valeur null est non.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-293">Indicates whether metrics from the call receiver were received; 1 is yes, a null value is no.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-294"><strong>MidCallReport</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-294"><strong>MidCallReport</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-295">bit</span><span class="sxs-lookup"><span data-stu-id="f2ffb-295">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f2ffb-296">Indique si l’état correspond à une partie de la session ou à la session complète.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-296">Indicates whether the report is for a portion of the session or for the complete session.</span></span></p>
<p><span data-ttu-id="f2ffb-297">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-297">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-298"><strong>ClassifiedPoorCall</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-298"><strong>ClassifiedPoorCall</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-299">bit</span><span class="sxs-lookup"><span data-stu-id="f2ffb-299">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f2ffb-300">Indique si un appel a été considéré comme un appel médiocre (valeur de 1) ou comme bon appel (0).</span><span class="sxs-lookup"><span data-stu-id="f2ffb-300">Indicates whether a call was classified as a poor call (value of 1) or as a good call (0).</span></span></p>
<p><span data-ttu-id="f2ffb-301">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-301">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-302"><strong>CallerConnectivityICE</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-302"><strong>CallerConnectivityICE</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-303">Sa</span><span class="sxs-lookup"><span data-stu-id="f2ffb-303">tinyInt</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f2ffb-304">Indique si l’appelant s’est connecté au réseau via le protocole ICE (établissement de connectivité Internet).</span><span class="sxs-lookup"><span data-stu-id="f2ffb-304">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p>
<p><span data-ttu-id="f2ffb-305">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-305">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-306"><strong>CalleeConnectivityICE</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-306"><strong>CalleeConnectivityICE</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-307">tinyint</span><span class="sxs-lookup"><span data-stu-id="f2ffb-307">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f2ffb-308">Indique si l’appelant s’est connecté au réseau via le protocole ICE (établissement de connectivité Internet).</span><span class="sxs-lookup"><span data-stu-id="f2ffb-308">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p>
<p><span data-ttu-id="f2ffb-309">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-309">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-310"><strong>CallerReflexiveLocalIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-310"><strong>CallerReflexiveLocalIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-311">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-311">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-312">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-312">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-313">Adresse IP réflexive de l’utilisateur qui a placé l’appel.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-313">Reflexive IP address of the user who placed the call.</span></span> <span data-ttu-id="f2ffb-314">Dans les organisations qui utilisent la traduction d’adresses réseau (NAT), l’adresse IP réflexive est l’adresse IP du serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-314">In organizations that use NAT (network address translation), the reflexive IP address is the IP address of the proxy server.</span></span></p>
<p><span data-ttu-id="f2ffb-315">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-315">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-316"><strong>CallerWiFiDriverDevicesDesc</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-316"><strong>CallerWiFiDriverDevicesDesc</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-317">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-317">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-318">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-318">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-319">Description de l’appareil pour le pilote WiFi utilisé par l’utilisateur qui a placé l’appel.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-319">Device description for the WiFi driver employed by the user who placed the call.</span></span></p>
<p><span data-ttu-id="f2ffb-320">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-320">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-321"><strong>CallerWiFiDriverVersion</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-321"><strong>CallerWiFiDriverVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-322">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-322">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-323">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-323">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-324">Numéro de version du pilote WiFi utilisé par l’utilisateur qui a placé l’appel.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-324">Version number for the WiFi driver employed by the user who placed the call.</span></span></p>
<p><span data-ttu-id="f2ffb-325">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-325">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-326"><strong>CalleReflexiveLocalIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-326"><strong>CalleReflexiveLocalIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-327">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-327">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-328">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-328">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-329">Adresse IP réflexive de l’utilisateur qui a reçu l’appel.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-329">Reflexive IP address of the user who received the call.</span></span> <span data-ttu-id="f2ffb-330">Dans les organisations qui utilisent la traduction d’adresses réseau (NAT), l’adresse IP réflexive est l’adresse IP du serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-330">In organizations that use NAT (network address translation), the reflexive IP address is the IP address of the proxy server.</span></span></p>
<p><span data-ttu-id="f2ffb-331">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-331">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2ffb-332"><strong>CalleeWiFiDriverDevicesDesc</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-332"><strong>CalleeWiFiDriverDevicesDesc</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-333">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-333">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-334">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-334">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-335">Description de l’appareil pour le pilote WiFi utilisé par l’utilisateur qui a reçu l’appel.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-335">Device description for the WiFi driver employed by the user who received the call.</span></span></p>
<p><span data-ttu-id="f2ffb-336">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-336">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2ffb-337"><strong>CalleeWiFiDriverVersion</strong></span><span class="sxs-lookup"><span data-stu-id="f2ffb-337"><strong>CalleeWiFiDriverVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="f2ffb-338">int</span><span class="sxs-lookup"><span data-stu-id="f2ffb-338">int</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-339">Externes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-339">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f2ffb-340">Numéro de version du pilote WiFi utilisé par l’utilisateur qui a reçu l’appel.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-340">Version number for the WiFi driver employed by the user who received the call.</span></span></p>
<p><span data-ttu-id="f2ffb-341">Cette colonne a été introduite dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-341">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f2ffb-342">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f2ffb-342">


</div>

<span> </span>

</div>

</div>

</span></span></div>

