---
title: 'Lync Server 2013 : gestion des modifications'
description: 'Lync Server 2013 : gestion des modifications.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Change management
ms:assetid: 73c774f5-c12f-4c72-be73-e07dc745b994
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720336(v=OCS.15)
ms:contentKeyID: 63969618
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69ea019f6366528c40b60a39ca8b646b49b336b0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435125"
---
# <a name="change-management-in-lync-server-2013"></a><span data-ttu-id="a0c0a-103">Gestion des modifications dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0c0a-103">Change management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0c0a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0c0a-104">

<span> </span></span></span>

<span data-ttu-id="a0c0a-105">_**Dernière modification de la rubrique :** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="a0c0a-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="a0c0a-106">La modification de l’environnement informatique est inévitable.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-106">Changes to the IT environment are unavoidable.</span></span> <span data-ttu-id="a0c0a-107">Les modifications incluent de nouvelles technologies, systèmes, applications, matériel, outils, processus et modifications dans les rôles et les responsabilités.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-107">Changes include new technologies, systems, applications, hardware, tools, processes, and changes in roles and responsibilities.</span></span> <span data-ttu-id="a0c0a-108">Un système de gestion des modifications efficace vous permet d’apporter des modifications à l’environnement informatique en toute simplicité et en minimisant les interruptions de service.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-108">An effective change management system lets you introduce changes to the IT environment quickly and with minimal service disruption.</span></span> <span data-ttu-id="a0c0a-109">Un système de gestion des modifications réunit les équipes impliquées dans le changement de système.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-109">A change management system brings together the teams involved in changing a system.</span></span> <span data-ttu-id="a0c0a-110">Par exemple, en choisissant de tirer parti d’Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-110">For example, deciding to take advantage of the Office Web Apps.</span></span> <span data-ttu-id="a0c0a-111">Il s’agit d’une application de service Lync intégrée qui permet aux utilisateurs de lire et de modifier des documents dans un navigateur.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-111">This is an integrated Lync Service application that enables users to read and edit documents in a browser.</span></span> <span data-ttu-id="a0c0a-112">La mise en place de ce service, une fois que vous êtes passé en production, nécessite la participation de plusieurs équipes :</span><span class="sxs-lookup"><span data-stu-id="a0c0a-112">The implementation of this service, after you have gone into production, requires the involvement of several teams:</span></span>

  - <span data-ttu-id="a0c0a-113">**Équipe de test**   Cette équipe est chargée de tester les applications Office Web Apps sur un serveur de test, dans le processus fournissant des informations sur les modèles d’utilisation prévus et les performances attendues des serveurs de production.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-113">**Test Team**   This team load-tests the Office Web Apps on a test server, in the process providing information about the expected usage patterns and expected performance of the production servers.</span></span>

  - <span data-ttu-id="a0c0a-114">**Administrateurs Lync**   Cette équipe détermine la stratégie de déploiement et les scripts d’installation à l’endroit où il était possible.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-114">**Lync Administrators**   This team determines the deployment strategy and scripts the installation where it was possible.</span></span> <span data-ttu-id="a0c0a-115">L’équipe doit s’assurer que le changement est déployé dans l’environnement de production et qu’il est responsable de l’administration par la suite.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-115">The team is responsible for making sure that the change is deployed on the production environment, and it is responsible for administration afterward.</span></span> <span data-ttu-id="a0c0a-116">L’équipe doit comprendre l’impact des modifications et les inclure dans les procédures avant que les modifications soient apportées à la production.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-116">The team must understand the effect of the changes and incorporate them in procedures before the changes are put into production</span></span>

  - <span data-ttu-id="a0c0a-117">**Équipe réseau**   Cette équipe est responsable des modifications apportées aux règles de pare-feu qui autorisent l’accès à partir d’Internet aux serveurs de pools Lync internes.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-117">**Network Team**   This team is responsible for changes to firewall rules that allow access from the Internet to the internal Lync pool servers.</span></span> <span data-ttu-id="a0c0a-118">L’équipe est également responsable de l’utilisation des administrateurs Lync pour s’assurer que la bande passante disponible peut prendre en charge la charge supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-118">The team is also responsible in working with the Lync administrators for making sure that the available bandwidth can support the additional load.</span></span>

  - <span data-ttu-id="a0c0a-119">**Équipe de sécurité**   Cette équipe évalue la sécurité et réduit les risques.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-119">**Security Team**   This team assesses security and minimizes risks.</span></span> <span data-ttu-id="a0c0a-120">L’équipe de sécurité doit revoir les vulnérabilités connues et garantir le minimum de risques en matière de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-120">The security team must review known vulnerabilities and help ensure that security risks are minimized.</span></span>

  - <span data-ttu-id="a0c0a-121">**Équipe d’approbation des utilisateurs**   Cette équipe est composée d’utilisateurs désireux de tester le système et de fournir des commentaires pour les améliorations.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-121">**User Acceptance Team**   This team is composed of users who are willing to test the system and offer feedback for improvements.</span></span>

