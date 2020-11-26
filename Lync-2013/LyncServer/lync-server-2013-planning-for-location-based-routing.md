---
title: 'Lync Server 2013 : Planification du routage géodépendant'
description: 'Lync Server 2013 : planification du routage Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Location-Based Routing
ms:assetid: bb035924-6b52-4f0f-8e05-b76864fb9ef3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994068(v=OCS.15)
ms:contentKeyID: 51803979
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 894a596e998fe07b97ad7911441eced670ba85b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442949"
---
# <a name="planning-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="fa96c-103">Planification du routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa96c-103">Planning for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fa96c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fa96c-104">

<span> </span></span></span>

<span data-ttu-id="fa96c-105">_**Dernière modification de la rubrique :** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="fa96c-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="fa96c-106">Les informations de cette rubrique font partie des mises à jour cumulatives pour Lync Server 2013 : février 2013.</span><span class="sxs-lookup"><span data-stu-id="fa96c-106">The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.</span></span>

<span data-ttu-id="fa96c-107">Location-Based le routage permet de limiter le routage des appels entre les points de terminaison VoIP et les points de terminaison RTC en fonction de l’emplacement des parties de l’appel.</span><span class="sxs-lookup"><span data-stu-id="fa96c-107">Location-Based Routing makes it possible to restrict the routing of calls between VoIP endpoints and PSTN endpoints based on the location of the parties in the call.</span></span> <span data-ttu-id="fa96c-108">Location-Based routage fait partie de l’infrastructure de voix entreprise 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fa96c-108">Location-Based Routing is part of the Lync Server 2013 Enterprise Voice infrastructure.</span></span> <span data-ttu-id="fa96c-109">Location-Based le routage est une fonctionnalité de gestion des appels qui contrôle le routage des appels par Lync Server 2013 CU1.</span><span class="sxs-lookup"><span data-stu-id="fa96c-109">Location-Based Routing is a call management feature that controls how calls are routed by Lync Server 2013 CU1.</span></span> <span data-ttu-id="fa96c-110">Il applique des règles d’autorisation des appels si les appels peuvent être routés vers des points de terminaison PBX ou PSTN en fonction de l’emplacement géographique de l’appelant Lync.</span><span class="sxs-lookup"><span data-stu-id="fa96c-110">It enforces call authorization rules on whether calls can be routed to PBX or PSTN endpoints based on the Lync caller’s geographic location.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="fa96c-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="fa96c-111">In This Section</span></span>

  - [<span data-ttu-id="fa96c-112">Vue d’ensemble du routage Location-Based dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa96c-112">Overview of Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-overview-of-location-based-routing.md)

  - [<span data-ttu-id="fa96c-113">Instructions de routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa96c-113">Guidance for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-guidance-for-location-based-routing.md)

  - [<span data-ttu-id="fa96c-114">Scénarios de routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa96c-114">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)

  - [<span data-ttu-id="fa96c-115">Considérations techniques relatives au routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa96c-115">Technical considerations for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-technical-considerations-for-location-based-routing.md)

  - [<span data-ttu-id="fa96c-116">Prise en charge des clients et des serveurs pour le routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa96c-116">Client and server support for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-client-and-server-support-for-location-based-routing.md)

  - [<span data-ttu-id="fa96c-117">Fonctionnalités non prises en charge par le routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa96c-117">Capabilities not supported by Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-capabilities-not-supported-by-location-based-routing.md)

  - [<span data-ttu-id="fa96c-118">Processus de déploiement du routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa96c-118">Deployment process for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-location-based-routing.md)

  - [<span data-ttu-id="fa96c-119">Routage basé sur l’emplacement pour les conférences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa96c-119">Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-location-based-routing-for-conferencing.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fa96c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa96c-120">See Also</span></span>


[<span data-ttu-id="fa96c-121">Planification d’Enterprise Voice dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa96c-121">Planning for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice.md)  
  

<span data-ttu-id="fa96c-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fa96c-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

