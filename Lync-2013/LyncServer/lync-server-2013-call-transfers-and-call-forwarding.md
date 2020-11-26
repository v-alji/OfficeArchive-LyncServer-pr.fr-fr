---
title: 'Lync Server 2013 : Transferts et renvois d’appels'
description: 'Lync Server 2013 : transfert d’appel et transfert d’appel.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call transfers and call forwarding
ms:assetid: 978610ec-63c7-4cf6-ad7a-9ef91559bf12
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994051(v=OCS.15)
ms:contentKeyID: 51803962
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9359cb64b386d022eab33e4523dfaccf784075b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435683"
---
# <a name="call-transfers-and-call-forwarding-in-lync-server-2013"></a><span data-ttu-id="226ca-103">Transferts et renvois d’appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="226ca-103">Call transfers and call forwarding in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="226ca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="226ca-104">

<span> </span></span></span>

<span data-ttu-id="226ca-105">_**Dernière modification de la rubrique :** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="226ca-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="226ca-106">Lorsqu’un point de terminaison PSTN est impliqué, Location-Based le routage analyse l’emplacement du point de terminaison de 134 et le point de terminaison de transfert ou de transfert de l’appel vers (c.-à-d. transférer/transférer la cible).</span><span class="sxs-lookup"><span data-stu-id="226ca-106">When a PSTN endpoint is involved, Location-Based Routing analyzes the location of the calle’s endpoint and the endpoint where the call will be transferred or forwarded to (i.e. transfer/forward target).</span></span> <span data-ttu-id="226ca-107">Location-Based le routage détermine si l’appel doit être transféré ou transféré en fonction de l’emplacement des deux points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="226ca-107">Location-Based Routing determines whether the call should be transferred or forwarded depending on the location of both endpoints.</span></span>

<span data-ttu-id="226ca-108">Le tableau suivant illustre le scénario d’un utilisateur Lync dans un appel avec un point de terminaison PSTN et l’utilisateur de Lync transfère l’appel vers un autre utilisateur Lync.</span><span class="sxs-lookup"><span data-stu-id="226ca-108">The following table illustrates the scenario of a Lync user in a call with a PSTN endpoint, and the Lync user transfers the call to another Lync user.</span></span> <span data-ttu-id="226ca-109">En fonction de l’emplacement du site du réseau du point de terminaison du destinataire, Location-Based le routage affecte le routage du transfert ou du transfert d’appel.</span><span class="sxs-lookup"><span data-stu-id="226ca-109">Depending on the network site location of the transferee’s endpoint, Location-Based Routing affects the routing of the call transfer or forward.</span></span>

### <a name="initiating-call-transfer-or-forward"></a><span data-ttu-id="226ca-110">Lancement du transfert ou du renvoi d’appel</span><span class="sxs-lookup"><span data-stu-id="226ca-110">Initiating call transfer or forward</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="226ca-111">Utilisateur à l’origine du transfert/renvoi d’appel</span><span class="sxs-lookup"><span data-stu-id="226ca-111">User initiating the call transfer/forward</span></span></th>
<th><span data-ttu-id="226ca-112">Point de terminaison cible dans le même site réseau que l’utilisateur à l’origine du transfert ou du renvoi d’appel</span><span class="sxs-lookup"><span data-stu-id="226ca-112">Target endpoint is in same network site as user initiating call transfer or forward</span></span></th>
<th><span data-ttu-id="226ca-113">Point de terminaison cible dans un autre site réseau que l’utilisateur à l’origine du transfert ou du renvoi d’appel</span><span class="sxs-lookup"><span data-stu-id="226ca-113">Target endpoint is in different network site as user initiating call transfer or forward</span></span></th>
<th><span data-ttu-id="226ca-114">Le point de terminaison cible est dans un site réseau inconnu ou un site réseau non activé pour le routage de Location-Based</span><span class="sxs-lookup"><span data-stu-id="226ca-114">Target endpoint is in unknown network site or network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="226ca-115">Utilisateur Lync</span><span class="sxs-lookup"><span data-stu-id="226ca-115">Lync user</span></span></p></td>
<td><p><span data-ttu-id="226ca-116">Le transfert ou renvoi de l’appel est autorisé</span><span class="sxs-lookup"><span data-stu-id="226ca-116">Call forward or transfer is allowed</span></span></p></td>
<td><p><span data-ttu-id="226ca-117">Le transfert ou renvoi de l’appel n’est pas autorisé</span><span class="sxs-lookup"><span data-stu-id="226ca-117">Call forward or transfer is not allowed</span></span></p></td>
<td><p><span data-ttu-id="226ca-118">Le transfert ou renvoi de l’appel n’est pas autorisé</span><span class="sxs-lookup"><span data-stu-id="226ca-118">Call forward or transfer is not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  

