---
title: Résumé des ports - Serveur Edge consolidé mis à l’échelle avec des équilibreurs de charge matérielle
description: Résumé de port-bordure consolidée mise à l’échelle avec des équilibreurs de charge matérielle.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge with hardware load balancers
ms:assetid: 91213b1e-f875-464b-83e8-fe3a351595a4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398739(v=OCS.15)
ms:contentKeyID: 48184841
ms.date: 04/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1a03acb3644d83669bcf0065ebb20c526ef5fa32
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424312"
---
# <a name="port-summary---scaled-consolidated-edge-with-hardware-load-balancers-in-lync-server-2013"></a><span data-ttu-id="70e6d-103">Résumé des ports - Serveur Edge consolidé mis à l’échelle avec des équilibreurs de charge matérielle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="70e6d-103">Port summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="70e6d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="70e6d-104">

<span> </span></span></span>

<span data-ttu-id="70e6d-105">_**Dernière modification de la rubrique :** 2015-04-27_</span><span class="sxs-lookup"><span data-stu-id="70e6d-105">_**Topic Last Modified:** 2015-04-27_</span></span>

<span data-ttu-id="70e6d-106">La fonctionnalité Lync Server 2013, Edge Server décrite dans cette architecture de scénario est très similaire à celle implémentée dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="70e6d-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="70e6d-107">Le plus notable est le port **5269 sur entrée TCP** pour le protocole XMPP (extensible Messaging and Presence Protocol).</span><span class="sxs-lookup"><span data-stu-id="70e6d-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="70e6d-108">Le serveur Lync Server 2013 déploie éventuellement un proxy XMPP sur le serveur Edge ou le pool de bords et sur le serveur de passerelle XMPP sur le serveur frontal ou le pool frontal.</span><span class="sxs-lookup"><span data-stu-id="70e6d-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="70e6d-109">Outre IPv4, le serveur Edge prend désormais en charge le protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="70e6d-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="70e6d-110">Par souci de clarté, seul le protocole IPv4 est utilisé dans les scénarios.</span><span class="sxs-lookup"><span data-stu-id="70e6d-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="70e6d-111">**Contour consolidé mis à l’échelle à l’aide de l’équilibrage de charge matérielle**</span><span class="sxs-lookup"><span data-stu-id="70e6d-111">**Scaled Consolidated Edge using Hardware Load Balancing**</span></span>

<span data-ttu-id="70e6d-112">![Ports et protocoles du réseau de périmètre du serveur Edge](images/Gg398739.063f7dd1-16db-4cc7-8708-bca9bc41184d(OCS.15).jpg "Ports et protocoles du réseau de périmètre du serveur Edge")</span><span class="sxs-lookup"><span data-stu-id="70e6d-112">![Edge Server Perimeter Network ports and protocols](images/Gg398739.063f7dd1-16db-4cc7-8708-bca9bc41184d(OCS.15).jpg "Edge Server Perimeter Network ports and protocols")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="70e6d-113">Détails sur les ports et protocoles</span><span class="sxs-lookup"><span data-stu-id="70e6d-113">Port and Protocol Details</span></span>

