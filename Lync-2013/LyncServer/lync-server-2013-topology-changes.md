---
title: Modifications de la topologie dans Lync Server 2013
description: Modification de la topologie de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Topology changes
ms:assetid: 9e40ef93-9ab0-498c-9bbf-f94584353e53
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688153(v=OCS.15)
ms:contentKeyID: 49733756
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 562766eae939e4510a0d3af20e40b4731c361040
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436229"
---
# <a name="topology-changes-in-lync-server-2013"></a><span data-ttu-id="8b03a-103">Modifications de la topologie dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8b03a-103">Topology changes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8b03a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8b03a-104">

<span> </span></span></span>

<span data-ttu-id="8b03a-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="8b03a-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="8b03a-106">Les exigences et considérations en matière de topologie pour Lync Server 2013 diffèrent de celles des versions précédentes, comme décrit dans cette section.</span><span class="sxs-lookup"><span data-stu-id="8b03a-106">Topology requirements and considerations for Lync Server 2013 are different from those for earlier releases, as described in this section.</span></span>

<div>

## <a name="new-front-end-pools-architecture"></a><span data-ttu-id="8b03a-107">Architecture de pools front-end</span><span class="sxs-lookup"><span data-stu-id="8b03a-107">New Front End Pools Architecture</span></span>

<span data-ttu-id="8b03a-108">Dans Lync Server 2013, l’architecture des pools front-end Enterprise Edition a changé en architecture de systèmes distribués.</span><span class="sxs-lookup"><span data-stu-id="8b03a-108">In Lync Server 2013, the architecture of Enterprise Edition Front End pools has changed to a distributed systems architecture.</span></span>

<span data-ttu-id="8b03a-109">Avec cette nouvelle architecture, la base de données principale n’est plus le magasin de données en temps réel d’un pool.</span><span class="sxs-lookup"><span data-stu-id="8b03a-109">With this new architecture, the Back End database is no longer the real-time data store in a pool.</span></span> <span data-ttu-id="8b03a-110">Les informations relatives à un utilisateur particulier sont conservées sur trois serveurs frontaux de la liste.</span><span class="sxs-lookup"><span data-stu-id="8b03a-110">Information about a particular user is kept on three Front End Servers in the pool.</span></span> <span data-ttu-id="8b03a-111">Pour chaque utilisateur, un serveur frontal fait office de maître des informations de l’utilisateur et deux autres serveurs frontaux servent de réplicas.</span><span class="sxs-lookup"><span data-stu-id="8b03a-111">For each user, one Front End Server acts as the master for that user’s information, and two other Front End Servers serve as replicas.</span></span> <span data-ttu-id="8b03a-112">S’il s’agit d’un serveur frontal, un autre serveur frontal ayant servi de réplica est automatiquement promu maître.</span><span class="sxs-lookup"><span data-stu-id="8b03a-112">If a Front End Server goes down, another Front End Server which served as a replica is automatically promoted to master.</span></span>

<span data-ttu-id="8b03a-113">Cela se produit en coulisses et les administrateurs n’ont pas besoin de savoir quels serveurs frontaux sont les maîtres pour quels utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8b03a-113">This happens behind the scenes, and administrators do not need to know which Front End Servers are the masters for which users.</span></span> <span data-ttu-id="8b03a-114">Cette distribution de stockage de données améliore les performances et l’évolutivité au sein de la liste, et élimine le point de défaillance unique d’un serveur principal unique.</span><span class="sxs-lookup"><span data-stu-id="8b03a-114">This distribution of data storage improves performance and scalability within the pool, and eliminates the single point of failure of a single Back End Server.</span></span>

<span data-ttu-id="8b03a-115">Le serveur principal sert de stockage de sauvegarde pour les données d’utilisateur et de conférence, et il s’agit également du stockage principal pour d’autres bases de données telles que la base de données du groupe de réponse.</span><span class="sxs-lookup"><span data-stu-id="8b03a-115">The Back End Server serves as backup storage for user and conference data, and is also the primary storage for other databases such as the Response Group database.</span></span>

