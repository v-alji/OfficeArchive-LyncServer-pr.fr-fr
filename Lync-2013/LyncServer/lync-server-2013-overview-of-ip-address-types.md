---
title: 'Lync Server 2013 : Vue d’ensemble des types d’adresse IP'
description: 'Lync Server 2013 : vue d’ensemble des types d’adresses IP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of IP address types for Lync Server
ms:assetid: ee9a695f-5cf5-441e-94fb-6adeca50e8d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205363(v=OCS.15)
ms:contentKeyID: 48185759
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 81492b2e006a6f44f6deb78e6a0560f6e319992f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445133"
---
# <a name="overview-of-ip-address-types-for-lync-server-2013"></a><span data-ttu-id="9955e-103">Vue d’ensemble des types d’adresse IP pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9955e-103">Overview of IP address types for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9955e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9955e-104">

<span> </span></span></span>

<span data-ttu-id="9955e-105">_**Dernière modification de la rubrique :** 2013-01-29_</span><span class="sxs-lookup"><span data-stu-id="9955e-105">_**Topic Last Modified:** 2013-01-29_</span></span>

<span data-ttu-id="9955e-106">Trois options s’offrent à vous lorsque vous configurez les adresses IP dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9955e-106">You have three options when configuring IP addresses in Lync Server 2013.</span></span> <span data-ttu-id="9955e-107">Vous pouvez configurer Lync Server 2013 de manière à prendre en charge uniquement le protocole IP version 4 (IPv4), uniquement le protocole IPv4 version 6 (IPv6) ou une combinaison des deux (appelé *pile double*).</span><span class="sxs-lookup"><span data-stu-id="9955e-107">You can configure Lync Server 2013 to support only IP version 4 (IPv4), only IP version 6 (IPv6), or a combination of both (known as a *dual stack*).</span></span> <span data-ttu-id="9955e-108">Chaque type de configuration implique certains problèmes à prendre en considération :</span><span class="sxs-lookup"><span data-stu-id="9955e-108">There are several issues to consider with each type of configuration:</span></span>

  - <span data-ttu-id="9955e-109">**IPv4 uniquement**   Le protocole IPv6 a été créé, car le monde ne dispose pas d’adresses IPv4.</span><span class="sxs-lookup"><span data-stu-id="9955e-109">**IPv4 only**   IPv6 was created because the world is running out of IPv4 addresses.</span></span> <span data-ttu-id="9955e-110">Au final, IPv6 sera entièrement pris en charge partout mais, pour l’instant, de nombreuses sociétés et périphériques avec lesquels votre entreprise peut avoir à communiquer ne prennent pas encore en charge IPv6, et ce pour encore quelque temps.</span><span class="sxs-lookup"><span data-stu-id="9955e-110">Ultimately, IPv6 will be fully supported worldwide, but at this time, many companies and devices that your enterprise might need to communicate with do not yet support IPv6, and may not for some time.</span></span> <span data-ttu-id="9955e-111">Une configuration IPv4 uniquement permet de s’assurer que votre implémentation Lync Server peut communiquer avec la plupart des appareils existants.</span><span class="sxs-lookup"><span data-stu-id="9955e-111">An IPv4-only configuration will help to ensure that your Lync Server implementation can communicate with most existing devices.</span></span>

  - <span data-ttu-id="9955e-112">**IPv6 uniquement**   À l’inverse, une implémentation complète D’ipv6, à ce stade, exclut la communication avec de nombreux appareils existants.</span><span class="sxs-lookup"><span data-stu-id="9955e-112">**IPv6 only**   Conversely, a full IPv6 implementation, at this time, will exclude communication with many existing devices.</span></span>

  - <span data-ttu-id="9955e-113">**Pile double**   La double pile est un réseau sur lequel les adresses IPv4 et IPv6 sont activées.</span><span class="sxs-lookup"><span data-stu-id="9955e-113">**Dual Stack**   Dual stack is a network where both IPv4 and IPv6 addresses are enabled.</span></span> <span data-ttu-id="9955e-114">Cette configuration est prise en charge dans Lync Server 2013, car dans la plupart des cas, le passage de l’intégralité du protocole IPv4 au protocole IPv6 complet nécessite plusieurs années.</span><span class="sxs-lookup"><span data-stu-id="9955e-114">This configuration is supported in Lync Server 2013 because in most cases the transition from full-IPv4 to full-IPv6 will take several years.</span></span>

