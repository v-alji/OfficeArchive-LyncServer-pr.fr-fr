---
title: Migration d’Office Communications Server 2007 R2 vers Lync Server 2013
description: Migration d’Office Communications Server 2007 R2 vers Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Office Communications Server 2007 R2 to Lync Server 2013
ms:assetid: f3fa4f5f-e9a2-4fb7-a12d-20f04173e697
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205375(v=OCS.15)
ms:contentKeyID: 48185802
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0afdc754ae691bc674c200addb9fb97c1eb4199
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446148"
---
# <a name="migration-from-office-communications-server-2007-r2-to-lync-server-2013"></a><span data-ttu-id="374fe-103">Migration d’Office Communications Server 2007 R2 vers Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="374fe-103">Migration from Office Communications Server 2007 R2 to Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="374fe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="374fe-104">

<span> </span></span></span>

<span data-ttu-id="374fe-105">_**Dernière modification de la rubrique :** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="374fe-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="374fe-106">Les rubriques de cette section vous guident tout au long du processus de migration d’Office Communications Server 2007 R2 vers Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="374fe-106">The topics in this section guide you through the process of migrating from Office Communications Server 2007 R2 to Lync Server 2013</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="374fe-107">Ce document décrit les étapes généralement requises pour effectuer chaque phase de la migration.</span><span class="sxs-lookup"><span data-stu-id="374fe-107">This document describes the steps generally required to accomplish each phase of migration.</span></span> <span data-ttu-id="374fe-108">Elle ne traite pas chaque topologie de déploiement hérité possible ou chaque scénario de migration possible.</span><span class="sxs-lookup"><span data-stu-id="374fe-108">It does not address every possible legacy deployment topology or every possible migration scenario.</span></span> <span data-ttu-id="374fe-109">Par conséquent, il est possible que vous n’ayez pas à effectuer toutes les étapes décrites ou que vous deviez effectuer des étapes supplémentaires, selon votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="374fe-109">Therefore, you may not need to perform every step described, or you may need to perform additional steps, depending on your deployment.</span></span> <span data-ttu-id="374fe-110">Ce document fournit également des exemples de procédure de vérification.</span><span class="sxs-lookup"><span data-stu-id="374fe-110">This document also provides examples of verification steps.</span></span> <span data-ttu-id="374fe-111">Ces étapes de vérification sont fournies pour vous aider à comprendre ce que vous devez savoir pour vous assurer que toutes les phases s’exécutent correctement lors de la migration.</span><span class="sxs-lookup"><span data-stu-id="374fe-111">These verification steps are provided to help you understand what you need to look for to ensure that each phase completes successfully as you progress through your migration.</span></span> <span data-ttu-id="374fe-112">Adaptez ces étapes de vérification à votre processus de migration spécifique.</span><span class="sxs-lookup"><span data-stu-id="374fe-112">Tailor these verification steps to your specific migration process.</span></span>



</div>

<span data-ttu-id="374fe-113">Ce guide fournit des informations spécifiques à la mise à niveau de votre déploiement existant.</span><span class="sxs-lookup"><span data-stu-id="374fe-113">This guide provides information specific to upgrading your existing deployment.</span></span> <span data-ttu-id="374fe-114">Il n’explique pas comment modifier votre topologie existante.</span><span class="sxs-lookup"><span data-stu-id="374fe-114">It does not explain how to change your existing topology.</span></span> <span data-ttu-id="374fe-115">Ce guide ne traite pas de l’implémentation des nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="374fe-115">This guide does not cover the implementation of new features.</span></span> <span data-ttu-id="374fe-116">Lorsqu’une procédure détaillée est documentée à un autre emplacement, ce guide vous dirige vers la section document ou document appropriée.</span><span class="sxs-lookup"><span data-stu-id="374fe-116">When a detailed procedure is documented elsewhere, this guide directs you to the appropriate document or document section.</span></span>

<span data-ttu-id="374fe-117">Ce document définit les termes indiqués dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="374fe-117">This document defines terms as specified in the following list.</span></span>

  - <span data-ttu-id="374fe-118">*vers*</span><span class="sxs-lookup"><span data-stu-id="374fe-118">*migration*</span></span>  
    <span data-ttu-id="374fe-119">Migration de votre déploiement de production d’une version antérieure d’Office Communications Server 2007 R2 vers Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="374fe-119">Moving your production deployment from a previous version of Office Communications Server 2007 R2 to Lync Server 2013.</span></span>

