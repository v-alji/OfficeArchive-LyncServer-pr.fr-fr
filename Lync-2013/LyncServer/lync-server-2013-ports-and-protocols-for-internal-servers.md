---
title: 'Lync Server 2013 : ports et protocoles pour les serveurs internes'
description: 'Lync Server 2013 : ports et protocoles pour les serveurs internes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Ports and protocols for internal servers
ms:assetid: c94063f1-e802-4a61-be90-022fc185335e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398833(v=OCS.15)
ms:contentKeyID: 48185402
ms.date: 04/06/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d7d8f12c78c5dec5caacaeb1156f4d228b7cd591
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424246"
---
# <a name="ports-and-protocols-for-internal-servers-in-lync-server-2013"></a><span data-ttu-id="44ffa-103">Ports et protocoles pour les serveurs internes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="44ffa-103">Ports and protocols for internal servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="44ffa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="44ffa-104">

<span> </span></span></span>

<span data-ttu-id="44ffa-105">_**Dernière modification de la rubrique :** 2016-04-06_</span><span class="sxs-lookup"><span data-stu-id="44ffa-105">_**Topic Last Modified:** 2016-04-06_</span></span>

<span data-ttu-id="44ffa-106">Cette section résume les ports et les protocoles utilisés par les serveurs, les équilibreurs de charge et les clients dans le déploiement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="44ffa-106">This section summarizes the ports and protocols used by servers, load balancers, and clients in a Lync Server deployment.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="44ffa-107">Les clients Lync et Communicator intervenant dans le cadre d’une communication une à une, sont souvent désignés sous le nom d’égal à égal.</span><span class="sxs-lookup"><span data-stu-id="44ffa-107">Lync and Communicator clients when involved in a one to one communication, is often referred to as peer-to-peer.</span></span> <span data-ttu-id="44ffa-108">Techniquement, les deux clients communiquent en une seule conversation avec l’unité de contrôle multipoint (IMMCU) de messagerie instantanée au milieu.</span><span class="sxs-lookup"><span data-stu-id="44ffa-108">Technically, the two clients are communicating in a one to one conversation, with the Instant Messaging multipoint control unit (IMMCU) in the middle.</span></span> <span data-ttu-id="44ffa-109">IMMCU est un composant du serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="44ffa-109">The IMMCU is a component of Front End Server.</span></span> <span data-ttu-id="44ffa-110">Le placement du IMMCU dans le flux de travail de communication requis autorise l’enregistrement des détails des appels et d’autres fonctionnalités que le serveur frontal autorise.</span><span class="sxs-lookup"><span data-stu-id="44ffa-110">Placing the IMMCU in the required communication workflow allows call detail recording and other features that the Front End Server enables.</span></span> <span data-ttu-id="44ffa-111">La communication provient d’un port source dynamique du client vers le port de serveur frontal TLS/TCP/5061 (en partant du principe que l’utilisation de la sécurité de couche de transport recommandée).</span><span class="sxs-lookup"><span data-stu-id="44ffa-111">Communication is from a dynamic source port on the client to the Front End Server port TLS/TCP/5061 (assuming the use of the recommended transport layer security).</span></span> <span data-ttu-id="44ffa-112">Par conception, la communication d’égal à égal (et la messagerie instantanée à plusieurs parties) est possible uniquement lorsque Lync Server et IMMCU est actif et disponible.</span><span class="sxs-lookup"><span data-stu-id="44ffa-112">By design, peer-to-peer communication (as well as multi-party IM) is possible only when Lync Server and the IMMCU is active and available.</span></span>



</div>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="44ffa-113">Détails sur les ports et protocoles</span><span class="sxs-lookup"><span data-stu-id="44ffa-113">Port and Protocol Details</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="44ffa-114">Le pare-feu Windows doit être en cours d’exécution avant que vous ne démarriez les services Lync Server sur un serveur, car c’est le cas lorsque Lync Server ouvre les ports requis dans le pare-feu.</span><span class="sxs-lookup"><span data-stu-id="44ffa-114">Windows Firewall must be running before you start the Lync Server services on a server, because that is when Lync Server opens the required ports in the firewall.</span></span>



</div>

