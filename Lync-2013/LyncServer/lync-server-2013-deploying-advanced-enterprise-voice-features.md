---
title: 'Lync Server 2013 : déploiement de fonctionnalités avancées de voix entreprise'
description: 'Lync Server 2013 : déploiement de fonctionnalités avancées d’entreprise voix.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying advanced Enterprise Voice features
ms:assetid: 286d9c0b-9442-448f-a6e5-95b3034278fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425753(v=OCS.15)
ms:contentKeyID: 48183675
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e5cab05de60e1df1611a14af1f5239c24402c6d9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430111"
---
# <a name="deploying-advanced-enterprise-voice-features-in-lync-server-2013"></a><span data-ttu-id="c0b8f-103">Déploiement de fonctionnalités avancées d’entreprise voix dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0b8f-103">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c0b8f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c0b8f-104">

<span> </span></span></span>

<span data-ttu-id="c0b8f-105">_**Dernière modification de la rubrique :** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="c0b8f-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="c0b8f-106">Après avoir configuré Voix Entreprise dans votre organisation, vous pouvez déployer une ou plusieurs fonctionnalités Voix Entreprise plus avancées en procédant comme indiqué dans cette section.</span><span class="sxs-lookup"><span data-stu-id="c0b8f-106">After you have configured basic Enterprise Voice functionality for your organization, you can optionally deploy one or more advanced Enterprise Voice features by following the procedures in this section.</span></span>

<span data-ttu-id="c0b8f-107">Pour plus d’informations sur les fonctionnalités avancées de voix entreprise, reportez-vous aux sections suivantes de la documentation relative [à la planification de Lync Server 2013](lync-server-2013-planning.md) :</span><span class="sxs-lookup"><span data-stu-id="c0b8f-107">For details about the advanced Enterprise Voice features, see the following sections of the [Planning for Lync Server 2013](lync-server-2013-planning.md) documentation:</span></span>

  - [<span data-ttu-id="c0b8f-108">Planification du contrôle d’admission des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0b8f-108">Planning for call admission control in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-admission-control.md)

  - [<span data-ttu-id="c0b8f-109">Planification des services d’urgence (E9-1-1) dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0b8f-109">Planning for emergency services (E9-1-1) in Lync Server 2013</span></span>](lync-server-2013-planning-for-emergency-services-e9-1-1.md)

  - [<span data-ttu-id="c0b8f-110">Planification de la déviation du trafic multimédia dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0b8f-110">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)

<div>

## <a name="in-this-section"></a><span data-ttu-id="c0b8f-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="c0b8f-111">In This Section</span></span>

  - [<span data-ttu-id="c0b8f-112">À propos des régions réseau, des sites réseau et des sous-réseaux dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0b8f-112">About network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-about-network-regions-sites-and-subnets.md)

  - [<span data-ttu-id="c0b8f-113">Créer ou modifier une région réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0b8f-113">Create or modify a network region in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-region.md)

  - [<span data-ttu-id="c0b8f-114">Création ou modification d’un site réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0b8f-114">Create or modify a network site in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-site.md)

  - [<span data-ttu-id="c0b8f-115">Association d’un sous-réseau à un site réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0b8f-115">Associate a subnet with a network site in Lync Server 2013</span></span>](lync-server-2013-associate-a-subnet-with-a-network-site.md)

  - [<span data-ttu-id="c0b8f-116">Configurer le contrôle d’admission des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0b8f-116">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)

  - [<span data-ttu-id="c0b8f-117">Configuration d’Enhanced 9-1-1 dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0b8f-117">Configure Enhanced 9-1-1 in Lync Server 2013</span></span>](lync-server-2013-configure-enhanced-9-1-1.md)

  - [<span data-ttu-id="c0b8f-118">Configuration de la déviation du trafic multimédia dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0b8f-118">Configure media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-media-bypass.md)

<span data-ttu-id="c0b8f-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c0b8f-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

