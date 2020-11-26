---
title: Configurations requises pour l’infrastructure réseau de Lync Server 2013
description: Configurations requises pour l’infrastructure réseau de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Network infrastructure requirements
ms:assetid: 35c7bb3f-8e0f-48b7-8a2c-857d4b42a4c4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425841(v=OCS.15)
ms:contentKeyID: 48183804
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6f7ff21c2f936ef8e048f6831d55408994055400
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425191"
---
# <a name="network-infrastructure-requirements-for-lync-server-2013"></a><span data-ttu-id="f96ec-103">Configuration requise pour l’infrastructure réseau pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f96ec-103">Network infrastructure requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f96ec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f96ec-104">

<span> </span></span></span>

<span data-ttu-id="f96ec-105">_**Dernière modification de la rubrique :** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="f96ec-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="f96ec-106">La carte réseau de chaque serveur dans la topologie Lync Server 2013 doit prendre en charge au moins 1 Gbit/s (Gbps).</span><span class="sxs-lookup"><span data-stu-id="f96ec-106">The network adapter card of each server in the Lync Server 2013 topology must support at least 1 gigabit per second (Gbps).</span></span> <span data-ttu-id="f96ec-107">En règle générale, vous devez connecter tous les rôles de serveur dans la topologie du serveur Lync à l’aide d’un réseau local (LAN) à faible latence et de haut débit.</span><span class="sxs-lookup"><span data-stu-id="f96ec-107">In general, you should connect all server roles within the Lync Server topology using a low latency and high bandwidth local area network (LAN).</span></span> <span data-ttu-id="f96ec-108">La taille du réseau local dépend de la taille de la topologie :</span><span class="sxs-lookup"><span data-stu-id="f96ec-108">The size of the LAN is dependent on the size of the topology:</span></span>

  - <span data-ttu-id="f96ec-109">Dans les topologies Standard Edition, les serveurs doivent se trouver dans un réseau qui prend en charge Ethernet 1 Gbit ou équivalent.</span><span class="sxs-lookup"><span data-stu-id="f96ec-109">In Standard Edition topologies, servers should be in a network that supports 1 Gbps Ethernet or equivalent.</span></span>

  - <span data-ttu-id="f96ec-110">Dans les topologies de pool frontal, la plupart des serveurs doivent se trouver dans un réseau qui prend en charge plus de 1 Gbit/s, en particulier lors de la prise en charge du partage d’applications et de conférences audio/vidéo (A/V).</span><span class="sxs-lookup"><span data-stu-id="f96ec-110">In Front End pool topologies, most servers should be in a network that supports more than 1 Gbps, especially when supporting audio/video (A/V) conferencing and application sharing.</span></span>

<span data-ttu-id="f96ec-111">Dans le cas de l'intégration au réseau téléphonique commuté (RTC ou, en anglais, PSTN pour Public Switched Telephone Network), vous pouvez utiliser les lignes T1/E1 ou les jonctions SIP.</span><span class="sxs-lookup"><span data-stu-id="f96ec-111">For public switched telephone network (PSTN) integration, you can integrate by using either T1/E1 lines or SIP trunking.</span></span>

<div>

## <a name="audiovideo-network-requirements"></a><span data-ttu-id="f96ec-112">Configuration requise du réseau audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="f96ec-112">Audio/Video Network Requirements</span></span>