<span data-ttu-id="8b03a-116">Ces améliorations impliquent également la planification et la gestion de vos groupes.</span><span class="sxs-lookup"><span data-stu-id="8b03a-116">These improvements also mean there are changes in how you plan and maintain your pools.</span></span> <span data-ttu-id="8b03a-117">Nous vous recommandons de faire en sorte que toutes les plages frontales de votre entreprise Edition incluent au moins trois serveurs frontaux pour fournir le nombre complet de réplicas pour lesquels l’architecture du pool frontal est conçue.</span><span class="sxs-lookup"><span data-stu-id="8b03a-117">We recommend that all your Enterprise Edition Front End pools include at least three Front End Servers, to provide the full number of replicas that the Front End pool architecture is designed for.</span></span> <span data-ttu-id="8b03a-118">Par ailleurs, vous devez suivre certaines procédures lors de l’ajout de serveurs à un pool frontal, en supprimant des serveurs ou à la mise à niveau de vos serveurs.</span><span class="sxs-lookup"><span data-stu-id="8b03a-118">Additionally, you must follow certain procedures when adding servers to a Front End pool, removing servers from it, or upgrading servers.</span></span> <span data-ttu-id="8b03a-119">Pour plus d’informations, reportez-vous à la rubrique [topologies et composants pour les serveurs frontaux, la messagerie instantanée et la présence dans Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span><span class="sxs-lookup"><span data-stu-id="8b03a-119">For more information, see [Topologies and components for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span></span>

<div>

## <a name="server-role-topology-changes"></a><span data-ttu-id="8b03a-120">Changements de topologie de rôles de serveur</span><span class="sxs-lookup"><span data-stu-id="8b03a-120">Server Role Topology Changes</span></span>

<span data-ttu-id="8b03a-121">Certains rôles de serveur déjà exécutés sur des serveurs distincts sont désormais consolidés dans le rôle serveur frontal, ce qui vous permet de faire des économies sur les coûts liés au matériel.</span><span class="sxs-lookup"><span data-stu-id="8b03a-121">Some server roles that previously ran on separate servers are now consolidated into the Front End Server role, enabling you to save on hardware costs</span></span>

  - <span data-ttu-id="8b03a-122">Dans Lync Server 2013, le serveur de conférence A/V est toujours colocalisé avec le serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="8b03a-122">In Lync Server 2013, A/V Conferencing Server is always collocated with Front End Server.</span></span>

  - <span data-ttu-id="8b03a-123">Les extrémités frontales pour la surveillance et l’archivage sont désormais toujours colocalisées avec le serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="8b03a-123">The front ends for both Monitoring and Archiving are now always collocated with Front End Server.</span></span> <span data-ttu-id="8b03a-124">La surveillance et l’archivage requièrent chaque fois qu’une base de données Back-End séparée, qui peut être désactivée sur le même serveur que la base de données principale du pool frontal, ou qui peut être hébergée sur des serveurs Back-End distincts.</span><span class="sxs-lookup"><span data-stu-id="8b03a-124">Monitoring and Archiving each still require a separate Back-End Database, which can be collocated on the same server as the Front End Pool’s back-end database, or can be hosted on separate Back-End Servers.</span></span>

  - <span data-ttu-id="8b03a-125">Le serveur Chat permanent est désormais un rôle serveur.</span><span class="sxs-lookup"><span data-stu-id="8b03a-125">Persistent Chat Server is now a server role.</span></span> <span data-ttu-id="8b03a-126">Dans Microsoft Lync Server 2010, le serveur de discussion de groupe était une application de confiance tierce pour Microsoft Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="8b03a-126">In Microsoft Lync Server 2010, Group Chat Server was a third-party trusted application for Microsoft Lync Server 2010.</span></span> <span data-ttu-id="8b03a-127">Dans Lync Server 2013, la fonctionnalité de serveur Chat permanent est implémentée en utilisant trois rôles de serveur :</span><span class="sxs-lookup"><span data-stu-id="8b03a-127">In Lync Server 2013, Persistent Chat Server functionality is implemented using three new server roles:</span></span>
    
      - <span data-ttu-id="8b03a-128">**PersistentChatService :** Principaux services serveur de chat permanent implémentés en tant que rôle frontal</span><span class="sxs-lookup"><span data-stu-id="8b03a-128">**PersistentChatService:** Main Persistent Chat Server services implemented as a front end role</span></span>
    
      - <span data-ttu-id="8b03a-129">**PersistentChatStore :** Rôle serveur principal</span><span class="sxs-lookup"><span data-stu-id="8b03a-129">**PersistentChatStore:** Back End Server role</span></span>
    
      - <span data-ttu-id="8b03a-130">**PersistentChatComplianceStore :** Rôle serveur principal pour la conformité de la conversation persistante</span><span class="sxs-lookup"><span data-stu-id="8b03a-130">**PersistentChatComplianceStore:** Back End Server role for Persistent Chat Compliance</span></span>

<span data-ttu-id="8b03a-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8b03a-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