<span data-ttu-id="9955e-115">Les sections suivantes décrivent la compatibilité entre ces trois configurations pour différentes fonctionnalités de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9955e-115">The following sections outline the compatibility among these three configurations for various Lync Server features.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9955e-p104">La configuration client ou serveur avec IPv6 uniquement n’est prise en charge qu’à des fins de validation ou en laboratoire. La configuration IPv6 uniquement n’est pas prise en charge dans le déploiement de production.</span><span class="sxs-lookup"><span data-stu-id="9955e-p104">Client or server configuration with IPv6 only is supported only for lab or validation purposes. IPv6 only configuration is not supported in the production deployment.</span></span>



</div>

<div>

## <a name="client-registration"></a><span data-ttu-id="9955e-118">Enregistrement client</span><span class="sxs-lookup"><span data-stu-id="9955e-118">Client Registration</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9955e-119">Réseau de point de terminaison client</span><span class="sxs-lookup"><span data-stu-id="9955e-119">Client endpoint network</span></span></th>
<th><span data-ttu-id="9955e-120">Réseau de serveur</span><span class="sxs-lookup"><span data-stu-id="9955e-120">Server network</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9955e-121">IPv4</span><span class="sxs-lookup"><span data-stu-id="9955e-121">IPv4</span></span></p></td>
<td><p><span data-ttu-id="9955e-122">IPv4</span><span class="sxs-lookup"><span data-stu-id="9955e-122">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9955e-123">IPv4</span><span class="sxs-lookup"><span data-stu-id="9955e-123">IPv4</span></span></p></td>
<td><p><span data-ttu-id="9955e-124">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-124">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9955e-125">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-125">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="9955e-126">IPv4</span><span class="sxs-lookup"><span data-stu-id="9955e-126">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9955e-127">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-127">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="9955e-128">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-128">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9955e-129">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-129">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="9955e-130">IPv6</span><span class="sxs-lookup"><span data-stu-id="9955e-130">IPv6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9955e-131">IPv6</span><span class="sxs-lookup"><span data-stu-id="9955e-131">IPv6</span></span></p></td>
<td><p><span data-ttu-id="9955e-132">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-132">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9955e-133">IPv6</span><span class="sxs-lookup"><span data-stu-id="9955e-133">IPv6</span></span></p></td>
<td><p><span data-ttu-id="9955e-134">IPv6</span><span class="sxs-lookup"><span data-stu-id="9955e-134">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="peer-to-peer-client"></a><span data-ttu-id="9955e-135">Client P2P</span><span class="sxs-lookup"><span data-stu-id="9955e-135">Peer-to-Peer Client</span></span>

<span data-ttu-id="9955e-p105">Les communications P2P incluent l’audio, l’audio/vidéo, le partage d’application et le transfert de fichiers. Lorsque les deux clients sont enregistrés, les combinaisons suivantes sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9955e-p105">Peer-to-peer communications include audio, audio/video, application sharing, and file transfer. After both clients have successfully registered, the following combinations are supported.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9955e-138">Point de terminaison client 1</span><span class="sxs-lookup"><span data-stu-id="9955e-138">Client endpoint 1</span></span></th>
<th><span data-ttu-id="9955e-139">Point de terminaison client 2</span><span class="sxs-lookup"><span data-stu-id="9955e-139">Client endpoint 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9955e-140">IPv4</span><span class="sxs-lookup"><span data-stu-id="9955e-140">IPv4</span></span></p></td>
<td><p><span data-ttu-id="9955e-141">IPv4</span><span class="sxs-lookup"><span data-stu-id="9955e-141">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9955e-142">IPv4</span><span class="sxs-lookup"><span data-stu-id="9955e-142">IPv4</span></span></p></td>
<td><p><span data-ttu-id="9955e-143">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-143">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9955e-144">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-144">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="9955e-145">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-145">Dual stack</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9955e-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="9955e-146">IPv6</span></span></p></td>
<td><p><span data-ttu-id="9955e-147">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-147">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9955e-148">IPv6</span><span class="sxs-lookup"><span data-stu-id="9955e-148">IPv6</span></span></p></td>
<td><p><span data-ttu-id="9955e-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="9955e-149">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="conferencing"></a><span data-ttu-id="9955e-150">Téléconférence</span><span class="sxs-lookup"><span data-stu-id="9955e-150">Conferencing</span></span>

