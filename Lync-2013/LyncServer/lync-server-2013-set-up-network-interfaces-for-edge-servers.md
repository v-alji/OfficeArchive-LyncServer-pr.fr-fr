---
title: 'Lync Server 2013 : Configuration des interfaces réseau pour les serveurs Edge'
description: 'Lync Server 2013 : configurez les interfaces réseau pour les serveurs Edge.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set up network interfaces for Edge Servers
ms:assetid: b0aecdf6-4ae2-46f6-b9b6-948bfc3df11e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412847(v=OCS.15)
ms:contentKeyID: 48185152
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 576ca8670a34be022e3df0a699edaf0df10f5b70
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441738"
---
# <a name="set-up-network-interfaces-for-edge-servers-in-lync-server-2013"></a><span data-ttu-id="5b122-103">Configuration des interfaces réseau pour les serveurs Edge dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5b122-103">Set up network interfaces for Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b122-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b122-104">

<span> </span></span></span>

<span data-ttu-id="5b122-105">_**Dernière modification de la rubrique :** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="5b122-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="5b122-106">Chaque serveur Edge est un ordinateur multirésident doté d’interfaces externes et internes.</span><span class="sxs-lookup"><span data-stu-id="5b122-106">Each Edge Server is a multihomed computer with external and internal facing interfaces.</span></span> <span data-ttu-id="5b122-107">Les paramètres de système de noms de domaine (DNS) d’adaptateur dépendent de la présence de serveurs DNS dans le réseau de périmètre.</span><span class="sxs-lookup"><span data-stu-id="5b122-107">The adapter Domain Name System (DNS) settings depend on whether there are DNS servers in the perimeter network.</span></span> <span data-ttu-id="5b122-108">Si les serveurs DNS existent dans le périmètre, ils doivent disposer d’une zone contenant un ou plusieurs enregistrements DNS A pour le serveur de tronçon suivant ou le pool (c’est-à-dire, un directeur ou un pool frontal désigné) et pour les requêtes externes, elles font référence à des recherches de nom à d’autres serveurs DNS publics.</span><span class="sxs-lookup"><span data-stu-id="5b122-108">If DNS servers exist in the perimeter, they must have a zone containing one or more DNS A records for the next hop server or pool (that is, either a Director or a designated Front End pool), and for external queries they refer name lookups to other public DNS servers.</span></span> <span data-ttu-id="5b122-109">S’il n’existe aucun serveur DNS sur le périmètre, le ou les serveurs de périphérie utilisent des serveurs DNS externes pour résoudre les recherches de noms Internet et chaque serveur Edge utilise un hôte pour résoudre les noms de serveurs de sauts suivants en adresses IP.</span><span class="sxs-lookup"><span data-stu-id="5b122-109">If no DNS servers exist in the perimeter, the Edge Server(s) use external DNS servers to resolve Internet name lookups, and each Edge Server uses a HOST to resolve the next hop server names to IP addresses.</span></span>

<div>

<table>
<thead>
<tr class="header">
<th><img src="images/Gg398321.security(OCS.15).gif" title="sûreté" alt="security" /><span data-ttu-id="5b122-111">Note de sécurité :</span><span class="sxs-lookup"><span data-stu-id="5b122-111">Security Note:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b122-112">Pour des raisons de sécurité, nous vous recommandons de ne pas que vos serveurs Edge accèdent à un serveur DNS situé dans le réseau interne.</span><span class="sxs-lookup"><span data-stu-id="5b122-112">For security reasons, we recommend that you do not have your Edge Servers access a DNS server located in the internal network.</span></span></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="to-configure-interfaces-with-dns-servers-in-the-perimeter-network"></a><span data-ttu-id="5b122-113">Pour configurer des interfaces avec des serveurs DNS dans le réseau de périmètre</span><span class="sxs-lookup"><span data-stu-id="5b122-113">To configure interfaces with DNS servers in the perimeter network</span></span>