<span data-ttu-id="a0c0a-122">Le processus de gestion des modifications définit les responsabilités de chaque équipe et planifie le travail à effectuer, en incluant des contrôles et des tests là où ils sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-122">The change management process defines the responsibilities of each team and schedules the work to be performed, incorporating checks and tests where they are required.</span></span> <span data-ttu-id="a0c0a-123">Les contrôles de modification varient en fonction de la complexité et de l’effet attendu d’une modification.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-123">Change controls will vary depending on the complexity and expected effect of a change.</span></span> <span data-ttu-id="a0c0a-124">Ils peuvent varier en fonction de l’approbation automatique des modifications mineures, de la modification des réunions de révision et des avis complets au niveau du projet.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-124">They can vary from automatic approval of minor changes, to change review meetings, to full project-level reviews.</span></span> <span data-ttu-id="a0c0a-125">Pour en expliquer davantage, les groupes de modifications sont décrits dans cette section.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-125">To explain this better, the groups of changes are discussed in this section.</span></span>

  - <span data-ttu-id="a0c0a-126">**Principales modifications**   Les modifications majeures ont un effet global sur le système et peuvent nécessiter une entrée de diverses équipes.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-126">**Major Changes**   Major changes have a global effect on the system and may require input from various teams.</span></span> <span data-ttu-id="a0c0a-127">Voici un exemple de mise à niveau vers Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-127">An example of this is upgrading to Lync Server 2013.</span></span> <span data-ttu-id="a0c0a-128">Les modifications majeures affectent de nombreuses équipes et peut-être des systèmes différents.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-128">Major changes affect many teams and perhaps different systems.</span></span> <span data-ttu-id="a0c0a-129">Le processus de gestion des modifications inclura probablement une ou plusieurs réunions d’avis de modification pour informer les équipes participant au changement ou affectées par le changement.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-129">The change management process will probably include one or more change review meetings to inform the teams that will be involved in the change or be affected by the change.</span></span>

  - <span data-ttu-id="a0c0a-130">**Modifications importantes**   Les modifications significatives nécessitent des ressources significatives pour la planification, la création et l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-130">**Significant Changes**   Significant changes require significant resources to plan, build, and implement.</span></span> <span data-ttu-id="a0c0a-131">Des contrôles de modification appropriés doivent être introduits pour s’assurer que l’effet du changement est compris, que les procédures de déploiement sont testées et que les plans de restauration et de contingence sont prêts.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-131">Appropriate change controls should be introduced to help make ensure that the effect of the change is understood, deployment procedures are tested, and the rollback and contingency plans are ready.</span></span> <span data-ttu-id="a0c0a-132">Le déploiement d’une nouvelle mise à jour cumulative est un exemple de modification notable.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-132">An example of a significant change is deploying a new cumulative update.</span></span>

  - <span data-ttu-id="a0c0a-133">**Changements mineurs**   Les changements mineurs n’affectent pas de façon significative l’environnement informatique, par exemple, la modification de certaines stratégies Lync via le panneau de configuration Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-133">**Minor Changes**   Minor changes do not significantly affect the IT environment, for example, changing certain Lync policies via the Microsoft Lync Server 2013 Control Panel.</span></span>

  - <span data-ttu-id="a0c0a-134">**Modifications standard**   Les modifications standard sont effectuées régulièrement et sont bien entendues et documentées.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-134">**Standard Changes**   Standard changes are performed regularly and are well understood and documented.</span></span> <span data-ttu-id="a0c0a-135">Le processus de gestion des modifications doit examiner toutes les modifications apportées aux procédures.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-135">The change management process should review all changes to the procedures.</span></span> <span data-ttu-id="a0c0a-136">Il n’est pas nécessaire de procéder à des modifications de routine comme la création d’une base de données de contenu ou l’ajout d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-136">It should not be needed for routine changes like creating a content database or adding a user.</span></span>

