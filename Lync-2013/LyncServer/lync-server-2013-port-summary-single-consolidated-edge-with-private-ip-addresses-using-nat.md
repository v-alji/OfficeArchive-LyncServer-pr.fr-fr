---
title: Résumé des ports - Serveur Edge unique consolidé avec adresses IP privées avecla conversion d’adresses réseau
description: Summary de port-Edge unique avec des adresses IP privées utilisant tar.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single consolidated edge with private IP addresses using NAT
ms:assetid: 3c1a389f-5f42-4719-a05b-e0b84aa3eb9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425891(v=OCS.15)
ms:contentKeyID: 48183877
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3fc182b9fbbd24d589feb7f73e3c0086fa23152
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424295"
---
# <a name="port-summary---single-consolidated-edge-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="6cf32-103">Résumé des ports - Serveur Edge unique consolidé avec adresses IP privées avec la conversion d’adresses réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6cf32-103">Port summary - Single consolidated edge with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6cf32-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6cf32-104">

<span> </span></span></span>

<span data-ttu-id="6cf32-105">_**Dernière modification de la rubrique :** 2013-04-03_</span><span class="sxs-lookup"><span data-stu-id="6cf32-105">_**Topic Last Modified:** 2013-04-03_</span></span>

<span data-ttu-id="6cf32-106">La fonctionnalité Lync Server 2013, Edge Server décrite dans cette architecture de scénario est très similaire à celle implémentée dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="6cf32-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="6cf32-107">Le plus notable est le port **5269 sur entrée TCP** pour le protocole XMPP (extensible Messaging and Presence Protocol).</span><span class="sxs-lookup"><span data-stu-id="6cf32-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="6cf32-108">Le serveur Lync Server 2013 déploie éventuellement un proxy XMPP sur le serveur Edge ou le pool de bords et sur le serveur de passerelle XMPP sur le serveur frontal ou le pool frontal.</span><span class="sxs-lookup"><span data-stu-id="6cf32-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="6cf32-109">Outre IPv4, le serveur Edge prend désormais en charge le protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="6cf32-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="6cf32-110">Par souci de clarté, seul le protocole IPv4 est utilisé dans les scénarios.</span><span class="sxs-lookup"><span data-stu-id="6cf32-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="6cf32-111">**Périmètre réseau d’un serveur Edge consolidé unique avec adresse IP privée utilisant tar**</span><span class="sxs-lookup"><span data-stu-id="6cf32-111">**Network Perimeter for a Single Consolidated Edge Server with Private IP Addressing Using NAT**</span></span>

<span data-ttu-id="6cf32-112">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span><span class="sxs-lookup"><span data-stu-id="6cf32-112">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="6cf32-113">Détails sur les ports et protocoles</span><span class="sxs-lookup"><span data-stu-id="6cf32-113">Port and Protocol Details</span></span>

<span data-ttu-id="6cf32-114">Nous vous recommandons d’ouvrir uniquement les ports requis pour la prise en charge des fonctionnalités pour lesquelles vous fournissez un accès externe.</span><span class="sxs-lookup"><span data-stu-id="6cf32-114">We recommend that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="6cf32-115">Pour que l’accès à distance fonctionne pour tous les services Edge, il est obligatoire que le trafic SIP soit autorisé de manière bidirectionnelle, comme indiqué dans le schéma de trafic Edge entrant/sortant.</span><span class="sxs-lookup"><span data-stu-id="6cf32-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="6cf32-116">Autrement dit, la messagerie SIP vers et à partir du service Edge d’accès intervient dans la messagerie instantanée, la présence, les conférences Web, les appels audio/vidéo (A/V) et la Fédération.</span><span class="sxs-lookup"><span data-stu-id="6cf32-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V), and federation.</span></span>

