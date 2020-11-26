---
title: 'Lync Server 2013 : Résumé des enregistrements DNS - Serveur Edge consolidé mis à l’échelle, équilibrage de charge DNS avec adresses IP privées avec la conversion d’adresses réseau'
description: 'Lync Server 2013 : Résumé de port : un équilibrage de charge DNS avec des adresses IP privées à l’aide de tar.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT
ms:assetid: a296c2af-54d4-4b4f-9795-9191baf688cb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412756(v=OCS.15)
ms:contentKeyID: 48184955
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e0402b6682e86e5edf263fca78dfbe0f8fa070b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424283"
---
# <a name="port-summary---scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="7f597-103">Résumé des enregistrements DNS - Serveur Edge consolidé mis à l’échelle, équilibrage de charge DNS avec adresses IP privées avec la conversion d’adresses réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f597-103">Port summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7f597-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7f597-104">

<span> </span></span></span>

<span data-ttu-id="7f597-105">_**Dernière modification de la rubrique :** 2012-12-04_</span><span class="sxs-lookup"><span data-stu-id="7f597-105">_**Topic Last Modified:** 2012-12-04_</span></span>

<span data-ttu-id="7f597-106">La fonctionnalité Lync Server 2013, Edge Server décrite dans cette architecture de scénario est très similaire à celle implémentée dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="7f597-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="7f597-107">Le plus notable est le port **5269 sur entrée TCP** pour le protocole XMPP (extensible Messaging and Presence Protocol).</span><span class="sxs-lookup"><span data-stu-id="7f597-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="7f597-108">Le serveur Lync Server 2013 déploie éventuellement un proxy XMPP sur le serveur Edge ou le pool de bords et sur le serveur de passerelle XMPP sur le serveur frontal ou le pool frontal.</span><span class="sxs-lookup"><span data-stu-id="7f597-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="7f597-109">Outre IPv4, le serveur Edge prend désormais en charge le protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="7f597-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="7f597-110">Par souci de clarté, seul le protocole IPv4 est utilisé dans les scénarios.</span><span class="sxs-lookup"><span data-stu-id="7f597-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="7f597-111">**Réseau de périmètre d’entreprise pour bordure consolidée mise à l’échelle avec des adresses IP privées à l’aide de tar**</span><span class="sxs-lookup"><span data-stu-id="7f597-111">**Enterprise perimeter network for scaled consolidated edge with private IP addresses using NAT**</span></span>

<span data-ttu-id="7f597-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span><span class="sxs-lookup"><span data-stu-id="7f597-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="7f597-113">Détails sur les ports et protocoles</span><span class="sxs-lookup"><span data-stu-id="7f597-113">Port and Protocol Details</span></span>