<span data-ttu-id="f96ec-113">La configuration réseau requise pour les appels audio/vidéo (A/V) dans un déploiement Lync Server inclut les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="f96ec-113">Network requirements for audio/video (A/V) in a Lync Server deployment include the following:</span></span>

  - <span data-ttu-id="f96ec-114">Si vous déployez un serveur Edge unique ou un pool Edge à l’aide de l’équilibrage de charge DNS, vous pouvez configurer le pare-feu externe en tant que NAT.</span><span class="sxs-lookup"><span data-stu-id="f96ec-114">If you are deploying a single Edge Server or an Edge pool using DNS load balancing, you can configure the external firewall as a NAT.</span></span> <span data-ttu-id="f96ec-115">Vous ne pouvez pas configurer le pare-feu interne en tant que NAT.</span><span class="sxs-lookup"><span data-stu-id="f96ec-115">You cannot configure the internal firewall as a NAT.</span></span> <span data-ttu-id="f96ec-116">Pour plus d’informations sur ces exigences, voir [déterminer la configuration requise pour le pare-feu A/V et la configuration de port pour Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="f96ec-116">For details about these requirements, see [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md) in the Planning documentation.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="f96ec-117">Si vous disposez d’un pool Edge et que vous utilisez un dispositif d’équilibrage de la charge matérielle, vous devez utiliser des adresses IP publiques sur chacun des serveurs Edge et vous ne pouvez pas utiliser la traduction d’adresses réseau pour les serveurs ou le pool sur votre appareil NAT (par exemple, le pare-feu ou un autre appareil d’infrastructure qui interagit avec le trafic entrant ou sortant).</span><span class="sxs-lookup"><span data-stu-id="f96ec-117">If you have an Edge pool and are using a hardware load balancer, you must use public IP addresses on each of the Edge Servers and you cannot use NAT for the servers or the pool at your NAT device (for example, the firewall, or other infrastructure device that would NAT inbound or outbound traffic).</span></span> <span data-ttu-id="f96ec-118">Pour plus d’informations, reportez-vous à la section <A href="lync-server-2013-port-summary-scaled-consolidated-edge-with-hardware-load-balancers.md">Résumé de port-bordure consolidée mise en plan avec des équilibreurs de charge matérielle dans Lync Server 2013</A> dans la documentation relative à l’accès des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="f96ec-118">For details, see <A href="lync-server-2013-port-summary-scaled-consolidated-edge-with-hardware-load-balancers.md">Port summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</A> in the Planning for External User Access documentation.</span></span>

    
    </div>

  - <span data-ttu-id="f96ec-119">Si votre organisation utilise une infrastructure de qualité de service (QoS), le sous-système multimédia est compatible avec cette infrastructure.</span><span class="sxs-lookup"><span data-stu-id="f96ec-119">If your organization uses a Quality of Service (QoS) infrastructure, the media subsystem is designed to work within this existing infrastructure.</span></span>

  - <span data-ttu-id="f96ec-120">Si vous utilisez le protocole IPSec, nous vous recommandons de le désactiver sur les plages de ports utilisées pour le trafic A/V.</span><span class="sxs-lookup"><span data-stu-id="f96ec-120">If you use Internet Protocol security (IPsec), we recommend disabling IPsec over the port ranges used for A/V traffic.</span></span> <span data-ttu-id="f96ec-121">Pour plus d’informations, reportez-vous à la section [exceptions IPSec dans Lync Server 2013](lync-server-2013-ipsec-exceptions.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="f96ec-121">For details, see [IPsec exceptions in Lync Server 2013](lync-server-2013-ipsec-exceptions.md) in the Planning documentation.</span></span>

<span data-ttu-id="f96ec-122">Pour garantir une qualité multimédia optimale, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="f96ec-122">To ensure optimal media quality, do the following:</span></span>

  - <span data-ttu-id="f96ec-123">Mise en service de vos liens réseau pour prendre en charge le débit de 65 kilobits par seconde (kbps) par flux audio et 500 kbps par flux vidéo, s’il est activé, pendant les périodes d’utilisation maximale.</span><span class="sxs-lookup"><span data-stu-id="f96ec-123">Provision your network links to support throughput of 65 kilobits per second (Kbps) per audio stream and 500 Kbps per video stream, if enabled, during peak usage periods.</span></span> <span data-ttu-id="f96ec-124">Une session audio ou vidéo bidirectionnelle est composée de deux flux.</span><span class="sxs-lookup"><span data-stu-id="f96ec-124">A bidirectional audio or video session consists of two streams.</span></span>

  - <span data-ttu-id="f96ec-125">Pour gérer les pics inattendus du trafic au-dessus de ce niveau et augmenter l’utilisation au fil du temps, les points de terminaison de Lync Server Media peuvent s’adapter à des conditions de réseau variables et prendre en charge des charges de trois fois sur le débit (voir le paragraphe précédent) pour les appels audio et vidéo tout en préservant la qualité acceptable.</span><span class="sxs-lookup"><span data-stu-id="f96ec-125">To cope with unexpected spikes in traffic above this level and increased usage over time, Lync Server media endpoints can adapt to varying network conditions and support loads of three times the throughput (see previous paragraph) for audio and video while still retaining acceptable quality.</span></span> <span data-ttu-id="f96ec-126">Toutefois, ne supposez pas que cette capacité d’adaptation prend en charge un réseau sous-approvisionné.</span><span class="sxs-lookup"><span data-stu-id="f96ec-126">However, do not assume that this adaptability will support an under-provisioned network.</span></span> <span data-ttu-id="f96ec-127">Dans un réseau sous-approvisionné, la capacité des points de terminaison Lync Server Media d’une manière dynamique avec des conditions de réseau variables (par exemple, une perte de paquets de grande durée temporaire) est réduite.</span><span class="sxs-lookup"><span data-stu-id="f96ec-127">In an under-provisioned network, the ability of the Lync Server media endpoints to dynamically deal with varying network conditions (for example, temporary high packet loss) is reduced.</span></span>

  - <span data-ttu-id="f96ec-128">Pour les liens réseau dans lesquels la mise en service est extrêmement onéreuse et difficile, il est possible que vous deviez envisager la mise en service pour un volume inférieur de trafic.</span><span class="sxs-lookup"><span data-stu-id="f96ec-128">For network links where provisioning is extremely costly and difficult, you may need to consider provisioning for a lower volume of traffic.</span></span> <span data-ttu-id="f96ec-129">Dans ce scénario, l’élasticité des points de terminaison de Lync Server Media absorbe la différence entre le volume de trafic et le niveau de trafic de pointe, au coût d’une diminution de la qualité de la voix.</span><span class="sxs-lookup"><span data-stu-id="f96ec-129">In this scenario, let the elasticity of the Lync Server media endpoints absorb the difference between the traffic volume and the peak traffic level, at the cost of some reduction in the voice quality.</span></span> <span data-ttu-id="f96ec-130">Par ailleurs, il y a une diminution de l’impasse de la hauteur pour absorber les crêtes soudaines du trafic.</span><span class="sxs-lookup"><span data-stu-id="f96ec-130">Also, there is a decrease in the headroom otherwise available to absorb sudden peaks in traffic.</span></span>

  - <span data-ttu-id="f96ec-131">Pour les liens qui ne peuvent pas être configurés correctement en courte durée (par exemple, un site avec de très mauvaises liaisons WAN), envisagez de désactiver la vidéo pour certains utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f96ec-131">For links that cannot be correctly provisioned in the short term (for example, a site with very poor WAN links), consider disabling video for certain users.</span></span>

  - <span data-ttu-id="f96ec-132">Mise en service de votre réseau pour garantir un délai de bout en bout maximal (latence) de 150 millisecondes (MS) en faible charge.</span><span class="sxs-lookup"><span data-stu-id="f96ec-132">Provision your network to ensure a maximum end-to-end delay (latency) of 150 milliseconds (ms) under peak load.</span></span> <span data-ttu-id="f96ec-133">La latence correspond à une déficience du réseau qui empêche les composants multimédias de Lync Server de réduire, et il est important de rechercher et d’éliminer les points faibles.</span><span class="sxs-lookup"><span data-stu-id="f96ec-133">Latency is the one network impairment that Lync Server media components cannot reduce, and it is important to find and eliminate the weak points.</span></span>

  - <span data-ttu-id="f96ec-134">Pour les serveurs exécutant un logiciel antivirus, incluez tous les serveurs exécutant Lync Server dans la liste des exceptions afin de fournir des performances et une qualité audio optimales.</span><span class="sxs-lookup"><span data-stu-id="f96ec-134">For servers running antivirus software, include all servers running Lync Server in the exception list in order to provide optimal performance and audio quality.</span></span>

</div>

<div>

## <a name="conferencing-network-requirements"></a><span data-ttu-id="f96ec-135">Configuration réseau requise</span><span class="sxs-lookup"><span data-stu-id="f96ec-135">Conferencing Network Requirements</span></span>

<span data-ttu-id="f96ec-136">La bande passante utilisée pour télécharger le contenu de la Conférence à partir du serveur IIS (Internet Information Services) dépend de la taille du contenu chargé.</span><span class="sxs-lookup"><span data-stu-id="f96ec-136">The bandwidth that is used to download conference content from the Internet Information Services (IIS) server depends on the size of the content that is uploaded.</span></span>

<span data-ttu-id="f96ec-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f96ec-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