<span data-ttu-id="a0c0a-137">Dans l’exemple suivant, la gestion des modifications examine le mode d’interaction des différentes équipes et les actions effectuées lors du déploiement d’un nouveau Service Pack.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-137">The following example of change management examines how different teams interact and the actions that are performed when a new service pack is deployed.</span></span> <span data-ttu-id="a0c0a-138">Ces actions sont organisées et gérées par le processus de gestion des modifications.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-138">These actions are organized and managed by the change management process.</span></span>

  - <span data-ttu-id="a0c0a-139">**Élever une demande de modification**   L’équipe de sécurité a évalué le dernier Service Pack et confirme qu’il résout une vulnérabilité dans le système de production.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-139">**Raise a change request**   The security team has assessed the latest service pack and confirmed that it resolves a possible vulnerability in the production system.</span></span> <span data-ttu-id="a0c0a-140">L’équipe déclenche une demande de modification pour que la nouvelle mise à jour cumulative s’applique à tous les serveurs exécutant Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-140">The team raises a change request to have the new cumulative update applied to all servers that are running Lync Server.</span></span>

  - <span data-ttu-id="a0c0a-141">**Réviser les notes de publication du Service Pack**   L’équipe de l’administrateur de Lync examine les notes de publication du Service Pack pour identifier l’effet sur le système.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-141">**Service pack release notes review**   The Lync administrator team reviews the service pack release notes to identify the effect on the system.</span></span>

  - <span data-ttu-id="a0c0a-142">**Une série de tests en laboratoire est effectuée**   L’équipe de l’administrateur de Lync doit effectuer des mises à jour de test sur un serveur dans un environnement de test pour déterminer si le Service Pack peut être appliqué correctement sans affecter les applications et systèmes serveur installés.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-142">**A series of lab tests is performed**   The Lync administrator team must perform test updates on a server in a test environment to decide whether the service pack can be applied successfully without affecting any of the installed applications and server systems.</span></span> <span data-ttu-id="a0c0a-143">S’il existe des applications tierces ou créées en interne qui interservent le serveur Lync dans un environnement de production, celles-ci doivent également être testées.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-143">If there are third-party or internally created applications that interface with Lync Server in a production environment, these should be also tested.</span></span> <span data-ttu-id="a0c0a-144">Ces tests peuvent également être utilisés pour estimer le temps nécessaire pour effectuer les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-144">These tests can also be used to estimate the time that is required to perform the upgrades.</span></span>

  - <span data-ttu-id="a0c0a-145">Les **utilisateurs sont informés de la panne** .   L’équipe d’administrateur de Lync, l’équipe de communication ou le support technique de l’utilisateur informe tous les utilisateurs concernés du cycle de maintenance planifié et de la durée de leur indisponibilité.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-145">**Users are informed of the outage**   The Lync administrator team, communications team, or user help desk informs all affected users about the planned maintenance cycle and how long the service will be unavailable.</span></span>

  - <span data-ttu-id="a0c0a-146">**Une sauvegarde complète de Lync est effectuée avant la mise à niveau**   L’équipe de l’administrateur de Lync doit vérifier qu’il existe une sauvegarde valide permettant de rétablir l’état d’origine du système en cas d’échec de l’installation du Service Pack.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-146">**A full backup of Lync is performed before the upgrade**   The Lync administrator team must verify that there is a valid backup that can be used to revert to the original system state if the service pack installation fails.</span></span> <span data-ttu-id="a0c0a-147">Nous vous recommandons de restaurer la sauvegarde sur un serveur de secours pour que ce système soit facilement disponible en cas de problème.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-147">We recommend that the backup be restored to a standby server to have this system readily available if there are issues.</span></span>

  - <span data-ttu-id="a0c0a-148">**La mise à jour cumulative est déployée**   L’équipe de l’administrateur de Lync effectue l’installation pendant le cycle de maintenance planifiée.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-148">**The cumulative update is deployed**   The Lync administrator team does the installation during the planned maintenance cycle.</span></span>

<div>

## <a name="managing-the-timing-of-changes"></a><span data-ttu-id="a0c0a-149">Gestion de la durée des modifications</span><span class="sxs-lookup"><span data-stu-id="a0c0a-149">Managing the timing of changes</span></span>

<span data-ttu-id="a0c0a-150">Nous vous recommandons d’implémenter une procédure pour la planification des modifications afin d’éviter toute interruption dans les sections qui se chevauchent.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-150">We recommend that you implement a procedure for scheduling changes to avoid disruptions in overlapping sections of your work.</span></span> <span data-ttu-id="a0c0a-151">Par exemple, il est possible que deux équipes envisagent une modification mineure d’un système.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-151">For example, two teams may both be planning a minor change to a system.</span></span> <span data-ttu-id="a0c0a-152">Une équipe peut appliquer une mise à jour cumulative sur un pool alors qu’une autre équipe migre des utilisateurs hérités vers ce pool.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-152">One team may be applying a cumulative update on a pool while another team is migrating legacy users into that pool.</span></span> <span data-ttu-id="a0c0a-153">Aucune équipe n’est concernée par les modifications que l’autre équipe planifie, et chaque équipe ne connaît peut-être pas nécessairement les modifications que l’autre équipe planifie.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-153">Neither team is affected by the changes that the other team is planning, and each team may not necessarily know about changes that the other team is planning.</span></span> <span data-ttu-id="a0c0a-154">Si les deux modifications ont été apportées en même temps, il est possible que les modifications soient implémentées.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-154">If both changes occurred at the same time, there might be issues implementing the changes.</span></span> <span data-ttu-id="a0c0a-155">Par ailleurs, s’il y a des problèmes une fois les modifications appliquées (par exemple, en cas d’échec de la migration des utilisateurs), il peut être difficile de déterminer quelles modifications doivent être répercutées.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-155">Also, if there are issues after the changes were applied, for example, if the user migration fails, it may be difficult to decide which change should be rolled back.</span></span> <span data-ttu-id="a0c0a-156">Des périodes de maintenance normales doivent être définies entre le service informatique et la gestion pour tester les modifications et les accepter.</span><span class="sxs-lookup"><span data-stu-id="a0c0a-156">There should be regular maintenance periods set up between IT and management to test the changes and accept them.</span></span>

<span data-ttu-id="a0c0a-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0c0a-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

