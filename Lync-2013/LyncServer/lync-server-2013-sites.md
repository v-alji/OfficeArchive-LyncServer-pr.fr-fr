---
title: Sites Lync Server 2013
description: Sites Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Sites
ms:assetid: 022cb6dd-37e2-4882-a53e-5ddfdbc6f53a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398076(v=OCS.15)
ms:contentKeyID: 48183233
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 59739c5a81fca1f1f3ab5c1b83a23f0be0a5ee2d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423798"
---
# <a name="lync-server-sites-for-lync-server-2013"></a><span data-ttu-id="1a0e8-103">Sites Lync Server pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a0e8-103">Lync Server sites for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1a0e8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1a0e8-104">

<span> </span></span></span>

<span data-ttu-id="1a0e8-105">_**Dernière modification de la rubrique :** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="1a0e8-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="1a0e8-106">Dans Lync Server, vous définissez des *sites* sur votre réseau qui contiennent des composants serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-106">In Lync Server, you define *sites* on your network that contain Lync Server components.</span></span> <span data-ttu-id="1a0e8-107">Un site désigne un ensemble d’ordinateurs connectés comme il se doit par un réseau haut débit à faible latence, par exemple, un réseau local unique (LAN) ou bien deux réseaux connectés via un réseau haut débit à fibre optique.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-107">A site is a set of computers that is well-connected by a high-speed, low-latency network, such as a single local area network (LAN) or two networks connected by a high-speed fiber optic network.</span></span> <span data-ttu-id="1a0e8-108">Notez que les sites serveur Lync constituent un concept distinct des sites services de domaine Active Directory et des sites Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-108">Note that Lync Server sites are a separate concept from Active Directory Domain Services sites and Microsoft Exchange Server sites.</span></span> <span data-ttu-id="1a0e8-109">Les sites de votre serveur Lync n’ont pas besoin de correspondre à vos sites Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-109">Your Lync Server sites do not need to correspond to your Active Directory sites.</span></span>

<div>

## <a name="site-types"></a><span data-ttu-id="1a0e8-110">Types de sites</span><span class="sxs-lookup"><span data-stu-id="1a0e8-110">Site Types</span></span>

<span data-ttu-id="1a0e8-111">Chaque site est un *site central* contenant au moins un pool frontal ou un serveur Standard Edition Server ou un *site de succursale*.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-111">Each site is either a *central site*, which contains at least one Front End pool or a Standard Edition server, or a *branch site*.</span></span> <span data-ttu-id="1a0e8-112">Chaque site de filiale est associé à un seul site central, et les utilisateurs du site de succursale obtiennent la plupart des fonctionnalités de Lync Server sur les serveurs du site central associé.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-112">Each branch site is associated with exactly one central site, and the users at the branch site get most of their Lync Server functionality from the servers at the associated central site.</span></span>

<span data-ttu-id="1a0e8-113">Chaque site de filiale contient l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a0e8-113">Each branch site contains one of the following:</span></span>

  - <span data-ttu-id="1a0e8-114">Un *appareil de branchement survivant (SBA)*, qui est un serveur de Blades standard avec un bureau d’enregistrement de serveurs Lync et un serveur de médiation exécuté sur Windows Server.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-114">A *Survivable Branch Appliance (SBA)*, which is an industry-standard blade server with a Lync Server Registrar and a Mediation Server running on Windows Server.</span></span> <span data-ttu-id="1a0e8-115">L’unité de branchement Survivable comporte également une passerelle RTC (réseau téléphonique commuté).</span><span class="sxs-lookup"><span data-stu-id="1a0e8-115">The Survivable Branch Appliance also contains a public switched telephone network (PSTN) gateway.</span></span> <span data-ttu-id="1a0e8-116">L’unité de branchement survivant est conçue pour les sites de succursale entre 25 et 1000 utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-116">The Survivable Branch Appliance is designed for branch sites with between 25 and 1000 users.</span></span>

  - <span data-ttu-id="1a0e8-117">Un *serveur de succursales survivant (SBS)*, qui est un serveur exécutant Windows Server qui répond à la configuration matérielle requise, et sur lequel sont installés le logiciel serveur du Bureau d’enregistrement et de médiation de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-117">A *Survivable Branch Server (SBS)*, which is a server running Windows Server that meets specified hardware requirements, and that has Lync Server Registrar and Mediation Server software installed on it.</span></span> <span data-ttu-id="1a0e8-118">Il doit se connecter à une passerelle PSTN ou à une jonction SIP à un fournisseur de services téléphoniques.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-118">It must connect to either a PSTN gateway or a SIP trunk to a telephone service provider.</span></span> <span data-ttu-id="1a0e8-119">Le serveur de succursales survivant est conçu pour les sites de succursale entre les utilisateurs 1000 et 5000.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-119">The Survivable Branch Server is designed for branch sites with between 1000 and 5000 users.</span></span>

  - <span data-ttu-id="1a0e8-120">Passerelle RTC et, éventuellement, *serveur de médiation*.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-120">A PSTN gateway, and, optionally, a *Mediation Server*.</span></span> <span data-ttu-id="1a0e8-121">Pour plus d’informations sur ces rôles de serveur, voir [rôles de serveur dans Lync server 2013](lync-server-2013-server-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1a0e8-121">For details on this and other server roles, see [Server roles in Lync Server 2013](lync-server-2013-server-roles.md).</span></span>

