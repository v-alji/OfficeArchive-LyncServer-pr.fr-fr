---
title: 'Lync Server 2013 : Délégation'
description: 'Lync Server 2013 : délégation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delegation
ms:assetid: 89e76e5c-3cfb-4504-8d0d-7509c8ba9815
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994045(v=OCS.15)
ms:contentKeyID: 51803956
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6dc25d0ea3dfd64ee1b71677e6bac55c1cb1ca32
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430741"
---
# <a name="delegation-in-lync-server-2013"></a><span data-ttu-id="dd10f-103">Délégation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dd10f-103">Delegation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dd10f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dd10f-104">

<span> </span></span></span>

<span data-ttu-id="dd10f-105">_**Dernière modification de la rubrique :** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="dd10f-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="dd10f-106">Les fonctionnalités de délégation de Lync sont affectées par le routage Location-Based de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="dd10f-106">The delegation capabilities in Lync are affected by Location-Based Routing in the following manner:</span></span>

  - <span data-ttu-id="dd10f-107">Lorsqu’un délégué activé pour le routage de Location-Based place un appel au nom d’un responsable, la stratégie vocale du délégué est utilisée pour autoriser l’appel et la stratégie de routage de la voix du site du délégué sera utilisée pour diriger l’appel.</span><span class="sxs-lookup"><span data-stu-id="dd10f-107">When a delegate enabled for Location-Based Routing places a call on behalf of a manager, the delegate’s voice policy is used to authorize the call and the delegate’s site voice routing policy will be used to route the call</span></span>

  - <span data-ttu-id="dd10f-108">Pour les appels RTC passés à un responsable, les règles applicables au transfert d’appel ou à la sonnerie simultanée sont utilisées, comme décrit dans les rubriques « Transfert et renvoi des appels » et « Sonnerie simultanée ».</span><span class="sxs-lookup"><span data-stu-id="dd10f-108">For incoming PSTN calls to a manager, the same rules applicable for call forwarding or simultaneously ringing will apply as described in the Call transfers and forwarding and Simultaneous ringing topics.</span></span>

  - <span data-ttu-id="dd10f-109">Si un délégué définit un point de terminaison RTC comme cible de sonnerie simultanée, pour un appel entrant passé à un responsable, la stratégie de routage des communications vocales du site associé à la jonction entrante est utilisée pour acheminer l‘appel vers le point de terminaison RTC du délégué.</span><span class="sxs-lookup"><span data-stu-id="dd10f-109">When a delegate sets a PSTN endpoint as a simultaneous ring target, for an incoming call to the manager, the voice routing policy of the site that is associated to the incoming trunk will be used to route the call to the delegate’s PSTN endpoint.</span></span>

  - <span data-ttu-id="dd10f-110">Pour la délégation, il est recommandé que le responsable et ses délégués soient situés dans le même site réseau.</span><span class="sxs-lookup"><span data-stu-id="dd10f-110">For delegation, it’s recommended that the manager and his associated delegates to be usually located in the same network site.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="dd10f-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd10f-111">See Also</span></span>


[<span data-ttu-id="dd10f-112">Scénarios de routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dd10f-112">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="dd10f-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dd10f-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