<!-- end list -->

  - <span data-ttu-id="374fe-120">*installation*</span><span class="sxs-lookup"><span data-stu-id="374fe-120">*upgrade*</span></span>  
    <span data-ttu-id="374fe-121">Installation d’une nouvelle version du logiciel sur un ordinateur client ou serveur.</span><span class="sxs-lookup"><span data-stu-id="374fe-121">Installing a newer version of software on a server or client computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="374fe-122">*coexistence*</span><span class="sxs-lookup"><span data-stu-id="374fe-122">*coexistence*</span></span>  
    <span data-ttu-id="374fe-123">L’environnement temporaire existant lors de la migration lors de la migration de certaines fonctionnalités vers Lync Server 2013 et d’autres fonctionnalités continuent de subsister sur une version antérieure d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="374fe-123">The temporary environment that exists during migration when some functionality has been migrated to Lync Server 2013 and other functionality still remains on a prior version of Office Communications Server 2007 R2.</span></span>

<!-- end list -->

  - <span data-ttu-id="374fe-124">*interopérabilité*</span><span class="sxs-lookup"><span data-stu-id="374fe-124">*interoperability*</span></span>  
    <span data-ttu-id="374fe-125">La capacité de votre déploiement à fonctionner correctement pendant la période de coexistence.</span><span class="sxs-lookup"><span data-stu-id="374fe-125">The ability of your deployment to operate successfully during the period of coexistence.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="374fe-126">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="374fe-126">In This Section</span></span>

  - [<span data-ttu-id="374fe-127">Avant de commencer la migration</span><span class="sxs-lookup"><span data-stu-id="374fe-127">Before you begin the migration</span></span>](before-you-begin-the-migration.md)

  - [<span data-ttu-id="374fe-128">Phases de migration</span><span class="sxs-lookup"><span data-stu-id="374fe-128">Migration phases</span></span>](migration-phases.md)

  - [<span data-ttu-id="374fe-129">Étape 1 : planifier la migration à partir d’Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="374fe-129">Phase 1: Plan your migration from Office Communications Server 2007 R2</span></span>](phase-1-plan-your-migration-from-office-communications-server-2007-r2.md)

  - [<span data-ttu-id="374fe-130">Étape 2 : Préparer la migration</span><span class="sxs-lookup"><span data-stu-id="374fe-130">Phase 2: Prepare for migration</span></span>](phase-2-prepare-for-migration.md)

  - [<span data-ttu-id="374fe-131">Étape 3 : déployer le pool de pilotes de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="374fe-131">Phase 3: Deploy Lync Server 2013 pilot pool</span></span>](phase-3-deploy-lync-server-2013-pilot-pool.md)

  - [<span data-ttu-id="374fe-132">Étape 4 : fusionner les topologies</span><span class="sxs-lookup"><span data-stu-id="374fe-132">Phase 4: Merge topologies</span></span>](phase-4-merge-topologies.md)

  - [<span data-ttu-id="374fe-133">Étape 5 : configurer le pool de pilotes</span><span class="sxs-lookup"><span data-stu-id="374fe-133">Phase 5: Configure the pilot pool</span></span>](phase-5-configure-the-pilot-pool.md)

  - [<span data-ttu-id="374fe-134">Étape 6 : déplacer les utilisateurs vers le pool de pilotes</span><span class="sxs-lookup"><span data-stu-id="374fe-134">Phase 6: Move users to the pilot pool</span></span>](phase-6-move-users-to-the-pilot-pool.md)

  - [<span data-ttu-id="374fe-135">Étape 7 : ajouter le serveur Edge Lync Server 2013 au pool de pilotes</span><span class="sxs-lookup"><span data-stu-id="374fe-135">Phase 7: Add Lync Server 2013 Edge Server to pilot pool</span></span>](phase-7-add-lync-server-2013-edge-server-to-pilot-pool.md)

  - [<span data-ttu-id="374fe-136">Phase 8 : basculer entre le déploiement pilote et la production</span><span class="sxs-lookup"><span data-stu-id="374fe-136">Phase 8: Move from pilot deployment into production</span></span>](phase-8-move-from-pilot-deployment-into-production.md)

  - [<span data-ttu-id="374fe-137">Phase 9 : effectuer les tâches postérieures à la migration</span><span class="sxs-lookup"><span data-stu-id="374fe-137">Phase 9: Complete post-migration tasks</span></span>](phase-9-complete-post-migration-tasks.md)

  - [<span data-ttu-id="374fe-138">Étape 10 : désaffecter le site hérité</span><span class="sxs-lookup"><span data-stu-id="374fe-138">Phase 10: Decommission legacy site</span></span>](phase-10-decommission-legacy-site.md)

<span data-ttu-id="374fe-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="374fe-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