<span data-ttu-id="9955e-151">Les conférences incluent l’audio/la vidéo, le partage d’application et la collaboration sur les données (tableau blanc et partage de fichiers).</span><span class="sxs-lookup"><span data-stu-id="9955e-151">Conferencing includes audio/video, application sharing, and data collaboration (whiteboarding and file sharing).</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9955e-152">Réseau de point de terminaison client</span><span class="sxs-lookup"><span data-stu-id="9955e-152">Client endpoint network</span></span></th>
<th><span data-ttu-id="9955e-153">Réseau de serveur</span><span class="sxs-lookup"><span data-stu-id="9955e-153">Server network</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9955e-154">IPv4</span><span class="sxs-lookup"><span data-stu-id="9955e-154">IPv4</span></span></p></td>
<td><p><span data-ttu-id="9955e-155">IPv4</span><span class="sxs-lookup"><span data-stu-id="9955e-155">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9955e-156">IPv4</span><span class="sxs-lookup"><span data-stu-id="9955e-156">IPv4</span></span></p></td>
<td><p><span data-ttu-id="9955e-157">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-157">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9955e-158">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-158">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="9955e-159">IPv4</span><span class="sxs-lookup"><span data-stu-id="9955e-159">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9955e-160">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-160">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="9955e-161">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-161">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9955e-162">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-162">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="9955e-163">IPv6</span><span class="sxs-lookup"><span data-stu-id="9955e-163">IPv6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9955e-164">IPv6</span><span class="sxs-lookup"><span data-stu-id="9955e-164">IPv6</span></span></p></td>
<td><p><span data-ttu-id="9955e-165">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-165">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9955e-166">IPv6</span><span class="sxs-lookup"><span data-stu-id="9955e-166">IPv6</span></span></p></td>
<td><p><span data-ttu-id="9955e-167">IPv6</span><span class="sxs-lookup"><span data-stu-id="9955e-167">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="mediation-serverpstn"></a><span data-ttu-id="9955e-168">Serveur de médiation/RTC</span><span class="sxs-lookup"><span data-stu-id="9955e-168">Mediation Server/PSTN</span></span>

<span data-ttu-id="9955e-169">Lync Server 2013 ne prend pas en charge la dérivation multimédia pour les appels de réseau téléphonique commuté (PSTN) si le trafic provient d’une interface IPv6.</span><span class="sxs-lookup"><span data-stu-id="9955e-169">Lync Server 2013 does not support media bypass for public switched telephone network (PSTN) calls if the traffic is through an IPv6 interface.</span></span> <span data-ttu-id="9955e-170">Si la déviation du trafic multimédia est requise, nous recommandons que la passerelle RTC soit configurée sur IPv4.</span><span class="sxs-lookup"><span data-stu-id="9955e-170">If media bypass is required, we recommend that the PSTN gateway is configured to IPv4.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9955e-171">Interface principale\*</span><span class="sxs-lookup"><span data-stu-id="9955e-171">Primary interface\*</span></span></th>
<th><span data-ttu-id="9955e-172">Interface RTC (sur le serveur de médiation)</span><span class="sxs-lookup"><span data-stu-id="9955e-172">PSTN interface (on Mediation Server)</span></span></th>
<th><span data-ttu-id="9955e-173">Paramètre de passerelle RTC</span><span class="sxs-lookup"><span data-stu-id="9955e-173">PSTN gateway setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9955e-174">IPv4</span><span class="sxs-lookup"><span data-stu-id="9955e-174">IPv4</span></span></p></td>
<td><p><span data-ttu-id="9955e-175">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-175">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="9955e-176">IPv4</span><span class="sxs-lookup"><span data-stu-id="9955e-176">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9955e-177">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-177">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="9955e-178">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-178">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="9955e-179">IPv4</span><span class="sxs-lookup"><span data-stu-id="9955e-179">IPv4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9955e-180">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-180">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="9955e-181">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-181">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="9955e-182">IPv6</span><span class="sxs-lookup"><span data-stu-id="9955e-182">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9955e-183">\* L’interface principale est l’interface qui communique avec les composants serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="9955e-183">\* The primary interface is the interface that communicates with the Lync Server components.</span></span>

