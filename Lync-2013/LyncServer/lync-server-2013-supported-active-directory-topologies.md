---
title: 'Lync Server 2013 : Topologies Active Directory prises en charge'
description: 'Lync Server 2013 : topologies Active Directory prises en charge.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported Active Directory topologies
ms:assetid: 0c76b778-7652-4eb0-b161-86f2d4a94ccf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398173(v=OCS.15)
ms:contentKeyID: 48183391
ms.date: 10/02/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9ce820a36cb033933b423e01deb5a3049ed3ea2e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441533"
---
# <a name="supported-active-directory-topologies-in-lync-server-2013"></a><span data-ttu-id="d3673-103">Topologies Active Directory prises en charge dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3673-103">Supported Active Directory topologies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d3673-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d3673-104">

<span> </span></span></span>

<span data-ttu-id="d3673-105">_**Dernière modification de la rubrique :** 2014-10-02_</span><span class="sxs-lookup"><span data-stu-id="d3673-105">_**Topic Last Modified:** 2014-10-02_</span></span>

<span data-ttu-id="d3673-106">Lync Server 2013 prend en charge les mêmes topologies de services de domaine Active Directory que Microsoft Lync Server 2010 et Microsoft Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d3673-106">Lync Server 2013 supports the same Active Directory Domain Services topologies as Microsoft Lync Server 2010 and Microsoft Office Communications Server 2007 R2.</span></span> <span data-ttu-id="d3673-107">Les topologies suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="d3673-107">The following topologies are supported:</span></span>

  - <span data-ttu-id="d3673-108">Forêt unique avec domaine unique</span><span class="sxs-lookup"><span data-stu-id="d3673-108">Single forest with single domain</span></span>

  - <span data-ttu-id="d3673-109">Forêt unique avec un arbre unique et plusieurs domaines</span><span class="sxs-lookup"><span data-stu-id="d3673-109">Single forest with a single tree and multiple domains</span></span>

  - <span data-ttu-id="d3673-110">Forêt unique avec plusieurs arbres et des espaces de noms disjoints</span><span class="sxs-lookup"><span data-stu-id="d3673-110">Single forest with multiple trees and disjoint namespaces</span></span>

  - <span data-ttu-id="d3673-111">Plusieurs forêts dans une topologie de forêt centrale</span><span class="sxs-lookup"><span data-stu-id="d3673-111">Multiple forests in a central forest topology</span></span>

  - <span data-ttu-id="d3673-112">Plusieurs forêts dans une topologie de forêt de ressources</span><span class="sxs-lookup"><span data-stu-id="d3673-112">Multiple forests in a resource forest topology</span></span>

  - <span data-ttu-id="d3673-113">Plusieurs forêts dans une topologie de forêt de ressources Lync avec Exchange Online</span><span class="sxs-lookup"><span data-stu-id="d3673-113">Multiple forests in a Lync resource forest topology with Exchange Online</span></span>

<span data-ttu-id="d3673-114">La figure suivante identifie les icônes utilisées dans les illustrations de cette section.</span><span class="sxs-lookup"><span data-stu-id="d3673-114">The following figure identifies the icons used in the illustrations in this section.</span></span>

<span data-ttu-id="d3673-115">**Clé pour les illustrations topologiques**</span><span class="sxs-lookup"><span data-stu-id="d3673-115">**Key to topology illustrations**</span></span>

<span data-ttu-id="d3673-116">![Clé pour les illustrations topologiques](images/Gg398173.0c3cc89f-6c43-4bc8-b2ec-61d89e391ee9(OCS.15).jpg "Clé pour les illustrations topologiques")</span><span class="sxs-lookup"><span data-stu-id="d3673-116">![Key to topology illustrations](images/Gg398173.0c3cc89f-6c43-4bc8-b2ec-61d89e391ee9(OCS.15).jpg "Key to topology illustrations")</span></span>

<div>