<span data-ttu-id="1a0e8-122">Une succursale disposant d’une liaison réseau étendu (WAN) fiable vers un site central peut utiliser la troisième option : une passerelle RTC et éventuellement un serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-122">A branch office with a resilient wide area network (WAN) link to a central site can use the third option—a PSTN gateway, and, optionally, a Mediation Server.</span></span> <span data-ttu-id="1a0e8-123">Les sites de succursales dotés de liens moins résilients doivent utiliser un appareil de succursales ou un serveur de succursales Survivables, qui fournit la résilience en cas de panne du réseau étendu.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-123">Branch office sites with less-resilient links should use a Survivable Branch Appliance or Survivable Branch Server, which provide resiliency in times of wide-area network failures.</span></span> <span data-ttu-id="1a0e8-124">Par exemple, dans le cas d’un site disposant d’une unité de succursale ou d’un serveur de succursale survivant, les utilisateurs peuvent quand même passer et recevoir des appels voix d’entreprise si le WAN qui connecte le site de la succursale au site central est arrêté.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-124">For example, in a site with a Survivable Branch Appliance or Survivable Branch Server deployed, users can still make and receive Enterprise Voice calls if the WAN connecting the branch site to the central site is down.</span></span> <span data-ttu-id="1a0e8-125">Pour plus d’informations sur l’appareil de succursale survivant, le serveur de succursales survivant et la résilience, voir [planification de la résilience vocale d’entreprise dans Lync Server 2013](lync-server-2013-planning-for-enterprise-voice-resiliency.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-125">For details about the Survivable Branch Appliance, Survivable Branch Server, and resiliency, see [Planning for Enterprise Voice resiliency in Lync Server 2013](lync-server-2013-planning-for-enterprise-voice-resiliency.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="site-topologies"></a><span data-ttu-id="1a0e8-126">Topologies de site</span><span class="sxs-lookup"><span data-stu-id="1a0e8-126">Site Topologies</span></span>

<span data-ttu-id="1a0e8-127">Votre déploiement doit inclure au moins un site central et peut inclure zéro sur plusieurs sites de succursales.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-127">Your deployment must include at least one central site, and can include zero to many branch sites.</span></span> <span data-ttu-id="1a0e8-128">Chaque site de filiale est affilié à un site central.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-128">Each branch site is affiliated with one central site.</span></span> <span data-ttu-id="1a0e8-129">Le site central fournit les services serveur Lync au site de succursale qui ne sont pas hébergés localement sur le site de la succursale, tels que la présence et la Conférence.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-129">The central site provides the Lync Server services to the branch site that are not hosted locally at the branch site, such as presence and conferencing.</span></span>

<span data-ttu-id="1a0e8-130">Si vous disposez de plusieurs sites, vous pouvez associer les pools front-end sur différents sites pour activer la fonction de reprise après sinistre.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-130">If you have multiple sites, you can pair together the Front End pools at different sites to enable disaster recovery abilities.</span></span> <span data-ttu-id="1a0e8-131">Pour plus d’informations, voir [prise en charge de la haute disponibilité et de la reprise après sinistre dans Lync Server 2013](lync-server-2013-high-availability-and-disaster-recovery-support.md).</span><span class="sxs-lookup"><span data-stu-id="1a0e8-131">For details, see [High availability and disaster recovery support in Lync Server 2013](lync-server-2013-high-availability-and-disaster-recovery-support.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1a0e8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a0e8-132">See Also</span></span>


[<span data-ttu-id="1a0e8-133">Rôles serveur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a0e8-133">Server roles in Lync Server 2013</span></span>](lync-server-2013-server-roles.md)  
[<span data-ttu-id="1a0e8-134">Prise en charge de la haute disponibilité et de la récupération d’urgence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a0e8-134">High availability and disaster recovery support in Lync Server 2013</span></span>](lync-server-2013-high-availability-and-disaster-recovery-support.md)  


[<span data-ttu-id="1a0e8-135">Planification de la résistance Voix Entreprise dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a0e8-135">Planning for Enterprise Voice resiliency in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice-resiliency.md)  
  

<span data-ttu-id="1a0e8-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1a0e8-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

