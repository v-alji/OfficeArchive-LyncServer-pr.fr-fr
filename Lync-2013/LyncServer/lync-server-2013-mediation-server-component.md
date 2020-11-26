---
title: 'Lync Server 2013 : composant du serveur de médiation'
description: 'Lync Server 2013 : serveur de médiation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mediation Server component
ms:assetid: 5b19edef-4a54-43c9-aa12-5643b8108355
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398399(v=OCS.15)
ms:contentKeyID: 48184239
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 08c11bff3ee7077d991204cda5a9885787c50ec2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445970"
---
# <a name="mediation-server-component-in-lync-server-2013"></a><span data-ttu-id="a22e6-103">Composant serveur de médiation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a22e6-103">Mediation Server component in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a22e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a22e6-104">

<span> </span></span></span>

<span data-ttu-id="a22e6-105">_**Dernière modification de la rubrique :** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="a22e6-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="a22e6-106">Si vous déployez la charge de travail voix entreprise, vous devez déployer Lync Server 2013, serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="a22e6-106">You must deploy Lync Server 2013, Mediation Server if you deploy the Enterprise Voice workload.</span></span> <span data-ttu-id="a22e6-107">Cette section décrit les fonctionnalités de base, les dépendances, les topologies de base et les recommandations en matière de planification.</span><span class="sxs-lookup"><span data-stu-id="a22e6-107">This section describes basic functionality, dependencies, basic topologies, and planning guidelines.</span></span>

<span data-ttu-id="a22e6-108">Le serveur de médiation translate les signaux et, dans certaines configurations, les éléments multimédias entre votre serveur interne Lync Server 2013, l’infrastructure voix entreprise et une passerelle de réseau téléphonique commuté (PSTN) ou un Trunk SIP (Session Initiation Protocol).</span><span class="sxs-lookup"><span data-stu-id="a22e6-108">The Mediation Server translates signaling and, in some configurations, media between your internal Lync Server 2013, Enterprise Voice infrastructure and a public switched telephone network (PSTN) gateway or a Session Initiation Protocol (SIP) trunk.</span></span> <span data-ttu-id="a22e6-109">Sur le site Lync Server 2013, le serveur de médiation écoute une seule adresse de transport Mutual TLS (MTLS).</span><span class="sxs-lookup"><span data-stu-id="a22e6-109">On the Lync Server 2013 side, Mediation Server listens on a single mutual TLS (MTLS) transport address.</span></span> <span data-ttu-id="a22e6-110">Sur le côté passerelle, le serveur de médiation écoute tous les ports d’écoute associés associés à des lignes définies dans le document topologique.</span><span class="sxs-lookup"><span data-stu-id="a22e6-110">On the gateway side, Mediation Server listens on all associated listening ports associated with trunks defined in the Topology document.</span></span> <span data-ttu-id="a22e6-111">Toutes les passerelles qualifiées doivent prendre en charge le protocole TLS mais peuvent aussi activer le protocole TCP.</span><span class="sxs-lookup"><span data-stu-id="a22e6-111">All qualified gateways must support TLS, but can enable TCP as well.</span></span> <span data-ttu-id="a22e6-112">Le protocole TCP est pris en charge pour les passerelles qui ne prennent pas en charge le protocole TLS.</span><span class="sxs-lookup"><span data-stu-id="a22e6-112">TCP is supported for gateways that do not support TLS.</span></span>

<span data-ttu-id="a22e6-113">Si vous avez également un échange de succursale publique (PBX) existant dans votre environnement, le serveur de médiation gère les appels entre les utilisateurs voix entreprise et le PBX.</span><span class="sxs-lookup"><span data-stu-id="a22e6-113">If you also have an existing Public Branch Exchange (PBX) in your environment, Mediation Server handles calls between Enterprise Voice users and the PBX.</span></span> <span data-ttu-id="a22e6-114">S’il s’agit d’un PBX IP, vous pouvez créer une connexion SIP directe entre le PBX et le serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="a22e6-114">If your PBX is an IP-PBX, you can create a direct SIP connection between the PBX and Mediation Server.</span></span> <span data-ttu-id="a22e6-115">S’il s’agit d’un système PBX (TDM) PBX, vous devez également déployer une passerelle RTC entre le serveur de médiation et le PBX.</span><span class="sxs-lookup"><span data-stu-id="a22e6-115">If your PBX is a Time Division Multiplex (TDM) PBX, you must also deploy a PSTN gateway between Mediation Server and the PBX.</span></span>

