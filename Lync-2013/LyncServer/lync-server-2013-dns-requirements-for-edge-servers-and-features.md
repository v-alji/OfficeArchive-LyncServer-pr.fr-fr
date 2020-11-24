---
title: 'Lync Server 2013 : configuration requise pour DNS pour les serveurs et fonctionnalités Edge'
description: 'Lync Server 2013 : configuration requise pour DNS pour les serveurs et fonctionnalités Edge.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Edge Servers and features
ms:assetid: e3bf05c8-96fb-4dd2-acb1-f0d141c9e2ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721912(v=OCS.15)
ms:contentKeyID: 49733846
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9bcfd00080e765924eecc3138bc3d552ce331b63
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395024"
---
# <a name="dns-requirements-for-edge-servers-and-features-in-lync-server-2013"></a><span data-ttu-id="cf0d7-103">Configuration requise pour DNS pour les serveurs et fonctionnalités Edge dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf0d7-103">DNS requirements for Edge Servers and features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cf0d7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cf0d7-104">

<span> </span></span></span>

<span data-ttu-id="cf0d7-105">_**Dernière modification de la rubrique :** 2014-04-08_</span><span class="sxs-lookup"><span data-stu-id="cf0d7-105">_**Topic Last Modified:** 2014-04-08_</span></span>

<span data-ttu-id="cf0d7-106">Les serveurs Edge Lync Server 2013, les pools de bords et les proxys inversés ont des exigences spécifiques pour les enregistrements DNS (Domain Name System).</span><span class="sxs-lookup"><span data-stu-id="cf0d7-106">Lync Server 2013 Edge Servers, Edge pools, and reverse proxies have specific requirements for Domain Name System (DNS) records.</span></span> <span data-ttu-id="cf0d7-107">Dans Lync Server 2013 lorsque IPv4 et IPv6 sont en cours d’utilisation, vous devez planifier pour les enregistrements hôte A et AAAA.</span><span class="sxs-lookup"><span data-stu-id="cf0d7-107">In Lync Server 2013 when IPv4 and IPv6 are in use, you must plan for both host A and AAAA records.</span></span>

<span data-ttu-id="cf0d7-108">Les rubriques répertoriées ci-dessous décrivent l’utilisation des enregistrements DNS pour votre planification de déploiement :</span><span class="sxs-lookup"><span data-stu-id="cf0d7-108">The topics listed below define the use of DNS records for your deployment planning:</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="cf0d7-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="cf0d7-109">In This Section</span></span>

  - [<span data-ttu-id="cf0d7-110">Résumé des enregistrements DNS - Serveur Edge unique consolidé avec adresses IP privées avec la conversion d’adresses réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf0d7-110">DNS summary - Single consolidated edge with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-dns-summary-single-consolidated-edge-with-private-ip-addresses-using-nat.md)

  - [<span data-ttu-id="cf0d7-111">Résumé des enregistrements DNS - Serveur Edge unique consolidé avec adresses IP publiques dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf0d7-111">DNS summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-dns-summary-single-consolidated-edge-with-public-ip-addresses.md)

  - [<span data-ttu-id="cf0d7-112">Résumé DNS - Serveur Edge consolidé mis à l’échelle, équilibrage de charge DNS avec adresses IP privées avec la conversion d’adresses réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf0d7-112">DNS summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-dns-summary-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)

  - [<span data-ttu-id="cf0d7-113">Résumé des enregistrements DNS - Serveur Edge consolidé mis à l’échelle, équilibrage de charge DNS avec des adresses IP publiques dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf0d7-113">DNS summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-dns-summary-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)

  - [<span data-ttu-id="cf0d7-114">Résumé des enregistrements DNS - Serveur Edge consolidé mis à l’échelle avec des équilibreurs de charge matérielle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf0d7-114">DNS summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>](lync-server-2013-dns-summary-scaled-consolidated-edge-with-hardware-load-balancers.md)

  - [<span data-ttu-id="cf0d7-115">Résumé DNS - Proxy inverse dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf0d7-115">DNS summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-dns-summary-reverse-proxy.md)

  - [<span data-ttu-id="cf0d7-116">Résumé DNS-SIP, Fédération de XMPP et messagerie instantanée publique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf0d7-116">DNS summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-dns-summary-sip-xmpp-federation-and-public-instant-messaging.md)

<span data-ttu-id="cf0d7-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cf0d7-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