</div>

<div>

## <a name="remote-user-peer-to-peer-communications"></a><span data-ttu-id="9955e-184">Communications P2P d’utilisateur distant</span><span class="sxs-lookup"><span data-stu-id="9955e-184">Remote User Peer-to-Peer Communications</span></span>

<span data-ttu-id="9955e-185">Les communications P2P avec des utilisateurs distants incluent la messagerie instantanée, l’audio/vidéo, le partage d’application et le transfert de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9955e-185">Peer-to-peer communications with remote users include instant messaging, audio/video, application sharing, and file transfer.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9955e-186">Réseau d’utilisateur distant</span><span class="sxs-lookup"><span data-stu-id="9955e-186">Remote user network</span></span></th>
<th><span data-ttu-id="9955e-187">Serveur Edge (périmètre externe)</span><span class="sxs-lookup"><span data-stu-id="9955e-187">Edge server (External edge)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9955e-188">IPv4</span><span class="sxs-lookup"><span data-stu-id="9955e-188">IPv4</span></span></p></td>
<td><p><span data-ttu-id="9955e-189">IPv4</span><span class="sxs-lookup"><span data-stu-id="9955e-189">IPv4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9955e-190">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-190">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="9955e-191">IPv4</span><span class="sxs-lookup"><span data-stu-id="9955e-191">IPv4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9955e-192">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-192">Dual stack</span></span></p></td>
<td><p><span data-ttu-id="9955e-193">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-193">Dual stack</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9955e-194">IPv6</span><span class="sxs-lookup"><span data-stu-id="9955e-194">IPv6</span></span></p></td>
<td><p><span data-ttu-id="9955e-195">Double pile</span><span class="sxs-lookup"><span data-stu-id="9955e-195">Dual stack</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9955e-196">IPv6</span><span class="sxs-lookup"><span data-stu-id="9955e-196">IPv6</span></span></p></td>
<td><p><span data-ttu-id="9955e-197">IPv6</span><span class="sxs-lookup"><span data-stu-id="9955e-197">IPv6</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="front-end-pool-and-edge-pool-configuration"></a><span data-ttu-id="9955e-198">Configuration des pools frontal et Edge</span><span class="sxs-lookup"><span data-stu-id="9955e-198">Front End Pool and Edge Pool Configuration</span></span>

<span data-ttu-id="9955e-199">Le tableau suivant montre la matrice de prise en charge entre le pool de serveurs frontal et le pool de serveurs Edge interne.</span><span class="sxs-lookup"><span data-stu-id="9955e-199">The following table shows the support matrix between the Front End Server pool and the internal Edge Server pool.</span></span>

### <a name="front-end-pool-and-edge-pool-internal-edge-matrix"></a><span data-ttu-id="9955e-200">Matrice de pool frontal et de pool Edge (périmètre interne)</span><span class="sxs-lookup"><span data-stu-id="9955e-200">Front End Pool and Edge Pool (Internal Edge) Matrix</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="9955e-201"><strong>Pool Edge : IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="9955e-201"><strong>Edge Pool: IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="9955e-202"><strong>Pool Edge : Double pile</strong></span><span class="sxs-lookup"><span data-stu-id="9955e-202"><strong>Edge Pool: Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="9955e-203"><strong>Pool Edge : IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="9955e-203"><strong>Edge Pool: IPv6</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9955e-204"><strong>Pool frontal : IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="9955e-204"><strong>Front End Pool: IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="9955e-205">Oui</span><span class="sxs-lookup"><span data-stu-id="9955e-205">Yes</span></span></p></td>
<td><p><span data-ttu-id="9955e-206">Oui</span><span class="sxs-lookup"><span data-stu-id="9955e-206">Yes</span></span></p></td>
<td><p><span data-ttu-id="9955e-207">Non</span><span class="sxs-lookup"><span data-stu-id="9955e-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9955e-208"><strong>Pool frontal : Double pile</strong></span><span class="sxs-lookup"><span data-stu-id="9955e-208"><strong>Front End Pool: Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="9955e-209">Oui</span><span class="sxs-lookup"><span data-stu-id="9955e-209">Yes</span></span></p></td>
<td><p><span data-ttu-id="9955e-210">Oui</span><span class="sxs-lookup"><span data-stu-id="9955e-210">Yes</span></span></p></td>
<td><p><span data-ttu-id="9955e-211">Non</span><span class="sxs-lookup"><span data-stu-id="9955e-211">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9955e-212"><strong>Pool frontal : IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="9955e-212"><strong>Front End Pool: IPv6</strong></span></span></p></td>
<td><p><span data-ttu-id="9955e-213">Non</span><span class="sxs-lookup"><span data-stu-id="9955e-213">No</span></span></p></td>
<td><p><span data-ttu-id="9955e-214">Non</span><span class="sxs-lookup"><span data-stu-id="9955e-214">No</span></span></p></td>
<td><p><span data-ttu-id="9955e-215">Oui\*</span><span class="sxs-lookup"><span data-stu-id="9955e-215">Yes\*</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9955e-216">\* Utilisez cette combinaison uniquement dans un environnement Lab.</span><span class="sxs-lookup"><span data-stu-id="9955e-216">\* Use this combination only in a lab environment.</span></span>

