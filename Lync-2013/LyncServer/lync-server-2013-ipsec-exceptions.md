---
title: Exceptions IPsec de Lync Server 2013
description: Exceptions IPsec de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IPsec exceptions
ms:assetid: 241f1eca-6f2f-44de-90b1-2cb659cbe27c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425719(v=OCS.15)
ms:contentKeyID: 48183627
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b01264171592ec352b778e1aa7eee5861801991
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426724"
---
# <a name="ipsec-exceptions-in-lync-server-2013"></a><span data-ttu-id="b2596-103">Exceptions IPsec dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b2596-103">IPsec exceptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b2596-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b2596-104">

<span> </span></span></span>

<span data-ttu-id="b2596-105">_**Dernière modification de la rubrique :** 2012-06-27_</span><span class="sxs-lookup"><span data-stu-id="b2596-105">_**Topic Last Modified:** 2012-06-27_</span></span>

<span data-ttu-id="b2596-106">Pour les réseaux d’entreprise pour lesquels la sécurité du protocole Internet (IPsec) (voir IETF RFC 4301-4309) a été déployée, le protocole IPsec doit être désactivé sur la plage de ports utilisée pour la remise de la vidéo audio, vidéo et de panorama.</span><span class="sxs-lookup"><span data-stu-id="b2596-106">For enterprise networks where Internet Protocol security (IPsec) (see IETF RFC 4301-4309) has been deployed, IPsec must be disabled over the range of ports used for the delivery of audio, video, and panorama video.</span></span> <span data-ttu-id="b2596-107">Cette recommandation s’explique par la nécessité d’éviter tout retard dans l’affectation des ports multimédias lors de la négociation IPsec.</span><span class="sxs-lookup"><span data-stu-id="b2596-107">The recommendation is motivated by the need to avoid any delay in the allocation of media ports due to IPsec negotiation.</span></span>

<span data-ttu-id="b2596-108">Le tableau suivant présente les paramètres recommandés pour les exceptions IPsec.</span><span class="sxs-lookup"><span data-stu-id="b2596-108">The following table explains the recommended IPsec exception settings.</span></span>