1.  <span data-ttu-id="5b122-114">Installez deux cartes réseau pour chaque serveur Edge, une pour l’interface interne et une pour l’interface externe.</span><span class="sxs-lookup"><span data-stu-id="5b122-114">Install two network adapters for each Edge Server, one for the internal-facing interface and one for the external-facing interface.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="5b122-115">Les sous-réseaux interne et externe ne doivent pas être routables entre eux.</span><span class="sxs-lookup"><span data-stu-id="5b122-115">The internal and external subnets must not be routable to each other.</span></span>

    
    </div>

2.  <span data-ttu-id="5b122-116">Sur l’interface externe, configurez trois adresses IP statiques sur le réseau de périmètre externe (également connu sous le nom de DMZ, zone démilitarisée et sous-réseau à écran), puis pointez la passerelle par défaut vers l’interface interne du pare-feu externe.</span><span class="sxs-lookup"><span data-stu-id="5b122-116">On the external interface, configure three static IP addresses on the external perimeter network (also known as DMZ, demilitarized zone, and screened subnet) subnet, and point the default gateway to the internal interface of the external firewall.</span></span> <span data-ttu-id="5b122-117">Configurez les paramètres DNS de l’adaptateur de façon à ce qu’ils pointent vers une paire de serveurs DNS de périmètre.</span><span class="sxs-lookup"><span data-stu-id="5b122-117">Configure adapter DNS settings to point to a pair of perimeter DNS servers.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5b122-118">Il est possible d’utiliser une seule adresse IP pour cette interface, mais pour cela, vous devez remplacer les affectations de port par des valeurs non standard.</span><span class="sxs-lookup"><span data-stu-id="5b122-118">It is possible to use as few as one IP address for this interface, but to do this you need to change the port assignments to non-standard values.</span></span> <span data-ttu-id="5b122-119">Vous déterminez cela lorsque vous créez la topologie dans le générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="5b122-119">You determine this when you create the topology in Topology Builder.</span></span>

    
    </div>

3.  <span data-ttu-id="5b122-120">Dans l’interface interne, configurez une adresse IP statique sur le sous-réseau de périmètre interne et ne définissez aucune passerelle par défaut.</span><span class="sxs-lookup"><span data-stu-id="5b122-120">On the internal interface, configure one static IP address on the internal perimeter network subnet and do not set a default gateway.</span></span> <span data-ttu-id="5b122-121">Configurez les paramètres DNS de l’adaptateur de façon à ce qu’ils pointent vers au moins un serveur DNS, de préférence une paire de serveurs DNS de périmètre.</span><span class="sxs-lookup"><span data-stu-id="5b122-121">Configure adapter DNS settings to point to at least one DNS server, preferably a pair of perimeter DNS servers.</span></span>

4.  <span data-ttu-id="5b122-122">Créez des itinéraires statiques persistants sur l’interface interne vers tous les réseaux internes dans lesquels résident les clients, Lync Server 2013 et les serveurs Exchange Unified Messaging (UM).</span><span class="sxs-lookup"><span data-stu-id="5b122-122">Create persistent static routes on the internal interface to all internal networks where clients, Lync Server 2013, and Exchange Unified Messaging (UM) servers reside.</span></span>

</div>

<div>

## <a name="to-configure-interfaces-without-dns-servers-in-the-perimeter-network"></a><span data-ttu-id="5b122-123">Pour configurer des interfaces sans serveurs DNS dans le réseau de périmètre</span><span class="sxs-lookup"><span data-stu-id="5b122-123">To configure interfaces without DNS servers in the perimeter network</span></span>

1.  <span data-ttu-id="5b122-124">Installez deux cartes réseau pour chaque serveur Edge, une pour l’interface interne et une pour l’interface externe.</span><span class="sxs-lookup"><span data-stu-id="5b122-124">Install two network adapters for each Edge Server, one for the internal-facing interface and one for the external-facing interface.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="5b122-125">Les sous-réseaux interne et externe ne doivent pas être routables entre eux.</span><span class="sxs-lookup"><span data-stu-id="5b122-125">The internal and external subnets must not be routable to each other.</span></span>

    
    </div>