<span data-ttu-id="9955e-217">Le tableau ci-dessous représente une matrice des combinaisons d’interfaces Edge internes et externes prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9955e-217">The following table is a matrix of the supported combinations of internal and external edge interfaces.</span></span>

### <a name="edge-pool-internal-edge-and-edge-pool-external-edge-matrix"></a><span data-ttu-id="9955e-218">Matrice de pool Edge (périmètre interne) et de pool Edge (périmètre externe)</span><span class="sxs-lookup"><span data-stu-id="9955e-218">Edge Pool (Internal Edge) and Edge pool (External Edge) Matrix</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="9955e-219"><strong>Pool Edge (périmètre externe) : IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="9955e-219"><strong>Edge Pool (External Edge) : IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="9955e-220"><strong>Pool Edge (périmètre externe) : Double pile</strong></span><span class="sxs-lookup"><span data-stu-id="9955e-220"><strong>Edge Pool (External Edge): Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="9955e-221"><strong>Pool Edge (périmètre externe) : IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="9955e-221"><strong>Edge Pool (External Edge): IPv6</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9955e-222"><strong>Pool Edge (périmètre interne) : IPv4</strong></span><span class="sxs-lookup"><span data-stu-id="9955e-222"><strong>Edge Pool (Internal Edge): IPv4</strong></span></span></p></td>
<td><p><span data-ttu-id="9955e-223">Oui</span><span class="sxs-lookup"><span data-stu-id="9955e-223">Yes</span></span></p></td>
<td><p><span data-ttu-id="9955e-224">Oui</span><span class="sxs-lookup"><span data-stu-id="9955e-224">Yes</span></span></p></td>
<td><p><span data-ttu-id="9955e-225">Non</span><span class="sxs-lookup"><span data-stu-id="9955e-225">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9955e-226"><strong>Pool Edge (périmètre interne) : Double pile</strong></span><span class="sxs-lookup"><span data-stu-id="9955e-226"><strong>Edge Pool (Internal Edge): Dual Stack</strong></span></span></p></td>
<td><p><span data-ttu-id="9955e-227">Non</span><span class="sxs-lookup"><span data-stu-id="9955e-227">No</span></span></p></td>
<td><p><span data-ttu-id="9955e-228">Oui</span><span class="sxs-lookup"><span data-stu-id="9955e-228">Yes</span></span></p></td>
<td><p><span data-ttu-id="9955e-229">Non</span><span class="sxs-lookup"><span data-stu-id="9955e-229">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9955e-230"><strong>Pool Edge (périmètre interne) : IPv6</strong></span><span class="sxs-lookup"><span data-stu-id="9955e-230"><strong>Edge Pool (Internal Edge): IPv6</strong></span></span></p></td>
<td><p><span data-ttu-id="9955e-231">Non</span><span class="sxs-lookup"><span data-stu-id="9955e-231">No</span></span></p></td>
<td><p><span data-ttu-id="9955e-232">Non</span><span class="sxs-lookup"><span data-stu-id="9955e-232">No</span></span></p></td>
<td><p><span data-ttu-id="9955e-233">Oui\*</span><span class="sxs-lookup"><span data-stu-id="9955e-233">Yes\*</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9955e-234">\* Utilisez cette combinaison uniquement dans un environnement Lab.</span><span class="sxs-lookup"><span data-stu-id="9955e-234">\* Use this combination only in a lab environment.</span></span>