## <a name="single-forest-single-domain"></a><span data-ttu-id="d3673-117">Forêt unique, domaine unique</span><span class="sxs-lookup"><span data-stu-id="d3673-117">Single Forest, Single Domain</span></span>

<span data-ttu-id="d3673-118">La topologie Active Directory la plus simple prise en charge par Lync Server (forêt de domaine unique) est une topologie courante.</span><span class="sxs-lookup"><span data-stu-id="d3673-118">The simplest Active Directory topology supported by Lync Server, a single domain forest, is a common topology.</span></span>

<span data-ttu-id="d3673-119">La figure suivante illustre un déploiement de serveur Lync dans une topologie Active Directory de domaine unique.</span><span class="sxs-lookup"><span data-stu-id="d3673-119">The following figure illustrates a Lync Server deployment in a single domain Active Directory topology.</span></span>

<span data-ttu-id="d3673-120">**Topologie à domaine unique**</span><span class="sxs-lookup"><span data-stu-id="d3673-120">**Single domain topology**</span></span>

<span data-ttu-id="d3673-121">![Topologie à domaine unique](images/Gg398173.258b3b3f-0558-4a36-a4c2-031be7299668(OCS.15).jpg "Topologie à domaine unique")</span><span class="sxs-lookup"><span data-stu-id="d3673-121">![Single domain topology](images/Gg398173.258b3b3f-0558-4a36-a4c2-031be7299668(OCS.15).jpg "Single domain topology")</span></span>

</div>

<div>

## <a name="single-forest-multiple-domains"></a><span data-ttu-id="d3673-122">Forêt unique, plusieurs domaines</span><span class="sxs-lookup"><span data-stu-id="d3673-122">Single Forest, Multiple Domains</span></span>

<span data-ttu-id="d3673-123">Une autre topologie Active Directory prise en charge par Lync Server est une forêt unique composée d’un domaine racine et d’un ou plusieurs domaines enfants.</span><span class="sxs-lookup"><span data-stu-id="d3673-123">Another Active Directory topology supported by Lync Server is a single forest that consists of a root domain and one or more child domains.</span></span> <span data-ttu-id="d3673-124">Dans ce type de topologie Active Directory, le domaine dans lequel vous créez des utilisateurs peut être différent de celui dans lequel vous déployez Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d3673-124">In this type of Active Directory topology, the domain where you create users can be different from the domain where you deploy Lync Server.</span></span> <span data-ttu-id="d3673-125">Toutefois, si vous déployez un pool frontal, vous devez déployer tous les serveurs frontaux dans le pool au sein d’un domaine unique.</span><span class="sxs-lookup"><span data-stu-id="d3673-125">However, if you deploy a Front End pool, you must deploy all the Front End Servers in the pool within a single domain.</span></span> <span data-ttu-id="d3673-126">La prise en charge de Lync Server pour les groupes d’administrateurs Windows universelle autorise une administration entre domaines.</span><span class="sxs-lookup"><span data-stu-id="d3673-126">Lync Server support for Windows universal administrator groups enables cross-domain administration.</span></span>

<span data-ttu-id="d3673-127">La figure suivante illustre un déploiement au sein d’une seule forêt avec plusieurs domaines.</span><span class="sxs-lookup"><span data-stu-id="d3673-127">The following figure illustrates a deployment in a single forest with multiple domains.</span></span> <span data-ttu-id="d3673-128">Dans cette figure, une icône utilisateur affiche le domaine dans lequel le compte d’utilisateur est hébergé et la flèche pointe vers le domaine dans lequel réside le pool de serveurs Lync.</span><span class="sxs-lookup"><span data-stu-id="d3673-128">In this figure, a user icon shows the domain where the user account is homed, and the arrow points to the domain where the Lync Server pool resides.</span></span> <span data-ttu-id="d3673-129">Les comptes d’utilisateurs incluent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d3673-129">User accounts include the following:</span></span>

  - <span data-ttu-id="d3673-130">Comptes d’utilisateurs au sein du même domaine que le pool de serveurs Lync</span><span class="sxs-lookup"><span data-stu-id="d3673-130">User accounts within the same domain as the Lync Server pool</span></span>

  - <span data-ttu-id="d3673-131">Comptes d’utilisateurs d’un domaine différent du pool de serveurs Lync</span><span class="sxs-lookup"><span data-stu-id="d3673-131">User accounts in a different domain from the Lync Server pool</span></span>

  - <span data-ttu-id="d3673-132">Comptes d’utilisateurs dans un domaine enfant du domaine avec le pool de serveurs Lync</span><span class="sxs-lookup"><span data-stu-id="d3673-132">User accounts in a child domain of the domain with the Lync Server pool</span></span>

