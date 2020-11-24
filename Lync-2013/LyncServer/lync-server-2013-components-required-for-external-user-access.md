---
title: 'Lync Server 2013 : Composants requis pour l’accès des utilisateurs externes'
description: 'Lync Server 2013 : composants requis pour l’accès des utilisateurs externes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components required for external user access
ms:assetid: 2d0f9817-14e7-4109-95dc-62420e3c29e2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425779(v=OCS.15)
ms:contentKeyID: 48183711
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d75ef0c7f2000353a35acefa0b177c90bdcc879b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394213"
---
# <a name="components-required-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="b2679-103">Composants requis pour l’accès des utilisateurs externes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b2679-103">Components required for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b2679-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b2679-104">

<span> </span></span></span>

<span data-ttu-id="b2679-105">_**Dernière modification de la rubrique :** 2014-05-29_</span><span class="sxs-lookup"><span data-stu-id="b2679-105">_**Topic Last Modified:** 2014-05-29_</span></span>

<span data-ttu-id="b2679-106">La plupart des composants Edge sont déployés sur un réseau de périmètre.</span><span class="sxs-lookup"><span data-stu-id="b2679-106">Most Edge components are deployed in a perimeter network.</span></span> <span data-ttu-id="b2679-107">Les composants suivants constituent la topologie latérale du réseau de périmètre.</span><span class="sxs-lookup"><span data-stu-id="b2679-107">The following components make up the edge topology of the perimeter network.</span></span> <span data-ttu-id="b2679-108">Sauf indication contraire, les composants font partie des [scénarios d’accès des utilisateurs externes dans Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) et se trouvent dans le réseau de périmètre.</span><span class="sxs-lookup"><span data-stu-id="b2679-108">Except where noted, the components are part of the [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) and are in the perimeter network.</span></span> <span data-ttu-id="b2679-109">Ces composants Edge sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="b2679-109">Edge components include the following:</span></span>

  - <span data-ttu-id="b2679-110">Edge Servers</span><span class="sxs-lookup"><span data-stu-id="b2679-110">Edge Servers</span></span>

  - <span data-ttu-id="b2679-111">Reverse proxies</span><span class="sxs-lookup"><span data-stu-id="b2679-111">Reverse proxies</span></span>

  - <span data-ttu-id="b2679-112">Firewalls</span><span class="sxs-lookup"><span data-stu-id="b2679-112">Firewalls</span></span>

  - <span data-ttu-id="b2679-113">Directeurs (facultatif et logiquement situé sur le réseau interne)</span><span class="sxs-lookup"><span data-stu-id="b2679-113">Directors (optional, and logically located on the internal network)</span></span>

  - <span data-ttu-id="b2679-114">Équilibrage de la charge pour les topologies Edge mises à l’échelle (avec charge DNS équilibrée ou un équilibreur de la charge matérielle)</span><span class="sxs-lookup"><span data-stu-id="b2679-114">Load balancing for Scaled Edge Topologies (either DNS load balancing or a hardware load balancer)</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b2679-p102">L’utilisation de l’équilibrage de charge DNS sur une interface et de l’équilibrage de charge matérielle sur l’autre n’est pas prise en charge. Sur les deux interfaces, vous devez utiliser l’équilibrage de charge matérielle ou l’équilibrage de charge DNS.</span><span class="sxs-lookup"><span data-stu-id="b2679-p102">Using DNS load balancing on one interface and hardware load balancing on the other is not supported. You must use hardware load balancing for both interfaces or DNS load balancing for both.</span></span>

    
    </div>

<div>

## <a name="edge-servers"></a><span data-ttu-id="b2679-117">serveurs Edge</span><span class="sxs-lookup"><span data-stu-id="b2679-117">Edge Servers</span></span>