<span data-ttu-id="7f597-114">Il est recommandé d’ouvrir uniquement les ports requis pour la prise en charge des fonctionnalités pour lesquelles vous fournissez un accès externe.</span><span class="sxs-lookup"><span data-stu-id="7f597-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="7f597-115">Pour que l’accès à distance fonctionne pour tous les services Edge, il est obligatoire que le trafic SIP soit autorisé de manière bidirectionnelle, comme indiqué dans le schéma de trafic Edge entrant/sortant.</span><span class="sxs-lookup"><span data-stu-id="7f597-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="7f597-116">Autrement dit, la messagerie SIP vers et à partir du service Edge d’accès intervient dans les fonctionnalités de messagerie instantanée, de présence, de conférence Web, audio/vidéo (A/V) et de Fédération.</span><span class="sxs-lookup"><span data-stu-id="7f597-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="7f597-117">Résumé du pare-feu pour les bords consolidés mis à l’échelle de l’équilibrage de charge DNS avec des adresses IP privées utilisant tar : interface externe-nœud 1 et nœud 2 (exemple)</span><span class="sxs-lookup"><span data-stu-id="7f597-117">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Private IP Addresses Using NAT: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f597-118">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="7f597-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="7f597-119">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="7f597-119">Source IP address</span></span></th>
<th><span data-ttu-id="7f597-120">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="7f597-120">Destination IP address</span></span></th>
<th><span data-ttu-id="7f597-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="7f597-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f597-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="7f597-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="7f597-123">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-123">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-124">Service proxy XMPP (adresse IP du partage avec service Edge d’accès)</span><span class="sxs-lookup"><span data-stu-id="7f597-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="7f597-125">Le service proxy XMPP accepte le trafic de contacts XMPP dans les fédérations de XMPP définies</span><span class="sxs-lookup"><span data-stu-id="7f597-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f597-126">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="7f597-126">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="7f597-127">Service proxy XMPP (adresse IP du partage avec service Edge d’accès)</span><span class="sxs-lookup"><span data-stu-id="7f597-127">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="7f597-128">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-128">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-129">Le service de proxy XMPP envoie le trafic aux contacts XMPP dans les fédérations de XMPP définies.</span><span class="sxs-lookup"><span data-stu-id="7f597-129">XMPP Proxy service sends traffic to XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f597-130">Accès/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="7f597-130">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="7f597-131">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="7f597-131">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-132">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-132">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-133">Vérification et récupération des certificats</span><span class="sxs-lookup"><span data-stu-id="7f597-133">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f597-134">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="7f597-134">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="7f597-135">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="7f597-135">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-136">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-136">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-137">Requête DNS sur TCP</span><span class="sxs-lookup"><span data-stu-id="7f597-137">DNS query over TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f597-138">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="7f597-138">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="7f597-139">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="7f597-139">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-140">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-140">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-141">Requête DNS via UDP</span><span class="sxs-lookup"><span data-stu-id="7f597-141">DNS query over UDP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f597-142">/TCP/443 d’accès/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="7f597-142">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="7f597-143">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-143">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-144">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="7f597-144">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-145">Trafic SIP client à serveur pour l’accès des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="7f597-145">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f597-146">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="7f597-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="7f597-147">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-147">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-148">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="7f597-148">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-149">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="7f597-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f597-150">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="7f597-150">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="7f597-151">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="7f597-151">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-152">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-152">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-153">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="7f597-153">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f597-154">PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="7f597-154">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="7f597-155">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-155">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-156">Service Edge de conférence Web Edge Server</span><span class="sxs-lookup"><span data-stu-id="7f597-156">Edge Server Web Conferencing Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-157">Support de conférences Web</span><span class="sxs-lookup"><span data-stu-id="7f597-157">Web Conferencing media</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f597-158">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="7f597-158">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="7f597-159">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="7f597-159">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-160">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-160">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-161">Requis pour la Fédération avec des partenaires exécutant Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 et Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7f597-161">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f597-162">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="7f597-162">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="7f597-163">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="7f597-163">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-164">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-164">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-165">Requis uniquement pour la Fédération avec les partenaires exécutant Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="7f597-165">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f597-166">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="7f597-166">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="7f597-167">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-167">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-168">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="7f597-168">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-169">Requis uniquement pour la Fédération avec les partenaires exécutant Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="7f597-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f597-170">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="7f597-170">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="7f597-171">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-171">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-172">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="7f597-172">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-173">Requis uniquement pour la Fédération avec les partenaires exécutant Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="7f597-173">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f597-174">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="7f597-174">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="7f597-175">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="7f597-175">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-176">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-176">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-177">3478 en sortie est utilisé pour déterminer la version de Edge Server avec laquelle Lync Server communique et le trafic multimédia à partir d’un serveur Edge serveur à périphérie.</span><span class="sxs-lookup"><span data-stu-id="7f597-177">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="7f597-178">Requis pour la Fédération avec Lync Server 2010, Windows Live Messenger et Office Communications Server 2007 R2, ainsi que le déploiement de plusieurs pools Edge au sein d’une entreprise.</span><span class="sxs-lookup"><span data-stu-id="7f597-178">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f597-179">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="7f597-179">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="7f597-180">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-180">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-181">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="7f597-181">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-182">STUN/activer la négociation des candidats via UDP/3478</span><span class="sxs-lookup"><span data-stu-id="7f597-182">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f597-183">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="7f597-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="7f597-184">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-184">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-185">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="7f597-185">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-186">STUN/activer la négociation des candidats via TCP/443</span><span class="sxs-lookup"><span data-stu-id="7f597-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f597-187">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="7f597-187">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="7f597-188">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="7f597-188">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-189">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-189">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-190">STUN/activer la négociation des candidats via TCP/443</span><span class="sxs-lookup"><span data-stu-id="7f597-190">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-internal-interface--node-1-and-node-2-example"></a><span data-ttu-id="7f597-191">Résumé du pare-feu pour les bords consolidés mis à l’échelle de l’équilibrage de charge DNS avec des adresses IP privées à l’aide de tar : interface interne-nœud 1 et nœud 2 (exemple)</span><span class="sxs-lookup"><span data-stu-id="7f597-191">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Private IP Addresses Using NAT: Internal Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f597-192">Protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="7f597-192">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="7f597-193">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="7f597-193">Source IP address</span></span></th>
<th><span data-ttu-id="7f597-194">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="7f597-194">Destination IP address</span></span></th>
<th><span data-ttu-id="7f597-195">Commentaires</span><span class="sxs-lookup"><span data-stu-id="7f597-195">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f597-196">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="7f597-196">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="7f597-197">Tout (peut être défini comme adresse serveur frontale ou adresse IP de pool frontal exécutant le service passerelle XMPP)</span><span class="sxs-lookup"><span data-stu-id="7f597-197">Any (can be defined as Front End Server address, or Front End pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="7f597-198">Adresse IP de l’interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="7f597-198">Edge Server internal interface IP address</span></span></p></td>
<td><p><span data-ttu-id="7f597-199">Trafic XMPP sortant du service de passerelle XMPP exécuté sur le serveur frontal ou le pool frontal</span><span class="sxs-lookup"><span data-stu-id="7f597-199">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f597-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="7f597-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="7f597-201">Tout (peut être défini comme directeur, adresse IP du pool de directeurs, adresse IP du serveur frontal ou adresse IP du pool frontal)</span><span class="sxs-lookup"><span data-stu-id="7f597-201">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="7f597-202">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="7f597-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7f597-203">Trafic SIP sortant (à partir du réalisateur, adresse IP du pool de réalisateurs, adresse IP du serveur frontal ou de la liste frontale) vers l’interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="7f597-203">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f597-204">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="7f597-204">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="7f597-205">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="7f597-205">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7f597-206">Tout (peut être défini comme directeur, adresse IP du pool de directeurs, adresse IP du serveur frontal ou adresse IP du pool frontal)</span><span class="sxs-lookup"><span data-stu-id="7f597-206">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="7f597-207">Trafic SIP entrant (adresse IP du pool Directeur, serveur frontal ou adresse IP du pool frontal) à partir de l’interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="7f597-207">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f597-208">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="7f597-208">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="7f597-209">Tout (peut être défini comme adresse IP du serveur frontal ou chaque adresse IP du serveur frontal dans un pool frontal)</span><span class="sxs-lookup"><span data-stu-id="7f597-209">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="7f597-210">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="7f597-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7f597-211">Trafic de conférences Web à partir du serveur frontal ou de chaque serveur frontal, s’il se trouve dans un pool, vers l’interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="7f597-211">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f597-212">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="7f597-212">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="7f597-213">Tout (peut être défini en tant qu’adresse IP du serveur frontal ou adresse IP du pool frontal ou tout autre appareil de succursale survivant ou succursale Survivable à l’aide de ce serveur Edge)</span><span class="sxs-lookup"><span data-stu-id="7f597-213">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="7f597-214">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="7f597-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7f597-215">L’authentification des utilisateurs A/V (service d’authentification A/V) à partir du serveur frontal ou de l’adresse IP du pool frontal ou de tout appareil de succursale ou de succursale survivant utilisant ce serveur Edge</span><span class="sxs-lookup"><span data-stu-id="7f597-215">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f597-216">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="7f597-216">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="7f597-217">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-217">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-218">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="7f597-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7f597-219">Chemin préféré pour le transfert de média A/V entre des utilisateurs internes et externes, une unité de branchement survivant ou un serveur de succursales survivant</span><span class="sxs-lookup"><span data-stu-id="7f597-219">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f597-220">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="7f597-220">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="7f597-221">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-221">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-222">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="7f597-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7f597-223">Pour le transfert de média A/V entre des utilisateurs internes et externes, une unité de branchement survivant ou un serveur de succursales survivant si la communication UDP ne peut pas être établie, le protocole TCP est utilisé pour le transfert de fichiers et le partage de bureau</span><span class="sxs-lookup"><span data-stu-id="7f597-223">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f597-224">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="7f597-224">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="7f597-225">Tout (peut être défini en tant qu’adresse IP du serveur frontal ou pool contenant la Banque centrale de gestion).</span><span class="sxs-lookup"><span data-stu-id="7f597-225">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="7f597-226">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="7f597-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7f597-227">Réplication des modifications du magasin de gestion central vers le serveur de périphérie</span><span class="sxs-lookup"><span data-stu-id="7f597-227">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f597-228">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="7f597-228">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="7f597-229">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-229">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-230">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="7f597-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7f597-231">Contrôleur de service de journalisation centralisé à l’aide de Lync Server Management Shell et des applets de ClsAgent.exe ClsController.exe commande de service de journalisation centralisée</span><span class="sxs-lookup"><span data-stu-id="7f597-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f597-232">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="7f597-232">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="7f597-233">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-233">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-234">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="7f597-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7f597-235">Contrôleur de service de journalisation centralisé à l’aide de Lync Server Management Shell et des applets de ClsAgent.exe ClsController.exe commande de service de journalisation centralisée</span><span class="sxs-lookup"><span data-stu-id="7f597-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f597-236">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="7f597-236">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="7f597-237">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-237">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-238">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="7f597-238">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7f597-239">Contrôleur de service de journalisation centralisé à l’aide de Lync Server Management Shell et des applets de ClsAgent.exe ClsController.exe commande de service de journalisation centralisée</span><span class="sxs-lookup"><span data-stu-id="7f597-239">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="7f597-240">Résumé du pare-feu pour la Fédération</span><span class="sxs-lookup"><span data-stu-id="7f597-240">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f597-241">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="7f597-241">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="7f597-242">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="7f597-242">Source IP address</span></span></th>
<th><span data-ttu-id="7f597-243">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="7f597-243">Destination IP address</span></span></th>
<th><span data-ttu-id="7f597-244">Remarques</span><span class="sxs-lookup"><span data-stu-id="7f597-244">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f597-245">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="7f597-245">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="7f597-246">Adresse IP publique du service Edge d’accès</span><span class="sxs-lookup"><span data-stu-id="7f597-246">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="7f597-247">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-247">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-248">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="7f597-248">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="7f597-249">Résumé du pare-feu-connectivité de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="7f597-249">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f597-250">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="7f597-250">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="7f597-251">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="7f597-251">Source IP address</span></span></th>
<th><span data-ttu-id="7f597-252">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="7f597-252">Destination IP address</span></span></th>
<th><span data-ttu-id="7f597-253">Remarques</span><span class="sxs-lookup"><span data-stu-id="7f597-253">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f597-254">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="7f597-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="7f597-255">Partenaires de connectivité de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="7f597-255">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="7f597-256">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="7f597-256">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-257">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="7f597-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f597-258">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="7f597-258">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="7f597-259">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="7f597-259">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-260">Partenaires de connectivité de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="7f597-260">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="7f597-261">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="7f597-261">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f597-262">/TCP/443 d’accès/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="7f597-262">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="7f597-263">Clients</span><span class="sxs-lookup"><span data-stu-id="7f597-263">Clients</span></span></p></td>
<td><p><span data-ttu-id="7f597-264">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="7f597-264">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-265">Trafic SIP client à serveur pour l’accès des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="7f597-265">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f597-266">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="7f597-266">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="7f597-267">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="7f597-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-268">Clients Live Messenger</span><span class="sxs-lookup"><span data-stu-id="7f597-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="7f597-269">Utilisé pour les sessions A/V avec Windows Live Messenger si la connectivité PIC (Public IM Connectivity) est configurée.</span><span class="sxs-lookup"><span data-stu-id="7f597-269">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f597-270">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="7f597-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="7f597-271">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="7f597-271">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-272">Clients Live Messenger</span><span class="sxs-lookup"><span data-stu-id="7f597-272">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="7f597-273">Requis pour la connectivité de messagerie instantanée publique avec Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="7f597-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f597-274">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="7f597-274">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="7f597-275">Clients Live Messenger</span><span class="sxs-lookup"><span data-stu-id="7f597-275">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="7f597-276">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="7f597-276">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="7f597-277">Requis pour la connectivité de messagerie instantanée publique avec Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="7f597-277">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="7f597-278">Résumé du pare-feu pour le protocole extensible de messagerie et de présence</span><span class="sxs-lookup"><span data-stu-id="7f597-278">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f597-279">Protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="7f597-279">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="7f597-280">Source (adresse IP)</span><span class="sxs-lookup"><span data-stu-id="7f597-280">Source (IP address)</span></span></th>
<th><span data-ttu-id="7f597-281">Destination (adresse IP)</span><span class="sxs-lookup"><span data-stu-id="7f597-281">Destination (IP address)</span></span></th>
<th><span data-ttu-id="7f597-282">Commentaires</span><span class="sxs-lookup"><span data-stu-id="7f597-282">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f597-283">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="7f597-283">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="7f597-284">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-284">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-285">Adresse IP de l’interface du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="7f597-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="7f597-286">Port de communication serveur à serveur standard pour XMPP.</span><span class="sxs-lookup"><span data-stu-id="7f597-286">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="7f597-287">Autorise la communication au proxy de serveur Edge XMPP auprès des partenaires XMPP fédérés</span><span class="sxs-lookup"><span data-stu-id="7f597-287">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f597-288">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="7f597-288">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="7f597-289">Adresse IP de l’interface du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="7f597-289">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="7f597-290">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-290">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-291">Port de communication serveur à serveur standard pour XMPP.</span><span class="sxs-lookup"><span data-stu-id="7f597-291">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="7f597-292">Autorise la communication du proxy de serveur Edge XMPP aux partenaires XMPP fédérés</span><span class="sxs-lookup"><span data-stu-id="7f597-292">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f597-293">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="7f597-293">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="7f597-294">Indifférente</span><span class="sxs-lookup"><span data-stu-id="7f597-294">Any</span></span></p></td>
<td><p><span data-ttu-id="7f597-295">Chaque adresse IP de l’interface du serveur Edge interne</span><span class="sxs-lookup"><span data-stu-id="7f597-295">Each internal Edge Server interface IP</span></span></p></td>
<td><p><span data-ttu-id="7f597-296">Trafic de XMPP interne depuis la passerelle XMPP du serveur frontal ou du pool frontal vers l’adresse IP interne du serveur Edge ou l’adresse IP interne de chaque membre du pool de périphériques</span><span class="sxs-lookup"><span data-stu-id="7f597-296">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7f597-297">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7f597-297">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