<span data-ttu-id="226ca-119">Par exemple, un utilisateur Lync dans un appel avec un point de terminaison PSTN transfère l’appel vers un autre utilisateur Lync qui se trouve sur le même site réseau.</span><span class="sxs-lookup"><span data-stu-id="226ca-119">For example: a Lync user in a call with a PSTN endpoint transfers the call to another Lync user that is in the same network site.</span></span> <span data-ttu-id="226ca-120">Dans ce cas, le transfert de l’appel est autorisé.</span><span class="sxs-lookup"><span data-stu-id="226ca-120">In this case, the call transfer is allowed.</span></span>

<span data-ttu-id="226ca-121">Le tableau suivant illustre le scénario d’un utilisateur Lync dans un appel d’un autre utilisateur Lync et l’un d’entre eux transfère l’appel à un point de terminaison PSTN.</span><span class="sxs-lookup"><span data-stu-id="226ca-121">The following table illustrates the scenario of a Lync user in a call with another Lync user, and one of the users transfers the call to a PSTN endpoint.</span></span> <span data-ttu-id="226ca-122">En fonction de l’emplacement de l’utilisateur sur lequel l’appel est transféré, le tableau décrit la façon dont Location-Based le routage affecte l’appel.</span><span class="sxs-lookup"><span data-stu-id="226ca-122">Depending on the location of the user the call is being transferred to, the table details how Location-Based Routing affects the call.</span></span>

### <a name="call-transfer-or-forward-to-pstn-endpoint"></a><span data-ttu-id="226ca-123">Transfert ou renvoi de l’appel vers le point de terminaison RTC</span><span class="sxs-lookup"><span data-stu-id="226ca-123">Call transfer or forward to PSTN endpoint</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="226ca-124">Point de terminaison cible du transfert/renvoi de l’appel</span><span class="sxs-lookup"><span data-stu-id="226ca-124">Call transfer/forward endpoint target</span></span></th>
<th><span data-ttu-id="226ca-125">Utilisateurs de Lync sur le même site réseau</span><span class="sxs-lookup"><span data-stu-id="226ca-125">Lync users in same network site</span></span></th>
<th><span data-ttu-id="226ca-126">Utilisateurs de Lync dans différents sites réseau</span><span class="sxs-lookup"><span data-stu-id="226ca-126">Lync users in different network sites</span></span></th>
<th><span data-ttu-id="226ca-127">L’un ou les deux utilisateurs de Lync sur un site réseau ou un site réseau inconnu n’ont pas été activés pour le routage Location-Based</span><span class="sxs-lookup"><span data-stu-id="226ca-127">One or both Lync users in unknown network site or network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="226ca-128">Point de terminaison RTC</span><span class="sxs-lookup"><span data-stu-id="226ca-128">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="226ca-129">Le transfert ou le renvoi de l’appel est autorisé par la stratégie de routage des communications vocales du site du cessionnaire</span><span class="sxs-lookup"><span data-stu-id="226ca-129">Call forward or transfer allowed by the transferred user’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="226ca-130">Le transfert ou le renvoi de l’appel est autorisé par la stratégie de routage des communications vocales du site du cessionnaire</span><span class="sxs-lookup"><span data-stu-id="226ca-130">Call forward or transfer allowed by the transferred user’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="226ca-131">Le transfert ou le renvoi de l’appel est autorisé par la stratégie de voix du cessionnaire, uniquement via des jonctions pour lesquelles le routage géodépendant n’est pas activé</span><span class="sxs-lookup"><span data-stu-id="226ca-131">Call forward or transfer allowed by the transferred user’s voice policy only through trunks not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="226ca-132">Par exemple, un utilisateur Lync dans un appel avec un autre utilisateur Lync figurant dans le même site réseau transfère l’appel vers un point de terminaison PSTN et le transfert d’appel est autorisé.</span><span class="sxs-lookup"><span data-stu-id="226ca-132">For example: a Lync user in a call with another Lync user that is in the same network site transfers the call to a PSTN endpoint and the call transfer is allowed.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="226ca-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="226ca-133">See Also</span></span>


[<span data-ttu-id="226ca-134">Scénarios de routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="226ca-134">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="226ca-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="226ca-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