<span data-ttu-id="a22e6-116">Le serveur de médiation est colocalisé par défaut avec le serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="a22e6-116">The Mediation Server is collocated with the Front End Server by default.</span></span> <span data-ttu-id="a22e6-117">Le serveur de médiation peut également être déployé dans un pool autonome pour des raisons de performances, ou si vous déployez le trunking SIP, auquel cas le pool autonome est fortement recommandé.</span><span class="sxs-lookup"><span data-stu-id="a22e6-117">The Mediation Server can also be deployed in a stand-alone pool for performance reasons, or if you deploy SIP trunking, in which case the stand-alone pool is strongly recommended.</span></span>

<span data-ttu-id="a22e6-118">Si vous déployez des connexions SIP directes vers une passerelle RTC qualifiée qui prend en charge le contournement du contenu multimédia et l’équilibrage de charge DNS, vous n’avez pas besoin d’un pool de serveurs de médiation autonome.</span><span class="sxs-lookup"><span data-stu-id="a22e6-118">If you deploy Direct SIP connections to a qualified PSTN gateway that supports media bypass and DNS load balancing, a stand-alone Mediation Server pool is not necessary.</span></span> <span data-ttu-id="a22e6-119">Il n’est pas nécessaire de disposer d’un pool de serveurs de médiation autonomes, car les passerelles qualifiées sont en mesure d’équilibrer la charge DNS vers un pool de serveurs de médiation et ils peuvent recevoir le trafic de n’importe quel serveur de médiation dans un pool.</span><span class="sxs-lookup"><span data-stu-id="a22e6-119">A stand-alone Mediation Server pool is not necessary because qualified gateways are capable of DNS load balancing to a pool of Mediation Servers and they can receive traffic from any Mediation Server in a pool.</span></span>

<span data-ttu-id="a22e6-120">Nous vous recommandons également de collocate le serveur de médiation sur un pool frontal lorsque vous avez déployé IP-PBXs ou que vous vous connectez à un contrôleur de bordure de session du fournisseur de services de téléphonie Internet (SBC), à condition que l’une des conditions suivantes soit remplie :</span><span class="sxs-lookup"><span data-stu-id="a22e6-120">We also recommend that you collocate the Mediation Server on a Front End pool when you have deployed IP-PBXs or connect to an Internet Telephony Server Provider’s Session Border Controller (SBC), as long as any of the following conditions are met:</span></span>

  - <span data-ttu-id="a22e6-121">Le PBX IP ou le SBC est configuré pour recevoir le trafic de n’importe quel serveur de médiation dans le pool et peut acheminer le trafic uniformément vers tous les serveurs de médiation du pool.</span><span class="sxs-lookup"><span data-stu-id="a22e6-121">The IP-PBX or SBC is configured to receive traffic from any Mediation Server in the pool and can route traffic uniformly to all Mediation Servers in the pool.</span></span>

  - <span data-ttu-id="a22e6-122">Le PBX IP ne prend pas en charge la dérivation multimédia, mais le pool frontal qui héberge le serveur de médiation peut gérer le transcodage de la voix pour les appels pour lesquels aucune dérivation de média ne s’applique.</span><span class="sxs-lookup"><span data-stu-id="a22e6-122">The IP-PBX does not support media bypass, but the Front End pool that is hosting the Mediation Server can handle voice transcoding for calls to which media bypass does not apply.</span></span>

<span data-ttu-id="a22e6-123">Vous pouvez utiliser l’outil de planification de Microsoft Lync Server 2013 pour déterminer si le pool frontal sur lequel vous souhaitez collocate le serveur de médiation peut gérer le chargement.</span><span class="sxs-lookup"><span data-stu-id="a22e6-123">You can use the Microsoft Lync Server 2013, Planning Tool to evaluate whether the Front End pool where you want to collocate the Mediation Server can handle the load.</span></span> <span data-ttu-id="a22e6-124">Si votre environnement ne peut pas répondre à ces exigences, vous devez déployer un pool de serveurs de médiation autonome.</span><span class="sxs-lookup"><span data-stu-id="a22e6-124">If your environment cannot meet these requirements, then you must deploy a stand-alone Mediation Server pool.</span></span>