<span data-ttu-id="b2679-118">Les serveurs Edge envoient et reçoivent le trafic réseau pour les services proposés par un déploiement interne par des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="b2679-118">The Edge Servers send and receive network traffic for the services offered by internal deployment by external users.</span></span> <span data-ttu-id="b2679-119">Le serveur Edge exécute les services suivants :</span><span class="sxs-lookup"><span data-stu-id="b2679-119">The Edge Server runs the following services:</span></span>

  - <span data-ttu-id="b2679-120">**Service Edge d’accès**   Le service Edge d’accès fournit un point de connexion unique et approuvé pour le trafic SIP (Session Initiation Protocol) entrant et sortant.</span><span class="sxs-lookup"><span data-stu-id="b2679-120">**Access Edge service**   The Access Edge service provides a single, trusted connection point for both outbound and inbound Session Initiation Protocol (SIP) traffic.</span></span>

  - <span data-ttu-id="b2679-121">**Service Edge de conférence Web**   Ce service permet aux utilisateurs externes de rejoindre des réunions hébergées sur votre déploiement interne Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b2679-121">**Web Conferencing Edge service**   The Web Conferencing Edge service enables external users to join meetings that are hosted on your internal Lync Server 2013 deployment.</span></span>

  - <span data-ttu-id="b2679-122">**Service Edge A/V**   Le service Edge A/V effectue des opérations audio, vidéo, de partage d’application et de transfert de fichiers aux utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="b2679-122">**A/V Edge service**   The A/V Edge service makes audio, video, application sharing, and file transfer available to external users.</span></span> <span data-ttu-id="b2679-123">Vos utilisateurs peuvent ajouter de l’audio et de la vidéo à des réunions qui incluent des participants externes, et ils peuvent communiquer en utilisant directement l’audio et/ou la vidéo avec un utilisateur externe dans les sessions de point à point.</span><span class="sxs-lookup"><span data-stu-id="b2679-123">Your users can add audio and video to meetings that include external participants, and they can communicate using audio and/or video directly with an external user in point-to-point sessions.</span></span> <span data-ttu-id="b2679-124">Le service Edge A/V fournit également une prise en charge du partage de bureau et du transfert de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b2679-124">The A/V Edge service also provides support for desktop sharing and file transfer.</span></span>

  - <span data-ttu-id="b2679-125">**Service proxy XMPP**   Le service proxy XMPP accepte et envoie les messages de la messagerie électronique extensible (XMPP) vers et depuis les partenaires fédérés de XMPP configurés.</span><span class="sxs-lookup"><span data-stu-id="b2679-125">**XMPP Proxy service**   The XMPP Proxy service accepts and sends extensible messaging and presence protocol (XMPP) messages to and from configured XMPP Federated partners.</span></span>

<span data-ttu-id="b2679-126">Les utilisateurs externes autorisés peuvent accéder aux serveurs de périphérie afin de se connecter à votre déploiement interne de Lync Server 2013, mais les serveurs de périphérie ne fournissent aucun moyen pour tout autre accès au réseau interne.</span><span class="sxs-lookup"><span data-stu-id="b2679-126">Authorized external users can access the Edge Servers in order to connect to your internal Lync Server 2013 deployment, but the Edge Servers do not provide a means for any other access to the internal network.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b2679-127">Les serveurs Edge sont déployés de manière à fournir des connexions pour les clients Lync et les autres serveurs Microsoft Edge compatibles (comme dans les scénarios de Fédération).</span><span class="sxs-lookup"><span data-stu-id="b2679-127">Edge servers are deployed to provide connections for enabled Lync clients and other Microsoft Edge servers (as in federation scenarios).</span></span> <span data-ttu-id="b2679-128">Elles ne sont pas conçues pour autoriser les connexions à partir d’un autre client ou type de serveur principal.</span><span class="sxs-lookup"><span data-stu-id="b2679-128">They are not designed to allow connections from other end point client or server types.</span></span> <span data-ttu-id="b2679-129">Le serveur de passerelle XMPP peut être déployé pour autoriser les connexions avec les partenaires XMPP configurés.</span><span class="sxs-lookup"><span data-stu-id="b2679-129">The XMPP Gateway server can be deployed to allow connections with configured XMPP partners.</span></span> <span data-ttu-id="b2679-130">Le serveur de périphérie et la passerelle XMPP peuvent uniquement prendre en charge les connexions de point de terminaison de ces types de client et de Fédération.</span><span class="sxs-lookup"><span data-stu-id="b2679-130">The Edge server and XMPP Gateway can only support end point connections from these client and federation types.</span></span>



</div>

</div>

<div>

## <a name="reverse-proxy"></a><span data-ttu-id="b2679-131">Proxy inverse</span><span class="sxs-lookup"><span data-stu-id="b2679-131">Reverse Proxy</span></span>