<span data-ttu-id="d3673-133">**Forêt unique avec plusieurs domaines**</span><span class="sxs-lookup"><span data-stu-id="d3673-133">**Single forest with multiple domains**</span></span>

<span data-ttu-id="d3673-134">![Forêt unique avec plusieurs domaines](images/Gg398173.2b809c72-c3cd-4fad-afe6-8c2dae779750(OCS.15).jpg "Forêt unique avec plusieurs domaines")</span><span class="sxs-lookup"><span data-stu-id="d3673-134">![Single forest with multiple domains](images/Gg398173.2b809c72-c3cd-4fad-afe6-8c2dae779750(OCS.15).jpg "Single forest with multiple domains")</span></span>

</div>

<div>

## <a name="single-forest-multiple-trees"></a><span data-ttu-id="d3673-135">Forêt unique, plusieurs arbres</span><span class="sxs-lookup"><span data-stu-id="d3673-135">Single Forest, Multiple Trees</span></span>

<span data-ttu-id="d3673-136">Une topologie à plusieurs arborescences de forêts se compose de deux domaines ou plus qui définissent des structures d’arborescence indépendantes et des espaces de noms Active Directory distincts.</span><span class="sxs-lookup"><span data-stu-id="d3673-136">A multiple-tree forest topology consists of two or more domains that define independent tree structures and separate Active Directory namespaces.</span></span>

<span data-ttu-id="d3673-137">La figure suivante illustre une seule forêt avec plusieurs arborescences.</span><span class="sxs-lookup"><span data-stu-id="d3673-137">The following figure illustrates a single forest with multiple trees.</span></span> <span data-ttu-id="d3673-138">Dans cette figure, une icône d’utilisateur affiche le domaine dans lequel le compte d’utilisateur est hébergé, une ligne pleine pointe vers un pool de serveurs Lync résidant au sein d’un même domaine ou d’un autre domaine et un trait en pointillés vers Lync Server pool se trouvant dans une autre arborescence.</span><span class="sxs-lookup"><span data-stu-id="d3673-138">In this figure, a user icon shows the domain where the user account is homed, a solid line points to a Lync Server pool that resides in the same or a different domain, and a dashed line points to Lync Server pool that resides in a different tree.</span></span> <span data-ttu-id="d3673-139">Les comptes d’utilisateurs incluent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d3673-139">User accounts include the following:</span></span>

  - <span data-ttu-id="d3673-140">Comptes d’utilisateurs au sein du même domaine que le pool de serveurs Lync</span><span class="sxs-lookup"><span data-stu-id="d3673-140">User accounts within the same domain as the Lync Server pool</span></span>

  - <span data-ttu-id="d3673-141">Comptes d’utilisateurs d’un domaine différent de (mais de l’arborescence)</span><span class="sxs-lookup"><span data-stu-id="d3673-141">User accounts in a different domain from (but the same tree as) the Lync Server pool</span></span>

  - <span data-ttu-id="d3673-142">Comptes utilisateur dans une autre arborescence que le pool de serveurs Lync</span><span class="sxs-lookup"><span data-stu-id="d3673-142">User accounts in a different tree from the Lync Server pool</span></span>

<span data-ttu-id="d3673-143">**Forêt unique avec plusieurs arborescences**</span><span class="sxs-lookup"><span data-stu-id="d3673-143">**Single forest with multiple trees**</span></span>

