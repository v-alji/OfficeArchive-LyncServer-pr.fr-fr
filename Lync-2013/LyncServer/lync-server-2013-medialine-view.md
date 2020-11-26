---
title: 'Affichage Lync Server 2013 : MediaLine'
description: 'Affichage Lync Server 2013 : MediaLine'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaLine view
ms:assetid: 132eca13-8913-4218-9eff-4960ced8c3dc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687972(v=OCS.15)
ms:contentKeyID: 49733560
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c61fcc15b46958622e6cddd66427255a6def154
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445945"
---
# <a name="medialine-view-in-lync-server-2013"></a><span data-ttu-id="e78f1-103">Affichage MediaLine dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e78f1-103">MediaLine view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e78f1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e78f1-104">

<span> </span></span></span>

<span data-ttu-id="e78f1-105">_**Dernière modification de la rubrique :** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="e78f1-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="e78f1-106">Le mode MediaLine stocke les informations relatives à chaque ligne multimédia dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="e78f1-106">The MediaLine View stores information about each media line in the database.</span></span> <span data-ttu-id="e78f1-107">Une seule session audio contient généralement une ligne multimédia audio.</span><span class="sxs-lookup"><span data-stu-id="e78f1-107">One audio session typically contains one audio media line.</span></span> <span data-ttu-id="e78f1-108">Une session audio et vidéo (A/V) contient généralement une seule ligne de médias audio et une seule ligne de média vidéo. Toutefois, la session peut contenir deux lignes de média vidéo si un appareil de conférence est utilisé ou si la vue Galerie est utilisée.</span><span class="sxs-lookup"><span data-stu-id="e78f1-108">One audio and video (A/V) session typically contains one audio media line and one video media line; however, the session might contain two video media lines if a conferencing device is used or if Gallery View is used.</span></span> <span data-ttu-id="e78f1-109">Cet affichage a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e78f1-109">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e78f1-110">Colonne</span><span class="sxs-lookup"><span data-stu-id="e78f1-110">Column</span></span></th>
<th><span data-ttu-id="e78f1-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="e78f1-111">Data Type</span></span></th>
<th><span data-ttu-id="e78f1-112">taille</span><span class="sxs-lookup"><span data-stu-id="e78f1-112">details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-113">ConferenceDateTime</span><span class="sxs-lookup"><span data-stu-id="e78f1-113">ConferenceDateTime</span></span></p></td>
<td><p><span data-ttu-id="e78f1-114">DateHeure</span><span class="sxs-lookup"><span data-stu-id="e78f1-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="e78f1-115">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e78f1-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-116">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="e78f1-116">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="e78f1-117">int</span><span class="sxs-lookup"><span data-stu-id="e78f1-117">int</span></span></p></td>
<td><p><span data-ttu-id="e78f1-118">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e78f1-118">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-119">MediaLineLabel</span><span class="sxs-lookup"><span data-stu-id="e78f1-119">MediaLineLabel</span></span></p></td>
<td><p><span data-ttu-id="e78f1-120">tinyint</span><span class="sxs-lookup"><span data-stu-id="e78f1-120">tinyint</span></span></p></td>
<td><p><span data-ttu-id="e78f1-121">Fait référence à partir de la <a href="lync-server-2013-medialine-table.md">table MediaLine dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e78f1-121">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-122">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="e78f1-122">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="e78f1-123">int</span><span class="sxs-lookup"><span data-stu-id="e78f1-123">int</span></span></p></td>
<td><p><span data-ttu-id="e78f1-124">Informations sur le processus de création d’une connexion interactive (ICE) décrite dans les indicateurs bits pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-124">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="e78f1-125">Pour plus d’informations, reportez-vous à la spécification relative au protocole serveur pour le contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="e78f1-125">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-126">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="e78f1-126">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="e78f1-127">int</span><span class="sxs-lookup"><span data-stu-id="e78f1-127">int</span></span></p></td>
<td><p><span data-ttu-id="e78f1-128">Informations sur le processus de création d’une connexion interactive (ICE) décrite dans les indicateurs bits pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-128">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="e78f1-129">Pour plus d’informations, reportez-vous à la spécification relative au protocole serveur pour le contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="e78f1-129">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-130">Sécurité</span><span class="sxs-lookup"><span data-stu-id="e78f1-130">Security</span></span></p></td>
<td><p><span data-ttu-id="e78f1-131">tinyint</span><span class="sxs-lookup"><span data-stu-id="e78f1-131">tinyint</span></span></p></td>
<td><p><span data-ttu-id="e78f1-132">Profil de sécurité en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="e78f1-132">Security profile in use.</span></span> <span data-ttu-id="e78f1-133">0 est aucun, 1 est SRTP, 2 est v1.</span><span class="sxs-lookup"><span data-stu-id="e78f1-133">0 is NONE, 1 is SRTP, 2 is V1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-134">Transport</span><span class="sxs-lookup"><span data-stu-id="e78f1-134">Transport</span></span></p></td>
<td><p><span data-ttu-id="e78f1-135">tinyint</span><span class="sxs-lookup"><span data-stu-id="e78f1-135">tinyint</span></span></p></td>
<td><p><span data-ttu-id="e78f1-136">Type de transport.</span><span class="sxs-lookup"><span data-stu-id="e78f1-136">Transport type.</span></span> <span data-ttu-id="e78f1-137">0 correspond au protocole UDP, 1 au port TCP.</span><span class="sxs-lookup"><span data-stu-id="e78f1-137">0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-138">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="e78f1-138">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="e78f1-139">var (50)</span><span class="sxs-lookup"><span data-stu-id="e78f1-139">var(50)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-140">Adresse IP de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-140">IP address of the caller.</span></span> <span data-ttu-id="e78f1-141">Il peut s’agir d’une adresse IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="e78f1-141">This can be either an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-142">CallerPort</span><span class="sxs-lookup"><span data-stu-id="e78f1-142">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="e78f1-143">int</span><span class="sxs-lookup"><span data-stu-id="e78f1-143">int</span></span></p></td>
<td><p><span data-ttu-id="e78f1-144">Port utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-144">Port used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-145">CallerInside</span><span class="sxs-lookup"><span data-stu-id="e78f1-145">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="e78f1-146">bit</span><span class="sxs-lookup"><span data-stu-id="e78f1-146">bit</span></span></p></td>
<td><p><span data-ttu-id="e78f1-147">Indique si l’appelant figure ou non dans le réseau de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="e78f1-147">Indicates whether or not the caller is inside the organization network.</span></span> <span data-ttu-id="e78f1-148">1 désigne l’appelant au sein du réseau d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="e78f1-148">1 means that the caller is inside the enterprise network.</span></span> <span data-ttu-id="e78f1-149">0 signifie que l’appelant se trouve hors du réseau.</span><span class="sxs-lookup"><span data-stu-id="e78f1-149">0 means that the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-150">CallerMacAddress</span><span class="sxs-lookup"><span data-stu-id="e78f1-150">CallerMacAddress</span></span></p></td>
<td><p><span data-ttu-id="e78f1-151">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e78f1-151">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-152">Adresse MAC de l’interface réseau utilisée par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-152">MAC address of network interface used by caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-153">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="e78f1-153">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="e78f1-154">var (50)</span><span class="sxs-lookup"><span data-stu-id="e78f1-154">var(50)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-155">Adresse IP du service Edge A/V utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-155">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="e78f1-156">Pour plus d’informations, consultez la <a href="lync-server-2013-ipaddress-table.md">table IPAddress dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e78f1-156">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-157">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="e78f1-157">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="e78f1-158">int</span><span class="sxs-lookup"><span data-stu-id="e78f1-158">int</span></span></p></td>
<td><p><span data-ttu-id="e78f1-159">Port utilisé sur le service Edge A/V utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-159">Port used on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-160">CallerReflexiveIPAddr</span><span class="sxs-lookup"><span data-stu-id="e78f1-160">CallerReflexiveIPAddr</span></span></p></td>
<td><p><span data-ttu-id="e78f1-161">var (50)</span><span class="sxs-lookup"><span data-stu-id="e78f1-161">var(50)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-162">Adresse IP de l’appelant communiquée par le service Edge A/V.</span><span class="sxs-lookup"><span data-stu-id="e78f1-162">Caller’s IP address as reported by the A/V Edge service.</span></span> <span data-ttu-id="e78f1-163">Cette adresse peut être différente de l’CallerIPAddr si le client est situé derrière un NAT par exemple.</span><span class="sxs-lookup"><span data-stu-id="e78f1-163">This address may be different that the CallerIPAddr if the client is located behind a NAT for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-164">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="e78f1-164">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="e78f1-165">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e78f1-165">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-166">Nom de l’appareil de capture de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-166">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-167">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="e78f1-167">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="e78f1-168">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e78f1-168">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-169">Nom de l’appareil de rendu de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-169">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-170">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="e78f1-170">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="e78f1-171">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e78f1-171">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-172">Nom du pilote de périphérique de capture de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-172">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-173">CallerRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="e78f1-173">CallerRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="e78f1-174">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e78f1-174">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-175">Nom du pilote de périphérique de rendu de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-175">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-176">CallerWifiDriverDeviceDesc</span><span class="sxs-lookup"><span data-stu-id="e78f1-176">CallerWifiDriverDeviceDesc</span></span></p></td>
<td><p><span data-ttu-id="e78f1-177">varchar (256</span><span class="sxs-lookup"><span data-stu-id="e78f1-177">varchar(256</span></span></p></td>
<td><p><span data-ttu-id="e78f1-178">Description du pilote WiFi de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-178">Caller’s Wifi driver description.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-179">CallerWifiDriverVersion</span><span class="sxs-lookup"><span data-stu-id="e78f1-179">CallerWifiDriverVersion</span></span></p></td>
<td><p><span data-ttu-id="e78f1-180">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e78f1-180">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-181">Version du pilote WiFi de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-181">Caller’s Wifi driver version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-182">CalleeNetworkConnectionDetail</span><span class="sxs-lookup"><span data-stu-id="e78f1-182">CalleeNetworkConnectionDetail</span></span></p></td>
<td><p><span data-ttu-id="e78f1-183">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e78f1-183">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-184">Détails de la connexion réseau de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-184">Details of caller’s network connection.</span></span> <span data-ttu-id="e78f1-185">Pour plus d’informations, voir la <a href="lync-server-2013-networkconnectiondetail-table.md">table NetworkConnectionDetail dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e78f1-185">See the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-186">CallerBssid</span><span class="sxs-lookup"><span data-stu-id="e78f1-186">CallerBssid</span></span></p></td>
<td><p><span data-ttu-id="e78f1-187">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e78f1-187">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-188">Identifiant de l’ensemble de services standard utilisé par les appelants WiFi.</span><span class="sxs-lookup"><span data-stu-id="e78f1-188">Basic Service Set Identifier used by callers WiFi connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-189">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="e78f1-189">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="e78f1-190">bit</span><span class="sxs-lookup"><span data-stu-id="e78f1-190">bit</span></span></p></td>
<td><p><span data-ttu-id="e78f1-191">Indique si l’appelant s’est connecté via un réseau privé virtuel.</span><span class="sxs-lookup"><span data-stu-id="e78f1-191">Indicates whether the caller connected over a virtual private network.</span></span> <span data-ttu-id="e78f1-192">1 est un réseau privé virtuel (VPN), 0 est non VPN.</span><span class="sxs-lookup"><span data-stu-id="e78f1-192">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-193">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="e78f1-193">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="e78f1-194">var (50)</span><span class="sxs-lookup"><span data-stu-id="e78f1-194">var(50)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-195">Adresse IP de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-195">IP address of the callee.</span></span> <span data-ttu-id="e78f1-196">Il peut s’agir d’une adresse IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="e78f1-196">This can be either an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-197">CalleePort</span><span class="sxs-lookup"><span data-stu-id="e78f1-197">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="e78f1-198">int</span><span class="sxs-lookup"><span data-stu-id="e78f1-198">int</span></span></p></td>
<td><p><span data-ttu-id="e78f1-199">Port utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-199">Port used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-200">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="e78f1-200">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="e78f1-201">bit</span><span class="sxs-lookup"><span data-stu-id="e78f1-201">bit</span></span></p></td>
<td><p><span data-ttu-id="e78f1-202">Indique si l’appel est inclus dans le réseau d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="e78f1-202">Indicates whether the callee is inside the enterprise network.</span></span> <span data-ttu-id="e78f1-203">1 signifie que l’appelant se trouve à l’intérieur du réseau d’entreprise, 0 indique que l’appelant se trouve hors du réseau.</span><span class="sxs-lookup"><span data-stu-id="e78f1-203">1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-204">CalleeMacAddress</span><span class="sxs-lookup"><span data-stu-id="e78f1-204">CalleeMacAddress</span></span></p></td>
<td><p><span data-ttu-id="e78f1-205">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e78f1-205">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-206">Adresse MAC de l’interface réseau utilisée par le destinataire.</span><span class="sxs-lookup"><span data-stu-id="e78f1-206">MAC address of network interface used by callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-207">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="e78f1-207">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="e78f1-208">var (50)</span><span class="sxs-lookup"><span data-stu-id="e78f1-208">var(50)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-209">Adresse IP du service Edge A/V utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-209">IP Address of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="e78f1-210">Pour plus d’informations, consultez la <a href="lync-server-2013-ipaddress-table.md">table IPAddress dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e78f1-210">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-211">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="e78f1-211">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="e78f1-212">int</span><span class="sxs-lookup"><span data-stu-id="e78f1-212">int</span></span></p></td>
<td><p><span data-ttu-id="e78f1-213">Port utilisé sur le service Edge A/V utilisé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-213">Port used on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-214">CalleeReflexiveIPAddr</span><span class="sxs-lookup"><span data-stu-id="e78f1-214">CalleeReflexiveIPAddr</span></span></p></td>
<td><p><span data-ttu-id="e78f1-215">var (50)</span><span class="sxs-lookup"><span data-stu-id="e78f1-215">var(50)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-216">Adresse IP du destinataire indiquée par le service Edge A/V.</span><span class="sxs-lookup"><span data-stu-id="e78f1-216">Callee’s IP address as reported by the A/V Edge service.</span></span> <span data-ttu-id="e78f1-217">Cette adresse peut être différente de l’CalleeIPAddr si le client est situé derrière un NAT par exemple.</span><span class="sxs-lookup"><span data-stu-id="e78f1-217">This address may be different that the CalleeIPAddr if the client is located behind a NAT for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-218">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="e78f1-218">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="e78f1-219">var (50)</span><span class="sxs-lookup"><span data-stu-id="e78f1-219">var(50)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-220">Nom de l’appareil de capture du destinataire.</span><span class="sxs-lookup"><span data-stu-id="e78f1-220">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-221">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="e78f1-221">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="e78f1-222">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e78f1-222">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-223">Nom de l’appareil de rendu de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-223">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-224">CalleeCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="e78f1-224">CalleeCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="e78f1-225">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e78f1-225">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-226">Nom du pilote de l’appareil de capture du appelé.</span><span class="sxs-lookup"><span data-stu-id="e78f1-226">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-227">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="e78f1-227">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="e78f1-228">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e78f1-228">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-229">Nom du pilote du périphérique de rendu de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-229">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-230">CalleeWifiDriverDeviceDesc</span><span class="sxs-lookup"><span data-stu-id="e78f1-230">CalleeWifiDriverDeviceDesc</span></span></p></td>
<td><p><span data-ttu-id="e78f1-231">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e78f1-231">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-232">Description du pilote WiFi de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-232">Callee’s Wifi driver description.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-233">CalleeWifiDriverVersion</span><span class="sxs-lookup"><span data-stu-id="e78f1-233">CalleeWifiDriverVersion</span></span></p></td>
<td><p><span data-ttu-id="e78f1-234">varchar (256</span><span class="sxs-lookup"><span data-stu-id="e78f1-234">varchar(256</span></span></p></td>
<td><p><span data-ttu-id="e78f1-235">Version du pilote WiFi de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-235">Callee’s Wifi driver version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-236">CalleeNetworkConnectionDetail</span><span class="sxs-lookup"><span data-stu-id="e78f1-236">CalleeNetworkConnectionDetail</span></span></p></td>
<td><p><span data-ttu-id="e78f1-237">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e78f1-237">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-238">Détails de la connexion réseau du destinataire.</span><span class="sxs-lookup"><span data-stu-id="e78f1-238">Details of callee’s network connection.</span></span> <span data-ttu-id="e78f1-239">Pour plus d’informations, voir la <a href="lync-server-2013-networkconnectiondetail-table.md">table NetworkConnectionDetail dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e78f1-239">See the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-240">CalleeBssid</span><span class="sxs-lookup"><span data-stu-id="e78f1-240">CalleeBssid</span></span></p></td>
<td><p><span data-ttu-id="e78f1-241">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e78f1-241">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-242">Identificateur du jeu de service utilisé par la connexion WiFi de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e78f1-242">Basic Service Set Identifier used by callee’s WiFi connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-243">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="e78f1-243">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="e78f1-244">bit</span><span class="sxs-lookup"><span data-stu-id="e78f1-244">bit</span></span></p></td>
<td><p><span data-ttu-id="e78f1-245">Indique si l’appelant est connecté via un réseau privé virtuel.</span><span class="sxs-lookup"><span data-stu-id="e78f1-245">Indicates whether the callee connected over a virtual private network.</span></span> <span data-ttu-id="e78f1-246">1 est un réseau privé virtuel (VPN), 0 est non VPN.</span><span class="sxs-lookup"><span data-stu-id="e78f1-246">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-247">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="e78f1-247">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="e78f1-248">décimale (3, 2)</span><span class="sxs-lookup"><span data-stu-id="e78f1-248">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-249">La fonction de conversation à bande étroite des sessions audio (en fonction des deux flux audio).</span><span class="sxs-lookup"><span data-stu-id="e78f1-249">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-250">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="e78f1-250">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="e78f1-251">int</span><span class="sxs-lookup"><span data-stu-id="e78f1-251">int</span></span></p></td>
<td><p><span data-ttu-id="e78f1-252">Il s’agit de la bande passante réelle appliquée au flux d’envoi indiqué en fonction de différents paramètres de stratégie (TURN, API, SDP, serveur de stratégie, etc.).</span><span class="sxs-lookup"><span data-stu-id="e78f1-252">This is the actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, etc.).</span></span> <span data-ttu-id="e78f1-253">Cela ne doit pas être confondu avec la bande passante effective, car il peut y avoir une bande passante effective plus faible en fonction de l’estimation de bande passante.</span><span class="sxs-lookup"><span data-stu-id="e78f1-253">This should not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="e78f1-254">Il s’agit essentiellement de la bande passante maximale que le flux d’envoi peut prendre en limitation par l’estimation de bande passante.</span><span class="sxs-lookup"><span data-stu-id="e78f1-254">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-255">AppliedBandwidthSource</span><span class="sxs-lookup"><span data-stu-id="e78f1-255">AppliedBandwidthSource</span></span></p></td>
<td><p><span data-ttu-id="e78f1-256">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e78f1-256">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e78f1-257">Source de la bande passante imposée.</span><span class="sxs-lookup"><span data-stu-id="e78f1-257">Source of the bandwidth cap being imposed.</span></span> <span data-ttu-id="e78f1-258">Il décrit l’emplacement vers lequel la limite de bande passante provient (par exemple, « serveur de stratégie », « activer le serveur » ou « modalité »).</span><span class="sxs-lookup"><span data-stu-id="e78f1-258">It describes where the bandwidth limit is coming from (for example, “Policy Server”, “TURN Server”, or “Modality”).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-259">Appelant</span><span class="sxs-lookup"><span data-stu-id="e78f1-259">Caller</span></span></p></td>
<td><p><span data-ttu-id="e78f1-260">bit</span><span class="sxs-lookup"><span data-stu-id="e78f1-260">bit</span></span></p></td>
<td><p><span data-ttu-id="e78f1-261">Indique si les mesures de l’appelant ont été reçues ; 1 est oui, 0 est non.</span><span class="sxs-lookup"><span data-stu-id="e78f1-261">Indicates whether metrics from the caller were received; 1 is yes, 0 is no.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-262">Appelé</span><span class="sxs-lookup"><span data-stu-id="e78f1-262">Callee</span></span></p></td>
<td><p><span data-ttu-id="e78f1-263">bit</span><span class="sxs-lookup"><span data-stu-id="e78f1-263">bit</span></span></p></td>
<td><p><span data-ttu-id="e78f1-264">Indique si les mesures du destinataire de l’appel ont été reçues. 1 est oui, 0 est non.</span><span class="sxs-lookup"><span data-stu-id="e78f1-264">Indicates whether metrics from the call receiver were received; 1 is yes, 0 is no.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-265">MidCallReport</span><span class="sxs-lookup"><span data-stu-id="e78f1-265">MidCallReport</span></span></p></td>
<td><p><span data-ttu-id="e78f1-266">bit</span><span class="sxs-lookup"><span data-stu-id="e78f1-266">bit</span></span></p></td>
<td><p><span data-ttu-id="e78f1-267">Indique s’il s’agit d’une portion de l’appel ou de l’appel complet.</span><span class="sxs-lookup"><span data-stu-id="e78f1-267">Indicates whether the report is for a portion of the call or for the complete call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-268">ClassifiedPoorCall</span><span class="sxs-lookup"><span data-stu-id="e78f1-268">ClassifiedPoorCall</span></span></p></td>
<td><p><span data-ttu-id="e78f1-269">bit</span><span class="sxs-lookup"><span data-stu-id="e78f1-269">bit</span></span></p></td>
<td><p><span data-ttu-id="e78f1-270">Indique si un appel a été considéré comme un appel médiocre (1) ou comme bon appel (0).</span><span class="sxs-lookup"><span data-stu-id="e78f1-270">Indicates whether a call was classified as a poor call (1) or as a good call (0).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e78f1-271">CallerConnectivityICE</span><span class="sxs-lookup"><span data-stu-id="e78f1-271">CallerConnectivityICE</span></span></p></td>
<td><p><span data-ttu-id="e78f1-272">tinyint</span><span class="sxs-lookup"><span data-stu-id="e78f1-272">tinyint</span></span></p></td>
<td><p><span data-ttu-id="e78f1-273">Indique si l’appelant s’est connecté au réseau via le protocole ICE (établissement de connectivité Internet).</span><span class="sxs-lookup"><span data-stu-id="e78f1-273">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e78f1-274">CalleeConnectivityICE</span><span class="sxs-lookup"><span data-stu-id="e78f1-274">CalleeConnectivityICE</span></span></p></td>
<td><p><span data-ttu-id="e78f1-275">tinyint</span><span class="sxs-lookup"><span data-stu-id="e78f1-275">tinyint</span></span></p></td>
<td><p><span data-ttu-id="e78f1-276">Indique si l’utilisateur s’est connecté au réseau à l’aide du protocole ICE (établissement d’une connexion Internet).</span><span class="sxs-lookup"><span data-stu-id="e78f1-276">Indicates whether the user called connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e78f1-277">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e78f1-277">


</div>

<span> </span>

</div>

</div>

</span></span></div>

