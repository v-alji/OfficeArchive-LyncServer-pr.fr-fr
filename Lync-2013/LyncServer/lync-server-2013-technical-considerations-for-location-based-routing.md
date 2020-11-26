---
title: 'Lync Server 2013 : Considérations techniques relatives au routage géodépendant'
description: 'Lync Server 2013 : considérations techniques pour le routage Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical considerations for Location-Based Routing
ms:assetid: 2e2a9199-7c6f-48d3-9adb-3873fc4f8c4e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994027(v=OCS.15)
ms:contentKeyID: 51803936
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54a025af81ab148ad41f95d0a8cf4f900beb7e00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423427"
---
# <a name="technical-considerations-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="120f2-103">Considérations techniques relatives au routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="120f2-103">Technical considerations for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="120f2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="120f2-104">

<span> </span></span></span>

<span data-ttu-id="120f2-105">_**Dernière modification de la rubrique :** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="120f2-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="120f2-106">Lors de la planification Location-Based le routage, vous devez prendre en compte l’impact sur les situations suivantes.</span><span class="sxs-lookup"><span data-stu-id="120f2-106">When planning Location-Based Routing, you should consider the impact to the following scenarios.</span></span>

<div>

## <a name="disaster-recovery"></a><span data-ttu-id="120f2-107">Récupération d’urgence</span><span class="sxs-lookup"><span data-stu-id="120f2-107">Disaster Recovery</span></span>

<span data-ttu-id="120f2-108">Lors d’un basculement entre le pool principal et un pool de sauvegarde, ainsi que lors de la restauration d’opérations normales sur le pool principal, Location-Based le routage reste appliqué à tout moment dans le cadre d’une procédure de sinistre et de récupération.</span><span class="sxs-lookup"><span data-stu-id="120f2-108">During a failover from the primary pool to a backup pool as well as when restoring normal operations to the primary pool, Location-Based Routing remains enforced at all times during a disaster and recovery procedure.</span></span>

</div>

<div>

## <a name="survivable-branch-appliance"></a><span data-ttu-id="120f2-109">Survivable Branch Appliance</span><span class="sxs-lookup"><span data-stu-id="120f2-109">Survivable Branch Appliance</span></span>

<span data-ttu-id="120f2-110">La configuration du routage Location-Based affecte la planification de l’endroit où vous déployez les passerelles associées à vos appareils distants.</span><span class="sxs-lookup"><span data-stu-id="120f2-110">Configuring Location-Based Routing impacts the planning of where you deploy the gateways associated to your Survivable Branch Appliances.</span></span> <span data-ttu-id="120f2-111">La passerelle associée à votre SBA doit se trouver dans le même site réseau que votre application de succursale Survivable ; dans le cas contraire, les utilisateurs hébergés sur votre unité de branchement Survivable ne sont pas autorisés à passer des appels sortants si Location-Based le routage est configuré.</span><span class="sxs-lookup"><span data-stu-id="120f2-111">The gateway associated to your SBA must be located in the same network site as your Survivable Branch Appliance; otherwise, users homed on your Survivable Branch Appliance will not be permitted to place outbound calls if Location-Based Routing is configured.</span></span> <span data-ttu-id="120f2-112">Lorsque la connexion WAN entre votre appareil de branchement Survivable et le site central est en panne, Location-Based restrictions de routage reste appliquées.</span><span class="sxs-lookup"><span data-stu-id="120f2-112">When the WAN connection between your Survivable Branch Appliance and the central site is down, Location-Based Routing restrictions remains enforced.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="120f2-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="120f2-113">See Also</span></span>


[<span data-ttu-id="120f2-114">Planification du routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="120f2-114">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="120f2-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="120f2-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