<span data-ttu-id="d3673-144">![Forêt unique avec plusieurs arborescences](images/Gg398173.db30fa49-174a-4974-8695-41dd78e39432(OCS.15).jpg "Forêt unique avec plusieurs arborescences")</span><span class="sxs-lookup"><span data-stu-id="d3673-144">![Single forest with multiple trees](images/Gg398173.db30fa49-174a-4974-8695-41dd78e39432(OCS.15).jpg "Single forest with multiple trees")</span></span>

</div>

<div>

## <a name="multiple-forests-central-forest"></a><span data-ttu-id="d3673-145">Forêts multiples, forêt centrale</span><span class="sxs-lookup"><span data-stu-id="d3673-145">Multiple Forests, Central Forest</span></span>

<span data-ttu-id="d3673-146">Lync Server prend en charge plusieurs forêts configurées dans une topologie de forêt centrale.</span><span class="sxs-lookup"><span data-stu-id="d3673-146">Lync Server supports multiple forests that are configured in a central forest topology.</span></span> <span data-ttu-id="d3673-147">Les topologies de forêt centralisées utilisent les objets de contact dans la forêt centrale pour représenter les utilisateurs dans les autres forêts.</span><span class="sxs-lookup"><span data-stu-id="d3673-147">Central forest topologies use contact objects in the central forest to represent users in the other forests.</span></span> <span data-ttu-id="d3673-148">La forêt centrale héberge également les comptes d’utilisateurs pour tous les utilisateurs de cette forêt.</span><span class="sxs-lookup"><span data-stu-id="d3673-148">The central forest also hosts user accounts for any users in this forest.</span></span> <span data-ttu-id="d3673-149">Un produit de synchronisation d’annuaires, tel que Microsoft Identity Integration Server (MIIS); Microsoft Forefront Identity Manager (FIM) 2010 ou Microsoft Identity Lifecycle Manager (ILM) 2007 Feature Pack 1 (FP1), gère le cycle de vie des comptes d’utilisateurs au sein de l’Organisation : lorsqu’un nouveau compte d’utilisateur est créé dans l’une des forêts ou qu’un compte d’utilisateur est supprimé d’une forêt</span><span class="sxs-lookup"><span data-stu-id="d3673-149">A directory synchronization product, such as Microsoft Identity Integration Server (MIIS), Microsoft Forefront Identity Manager (FIM) 2010, or Microsoft Identity Lifecycle Manager (ILM) 2007 Feature Pack 1 (FP1), manages the life cycle of user accounts within the organization: When a new user account is created in one of the forests or a user account is deleted from a forest, the directory synchronization product synchronizes the corresponding contact in the central forest.</span></span>

<span data-ttu-id="d3673-150">Une forêt centrale offre les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="d3673-150">A central forest has the following advantages:</span></span>

  - <span data-ttu-id="d3673-151">Les serveurs exécutant Lync Server sont centralisés au sein d’une même forêt.</span><span class="sxs-lookup"><span data-stu-id="d3673-151">Servers running Lync Server are centralized within a single forest.</span></span>

  - <span data-ttu-id="d3673-152">Les utilisateurs peuvent rechercher et communiquer avec d’autres utilisateurs dans n’importe quelle forêt.</span><span class="sxs-lookup"><span data-stu-id="d3673-152">Users can search for and communicate with other users in any forest.</span></span>

  - <span data-ttu-id="d3673-153">Les utilisateurs peuvent afficher le statut de présence d’autres utilisateurs dans n’importe quelle forêt.</span><span class="sxs-lookup"><span data-stu-id="d3673-153">Users can view presence of other users in any forest.</span></span>

  - <span data-ttu-id="d3673-154">Le produit de synchronisation d’annuaires automatise l’ajout et la suppression d’objets de contact dans la forêt centrale lors de la création ou de la suppression de comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d3673-154">The directory synchronization product automates the addition and deletion of contact objects in the central forest as user accounts are created or removed.</span></span>

