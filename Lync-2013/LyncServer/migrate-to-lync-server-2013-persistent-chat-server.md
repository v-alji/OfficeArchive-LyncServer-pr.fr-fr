---
title: Migration de Lync Server 2010, conversation de groupe ou de la conversation de groupe Office Communications Server 2007 R2 vers Lync Server 2013, serveur de conversation permanente
description: Migration à partir de Lync Server 2010, d’une conversation de groupe ou d’une conversation de groupe Office Communications Server 2007 R2 vers Lync Server 2013, serveur de conversation permanente.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server
ms:assetid: 5b4d3db1-6eba-4932-b49c-f60bcf9488f9
ms:mtpsurl: https://technet.microsoft.com/library/Gg615442(v=OCS.15)
ms:contentKeyID: 48184240
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6090d5924a203a960444d9a10700fd178d038887
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446856"
---
# <a name="migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server"></a><span data-ttu-id="029db-103">Migration de Lync Server 2010, conversation de groupe ou de la conversation de groupe Office Communications Server 2007 R2 vers Lync Server 2013, serveur de conversation permanente</span><span class="sxs-lookup"><span data-stu-id="029db-103">Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="029db-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="029db-104">

<span> </span></span></span>

<span data-ttu-id="029db-105">_**Dernière modification de la rubrique :** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="029db-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="029db-106">Les rubriques de cette section vous guident tout au long du processus de migration de Lync Server 2010, d’une conversation de groupe ou d’une conversation de groupe Microsoft Office Communications Server 2007 R2 vers Lync Server 2013, serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="029db-106">The topics in this section guide you through the process of migrating either Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="029db-107">Si vous envisagez d’utiliser Lync Server 2013, le déploiement permanent de Chat Server pour une coexistence avec un serveur Lync Server 2010, une conversation de groupe ou un déploiement d’Office Communications Server 2007 R2 en conversation de groupe, ce guide inclut également des informations essentielles pour l’utilisation de cet environnement mixte.</span><span class="sxs-lookup"><span data-stu-id="029db-107">If you intend for your Lync Server 2013, Persistent Chat Server deployment to coexist with a Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat deployment, this guide also includes some essential information for operating in this mixed environment.</span></span> <span data-ttu-id="029db-108">Ce guide porte essentiellement sur la migration des données pour le serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="029db-108">This guide primarily focuses on data migration for Persistent Chat Server.</span></span> <span data-ttu-id="029db-109">Pour les utilisateurs migrant d’une version héritée de Lync Server vers Lync Server 2013, voir [migration de Lync server 2010 vers Lync server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) et [migration d’Office Communications Server 2007 R2 vers Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="029db-109">For users who are migrating from legacy versions of Lync Server to Lync Server 2013, see [Migration from Lync Server 2010 to Lync Server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) and [Migration from Office Communications Server 2007 R2 to Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="029db-110">Cette rubrique part du principe que vous avez déjà installé Lync Server 2013 dans la coexistence avec Lync Server 2010 ou Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="029db-110">This topic assumes that you have already installed Lync Server 2013 in coexistence with Lync Server 2010 or Office Communications Server 2007 R2.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="029db-111">Ce guide décrit les étapes généralement requises pour effectuer chaque phase de migration.</span><span class="sxs-lookup"><span data-stu-id="029db-111">This guide describes the steps generally required to accomplish each phase of migration.</span></span> <span data-ttu-id="029db-112">Elle ne traite pas chaque topologie de déploiement hérité possible ou chaque scénario de migration possible.</span><span class="sxs-lookup"><span data-stu-id="029db-112">It does not address every possible legacy deployment topology or every possible migration scenario.</span></span> <span data-ttu-id="029db-113">Par conséquent, vous n’aurez peut-être pas besoin d’effectuer toutes les étapes décrites, ou vous devrez peut-être effectuer des étapes supplémentaires selon votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="029db-113">Therefore, you may not need to perform every step that is described, or you may need to perform additional steps, depending on your deployment.</span></span> <span data-ttu-id="029db-114">Ce guide fournit également des exemples de procédure de vérification.</span><span class="sxs-lookup"><span data-stu-id="029db-114">The guide also provides examples of verification steps.</span></span> <span data-ttu-id="029db-115">Ces étapes de vérification sont fournies pour vous aider à comprendre ce que vous devez savoir pour vous assurer que chaque phase se termine correctement lors de la migration.</span><span class="sxs-lookup"><span data-stu-id="029db-115">These verification steps are provided to help you understand what you need to look for to be sure that each phase completes successfully as you progress through your migration.</span></span> <span data-ttu-id="029db-116">Vous pouvez modifier ces étapes de vérification pour votre processus de migration spécifique.</span><span class="sxs-lookup"><span data-stu-id="029db-116">You can modify these verification steps to your specific migration process.</span></span>



</div>

<span data-ttu-id="029db-117">Ce guide fournit des informations spécifiques à la mise à niveau de votre déploiement existant.</span><span class="sxs-lookup"><span data-stu-id="029db-117">This guide provides information specific to upgrading your existing deployment.</span></span> <span data-ttu-id="029db-118">Il n’explique pas comment modifier votre topologie existante.</span><span class="sxs-lookup"><span data-stu-id="029db-118">It does not explain how to change your existing topology.</span></span> <span data-ttu-id="029db-119">Ce guide ne traite pas de l’implémentation des nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="029db-119">This guide does not cover the implementation of new features.</span></span> <span data-ttu-id="029db-120">Lorsqu’une procédure détaillée est documentée à un autre emplacement, ce guide vous dirige vers la section document ou document appropriée.</span><span class="sxs-lookup"><span data-stu-id="029db-120">When a detailed procedure is documented elsewhere, this guide directs you to the appropriate document or document section.</span></span>