<span data-ttu-id="70e6d-114">Il est recommandé d’ouvrir uniquement les ports requis pour la prise en charge des fonctionnalités pour lesquelles vous fournissez un accès externe.</span><span class="sxs-lookup"><span data-stu-id="70e6d-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="70e6d-115">Pour que l’accès à distance fonctionne pour tous les services Edge, il est obligatoire que le trafic SIP soit autorisé de manière bidirectionnelle, comme indiqué dans le schéma de trafic Edge entrant/sortant.</span><span class="sxs-lookup"><span data-stu-id="70e6d-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="70e6d-116">Autrement dit, la messagerie SIP vers et à partir du service Edge d’accès intervient dans les fonctionnalités de messagerie instantanée, de présence, de conférence Web, audio/vidéo (A/V) et de Fédération.</span><span class="sxs-lookup"><span data-stu-id="70e6d-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="70e6d-117">Résumé du pare-feu pour les bords consolidés mis à l’échelle : équilibrage de charge matérielle : interface externe-nœud 1 et nœud 2 (exemple)</span><span class="sxs-lookup"><span data-stu-id="70e6d-117">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70e6d-118">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="70e6d-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="70e6d-119">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="70e6d-119">Source IP address</span></span></th>
<th><span data-ttu-id="70e6d-120">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="70e6d-120">Destination IP address</span></span></th>
<th><span data-ttu-id="70e6d-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="70e6d-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70e6d-122">Accès/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="70e6d-122">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="70e6d-123">Adresse IP publique du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="70e6d-123">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="70e6d-124">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-124">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-125">Vérification et récupération des certificats</span><span class="sxs-lookup"><span data-stu-id="70e6d-125">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70e6d-126">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="70e6d-126">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="70e6d-127">Adresse IP publique du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="70e6d-127">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="70e6d-128">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-128">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-129">Requête DNS sur TCP</span><span class="sxs-lookup"><span data-stu-id="70e6d-129">DNS query over TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70e6d-130">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="70e6d-130">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="70e6d-131">Adresse IP publique du service Edge d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="70e6d-131">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="70e6d-132">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-132">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-133">Requête DNS via UDP</span><span class="sxs-lookup"><span data-stu-id="70e6d-133">DNS query over UDP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70e6d-134">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="70e6d-134">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="70e6d-135">Adresse IP du service Edge serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="70e6d-135">Edge Server A/V Edge service IP address</span></span></p></td>
<td><p><span data-ttu-id="70e6d-136">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-136">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-137">Requis pour la Fédération avec des partenaires exécutant Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 et Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="70e6d-137">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70e6d-138">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="70e6d-138">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="70e6d-139">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="70e6d-139">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="70e6d-140">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-140">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-141">Requis uniquement pour la Fédération avec les partenaires exécutant Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="70e6d-141">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70e6d-142">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="70e6d-142">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="70e6d-143">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-143">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-144">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="70e6d-144">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="70e6d-145">Requis uniquement pour la Fédération avec les partenaires exécutant Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="70e6d-145">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70e6d-146">A/V/RTP/UDP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="70e6d-146">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="70e6d-147">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-147">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-148">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="70e6d-148">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="70e6d-149">Requis uniquement pour la Fédération avec les partenaires exécutant Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="70e6d-149">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70e6d-150">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="70e6d-150">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="70e6d-151">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="70e6d-151">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="70e6d-152">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-152">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-153">3478 en sortie est utilisé pour déterminer la version de Edge Server avec laquelle Lync Server communique et le trafic multimédia à partir d’un serveur Edge serveur à périphérie.</span><span class="sxs-lookup"><span data-stu-id="70e6d-153">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="70e6d-154">Requis pour la Fédération avec Lync Server 2010, Windows Live Messenger et Office Communications Server 2007 R2, ainsi que le déploiement de plusieurs pools Edge au sein d’une entreprise.</span><span class="sxs-lookup"><span data-stu-id="70e6d-154">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70e6d-155">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="70e6d-155">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="70e6d-156">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-156">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-157">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="70e6d-157">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="70e6d-158">STUN/activer la négociation des candidats via UDP/3478</span><span class="sxs-lookup"><span data-stu-id="70e6d-158">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70e6d-159">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="70e6d-159">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="70e6d-160">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-160">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-161">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="70e6d-161">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="70e6d-162">STUN/activer la négociation des candidats via TCP/443</span><span class="sxs-lookup"><span data-stu-id="70e6d-162">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70e6d-163">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="70e6d-163">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="70e6d-164">Adresse IP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="70e6d-164">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="70e6d-165">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-165">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-166">STUN/activer la négociation des candidats via TCP/443</span><span class="sxs-lookup"><span data-stu-id="70e6d-166">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-internal-interface-node-1-and-node-2"></a><span data-ttu-id="70e6d-167">Résumé du pare-feu pour les bords consolidés mis à l’échelle : charge matérielle</span><span class="sxs-lookup"><span data-stu-id="70e6d-167">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: Internal Interface Node 1 and Node 2</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70e6d-168">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="70e6d-168">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="70e6d-169">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="70e6d-169">Source IP address</span></span></th>
<th><span data-ttu-id="70e6d-170">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="70e6d-170">Destination IP address</span></span></th>
<th><span data-ttu-id="70e6d-171">Remarques</span><span class="sxs-lookup"><span data-stu-id="70e6d-171">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70e6d-172">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="70e6d-172">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="70e6d-173">Tout (peut être défini comme adresse serveur frontale ou adresse IP virtuelle de pool frontal exécutant le service passerelle XMPP)</span><span class="sxs-lookup"><span data-stu-id="70e6d-173">Any (can be defined as Front End Server address, or Front End pool virtual IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="70e6d-174">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="70e6d-174">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="70e6d-175">Trafic XMPP sortant du service de passerelle XMPP exécuté sur le serveur frontal ou le pool frontal</span><span class="sxs-lookup"><span data-stu-id="70e6d-175">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70e6d-176">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="70e6d-176">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="70e6d-177">Tout (peut être défini en tant que serveur principal serveur ou pool serveur serveur principal)</span><span class="sxs-lookup"><span data-stu-id="70e6d-177">Any (can be defined as the Front End Server server IP or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="70e6d-178">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="70e6d-178">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="70e6d-179">Réplication des modifications du magasin de gestion central vers le serveur de périphérie</span><span class="sxs-lookup"><span data-stu-id="70e6d-179">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70e6d-180">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="70e6d-180">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="70e6d-181">Tout (peut être défini en tant que adresse IP du directeur, adresse IP du serveur frontal ou adresse IP virtuelle du pool)</span><span class="sxs-lookup"><span data-stu-id="70e6d-181">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="70e6d-182">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="70e6d-182">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="70e6d-183">Trafic de conférences Web entre le déploiement interne et l’interface du serveur Edge interne</span><span class="sxs-lookup"><span data-stu-id="70e6d-183">Web conferencing traffic from Internal deployment to Internal Edge Server interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70e6d-184">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="70e6d-184">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="70e6d-185">Tout (peut être défini en tant que adresse IP du directeur, adresse IP du serveur frontal ou adresse IP virtuelle du pool)</span><span class="sxs-lookup"><span data-stu-id="70e6d-185">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="70e6d-186">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="70e6d-186">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="70e6d-187">Chemin préféré pour le transfert de média A/V entre des utilisateurs internes et externes, une unité de branchement survivant ou un serveur de succursales survivant</span><span class="sxs-lookup"><span data-stu-id="70e6d-187">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70e6d-188">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="70e6d-188">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="70e6d-189">Tout (peut être défini en tant que adresse IP du directeur, adresse IP du serveur frontal ou adresse IP virtuelle du pool)</span><span class="sxs-lookup"><span data-stu-id="70e6d-189">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="70e6d-190">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="70e6d-190">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="70e6d-191">Pour le transfert de média A/V entre des utilisateurs internes et externes, une unité de branchement survivant ou un serveur de succursales survivant si la communication UDP ne peut pas être établie, le protocole TCP est utilisé pour le transfert de fichiers et le partage de bureau</span><span class="sxs-lookup"><span data-stu-id="70e6d-191">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70e6d-192">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="70e6d-192">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="70e6d-193">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-193">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-194">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="70e6d-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="70e6d-195">Contrôleur de service de journalisation centralisé à l’aide de Lync Server Management Shell et des applets de ClsAgent.exe ClsController.exe commande de service de journalisation centralisée</span><span class="sxs-lookup"><span data-stu-id="70e6d-195">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70e6d-196">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="70e6d-196">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="70e6d-197">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-197">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-198">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="70e6d-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="70e6d-199">Contrôleur de service de journalisation centralisé à l’aide de Lync Server Management Shell et des applets de ClsAgent.exe ClsController.exe commande de service de journalisation centralisée</span><span class="sxs-lookup"><span data-stu-id="70e6d-199">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70e6d-200">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="70e6d-200">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="70e6d-201">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-201">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-202">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="70e6d-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="70e6d-203">Contrôleur de service de journalisation centralisé à l’aide de Lync Server Management Shell et des applets de ClsAgent.exe ClsController.exe commande de service de journalisation centralisée</span><span class="sxs-lookup"><span data-stu-id="70e6d-203">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="70e6d-204">Les équilibreurs de charge matérielle nécessitent des exigences spécifiques pour assurer la disponibilité et l’équilibrage de charge de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="70e6d-204">Hardware load balancers have specific requirements when deployed to provide availability and load balancing for Lync Server.</span></span> <span data-ttu-id="70e6d-205">La configuration requise est définie dans les tableaux et figures suivants.</span><span class="sxs-lookup"><span data-stu-id="70e6d-205">The requirements are defined in the following figure and tables.</span></span> <span data-ttu-id="70e6d-206">Les fournisseurs tiers pourront utiliser une terminologie différente pour les exigences définies ici.</span><span class="sxs-lookup"><span data-stu-id="70e6d-206">Third party vendors may use different terminology for the requirements defined here.</span></span> <span data-ttu-id="70e6d-207">Il est nécessaire de mapper les exigences de Lync Server aux options et aux options de configuration fournies par le fournisseur du programme d’équilibrage de la charge matérielle.</span><span class="sxs-lookup"><span data-stu-id="70e6d-207">It will be necessary to map the requirements of Lync Server to the features and configuration options provided by your hardware load balancer vendor.</span></span>

<span data-ttu-id="70e6d-208">Lorsque vous configurez des équilibreurs de charge matérielle, prenez en compte les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="70e6d-208">When configuring hardware load balancers, consider the following requirements:</span></span>

  - <span data-ttu-id="70e6d-209">La traduction d’adresses réseau source (SNAT) peut être configurée sur l’équilibrage de charge matérielle (HLB) pour le service Edge d’accès et le service Edge de conférence Web.</span><span class="sxs-lookup"><span data-stu-id="70e6d-209">Source Network Address Translation (SNAT) can be configured on the hardware load balancer (HLB) for Access Edge service and Web Conferencing Edge service</span></span>

  - <span data-ttu-id="70e6d-210">Les données SNAT ne peuvent pas être configurées sur le service Edge A/V : le service Edge A/V doit répondre avec l’adresse réelle du serveur (et non l’adresse IP virtuelle HLB) pour une traversée simple du protocole UDP sur NAT (STUN)/Traversal à l’aide d’un NAT relais (FDÉSACTIVEZ) pour fonctionner correctement</span><span class="sxs-lookup"><span data-stu-id="70e6d-210">SNAT cannot be configured on the A/V Edge service– the A/V Edge service must respond with the real server address, not the HLB virtual IP (VIP), for simple traversal of UDP over NAT (STUN)/traversal using relay NAT (TURN)/federation TURN (FTURN) to work properly</span></span>
    
      - <span data-ttu-id="70e6d-211">Si le client envoie une demande à l’HLB, la réponse doit être retirée du VIP HLB</span><span class="sxs-lookup"><span data-stu-id="70e6d-211">If the client sends a request to the HLB, the response must come back from the HLB VIP</span></span>
    
      - <span data-ttu-id="70e6d-212">Si le client envoie une demande à l’Edge, la réponse doit être retirée de l’adresse IP du serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="70e6d-212">If the client sends a request to the Edge, the response must come back from the Edge IP</span></span>

  - <span data-ttu-id="70e6d-213">Les adresses IP publiques sont utilisées sur chaque interface serveur et sur les adresses IP 2 du HLB et les exigences relatives à l’adresse IP publique sont de N + 1, car il existe une adresse IP publique pour chaque interface de serveur réel et une pour chaque VIP HLB.</span><span class="sxs-lookup"><span data-stu-id="70e6d-213">Public IP addresses are used on each server interface and on the VIPs of the HLB, and your public IP address requirements are N+1, where there is a public IP address for each real server interface and one for each HLB VIP.</span></span> <span data-ttu-id="70e6d-214">Lorsque vous avez 2 serveurs de périmètre dans le pool, il s’agit de 9 adresses IP publiques, 3 qui sont utilisées pour les VIP HLB et une pour chaque interface de serveur Edge (un total de six pour les serveurs).</span><span class="sxs-lookup"><span data-stu-id="70e6d-214">Where you have 2 Edge servers in the pool, this results in 9 public IP addresses, where 3 are used for the HLB VIPs, and one for each Edge server interface (a total of six for the servers)</span></span>

  - <span data-ttu-id="70e6d-215">Pour le service Edge d’accès et le service Edge de conférence Web (et l’utilisation de la traduction d’adresses réseau sur le HLB), le client contacte l’adresse VIP, l’adresse VIP remplace l’adresse IP source du client par sa propre adresse IP.</span><span class="sxs-lookup"><span data-stu-id="70e6d-215">For the Access Edge service and Web Conferencing Edge service, (and using NAT on the HLB) the client contacts the VIP, the VIP changes the source IP address from the client to its own IP address.</span></span> <span data-ttu-id="70e6d-216">L’interface du serveur adresse l’adresse d’expéditeur au VIP, l’adresse VIP modifie l’adresse source à partir de l’adresse IP de l’interface du serveur et envoie le paquet au client.</span><span class="sxs-lookup"><span data-stu-id="70e6d-216">The server interface addresses the return address to the VIP, the VIP changes the source address from the server interface IP address and sends the packet to the client</span></span>

  - <span data-ttu-id="70e6d-217">Pour le service Edge A/V, l’adresse VIP ne doit pas modifier l’adresse IP source, et l’adresse réelle du serveur est directement renvoyée au client : vous ne pouvez pas configurer le NAT sur le HLB pour le trafic AV</span><span class="sxs-lookup"><span data-stu-id="70e6d-217">For the A/V Edge service, the VIP must NOT change the source IP address, and the real server address is returned to the client directly – you cannot configure NAT on the HLB for AV traffic</span></span>
    
      - <span data-ttu-id="70e6d-218">Si le client envoie une demande à l’adresse VIP de HLB, la réponse doit être retirée du VIP HLB</span><span class="sxs-lookup"><span data-stu-id="70e6d-218">If the client sends a request to the HLB VIP, the response must come back from the HLB VIP</span></span>
    
      - <span data-ttu-id="70e6d-219">Si le client envoie une demande à l’adresse IP du serveur Edge, la réponse doit être retirée de l’adresse IP du serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="70e6d-219">If the client sends a request to the Edge IP, the response must come back from the Edge IP</span></span>

  - <span data-ttu-id="70e6d-220">Pour les AV, le pare-feu externe conserve l’adresse IP publique réelle du serveur pour tous les paquets.</span><span class="sxs-lookup"><span data-stu-id="70e6d-220">For AV, the external firewall will retain the real server public IP address for all packets</span></span>

  - <span data-ttu-id="70e6d-221">Une fois établi, le client à la communication de service Edge A/V est destiné au serveur réel et non au HLB</span><span class="sxs-lookup"><span data-stu-id="70e6d-221">Once established, client to A/V Edge service communication is to the real server, not the HLB</span></span>

  - <span data-ttu-id="70e6d-222">Le bord interne des serveurs et clients internes doit être routé et des itinéraires persistants sont définis pour tous les réseaux internes qui hébergent des serveurs ou des clients.</span><span class="sxs-lookup"><span data-stu-id="70e6d-222">Internal edge to internal servers and clients must be routed, and persistent routes are set for all internal networks that host servers or clients</span></span>

  - <span data-ttu-id="70e6d-223">Le protocole VIP du service Edge d’accès HLB agit comme passerelle par défaut pour chaque interface de serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="70e6d-223">The HLB Access Edge service VIP will act as the default gateway for each Edge server interface</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="70e6d-224">Pour plus d’informations sur la planification et la fonctionnalité de NAT, voir <A href="lync-server-2013-hardware-load-balancer-requirements.md">Configuration requise pour l’équilibrage de charge matérielle pour Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="70e6d-224">For further information on NAT planning and functionality, please refer to <A href="lync-server-2013-hardware-load-balancer-requirements.md">Hardware load balancer requirements for Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="70e6d-225">![Détails des protocoles et des ports du serveur Edge](images/Gg398739.1c193b80-98ab-4d59-a854-dbfdb5e209e2(OCS.15).jpg "Détails des protocoles et des ports du serveur Edge")</span><span class="sxs-lookup"><span data-stu-id="70e6d-225">![Edge Server ports and protocols details](images/Gg398739.1c193b80-98ab-4d59-a854-dbfdb5e209e2(OCS.15).jpg "Edge Server ports and protocols details")</span></span>

### <a name="external-port-settings-required-for-scaled-consolidated-edge-hardware-load-balanced-external-interface-virtual-ips"></a><span data-ttu-id="70e6d-226">Paramètres de port externe requis pour les bords consolidés mis à l’échelle, équilibrage de charge matérielle : IPs virtuel d’interface externe</span><span class="sxs-lookup"><span data-stu-id="70e6d-226">External Port Settings Required for Scaled Consolidated Edge, Hardware Load Balanced: External Interface Virtual IPs</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70e6d-227">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="70e6d-227">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="70e6d-228">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="70e6d-228">Source IP address</span></span></th>
<th><span data-ttu-id="70e6d-229">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="70e6d-229">Destination IP address</span></span></th>
<th><span data-ttu-id="70e6d-230">Remarques</span><span class="sxs-lookup"><span data-stu-id="70e6d-230">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70e6d-231">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="70e6d-231">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="70e6d-232">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-232">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-233">Service proxy XMPP (adresse IP du partage avec service Edge d’accès)</span><span class="sxs-lookup"><span data-stu-id="70e6d-233">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="70e6d-234">Le service proxy XMPP accepte le trafic de contacts XMPP dans les fédérations de XMPP définies</span><span class="sxs-lookup"><span data-stu-id="70e6d-234">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70e6d-235">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="70e6d-235">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="70e6d-236">Service proxy XMPP (adresse IP du partage avec service Edge d’accès)</span><span class="sxs-lookup"><span data-stu-id="70e6d-236">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="70e6d-237">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-237">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-238">Le service de proxy XMPP envoie le trafic aux contacts XMPP dans les fédérations de XMPP définies.</span><span class="sxs-lookup"><span data-stu-id="70e6d-238">XMPP Proxy service sends traffic to XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70e6d-239">/TCP/443 d’accès/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="70e6d-239">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="70e6d-240">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-240">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-241">Adresse VIP publique du service Edge d’accès</span><span class="sxs-lookup"><span data-stu-id="70e6d-241">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="70e6d-242">Trafic SIP client à serveur pour l’accès des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="70e6d-242">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70e6d-243">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="70e6d-243">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="70e6d-244">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-244">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-245">Adresse VIP publique du service Edge d’accès</span><span class="sxs-lookup"><span data-stu-id="70e6d-245">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="70e6d-246">Signalisation SIP, connectivité par messagerie instantanée privée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="70e6d-246">SIP signaling, federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70e6d-247">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="70e6d-247">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="70e6d-248">Adresse VIP publique du service Edge d’accès</span><span class="sxs-lookup"><span data-stu-id="70e6d-248">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="70e6d-249">Partenaire fédéré</span><span class="sxs-lookup"><span data-stu-id="70e6d-249">Federated partner</span></span></p></td>
<td><p><span data-ttu-id="70e6d-250">Signalisation SIP, connectivité par messagerie instantanée privée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="70e6d-250">SIP signaling, federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70e6d-251">PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="70e6d-251">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="70e6d-252">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-252">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-253">Adresse VIP publique du service Edge Conferencing Server Web</span><span class="sxs-lookup"><span data-stu-id="70e6d-253">Edge Server Web Conferencing Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="70e6d-254">Support de conférences Web</span><span class="sxs-lookup"><span data-stu-id="70e6d-254">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70e6d-255">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="70e6d-255">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="70e6d-256">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-256">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-257">Adresse VIP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="70e6d-257">Edge Server A/V Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="70e6d-258">STUN/activer la négociation des candidats via UDP/3478</span><span class="sxs-lookup"><span data-stu-id="70e6d-258">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70e6d-259">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="70e6d-259">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="70e6d-260">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-260">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-261">Adresse VIP publique du service Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="70e6d-261">Edge Server A/V Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="70e6d-262">STUN/activer la négociation des candidats via TCP/443</span><span class="sxs-lookup"><span data-stu-id="70e6d-262">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-internal-interface-virtual-ips"></a><span data-ttu-id="70e6d-263">Résumé du pare-feu pour les bords consolidés mis à l’échelle, équilibrage de charge matérielle : IPs virtuel d’interface</span><span class="sxs-lookup"><span data-stu-id="70e6d-263">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: Internal Interface Virtual IPs</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70e6d-264">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="70e6d-264">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="70e6d-265">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="70e6d-265">Source IP address</span></span></th>
<th><span data-ttu-id="70e6d-266">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="70e6d-266">Destination IP address</span></span></th>
<th><span data-ttu-id="70e6d-267">Remarques</span><span class="sxs-lookup"><span data-stu-id="70e6d-267">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70e6d-268">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="70e6d-268">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="70e6d-269">Tout (peut être défini en tant que directeur, adresse IP virtuelle du pool de réalisateurs, serveur frontal ou adresse IP virtuelle de pool frontal)</span><span class="sxs-lookup"><span data-stu-id="70e6d-269">Any (can be defined as Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)</span></span></p></td>
<td><p><span data-ttu-id="70e6d-270">Interface VIP interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="70e6d-270">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="70e6d-271">Trafic SIP sortant (à partir du réalisateur, adresse IP virtuelle du pool de directeurs, serveur frontal ou liste d’adresses IP virtuelles) vers l’adresse VIP de périphérie interne</span><span class="sxs-lookup"><span data-stu-id="70e6d-271">Outbound SIP traffic (from Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)to Internal Edge VIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70e6d-272">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="70e6d-272">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="70e6d-273">Interface VIP interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="70e6d-273">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="70e6d-274">Tout (peut être défini en tant que directeur, adresse IP virtuelle du pool de réalisateurs, serveur frontal ou adresse IP virtuelle de pool frontal)</span><span class="sxs-lookup"><span data-stu-id="70e6d-274">Any (can be defined as Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)</span></span></p></td>
<td><p><span data-ttu-id="70e6d-275">Trafic SIP entrant (adresse IP virtuelle du pool de directeurs, serveur frontal ou liste d’adresses IP virtuelle) à partir de l’interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="70e6d-275">Inbound SIP traffic (to Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70e6d-276">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="70e6d-276">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="70e6d-277">Tout (peut être défini en tant qu’adresse IP du serveur frontal ou adresse IP du pool frontal ou tout autre appareil de succursale survivant ou succursale Survivable à l’aide de ce serveur Edge)</span><span class="sxs-lookup"><span data-stu-id="70e6d-277">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="70e6d-278">Interface VIP interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="70e6d-278">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="70e6d-279">L’authentification des utilisateurs A/V (service d’authentification A/V) à partir du serveur frontal ou de l’adresse IP du pool frontal ou de tout appareil de succursale ou de succursale survivant utilisant ce serveur Edge</span><span class="sxs-lookup"><span data-stu-id="70e6d-279">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70e6d-280">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="70e6d-280">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="70e6d-281">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-281">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-282">Interface VIP interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="70e6d-282">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="70e6d-283">Chemin préféré pour le transfert de média A/V entre les utilisateurs internes et externes</span><span class="sxs-lookup"><span data-stu-id="70e6d-283">Preferred path for A/V media transfer between internal and external users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70e6d-284">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="70e6d-284">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="70e6d-285">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-285">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-286">Interface VIP interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="70e6d-286">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="70e6d-287">Chemin de secours pour le transfert de média A/V entre les utilisateurs internes et externes si la communication UDP ne peut pas être établie, le protocole TCP est utilisé pour le transfert de fichiers et le partage de bureau</span><span class="sxs-lookup"><span data-stu-id="70e6d-287">Fallback path for A/V media transfer between internal and external users if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70e6d-288">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="70e6d-288">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="70e6d-289">Interface VIP interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="70e6d-289">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="70e6d-290">Indifférente</span><span class="sxs-lookup"><span data-stu-id="70e6d-290">Any</span></span></p></td>
<td><p><span data-ttu-id="70e6d-291">Chemin de secours pour le transfert de média A/V entre les utilisateurs internes et externes si la communication UDP ne peut pas être établie, le protocole TCP est utilisé pour le transfert de fichiers et le partage de bureau</span><span class="sxs-lookup"><span data-stu-id="70e6d-291">Fallback path for A/V media transfer between internal and external users if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="70e6d-292">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="70e6d-292">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

