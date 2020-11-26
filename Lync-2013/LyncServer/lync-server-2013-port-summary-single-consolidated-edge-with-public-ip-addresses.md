---
title: Résumé des ports - Serveur Edge unique consolidé avec adresses IP publiques
description: Summary de port-Edge unique avec adresse IP publique.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single consolidated edge with public IP addresses
ms:assetid: 28407acc-8b92-4f78-875c-fd6b4323b602
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204756(v=OCS.15)
ms:contentKeyID: 48183685
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82ab2d89404fb174994d8e5b798f64bb68768326
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424255"
---
# <a name="port-summary---single-consolidated-edge-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="0651c-103">Résumé des ports - Serveur Edge unique consolidé avec adresses IP publiques dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0651c-103">Port summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0651c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0651c-104">

<span> </span></span></span>

<span data-ttu-id="0651c-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="0651c-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="0651c-106">La fonctionnalité Lync Server 2013, Edge Server décrite dans cette architecture de scénario est très similaire à celle implémentée dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="0651c-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="0651c-107">Le plus notable est le port **5269 sur entrée TCP** pour le protocole XMPP (extensible Messaging and Presence Protocol).</span><span class="sxs-lookup"><span data-stu-id="0651c-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="0651c-108">Le serveur Lync Server 2013 déploie éventuellement un proxy XMPP sur le serveur Edge ou le pool de bords et sur le serveur de passerelle XMPP sur le serveur frontal ou le pool frontal.</span><span class="sxs-lookup"><span data-stu-id="0651c-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span> <span data-ttu-id="0651c-109">Les informations de planification du proxy inverse et de la Fédération s’exécutent dans [les scénarios de proxy inverse dans Lync server 2013](lync-server-2013-scenarios-for-reverse-proxy.md) et la [planification de la Fédération SIP, de la Fédération et de la messagerie instantanée publique dans les sections de Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="0651c-109">Planning information for the reverse proxy and federation are found in [Scenarios for reverse proxy in Lync Server 2013](lync-server-2013-scenarios-for-reverse-proxy.md) and [Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md) sections, respectively.</span></span>

<span data-ttu-id="0651c-110">Outre IPv4, le serveur Edge prend désormais en charge le protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="0651c-110">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="0651c-111">Par souci de clarté, seul le protocole IPv4 est utilisé dans les scénarios.</span><span class="sxs-lookup"><span data-stu-id="0651c-111">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="0651c-112">**Réseau de périmètre d’entreprise pour une seule périphérie consolidée avec un adresse IP publique**</span><span class="sxs-lookup"><span data-stu-id="0651c-112">**Enterprise perimeter network for single consolidated edge with public IP addressing**</span></span>

<span data-ttu-id="0651c-113">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span><span class="sxs-lookup"><span data-stu-id="0651c-113">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="0651c-114">Détails sur les ports et protocoles</span><span class="sxs-lookup"><span data-stu-id="0651c-114">Port and Protocol Details</span></span>

