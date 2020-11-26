---
title: 'Lync Server 2013 : Résumé des ports - Serveur Edge consolidé mis à l’échelle, équilibrage de charge DNS avec des adresses IP publiques'
description: 'Lync Server 2013 : Résumé de port-niveau d’équilibrage de la charge DNS avec des adresses IP publiques.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses
ms:assetid: f7cbd0f1-841d-4116-8d17-e9d991daa4a8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205394(v=OCS.15)
ms:contentKeyID: 48185865
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8090435485b4b6a183702a608b139cec91ae26a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446338"
---
# <a name="port-summary---scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="8d7b2-103">Résumé des ports - Serveur Edge consolidé mis à l’échelle, équilibrage de charge DNS avec des adresses IP publiques dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8d7b2-103">Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8d7b2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8d7b2-104">

<span> </span></span></span>

<span data-ttu-id="8d7b2-105">_**Dernière modification de la rubrique :** 2013-04-03_</span><span class="sxs-lookup"><span data-stu-id="8d7b2-105">_**Topic Last Modified:** 2013-04-03_</span></span>

<span data-ttu-id="8d7b2-106">La fonctionnalité Lync Server 2013, Edge Server décrite dans cette architecture de scénario est très similaire à celle implémentée dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="8d7b2-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="8d7b2-107">Le plus notable est le port **5269 sur entrée TCP** pour le protocole XMPP (extensible Messaging and Presence Protocol).</span><span class="sxs-lookup"><span data-stu-id="8d7b2-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="8d7b2-108">Le serveur Lync Server 2013 déploie éventuellement un proxy XMPP sur le serveur Edge ou le pool de bords et sur le serveur de passerelle XMPP sur le serveur frontal ou le pool frontal.</span><span class="sxs-lookup"><span data-stu-id="8d7b2-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="8d7b2-109">Outre IPv4, le serveur Edge prend désormais en charge le protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="8d7b2-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="8d7b2-110">Par souci de clarté, seul le protocole IPv4 est utilisé dans les scénarios.</span><span class="sxs-lookup"><span data-stu-id="8d7b2-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="8d7b2-111">**Réseau de périmètre d’entreprise pour l’équilibrage de charge DNS à l’échelle**</span><span class="sxs-lookup"><span data-stu-id="8d7b2-111">**Enterprise perimeter network for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses**</span></span>

<span data-ttu-id="8d7b2-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span><span class="sxs-lookup"><span data-stu-id="8d7b2-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="8d7b2-113">Détails sur les ports et protocoles</span><span class="sxs-lookup"><span data-stu-id="8d7b2-113">Port and Protocol Details</span></span>

