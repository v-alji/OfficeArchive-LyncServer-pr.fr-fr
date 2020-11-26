---
title: 'Lync Server 2013 : Vue d’ensemble du directeur'
description: 'Lync Server 2013 : vue d’ensemble du directeur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of the Director
ms:assetid: cf9919b3-e16b-47c5-be1d-2c4bc64f44ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398879(v=OCS.15)
ms:contentKeyID: 48185393
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6686534e22bab5b02a2663789298e4cf7ea582c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424708"
---
# <a name="overview-of-the-director-in-lync-server-2013"></a><span data-ttu-id="ad5d6-103">Vue d’ensemble du directeur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ad5d6-103">Overview of the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ad5d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ad5d6-104">

<span> </span></span></span>

<span data-ttu-id="ad5d6-105">_**Dernière modification de la rubrique :** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="ad5d6-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="ad5d6-106">Un directeur est un serveur exécutant Lync Server 2013 qui authentifie les demandes des utilisateurs, mais qui n’utilise pas les comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ad5d6-106">A Director is a server running Lync Server 2013 that authenticates user requests, but does not home any user accounts.</span></span> <span data-ttu-id="ad5d6-107">Vous pouvez également déployer un réalisateur dans les deux scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="ad5d6-107">You optionally can deploy a Director in the following two scenarios:</span></span>

  - <span data-ttu-id="ad5d6-108">Si vous autorisez l’accès par des utilisateurs externes en déployant des serveurs de périphérie, vous devez également déployer un directeur.</span><span class="sxs-lookup"><span data-stu-id="ad5d6-108">If you enable access by external users by deploying Edge Servers, you should also deploy a Director.</span></span> <span data-ttu-id="ad5d6-109">Dans ce scénario, le directeur authentifie les utilisateurs externes, puis transmet leur trafic aux serveurs internes.</span><span class="sxs-lookup"><span data-stu-id="ad5d6-109">In this scenario, the Director authenticates the external users, and then passes their traffic on to internal servers.</span></span> <span data-ttu-id="ad5d6-110">Lorsqu’un directeur est utilisé pour authentifier des utilisateurs externes, il allège la surcharge des serveurs du pool frontal en effectuant une authentification de ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ad5d6-110">When a Director is used to authenticate external users, it relieves Front End pool servers from the overhead of performing authentication of these users.</span></span> <span data-ttu-id="ad5d6-111">Il permet également d’isoler les listes frontales internes du trafic malveillant, par exemple pour les attaques par déni de service.</span><span class="sxs-lookup"><span data-stu-id="ad5d6-111">It also helps insulate internal Front End pools from malicious traffic such as denial-of-service attacks.</span></span> <span data-ttu-id="ad5d6-112">Si le réseau est inondé de trafic externe non valide lors d’une telle attaque, il se termine au directeur.</span><span class="sxs-lookup"><span data-stu-id="ad5d6-112">If the network is flooded with invalid external traffic in such an attack, this traffic ends at the Director.</span></span>

  - <span data-ttu-id="ad5d6-113">Si vous déployez plusieurs pools front-end sur un site central, en ajoutant un réalisateur à ce site, vous pouvez rationaliser les demandes d’authentification et améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="ad5d6-113">If you deploy multiple Front End pools at a central site, by adding a Director to that site you can streamline authentication requests and improve performance.</span></span> <span data-ttu-id="ad5d6-114">Dans ce scénario, toutes les demandes sont d’abord adressées au directeur, qui les route vers le pool frontal approprié.</span><span class="sxs-lookup"><span data-stu-id="ad5d6-114">In this scenario, all requests go first to the Director, which then routes them to the correct Front End pool.</span></span>

<span data-ttu-id="ad5d6-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ad5d6-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

