---
title: 'Lync Server 2013 : vue d’ensemble des Location-Based routage'
description: 'Lync Server 2013 : vue d’ensemble du routage Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Location-Based Routing
ms:assetid: 4aa494bd-0d66-4335-b9e8-f758d44a7202
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994032(v=OCS.15)
ms:contentKeyID: 51803941
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b1e026791a8562629231b91b58d7e7eff569ffa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394980"
---
# <a name="overview-of-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="e8b49-103">Vue d’ensemble du routage Location-Based dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e8b49-103">Overview of Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e8b49-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e8b49-104">

<span> </span></span></span>

<span data-ttu-id="e8b49-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="e8b49-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="e8b49-p101">Le routage géodépendant introduit de nouvelles règles modifiant le routage des appels RTC nationaux et internationaux pour empêcher le contournement des frais de réseau téléphonique commuté. Il offre la flexibilité nécessaire pour appliquer ces règles à certaines régions, passerelles ou groupes d’utilisateurs uniquement.</span><span class="sxs-lookup"><span data-stu-id="e8b49-p101">Location-Based Routing introduces a new set of rules that modifies the routing of national and international PSTN calls to prevent toll bypass. Location-Based Routing provides the flexibility to scope these rules to specific regions, specific gateways or to specific set of users only.</span></span>

<span data-ttu-id="e8b49-108">Les scénarios suivants illustrent les types principaux de restrictions Location-Based le routage peut appliquer :</span><span class="sxs-lookup"><span data-stu-id="e8b49-108">The following scenarios illustrate the main types of restrictions Location-Based Routing can enforce:</span></span>

  - <span data-ttu-id="e8b49-109">Appels de sortie : Location-Based le routage peut imposer des appels sortants à partir d’une passerelle PSTN qui se trouve dans la même région que celle de l’appelant, qui empêche les appels entrants vers la sortie à partir d’une passerelle RTC située dans une région différente de celle de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e8b49-109">Egress calls – Location-Based Routing can enforce outgoing calls to egress from a PSTN gateway that is located in the same region as where the caller is to prevent PSTN toll bypass, which prevents calls to egress from a PSTN gateway located in a different region as the caller.</span></span>

  - <span data-ttu-id="e8b49-110">Appels entrants : le routage Location-Based peut empêcher les appels RTC entrants de sonner sur des points de terminaison Lync si la passerelle RTC qui achemine l’appel entrant ne se trouve pas dans la même région que l’utilisateur appelé Lync.</span><span class="sxs-lookup"><span data-stu-id="e8b49-110">Ingress calls – Location-Based Routing can prevent incoming PSTN calls to ring Lync endpoints if the PSTN gateway routing the incoming call is not located in the same region as the called Lync user.</span></span>

  - <span data-ttu-id="e8b49-111">Régions inconnues : Location-Based le routage limite les appels RTC entrants et sortants vers et depuis les utilisateurs situés dans des emplacements indéterminés (c’est-à-dire, des utilisateurs distants qui se connectent à partir d’Internet ou qui se trouvent dans des régions inconnues).</span><span class="sxs-lookup"><span data-stu-id="e8b49-111">Unknown regions – Location-Based Routing restricts incoming and outgoing PSTN calls to and from users that are located in undetermined locations (i.e. remote users connecting from the Internet or located in unknown regions).</span></span>

  - <span data-ttu-id="e8b49-112">Régions internationales : le routage Location-Based applique le routage des appels sortants par le biais des passerelles RTC internationales s’il n’y a aucune passerelle locale vers l’emplacement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e8b49-112">International regions – Location-Based Routing enforces routing of outgoing calls through international PSTN gateways if a gateway local to the user’s location cannot be found.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="e8b49-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8b49-113">See Also</span></span>


[<span data-ttu-id="e8b49-114">Planification du routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e8b49-114">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="e8b49-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e8b49-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