</div>

<div>

## <a name="advanced-enterprise-voice-support-for-ipv6"></a><span data-ttu-id="9955e-235">Prise en charge Voix Entreprise pour IPv6 avancée</span><span class="sxs-lookup"><span data-stu-id="9955e-235">Advanced Enterprise Voice Support for IPv6</span></span>

<span data-ttu-id="9955e-236">Les déploiements qui incluent le service Contrôle d’admission des appels (CAC), Enhanced 9-1-1 (E9-1-1), ou la déviation du trafic multimédia doivent être configurés sur une implémentation IPv4 uniquement ou double pile.</span><span class="sxs-lookup"><span data-stu-id="9955e-236">Deployments that include call admission control (CAC), Enhanced 9-1-1 (E9-1-1), or media bypass must be configured as IPv4 only or as a dual-stacked implementation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9955e-237">Dans un déploiement à double empilage, même si un client Lync se connecte à un serveur Lync à l’aide du protocole IPv6, Lync fera tout particulièrement un effort pour mapper une adresse IPv4 appropriée à la prise en charge de E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="9955e-237">In a dual-stacked deployment, even if a Lync client connects to a Lync Server by using IPv6, Lync will make a best effort to map an appropriate IPv4 address to support E9-1-1.</span></span>



</div>

<span data-ttu-id="9955e-238">Le service d’information d’emplacement avec les adresses IPv6 n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9955e-238">Location Information service with IPv6 addresses is not supported.</span></span>

<span data-ttu-id="9955e-p107">La messagerie unifiée Exchange (UM) ne prend pas en charge IPv6. Pour cette fonctionnalité, assurez-vous que la résolution DNS ne renvoie pas une adresse IPv6. L’utilisation d’IPv6 peut entraîner des échecs lorsque les appels sont envoyés vers la messagerie vocale.</span><span class="sxs-lookup"><span data-stu-id="9955e-p107">Exchange Unified Messaging (UM) does not support IPv6. For Exchange UM, be sure that DNS resolution does not return an IPv6 address. Using IPv6 may cause failure when calls are sent to voice mail.</span></span>

</div>

<div>

## <a name="other-lync-server-2013-feature-support-for-ipv6"></a><span data-ttu-id="9955e-242">Autres fonctionnalités de Lync Server 2013 prises en charge pour IPv6</span><span class="sxs-lookup"><span data-stu-id="9955e-242">Other Lync Server 2013 Feature Support for IPv6</span></span>

<span data-ttu-id="9955e-243">Outre les fonctionnalités et composants mentionnés précédemment, Lync Server 2013 prend en charge le protocole IPv6 pour les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="9955e-243">In addition to the features and components mentioned previously, Lync Server 2013 supports IPv6 for the following features:</span></span>

  - <span data-ttu-id="9955e-244">**Conversation permanente**</span><span class="sxs-lookup"><span data-stu-id="9955e-244">**Persistent Chat**</span></span>
    
    <span data-ttu-id="9955e-245">Vous pouvez configurer le protocole IPv6 pour une conversation permanente à l’aide du générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="9955e-245">You configure IPv6 for Persistent Chat by using Topology Builder.</span></span> <span data-ttu-id="9955e-246">Pour plus d’informations sur la configuration d’une conversation permanente, voir la documentation déploiement d’un serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="9955e-246">For details about configuring Persistent Chat, see the Deploying Persistent Chat Server documentation.</span></span>

  - <span data-ttu-id="9955e-247">**Rapports de qualité de l’expérience (QoE) et d’enregistrement des détails des appels**</span><span class="sxs-lookup"><span data-stu-id="9955e-247">**Quality of Experience (QoE) and call detail recording (CDR) reports**</span></span>
    
    <span data-ttu-id="9955e-248">Les rapports de suivi comportent l’adresse IP telle que stockée dans la base de données du serveur de suivi, qu’elle soit de type IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="9955e-248">Monitoring reports include the IP address as it is stored in the Monitoring Server database, whether of type IPv4 or IPv6.</span></span>

<span data-ttu-id="9955e-249"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9955e-249"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