<span data-ttu-id="44ffa-115">Pour plus d’informations sur la configuration du pare-feu pour les composants Edge, voir [déterminer les exigences en matière de port et de pare-feu A/V externes pour Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="44ffa-115">For details about firewall configuration for edge components, see [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span></span>

<span data-ttu-id="44ffa-116">Le tableau suivant répertorie les ports qui doivent être ouverts sur chaque rôle serveur interne.</span><span class="sxs-lookup"><span data-stu-id="44ffa-116">The following table lists the ports that need to be open on each internal server role.</span></span>

### <a name="required-server-ports-by-server-role"></a><span data-ttu-id="44ffa-117">Ports de serveurs requis (par rôle serveur)</span><span class="sxs-lookup"><span data-stu-id="44ffa-117">Required Server Ports (by Server Role)</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="44ffa-118">Rôle serveur</span><span class="sxs-lookup"><span data-stu-id="44ffa-118">Server role</span></span></th>
<th><span data-ttu-id="44ffa-119">Nom du service</span><span class="sxs-lookup"><span data-stu-id="44ffa-119">Service name</span></span></th>
<th><span data-ttu-id="44ffa-120">Port</span><span class="sxs-lookup"><span data-stu-id="44ffa-120">Port</span></span></th>
<th><span data-ttu-id="44ffa-121">Protocole</span><span class="sxs-lookup"><span data-stu-id="44ffa-121">Protocol</span></span></th>
<th><span data-ttu-id="44ffa-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="44ffa-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-123">Tous les serveurs</span><span class="sxs-lookup"><span data-stu-id="44ffa-123">All Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-124">SQL Browser</span><span class="sxs-lookup"><span data-stu-id="44ffa-124">SQL Browser</span></span></p></td>
<td><p><span data-ttu-id="44ffa-125">1434</span><span class="sxs-lookup"><span data-stu-id="44ffa-125">1434</span></span></p></td>
<td><p><span data-ttu-id="44ffa-126">UDP</span><span class="sxs-lookup"><span data-stu-id="44ffa-126">UDP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-127">Navigateur SQL pour la copie locale répliquée de la base de données centrale de la Banque d’administration.</span><span class="sxs-lookup"><span data-stu-id="44ffa-127">SQL Browser for the local replicated copy of the Central Management Store database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-128">serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-128">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-129">Service Lync Server Front-End</span><span class="sxs-lookup"><span data-stu-id="44ffa-129">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-130">5060</span><span class="sxs-lookup"><span data-stu-id="44ffa-130">5060</span></span></p></td>
<td><p><span data-ttu-id="44ffa-131">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-131">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-132">Utilisé facultativement par les serveurs Standard Edition Server et les serveurs frontaux pour les itinéraires statiques vers des services approuvés, comme les serveurs de contrôle d’appel distant.</span><span class="sxs-lookup"><span data-stu-id="44ffa-132">Optionally used by Standard Edition servers and Front End Servers for static routes to trusted services, such as remote call control servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-133">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-133">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-134">Service Lync Server Front-End</span><span class="sxs-lookup"><span data-stu-id="44ffa-134">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-135">5061</span><span class="sxs-lookup"><span data-stu-id="44ffa-135">5061</span></span></p></td>
<td><p><span data-ttu-id="44ffa-136">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-136">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-137">Utilisé par les serveurs Standard Edition Server et les pools frontaux pour toutes les communications SIP internes entre serveurs (MTLS), pour les communications SIP entre serveurs et clients (TLS) et pour les communications SIP entre serveurs frontaux et serveurs de médiation (MTLS).</span><span class="sxs-lookup"><span data-stu-id="44ffa-137">Used by Standard Edition servers and Front End pools for all internal SIP communications between servers (MTLS), for SIP communications between Server and Client (TLS) and for SIP communications between Front End Servers and Mediation Servers (MTLS).</span></span> <span data-ttu-id="44ffa-138">Également utilisé pour communiquer avec le serveur de surveillance.</span><span class="sxs-lookup"><span data-stu-id="44ffa-138">Also used for communications with Monitoring Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-139">serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-139">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-140">Service Lync Server Front-End</span><span class="sxs-lookup"><span data-stu-id="44ffa-140">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-141">444</span><span class="sxs-lookup"><span data-stu-id="44ffa-141">444</span></span></p></td>
<td><p><span data-ttu-id="44ffa-142">HTTPS</span><span class="sxs-lookup"><span data-stu-id="44ffa-142">HTTPS</span></span></p>
<p><span data-ttu-id="44ffa-143">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-143">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-144">Utilisé pour la communication HTTPs entre le focus (composant serveur Lync qui gère l’état de la Conférence) et les serveurs individuels.</span><span class="sxs-lookup"><span data-stu-id="44ffa-144">Used for HTTPS communication between the Focus (the Lync Server component that manages conference state) and the individual servers.</span></span></p>
<p><span data-ttu-id="44ffa-145">Ce port est également utilisé pour la communication TCP entre les appareils succursales Survivables et les serveurs frontaux.</span><span class="sxs-lookup"><span data-stu-id="44ffa-145">This port is also used for TCP communication between Survivable Branch Appliances and Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-146">serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-146">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-147">Service Lync Server Front-End</span><span class="sxs-lookup"><span data-stu-id="44ffa-147">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-148">135</span><span class="sxs-lookup"><span data-stu-id="44ffa-148">135</span></span></p></td>
<td><p><span data-ttu-id="44ffa-149">DCOM et appel de procédure distante (RPC)</span><span class="sxs-lookup"><span data-stu-id="44ffa-149">DCOM and remote procedure call (RPC)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-150">Utilisé pour les opérations DCOM, telles que le déplacement des utilisateurs, la synchronisation du réplicateur d’utilisateurs et la synchronisation du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="44ffa-150">Used for DCOM based operations such as Moving Users, User Replicator Synchronization, and Address Book Synchronization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-151">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-151">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-152">Service de conférence par messagerie instantanée Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-152">Lync Server IM Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-153">5062</span><span class="sxs-lookup"><span data-stu-id="44ffa-153">5062</span></span></p></td>
<td><p><span data-ttu-id="44ffa-154">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-154">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-155">Utilisé pour les demandes SIP entrantes dans le cadre de conférences de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="44ffa-155">Used for incoming SIP requests for instant messaging (IM) conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-156">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-156">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-157">Service de conférence Web Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-157">Lync Server Web Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-158">8057</span><span class="sxs-lookup"><span data-stu-id="44ffa-158">8057</span></span></p></td>
<td><p><span data-ttu-id="44ffa-159">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-159">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-160">Utilisé pour l’écoute des connexions PSOM (Persistent Shared Object Model) à partir d’un client.</span><span class="sxs-lookup"><span data-stu-id="44ffa-160">Used to listen for Persistent Shared Object Model (PSOM) connections from client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-161">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-161">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-162">Service de compatibilité des conférences Web de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-162">Lync Server Web Conferencing Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-163">8058</span><span class="sxs-lookup"><span data-stu-id="44ffa-163">8058</span></span></p></td>
<td><p><span data-ttu-id="44ffa-164">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-164">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-165">Utilisé pour écouter les connexions PSOM (persistent Shared Object mode) du client Live Meeting et des versions précédentes de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="44ffa-165">Used to listen for Persistent Shared Object Model (PSOM) connections from the Live Meeting client and previous versions of Lync Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-166">serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-166">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-167">Service de visioconférence Lync Server audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="44ffa-167">Lync Server Audio/Video Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-168">5063</span><span class="sxs-lookup"><span data-stu-id="44ffa-168">5063</span></span></p></td>
<td><p><span data-ttu-id="44ffa-169">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-169">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-170">Utilisé pour les demandes SIP entrantes dans le cadre de conférences audio/vidéo (A/V).</span><span class="sxs-lookup"><span data-stu-id="44ffa-170">Used for incoming SIP requests for audio/video (A/V) conferencing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-171">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-171">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-172">Service de visioconférence Lync Server audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="44ffa-172">Lync Server Audio/Video Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-173">57501-65535</span><span class="sxs-lookup"><span data-stu-id="44ffa-173">57501-65535</span></span></p></td>
<td><p><span data-ttu-id="44ffa-174">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="44ffa-174">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-175">Plage de ports multimédias utilisée pour les conférences vidéo.</span><span class="sxs-lookup"><span data-stu-id="44ffa-175">Media port range used for video conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-176">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-176">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-177">Service de compatibilité Web de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-177">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-178">80</span><span class="sxs-lookup"><span data-stu-id="44ffa-178">80</span></span></p></td>
<td><p><span data-ttu-id="44ffa-179">HTTP</span><span class="sxs-lookup"><span data-stu-id="44ffa-179">HTTP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-180">Utilisé pour les communications à partir des serveurs frontaux vers les noms de domaine complets des batteries de serveurs Web (URL utilisées par les composants Web IIS) lorsque HTTPS n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="44ffa-180">Used for communication from Front End Servers to the web farm FQDNs (the URLs used by IIS web components) when HTTPS is not used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-181">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-181">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-182">Service de compatibilité Web de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-182">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-183">443</span><span class="sxs-lookup"><span data-stu-id="44ffa-183">443</span></span></p></td>
<td><p><span data-ttu-id="44ffa-184">HTTPS</span><span class="sxs-lookup"><span data-stu-id="44ffa-184">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="44ffa-185">Utilisé pour les communications à partir des serveurs frontaux vers les noms de domaine complets des batteries de serveurs Web (URL utilisées par les composants Web IIS).</span><span class="sxs-lookup"><span data-stu-id="44ffa-185">Used for communication from Front End Servers to the web farm FQDNs (the URLs used by IIS web components).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-186">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-186">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-187">Service de compatibilité Web de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-187">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-188">8080</span><span class="sxs-lookup"><span data-stu-id="44ffa-188">8080</span></span></p></td>
<td><p><span data-ttu-id="44ffa-189">TCP et HTTP</span><span class="sxs-lookup"><span data-stu-id="44ffa-189">TCP and HTTP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-190">Utilisé par les composants web pour l’accès externe.</span><span class="sxs-lookup"><span data-stu-id="44ffa-190">Used by web components for external access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-191">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-191">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-192">Composant de serveur web</span><span class="sxs-lookup"><span data-stu-id="44ffa-192">Web server component</span></span></p></td>
<td><p><span data-ttu-id="44ffa-193">4443</span><span class="sxs-lookup"><span data-stu-id="44ffa-193">4443</span></span></p></td>
<td><p><span data-ttu-id="44ffa-194">HTTPS</span><span class="sxs-lookup"><span data-stu-id="44ffa-194">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="44ffa-195">Communications HTTPS (du proxy inverse) et HTTPS inter-pool frontal pour connexion à la découverte automatique.</span><span class="sxs-lookup"><span data-stu-id="44ffa-195">HTTPS (from Reverse Proxy) and HTTPS Front End inter-pool communications for Autodiscover sign-in.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-196">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-196">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-197">Composant de serveur web</span><span class="sxs-lookup"><span data-stu-id="44ffa-197">Web server component</span></span></p></td>
<td><p><span data-ttu-id="44ffa-198">8060</span><span class="sxs-lookup"><span data-stu-id="44ffa-198">8060</span></span></p></td>
<td><p><span data-ttu-id="44ffa-199">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-199">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-200">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-200">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-201">Composant de serveur web</span><span class="sxs-lookup"><span data-stu-id="44ffa-201">Web server component</span></span></p></td>
<td><p><span data-ttu-id="44ffa-202">8061</span><span class="sxs-lookup"><span data-stu-id="44ffa-202">8061</span></span></p></td>
<td><p><span data-ttu-id="44ffa-203">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-203">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-204">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-204">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-205">Composant des services de mobilité</span><span class="sxs-lookup"><span data-stu-id="44ffa-205">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="44ffa-206">5086</span><span class="sxs-lookup"><span data-stu-id="44ffa-206">5086</span></span></p></td>
<td><p><span data-ttu-id="44ffa-207">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-207">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-208">Port SIP utilisé pour les processus internes des services de mobilité.</span><span class="sxs-lookup"><span data-stu-id="44ffa-208">SIP port used by Mobility Services internal processes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-209">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-209">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-210">Composant des services de mobilité</span><span class="sxs-lookup"><span data-stu-id="44ffa-210">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="44ffa-211">5087</span><span class="sxs-lookup"><span data-stu-id="44ffa-211">5087</span></span></p></td>
<td><p><span data-ttu-id="44ffa-212">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-212">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-213">Port SIP utilisé pour les processus internes des services de mobilité.</span><span class="sxs-lookup"><span data-stu-id="44ffa-213">SIP port used by Mobility Services internal processes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-214">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-214">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-215">Composant des services de mobilité</span><span class="sxs-lookup"><span data-stu-id="44ffa-215">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="44ffa-216">443</span><span class="sxs-lookup"><span data-stu-id="44ffa-216">443</span></span></p></td>
<td><p><span data-ttu-id="44ffa-217">HTTPS</span><span class="sxs-lookup"><span data-stu-id="44ffa-217">HTTPS</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-218">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-218">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-219">Service de surveillance des conférences de Lync Server (Conférence rendez-vous)</span><span class="sxs-lookup"><span data-stu-id="44ffa-219">Lync Server Conferencing Attendant service (dial-in conferencing)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-220">5064</span><span class="sxs-lookup"><span data-stu-id="44ffa-220">5064</span></span></p></td>
<td><p><span data-ttu-id="44ffa-221">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-221">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-222">Utilisé pour les demandes SIP entrantes dans le cadre de conférences rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="44ffa-222">Used for incoming SIP requests for dial-in conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-223">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-223">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-224">Service de surveillance des conférences de Lync Server (Conférence rendez-vous)</span><span class="sxs-lookup"><span data-stu-id="44ffa-224">Lync Server Conferencing Attendant service (dial-in conferencing)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-225">5072</span><span class="sxs-lookup"><span data-stu-id="44ffa-225">5072</span></span></p></td>
<td><p><span data-ttu-id="44ffa-226">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-226">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-227">Utilisé pour les demandes SIP entrantes pour le service d’assistance téléphonique (Conférence rendez-vous).</span><span class="sxs-lookup"><span data-stu-id="44ffa-227">Used for incoming SIP requests for Attendant (dial in conferencing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-228">Serveurs frontaux qui exécutent également un serveur de médiation colocalisé.</span><span class="sxs-lookup"><span data-stu-id="44ffa-228">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="44ffa-229">Service médiation de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-229">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-230">5070</span><span class="sxs-lookup"><span data-stu-id="44ffa-230">5070</span></span></p></td>
<td><p><span data-ttu-id="44ffa-231">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-231">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-232">Utilisé par le serveur de médiation pour les demandes entrantes du serveur frontal vers le serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="44ffa-232">Used by the Mediation Server for incoming requests from the Front End Server to the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-233">Serveurs frontaux qui exécutent également un serveur de médiation colocalisé.</span><span class="sxs-lookup"><span data-stu-id="44ffa-233">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="44ffa-234">Service médiation de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-234">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-235">5067</span><span class="sxs-lookup"><span data-stu-id="44ffa-235">5067</span></span></p></td>
<td><p><span data-ttu-id="44ffa-236">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-236">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-237">Utilisé pour les demandes SIP entrantes de la passerelle PSTN vers le serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="44ffa-237">Used for incoming SIP requests from the PSTN gateway to the Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-238">Serveurs frontaux qui exécutent également un serveur de médiation colocalisé.</span><span class="sxs-lookup"><span data-stu-id="44ffa-238">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="44ffa-239">Service médiation de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-239">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-240">5068</span><span class="sxs-lookup"><span data-stu-id="44ffa-240">5068</span></span></p></td>
<td><p><span data-ttu-id="44ffa-241">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-241">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-242">Utilisé pour les demandes SIP entrantes de la passerelle PSTN vers le serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="44ffa-242">Used for incoming SIP requests from the PSTN gateway to the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-243">Serveurs frontaux qui exécutent également un serveur de médiation colocalisé.</span><span class="sxs-lookup"><span data-stu-id="44ffa-243">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="44ffa-244">Service médiation de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-244">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-245">5081</span><span class="sxs-lookup"><span data-stu-id="44ffa-245">5081</span></span></p></td>
<td><p><span data-ttu-id="44ffa-246">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-246">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-247">Utilisé pour les demandes SIP sortantes du serveur de médiation vers la passerelle PSTN.</span><span class="sxs-lookup"><span data-stu-id="44ffa-247">Used for outgoing SIP requests from the Mediation Server to the PSTN gateway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-248">Serveurs frontaux qui exécutent également un serveur de médiation colocalisé.</span><span class="sxs-lookup"><span data-stu-id="44ffa-248">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="44ffa-249">Service médiation de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-249">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-250">5082</span><span class="sxs-lookup"><span data-stu-id="44ffa-250">5082</span></span></p></td>
<td><p><span data-ttu-id="44ffa-251">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-251">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-252">Utilisé pour les demandes SIP sortantes du serveur de médiation vers la passerelle PSTN.</span><span class="sxs-lookup"><span data-stu-id="44ffa-252">Used for outgoing SIP requests from the Mediation Server to the PSTN gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-253">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-253">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-254">Service de partage d’application Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-254">Lync Server Application Sharing service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-255">5065</span><span class="sxs-lookup"><span data-stu-id="44ffa-255">5065</span></span></p></td>
<td><p><span data-ttu-id="44ffa-256">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-256">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-257">Utilisé pour les demandes d’écoute SIP entrantes dans le cadre du partage d’application.</span><span class="sxs-lookup"><span data-stu-id="44ffa-257">Used for incoming SIP listening requests for application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-258">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-258">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-259">Service de partage d’application Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-259">Lync Server Application Sharing service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-260">49152-65535</span><span class="sxs-lookup"><span data-stu-id="44ffa-260">49152-65535</span></span></p></td>
<td><p><span data-ttu-id="44ffa-261">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-261">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-262">Plage de ports multimédias utilisée pour le partage d’application.</span><span class="sxs-lookup"><span data-stu-id="44ffa-262">Media port range used for application sharing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-263">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-263">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-264">Service d’annonce Lync Server Conferencing</span><span class="sxs-lookup"><span data-stu-id="44ffa-264">Lync Server Conferencing Announcement service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-265">5073</span><span class="sxs-lookup"><span data-stu-id="44ffa-265">5073</span></span></p></td>
<td><p><span data-ttu-id="44ffa-266">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-266">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-267">Utilisé pour les demandes SIP entrantes pour le service d’annonce Lync Server Conferencing (c’est-à-dire pour la Conférence rendez-vous).</span><span class="sxs-lookup"><span data-stu-id="44ffa-267">Used for incoming SIP requests for the Lync Server Conferencing Announcement service (that is, for dial-in conferencing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-268">serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-268">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-269">service de parcage d’appel Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-269">Lync Server Call Park service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-270">5075</span><span class="sxs-lookup"><span data-stu-id="44ffa-270">5075</span></span></p></td>
<td><p><span data-ttu-id="44ffa-271">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-271">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-272">Utilisé pour les demandes SIP entrantes de l’application de parcage d’appel.</span><span class="sxs-lookup"><span data-stu-id="44ffa-272">Used for incoming SIP requests for the Call Park application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-273">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-273">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-274">Service de test audio de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-274">Lync Server Audio Test service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-275">5076</span><span class="sxs-lookup"><span data-stu-id="44ffa-275">5076</span></span></p></td>
<td><p><span data-ttu-id="44ffa-276">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-276">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-277">Utilisé pour les demandes SIP entrantes du service de test audio.</span><span class="sxs-lookup"><span data-stu-id="44ffa-277">Used for incoming SIP requests for the Audio Test service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-278">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-278">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-279">Non applicable</span><span class="sxs-lookup"><span data-stu-id="44ffa-279">Not applicable</span></span></p></td>
<td><p><span data-ttu-id="44ffa-280">5066</span><span class="sxs-lookup"><span data-stu-id="44ffa-280">5066</span></span></p></td>
<td><p><span data-ttu-id="44ffa-281">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-281">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-282">Utilisé pour la passerelle Enhanced 9-1-1 (E9-1-1) sortante.</span><span class="sxs-lookup"><span data-stu-id="44ffa-282">Used for outbound Enhanced 9-1-1 (E9-1-1) gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-283">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-283">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-284">service Response Group Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-284">Lync Server Response Group service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-285">5071</span><span class="sxs-lookup"><span data-stu-id="44ffa-285">5071</span></span></p></td>
<td><p><span data-ttu-id="44ffa-286">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-286">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-287">Utilisé pour les demandes SIP entrantes de l’application Response Group.</span><span class="sxs-lookup"><span data-stu-id="44ffa-287">Used for incoming SIP requests for the Response Group application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-288">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-288">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-289">service Response Group Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-289">Lync Server Response Group service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-290">8404</span><span class="sxs-lookup"><span data-stu-id="44ffa-290">8404</span></span></p></td>
<td><p><span data-ttu-id="44ffa-291">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-291">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-292">Utilisé pour les demandes SIP entrantes de l’application Response Group.</span><span class="sxs-lookup"><span data-stu-id="44ffa-292">Used for incoming SIP requests for the Response Group application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-293">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-293">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-294">Service de stratégie de bande passante de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-294">Lync Server Bandwidth Policy Service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-295">5080</span><span class="sxs-lookup"><span data-stu-id="44ffa-295">5080</span></span></p></td>
<td><p><span data-ttu-id="44ffa-296">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-296">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-297">Utilisé pour le contrôle d’admission des appels par le service de stratégie de bande passante, lui-même utilisé pour le trafic TURN Edge A/V.</span><span class="sxs-lookup"><span data-stu-id="44ffa-297">Used for call admission control by the Bandwidth Policy service for A/V Edge TURN traffic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-298">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="44ffa-298">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-299">Service de stratégie de bande passante de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-299">Lync Server Bandwidth Policy Service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-300">448</span><span class="sxs-lookup"><span data-stu-id="44ffa-300">448</span></span></p></td>
<td><p><span data-ttu-id="44ffa-301">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-301">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-302">Utilisé pour le contrôle d’admission des appels par le service de stratégie de bande passante de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="44ffa-302">Used for call admission control by the Lync Server Bandwidth Policy Service.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-303">Serveurs frontaux dans lesquels réside le magasin de gestion central</span><span class="sxs-lookup"><span data-stu-id="44ffa-303">Front End Servers where the Central Management store resides</span></span></p></td>
<td><p><span data-ttu-id="44ffa-304">Service de l’agent réplicateur de serveurs maîtres de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-304">Lync Server Master Replicator Agent service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-305">445</span><span class="sxs-lookup"><span data-stu-id="44ffa-305">445</span></span></p></td>
<td><p><span data-ttu-id="44ffa-306">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-306">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-307">Utilisé pour transmettre les données de configuration du magasin central de gestion à des serveurs exécutant Lync Server.</span><span class="sxs-lookup"><span data-stu-id="44ffa-307">Used to push configuration data from the Central Management store to servers running Lync Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-308">Tous les serveurs</span><span class="sxs-lookup"><span data-stu-id="44ffa-308">All Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-309">SQL Browser</span><span class="sxs-lookup"><span data-stu-id="44ffa-309">SQL Browser</span></span></p></td>
<td><p><span data-ttu-id="44ffa-310">1434</span><span class="sxs-lookup"><span data-stu-id="44ffa-310">1434</span></span></p></td>
<td><p><span data-ttu-id="44ffa-311">UDP</span><span class="sxs-lookup"><span data-stu-id="44ffa-311">UDP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-312">Navigateur SQL pour la copie locale répliquée des données du magasin de gestion central dans l’instance SQL Server locale</span><span class="sxs-lookup"><span data-stu-id="44ffa-312">SQL Browser for local replicated copy of Central Management store data in local SQL Server instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-313">Tous les serveurs internes</span><span class="sxs-lookup"><span data-stu-id="44ffa-313">All internal servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-314">Divers</span><span class="sxs-lookup"><span data-stu-id="44ffa-314">Various</span></span></p></td>
<td><p><span data-ttu-id="44ffa-315">49152-57500</span><span class="sxs-lookup"><span data-stu-id="44ffa-315">49152-57500</span></span></p></td>
<td><p><span data-ttu-id="44ffa-316">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="44ffa-316">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-317">Plage de ports multimédias utilisée pour les conférences audio sur tous les serveurs internes.</span><span class="sxs-lookup"><span data-stu-id="44ffa-317">Media port range used for audio conferencing on all internal servers.</span></span> <span data-ttu-id="44ffa-318">Utilisé par tous les serveurs qui terminent les appels audio : serveurs front-end (pour le service de surveillance des conférences de Lync Server, service d’annonce de conférence Lync Server et service de visioconférence Lync Server) et serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="44ffa-318">Used by all servers that terminate audio: Front End Servers (for Lync Server Conferencing Attendant service, Lync Server Conferencing Announcement service, and Lync Server Audio/Video Conferencing service), and Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-319">Serveurs Office Web Apps Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-319">Office Web Apps Servers</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="44ffa-320">443</span><span class="sxs-lookup"><span data-stu-id="44ffa-320">443</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="44ffa-321">Utilisé par Lync Server 2013 pour la connexion à Office Web Apps Server.</span><span class="sxs-lookup"><span data-stu-id="44ffa-321">Used by Lync Server 2013 to connect to Office Web Apps Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-322">directeurs</span><span class="sxs-lookup"><span data-stu-id="44ffa-322">Directors</span></span></p></td>
<td><p><span data-ttu-id="44ffa-323">Service Lync Server Front-End</span><span class="sxs-lookup"><span data-stu-id="44ffa-323">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-324">5060</span><span class="sxs-lookup"><span data-stu-id="44ffa-324">5060</span></span></p></td>
<td><p><span data-ttu-id="44ffa-325">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-325">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-326">Utilisé facultativement pour les itinéraires statiques vers des services approuvés, comme les serveurs de contrôle d’appel distant.</span><span class="sxs-lookup"><span data-stu-id="44ffa-326">Optionally used for static routes to trusted services, such as remote call control servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-327">Directeurs</span><span class="sxs-lookup"><span data-stu-id="44ffa-327">Directors</span></span></p></td>
<td><p><span data-ttu-id="44ffa-328">Service Lync Server Front-End</span><span class="sxs-lookup"><span data-stu-id="44ffa-328">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-329">444</span><span class="sxs-lookup"><span data-stu-id="44ffa-329">444</span></span></p></td>
<td><p><span data-ttu-id="44ffa-330">HTTPS</span><span class="sxs-lookup"><span data-stu-id="44ffa-330">HTTPS</span></span></p>
<p><span data-ttu-id="44ffa-331">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-331">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-332">Communication entre serveurs frontaux et directeurs.</span><span class="sxs-lookup"><span data-stu-id="44ffa-332">Inter-server communication between Front End and Director.</span></span> <span data-ttu-id="44ffa-333">Par ailleurs, le certificat client est publié (pour les serveurs frontaux) ou validé si le certificat client a déjà été publié.</span><span class="sxs-lookup"><span data-stu-id="44ffa-333">Additionally, client certificate publish (to Front End Servers) or validate if the client certificate has already been published.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-334">directeurs</span><span class="sxs-lookup"><span data-stu-id="44ffa-334">Directors</span></span></p></td>
<td><p><span data-ttu-id="44ffa-335">Service de compatibilité Web de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-335">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-336">80</span><span class="sxs-lookup"><span data-stu-id="44ffa-336">80</span></span></p></td>
<td><p><span data-ttu-id="44ffa-337">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-337">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-p105">Utilisé pour les communications initiales entre les directeurs et les noms de domaine complets des batteries de serveurs Web (URL utilisées par les composants Web IIS). En fonctionnement normal, bascule vers le trafic HTTPS en utilisant le port 443 et le type de protocole TCP.</span><span class="sxs-lookup"><span data-stu-id="44ffa-p105">Used for initial communication from Directors to the web farm FQDNs (the URLs used by IIS web components). In normal operation, will switch to HTTPS traffic, using port 443 and protocol type TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-340">Directeurs</span><span class="sxs-lookup"><span data-stu-id="44ffa-340">Directors</span></span></p></td>
<td><p><span data-ttu-id="44ffa-341">Service de compatibilité Web de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-341">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-342">443</span><span class="sxs-lookup"><span data-stu-id="44ffa-342">443</span></span></p></td>
<td><p><span data-ttu-id="44ffa-343">HTTPS</span><span class="sxs-lookup"><span data-stu-id="44ffa-343">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="44ffa-344">Utilisé pour les communications entre les directeurs et les noms de domaine complets des batteries de serveurs Web (URL utilisées par les composants Web IIS).</span><span class="sxs-lookup"><span data-stu-id="44ffa-344">Used for communication from Directors to the web farm FQDNs (the URLs used by IIS web components).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-345">Directeurs</span><span class="sxs-lookup"><span data-stu-id="44ffa-345">Directors</span></span></p></td>
<td><p><span data-ttu-id="44ffa-346">Service Lync Server Front-End</span><span class="sxs-lookup"><span data-stu-id="44ffa-346">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-347">5061</span><span class="sxs-lookup"><span data-stu-id="44ffa-347">5061</span></span></p></td>
<td><p><span data-ttu-id="44ffa-348">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-348">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-349">Utilisé pour les communications internes entre serveurs et pour les connexions client.</span><span class="sxs-lookup"><span data-stu-id="44ffa-349">Used for internal communications between servers and for client connections.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-350">Serveurs de médiation</span><span class="sxs-lookup"><span data-stu-id="44ffa-350">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-351">Service médiation de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-351">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-352">5070</span><span class="sxs-lookup"><span data-stu-id="44ffa-352">5070</span></span></p></td>
<td><p><span data-ttu-id="44ffa-353">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-353">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-354">Utilisé par le serveur de médiation pour les demandes entrantes du serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="44ffa-354">Used by the Mediation Server for incoming requests from the Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-355">Serveurs de médiation</span><span class="sxs-lookup"><span data-stu-id="44ffa-355">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-356">Service médiation de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-356">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-357">5067</span><span class="sxs-lookup"><span data-stu-id="44ffa-357">5067</span></span></p></td>
<td><p><span data-ttu-id="44ffa-358">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-358">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-359">Utilisé pour les demandes SIP entrantes de la passerelle PSTN.</span><span class="sxs-lookup"><span data-stu-id="44ffa-359">Used for incoming SIP requests from the PSTN gateway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-360">Serveurs de médiation</span><span class="sxs-lookup"><span data-stu-id="44ffa-360">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-361">Service médiation de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-361">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-362">5068</span><span class="sxs-lookup"><span data-stu-id="44ffa-362">5068</span></span></p></td>
<td><p><span data-ttu-id="44ffa-363">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-363">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-364">Utilisé pour les demandes SIP entrantes de la passerelle PSTN.</span><span class="sxs-lookup"><span data-stu-id="44ffa-364">Used for incoming SIP requests from the PSTN gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-365">Serveurs de médiation</span><span class="sxs-lookup"><span data-stu-id="44ffa-365">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="44ffa-366">Service médiation de Lync Server</span><span class="sxs-lookup"><span data-stu-id="44ffa-366">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-367">5070</span><span class="sxs-lookup"><span data-stu-id="44ffa-367">5070</span></span></p></td>
<td><p><span data-ttu-id="44ffa-368">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-368">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-369">Utilisé pour les demandes SIP des serveurs frontaux.</span><span class="sxs-lookup"><span data-stu-id="44ffa-369">Used for SIP requests from the Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-370">Serveur frontal de conversation permanente</span><span class="sxs-lookup"><span data-stu-id="44ffa-370">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="44ffa-371">SIP de conversation permanente</span><span class="sxs-lookup"><span data-stu-id="44ffa-371">Persistent Chat SIP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-372">5041</span><span class="sxs-lookup"><span data-stu-id="44ffa-372">5041</span></span></p></td>
<td><p><span data-ttu-id="44ffa-373">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-373">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-374">Serveur frontal de conversation permanente</span><span class="sxs-lookup"><span data-stu-id="44ffa-374">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="44ffa-375">Windows Communication Foundation (WCF) de conversation permanente</span><span class="sxs-lookup"><span data-stu-id="44ffa-375">Persistent Chat Windows Communication Foundation (WCF)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-376">881</span><span class="sxs-lookup"><span data-stu-id="44ffa-376">881</span></span></p></td>
<td><p><span data-ttu-id="44ffa-377">TCP (TLS) et TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-377">TCP (TLS) and TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-378">Serveur frontal de conversation permanente</span><span class="sxs-lookup"><span data-stu-id="44ffa-378">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="44ffa-379">Service de transfert de fichiers de conversation permanente</span><span class="sxs-lookup"><span data-stu-id="44ffa-379">Persistent Chat File Transfer Service</span></span></p></td>
<td><p><span data-ttu-id="44ffa-380">443</span><span class="sxs-lookup"><span data-stu-id="44ffa-380">443</span></span></p></td>
<td><p><span data-ttu-id="44ffa-381">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-381">TCP (TLS)</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="44ffa-382">Certains scénarios de contrôle d’appel distant requièrent une connexion TCP entre le serveur frontal ou le directeur et le PBX.</span><span class="sxs-lookup"><span data-stu-id="44ffa-382">Some remote call control scenarios require a TCP connection between the Front End Server or Director and the PBX.</span></span> <span data-ttu-id="44ffa-383">Même si Lync Server n’utilise plus 5060 port TCP, lors du déploiement d’un contrôle d’appel distant, vous créez une configuration de serveur approuvé, qui associe le nom de domaine complet du serveur de ligne RCC au port TCP utilisé par le serveur frontal ou le directeur pour se connecter au système PBX.</span><span class="sxs-lookup"><span data-stu-id="44ffa-383">Although Lync Server no longer uses TCP port 5060, during remote call control deployment you create a trusted server configuration, which associates the RCC Line Server FQDN with the TCP port that the Front End Server or Director will use to connect to the PBX system.</span></span> <span data-ttu-id="44ffa-384">Pour plus d’informations, voir l’applet de connexion <STRONG>CsTrustedApplicationComputer</STRONG> dans la documentation Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="44ffa-384">For details, see the <STRONG>CsTrustedApplicationComputer</STRONG> cmdlet in the Lync Server Management Shell documentation.</span></span>



</div>

<span data-ttu-id="44ffa-385">Pour les pools utilisant uniquement l’équilibrage de la charge matérielle (et non pas l’équilibrage de charge DNS), le tableau suivant indique les ports qui doivent ouvrir les programmes d’équilibrage de la charge matérielle.</span><span class="sxs-lookup"><span data-stu-id="44ffa-385">For your pools that use only hardware load balancing (not DNS load balancing), the following table shows the ports that need to open the hardware load balancers.</span></span>

### <a name="hardware-load-balancer-ports-if-using-only-hardware-load-balancing"></a><span data-ttu-id="44ffa-386">Ports des programmes d’équilibrage de la charge matérielle si uniquement l’équilibrage de la charge matérielle est utilisé</span><span class="sxs-lookup"><span data-stu-id="44ffa-386">Hardware Load Balancer Ports if Using Only Hardware Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="44ffa-387">Programme d’équilibrage de charge</span><span class="sxs-lookup"><span data-stu-id="44ffa-387">Load Balancer</span></span></th>
<th><span data-ttu-id="44ffa-388">Port</span><span class="sxs-lookup"><span data-stu-id="44ffa-388">Port</span></span></th>
<th><span data-ttu-id="44ffa-389">Protocole</span><span class="sxs-lookup"><span data-stu-id="44ffa-389">Protocol</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-390">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-390">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-391">5061</span><span class="sxs-lookup"><span data-stu-id="44ffa-391">5061</span></span></p></td>
<td><p><span data-ttu-id="44ffa-392">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-392">TCP (TLS)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-393">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-393">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-394">444</span><span class="sxs-lookup"><span data-stu-id="44ffa-394">444</span></span></p></td>
<td><p><span data-ttu-id="44ffa-395">HTTPS</span><span class="sxs-lookup"><span data-stu-id="44ffa-395">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-396">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-396">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-397">135</span><span class="sxs-lookup"><span data-stu-id="44ffa-397">135</span></span></p></td>
<td><p><span data-ttu-id="44ffa-398">DCOM et appel de procédure distante (RPC)</span><span class="sxs-lookup"><span data-stu-id="44ffa-398">DCOM and remote procedure call (RPC)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-399">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-399">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-400">80</span><span class="sxs-lookup"><span data-stu-id="44ffa-400">80</span></span></p></td>
<td><p><span data-ttu-id="44ffa-401">HTTP</span><span class="sxs-lookup"><span data-stu-id="44ffa-401">HTTP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-402">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-402">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-403">8080</span><span class="sxs-lookup"><span data-stu-id="44ffa-403">8080</span></span></p></td>
<td><p><span data-ttu-id="44ffa-404">TCP : récupération client/appareil du certificat racine à partir du serveur frontal, notamment clients et appareils authentifiés par NTLM</span><span class="sxs-lookup"><span data-stu-id="44ffa-404">TCP - Client and device retrieval of root certificate from Front End Server – clients and devices authenticated by NTLM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-405">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-405">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-406">443</span><span class="sxs-lookup"><span data-stu-id="44ffa-406">443</span></span></p></td>
<td><p><span data-ttu-id="44ffa-407">HTTPS</span><span class="sxs-lookup"><span data-stu-id="44ffa-407">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-408">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-408">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-409">4443</span><span class="sxs-lookup"><span data-stu-id="44ffa-409">4443</span></span></p></td>
<td><p><span data-ttu-id="44ffa-410">HTTPS (du proxy inverse)</span><span class="sxs-lookup"><span data-stu-id="44ffa-410">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-411">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-411">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-412">5072</span><span class="sxs-lookup"><span data-stu-id="44ffa-412">5072</span></span></p></td>
<td><p><span data-ttu-id="44ffa-413">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-413">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-414">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-414">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-415">5073</span><span class="sxs-lookup"><span data-stu-id="44ffa-415">5073</span></span></p></td>
<td><p><span data-ttu-id="44ffa-416">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-416">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-417">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-417">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-418">5075</span><span class="sxs-lookup"><span data-stu-id="44ffa-418">5075</span></span></p></td>
<td><p><span data-ttu-id="44ffa-419">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-419">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-420">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-420">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-421">5076</span><span class="sxs-lookup"><span data-stu-id="44ffa-421">5076</span></span></p></td>
<td><p><span data-ttu-id="44ffa-422">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-422">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-423">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-423">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-424">5071</span><span class="sxs-lookup"><span data-stu-id="44ffa-424">5071</span></span></p></td>
<td><p><span data-ttu-id="44ffa-425">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-425">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-426">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-426">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-427">5080</span><span class="sxs-lookup"><span data-stu-id="44ffa-427">5080</span></span></p></td>
<td><p><span data-ttu-id="44ffa-428">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-428">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-429">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-429">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-430">448</span><span class="sxs-lookup"><span data-stu-id="44ffa-430">448</span></span></p></td>
<td><p><span data-ttu-id="44ffa-431">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-431">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-432">Programme d’équilibrage de charge du serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="44ffa-432">Mediation Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-433">5070</span><span class="sxs-lookup"><span data-stu-id="44ffa-433">5070</span></span></p></td>
<td><p><span data-ttu-id="44ffa-434">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-434">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-435">Programme d’équilibrage de charge du serveur frontal (si le pool exécute également le serveur de médiation)</span><span class="sxs-lookup"><span data-stu-id="44ffa-435">Front End Server load balancer (if the pool also runs Mediation Server)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-436">5070</span><span class="sxs-lookup"><span data-stu-id="44ffa-436">5070</span></span></p></td>
<td><p><span data-ttu-id="44ffa-437">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-437">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-438">Programme d’équilibrage de charge du directeur</span><span class="sxs-lookup"><span data-stu-id="44ffa-438">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-439">443</span><span class="sxs-lookup"><span data-stu-id="44ffa-439">443</span></span></p></td>
<td><p><span data-ttu-id="44ffa-440">HTTPS</span><span class="sxs-lookup"><span data-stu-id="44ffa-440">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-441">Programme d’équilibrage de charge du directeur</span><span class="sxs-lookup"><span data-stu-id="44ffa-441">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-442">444</span><span class="sxs-lookup"><span data-stu-id="44ffa-442">444</span></span></p></td>
<td><p><span data-ttu-id="44ffa-443">HTTPS</span><span class="sxs-lookup"><span data-stu-id="44ffa-443">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-444">Programme d’équilibrage de charge du directeur</span><span class="sxs-lookup"><span data-stu-id="44ffa-444">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-445">5061</span><span class="sxs-lookup"><span data-stu-id="44ffa-445">5061</span></span></p></td>
<td><p><span data-ttu-id="44ffa-446">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-446">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-447">Programme d’équilibrage de charge du directeur</span><span class="sxs-lookup"><span data-stu-id="44ffa-447">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-448">4443</span><span class="sxs-lookup"><span data-stu-id="44ffa-448">4443</span></span></p></td>
<td><p><span data-ttu-id="44ffa-449">HTTPS (du proxy inverse)</span><span class="sxs-lookup"><span data-stu-id="44ffa-449">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="44ffa-p107">Vos pools frontaux et pools directeurs qui font appel à l’équilibrage de charge DNS doivent également déployer un programme d’équilibrage de la charge matérielle. Le tableau suivant affiche les ports qui doivent être ouverts sur ces programmes d’équilibrage de la charge matérielle.</span><span class="sxs-lookup"><span data-stu-id="44ffa-p107">Your Front End pools and Director pools that use DNS load balancing also must have a hardware load balancer deployed. The following table shows the ports that need to be open on these hardware load balancers.</span></span>

### <a name="hardware-load-balancer-ports-if-using-dns-load-balancing"></a><span data-ttu-id="44ffa-452">Ports des programmes d’équilibrage de la charge matérielle si l’équilibrage de charge DNS est utilisé</span><span class="sxs-lookup"><span data-stu-id="44ffa-452">Hardware Load Balancer Ports if Using DNS Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="44ffa-453">Programme d’équilibrage de charge</span><span class="sxs-lookup"><span data-stu-id="44ffa-453">Load Balancer</span></span></th>
<th><span data-ttu-id="44ffa-454">Port</span><span class="sxs-lookup"><span data-stu-id="44ffa-454">Port</span></span></th>
<th><span data-ttu-id="44ffa-455">Protocole</span><span class="sxs-lookup"><span data-stu-id="44ffa-455">Protocol</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-456">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-456">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-457">80</span><span class="sxs-lookup"><span data-stu-id="44ffa-457">80</span></span></p></td>
<td><p><span data-ttu-id="44ffa-458">HTTP</span><span class="sxs-lookup"><span data-stu-id="44ffa-458">HTTP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-459">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-459">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-460">443</span><span class="sxs-lookup"><span data-stu-id="44ffa-460">443</span></span></p></td>
<td><p><span data-ttu-id="44ffa-461">HTTPS</span><span class="sxs-lookup"><span data-stu-id="44ffa-461">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-462">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-462">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-463">8080</span><span class="sxs-lookup"><span data-stu-id="44ffa-463">8080</span></span></p></td>
<td><p><span data-ttu-id="44ffa-464">TCP : récupération client/appareil du certificat racine à partir du serveur frontal, notamment clients et appareils authentifiés par NTLM</span><span class="sxs-lookup"><span data-stu-id="44ffa-464">TCP - Client and device retrieval of root certificate from Front End Server – clients and devices authenticated by NTLM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-465">Programme d’équilibrage de charge du serveur frontal</span><span class="sxs-lookup"><span data-stu-id="44ffa-465">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-466">4443</span><span class="sxs-lookup"><span data-stu-id="44ffa-466">4443</span></span></p></td>
<td><p><span data-ttu-id="44ffa-467">HTTPS (du proxy inverse)</span><span class="sxs-lookup"><span data-stu-id="44ffa-467">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-468">Programme d’équilibrage de charge du directeur</span><span class="sxs-lookup"><span data-stu-id="44ffa-468">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-469">443</span><span class="sxs-lookup"><span data-stu-id="44ffa-469">443</span></span></p></td>
<td><p><span data-ttu-id="44ffa-470">HTTPS</span><span class="sxs-lookup"><span data-stu-id="44ffa-470">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td> </td>
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-471">Programme d’équilibrage de charge du directeur</span><span class="sxs-lookup"><span data-stu-id="44ffa-471">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="44ffa-472">4443</span><span class="sxs-lookup"><span data-stu-id="44ffa-472">4443</span></span></p></td>
<td><p><span data-ttu-id="44ffa-473">HTTPS (du proxy inverse)</span><span class="sxs-lookup"><span data-stu-id="44ffa-473">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="required-client-ports"></a><span data-ttu-id="44ffa-474">Ports client requis</span><span class="sxs-lookup"><span data-stu-id="44ffa-474">Required Client Ports</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="44ffa-475">Composant</span><span class="sxs-lookup"><span data-stu-id="44ffa-475">Component</span></span></th>
<th><span data-ttu-id="44ffa-476">Port</span><span class="sxs-lookup"><span data-stu-id="44ffa-476">Port</span></span></th>
<th><span data-ttu-id="44ffa-477">Protocole</span><span class="sxs-lookup"><span data-stu-id="44ffa-477">Protocol</span></span></th>
<th><span data-ttu-id="44ffa-478">Remarques</span><span class="sxs-lookup"><span data-stu-id="44ffa-478">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-479">Clients</span><span class="sxs-lookup"><span data-stu-id="44ffa-479">Clients</span></span></p></td>
<td><p><span data-ttu-id="44ffa-480">67/68</span><span class="sxs-lookup"><span data-stu-id="44ffa-480">67/68</span></span></p></td>
<td><p><span data-ttu-id="44ffa-481">DHCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-481">DHCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-482">Utilisé par Lync Server pour rechercher le nom de domaine complet (FQDN) du Bureau d’enregistrement (autrement dit, en cas d’échec de la configuration du service DNS SRV et de paramètres manuels).</span><span class="sxs-lookup"><span data-stu-id="44ffa-482">Used by Lync Server to find the Registrar FQDN (that is, if DNS SRV fails and manual settings are not configured).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-483">Clients</span><span class="sxs-lookup"><span data-stu-id="44ffa-483">Clients</span></span></p></td>
<td><p><span data-ttu-id="44ffa-484">443</span><span class="sxs-lookup"><span data-stu-id="44ffa-484">443</span></span></p></td>
<td><p><span data-ttu-id="44ffa-485">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-485">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-486">Utilisé pour le trafic SIP client à serveur pour l’accès des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="44ffa-486">Used for client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-487">Clients</span><span class="sxs-lookup"><span data-stu-id="44ffa-487">Clients</span></span></p></td>
<td><p><span data-ttu-id="44ffa-488">443</span><span class="sxs-lookup"><span data-stu-id="44ffa-488">443</span></span></p></td>
<td><p><span data-ttu-id="44ffa-489">TCP (PSOM/TLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-489">TCP (PSOM/TLS)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-490">Utilisé pour que les utilisateurs externes puissent accéder aux sessions de conférence Web.</span><span class="sxs-lookup"><span data-stu-id="44ffa-490">Used for external user access to web conferencing sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-491">Clients</span><span class="sxs-lookup"><span data-stu-id="44ffa-491">Clients</span></span></p></td>
<td><p><span data-ttu-id="44ffa-492">443</span><span class="sxs-lookup"><span data-stu-id="44ffa-492">443</span></span></p></td>
<td><p><span data-ttu-id="44ffa-493">TCP (STUN/MSTURN)</span><span class="sxs-lookup"><span data-stu-id="44ffa-493">TCP (STUN/MSTURN)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-494">Utilisé pour que les utilisateurs externes puissent accéder aux sessions A/V et multimédias (TCP).</span><span class="sxs-lookup"><span data-stu-id="44ffa-494">Used for external user access to A/V sessions and media (TCP)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-495">Clients</span><span class="sxs-lookup"><span data-stu-id="44ffa-495">Clients</span></span></p></td>
<td><p><span data-ttu-id="44ffa-496">3478</span><span class="sxs-lookup"><span data-stu-id="44ffa-496">3478</span></span></p></td>
<td><p><span data-ttu-id="44ffa-497">UDP (STUN/MSTURN)</span><span class="sxs-lookup"><span data-stu-id="44ffa-497">UDP (STUN/MSTURN)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-498">Utilisé pour que les utilisateurs externes puissent accéder aux sessions A/V et multimédias (UDP).</span><span class="sxs-lookup"><span data-stu-id="44ffa-498">Used for external user access to A/V sessions and media (UDP)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-499">Clients</span><span class="sxs-lookup"><span data-stu-id="44ffa-499">Clients</span></span></p></td>
<td><p><span data-ttu-id="44ffa-500">5061</span><span class="sxs-lookup"><span data-stu-id="44ffa-500">5061</span></span></p></td>
<td><p><span data-ttu-id="44ffa-501">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="44ffa-501">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="44ffa-502">Utilisé pour le trafic SIP client à serveur pour l’accès des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="44ffa-502">Used for client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-503">Clients</span><span class="sxs-lookup"><span data-stu-id="44ffa-503">Clients</span></span></p></td>
<td><p><span data-ttu-id="44ffa-504">6891-6901</span><span class="sxs-lookup"><span data-stu-id="44ffa-504">6891-6901</span></span></p></td>
<td><p><span data-ttu-id="44ffa-505">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-505">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-506">Utilisé pour le transfert de fichiers entre clients Lync et clients précédents (clients de Microsoft Office Communications Server 2007 R2, Microsoft Office Communications Server 2007 et Live Communications Server 2005).</span><span class="sxs-lookup"><span data-stu-id="44ffa-506">Used for file transfer between Lync clients and previous clients (clients of Microsoft Office Communications Server 2007 R2, Microsoft Office Communications Server 2007, and Live Communications Server 2005).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-507">Clients</span><span class="sxs-lookup"><span data-stu-id="44ffa-507">Clients</span></span></p></td>
<td><p><span data-ttu-id="44ffa-508">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="44ffa-508">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="44ffa-509">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="44ffa-509">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-510">Plage de ports audio (au moins 20 ports requis).</span><span class="sxs-lookup"><span data-stu-id="44ffa-510">Audio port range (minimum of 20 ports required)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-511">Clients</span><span class="sxs-lookup"><span data-stu-id="44ffa-511">Clients</span></span></p></td>
<td><p><span data-ttu-id="44ffa-512">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="44ffa-512">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="44ffa-513">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="44ffa-513">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-514">Plage de ports vidéo (au moins 20 ports requis).</span><span class="sxs-lookup"><span data-stu-id="44ffa-514">Video port range (minimum of 20 ports required).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-515">Clients</span><span class="sxs-lookup"><span data-stu-id="44ffa-515">Clients</span></span></p></td>
<td><p><span data-ttu-id="44ffa-516">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="44ffa-516">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="44ffa-517">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-517">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-518">Transfert de fichiers d’égal à égal. Pour le transfert de fichiers de conférence, les clients utilisent le modèle PSOM.</span><span class="sxs-lookup"><span data-stu-id="44ffa-518">Peer-to-peer file transfer (for conferencing file transfer, clients use PSOM).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ffa-519">Clients</span><span class="sxs-lookup"><span data-stu-id="44ffa-519">Clients</span></span></p></td>
<td><p><span data-ttu-id="44ffa-520">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="44ffa-520">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="44ffa-521">TCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-521">TCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-522">Partage d’application.</span><span class="sxs-lookup"><span data-stu-id="44ffa-522">Application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ffa-523">Téléphone de partie commune Aastra 6721ip</span><span class="sxs-lookup"><span data-stu-id="44ffa-523">Aastra 6721ip common area phone</span></span></p>
<p><span data-ttu-id="44ffa-524">Téléphone de bureau Aastra 6725ip</span><span class="sxs-lookup"><span data-stu-id="44ffa-524">Aastra 6725ip desk phone</span></span></p>
<p><span data-ttu-id="44ffa-525">Téléphone IP HP 4110 (téléphone de partie commune)</span><span class="sxs-lookup"><span data-stu-id="44ffa-525">HP 4110 IP Phone (common area phone)</span></span></p>
<p><span data-ttu-id="44ffa-526">Téléphone IP HP 4120 (téléphone de bureau)</span><span class="sxs-lookup"><span data-stu-id="44ffa-526">HP 4120 IP Phone (desk phone)</span></span></p>
<p><span data-ttu-id="44ffa-527">Téléphone de partie commune IP Polycom CX500</span><span class="sxs-lookup"><span data-stu-id="44ffa-527">Polycom CX500 IP common area phone</span></span></p>
<p><span data-ttu-id="44ffa-528">Téléphone de bureau IP Polycom CX600</span><span class="sxs-lookup"><span data-stu-id="44ffa-528">Polycom CX600 IP desk phone</span></span></p>
<p><span data-ttu-id="44ffa-529">Téléphone de bureau IP CX700</span><span class="sxs-lookup"><span data-stu-id="44ffa-529">Polycom CX700 IP desk phone</span></span></p>
<p><span data-ttu-id="44ffa-530">Téléphone de conférence IP Polycom CX3000</span><span class="sxs-lookup"><span data-stu-id="44ffa-530">Polycom CX3000 IP conference phone</span></span></p></td>
<td><p><span data-ttu-id="44ffa-531">67/68</span><span class="sxs-lookup"><span data-stu-id="44ffa-531">67/68</span></span></p></td>
<td><p><span data-ttu-id="44ffa-532">DHCP</span><span class="sxs-lookup"><span data-stu-id="44ffa-532">DHCP</span></span></p></td>
<td><p><span data-ttu-id="44ffa-533">Utilisé par les périphériques répertoriés pour trouver le certificat de serveur Lync, le nom de domaine complet de mise en service et le nom de domaine complet du Bureau d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="44ffa-533">Used by the listed devices to find the Lync Server certificate, provisioning FQDN, and Registrar FQDN.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="44ffa-534">**\*** Pour configurer des ports spécifiques pour ces types de médias, utilisez l’applet de applet de CsConferencingConfiguration (ClientMediaPortRangeEnabled, ClientMediaPort et les paramètres ClientMediaPortRange).</span><span class="sxs-lookup"><span data-stu-id="44ffa-534">**\*** To configure specific ports for these media types, use the CsConferencingConfiguration cmdlet (ClientMediaPortRangeEnabled, ClientMediaPort, and ClientMediaPortRange parameters).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="44ffa-535">Les programmes Set pour les clients Lync créent automatiquement les exceptions de pare-feu du système d’exploitation requises sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="44ffa-535">The set programs for Lync clients automatically create the required operating-system firewall exceptions on the client computer.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="44ffa-536">Les ports utilisés pour l’accès des utilisateurs externes sont nécessaires dans tout scénario où le client doit franchir le pare-feu de l’organisation (par exemple, les communications externes ou les réunions hébergées par d’autres organisations).</span><span class="sxs-lookup"><span data-stu-id="44ffa-536">The ports that are used for external user access are required for any scenario in which the client must traverse the organization’s firewall (for example, any external communications or meetings hosted by other organizations).</span></span>



<span data-ttu-id="44ffa-537"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="44ffa-537"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

