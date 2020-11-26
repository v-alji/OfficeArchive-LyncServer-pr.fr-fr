---
title: 'Lync Server 2013 : Appels entrants'
description: 'Lync Server 2013 : appels entrants.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Incoming calls
ms:assetid: 65b9c1b4-6af7-4527-8c33-22c4442bd209
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994038(v=OCS.15)
ms:contentKeyID: 51803948
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a72c7fc378240f9751eae8e6c24e9cc601b08d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427298"
---
# <a name="incoming-calls-in-lync-server-2013"></a><span data-ttu-id="76890-103">Appels entrants dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="76890-103">Incoming calls in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="76890-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="76890-104">

<span> </span></span></span>

<span data-ttu-id="76890-105">_**Dernière modification de la rubrique :** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="76890-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="76890-106">Le routage des appels entrants vers les utilisateurs activés pour le routage Location-Based dépend de l’emplacement du point de terminaison de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="76890-106">The routing of incoming calls to users enabled for Location-Based Routing depends on the location of the user’s endpoint.</span></span> <span data-ttu-id="76890-107">Le routage des appels entrants est affecté comme suit.</span><span class="sxs-lookup"><span data-stu-id="76890-107">The routing of incoming calls is affected in the following way.</span></span> <span data-ttu-id="76890-108">Si un utilisateur a un appel entrant vers un point de terminaison situé dans un site réseau de routage de Location-Based et que le point de terminaison se trouve sur le même site réseau que la passerelle RTC, l’appel est routé.</span><span class="sxs-lookup"><span data-stu-id="76890-108">If a user has an incoming call to an endpoint located in a Location-Based Routing enabled network site, and the endpoint is located in the same network site as the PSTN gateway, the call will be routed.</span></span> <span data-ttu-id="76890-109">Si un utilisateur dispose d’un appel entrant vers un point de terminaison situé dans un site réseau Location-Based de routage activé et que le point de terminaison se trouve dans un autre site réseau que la passerelle RTC, l’appel n’est pas acheminé.</span><span class="sxs-lookup"><span data-stu-id="76890-109">If a user has an incoming call to an endpoint located in a Location-Based Routing enabled network site, and the endpoint is located in a different network site than the PSTN gateway, the call will not be routed.</span></span> <span data-ttu-id="76890-110">Lorsqu’un utilisateur n’a pas de points de terminaison situés dans le même site réseau que la passerelle RTC à partir de laquelle l’appel entrant provient, l’appel entrant est acheminé directement vers la messagerie vocale de l’utilisateur et une notification d’appel manqué est envoyée à la personne appelée.</span><span class="sxs-lookup"><span data-stu-id="76890-110">When a user has no endpoints located in the same network site as the PSTN gateway where the incoming call is originating from, the incoming call will be routed directly to the user’s voicemail and a missed call notification will be sent to the called party.</span></span>

<span data-ttu-id="76890-111">Les paramètres de transfert d’appel d’un utilisateur qui est activé pour Location-Based le routage continuent d’être appliqués, toutefois, les appels transférés sont soumis à des restrictions de routage Location-Based de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="76890-111">The call forwarding settings of a user that is enabled for Location-Based Routing will continue to be enforced, however, calls forwarded will be subject to Location-Based Routing restrictions of the user.</span></span>

<span data-ttu-id="76890-112">Le tableau suivant illustre la façon dont Location-Based routage affecte le routage des appels entrants en fonction de l’emplacement du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="76890-112">The following table illustrates how Location-Based Routing affects the routing of inbound calls depending on the location of the callee’s endpoint.</span></span> <span data-ttu-id="76890-113">Le site réseau de la passerelle RTC est activé pour le routage Location-Based, et Location-Based le routage autorise uniquement le routage des appels RTC vers les points de terminaison au sein du même site réseau.</span><span class="sxs-lookup"><span data-stu-id="76890-113">The network site of the PSTN gateway is enabled for Location-Based Routing, and Location-Based Routing only permits routing of PSTN calls to endpoints within the same network site.</span></span>

### <a name="callee-receiving-an-inbound-call-from-the-pstn"></a><span data-ttu-id="76890-114">Appelé recevant un appel entrant à partir de la passerelle RTC</span><span class="sxs-lookup"><span data-stu-id="76890-114">Callee receiving an inbound call from the PSTN</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="76890-115">Point de terminaison de l’appelé situé dans le même site réseau que la passerelle RTC</span><span class="sxs-lookup"><span data-stu-id="76890-115">Callee’s endpoint located in the same network site as PSTN gateway</span></span></th>
<th><span data-ttu-id="76890-116">Point de terminaison de l’appelé non situé dans le même site réseau que la passerelle RTC</span><span class="sxs-lookup"><span data-stu-id="76890-116">Callee’s endpoint not located in the same network site as PSTN gateway</span></span></th>
<th><span data-ttu-id="76890-117">Point de terminaison de l’appelé situé dans un site réseau inconnu ou pour lequel le routage géodépendant n’est pas activé</span><span class="sxs-lookup"><span data-stu-id="76890-117">Callee’s endpoint located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76890-118">Routage de l’appel RTC entrant</span><span class="sxs-lookup"><span data-stu-id="76890-118">Routing of inbound PSTN call</span></span></p></td>
<td><p><span data-ttu-id="76890-119">L’appel entrant est routé vers les points de terminaison de l’appelé</span><span class="sxs-lookup"><span data-stu-id="76890-119">Incoming call is routed to callee’s endpoints</span></span></p></td>
<td><p><span data-ttu-id="76890-120">L’appel entrant n‘est pas routé vers les points de terminaison de l’appelé</span><span class="sxs-lookup"><span data-stu-id="76890-120">Incoming call is not routed to callee’s endpoints</span></span></p></td>
<td><p><span data-ttu-id="76890-121">L’appel entrant n‘est pas routé vers les points de terminaison de l’appelé</span><span class="sxs-lookup"><span data-stu-id="76890-121">Incoming call is not routed to callee’s endpoints</span></span></p></td>
</tr>
</tbody>
</table>

  

<div>

## <a name="see-also"></a><span data-ttu-id="76890-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76890-122">See Also</span></span>


[<span data-ttu-id="76890-123">Scénarios de routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="76890-123">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="76890-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="76890-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