<span data-ttu-id="029db-121">Ce document définit les termes indiqués dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="029db-121">This document defines terms as specified in the following list.</span></span>

  - <span data-ttu-id="029db-122">*vers*</span><span class="sxs-lookup"><span data-stu-id="029db-122">*migration*</span></span>  
    <span data-ttu-id="029db-123">Le déplacement de votre déploiement à partir d’une version précédente de chat permanent du serveur, auparavant appelé serveur de discussion de groupe, vers Lync Server 2013, serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="029db-123">Moving your deployment from a previous version of Persistent Chat Server, formerly known as Group Chat Server, to Lync Server 2013, Persistent Chat Server.</span></span>

<!-- end list -->

  - <span data-ttu-id="029db-124">*installation*</span><span class="sxs-lookup"><span data-stu-id="029db-124">*upgrade*</span></span>  
    <span data-ttu-id="029db-125">Installation d’une nouvelle version du logiciel sur un ordinateur client ou serveur.</span><span class="sxs-lookup"><span data-stu-id="029db-125">Installing a newer version of software on a server or client computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="029db-126">*coexistence*</span><span class="sxs-lookup"><span data-stu-id="029db-126">*coexistence*</span></span>  
    <span data-ttu-id="029db-127">L’environnement temporaire qui existe lors de la migration, lorsque certaines fonctionnalités ont été migrées vers Lync Server 2013, le serveur de conversations permanentes et d’autres fonctionnalités continuent de subsister sur une version antérieure du serveur de discussion de groupe.</span><span class="sxs-lookup"><span data-stu-id="029db-127">The temporary environment that exists during migration, when some functionality has been migrated to Lync Server 2013, Persistent Chat Server, and other functionality still remains on a prior version of Group Chat Server.</span></span>

<span data-ttu-id="029db-128">Le serveur Chat permanent est une extension de l’infrastructure 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="029db-128">Persistent Chat Server is an extension of the Lync Server 2013 infrastructure.</span></span> <span data-ttu-id="029db-129">En fonction de votre topologie, vous pouvez migrer Lync Server 2010, une conversation de groupe ou une conversation de groupe Office Communications Server 2007 R2 vers Lync Server 2013 permanent Chat Server.</span><span class="sxs-lookup"><span data-stu-id="029db-129">Depending on your topology, you can migrate Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013 Persistent Chat Server.</span></span> <span data-ttu-id="029db-130">Pour plus d’informations sur les topologies disponibles et la configuration logicielle requise pour la migration du serveur de discussion de groupe, reportez-vous à la section [planification du serveur de chat permanent dans Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="029db-130">For details about available topologies and the technical and software requirements for migrating Group Chat Server, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation.</span></span>

<span data-ttu-id="029db-131">Si votre organisation nécessite une prise en charge de la conformité, celle-ci est désormais automatiquement installée sur chaque serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="029db-131">If your organization requires compliance support, it is now automatically installed with each Persistent Chat Server.</span></span> <span data-ttu-id="029db-132">Un serveur distinct n’est plus nécessaire pour la conformité.</span><span class="sxs-lookup"><span data-stu-id="029db-132">A separate server is no longer needed for compliance.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="029db-133">Le serveur de chat permanent doit être installé sur un système de fichiers NTFS pour garantir la sécurité du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="029db-133">Persistent Chat Server must be installed on an NTFS file system to help enforce file system security.</span></span> <span data-ttu-id="029db-134">FAT32 n’est pas un système de fichiers pris en charge pour le serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="029db-134">FAT32 is not a supported file system for Persistent Chat Server.</span></span><BR><span data-ttu-id="029db-135">Si votre organisation nécessite une prise en charge de la conformité, celle-ci est désormais automatiquement installée sur chaque serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="029db-135">If your organization requires compliance support, it is now automatically installed with each Persistent Chat Server.</span></span> <span data-ttu-id="029db-136">Un serveur distinct n’est plus nécessaire pour la conformité.</span><span class="sxs-lookup"><span data-stu-id="029db-136">A separate server is no longer needed for compliance.</span></span> <span data-ttu-id="029db-137">Pour plus d’informations sur les modifications dans Lync Server 2013 &nbsp; persistent Chat Server, reportez-vous à la rubrique <A href="lync-server-2013-new-persistent-chat-server-features.md">nouvelles fonctionnalités du serveur de chat permanent de lync Server 2013</A> dans la documentation de mise en route.</span><span class="sxs-lookup"><span data-stu-id="029db-137">For more details about changes in Lync Server 2013&nbsp;Persistent Chat Server, see <A href="lync-server-2013-new-persistent-chat-server-features.md">New Persistent Chat Server features in Lync Server 2013</A> in the Getting Started documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="029db-138">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="029db-138">In This Section</span></span>

  - [<span data-ttu-id="029db-139">Scénario de migration standard - Haut niveau</span><span class="sxs-lookup"><span data-stu-id="029db-139">Standard migration scenario - high-level</span></span>](standard-migration-scenario-high-level.md)

  - [<span data-ttu-id="029db-140">Processus de migration - Détails</span><span class="sxs-lookup"><span data-stu-id="029db-140">Migration process - details</span></span>](migration-process-details.md)

  - [<span data-ttu-id="029db-141">Remarques liées à la coexistence</span><span class="sxs-lookup"><span data-stu-id="029db-141">Coexistence considerations</span></span>](coexistence-considerations.md)

<span data-ttu-id="029db-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="029db-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

