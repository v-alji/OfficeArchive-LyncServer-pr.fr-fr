---
title: Compatibilité de Lync Server 2013 avec la résistance de sites métropolitains Lync Server 2010
description: Compatibilité Lync Server 2013 avec la résilience du site métropolitain de Lync Server 2010.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2010 metropolitan site resiliency
ms:assetid: 18673ff6-b664-4a57-a89b-cbda8b129e6a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204715(v=OCS.15)
ms:contentKeyID: 48183526
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec72f261ac593b24bad13dcd400f495ba7ba0722
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434605"
---
# <a name="lync-server-2010-metropolitan-site-resiliency"></a><span data-ttu-id="4005d-103">Résistance de sites métropolitains Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="4005d-103">Lync Server 2010 metropolitan site resiliency</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4005d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4005d-104">

<span> </span></span></span>

<span data-ttu-id="4005d-105">_**Dernière modification de la rubrique :** 2014-03-19_</span><span class="sxs-lookup"><span data-stu-id="4005d-105">_**Topic Last Modified:** 2014-03-19_</span></span>

<span data-ttu-id="4005d-106">La solution de résilience de site métropolitaine prise en charge pour Lync Server 2010 n’est pas prise en charge pour Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4005d-106">The metropolitan site resiliency solution supported for Lync Server 2010 is not supported for Lync Server 2013.</span></span> <span data-ttu-id="4005d-107">Cette solution impliquait le fractionnement d’un pool frontal unique entre deux centres de données dans la même zone métropolitaine.</span><span class="sxs-lookup"><span data-stu-id="4005d-107">This solution involved spanning a single Front End pool across two data centers in the same metropolitan area.</span></span>

<span data-ttu-id="4005d-108">La solution de résilience du site métropolitain a été conçue pour être récupérée suite à la perte d’un datacenter complet.</span><span class="sxs-lookup"><span data-stu-id="4005d-108">The metropolitan site resiliency solution was designed to recover from the loss of a full datacenter.</span></span> <span data-ttu-id="4005d-109">Lorsque vous étendez votre réserve sur deux centres de serveurs, vous placez en général la moitié de vos extrémités au sein d’un centre de ressources et l’autre moitié dans le deuxième centre de ressources.</span><span class="sxs-lookup"><span data-stu-id="4005d-109">When you span your pool across two datacenters, you typically put half of your front ends in one datacenter and the other half in the second datacenter.</span></span> <span data-ttu-id="4005d-110">Si vous perdez l’intégralité d’un centre de données, vous avez perdu la moitié de vos serveurs frontaux.</span><span class="sxs-lookup"><span data-stu-id="4005d-110">If you lose an entire datacenter, you have lost half of your Front End Servers.</span></span> <span data-ttu-id="4005d-111">Cela peut poser des problèmes avec le nouveau modèle de système distribué pour les pools front-end dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4005d-111">This can cause issues with the new distributed system model for Front End Pools in Lync Server 2013.</span></span> <span data-ttu-id="4005d-112">Pour plus d’informations, reportez-vous à la rubrique [topologies et composants pour les serveurs frontaux, la messagerie instantanée et la présence dans Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span><span class="sxs-lookup"><span data-stu-id="4005d-112">For more information, see [Topologies and components for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span></span>

<span data-ttu-id="4005d-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4005d-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

