---
title: 'Lync Server 2013 : Sonnerie simultanée'
description: 'Lync Server 2013 : sonnerie simultanée.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Simultaneous ringing
ms:assetid: df02f919-4d50-4832-9300-6c51f8b4fc56
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994079(v=OCS.15)
ms:contentKeyID: 51803990
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 595c8c1d4ce105e2189002f18733ffae92cff8bf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423819"
---
# <a name="simultaneous-ringing-in-lync-server-2013"></a><span data-ttu-id="2afeb-103">Sonnerie simultanée dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2afeb-103">Simultaneous ringing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2afeb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2afeb-104">

<span> </span></span></span>

<span data-ttu-id="2afeb-105">_**Dernière modification de la rubrique :** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="2afeb-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="2afeb-106">Lorsque la partie appelée dispose d’une sonnerie simultanée activée, Location-Based le routage analyse l’emplacement de la partie appelante et les points de terminaison des parties appelées pour déterminer si l’appel doit être routé.</span><span class="sxs-lookup"><span data-stu-id="2afeb-106">When the called party has simultaneous ringing enabled, Location-Based Routing analyzes the location of the calling party and the endpoints of the called parties to determine whether the call should be routed.</span></span>

<span data-ttu-id="2afeb-107">Le tableau ci-dessous illustre un utilisateur pour lequel la sonnerie simultanée est configurée. La cible de la sonnerie simultanée est un utilisateur appartenant au même site réseau, à un autre site réseau ou à un site réseau inconnu.</span><span class="sxs-lookup"><span data-stu-id="2afeb-107">The following table illustrates a user configured with simultaneous ringing, and the simultaneous ringing target is a user in the same network site, in a different network site, or in an unknown network site.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2afeb-108">Appel RTC entrant pour</span><span class="sxs-lookup"><span data-stu-id="2afeb-108">Incoming PSTN call for</span></span></th>
<th><span data-ttu-id="2afeb-109">Situé dans le même site réseau que l’appelé</span><span class="sxs-lookup"><span data-stu-id="2afeb-109">Located in the same network site as callee</span></span></th>
<th><span data-ttu-id="2afeb-110">Situé dans un autre site réseau que l’appelé</span><span class="sxs-lookup"><span data-stu-id="2afeb-110">Located in different network site than callee</span></span></th>
<th><span data-ttu-id="2afeb-111">Se trouve sur un site réseau inconnu ou n’est pas activé pour le routage Location-Based</span><span class="sxs-lookup"><span data-stu-id="2afeb-111">Located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2afeb-112">Utilisateur Lync</span><span class="sxs-lookup"><span data-stu-id="2afeb-112">Lync user</span></span></p></td>
<td><p><span data-ttu-id="2afeb-113">Sonnerie simultanée autorisée</span><span class="sxs-lookup"><span data-stu-id="2afeb-113">Simultaneous ring allowed</span></span></p></td>
<td><p><span data-ttu-id="2afeb-114">Sonnerie simultanée non autorisée</span><span class="sxs-lookup"><span data-stu-id="2afeb-114">Simultaneous ring not allowed</span></span></p></td>
<td><p><span data-ttu-id="2afeb-115">Sonnerie simultanée non autorisée</span><span class="sxs-lookup"><span data-stu-id="2afeb-115">Simultaneous ring not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="2afeb-116">Le tableau suivant illustre un appel d’un utilisateur Lync (par exemple, appelant Lync) au sein d’un même site réseau, sur un autre site réseau ou à partir d’un site réseau inconnu.</span><span class="sxs-lookup"><span data-stu-id="2afeb-116">The following table illustrates a call from a Lync user (i.e. Lync caller) in the same network site, in a different network site, or from an unknown network site.</span></span> <span data-ttu-id="2afeb-117">L’appelé a un point de terminaison RTC (téléphone portable) configuré comme cible de la sonnerie simultanée.</span><span class="sxs-lookup"><span data-stu-id="2afeb-117">The callee has a PSTN endpoint (i.e. cellphone) configured as a simultaneous ring target.</span></span> <span data-ttu-id="2afeb-118">Dans ce scénario, Location-Based le routage détermine si l’appel doit être acheminé vers la cible en anneau simultanée (par exemple, téléphone mobile) de l’appelé ou non.</span><span class="sxs-lookup"><span data-stu-id="2afeb-118">In this scenario, Location-Based Routing will determine whether the call should be routed to the simultaneous ring target (i.e. cellphone) of the callee or not.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2afeb-119">Cible de la sonnerie simultanée</span><span class="sxs-lookup"><span data-stu-id="2afeb-119">Simultaneous ring target</span></span></th>
<th><span data-ttu-id="2afeb-120">Situé dans le même site réseau que l’appelé</span><span class="sxs-lookup"><span data-stu-id="2afeb-120">Located in the same network site as callee</span></span></th>
<th><span data-ttu-id="2afeb-121">Situé dans un autre site réseau que l’appelé</span><span class="sxs-lookup"><span data-stu-id="2afeb-121">Located in different network site than callee</span></span></th>
<th><span data-ttu-id="2afeb-122">Se trouve sur un site réseau inconnu ou n’est pas activé pour le routage Location-Based</span><span class="sxs-lookup"><span data-stu-id="2afeb-122">Located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2afeb-123">Point de terminaison RTC</span><span class="sxs-lookup"><span data-stu-id="2afeb-123">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="2afeb-124">Sonnerie simultanée autorisée via la stratégie de routage des communications vocales du site de l’appelant</span><span class="sxs-lookup"><span data-stu-id="2afeb-124">Simultaneous ring allowed through the caller’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="2afeb-125">Sonnerie simultanée autorisée via la stratégie de routage des communications vocales du site de l’appelant</span><span class="sxs-lookup"><span data-stu-id="2afeb-125">Simultaneous ring allowed through the caller’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="2afeb-126">Sonnerie simultanée autorisée via la stratégie de voix de l’appelant vers les jonctions sur lesquelles le routage géodépendant n’est pas activé</span><span class="sxs-lookup"><span data-stu-id="2afeb-126">Simultaneous ring allowed through the caller’s voice policy to trunks not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="2afeb-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2afeb-127">See Also</span></span>


[<span data-ttu-id="2afeb-128">Scénarios de routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2afeb-128">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="2afeb-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2afeb-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

