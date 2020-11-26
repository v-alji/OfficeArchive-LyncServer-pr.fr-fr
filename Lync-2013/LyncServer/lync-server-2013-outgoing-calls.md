---
title: 'Lync Server 2013 : Appels sortants'
description: 'Lync Server 2013 : appels sortants.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Outgoing calls
ms:assetid: 885ffe6f-cd51-4f21-8d4f-a1ff8d818858
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994049(v=OCS.15)
ms:contentKeyID: 51803960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e14f19dec35a6da47a2ddd62657d5d087a854f16
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424834"
---
# <a name="outgoing-calls-in-lync-server-2013"></a><span data-ttu-id="105a7-103">Appels sortants dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="105a7-103">Outgoing calls in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="105a7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="105a7-104">

<span> </span></span></span>

<span data-ttu-id="105a7-105">_**Dernière modification de la rubrique :** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="105a7-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="105a7-106">Le routage des appels sortants d’utilisateurs activés pour le routage Location-Based est affecté par l’emplacement réseau du point de terminaison de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="105a7-106">The routing of outbound calls of users enabled for Location-Based Routing is affected by the network location of the user’s endpoint.</span></span> <span data-ttu-id="105a7-107">Le tableau suivant illustre la façon dont Location-Based routage affecte le routage des appels sortants en fonction de l’emplacement du point de terminaison de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="105a7-107">The following table illustrates how Location-Based Routing affects the routing of outbound calls depending on the location of the caller’s endpoint.</span></span>

### <a name="caller-placing-an-outbound-call-to-the-pstn"></a><span data-ttu-id="105a7-108">Appelant passant un appel sortant vers le réseau téléphonique commuté (RTC)</span><span class="sxs-lookup"><span data-stu-id="105a7-108">Caller placing an outbound call to the PSTN</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="105a7-109">Point de terminaison d’un utilisateur situé dans un site réseau pour lequel le routage géodépendant est activé</span><span class="sxs-lookup"><span data-stu-id="105a7-109">User endpoint located in a network site enabled for Location-Based Routing</span></span></th>
<th><span data-ttu-id="105a7-110">Point de terminaison de l’utilisateur situé dans un site réseau inconnu ou pour lequel le routage géodépendant n’est pas activé</span><span class="sxs-lookup"><span data-stu-id="105a7-110">User endpoint located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="105a7-111">Autorisation des appels sortants</span><span class="sxs-lookup"><span data-stu-id="105a7-111">Authorization of outbound calls</span></span></p></td>
<td><p><span data-ttu-id="105a7-112">L’appel est autorisé sur la base de la stratégie de voix de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="105a7-112">Call is authorized based on user’s voice policy</span></span></p></td>
<td><p><span data-ttu-id="105a7-113">L’appel est autorisé sur la base de la stratégie de voix de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="105a7-113">Call is authorized based on user’s voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="105a7-114">Routage de l’appel sortant</span><span class="sxs-lookup"><span data-stu-id="105a7-114">Routing of outbound call</span></span></p></td>
<td><p><span data-ttu-id="105a7-115">L’appel est routé selon le stratégie de routage des communications vocales du site réseau</span><span class="sxs-lookup"><span data-stu-id="105a7-115">Call is routed according to the network site’s voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="105a7-116">L’appel est routé selon la stratégie de voix de l’utilisateur en utilisant uniquement des jonctions pour lesquelles le routage géodépendant n’est pas activé (si celui-ci est disponible)</span><span class="sxs-lookup"><span data-stu-id="105a7-116">Call is routed according to user’s voice policy and only through trunks not enabled for Location-Based Routing (if available)</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="105a7-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="105a7-117">See Also</span></span>


[<span data-ttu-id="105a7-118">Scénarios de routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="105a7-118">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="105a7-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="105a7-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