2.  <span data-ttu-id="5b122-126">Sur l’interface externe, configurez trois adresses IP statiques sur le sous-réseau de périmètre externe.</span><span class="sxs-lookup"><span data-stu-id="5b122-126">On the external interface, configure three static IP addresses on the external perimeter network subnet.</span></span> <span data-ttu-id="5b122-127">Vous configurez également la passerelle par défaut sur l’interface externe.</span><span class="sxs-lookup"><span data-stu-id="5b122-127">You also configure the default gateway on the external interface.</span></span> <span data-ttu-id="5b122-128">Par exemple, définissez le routeur Internet ou le pare-feu externe comme passerelle par défaut.</span><span class="sxs-lookup"><span data-stu-id="5b122-128">For example, define the Internet-facing router or the external firewall as the default gateway.</span></span> <span data-ttu-id="5b122-129">Configurez les paramètres DNS pour qu’ils pointent vers un serveur DNS, de préférence vers une paire de serveurs DNS externes.</span><span class="sxs-lookup"><span data-stu-id="5b122-129">Configure DNS settings to point to a DNS server, preferably to a pair of external DNS servers.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5b122-130">Il est possible, mais déconseillé, d’utiliser autant qu’une seule adresse IP pour l’interface externe.</span><span class="sxs-lookup"><span data-stu-id="5b122-130">It is possible, but not recommended, to use as few as one IP address for the external interface.</span></span> <span data-ttu-id="5b122-131">Pour cela, vous devez remplacer les affectations de port par des valeurs non standard et quitter le port 443 par défaut, qui est généralement « compatible avec le pare-feu » pour la communication client.</span><span class="sxs-lookup"><span data-stu-id="5b122-131">To allow this to work, you need to change the port assignments to non-standard values, and away from the default port 443 that is typically “firewall friendly” for client communication.</span></span> <span data-ttu-id="5b122-132">Vous déterminez le paramètre d’adresse IP et les paramètres de port lorsque vous créez la topologie dans le générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="5b122-132">You determine the IP address setting and the port settings when you create the topology in Topology Builder.</span></span>

    
    </div>

3.  <span data-ttu-id="5b122-133">Dans l’interface interne, configurez une adresse IP statique sur le sous-réseau de périmètre interne et ne définissez aucune passerelle par défaut.</span><span class="sxs-lookup"><span data-stu-id="5b122-133">On the internal interface, configure one static IP address on the internal perimeter network subnet and do not set a default gateway.</span></span> <span data-ttu-id="5b122-134">Laissez les paramètres DNS de l’adaptateur vides.</span><span class="sxs-lookup"><span data-stu-id="5b122-134">Leave adapter DNS settings empty.</span></span>

4.  <span data-ttu-id="5b122-135">Créez des itinéraires statiques persistants sur l’interface interne vers tous les réseaux internes pour lesquels résident les clients ou serveurs Lync exécutant Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5b122-135">Create persistent static routes on the internal interface to all internal networks where Lync clients or servers running Lync Server 2013 reside.</span></span>

5.  <span data-ttu-id="5b122-136">Modifiez le fichier hôte sur chaque serveur Edge pour qu’il contienne un enregistrement pour le serveur du tronçon suivant ou l’adresse IP virtuelle (VIP) (l’enregistrement sera le directeur, Standard Edition Server, ou un pool frontal configuré en tant que serveur de périphérie du tronçon suivant dans le générateur de topologie).</span><span class="sxs-lookup"><span data-stu-id="5b122-136">Edit the HOST file on each Edge Server to contain a record for the next hop server or virtual IP (VIP) (the record will be the Director, Standard Edition server, or a Front End pool that was configured as the Edge Server next hop address in Topology Builder).</span></span> <span data-ttu-id="5b122-137">Si vous utilisez l’équilibrage de charge DNS, incluez une ligne pour chaque membre du pool de prochains tronçons.</span><span class="sxs-lookup"><span data-stu-id="5b122-137">If you are using DNS load balancing, include a line for each member of the next hop pool.</span></span>

<span data-ttu-id="5b122-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b122-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