<span data-ttu-id="b2679-132">Le proxy inverse est requis pour les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b2679-132">The reverse proxy is required for the following:</span></span>

  - <span data-ttu-id="b2679-133">Pour permettre aux utilisateurs de se connecter à des réunions ou des conférences rendez-vous à l’aide d’URL simples</span><span class="sxs-lookup"><span data-stu-id="b2679-133">To allow users to connect to meetings or dial-in conferences using simple URLs</span></span>

  - <span data-ttu-id="b2679-134">Pour permettre aux utilisateurs externes de télécharger le contenu d’une réunion</span><span class="sxs-lookup"><span data-stu-id="b2679-134">To enable external users to download meeting content</span></span>

  - <span data-ttu-id="b2679-135">Pour permettre aux utilisateurs externes d’étendre les groupes de distribution</span><span class="sxs-lookup"><span data-stu-id="b2679-135">To enable external users to expand distribution groups</span></span>

  - <span data-ttu-id="b2679-136">Pour permettre à l’utilisateur d’obtenir un certificat basé sur l’utilisateur pour l’authentification par certificat client</span><span class="sxs-lookup"><span data-stu-id="b2679-136">To allow the user to obtain a user-based certificate for client certificate based authentication</span></span>

  - <span data-ttu-id="b2679-137">Pour permettre aux utilisateurs distants de télécharger des fichiers à partir du serveur du carnet d’adresses ou d’adresser des requêtes au service de requête sur le carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="b2679-137">To enable remote users to download files from the Address Book Server or to submit queries to the Address Book Web Query service</span></span>

  - <span data-ttu-id="b2679-138">Pour permettre aux utilisateurs distants d’obtenir les mises à jour du logiciel client et de l’appareil</span><span class="sxs-lookup"><span data-stu-id="b2679-138">To enable remote users to obtain updates to client and device software</span></span>

  - <span data-ttu-id="b2679-139">Pour permettre aux appareils mobiles de détecter automatiquement les serveurs frontaux proposant des services de mobilité</span><span class="sxs-lookup"><span data-stu-id="b2679-139">To enable mobile devices to automatically discover Front End Servers offering mobility services</span></span>

  - <span data-ttu-id="b2679-140">Pour activer les notifications de transmission vers des appareils mobiles à partir des services Microsoft 365, Office 365 ou Apple notification</span><span class="sxs-lookup"><span data-stu-id="b2679-140">To enable push notifications to mobile devices from the Microsoft 365, Office 365, or Apple push notification services</span></span>

