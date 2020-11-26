---
title: 'Lync Server 2013 : Fonctionnalités non prises en charge par le routage géodépendant'
description: 'Lync Server 2013 : les fonctionnalités ne sont pas prises en charge par le routage Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capabilities not supported by Location-Based Routing
ms:assetid: c3d54953-a7d6-4465-a6c3-ae411b2d8ea9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994071(v=OCS.15)
ms:contentKeyID: 51803982
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf9cd03a8cbdd50e136605c4f172598b2ad3f523
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435606"
---
# <a name="capabilities-not-supported-by-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="92367-103">Fonctionnalités non prises en charge par le routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="92367-103">Capabilities not supported by Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="92367-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="92367-104">

<span> </span></span></span>

<span data-ttu-id="92367-105">_**Dernière modification de la rubrique :** 2014-03-12_</span><span class="sxs-lookup"><span data-stu-id="92367-105">_**Topic Last Modified:** 2014-03-12_</span></span>

<span data-ttu-id="92367-106">Location-Based le routage n’est pas applicable aux types d’interactions suivants.</span><span class="sxs-lookup"><span data-stu-id="92367-106">Location-Based Routing does not apply to the following types of interactions.</span></span> <span data-ttu-id="92367-107">Location-Based le routage n’est pas appliqué lorsque les points de terminaison Lync interagissent avec les points de terminaison RTC grâce à ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="92367-107">Location-Based Routing is not enforced when Lync endpoints interact with PSTN endpoints using these capabilities.</span></span>

  - <span data-ttu-id="92367-108">Appels RTC entrants pour les conférences</span><span class="sxs-lookup"><span data-stu-id="92367-108">PSTN dial-in to conferences</span></span>

  - <span data-ttu-id="92367-109">Appels RTC entrants et sortants via le groupe de réponse</span><span class="sxs-lookup"><span data-stu-id="92367-109">Incoming and outgoing PSTN calls through Response Group</span></span>

  - <span data-ttu-id="92367-110">Parcage d’appel ou récupération des appels via le parcage d’appels</span><span class="sxs-lookup"><span data-stu-id="92367-110">Call park or retrieval of PSTN calls through Call Park</span></span>

  - <span data-ttu-id="92367-111">Appels RTC entrants pour le service d’annonce</span><span class="sxs-lookup"><span data-stu-id="92367-111">Incoming PSTN calls to Announcement Service</span></span>

  - <span data-ttu-id="92367-112">Appels RTC entrants récupérés via la prise d’appel de groupe</span><span class="sxs-lookup"><span data-stu-id="92367-112">Incoming PSTN calls retrieved via Group Call Pickup</span></span>

<span data-ttu-id="92367-113">Pour appliquer les règles de routage de Location-Based aux types d’interactions dans la liste suivante, vous devez activer le routage Location-Based pour les conférences :</span><span class="sxs-lookup"><span data-stu-id="92367-113">To enforce Location-Based Routing rules to the types of interactions in the following list, you must enable Location-Based Routing for Conferencing:</span></span>

  - <span data-ttu-id="92367-114">Appels RTC sortants à partir des conférences</span><span class="sxs-lookup"><span data-stu-id="92367-114">PSTN dial-out from conferences</span></span>

  - <span data-ttu-id="92367-115">Escalades à partir de conversations audio d’P2P vers des conférences impliquant des points de terminaison RTC</span><span class="sxs-lookup"><span data-stu-id="92367-115">Escalations from peer-to-peer audio conversations to conferencing involving PSTN endpoints</span></span>

  - <span data-ttu-id="92367-116">Transferts consultatifs impliquant les points de terminaison RTC</span><span class="sxs-lookup"><span data-stu-id="92367-116">Consultative transfers involving PSTN endpoints</span></span>

<span data-ttu-id="92367-117">Pour activer Location-Based le routage des conférences, voir [routage basé sur l’emplacement pour les conférences dans Lync Server 2013](lync-server-2013-location-based-routing-for-conferencing.md).</span><span class="sxs-lookup"><span data-stu-id="92367-117">To enable Location-Based Routing for Conferencing, see [Location-Based Routing for conferencing in Lync Server 2013](lync-server-2013-location-based-routing-for-conferencing.md).</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="92367-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92367-118">See Also</span></span>


[<span data-ttu-id="92367-119">Planification du routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="92367-119">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="92367-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="92367-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

