---
title: 'Lync Server 2013 : Routage interjonctions'
description: 'Lync Server 2013 : routage intertrunk.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Intertrunk routing
ms:assetid: d3a33b4a-8bf4-4a8c-a371-8ef79e740780
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205272(v=OCS.15)
ms:contentKeyID: 48185442
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 30c838ee94a2df0807195c172d7e2a3a393523af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426769"
---
# <a name="intertrunk-routing-in-lync-server-2013"></a><span data-ttu-id="85516-103">Routage interjonctions dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85516-103">Intertrunk routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85516-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85516-104">

<span> </span></span></span>

<span data-ttu-id="85516-105">_**Dernière modification de la rubrique :** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="85516-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="85516-106">Lync Server 2013 peut interconnecter un PBX IP à une passerelle RTC (réseau téléphonique commuté) pour que les appels d’un téléphone PBX puissent être routés vers le RTC et que les appels RTC entrants puissent être routés vers un téléphone PBX (Private Branch Exchange).</span><span class="sxs-lookup"><span data-stu-id="85516-106">Lync Server 2013 can interconnect an IP-PBX to a public switched telephone network (PSTN) gateway so that calls from a PBX phone can be routed to the PSTN, and incoming PSTN calls can be routed to a private branch exchange (PBX) phone.</span></span> <span data-ttu-id="85516-107">De la même façon, Lync Server 2013 peut interconnecter au moins deux systèmes IP-PBX pour que les appels puissent être placés et reçus entre les téléphones PBX des différents systèmes IP PBX.</span><span class="sxs-lookup"><span data-stu-id="85516-107">Similarly, Lync Server 2013 can interconnect two or more IP-PBX systems so that calls can be placed and received between PBX phones from the different IP-PBX systems.</span></span>

<span data-ttu-id="85516-108">Cette fonctionnalité de routage intertrunk peut être configurée à l’aide de la cmdlet Lync Server Management Shell, **Set-CsTrunkConfiguration**, avec le nouveau paramètre PstnUsages.</span><span class="sxs-lookup"><span data-stu-id="85516-108">This intertrunk routing feature can be configured by using the Lync Server Management Shell cmdlet, **Set-CsTrunkConfiguration**, with the new parameter, PstnUsages.</span></span> <span data-ttu-id="85516-109">Ce paramètre spécifie l’ensemble d’enregistrements d’utilisation RTC à utiliser.</span><span class="sxs-lookup"><span data-stu-id="85516-109">This parameter specifies the set of PSTN usage records to use.</span></span> <span data-ttu-id="85516-110">Un Trunk utilise cette utilisation PSTN pour déterminer un itinéraire et acheminer tous les appels entrants en conséquence.</span><span class="sxs-lookup"><span data-stu-id="85516-110">A trunk uses this PSTN usage to determine a route and to route all incoming calls accordingly.</span></span>

    Set-CsTrunkConfiguration -Identity <TrunkId> -PstnUsages @{add="<UsageString>"}

<span data-ttu-id="85516-111">Le diagramme suivant illustre Lync Server 2013 permettant une interconnexion entre une passerelle RTC et un PBX IP.</span><span class="sxs-lookup"><span data-stu-id="85516-111">The following diagram illustrates Lync Server 2013 providing interconnectivity between a PSTN gateway and an IP-PBX.</span></span>

<span data-ttu-id="85516-112">**Routage intertrunk entre passerelle et PBX IP**</span><span class="sxs-lookup"><span data-stu-id="85516-112">**Intertrunk routing between gateway and IP PBX**</span></span>

<span data-ttu-id="85516-113">![Diagramme IP-PBX/Passerelle RTC connectant Lync Server](images/JJ721940.cc3858ca-2ee3-4d51-8a51-db078366b50b(OCS.15).jpg "Diagramme IP-PBX/Passerelle RTC connectant Lync Server")</span><span class="sxs-lookup"><span data-stu-id="85516-113">![Lync Server connecting PSTN gateway/IP-PBX diagram](images/JJ721940.cc3858ca-2ee3-4d51-8a51-db078366b50b(OCS.15).jpg "Lync Server connecting PSTN gateway/IP-PBX diagram")</span></span>

<span data-ttu-id="85516-114">Le diagramme suivant illustre Lync Server 2013 qui interconnecte deux systèmes PBX IP.</span><span class="sxs-lookup"><span data-stu-id="85516-114">The following diagram illustrates Lync Server 2013 interconnecting two IP-PBX systems.</span></span>

<span data-ttu-id="85516-115">**Routage intertrunk entre deux PBX IP**</span><span class="sxs-lookup"><span data-stu-id="85516-115">**Intertrunk routing between two IP PBXs**</span></span>

<span data-ttu-id="85516-116">![Diagramme IP-PBX/Passerelle RTC interconnectant Lync Server](images/JJ721940.6ba18ec9-df70-498a-9cf7-7fc41e5ec432(OCS.15).jpg "Diagramme IP-PBX/Passerelle RTC interconnectant Lync Server")</span><span class="sxs-lookup"><span data-stu-id="85516-116">![Lync Server interconnecting IP-PAX systems diagram](images/JJ721940.6ba18ec9-df70-498a-9cf7-7fc41e5ec432(OCS.15).jpg "Lync Server interconnecting IP-PAX systems diagram")</span></span>

<span data-ttu-id="85516-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85516-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

