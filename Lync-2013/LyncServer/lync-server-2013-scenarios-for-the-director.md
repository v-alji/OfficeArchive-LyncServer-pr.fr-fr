---
title: 'Lync Server 2013 : Scénarios pour le directeur'
description: 'Lync Server 2013 : scénarios pour le directeur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scenarios for the Director
ms:assetid: d2cf384a-0860-4779-80ce-cba2543be322
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398908(v=OCS.15)
ms:contentKeyID: 48185419
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45c611fbe680ba55fb148c08fed26d96a848507e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444979"
---
# <a name="scenarios-for-the-director-in-lync-server-2013"></a><span data-ttu-id="b48a0-103">Scénarios pour le directeur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b48a0-103">Scenarios for the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b48a0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b48a0-104">

<span> </span></span></span>

<span data-ttu-id="b48a0-105">_**Dernière modification de la rubrique :** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="b48a0-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="b48a0-106">Un directeur est un serveur exécutant un logiciel de communication Microsoft Lync Server 2013 capable d’authentifier les demandes des utilisateurs, mais qui ne famille pas les comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b48a0-106">A Director is a server running Microsoft Lync Server 2013 communications software that can authenticate user requests, but does not home any user accounts.</span></span> <span data-ttu-id="b48a0-107">Le directeur héberge également des services Web similaires au serveur frontal, et authentifie les demandes de tickets Web et fournit d’autres services.</span><span class="sxs-lookup"><span data-stu-id="b48a0-107">The Director also hosts web services similar to the Front End Server and will authenticate web ticket requests and provide other services.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b48a0-108">Si vous déployez des directeurs, vous devez publier les services Web de Director en externe via le proxy inverse, ainsi que les services Web du serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="b48a0-108">If you deploy Directors, you must publish the Director web services externally through the reverse proxy as well as the web services of the Front End Server.</span></span> <span data-ttu-id="b48a0-109">Les rubriques suivantes décrivent le processus de planification des topologies de réalisateur possibles.</span><span class="sxs-lookup"><span data-stu-id="b48a0-109">The topics following describe the planning process for the possible Director topologies.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b48a0-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b48a0-110">In This Section</span></span>

  - [<span data-ttu-id="b48a0-111">Vue d’ensemble du directeur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b48a0-111">Overview of the Director in Lync Server 2013</span></span>](lync-server-2013-overview-of-the-director.md)

  - [<span data-ttu-id="b48a0-112">Composants requis pour le directeur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b48a0-112">Components required for the Director in Lync Server 2013</span></span>](lync-server-2013-components-required-for-the-director.md)

  - [<span data-ttu-id="b48a0-113">Configuration matérielle et logicielle requise pour le directeur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b48a0-113">Hardware and software requirements for the Director in Lync Server 2013</span></span>](lync-server-2013-hardware-and-software-requirements-for-the-director.md)

  - [<span data-ttu-id="b48a0-114">Directeur unique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b48a0-114">Single Director in Lync Server 2013</span></span>](lync-server-2013-single-director.md)

  - [<span data-ttu-id="b48a0-115">Pool directeur mis à l’échelle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b48a0-115">Scaled Director pool in Lync Server 2013</span></span>](lync-server-2013-scaled-director-pool.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b48a0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b48a0-116">See Also</span></span>


[<span data-ttu-id="b48a0-117">Topologies prises en charge dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b48a0-117">Supported topologies in Lync Server 2013</span></span>](lync-server-2013-supported-topologies.md)  
[<span data-ttu-id="b48a0-118">Server Hardware Platforms pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b48a0-118">Server hardware platforms for Lync Server 2013</span></span>](lync-server-2013-server-hardware-platforms.md)  
  

<span data-ttu-id="b48a0-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b48a0-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