<span data-ttu-id="d3673-155">La figure suivante illustre une topologie de forêt centrale.</span><span class="sxs-lookup"><span data-stu-id="d3673-155">The following figure illustrates a central forest topology.</span></span> <span data-ttu-id="d3673-156">Dans cette figure, il existe des relations d’approbation à double sens entre le domaine qui héberge Lync Server, qui se trouve dans la forêt centrale et chaque domaine utilisateur uniquement, qui se trouve dans une autre forêt.</span><span class="sxs-lookup"><span data-stu-id="d3673-156">In this figure, there are two-way trust relationships between the domain that hosts Lync Server, which is in the central forest, and each user-only domain, which is in a separate forest.</span></span> <span data-ttu-id="d3673-157">Il n’est pas nécessaire de prolonger le schéma dans les forêts utilisateurs distinctes.</span><span class="sxs-lookup"><span data-stu-id="d3673-157">The schema in the separate user forests does not need to be extended.</span></span>

<span data-ttu-id="d3673-158">**Topologie de forêt centrale**</span><span class="sxs-lookup"><span data-stu-id="d3673-158">**Central forest topology**</span></span>

<span data-ttu-id="d3673-159">![Topologie de forêt centrale](images/Gg398173.7feb049a-453b-4134-9128-873b83ee1755(OCS.15).jpg "Topologie de forêt centrale")</span><span class="sxs-lookup"><span data-stu-id="d3673-159">![Central forest topology](images/Gg398173.7feb049a-453b-4134-9128-873b83ee1755(OCS.15).jpg "Central forest topology")</span></span>

</div>

<div>

## <a name="multiple-forests-resource-forest"></a><span data-ttu-id="d3673-160">Forêts multiples, forêt de ressources</span><span class="sxs-lookup"><span data-stu-id="d3673-160">Multiple Forests, Resource Forest</span></span>

<span data-ttu-id="d3673-161">Dans une topologie de forêt de ressources, une forêt est consacrée aux applications serveur en cours d’exécution, comme Microsoft Exchange Server et Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d3673-161">In a resource forest topology, one forest is dedicated to running server applications, such as Microsoft Exchange Server and Lync Server.</span></span> <span data-ttu-id="d3673-162">La forêt de ressources héberge les applications serveur et une représentation synchronisée de l’objet utilisateur actif, mais elle ne contient pas de comptes d’utilisateur à extension messagerie.</span><span class="sxs-lookup"><span data-stu-id="d3673-162">The resource forest hosts the server applications and a synchronized representation of the active user object, but it does not contain logon-enabled user accounts.</span></span> <span data-ttu-id="d3673-163">La forêt de ressources agit en tant qu’environnement de services partagés pour les autres forêts où résident les objets utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d3673-163">The resource forest acts as a shared services environment for the other forests where user objects reside.</span></span> <span data-ttu-id="d3673-164">Les forêts utilisateur disposent d’une relation d’approbation de niveau forêt avec la forêt de ressources.</span><span class="sxs-lookup"><span data-stu-id="d3673-164">The user forests have a forest-level trust relationship with the resource forest.</span></span> <span data-ttu-id="d3673-165">Lorsque vous déployez Lync Server dans ce type de topologie, vous devez créer un objet utilisateur désactivé dans la forêt de ressources pour chaque compte d’utilisateur dans les forêts utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d3673-165">When you deploy Lync Server in this type of topology, you create one disabled user object in the resource forest for every user account in the user forests.</span></span> <span data-ttu-id="d3673-166">Si Microsoft Exchange est déjà déployé dans la forêt de ressources, il est possible que les comptes d’utilisateurs désactivés existent déjà.</span><span class="sxs-lookup"><span data-stu-id="d3673-166">If Microsoft Exchange is already deployed in the resource forest, the disabled user accounts might already exist.</span></span> <span data-ttu-id="d3673-167">Un produit de synchronisation d’annuaires, tel que MIIS, Microsoft Forefront Identity Manager (FIM) 2010 ou Microsoft Identity Lifecycle Manager (ILM) 2007 Feature Pack 1 (FP1), gère le cycle de vie des comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d3673-167">A directory synchronization product, such as MIIS, Microsoft Forefront Identity Manager (FIM) 2010, or Microsoft Identity Lifecycle Manager (ILM) 2007 Feature Pack 1 (FP1), manages the life cycle of user accounts.</span></span> <span data-ttu-id="d3673-168">Lorsqu’un nouveau compte d’utilisateur est créé dans l’une des forêts utilisateur ou qu’un compte d’utilisateur est supprimé d’une forêt, le produit de synchronisation d’annuaires synchronise la représentation utilisateur correspondante dans la forêt de ressources.</span><span class="sxs-lookup"><span data-stu-id="d3673-168">When a new user account is created in one of the user forests or a user account is deleted from a forest, the directory synchronization product synchronizes the corresponding user representation in the resource forest.</span></span>

