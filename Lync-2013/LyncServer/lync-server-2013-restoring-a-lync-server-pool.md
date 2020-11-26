---
title: 'Lync Server 2013 : restauration d’un pool de serveurs Lync'
description: 'Lync Server 2013 : restauration d’un pool de serveurs Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a Lync Server pool
ms:assetid: 6fe80fb3-38ad-4931-a07b-1763b61aa448
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202176(v=OCS.15)
ms:contentKeyID: 51541488
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 02e92b4e7af9cf782d49c265425006e0118b9161
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442599"
---
# <a name="restoring-a-lync-server-pool-in-lync-server-2013"></a><span data-ttu-id="e9490-103">Restauration d’un pool de serveurs Lync dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e9490-103">Restoring a Lync Server pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e9490-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e9490-104">

<span> </span></span></span>

<span data-ttu-id="e9490-105">_**Dernière modification de la rubrique :** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="e9490-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="e9490-106">Votre déploiement de Lync Server est susceptible de comprendre les types de pools suivants :</span><span class="sxs-lookup"><span data-stu-id="e9490-106">Your Lync Server deployment may include any of the following types of pools:</span></span>

  - <span data-ttu-id="e9490-107">serveur frontal</span><span class="sxs-lookup"><span data-stu-id="e9490-107">Front End Server</span></span>

  - <span data-ttu-id="e9490-108">serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="e9490-108">Mediation Server</span></span>

  - <span data-ttu-id="e9490-109">serveur de conversations permanentes</span><span class="sxs-lookup"><span data-stu-id="e9490-109">Persistent Chat Server</span></span>

  - <span data-ttu-id="e9490-110">serveur Edge</span><span class="sxs-lookup"><span data-stu-id="e9490-110">Edge Server</span></span>

<span data-ttu-id="e9490-111">Si un pool entier rencontre une panne, procédez comme suit pour chaque serveur membre du pool.</span><span class="sxs-lookup"><span data-stu-id="e9490-111">If an entire pool experiences an outage, follow these procedures for each member server in the pool.</span></span>

  - <span data-ttu-id="e9490-112">Dans le cas d’une réserve frontale, restaurez d’abord le serveur principal, puis restaurez chaque serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="e9490-112">For a Front End pool, restore the Back End Server first, and then restore each Front End Server.</span></span> <span data-ttu-id="e9490-113">Pour plus d’informations, reportez-vous à la rubrique [restauration d’un serveur principal Enterprise Edition dans Lync server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md) et [restauration d’un serveur membre Enterprise Edition dans Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span><span class="sxs-lookup"><span data-stu-id="e9490-113">For details, see [Restoring an Enterprise Edition Back End Server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md) and [Restoring an Enterprise Edition member server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span></span>

  - <span data-ttu-id="e9490-114">Pour tous les autres types de pools, restaurez chaque serveur membre.</span><span class="sxs-lookup"><span data-stu-id="e9490-114">For all other types of pools, restore each member server.</span></span> <span data-ttu-id="e9490-115">Pour plus d’informations, reportez-vous à la rubrique [restauration d’un serveur membre Enterprise Edition dans Lync server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span><span class="sxs-lookup"><span data-stu-id="e9490-115">For details, see [Restoring an Enterprise Edition member server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span></span>

<span data-ttu-id="e9490-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e9490-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