<span data-ttu-id="a22e6-125">Les principales fonctions du serveur de médiation sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a22e6-125">The main functions of the Mediation Server are as follows:</span></span>

  - <span data-ttu-id="a22e6-126">Le chiffrement et le déchiffrement de SRTP du côté serveur Lync</span><span class="sxs-lookup"><span data-stu-id="a22e6-126">Encrypting and decrypting SRTP on the Lync Server side</span></span>

  - <span data-ttu-id="a22e6-127">Traduction SIP sur TCP (pour les passerelles qui ne prennent pas en charge TLS) pour SIP sur Mutual TLS</span><span class="sxs-lookup"><span data-stu-id="a22e6-127">Translating SIP over TCP (for gateways that do not support TLS) to SIP over mutual TLS</span></span>

  - <span data-ttu-id="a22e6-128">Traduction de flux multimédias entre Lync Server et l’homologue de passerelle du serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="a22e6-128">Translating media streams between Lync Server and the gateway peer of the Mediation Server</span></span>

  - <span data-ttu-id="a22e6-129">Connexion de clients se trouvant hors du réseau à des composants de glace internes, qui permettent le passage de contenus multimédias de tar et de pare-feu</span><span class="sxs-lookup"><span data-stu-id="a22e6-129">Connecting clients that are outside the network to internal ICE components, which enable media traversal of NAT and firewalls</span></span>

  - <span data-ttu-id="a22e6-130">Agissant en tant qu’intermédiaire pour les flux d’appels qui n’est pas pris en charge par une passerelle, comme les appels de travailleurs à distance sur un client voix entreprise</span><span class="sxs-lookup"><span data-stu-id="a22e6-130">Acting as an intermediary for call flows that a gateway does not support, such as calls from remote workers on an Enterprise Voice client</span></span>

  - <span data-ttu-id="a22e6-131">Dans les déploiements qui incluent le trunking SIP, en travaillant avec le fournisseur de service de trunking SIP pour fournir la prise en charge RTC, qui rend inutile le besoin d’une passerelle RTC</span><span class="sxs-lookup"><span data-stu-id="a22e6-131">In deployments that include SIP trunking, working with the SIP trunking service provider to provide PSTN support, which eliminates the need for a PSTN gateway</span></span>

<span data-ttu-id="a22e6-132">La figure suivante illustre les protocoles de signalisation et de média utilisés par le serveur de médiation pour communiquer avec une passerelle RTC de base et l’infrastructure voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="a22e6-132">The following figure shows the signaling and media protocols that are used by the Mediation Server when communicating with a basic PSTN gateway and the Enterprise Voice infrastructure.</span></span>

<span data-ttu-id="a22e6-133">**Protocoles de signalisation et de données multimédias utilisés par le serveur de médiation**</span><span class="sxs-lookup"><span data-stu-id="a22e6-133">**Signaling and media protocols used by the Mediation Server**</span></span>

<span data-ttu-id="a22e6-134">![Diagramme de protocoles de serveur de médiation](images/Gg398399.c3d39ba0-e323-4a58-8f07-4e80d3278af2(OCS.15).jpg "Diagramme de protocoles de serveur de médiation")</span><span class="sxs-lookup"><span data-stu-id="a22e6-134">![Mediation Server Protocols diagram](images/Gg398399.c3d39ba0-e323-4a58-8f07-4e80d3278af2(OCS.15).jpg "Mediation Server Protocols diagram")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a22e6-135">Si vous utilisez TCP ou RTP/RTCP (au lieu de SRTP ou SRTCP) sur le réseau entre la passerelle RTC et le serveur de médiation, nous vous conseillons de prendre des mesures pour garantir la sécurité et la confidentialité du réseau.</span><span class="sxs-lookup"><span data-stu-id="a22e6-135">If you are using TCP or RTP/RTCP (instead of SRTP or SRTCP) on the network between the PSTN gateway and the Mediation Server, we recommend that you take measures to help ensure the security and privacy of the network.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a22e6-136">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a22e6-136">In This Section</span></span>

  - [<span data-ttu-id="a22e6-137">M :N Trunk dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a22e6-137">M:N trunk in Lync Server 2013</span></span>](lync-server-2013-m-n-trunk.md)

  - [<span data-ttu-id="a22e6-138">Contrôle d’admission des appels et serveur de médiation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a22e6-138">Call admission control and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-call-admission-control-and-mediation-server.md)

  - [<span data-ttu-id="a22e6-139">Enhanced 9-1-1 (E9-1-1) et serveur de médiation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a22e6-139">Enhanced 9-1-1 (E9-1-1) and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-enhanced-9-1-1-e9-1-1-and-mediation-server.md)

  - [<span data-ttu-id="a22e6-140">Déviation du trafic multimédia et serveur de médiation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a22e6-140">Media bypass and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-media-bypass-and-mediation-server.md)

  - [<span data-ttu-id="a22e6-141">Composants et topologies utilisés pour le serveur de médiation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a22e6-141">Components and topologies for Mediation Server in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-mediation-server.md)

  - [<span data-ttu-id="a22e6-142">Recommandations en matière de déploiement pour le serveur de médiation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a22e6-142">Deployment guidelines for Mediation Server in Lync Server 2013</span></span>](lync-server-2013-deployment-guidelines-for-mediation-server.md)

<span data-ttu-id="a22e6-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a22e6-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

