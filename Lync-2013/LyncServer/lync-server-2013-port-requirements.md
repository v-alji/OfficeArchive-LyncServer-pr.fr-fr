---
title: Configuration requise pour les ports Lync Server 2013
description: Configuration requise pour les ports Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port requirements
ms:assetid: 9a6c1300-ef88-4181-a8f1-43cd3093962b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398798(v=OCS.15)
ms:contentKeyID: 48184886
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba7ae9a1ee098f55c61ae476f12c3b856c69f90e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424393"
---
# <a name="port-requirements-for-lync-server-2013"></a><span data-ttu-id="b8a33-103">Configuration requise pour les ports pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8a33-103">Port requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b8a33-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b8a33-104">

<span> </span></span></span>

<span data-ttu-id="b8a33-105">_**Dernière modification de la rubrique :** 2013-03-27_</span><span class="sxs-lookup"><span data-stu-id="b8a33-105">_**Topic Last Modified:** 2013-03-27_</span></span>

<span data-ttu-id="b8a33-106">Le serveur Lync nécessite l’ouverture des ports spécifiques du pare-feu.</span><span class="sxs-lookup"><span data-stu-id="b8a33-106">Lync Server requires that specific ports on the firewall be open.</span></span> <span data-ttu-id="b8a33-107">De plus, si la sécurité IPsec (Internet Protocol security) est déployée dans votre organisation, elle doit être désactivée sur la plage de ports utilisée pour l’acheminement des flux audio, vidéo et de vidéo panoramique.</span><span class="sxs-lookup"><span data-stu-id="b8a33-107">Additionally, if Internet Protocol security (IPsec) is deployed in your organization, IPsec must be disabled over the range of ports used for the delivery of audio, video, and panorama video.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b8a33-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b8a33-108">In This Section</span></span>

<span data-ttu-id="b8a33-109">Cette section comprend les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b8a33-109">This section includes the following topics:</span></span>

  - [<span data-ttu-id="b8a33-110">Ports et protocoles pour les serveurs internes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8a33-110">Ports and protocols for internal servers in Lync Server 2013</span></span>](lync-server-2013-ports-and-protocols-for-internal-servers.md)

  - [<span data-ttu-id="b8a33-111">Exceptions IPsec dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8a33-111">IPsec exceptions in Lync Server 2013</span></span>](lync-server-2013-ipsec-exceptions.md)

  - [<span data-ttu-id="b8a33-112">Résumé des ports - Serveur Edge unique consolidé avec adresses IP privées avec la conversion d’adresses réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8a33-112">Port summary - Single consolidated edge with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-port-summary-single-consolidated-edge-with-private-ip-addresses-using-nat.md)

  - [<span data-ttu-id="b8a33-113">Résumé des ports - Serveur Edge unique consolidé avec adresses IP publiques dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8a33-113">Port summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-port-summary-single-consolidated-edge-with-public-ip-addresses.md)

  - [<span data-ttu-id="b8a33-114">Résumé des enregistrements DNS - Serveur Edge consolidé mis à l’échelle, équilibrage de charge DNS avec adresses IP privées avec la conversion d’adresses réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8a33-114">Port summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-port-summary-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)

  - [<span data-ttu-id="b8a33-115">Résumé des ports - Serveur Edge consolidé mis à l’échelle, équilibrage de charge DNS avec des adresses IP publiques dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8a33-115">Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-port-summary-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)

  - [<span data-ttu-id="b8a33-116">Résumé des ports - Serveur Edge consolidé mis à l’échelle avec des équilibreurs de charge matérielle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8a33-116">Port summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>](lync-server-2013-port-summary-scaled-consolidated-edge-with-hardware-load-balancers.md)

  - [<span data-ttu-id="b8a33-117">Résumé des ports - Proxy inverse dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8a33-117">Port summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-port-summary-reverse-proxy.md)

  - [<span data-ttu-id="b8a33-118">Résumé de port-SIP, Fédération de XMPP et messagerie instantanée publique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8a33-118">Port summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-port-summary-sip-xmpp-federation-and-public-instant-messaging.md)

<span data-ttu-id="b8a33-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b8a33-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