<span data-ttu-id="0651c-115">Nous vous recommandons d’ouvrir uniquement les ports requis pour la prise en charge des fonctionnalités pour lesquelles vous fournissez un accès externe.</span><span class="sxs-lookup"><span data-stu-id="0651c-115">We recommend that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="0651c-116">Pour que l’accès à distance fonctionne pour tout service Edge, il est obligatoire que le trafic SIP soit acheminé de manière bidirectionnelle, comme le montre la figure dans le trafic de périphérie entrant/sortant.</span><span class="sxs-lookup"><span data-stu-id="0651c-116">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bidirectionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="0651c-117">Autrement dit, la messagerie SIP vers et à partir du service Edge d’accès intervient dans les fonctionnalités de messagerie instantanée, de présence, de conférence Web, audio/vidéo (A/V) et de Fédération.</span><span class="sxs-lookup"><span data-stu-id="0651c-117">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-single-consolidated-edge-with-public-ip-addresses-external-interface"></a><span data-ttu-id="0651c-118">Résumé du pare-feu pour une périphérie unique consolidée avec des adresses IP publiques : interface externe</span><span class="sxs-lookup"><span data-stu-id="0651c-118">Firewall Summary for Single Consolidated Edge with Public IP Addresses: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0651c-119">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="0651c-119">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="0651c-120">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="0651c-120">Source IP address</span></span></th>
<th><span data-ttu-id="0651c-121">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="0651c-121">Destination IP address</span></span></th>
<th><span data-ttu-id="0651c-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="0651c-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0651c-123">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="0651c-123">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="0651c-124">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-124">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-125">Service proxy XMPP (adresse IP du partage avec service Edge d’accès)</span><span class="sxs-lookup"><span data-stu-id="0651c-125">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="0651c-126">Le service proxy XMPP accepte le trafic de contacts XMPP dans les fédérations de XMPP définies</span><span class="sxs-lookup"><span data-stu-id="0651c-126">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0651c-127">Accès/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="0651c-127">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="0651c-128">Adresse IP publique du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="0651c-128">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-129">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-129">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-130">Vérification et récupération des certificats</span><span class="sxs-lookup"><span data-stu-id="0651c-130">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0651c-131">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="0651c-131">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="0651c-132">Adresse IP publique du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="0651c-132">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-133">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-133">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-134">Requête DNS sur TCP</span><span class="sxs-lookup"><span data-stu-id="0651c-134">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0651c-135">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="0651c-135">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="0651c-136">Adresse IP publique du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="0651c-136">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-137">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-137">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-138">Requête DNS via UDP</span><span class="sxs-lookup"><span data-stu-id="0651c-138">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0651c-139">/TCP/443 d’accès/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="0651c-139">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="0651c-140">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-140">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-141">Adresse IP publique du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="0651c-141">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-142">Trafic SIP client à serveur pour l’accès des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="0651c-142">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0651c-143">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="0651c-143">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="0651c-144">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-144">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-145">Adresse IP publique du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="0651c-145">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-146">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="0651c-146">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0651c-147">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="0651c-147">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="0651c-148">Adresse IP publique du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="0651c-148">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-149">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-149">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-150">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="0651c-150">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0651c-151">PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="0651c-151">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="0651c-152">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-152">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-153">Adresse IP publique du service Edge Conferencing Server Web</span><span class="sxs-lookup"><span data-stu-id="0651c-153">Edge Server Web Conferencing Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-154">Support de conférences Web</span><span class="sxs-lookup"><span data-stu-id="0651c-154">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0651c-155">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="0651c-155">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="0651c-156">Adresse IP publique du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="0651c-156">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-157">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-157">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-158">Requis pour la Fédération avec des partenaires exécutant Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 et Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0651c-158">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0651c-159">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="0651c-159">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="0651c-160">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="0651c-160">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-161">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-161">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-162">Requis uniquement pour la Fédération avec les partenaires exécutant Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="0651c-162">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0651c-163">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="0651c-163">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="0651c-164">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-164">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-165">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="0651c-165">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-166">Requis uniquement pour la Fédération avec les partenaires exécutant Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0651c-166">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0651c-167">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="0651c-167">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="0651c-168">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-168">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-169">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="0651c-169">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-170">Requis uniquement pour la Fédération avec les partenaires exécutant Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0651c-170">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0651c-171">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="0651c-171">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="0651c-172">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="0651c-172">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-173">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-173">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-174">3478 en sortie est utilisé pour déterminer la version de Edge Server avec laquelle Lync Server communique et le trafic multimédia à partir d’un serveur Edge serveur à périphérie.</span><span class="sxs-lookup"><span data-stu-id="0651c-174">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="0651c-175">Requis pour la Fédération avec Lync Server 2010, Windows Live Messenger et Office Communications Server 2007 R2, ainsi que le déploiement de plusieurs pools Edge au sein d’une entreprise.</span><span class="sxs-lookup"><span data-stu-id="0651c-175">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0651c-176">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="0651c-176">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="0651c-177">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-177">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-178">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="0651c-178">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-179">STUN/activer la négociation des candidats via UDP/3478</span><span class="sxs-lookup"><span data-stu-id="0651c-179">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0651c-180">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="0651c-180">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="0651c-181">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-181">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-182">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="0651c-182">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-183">STUN/activer la négociation des candidats via TCP/443</span><span class="sxs-lookup"><span data-stu-id="0651c-183">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0651c-184">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="0651c-184">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="0651c-185">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="0651c-185">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-186">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-186">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-187">STUN/activer la négociation des candidats via TCP/443</span><span class="sxs-lookup"><span data-stu-id="0651c-187">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-single-consolidated-edge-with-public-ip-addresses-internal-interface"></a><span data-ttu-id="0651c-188">Résumé du pare-feu pour une périphérie unique consolidée avec des adresses IP publiques : interface interne</span><span class="sxs-lookup"><span data-stu-id="0651c-188">Firewall Summary for Single Consolidated Edge with Public IP Addresses: Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0651c-189">Protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="0651c-189">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="0651c-190">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="0651c-190">Source IP address</span></span></th>
<th><span data-ttu-id="0651c-191">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="0651c-191">Destination IP address</span></span></th>
<th><span data-ttu-id="0651c-192">Commentaires</span><span class="sxs-lookup"><span data-stu-id="0651c-192">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0651c-193">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="0651c-193">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="0651c-194">Tout (peut être défini comme Standard Edition Server IP, adresse IP du serveur Standard Edition ou adresse IP du pool exécutant le service passerelle XMPP)</span><span class="sxs-lookup"><span data-stu-id="0651c-194">Any (can be defined as Standard Edition server IP, Standard Edition server IP address, or pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="0651c-195">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="0651c-195">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0651c-196">Trafic XMPP sortant du service de passerelle XMPP exécuté sur le serveur frontal ou le pool frontal</span><span class="sxs-lookup"><span data-stu-id="0651c-196">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0651c-197">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="0651c-197">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="0651c-198">Tout (peut être défini comme directeur, adresse IP du pool de directeurs, adresse IP du serveur frontal ou adresse IP du pool frontal)</span><span class="sxs-lookup"><span data-stu-id="0651c-198">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="0651c-199">Adresse IP du serveur Edge ou pool qui contient l’interface interne</span><span class="sxs-lookup"><span data-stu-id="0651c-199">Edge Server IP, or pool that holds the internal interface</span></span></p></td>
<td><p><span data-ttu-id="0651c-200">Trafic SIP sortant (à partir du réalisateur, adresse IP du pool de réalisateurs, adresse IP du serveur frontal ou de la liste frontale) vers l’interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="0651c-200">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0651c-201">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="0651c-201">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="0651c-202">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="0651c-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0651c-203">Tout (peut être défini comme directeur, adresse IP du pool de directeurs, serveur frontal ou adresse du pool frontal)</span><span class="sxs-lookup"><span data-stu-id="0651c-203">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool address)</span></span></p></td>
<td><p><span data-ttu-id="0651c-204">Trafic SIP entrant (adresse IP du pool Directeur, serveur frontal ou adresse IP du pool frontal) à partir de l’interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="0651c-204">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0651c-205">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="0651c-205">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="0651c-206">Tout (peut être défini comme adresse IP du serveur frontal ou chaque adresse IP du serveur frontal dans un pool frontal)</span><span class="sxs-lookup"><span data-stu-id="0651c-206">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="0651c-207">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="0651c-207">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0651c-208">Trafic de conférences Web à partir du serveur frontal ou de chaque serveur frontal, s’il se trouve dans un pool, vers l’interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="0651c-208">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0651c-209">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="0651c-209">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="0651c-210">Tout (peut être défini en tant qu’adresse IP du serveur frontal ou adresse IP du pool frontal ou tout autre appareil de succursale survivant ou succursale Survivable à l’aide de ce serveur Edge)</span><span class="sxs-lookup"><span data-stu-id="0651c-210">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="0651c-211">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="0651c-211">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0651c-212">L’authentification des utilisateurs A/V (service d’authentification A/V) à partir du serveur frontal ou de l’adresse IP du pool frontal ou de tout appareil de succursale ou de succursale survivant utilisant ce serveur Edge</span><span class="sxs-lookup"><span data-stu-id="0651c-212">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0651c-213">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="0651c-213">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="0651c-214">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-214">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-215">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="0651c-215">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0651c-216">Chemin préféré pour le transfert de média A/V entre des utilisateurs internes et externes, une unité de branchement survivant ou un serveur de succursales survivant</span><span class="sxs-lookup"><span data-stu-id="0651c-216">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0651c-217">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="0651c-217">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="0651c-218">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-218">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-219">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="0651c-219">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0651c-220">Pour le transfert de média A/V entre des utilisateurs internes et externes, une unité de branchement survivant ou un serveur de succursales survivant si la communication UDP ne peut pas être établie, le protocole TCP est utilisé pour le transfert de fichiers et le partage de bureau</span><span class="sxs-lookup"><span data-stu-id="0651c-220">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0651c-221">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="0651c-221">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="0651c-222">Tout (peut être défini en tant qu’adresse IP du serveur frontal ou pool contenant la Banque centrale de gestion).</span><span class="sxs-lookup"><span data-stu-id="0651c-222">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="0651c-223">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="0651c-223">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0651c-224">Réplication des modifications du magasin de gestion central vers le serveur de périphérie</span><span class="sxs-lookup"><span data-stu-id="0651c-224">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0651c-225">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="0651c-225">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="0651c-226">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-226">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-227">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="0651c-227">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0651c-228">Contrôleur de service de journalisation centralisé à l’aide de Lync Server Management Shell et des applets de ClsAgent.exe ClsController.exe commande de service de journalisation centralisée</span><span class="sxs-lookup"><span data-stu-id="0651c-228">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0651c-229">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="0651c-229">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="0651c-230">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-230">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-231">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="0651c-231">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0651c-232">Contrôleur de service de journalisation centralisé à l’aide de Lync Server Management Shell et des applets de ClsAgent.exe ClsController.exe commande de service de journalisation centralisée</span><span class="sxs-lookup"><span data-stu-id="0651c-232">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0651c-233">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="0651c-233">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="0651c-234">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-234">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-235">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="0651c-235">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0651c-236">Contrôleur de service de journalisation centralisé à l’aide de Lync Server Management Shell et des applets de ClsAgent.exe ClsController.exe commande de service de journalisation centralisée</span><span class="sxs-lookup"><span data-stu-id="0651c-236">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="0651c-237">Résumé du pare-feu pour la Fédération</span><span class="sxs-lookup"><span data-stu-id="0651c-237">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0651c-238">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="0651c-238">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="0651c-239">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="0651c-239">Source IP address</span></span></th>
<th><span data-ttu-id="0651c-240">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="0651c-240">Destination IP address</span></span></th>
<th><span data-ttu-id="0651c-241">Remarques</span><span class="sxs-lookup"><span data-stu-id="0651c-241">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0651c-242">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="0651c-242">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="0651c-243">Adresse IP publique du service Edge d’accès</span><span class="sxs-lookup"><span data-stu-id="0651c-243">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-244">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-244">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-245">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="0651c-245">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="0651c-246">Résumé du pare-feu-connectivité de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="0651c-246">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0651c-247">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="0651c-247">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="0651c-248">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="0651c-248">Source IP address</span></span></th>
<th><span data-ttu-id="0651c-249">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="0651c-249">Destination IP address</span></span></th>
<th><span data-ttu-id="0651c-250">Remarques</span><span class="sxs-lookup"><span data-stu-id="0651c-250">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0651c-251">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="0651c-251">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="0651c-252">Partenaires de connectivité de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="0651c-252">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="0651c-253">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="0651c-253">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="0651c-254">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="0651c-254">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0651c-255">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="0651c-255">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="0651c-256">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="0651c-256">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="0651c-257">Partenaires de connectivité de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="0651c-257">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="0651c-258">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="0651c-258">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0651c-259">/TCP/443 d’accès/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="0651c-259">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="0651c-260">Clients</span><span class="sxs-lookup"><span data-stu-id="0651c-260">Clients</span></span></p></td>
<td><p><span data-ttu-id="0651c-261">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="0651c-261">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="0651c-262">Trafic SIP client à serveur pour l’accès des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="0651c-262">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0651c-263">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="0651c-263">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="0651c-264">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="0651c-264">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="0651c-265">Clients Live Messenger</span><span class="sxs-lookup"><span data-stu-id="0651c-265">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="0651c-266">Utilisé pour les sessions A/V avec Windows Live Messenger si la connectivité PIC (Public IM Connectivity) est configurée.</span><span class="sxs-lookup"><span data-stu-id="0651c-266">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0651c-267">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="0651c-267">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="0651c-268">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="0651c-268">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="0651c-269">Clients Live Messenger</span><span class="sxs-lookup"><span data-stu-id="0651c-269">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="0651c-270">Requis pour la connectivité de messagerie instantanée publique avec Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="0651c-270">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0651c-271">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="0651c-271">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="0651c-272">Clients Live Messenger</span><span class="sxs-lookup"><span data-stu-id="0651c-272">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="0651c-273">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="0651c-273">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="0651c-274">Requis pour la connectivité de messagerie instantanée publique avec Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="0651c-274">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="0651c-275">Résumé du pare-feu pour le protocole extensible de messagerie et de présence</span><span class="sxs-lookup"><span data-stu-id="0651c-275">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0651c-276">Protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="0651c-276">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="0651c-277">Source (adresse IP)</span><span class="sxs-lookup"><span data-stu-id="0651c-277">Source (IP address)</span></span></th>
<th><span data-ttu-id="0651c-278">Destination (adresse IP)</span><span class="sxs-lookup"><span data-stu-id="0651c-278">Destination (IP address)</span></span></th>
<th><span data-ttu-id="0651c-279">Commentaires</span><span class="sxs-lookup"><span data-stu-id="0651c-279">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0651c-280">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="0651c-280">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="0651c-281">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-281">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-282">Adresse IP de l’interface du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="0651c-282">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-283">Port de communication serveur à serveur standard pour XMPP.</span><span class="sxs-lookup"><span data-stu-id="0651c-283">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="0651c-284">Autorise la communication au proxy de serveur Edge XMPP auprès des partenaires XMPP fédérés</span><span class="sxs-lookup"><span data-stu-id="0651c-284">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0651c-285">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="0651c-285">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="0651c-286">Adresse IP de l’interface du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="0651c-286">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="0651c-287">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-287">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-288">Port de communication serveur à serveur standard pour XMPP.</span><span class="sxs-lookup"><span data-stu-id="0651c-288">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="0651c-289">Autorise la communication du proxy de serveur Edge XMPP aux partenaires XMPP fédérés</span><span class="sxs-lookup"><span data-stu-id="0651c-289">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0651c-290">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="0651c-290">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="0651c-291">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0651c-291">Any</span></span></p></td>
<td><p><span data-ttu-id="0651c-292">Chaque adresse IP de l’interface du serveur Edge interne</span><span class="sxs-lookup"><span data-stu-id="0651c-292">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="0651c-293">Trafic de XMPP interne depuis la passerelle XMPP du serveur frontal ou du pool frontal vers l’adresse IP interne du serveur Edge ou l’adresse IP interne de chaque membre du pool de périphériques</span><span class="sxs-lookup"><span data-stu-id="0651c-293">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0651c-294">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0651c-294">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