<span data-ttu-id="8d7b2-114">Il est recommandé d’ouvrir uniquement les ports requis pour la prise en charge des fonctionnalités pour lesquelles vous fournissez un accès externe.</span><span class="sxs-lookup"><span data-stu-id="8d7b2-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="8d7b2-115">Pour que l’accès à distance fonctionne pour tous les services Edge, il est obligatoire que le trafic SIP soit autorisé de manière bidirectionnelle, comme indiqué dans le schéma de trafic Edge entrant/sortant.</span><span class="sxs-lookup"><span data-stu-id="8d7b2-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="8d7b2-116">Autrement dit, la messagerie SIP vers et à partir du service Edge d’accès intervient dans les fonctionnalités de messagerie instantanée, de présence, de conférence Web, audio/vidéo (A/V) et de Fédération.</span><span class="sxs-lookup"><span data-stu-id="8d7b2-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="8d7b2-117">Résumé du pare-feu pour le bord consolidé mis à l’échelle, équilibrage de charge DNS avec adresses IP publiques : interface externe-nœud 1 et nœud 2 (exemple)</span><span class="sxs-lookup"><span data-stu-id="8d7b2-117">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8d7b2-118">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="8d7b2-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="8d7b2-119">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="8d7b2-119">Source IP address</span></span></th>
<th><span data-ttu-id="8d7b2-120">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="8d7b2-120">Destination IP address</span></span></th>
<th><span data-ttu-id="8d7b2-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="8d7b2-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="8d7b2-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-123">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-123">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-124">Service proxy XMPP (adresse IP du partage avec service Edge d’accès)</span><span class="sxs-lookup"><span data-stu-id="8d7b2-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-125">Le service proxy XMPP accepte le trafic de contacts XMPP dans les fédérations de XMPP définies</span><span class="sxs-lookup"><span data-stu-id="8d7b2-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d7b2-126">Accès/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="8d7b2-126">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-127">Adresse IP publique du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="8d7b2-127">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-128">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-128">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-129">Vérification et récupération des certificats</span><span class="sxs-lookup"><span data-stu-id="8d7b2-129">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-130">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="8d7b2-130">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-131">Adresse IP publique du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="8d7b2-131">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-132">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-132">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-133">Requête DNS sur TCP</span><span class="sxs-lookup"><span data-stu-id="8d7b2-133">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d7b2-134">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="8d7b2-134">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-135">Adresse IP publique du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="8d7b2-135">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-136">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-136">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-137">Requête DNS via UDP</span><span class="sxs-lookup"><span data-stu-id="8d7b2-137">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-138">/TCP/443 d’accès/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="8d7b2-138">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-139">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-139">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-140">Adresse IP publique du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="8d7b2-140">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-141">Trafic SIP client à serveur pour l’accès des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="8d7b2-141">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d7b2-142">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="8d7b2-142">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-143">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-143">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-144">Adresse IP publique du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="8d7b2-144">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-145">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="8d7b2-145">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-146">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="8d7b2-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-147">Adresse IP publique du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="8d7b2-147">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-148">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-148">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-149">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="8d7b2-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d7b2-150">PSOM (TLS) TCP/443</span><span class="sxs-lookup"><span data-stu-id="8d7b2-150">Web Conferencing/PSOM(TLS)TCP/443</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-151">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-151">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-152">Adresse IP publique du service Edge Conferencing Server Web</span><span class="sxs-lookup"><span data-stu-id="8d7b2-152">Edge Server Web Conferencing Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-153">Support de conférences Web</span><span class="sxs-lookup"><span data-stu-id="8d7b2-153">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-154">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="8d7b2-154">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-155">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="8d7b2-155">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-156">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-156">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-157">Requis pour la Fédération avec des partenaires exécutant Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 et Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8d7b2-157">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d7b2-158">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="8d7b2-158">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-159">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="8d7b2-159">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-160">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-160">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-161">Requis uniquement pour la Fédération avec les partenaires exécutant Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="8d7b2-161">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-162">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="8d7b2-162">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-163">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-163">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-164">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="8d7b2-164">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-165">Requis uniquement pour la Fédération avec les partenaires exécutant Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="8d7b2-165">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d7b2-166">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="8d7b2-166">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-167">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-167">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-168">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="8d7b2-168">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-169">Requis uniquement pour la Fédération avec les partenaires exécutant Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="8d7b2-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-170">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="8d7b2-170">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-171">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="8d7b2-171">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-172">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-172">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-173">3478 en sortie est utilisé pour déterminer la version de Edge Server avec laquelle Lync Server communique et le trafic multimédia à partir d’un serveur Edge serveur à périphérie.</span><span class="sxs-lookup"><span data-stu-id="8d7b2-173">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="8d7b2-174">Requis pour la Fédération avec Lync Server 2010, Windows Live Messenger et Office Communications Server 2007 R2, ainsi que le déploiement de plusieurs pools Edge au sein d’une entreprise.</span><span class="sxs-lookup"><span data-stu-id="8d7b2-174">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d7b2-175">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="8d7b2-175">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-176">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-176">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-177">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="8d7b2-177">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-178">STUN/activer la négociation des candidats via UDP/3478</span><span class="sxs-lookup"><span data-stu-id="8d7b2-178">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-179">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="8d7b2-179">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-180">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-180">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-181">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="8d7b2-181">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-182">STUN/activer la négociation des candidats via TCP/443</span><span class="sxs-lookup"><span data-stu-id="8d7b2-182">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d7b2-183">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="8d7b2-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-184">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="8d7b2-184">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-185">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-185">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-186">STUN/activer la négociation des candidats via TCP/443</span><span class="sxs-lookup"><span data-stu-id="8d7b2-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-internal-interface--node-1-and-node-2-example"></a><span data-ttu-id="8d7b2-187">Résumé du pare-feu pour les bords consolidés mis à l’échelle, équilibrage de charge DNS avec adresses IP publiques : interface interne – nœud 1 et nœud 2 (exemple)</span><span class="sxs-lookup"><span data-stu-id="8d7b2-187">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses: Internal Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8d7b2-188">Protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="8d7b2-188">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="8d7b2-189">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="8d7b2-189">Source IP address</span></span></th>
<th><span data-ttu-id="8d7b2-190">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="8d7b2-190">Destination IP address</span></span></th>
<th><span data-ttu-id="8d7b2-191">Commentaires</span><span class="sxs-lookup"><span data-stu-id="8d7b2-191">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-192">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="8d7b2-192">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-193">Tout (peut être défini comme adresse serveur frontale ou adresse IP de pool frontal exécutant le service passerelle XMPP)</span><span class="sxs-lookup"><span data-stu-id="8d7b2-193">Any (can be defined as Front End Server address, or Front End pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-194">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="8d7b2-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-195">Trafic XMPP sortant du service de passerelle XMPP exécuté sur le serveur frontal ou le pool frontal</span><span class="sxs-lookup"><span data-stu-id="8d7b2-195">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d7b2-196">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="8d7b2-196">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-197">Tout (peut être défini comme directeur, adresse IP du pool de directeurs, adresse IP du serveur frontal ou adresse IP du pool frontal)</span><span class="sxs-lookup"><span data-stu-id="8d7b2-197">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-198">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="8d7b2-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-199">Trafic SIP sortant (à partir du réalisateur, adresse IP du pool de réalisateurs, adresse IP du serveur frontal ou de la liste frontale) vers l’interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="8d7b2-199">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="8d7b2-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-201">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="8d7b2-201">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-202">Tout (peut être défini comme directeur, adresse IP du pool de directeurs, adresse IP du serveur frontal ou adresse IP du pool frontal)</span><span class="sxs-lookup"><span data-stu-id="8d7b2-202">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-203">Trafic SIP entrant (adresse IP du pool Directeur, serveur frontal ou adresse IP du pool frontal) à partir de l’interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="8d7b2-203">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d7b2-204">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="8d7b2-204">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-205">Tout (peut être défini comme adresse IP du serveur frontal ou chaque adresse IP du serveur frontal dans un pool frontal)</span><span class="sxs-lookup"><span data-stu-id="8d7b2-205">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-206">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="8d7b2-206">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-207">Trafic de conférences Web à partir du serveur frontal ou de chaque serveur frontal, s’il se trouve dans un pool, vers l’interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="8d7b2-207">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-208">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="8d7b2-208">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-209">Tout (peut être défini en tant qu’adresse IP du serveur frontal ou adresse IP du pool frontal ou tout autre appareil de succursale survivant ou succursale Survivable à l’aide de ce serveur Edge)</span><span class="sxs-lookup"><span data-stu-id="8d7b2-209">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-210">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="8d7b2-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-211">L’authentification des utilisateurs A/V (service d’authentification A/V) à partir du serveur frontal ou de l’adresse IP du pool frontal ou de tout appareil de succursale ou de succursale survivant utilisant ce serveur Edge</span><span class="sxs-lookup"><span data-stu-id="8d7b2-211">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d7b2-212">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="8d7b2-212">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-213">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-213">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-214">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="8d7b2-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-215">Chemin préféré pour le transfert de média A/V entre des utilisateurs internes et externes, une unité de branchement survivant ou un serveur de succursales survivant</span><span class="sxs-lookup"><span data-stu-id="8d7b2-215">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-216">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="8d7b2-216">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-217">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-217">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-218">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="8d7b2-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-219">Pour le transfert de média A/V entre des utilisateurs internes et externes, une unité de branchement survivant ou un serveur de succursales survivant si la communication UDP ne peut pas être établie, le protocole TCP est utilisé pour le transfert de fichiers et le partage de bureau</span><span class="sxs-lookup"><span data-stu-id="8d7b2-219">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d7b2-220">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="8d7b2-220">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-221">Tout (peut être défini en tant qu’adresse IP du serveur frontal ou pool contenant la Banque centrale de gestion).</span><span class="sxs-lookup"><span data-stu-id="8d7b2-221">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-222">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="8d7b2-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-223">Réplication des modifications du magasin de gestion central vers le serveur de périphérie</span><span class="sxs-lookup"><span data-stu-id="8d7b2-223">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-224">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="8d7b2-224">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-225">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-225">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-226">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="8d7b2-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-227">Contrôleur de service de journalisation centralisé à l’aide de Lync Server Management Shell et des applets de ClsAgent.exe ClsController.exe commande de service de journalisation centralisée</span><span class="sxs-lookup"><span data-stu-id="8d7b2-227">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d7b2-228">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="8d7b2-228">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-229">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-229">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-230">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="8d7b2-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-231">Contrôleur de service de journalisation centralisé à l’aide de Lync Server Management Shell et des applets de ClsAgent.exe ClsController.exe commande de service de journalisation centralisée</span><span class="sxs-lookup"><span data-stu-id="8d7b2-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-232">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="8d7b2-232">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-233">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-233">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-234">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="8d7b2-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-235">Contrôleur de service de journalisation centralisé à l’aide de Lync Server Management Shell et des applets de ClsAgent.exe ClsController.exe commande de service de journalisation centralisée</span><span class="sxs-lookup"><span data-stu-id="8d7b2-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="8d7b2-236">Résumé du pare-feu pour la Fédération</span><span class="sxs-lookup"><span data-stu-id="8d7b2-236">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8d7b2-237">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="8d7b2-237">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="8d7b2-238">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="8d7b2-238">Source IP address</span></span></th>
<th><span data-ttu-id="8d7b2-239">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="8d7b2-239">Destination IP address</span></span></th>
<th><span data-ttu-id="8d7b2-240">Remarques</span><span class="sxs-lookup"><span data-stu-id="8d7b2-240">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-241">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="8d7b2-241">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-242">Adresse IP publique du service Edge d’accès</span><span class="sxs-lookup"><span data-stu-id="8d7b2-242">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-243">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-243">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-244">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="8d7b2-244">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="8d7b2-245">Résumé du pare-feu-connectivité de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="8d7b2-245">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8d7b2-246">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="8d7b2-246">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="8d7b2-247">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="8d7b2-247">Source IP address</span></span></th>
<th><span data-ttu-id="8d7b2-248">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="8d7b2-248">Destination IP address</span></span></th>
<th><span data-ttu-id="8d7b2-249">Remarques</span><span class="sxs-lookup"><span data-stu-id="8d7b2-249">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-250">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="8d7b2-250">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-251">Partenaires de connectivité de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="8d7b2-251">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-252">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="8d7b2-252">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-253">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="8d7b2-253">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d7b2-254">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="8d7b2-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-255">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="8d7b2-255">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-256">Partenaires de connectivité de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="8d7b2-256">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-257">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="8d7b2-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-258">/TCP/443 d’accès/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="8d7b2-258">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-259">Clients</span><span class="sxs-lookup"><span data-stu-id="8d7b2-259">Clients</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-260">Service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="8d7b2-260">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-261">Trafic SIP client à serveur pour l’accès des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="8d7b2-261">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d7b2-262">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="8d7b2-262">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-263">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="8d7b2-263">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-264">Clients Live Messenger</span><span class="sxs-lookup"><span data-stu-id="8d7b2-264">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-265">Utilisé pour les sessions A/V avec Windows Live Messenger si la connectivité PIC (Public IM Connectivity) est configurée.</span><span class="sxs-lookup"><span data-stu-id="8d7b2-265">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-266">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="8d7b2-266">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-267">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="8d7b2-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-268">Clients Live Messenger</span><span class="sxs-lookup"><span data-stu-id="8d7b2-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-269">Requis pour la connectivité de messagerie instantanée publique avec Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="8d7b2-269">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d7b2-270">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="8d7b2-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-271">Clients Live Messenger</span><span class="sxs-lookup"><span data-stu-id="8d7b2-271">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-272">Service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="8d7b2-272">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-273">Requis pour la connectivité de messagerie instantanée publique avec Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="8d7b2-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="8d7b2-274">Résumé du pare-feu pour le protocole extensible de messagerie et de présence</span><span class="sxs-lookup"><span data-stu-id="8d7b2-274">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8d7b2-275">Protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="8d7b2-275">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="8d7b2-276">Source (adresse IP)</span><span class="sxs-lookup"><span data-stu-id="8d7b2-276">Source (IP address)</span></span></th>
<th><span data-ttu-id="8d7b2-277">Destination (adresse IP)</span><span class="sxs-lookup"><span data-stu-id="8d7b2-277">Destination (IP address)</span></span></th>
<th><span data-ttu-id="8d7b2-278">Commentaires</span><span class="sxs-lookup"><span data-stu-id="8d7b2-278">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-279">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="8d7b2-279">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-280">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-280">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-281">Adresse IP de l’interface du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="8d7b2-281">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-282">Port de communication serveur à serveur standard pour XMPP.</span><span class="sxs-lookup"><span data-stu-id="8d7b2-282">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="8d7b2-283">Autorise la communication au proxy de serveur Edge XMPP auprès des partenaires XMPP fédérés</span><span class="sxs-lookup"><span data-stu-id="8d7b2-283">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d7b2-284">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="8d7b2-284">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-285">Adresse IP de l’interface du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="8d7b2-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-286">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-286">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-287">Port de communication serveur à serveur standard pour XMPP.</span><span class="sxs-lookup"><span data-stu-id="8d7b2-287">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="8d7b2-288">Autorise la communication du proxy de serveur Edge XMPP aux partenaires XMPP fédérés</span><span class="sxs-lookup"><span data-stu-id="8d7b2-288">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d7b2-289">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="8d7b2-289">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-290">Indifférente</span><span class="sxs-lookup"><span data-stu-id="8d7b2-290">Any</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-291">Chaque adresse IP de l’interface du serveur Edge interne</span><span class="sxs-lookup"><span data-stu-id="8d7b2-291">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="8d7b2-292">Trafic de XMPP interne depuis la passerelle XMPP du serveur frontal ou du pool frontal vers l’adresse IP interne du serveur Edge ou l’adresse IP interne de chaque membre du pool de périphériques</span><span class="sxs-lookup"><span data-stu-id="8d7b2-292">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8d7b2-293">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8d7b2-293">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