### <a name="recommended-ipsec-exceptions"></a><span data-ttu-id="b2596-109">Exceptions recommandées pour IPsec</span><span class="sxs-lookup"><span data-stu-id="b2596-109">Recommended IPsec Exceptions</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b2596-110">Nom de la règle</span><span class="sxs-lookup"><span data-stu-id="b2596-110">Rule name</span></span></th>
<th><span data-ttu-id="b2596-111">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="b2596-111">Source IP</span></span></th>
<th><span data-ttu-id="b2596-112">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="b2596-112">Destination IP</span></span></th>
<th><span data-ttu-id="b2596-113">Protocole</span><span class="sxs-lookup"><span data-stu-id="b2596-113">Protocol</span></span></th>
<th><span data-ttu-id="b2596-114">Port source</span><span class="sxs-lookup"><span data-stu-id="b2596-114">Source port</span></span></th>
<th><span data-ttu-id="b2596-115">Port de destination</span><span class="sxs-lookup"><span data-stu-id="b2596-115">Destination port</span></span></th>
<th><span data-ttu-id="b2596-116">Besoin d’authentification</span><span class="sxs-lookup"><span data-stu-id="b2596-116">Authentication Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2596-117">Serveur Edge A/V, ports internes/entrants</span><span class="sxs-lookup"><span data-stu-id="b2596-117">A/V Edge Server Internal Inbound</span></span></p></td>
<td><p><span data-ttu-id="b2596-118">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-118">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-119">Serveur Edge A/V - interne</span><span class="sxs-lookup"><span data-stu-id="b2596-119">A/V Edge Server Internal</span></span></p></td>
<td><p><span data-ttu-id="b2596-120">UDP et TCP</span><span class="sxs-lookup"><span data-stu-id="b2596-120">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="b2596-121">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-121">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-122">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-122">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-123">Ne pas authentifier</span><span class="sxs-lookup"><span data-stu-id="b2596-123">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2596-124">Serveur Edge A/V, ports externes/entrants</span><span class="sxs-lookup"><span data-stu-id="b2596-124">A/V Edge Server External Inbound</span></span></p></td>
<td><p><span data-ttu-id="b2596-125">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-125">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-126">Serveur Edge A/V - externe</span><span class="sxs-lookup"><span data-stu-id="b2596-126">A/V Edge Server External</span></span></p></td>
<td><p><span data-ttu-id="b2596-127">UDP et TCP</span><span class="sxs-lookup"><span data-stu-id="b2596-127">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="b2596-128">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-128">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-129">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-129">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-130">Ne pas authentifier</span><span class="sxs-lookup"><span data-stu-id="b2596-130">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2596-131">Serveur Edge A/V, ports internes/sortants</span><span class="sxs-lookup"><span data-stu-id="b2596-131">A/V Edge Server Internal Outbound</span></span></p></td>
<td><p><span data-ttu-id="b2596-132">Serveur Edge A/V - interne</span><span class="sxs-lookup"><span data-stu-id="b2596-132">A/V Edge Server Internal</span></span></p></td>
<td><p><span data-ttu-id="b2596-133">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-133">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-134">&amp;TCP UDP</span><span class="sxs-lookup"><span data-stu-id="b2596-134">UDP &amp; TCP</span></span></p></td>
<td><p><span data-ttu-id="b2596-135">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-135">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-136">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-136">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-137">Ne pas authentifier</span><span class="sxs-lookup"><span data-stu-id="b2596-137">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2596-138">Serveur Edge A/V, ports externes/sortants</span><span class="sxs-lookup"><span data-stu-id="b2596-138">A/V Edge Server External Outbound</span></span></p></td>
<td><p><span data-ttu-id="b2596-139">Serveur Edge A/V - externe</span><span class="sxs-lookup"><span data-stu-id="b2596-139">A/V Edge Server External</span></span></p></td>
<td><p><span data-ttu-id="b2596-140">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-140">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-141">UDP et TCP</span><span class="sxs-lookup"><span data-stu-id="b2596-141">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="b2596-142">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-142">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-143">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-143">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-144">Ne pas authentifier</span><span class="sxs-lookup"><span data-stu-id="b2596-144">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2596-145">Serveur de médiation, ports entrants</span><span class="sxs-lookup"><span data-stu-id="b2596-145">Mediation Server Inbound</span></span></p></td>
<td><p><span data-ttu-id="b2596-146">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-146">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-147">Serveur(s)</span><span class="sxs-lookup"><span data-stu-id="b2596-147">Mediation</span></span></p>
<p><span data-ttu-id="b2596-148">de médiation</span><span class="sxs-lookup"><span data-stu-id="b2596-148">Server(s)</span></span></p></td>
<td><p><span data-ttu-id="b2596-149">UDP et TCP</span><span class="sxs-lookup"><span data-stu-id="b2596-149">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="b2596-150">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-150">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-151">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-151">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-152">Ne pas authentifier</span><span class="sxs-lookup"><span data-stu-id="b2596-152">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2596-153">Serveur de médiation, ports sortants</span><span class="sxs-lookup"><span data-stu-id="b2596-153">Mediation Server Outbound</span></span></p></td>
<td><p><span data-ttu-id="b2596-154">Serveur(s)</span><span class="sxs-lookup"><span data-stu-id="b2596-154">Mediation</span></span></p>
<p><span data-ttu-id="b2596-155">de médiation</span><span class="sxs-lookup"><span data-stu-id="b2596-155">Server(s)</span></span></p></td>
<td><p><span data-ttu-id="b2596-156">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-156">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-157">UDP et TCP</span><span class="sxs-lookup"><span data-stu-id="b2596-157">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="b2596-158">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-158">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-159">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-159">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-160">Ne pas authentifier</span><span class="sxs-lookup"><span data-stu-id="b2596-160">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2596-161">Intendant Conférence entrant</span><span class="sxs-lookup"><span data-stu-id="b2596-161">Conferencing Attendant Inbound</span></span></p></td>
<td><p><span data-ttu-id="b2596-162">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-162">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-163">Serveur frontal exécutant l’Intendant Conférence</span><span class="sxs-lookup"><span data-stu-id="b2596-163">Front End Server running Conferencing Attendant</span></span></p></td>
<td><p><span data-ttu-id="b2596-164">UDP et TCP</span><span class="sxs-lookup"><span data-stu-id="b2596-164">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="b2596-165">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-165">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-166">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-166">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-167">Ne pas authentifier</span><span class="sxs-lookup"><span data-stu-id="b2596-167">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2596-168">Intendant Conférence sortant</span><span class="sxs-lookup"><span data-stu-id="b2596-168">Conferencing Attendant Outbound</span></span></p></td>
<td><p><span data-ttu-id="b2596-169">Serveur frontal exécutant l’Intendant Conférence</span><span class="sxs-lookup"><span data-stu-id="b2596-169">Front End Server running Conferencing Attendant</span></span></p></td>
<td><p><span data-ttu-id="b2596-170">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-170">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-171">UDP et TCP</span><span class="sxs-lookup"><span data-stu-id="b2596-171">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="b2596-172">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-172">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-173">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-173">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-174">Ne pas authentifier</span><span class="sxs-lookup"><span data-stu-id="b2596-174">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2596-175">Serveur de conférence A/V, ports entrants</span><span class="sxs-lookup"><span data-stu-id="b2596-175">A/V Conferencing Inbound</span></span></p></td>
<td><p><span data-ttu-id="b2596-176">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-176">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-177">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="b2596-177">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b2596-178">UDP et TCP</span><span class="sxs-lookup"><span data-stu-id="b2596-178">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="b2596-179">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-179">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-180">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-180">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-181">Ne pas authentifier</span><span class="sxs-lookup"><span data-stu-id="b2596-181">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2596-182">Conférence A/V, ports sortants</span><span class="sxs-lookup"><span data-stu-id="b2596-182">A/V Conferencing Outbound</span></span></p></td>
<td><p><span data-ttu-id="b2596-183">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="b2596-183">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b2596-184">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-184">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-185">UDP et TCP</span><span class="sxs-lookup"><span data-stu-id="b2596-185">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="b2596-186">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-186">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-187">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-187">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-188">Ne pas authentifier</span><span class="sxs-lookup"><span data-stu-id="b2596-188">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2596-189">Exchange, ports entrants</span><span class="sxs-lookup"><span data-stu-id="b2596-189">Exchange Inbound</span></span></p></td>
<td><p><span data-ttu-id="b2596-190">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-190">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-191">Messagerie unifiée Exchange</span><span class="sxs-lookup"><span data-stu-id="b2596-191">Exchange Unified Messaging</span></span></p></td>
<td><p><span data-ttu-id="b2596-192">UDP et TCP</span><span class="sxs-lookup"><span data-stu-id="b2596-192">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="b2596-193">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-193">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-194">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-194">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-195">Ne pas authentifier</span><span class="sxs-lookup"><span data-stu-id="b2596-195">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2596-196">Serveurs de partage d’application, ports entrants</span><span class="sxs-lookup"><span data-stu-id="b2596-196">Application Sharing Servers Inbound</span></span></p></td>
<td><p><span data-ttu-id="b2596-197">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-197">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-198">Serveurs de partage d’application</span><span class="sxs-lookup"><span data-stu-id="b2596-198">Application Sharing Servers</span></span></p></td>
<td><p><span data-ttu-id="b2596-199">TCP</span><span class="sxs-lookup"><span data-stu-id="b2596-199">TCP</span></span></p></td>
<td><p><span data-ttu-id="b2596-200">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-200">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-201">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-201">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-202">Ne pas authentifier</span><span class="sxs-lookup"><span data-stu-id="b2596-202">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2596-203">Serveur de partage d’application, ports sortants</span><span class="sxs-lookup"><span data-stu-id="b2596-203">Application Sharing Server Outbound</span></span></p></td>
<td><p><span data-ttu-id="b2596-204">Serveurs de partage d’application</span><span class="sxs-lookup"><span data-stu-id="b2596-204">Application Sharing Servers</span></span></p></td>
<td><p><span data-ttu-id="b2596-205">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-205">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-206">TCP</span><span class="sxs-lookup"><span data-stu-id="b2596-206">TCP</span></span></p></td>
<td><p><span data-ttu-id="b2596-207">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-207">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-208">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-208">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-209">Ne pas authentifier</span><span class="sxs-lookup"><span data-stu-id="b2596-209">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2596-210">Exchange, ports sortants</span><span class="sxs-lookup"><span data-stu-id="b2596-210">Exchange Outbound</span></span></p></td>
<td><p><span data-ttu-id="b2596-211">Messagerie unifiée Exchange</span><span class="sxs-lookup"><span data-stu-id="b2596-211">Exchange Unified Messaging</span></span></p></td>
<td><p><span data-ttu-id="b2596-212">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-212">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-213">UDP et TCP</span><span class="sxs-lookup"><span data-stu-id="b2596-213">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="b2596-214">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-214">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-215">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-215">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-216">Ne pas authentifier</span><span class="sxs-lookup"><span data-stu-id="b2596-216">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2596-217">Clients</span><span class="sxs-lookup"><span data-stu-id="b2596-217">Clients</span></span></p></td>
<td><p><span data-ttu-id="b2596-218">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-218">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-219">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-219">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-220">UDP</span><span class="sxs-lookup"><span data-stu-id="b2596-220">UDP</span></span></p></td>
<td><p><span data-ttu-id="b2596-221">Plage de ports multimédias définie</span><span class="sxs-lookup"><span data-stu-id="b2596-221">Specified media port range</span></span></p></td>
<td><p><span data-ttu-id="b2596-222">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b2596-222">Any</span></span></p></td>
<td><p><span data-ttu-id="b2596-223">Ne pas authentifier</span><span class="sxs-lookup"><span data-stu-id="b2596-223">Do not authenticate</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b2596-224">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b2596-224">


</div>

<span> </span>

</div>

</div>

</span></span></div>