<span data-ttu-id="d3673-169">Cette topologie peut être utilisée pour fournir une infrastructure partagée pour les services dans les organisations qui gèrent plusieurs forêts ou pour dissocier l’administration des objets Active Directory d’une autre administration.</span><span class="sxs-lookup"><span data-stu-id="d3673-169">This topology can be used to provide a shared infrastructure for services in organizations that manage multiple forests or to separate the administration of Active Directory objects from other administration.</span></span> <span data-ttu-id="d3673-170">Les sociétés qui ont besoin d’isoler l’administration Active Directory pour des raisons de sécurité choisissent souvent cette topologie.</span><span class="sxs-lookup"><span data-stu-id="d3673-170">Companies that need to isolate Active Directory administration for security reasons often choose this topology.</span></span>

<span data-ttu-id="d3673-171">Cette topologie offre l’avantage de limiter l’extension du schéma Active Directory à une seule forêt (c’est-à-dire la forêt de ressources).</span><span class="sxs-lookup"><span data-stu-id="d3673-171">This topology provides the benefit of limiting the need to extend the Active Directory schema to a single forest (that is, the resource forest).</span></span>

<span data-ttu-id="d3673-172">Le diagramme suivant illustre une topologie de forêt de ressources.</span><span class="sxs-lookup"><span data-stu-id="d3673-172">The following diagram illustrates a resource forest topology.</span></span>

<span data-ttu-id="d3673-173">**Topologie de forêt de ressources**</span><span class="sxs-lookup"><span data-stu-id="d3673-173">**Resource forest topology**</span></span>

<span data-ttu-id="d3673-174">![Topologie de la forêt de ressources Active Directory](images/Gg398173.54ab82f1-e9e5-40f0-a54e-86e340b65c2a(OCS.15).jpg "Topologie de la forêt de ressources Active Directory")</span><span class="sxs-lookup"><span data-stu-id="d3673-174">![Active Directory Resource Forest Topology](images/Gg398173.54ab82f1-e9e5-40f0-a54e-86e340b65c2a(OCS.15).jpg "Active Directory Resource Forest Topology")</span></span>

</div>

<div>

## <a name="multiple-forests-in-a-lync-resource-forest-topology-with-exchange-online"></a><span data-ttu-id="d3673-175">Plusieurs forêts dans une topologie de forêt de ressources Lync avec Exchange Online</span><span class="sxs-lookup"><span data-stu-id="d3673-175">Multiple forests in a Lync resource forest topology with Exchange Online</span></span>

