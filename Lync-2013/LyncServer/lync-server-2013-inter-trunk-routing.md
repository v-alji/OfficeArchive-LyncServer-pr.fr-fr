---
title: 'Lync Server 2013 : routage inter-Trunk'
description: 'Lync Server 2013 : routage inter-Trunk.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Inter-trunk routing
ms:assetid: f687a548-1f2e-48ed-9745-a13dc1f3698f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721940(v=OCS.15)
ms:contentKeyID: 49733877
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7e023956f28183423c04e94948acdec0df2c1284
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426864"
---
# <a name="inter-trunk-routing-in-lync-server-2013"></a><span data-ttu-id="e8bb4-103">Routage inter-Trunk dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e8bb4-103">Inter-trunk routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e8bb4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e8bb4-104">

<span> </span></span></span>

<span data-ttu-id="e8bb4-105">_**Dernière modification de la rubrique :** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="e8bb4-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="e8bb4-106">Lync Server 2013 fournit une gestion de session de base grâce à la prise en charge du routage intertrunk.</span><span class="sxs-lookup"><span data-stu-id="e8bb4-106">Lync Server 2013 provides basic session management through the support of intertrunk routing.</span></span> <span data-ttu-id="e8bb4-107">Cette nouvelle fonctionnalité permet à Lync Server de fournir des fonctionnalités de contrôle d’appel aux systèmes de téléphonie en aval.</span><span class="sxs-lookup"><span data-stu-id="e8bb4-107">This new capability enables Lync Server to provide call control functionalities to downstream telephony systems.</span></span> <span data-ttu-id="e8bb4-108">Le routage entre les jonctions peut interconnecter un IP-PBX à une passerelle de réseau de téléphonique commuté (PSTN) pour que les appels d’un téléphone PBX (autocommutateur privé) puissent être acheminés vers la passerelle PSTN et que les appels PSTN entrants puissent être acheminés vers un téléphone PBX.</span><span class="sxs-lookup"><span data-stu-id="e8bb4-108">Intertrunk routing can interconnect an IP-PBX to a public switched telephone network (PSTN) gateway so that calls from a private branch exchange (PBX) phone can be routed to the PSTN, and incoming PSTN calls can be routed to a PBX phone.</span></span> <span data-ttu-id="e8bb4-109">De la même façon, Lync Server peut interconnecter au moins deux systèmes IP-PBX pour que les appels puissent être placés et reçus entre les téléphones PBX des différents systèmes IP PBX.</span><span class="sxs-lookup"><span data-stu-id="e8bb4-109">Similarly, Lync Server can interconnect two or more IP-PBX systems so that calls can be placed and received between PBX phones from the different IP-PBX systems.</span></span>

<span data-ttu-id="e8bb4-110">La figure suivante illustre Lync Server 2013 permettant une interconnexion entre une passerelle RTC et un PBX IP.</span><span class="sxs-lookup"><span data-stu-id="e8bb4-110">The following figure illustrates Lync Server 2013 providing interconnectivity between a PSTN gateway and an IP-PBX.</span></span>

<span data-ttu-id="e8bb4-111">![Diagramme IP-PBX/Passerelle RTC connectant Lync Server](images/JJ721940.cc3858ca-2ee3-4d51-8a51-db078366b50b(OCS.15).jpg "Diagramme IP-PBX/Passerelle RTC connectant Lync Server")</span><span class="sxs-lookup"><span data-stu-id="e8bb4-111">![Lync Server connecting PSTN gateway/IP-PBX diagram](images/JJ721940.cc3858ca-2ee3-4d51-8a51-db078366b50b(OCS.15).jpg "Lync Server connecting PSTN gateway/IP-PBX diagram")</span></span>

<span data-ttu-id="e8bb4-112">La figure suivante illustre Lync Server 2013 connectant deux systèmes PBX IP.</span><span class="sxs-lookup"><span data-stu-id="e8bb4-112">The next figure illustrates Lync Server 2013 connecting two IP-PBX systems.</span></span>

<span data-ttu-id="e8bb4-113">![Diagramme IP-PBX/Passerelle RTC interconnectant Lync Server](images/JJ721940.6ba18ec9-df70-498a-9cf7-7fc41e5ec432(OCS.15).jpg "Diagramme IP-PBX/Passerelle RTC interconnectant Lync Server")</span><span class="sxs-lookup"><span data-stu-id="e8bb4-113">![Lync Server interconnecting IP-PAX systems diagram](images/JJ721940.6ba18ec9-df70-498a-9cf7-7fc41e5ec432(OCS.15).jpg "Lync Server interconnecting IP-PAX systems diagram")</span></span>

<span data-ttu-id="e8bb4-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e8bb4-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

