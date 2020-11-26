---
title: 'Lync Server 2013 : Prise en charge de la haute disponibilité et de la récupération d’urgence'
description: 'Lync Server 2013 : prise en charge du service de haute disponibilité et de récupération d’urgence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: High availability and disaster recovery support
ms:assetid: 47e77e85-c7c3-4ade-8db7-a34c71aeafd7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204866(v=OCS.15)
ms:contentKeyID: 48184053
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8113c6b54cbb55e8149f8d6dd1b53ccbdc9436d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427627"
---
# <a name="high-availability-and-disaster-recovery-support-in-lync-server-2013"></a><span data-ttu-id="31cda-103">Prise en charge de la haute disponibilité et de la récupération d’urgence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31cda-103">High availability and disaster recovery support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="31cda-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="31cda-104">

<span> </span></span></span>

<span data-ttu-id="31cda-105">_**Dernière modification de la rubrique :** 2012-09-25_</span><span class="sxs-lookup"><span data-stu-id="31cda-105">_**Topic Last Modified:** 2012-09-25_</span></span>

<span data-ttu-id="31cda-106">Lync Server 2013 offre une haute disponibilité grâce à la redondance du serveur via le regroupement.</span><span class="sxs-lookup"><span data-stu-id="31cda-106">Lync Server 2013 provides high availability by server redundancy via pooling.</span></span> <span data-ttu-id="31cda-107">Si un serveur exécutant un rôle serveur particulier rencontre une défaillance, les autres serveurs du pool qui exécutent le même rôle assument la charge de ce serveur.</span><span class="sxs-lookup"><span data-stu-id="31cda-107">If a server running a certain server role fails, the other servers in the pool running the same role take the load of that server.</span></span> <span data-ttu-id="31cda-108">Cela s’applique aux serveurs frontaux, aux serveurs Edge, aux serveurs de médiation et aux directeurs.</span><span class="sxs-lookup"><span data-stu-id="31cda-108">This applies to Front End Servers, Edge Servers, Mediation Servers, and Directors.</span></span> <span data-ttu-id="31cda-109">Pour plus d’informations sur les rôles de serveur, voir [rôles de serveur dans Lync server 2013](lync-server-2013-server-roles.md).</span><span class="sxs-lookup"><span data-stu-id="31cda-109">For details about server roles, see [Server roles in Lync Server 2013](lync-server-2013-server-roles.md).</span></span>

<span data-ttu-id="31cda-110">Lync Server 2013 fournit également des mesures de reprise après sinistre en activant le jumelage de pools.</span><span class="sxs-lookup"><span data-stu-id="31cda-110">Lync Server 2013 also provides disaster recovery measures by enabling pool pairing.</span></span> <span data-ttu-id="31cda-111">Si vous déployez cette topologie, vous désignez des paires de pools frontaux, chaque pool d’une paire étant situé dans un centre de données distinct et dans une zone géographique distincte.</span><span class="sxs-lookup"><span data-stu-id="31cda-111">If you deploy this topology, you will designate pairs of Front End pools, with each pool in a pair located in a separate data center, and in a separate geographical area.</span></span> <span data-ttu-id="31cda-112">Si un pool ou un site n’est plus opérationnel, vous pouvez rediriger les utilisateurs de ce pool afin qu’ils se servent de l’autre pool de la paire, avec une interruption minimale du service.</span><span class="sxs-lookup"><span data-stu-id="31cda-112">If one pool or site goes down, you can redirect the users of that pool to use the other pool in the pair, with minimal interruption of service.</span></span>

<span data-ttu-id="31cda-113">Lync Server 2013 prend également en charge la haute disponibilité du serveur principal.</span><span class="sxs-lookup"><span data-stu-id="31cda-113">Lync Server 2013 also supports Back End Server high availability.</span></span> <span data-ttu-id="31cda-114">Il s’agit d’une topologie facultative dans laquelle vous déployez deux serveurs back-end pour une liste frontale et configurez la mise en miroir SQL Server synchrone pour toutes les bases de données Lync exécutées sur les serveurs principaux.</span><span class="sxs-lookup"><span data-stu-id="31cda-114">This is an optional topology in which you deploy two Back End Servers for a Front End pool, and set up synchronous SQL Server mirroring for all the Lync databases running on the Back End Servers.</span></span>

<span data-ttu-id="31cda-115">Pour plus d’informations sur le jumelage de pools et la mise en miroir du serveur principal, voir [planification d’une haute disponibilité et reprise après sinistre dans Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="31cda-115">For details about pool pairing and Back End Server mirroring, see [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="31cda-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31cda-116">See Also</span></span>


[<span data-ttu-id="31cda-117">Rôles serveur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31cda-117">Server roles in Lync Server 2013</span></span>](lync-server-2013-server-roles.md)  
[<span data-ttu-id="31cda-118">Planification de la haute disponibilité et de la récupération d’urgence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31cda-118">Planning for high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)  
  

<span data-ttu-id="31cda-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="31cda-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

