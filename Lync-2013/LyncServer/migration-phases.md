---
title: Phases de migration
description: Phases de migration.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migration phases
ms:assetid: cb7747ba-b872-42ca-ab41-76e3c4e77d06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205336(v=OCS.15)
ms:contentKeyID: 48185642
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 72ef47cb9b6c9eba75c395eb9bd94c887ca5a433
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443334"
---
# <a name="migration-phases"></a><span data-ttu-id="755ab-103">Phases de migration</span><span class="sxs-lookup"><span data-stu-id="755ab-103">Migration phases</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="755ab-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="755ab-104">

<span> </span></span></span>

<span data-ttu-id="755ab-105">_**Dernière modification de la rubrique :** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="755ab-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="755ab-106">Dans Lync Server 2013, vous définissez des sites sur votre réseau qui contiennent les composants Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="755ab-106">In Lync Server 2013, you define sites on your network that contain Lync Server 2013 components.</span></span> <span data-ttu-id="755ab-107">Un site est un ensemble d’ordinateurs qui sont bien connectés par le biais d’un réseau haut débit à faible latence, par exemple un réseau local unique (LAN) ou deux réseaux connectés par un réseau fibres optiques haut débit.</span><span class="sxs-lookup"><span data-stu-id="755ab-107">A site is a set of computers that are well-connected by a high-speed, low-latency network, such as a single local area network (LAN) or two networks connected by a high-speed fiber optic network.</span></span>

<span data-ttu-id="755ab-108">Un *pool frontal* est un ensemble de serveurs frontaux configurés de manière identique et collabore pour fournir des services à un groupe d’utilisateurs communs.</span><span class="sxs-lookup"><span data-stu-id="755ab-108">A *Front End pool* is a set of Front End Servers that are configured identically and work together to provide services for a common group of users.</span></span> <span data-ttu-id="755ab-109">Un pool fournit une capacité d’évolutivité et de basculement pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="755ab-109">A pool provides scalability and failover capability to your users.</span></span> <span data-ttu-id="755ab-110">Chaque serveur d’un pool doit exécuter un ou plusieurs rôles serveur identiques.</span><span class="sxs-lookup"><span data-stu-id="755ab-110">Each server in a pool must run an identical server role or roles.</span></span> <span data-ttu-id="755ab-111">Un serveur Standard Edition, conçu pour les petites organisations, définit également un pool et s’exécute sur un serveur unique.</span><span class="sxs-lookup"><span data-stu-id="755ab-111">A Standard Edition server, designed for small organizations, also defines a pool and runs on a single server.</span></span> <span data-ttu-id="755ab-112">Cela vous permet d’utiliser la fonctionnalité Lync Server 2013 pour un coût inférieur, mais ne fournit pas de véritable solution de disponibilité élevée.</span><span class="sxs-lookup"><span data-stu-id="755ab-112">This enables you to have Lync Server 2013 functionality for a lesser cost, but does not provide a true high-availability solution.</span></span>

<span data-ttu-id="755ab-113">Les phases suivantes décrivent le processus de migration d’un pool de Lync Server 2010 vers Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="755ab-113">The following phases describe the process of a pool migration from Lync Server 2010 to Lync Server 2013.</span></span> <span data-ttu-id="755ab-114">Pour les sites multiples contenant plusieurs pools, chaque pool individuel doit suivre cette approche par phases.</span><span class="sxs-lookup"><span data-stu-id="755ab-114">For multiple sites containing multiple pools, each individual pool should follow this phased approach.</span></span>

1.  [<span data-ttu-id="755ab-115">Étape 1 : planifier la migration à partir de Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="755ab-115">Phase 1: Plan your migration from Lync Server 2010</span></span>](phase-1-plan-your-migration-from-lync-server-2010.md)

2.  [<span data-ttu-id="755ab-116">Étape 2 : Préparer la migration</span><span class="sxs-lookup"><span data-stu-id="755ab-116">Phase 2: Prepare for migration</span></span>](phase-2-prepare-for-migration.md)

3.  [<span data-ttu-id="755ab-117">Étape 3 : déployer le pool de pilotes de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="755ab-117">Phase 3: Deploy Lync Server 2013 pilot pool</span></span>](phase-3-deploy-lync-server-2013-pilot-pool.md)

4.  [<span data-ttu-id="755ab-118">Étape 4 : déplacer les utilisateurs de test vers le pool de pilotes</span><span class="sxs-lookup"><span data-stu-id="755ab-118">Phase 4: Move test users to the pilot pool</span></span>](phase-4-move-test-users-to-the-pilot-pool.md)

5.  [<span data-ttu-id="755ab-119">Étape 5 : ajouter le serveur Edge Lync Server 2013 au pool de pilotes</span><span class="sxs-lookup"><span data-stu-id="755ab-119">Phase 5: Add Lync Server 2013 Edge Server to pilot pool</span></span>](phase-5-add-lync-server-2013-edge-server-to-pilot-pool.md)

6.  [<span data-ttu-id="755ab-120">Phase 6 : Transition d’un déploiement pilote vers un environnement de production</span><span class="sxs-lookup"><span data-stu-id="755ab-120">Phase 6: Move from pilot deployment into production</span></span>](phase-6-move-from-pilot-deployment-into-production.md)

7.  [<span data-ttu-id="755ab-121">Étape 7 : Exécuter les tâches post-migration</span><span class="sxs-lookup"><span data-stu-id="755ab-121">Phase 7: Complete post-migration tasks</span></span>](phase-7-complete-post-migration-tasks.md)

8.  [<span data-ttu-id="755ab-122">Étape 8 : Mettre des pools hérités hors service</span><span class="sxs-lookup"><span data-stu-id="755ab-122">Phase 8: Decommission legacy pools</span></span>](phase-8-decommission-legacy-pools.md)

<span data-ttu-id="755ab-123"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="755ab-123"></div>

<span> </span>

</div>

</div>

</span></span></div>

