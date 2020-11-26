---
title: 'Lync Server 2013 : Prise en charge du protocole IP et de gestion réseau'
description: 'Lync Server 2013 : prise en charge des protocoles IP et réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IP and networking protocol support
ms:assetid: b0cffb10-3478-445c-89c7-8cb8b5027424
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412848(v=OCS.15)
ms:contentKeyID: 48185128
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dbd8022dd7197524334e0c70ea0ad875a30446de
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426745"
---
# <a name="ip-and-networking-protocol-support-in-lync-server-2013"></a><span data-ttu-id="103d0-103">Prise en charge du protocole IP et de gestion réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="103d0-103">IP and networking protocol support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="103d0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="103d0-104">

<span> </span></span></span>

<span data-ttu-id="103d0-105">_**Dernière modification de la rubrique :** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="103d0-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="103d0-106">Lync Server 2013 prend en charge les protocoles IP et réseau suivants :</span><span class="sxs-lookup"><span data-stu-id="103d0-106">Lync Server 2013 supports the following IP and networking protocols:</span></span>

  - <span data-ttu-id="103d0-107">**Protocoles IP.**</span><span class="sxs-lookup"><span data-stu-id="103d0-107">**IP Protocols.**</span></span>   <span data-ttu-id="103d0-108">Lync Server 2013 prend en charge les protocoles IP version 4 (IPv4) ou IP version 6 (IPv6) pour le réseau du serveur.</span><span class="sxs-lookup"><span data-stu-id="103d0-108">Lync Server 2013 supports either IP version 4 (IPv4) or IP version 6 (IPv6) for the server network.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="103d0-109">Lync Server 2013 peut fonctionner dans un réseau doté d’une pile IP double activée.</span><span class="sxs-lookup"><span data-stu-id="103d0-109">Lync Server 2013 can function in a network with dual IP stack enabled.</span></span>

    
    </div>

  - <span data-ttu-id="103d0-110">**Protocoles de transport SIP.**</span><span class="sxs-lookup"><span data-stu-id="103d0-110">**SIP Transport Protocols.**</span></span>   <span data-ttu-id="103d0-111">De manière générale, le protocole SIP peut utiliser au moins trois types de transport : protocole UDP (User Datagram Protocol), protocole TCP (Transmission Control Protocol) et TLS (Transport Layer Security).</span><span class="sxs-lookup"><span data-stu-id="103d0-111">Generically, SIP can use at least three transport types: User Datagram Protocol (UDP), Transmission Control Protocol (TCP), and Transport Layer Security (TLS).</span></span> <span data-ttu-id="103d0-112">Dans la configuration de transport SIP par défaut, le protocole TLS s’exécute sur TCP.</span><span class="sxs-lookup"><span data-stu-id="103d0-112">In the default SIP transport configuration, TLS runs over TCP.</span></span> <span data-ttu-id="103d0-113">TLS est utilisé au sein du réseau Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="103d0-113">TLS is used within the Lync Server 2013 network.</span></span> <span data-ttu-id="103d0-114">Au bord du réseau, Lync Server 2013 peut interagir via TCP.</span><span class="sxs-lookup"><span data-stu-id="103d0-114">At the edge of the network, Lync Server 2013 can interoperate over TCP.</span></span> <span data-ttu-id="103d0-115">Lync Server 2013 ne prend pas en charge le protocole UDP pour les transports SIP, car il ne respecte pas les normes minimales pour la sécurité, la fiabilité et l’évolutivité des communications d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="103d0-115">Lync Server 2013 does not support UDP for SIP transport because it doesn’t meet the minimum standards for enterprise communications security, reliability, and scalability.</span></span> <span data-ttu-id="103d0-116">Pour plus d’informations, reportez-vous à l’article de blog NextHop, «au protocole UDP ou pas à UDP, qui est la question «à [https://go.microsoft.com/fwlink/p/?linkId=185369](https://go.microsoft.com/fwlink/p/?linkid=185369) .</span><span class="sxs-lookup"><span data-stu-id="103d0-116">For details, see the NextHop blog article, "To UDP, or not to UDP, that is the question," at [https://go.microsoft.com/fwlink/p/?linkId=185369](https://go.microsoft.com/fwlink/p/?linkid=185369).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="103d0-117">Le contenu des blogs et leurs URL peuvent être modifiés sans préavis.</span><span class="sxs-lookup"><span data-stu-id="103d0-117">The content of each blog and its URL are subject to change without notice.</span></span>

    
    <span data-ttu-id="103d0-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="103d0-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

