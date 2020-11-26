---
title: 'Lync Server 2013 : Gestion de l’infrastructure réseau Lync Server 2013'
description: 'Lync Server 2013 : gestion de l’infrastructure réseau de Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing the Lync Server 2013 network infrastructure
ms:assetid: cb13456a-8f66-4595-be21-8887f30ad4eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182585(v=OCS.15)
ms:contentKeyID: 48185638
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ab1b5c6fe52374b012063ac26640e9bb25496ad7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425856"
---
# <a name="managing-the-lync-server-2013-network-infrastructure"></a><span data-ttu-id="6f423-103">Gestion de l’infrastructure réseau Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f423-103">Managing the Lync Server 2013 network infrastructure</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6f423-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6f423-104">

<span> </span></span></span>

<span data-ttu-id="6f423-105">_**Dernière modification de la rubrique :** 2014-02-11_</span><span class="sxs-lookup"><span data-stu-id="6f423-105">_**Topic Last Modified:** 2014-02-11_</span></span>

<span data-ttu-id="6f423-106">Microsoft Lync Server 2013 inclut la prise en charge du contrôle d’admission des appels (CAC) et du contournement multimédia.</span><span class="sxs-lookup"><span data-stu-id="6f423-106">Microsoft Lync Server 2013 includes support for call admission control (CAC) and media bypass.</span></span> <span data-ttu-id="6f423-107">Pour implémenter ces fonctionnalités, vous devez configurer un réseau de régions, de sites, de sous-réseaux, etc., afin de gérer la bande passante dans les situations où les transmissions audio et vidéo doivent être restreintes.</span><span class="sxs-lookup"><span data-stu-id="6f423-107">To implement these features you must configure a network of regions, sites, subnets, and so on that will allow you to manage bandwidth in situations where audio and video transmissions need to be restricted.</span></span> <span data-ttu-id="6f423-108">Vous pouvez également utiliser la technologie de mise en réseau de qualité de service (QoS) pour offrir une interface utilisateur optimale pour les communications audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="6f423-108">You can also use the Quality of Service (QoS) networking technology to help provide an optimal end-user experience for audio and video communications.</span></span>

<span data-ttu-id="6f423-109">Le panneau de configuration de Lync Server vous permet de configurer et de gérer le CAC, le contournement du contenu multimédia et la qualité de service (QoS).</span><span class="sxs-lookup"><span data-stu-id="6f423-109">You can use the Lync Server Control Panel to set up and manage CAC, media bypass, and QoS.</span></span> <span data-ttu-id="6f423-110">Les rubriques suivantes décrivent les étapes de la procédure à suivre.</span><span class="sxs-lookup"><span data-stu-id="6f423-110">The following topics provide steps for how to do this.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6f423-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="6f423-111">In This Section</span></span>

  - [<span data-ttu-id="6f423-112">Gestion de la qualité de service (QoS) dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f423-112">Managing Quality of Service (QoS) in Lync Server 2013</span></span>](lync-server-2013-managing-quality-of-service-qos.md)

  - [<span data-ttu-id="6f423-113">Gestion du contrôle d’admission des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f423-113">Managing call admission control in Lync Server 2013</span></span>](lync-server-2013-managing-call-admission-control.md)

  - [<span data-ttu-id="6f423-114">Interfaces réseau de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f423-114">Lync Server 2013 network interfaces</span></span>](lync-server-2013-lync-server-network-interfaces.md)

  - [<span data-ttu-id="6f423-115">Empêcher les nouvelles connexions à Lync Server 2013 pour la maintenance du serveur</span><span class="sxs-lookup"><span data-stu-id="6f423-115">Prevent new connections to Lync Server 2013 for server maintenance</span></span>](lync-server-2013-prevent-new-connections-to-lync-server-for-server-maintenance.md)

  - [<span data-ttu-id="6f423-116">Méthodologie de qualité d’appel Lync dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f423-116">Lync Call Quality Methodology in Lync Server 2013</span></span>](lync-server-2013-poster-lync-call-quality-methodology.md)

  - [<span data-ttu-id="6f423-117">Principaux indicateurs d’intégrité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f423-117">Key Health Indicators in Lync Server 2013</span></span>](lync-server-2013-poster-key-health-indicators.md)

<span data-ttu-id="6f423-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6f423-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