<span data-ttu-id="d3673-176">Dans cette topologie, une ou plusieurs forêts résident en local et sont dédiées à l’hébergement des comptes d’utilisateurs Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d3673-176">In this topology, one or more forests are located on-premises and are dedicated to hosting Active Directory user accounts.</span></span> <span data-ttu-id="d3673-177">La forêt de ressources est située en local et est gérée par un fournisseur d’hébergement tiers.</span><span class="sxs-lookup"><span data-stu-id="d3673-177">The resource forest is located off-premises and is maintained by a third-party hosting provider.</span></span> <span data-ttu-id="d3673-178">La forêt de ressources contient uniquement le déploiement de Lync Server et une réplication synchronisée des comptes d’utilisateurs des forêts de comptes d’utilisateurs locales.</span><span class="sxs-lookup"><span data-stu-id="d3673-178">The resource forest contains only the Lync Server deployment and a synchronized replication of the user accounts from the on-premises user accounts forest(s).</span></span> <span data-ttu-id="d3673-179">Il ne contient pas de comptes d’utilisateur à extension messagerie.</span><span class="sxs-lookup"><span data-stu-id="d3673-179">It does not contain logon-enabled user accounts.</span></span> <span data-ttu-id="d3673-180">Exchange est déployé soit dans les forêts de comptes d’utilisateurs locales intégrées que dans Exchange Online, ou les services de messagerie pour les comptes d’utilisateurs locaux sont fournis uniquement par Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="d3673-180">Exchange is deployed either in the on-premises user account forest(s) integrated along with Exchange Online (Hybrid), or email services for the on-premises user accounts are provided exclusively by Exchange Online.</span></span>

<span data-ttu-id="d3673-181">La forêt de ressources agit en tant qu’environnement de services partagés pour la ou les forêts Active Directory locales où résident les objets utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d3673-181">The resource forest acts as a shared services environment for the on-premises Active Directory forest(s) where user objects reside.</span></span> <span data-ttu-id="d3673-182">La ou les forêts de compte d’utilisateur disposent d’une relation d’approbation de forêt à une façon unique avec la forêt de ressources.</span><span class="sxs-lookup"><span data-stu-id="d3673-182">The user account forest(s) have a one way forest-level trust relationship with the resource forest.</span></span> <span data-ttu-id="d3673-183">Lorsque vous déployez Lync Server dans ce type de topologie, vous devez créer un objet utilisateur désactivé dans la forêt de ressources pour chaque compte d’utilisateur dans les forêts utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d3673-183">When you deploy Lync Server in this type of topology, you create one disabled user object in the resource forest for every user account in the user forests.</span></span> <span data-ttu-id="d3673-184">Un produit de synchronisation d’annuaires, tel que MIIS, Microsoft Forefront Identity Manager (FIM) 2010 ou Microsoft Identity Lifecycle Manager (ILM) 2007 Feature Pack 1 (FP1), gère le cycle de vie des comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d3673-184">A directory synchronization product, such as MIIS, Microsoft Forefront Identity Manager (FIM) 2010, or Microsoft Identity Lifecycle Manager (ILM) 2007 Feature Pack 1 (FP1), manages the life cycle of user accounts.</span></span> <span data-ttu-id="d3673-185">Lorsqu’un nouveau compte d’utilisateur est créé dans l’une des forêts utilisateur ou qu’un compte d’utilisateur est supprimé d’une forêt, le produit de synchronisation d’annuaires synchronise la représentation utilisateur correspondante dans la forêt de ressources.</span><span class="sxs-lookup"><span data-stu-id="d3673-185">When a new user account is created in one of the user forests or a user account is deleted from a forest, the directory synchronization product synchronizes the corresponding user representation in the resource forest.</span></span> <span data-ttu-id="d3673-186">Pour plus d’informations sur la configuration d’un déploiement de forêts multiples, voir [déploiement de Lync dans une architecture à plusieurs forêts (partenaire hébergé sur Lync avec Exchange hybride)](https://go.microsoft.com/fwlink/p/?linkid=513216).</span><span class="sxs-lookup"><span data-stu-id="d3673-186">For more information about configuring a multi-forest deployment, see [Deploying Lync in a Multi-Forest Architecture (Partner Hosted Lync with Exchange Hybrid)](https://go.microsoft.com/fwlink/p/?linkid=513216).</span></span>

<span data-ttu-id="d3673-187"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d3673-187"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