<span data-ttu-id="b2679-141">Pour plus d’informations sur les proxys inversés et les configurations requises pour les proxys inverse, voir les détails de la [Configuration requise pour le proxy inverse dans Lync Server 2013](lync-server-2013-configuration-requirements-for-reverse-proxy.md).</span><span class="sxs-lookup"><span data-stu-id="b2679-141">For additional information related to reverse proxies and the requirements that reverse proxies must meet, see the details in [Configuration requirements for reverse proxy in Lync Server 2013](lync-server-2013-configuration-requirements-for-reverse-proxy.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b2679-142">Les utilisateurs externes n’ont pas besoin d’une connexion de réseau privé virtuel (VPN) pour votre organisation afin de participer aux communications à l’aide de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b2679-142">External users do not need a virtual private network (VPN) connection to your organization in order to participate in communications using Lync Server 2013.</span></span> <span data-ttu-id="b2679-143">Si vous avez implémenté la technologie VPN au sein de votre organisation et que vos utilisateurs utilisent le VPN pour Lync, le trafic multimédia (par exemple, les conférences vidéo) peut être affecté.</span><span class="sxs-lookup"><span data-stu-id="b2679-143">If you have implemented VPN technology in your organization and your users use the VPN for Lync, media traffic (such as video conferencing) can be adversely affected.</span></span> <span data-ttu-id="b2679-144">Nous vous conseillons de fournir un moyen pour le trafic multimédia de se connecter directement au service Edge AV et de contourner le VPN.</span><span class="sxs-lookup"><span data-stu-id="b2679-144">You should consider providing a means for media traffic to connect to the AV Edge service directly and bypass the VPN.</span></span> <span data-ttu-id="b2679-145">Pour plus d’informations, reportez-vous à l’article de blog NextHop intitulé « activation de médias Lync pour ignorer un tunnel VPN » <A href="https://go.microsoft.com/fwlink/p/?linkid=256532">https://go.microsoft.com/fwlink/p/?LinkId=256532</A> .</span><span class="sxs-lookup"><span data-stu-id="b2679-145">For details, see the NextHop Blog article, “Enabling Lync Media to Bypass a VPN Tunnel,” at <A href="https://go.microsoft.com/fwlink/p/?linkid=256532">https://go.microsoft.com/fwlink/p/?LinkId=256532</A>.</span></span>



</div>

</div>

<div>

## <a name="firewall"></a><span data-ttu-id="b2679-146">Pare-feu</span><span class="sxs-lookup"><span data-stu-id="b2679-146">Firewall</span></span>

<span data-ttu-id="b2679-147">Vous pouvez déployer votre topologie de périphérie avec un pare-feu externe uniquement ou les pare-feu internes et externes.</span><span class="sxs-lookup"><span data-stu-id="b2679-147">You can deploy your edge topology with only an external firewall or both external and internal firewalls.</span></span> <span data-ttu-id="b2679-148">Les architectures de scénario incluent deux pare-feu.</span><span class="sxs-lookup"><span data-stu-id="b2679-148">The scenario architectures include two firewalls.</span></span> <span data-ttu-id="b2679-149">L’utilisation de deux pare-feu est l’approche recommandée, car elle assure le routage strict d’un bord réseau vers l’autre et protège votre déploiement interne derrière deux niveaux de pare-feu.</span><span class="sxs-lookup"><span data-stu-id="b2679-149">Using two firewalls is the recommended approach because it ensures strict routing from one network edge to the other, and it protects your internal deployment behind two levels of firewall.</span></span>

</div>

<div>

## <a name="director"></a><span data-ttu-id="b2679-150">directeur</span><span class="sxs-lookup"><span data-stu-id="b2679-150">Director</span></span>

<span data-ttu-id="b2679-151">Un directeur est un rôle de serveur distinct et facultatif dans Lync Server 2013 qui ne prend pas en charge les comptes d’utilisateurs personnels ou qui fournissent des services de présence et de conférence.</span><span class="sxs-lookup"><span data-stu-id="b2679-151">A Director is a separate, optional server role in Lync Server 2013 that does not home user accounts, or provide presence or conferencing services.</span></span> <span data-ttu-id="b2679-152">Il sert de serveur interne de tronçons de tronçon sur lequel un serveur de périphérie route le trafic SIP entrant destiné aux serveurs internes.</span><span class="sxs-lookup"><span data-stu-id="b2679-152">It serves as an internal next hop server to which an Edge Server routes inbound SIP traffic destined for internal servers.</span></span> <span data-ttu-id="b2679-153">Le directeur authentifie les demandes entrantes et les redirige vers le serveur ou le groupe d’accueil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b2679-153">The Director preauthenticates inbound requests and redirects them to the user’s home pool or server.</span></span> <span data-ttu-id="b2679-154">En effectuant une authentification au niveau du réalisateur, vous pouvez déplacer des requêtes de comptes d’utilisateur qui sont inconnus du déploiement.</span><span class="sxs-lookup"><span data-stu-id="b2679-154">By preauthenticating at the Director, you can drop requests from user accounts that are unknown to the deployment.</span></span>

<span data-ttu-id="b2679-155">Un directeur permet d’isoler les serveurs Standard Edition et les serveurs frontaux dans les listes frontales d’Enterprise Edition d’un trafic malveillant (par exemple, les attaques par déni de service (DoS)).</span><span class="sxs-lookup"><span data-stu-id="b2679-155">A Director helps insulate Standard Edition servers and Front End Servers in Enterprise Edition Front End pools from malicious traffic such as denial-of-service (DoS) attacks.</span></span> <span data-ttu-id="b2679-156">Si le réseau est inondé de trafic externe non valide lors d’une telle attaque, le trafic se termine au directeur.</span><span class="sxs-lookup"><span data-stu-id="b2679-156">If the network is flooded with invalid external traffic in such an attack, the traffic ends at the Director.</span></span> <span data-ttu-id="b2679-157">Pour plus d’informations sur l’utilisation des directeurs, voir [scénarios pour le directeur dans Lync Server 2013](lync-server-2013-scenarios-for-the-director.md).</span><span class="sxs-lookup"><span data-stu-id="b2679-157">For details about the use of Directors, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b2679-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2679-158">See Also</span></span>


[<span data-ttu-id="b2679-159">Configuration requise pour l’équilibreur de charge matérielle pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b2679-159">Hardware load balancer requirements for Lync Server 2013</span></span>](lync-server-2013-hardware-load-balancer-requirements.md)  
  

<span data-ttu-id="b2679-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b2679-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

