---
title: 'Lync Server 2013 : Pool directeur mis à l’échelle - Équilibreur de charge matérielle'
description: 'Lync Server 2013 : pool de Directors mis à l’échelle-équilibrage de charge matérielle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scaled Director pool - hardware load balancer
ms:assetid: cf34759a-b384-479c-855f-ea5e80a234b6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205316(v=OCS.15)
ms:contentKeyID: 48185585
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 022c5afb67687149f8ba24655be2a1461d4371f2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393952"
---
# <a name="scaled-director-pool---hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="2bf13-103">Pool directeur mis à l’échelle - Équilibreur de charge matérielle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2bf13-103">Scaled Director pool - hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2bf13-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2bf13-104">

<span> </span></span></span>

<span data-ttu-id="2bf13-105">_**Dernière modification de la rubrique :** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="2bf13-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="2bf13-106">Dans le cas d’un pool de Directors mis à l’échelle, lorsque plusieurs Directors sont déployés pour gérer une capacité supplémentaire et de garantir une haute disponibilité, l’équilibrage de la charge des clients et du serveur doit être distribué auprès de tous les membres du pool.</span><span class="sxs-lookup"><span data-stu-id="2bf13-106">A scaled Director pool, where there are more than one Director is deployed to handle additional capacity and to provide high availability, requires load balancing to distribute client and server communication to all members of the pool.</span></span> <span data-ttu-id="2bf13-107">Un directeur héberge des services Web de la même façon qu’un pool frontal.</span><span class="sxs-lookup"><span data-stu-id="2bf13-107">A Director hosts web services much like a Front End pool.</span></span> <span data-ttu-id="2bf13-108">L’équilibrage de charge matérielle est requis pour les services Web.</span><span class="sxs-lookup"><span data-stu-id="2bf13-108">Hardware load balancing is required for the web services.</span></span>

<span data-ttu-id="2bf13-109">Les rubriques suivantes décrivent les considérations en matière de planification pour le déploiement d’un pool de réalisateurs à l’aide de l’équilibrage de charge matérielle.</span><span class="sxs-lookup"><span data-stu-id="2bf13-109">The following topics describe the planning considerations for deploying a Director pool using hardware load balancing.</span></span> <span data-ttu-id="2bf13-110">Si vous envisagez d’utiliser l’équilibrage de charge matérielle et l’équilibrage de charge DNS pour le pool de directeurs, voir la rubrique [pool de répertoires mis à l’échelle-équilibrage de charge DNS et équilibrage de charge matérielle dans Lync Server 2013](lync-server-2013-scaled-director-pool-dns-load-balancing-and-hardware-load-balancer.md) qui décrit les exigences de planification pour cette topologie.</span><span class="sxs-lookup"><span data-stu-id="2bf13-110">If you intend to use hardware load balancing and DNS load balancing for the Director pool, see the topic [Scaled Director pool - DNS load balancing and hardware load balancer in Lync Server 2013](lync-server-2013-scaled-director-pool-dns-load-balancing-and-hardware-load-balancer.md) that describes the planning requirements for that topology.</span></span>

<span data-ttu-id="2bf13-111">![cfa892b9-5b24-4245-b5bd-c5da21984eeb](images/JJ205316.cfa892b9-5b24-4245-b5bd-c5da21984eeb(OCS.15).jpg "cfa892b9-5b24-4245-b5bd-c5da21984eeb")</span><span class="sxs-lookup"><span data-stu-id="2bf13-111">![cfa892b9-5b24-4245-b5bd-c5da21984eeb](images/JJ205316.cfa892b9-5b24-4245-b5bd-c5da21984eeb(OCS.15).jpg "cfa892b9-5b24-4245-b5bd-c5da21984eeb")</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2bf13-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="2bf13-112">In This Section</span></span>

  - [<span data-ttu-id="2bf13-113">Résumé des certificats - Pool directeur mis à l’échelle, équilibreur de charge matérielle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2bf13-113">Certificate summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-director-pool-hardware-load-balancer.md)

  - [<span data-ttu-id="2bf13-114">Résumé des ports - Pool directeur mis à l’échelle, équilibreur de charge matérielle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2bf13-114">Port summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-port-summary-scaled-director-pool-hardware-load-balancer.md)

  - [<span data-ttu-id="2bf13-115">Résumé DNS - Pool directeur mis à l’échelle, équilibreur de charge matérielle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2bf13-115">DNS summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-dns-summary-scaled-director-pool-hardware-load-balancer.md)

<span data-ttu-id="2bf13-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2bf13-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