### <a name="firewall-summary-for-single-consolidated-edge-with-private-ip-addresses-using-nat-external-interface"></a><span data-ttu-id="6cf32-117">Résumé du pare-feu pour une périphérie unique consolidée avec des adresses IP privées utilisant tar : interface externe</span><span class="sxs-lookup"><span data-stu-id="6cf32-117">Firewall Summary for Single Consolidated Edge with Private IP Addresses using NAT: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6cf32-118">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="6cf32-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="6cf32-119">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="6cf32-119">Source IP address</span></span></th>
<th><span data-ttu-id="6cf32-120">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="6cf32-120">Destination IP address</span></span></th>
<th><span data-ttu-id="6cf32-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="6cf32-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="6cf32-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="6cf32-123">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-123">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-124">Service proxy XMPP (adresse IP du partage avec service Edge d’accès)</span><span class="sxs-lookup"><span data-stu-id="6cf32-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="6cf32-125">Le service proxy XMPP accepte le trafic de contacts XMPP dans les fédérations de XMPP définies</span><span class="sxs-lookup"><span data-stu-id="6cf32-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf32-126">Accès/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="6cf32-126">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="6cf32-127">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="6cf32-127">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-128">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-128">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-129">Vérification et récupération des certificats</span><span class="sxs-lookup"><span data-stu-id="6cf32-129">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-130">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="6cf32-130">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="6cf32-131">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="6cf32-131">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-132">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-132">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-133">Requête DNS sur TCP</span><span class="sxs-lookup"><span data-stu-id="6cf32-133">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf32-134">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="6cf32-134">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="6cf32-135">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="6cf32-135">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-136">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-136">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-137">Requête DNS via UDP</span><span class="sxs-lookup"><span data-stu-id="6cf32-137">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-138">/TCP/443 d’accès/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="6cf32-138">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="6cf32-139">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-139">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-140">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="6cf32-140">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-141">Trafic SIP client à serveur pour l’accès des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="6cf32-141">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf32-142">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="6cf32-142">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="6cf32-143">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-143">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-144">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="6cf32-144">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-145">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="6cf32-145">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-146">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="6cf32-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="6cf32-147">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="6cf32-147">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-148">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-148">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-149">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="6cf32-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf32-150">PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="6cf32-150">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="6cf32-151">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-151">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-152">Service Edge de conférence Web Edge Server</span><span class="sxs-lookup"><span data-stu-id="6cf32-152">Edge Server Web Conferencing Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-153">Support de conférences Web</span><span class="sxs-lookup"><span data-stu-id="6cf32-153">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-154">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="6cf32-154">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="6cf32-155">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="6cf32-155">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-156">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-156">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-157">Requis pour la Fédération avec des partenaires exécutant Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 et Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6cf32-157">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf32-158">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="6cf32-158">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="6cf32-159">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="6cf32-159">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-160">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-160">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-161">Requis uniquement pour la Fédération avec les partenaires exécutant Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="6cf32-161">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-162">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="6cf32-162">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="6cf32-163">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-163">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-164">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="6cf32-164">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-165">Requis uniquement pour la Fédération avec les partenaires exécutant Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="6cf32-165">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf32-166">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="6cf32-166">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="6cf32-167">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-167">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-168">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="6cf32-168">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-169">Requis uniquement pour la Fédération avec les partenaires exécutant Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="6cf32-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-170">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="6cf32-170">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="6cf32-171">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="6cf32-171">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-172">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-172">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-173">3478 en sortie est utilisé pour déterminer la version de Edge Server avec laquelle Lync Server communique et le trafic multimédia à partir d’un serveur Edge serveur à périphérie.</span><span class="sxs-lookup"><span data-stu-id="6cf32-173">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="6cf32-174">Requis pour la Fédération avec Lync Server 2010, Windows Live Messenger et Office Communications Server 2007 R2, ainsi que le déploiement de plusieurs pools Edge au sein d’une entreprise.</span><span class="sxs-lookup"><span data-stu-id="6cf32-174">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf32-175">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="6cf32-175">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="6cf32-176">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-176">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-177">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="6cf32-177">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-178">STUN/activer la négociation des candidats via UDP/3478</span><span class="sxs-lookup"><span data-stu-id="6cf32-178">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-179">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="6cf32-179">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="6cf32-180">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-180">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-181">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="6cf32-181">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-182">STUN/activer la négociation des candidats via TCP/443</span><span class="sxs-lookup"><span data-stu-id="6cf32-182">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf32-183">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="6cf32-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="6cf32-184">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="6cf32-184">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-185">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-185">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-186">STUN/activer la négociation des candidats via TCP/443</span><span class="sxs-lookup"><span data-stu-id="6cf32-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-single-consolidated-edge-with-private-ip-addresses-using-nat-internal-interface"></a><span data-ttu-id="6cf32-187">Résumé du pare-feu pour une périphérie unique consolidée avec des adresses IP privées utilisant tar : interface interne</span><span class="sxs-lookup"><span data-stu-id="6cf32-187">Firewall Summary for Single Consolidated Edge with Private IP Addresses Using NAT: Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6cf32-188">Protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="6cf32-188">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="6cf32-189">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="6cf32-189">Source IP address</span></span></th>
<th><span data-ttu-id="6cf32-190">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="6cf32-190">Destination IP address</span></span></th>
<th><span data-ttu-id="6cf32-191">Commentaires</span><span class="sxs-lookup"><span data-stu-id="6cf32-191">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-192">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="6cf32-192">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="6cf32-193">Tout (peut être défini comme Standard Edition Server IP, adresse IP du serveur Standard Edition ou adresse IP du pool exécutant le service passerelle XMPP)</span><span class="sxs-lookup"><span data-stu-id="6cf32-193">Any (can be defined as Standard Edition server IP, Standard Edition server IP address, or pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="6cf32-194">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="6cf32-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6cf32-195">Trafic XMPP sortant du service de passerelle XMPP exécuté sur le serveur frontal ou le pool frontal</span><span class="sxs-lookup"><span data-stu-id="6cf32-195">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf32-196">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="6cf32-196">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="6cf32-197">Tout (peut être défini comme directeur, adresse IP du pool de directeurs, adresse IP du serveur frontal ou adresse IP du pool frontal)</span><span class="sxs-lookup"><span data-stu-id="6cf32-197">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="6cf32-198">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="6cf32-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6cf32-199">Trafic SIP sortant (à partir du réalisateur, adresse IP du pool de réalisateurs, adresse IP du serveur frontal ou de la liste frontale) vers l’interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="6cf32-199">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="6cf32-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="6cf32-201">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="6cf32-201">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6cf32-202">Tout (peut être défini comme directeur, adresse IP du pool de directeurs, adresse IP du serveur frontal ou adresse IP du pool frontal)</span><span class="sxs-lookup"><span data-stu-id="6cf32-202">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="6cf32-203">Trafic SIP entrant (adresse IP du pool Directeur, serveur frontal ou adresse IP du pool frontal) à partir de l’interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="6cf32-203">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf32-204">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="6cf32-204">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="6cf32-205">Tout (peut être défini comme adresse IP du serveur frontal ou chaque adresse IP du serveur frontal dans un pool frontal)</span><span class="sxs-lookup"><span data-stu-id="6cf32-205">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="6cf32-206">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="6cf32-206">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6cf32-207">Trafic de conférences Web à partir du serveur frontal ou de chaque serveur frontal, s’il se trouve dans un pool, vers l’interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="6cf32-207">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-208">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="6cf32-208">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="6cf32-209">Tout (peut être défini en tant qu’adresse IP du serveur frontal ou adresse IP du pool frontal ou tout autre appareil de succursale survivant ou succursale Survivable à l’aide de ce serveur Edge)</span><span class="sxs-lookup"><span data-stu-id="6cf32-209">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="6cf32-210">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="6cf32-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6cf32-211">L’authentification des utilisateurs A/V (service d’authentification A/V) à partir du serveur frontal ou de l’adresse IP du pool frontal ou de tout appareil de succursale ou de succursale survivant utilisant ce serveur Edge</span><span class="sxs-lookup"><span data-stu-id="6cf32-211">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf32-212">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="6cf32-212">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="6cf32-213">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-213">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-214">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="6cf32-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6cf32-215">Chemin préféré pour le transfert de média A/V entre des utilisateurs internes et externes, une unité de branchement survivant ou un serveur de succursales survivant</span><span class="sxs-lookup"><span data-stu-id="6cf32-215">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-216">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="6cf32-216">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="6cf32-217">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-217">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-218">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="6cf32-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6cf32-219">Pour le transfert de média A/V entre des utilisateurs internes et externes, une unité de branchement survivant ou un serveur de succursales survivant si la communication UDP ne peut pas être établie, le protocole TCP est utilisé pour le transfert de fichiers et le partage de bureau</span><span class="sxs-lookup"><span data-stu-id="6cf32-219">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf32-220">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="6cf32-220">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="6cf32-221">Tout (peut être défini en tant qu’adresse IP du serveur frontal ou pool contenant la Banque centrale de gestion).</span><span class="sxs-lookup"><span data-stu-id="6cf32-221">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="6cf32-222">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="6cf32-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6cf32-223">Réplication des modifications du magasin de gestion central vers le serveur de périphérie</span><span class="sxs-lookup"><span data-stu-id="6cf32-223">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-224">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="6cf32-224">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="6cf32-225">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-225">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-226">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="6cf32-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6cf32-227">Contrôleur de service de journalisation centralisé à l’aide de Lync Server Management Shell et des applets de ClsAgent.exe ClsController.exe commande de service de journalisation centralisée</span><span class="sxs-lookup"><span data-stu-id="6cf32-227">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf32-228">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="6cf32-228">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="6cf32-229">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-229">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-230">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="6cf32-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6cf32-231">Contrôleur de service de journalisation centralisé à l’aide de Lync Server Management Shell et des applets de ClsAgent.exe ClsController.exe commande de service de journalisation centralisée</span><span class="sxs-lookup"><span data-stu-id="6cf32-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-232">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="6cf32-232">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="6cf32-233">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-233">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-234">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="6cf32-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6cf32-235">Contrôleur de service de journalisation centralisé à l’aide de Lync Server Management Shell et des applets de ClsAgent.exe ClsController.exe commande de service de journalisation centralisée</span><span class="sxs-lookup"><span data-stu-id="6cf32-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="6cf32-236">Résumé du pare-feu pour la Fédération</span><span class="sxs-lookup"><span data-stu-id="6cf32-236">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6cf32-237">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="6cf32-237">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="6cf32-238">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="6cf32-238">Source IP address</span></span></th>
<th><span data-ttu-id="6cf32-239">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="6cf32-239">Destination IP address</span></span></th>
<th><span data-ttu-id="6cf32-240">Remarques</span><span class="sxs-lookup"><span data-stu-id="6cf32-240">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-241">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="6cf32-241">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="6cf32-242">Adresse IP publique du service Edge d’accès</span><span class="sxs-lookup"><span data-stu-id="6cf32-242">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="6cf32-243">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-243">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-244">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="6cf32-244">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="6cf32-245">Résumé du pare-feu-connectivité de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="6cf32-245">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6cf32-246">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="6cf32-246">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="6cf32-247">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="6cf32-247">Source IP address</span></span></th>
<th><span data-ttu-id="6cf32-248">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="6cf32-248">Destination IP address</span></span></th>
<th><span data-ttu-id="6cf32-249">Remarques</span><span class="sxs-lookup"><span data-stu-id="6cf32-249">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-250">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="6cf32-250">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="6cf32-251">Partenaires de connectivité de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="6cf32-251">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="6cf32-252">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="6cf32-252">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-253">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="6cf32-253">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf32-254">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="6cf32-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="6cf32-255">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="6cf32-255">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-256">Partenaires de connectivité de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="6cf32-256">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="6cf32-257">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="6cf32-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-258">/TCP/443 d’accès/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="6cf32-258">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="6cf32-259">Clients</span><span class="sxs-lookup"><span data-stu-id="6cf32-259">Clients</span></span></p></td>
<td><p><span data-ttu-id="6cf32-260">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="6cf32-260">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-261">Trafic SIP client à serveur pour l’accès des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="6cf32-261">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf32-262">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="6cf32-262">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="6cf32-263">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="6cf32-263">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-264">Clients Live Messenger</span><span class="sxs-lookup"><span data-stu-id="6cf32-264">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="6cf32-265">Utilisé pour les sessions A/V avec Windows Live Messenger si la connectivité PIC (Public IM Connectivity) est configurée.</span><span class="sxs-lookup"><span data-stu-id="6cf32-265">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-266">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="6cf32-266">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="6cf32-267">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="6cf32-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-268">Clients Live Messenger</span><span class="sxs-lookup"><span data-stu-id="6cf32-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="6cf32-269">Requis pour la connectivité de messagerie instantanée publique avec Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="6cf32-269">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf32-270">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="6cf32-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="6cf32-271">Clients Live Messenger</span><span class="sxs-lookup"><span data-stu-id="6cf32-271">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="6cf32-272">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="6cf32-272">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6cf32-273">Requis pour la connectivité de messagerie instantanée publique avec Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="6cf32-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="6cf32-274">Résumé du pare-feu pour le protocole extensible de messagerie et de présence</span><span class="sxs-lookup"><span data-stu-id="6cf32-274">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6cf32-275">Protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="6cf32-275">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="6cf32-276">Source (adresse IP)</span><span class="sxs-lookup"><span data-stu-id="6cf32-276">Source (IP address)</span></span></th>
<th><span data-ttu-id="6cf32-277">Destination (adresse IP)</span><span class="sxs-lookup"><span data-stu-id="6cf32-277">Destination (IP address)</span></span></th>
<th><span data-ttu-id="6cf32-278">Commentaires</span><span class="sxs-lookup"><span data-stu-id="6cf32-278">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-279">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="6cf32-279">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="6cf32-280">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-280">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-281">Adresse IP de l’interface du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="6cf32-281">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="6cf32-282">Port de communication serveur à serveur standard pour XMPP.</span><span class="sxs-lookup"><span data-stu-id="6cf32-282">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="6cf32-283">Autorise la communication au proxy de serveur Edge XMPP auprès des partenaires XMPP fédérés</span><span class="sxs-lookup"><span data-stu-id="6cf32-283">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf32-284">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="6cf32-284">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="6cf32-285">Adresse IP de l’interface du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="6cf32-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="6cf32-286">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-286">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-287">Port de communication serveur à serveur standard pour XMPP.</span><span class="sxs-lookup"><span data-stu-id="6cf32-287">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="6cf32-288">Autorise la communication du proxy de serveur Edge XMPP aux partenaires XMPP fédérés</span><span class="sxs-lookup"><span data-stu-id="6cf32-288">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf32-289">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="6cf32-289">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="6cf32-290">Indifférente</span><span class="sxs-lookup"><span data-stu-id="6cf32-290">Any</span></span></p></td>
<td><p><span data-ttu-id="6cf32-291">Chaque adresse IP de l’interface du serveur Edge interne</span><span class="sxs-lookup"><span data-stu-id="6cf32-291">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="6cf32-292">Trafic de XMPP interne depuis la passerelle XMPP du serveur frontal ou du pool frontal vers l’adresse IP interne du serveur Edge ou l’adresse IP interne de chaque membre du pool de périphériques</span><span class="sxs-lookup"><span data-stu-id="6cf32-292">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6cf32-293">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6cf32-293">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

