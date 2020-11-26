---
title: Topologies prises en charge dans Lync Server 2013
description: Topologies prises en charge par Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported topologies
ms:assetid: 3475d430-0394-491b-a09b-ba85bd62be70
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425833(v=OCS.15)
ms:contentKeyID: 48183832
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 39c19577fbda7e377e145abfd473d2cf8e6d4a1a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441430"
---
# <a name="supported-topologies-in-lync-server-2013"></a><span data-ttu-id="d720b-103">Topologies prises en charge dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d720b-103">Supported topologies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d720b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d720b-104">

<span> </span></span></span>

<span data-ttu-id="d720b-105">_**Dernière modification de la rubrique :** 2014-01-14_</span><span class="sxs-lookup"><span data-stu-id="d720b-105">_**Topic Last Modified:** 2014-01-14_</span></span>

<span data-ttu-id="d720b-106">Lync Server 2013 prend en charge le déploiement de sites en local au sein d’une organisation et l’intégration de déploiements sur site à des déploiements Lync Online, un déploiement hybride.</span><span class="sxs-lookup"><span data-stu-id="d720b-106">Lync Server 2013 supports deployment of sites on premises in an organization and integration of on-premises deployments with Lync Online deployments, which is known as a hybrid deployment.</span></span> <span data-ttu-id="d720b-107">Dans un déploiement hybride, certains utilisateurs sont hébergés sur site et certains utilisateurs sont hébergés en ligne.</span><span class="sxs-lookup"><span data-stu-id="d720b-107">In a hybrid deployment, some users are homed on-premises and some users are homed online.</span></span>

<span data-ttu-id="d720b-108">Pour les déploiements sur site, Lync Server 2013 prend en charge le déploiement d’un ou de plusieurs sites qui peuvent être mis à l’échelle afin de répondre aux exigences d’emplacement et de haute disponibilité.</span><span class="sxs-lookup"><span data-stu-id="d720b-108">For on-premises deployments, Lync Server 2013 supports deployment of one or more sites that can be scaled to meet high availability and location requirements.</span></span> <span data-ttu-id="d720b-109">Vous pouvez structurer ces sites et leurs composants conformément aux exigences d’accès et de résilience de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d720b-109">You can structure these sites and their components to meet the access and resiliency requirements of your organization.</span></span>

<span data-ttu-id="d720b-110">Un déploiement local de Lync Server 2013 se compose des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d720b-110">A Lync Server 2013 on-premises deployment consists of the following:</span></span>

  - <span data-ttu-id="d720b-111">Votre déploiement doit inclure au moins un site central (également appelé centre de données).</span><span class="sxs-lookup"><span data-stu-id="d720b-111">Your deployment must include at least one central site (also known as a data center).</span></span> <span data-ttu-id="d720b-112">Chaque site central doit contenir au moins un pool frontal Enterprise Edition ou un serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="d720b-112">Each central site must contain at least one Enterprise Edition Front End pool or one Standard Edition server.</span></span> <span data-ttu-id="d720b-113">Il s’agit des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d720b-113">These consist of the following:</span></span>
    
      - <span data-ttu-id="d720b-114">Pool frontal Enterprise Edition, qui se compose d’un ou de plusieurs serveurs frontaux (en général, au moins deux serveurs frontaux pour l’évolutivité) et d’un serveur principal séparé.</span><span class="sxs-lookup"><span data-stu-id="d720b-114">Enterprise Edition Front End pool, which consists of one or more Front End Servers (typically, at least two Front End Servers for scalability) and a separate Back End Server.</span></span> <span data-ttu-id="d720b-115">Un pool frontal peut contenir un maximum de 12 serveurs frontaux.</span><span class="sxs-lookup"><span data-stu-id="d720b-115">A Front End pool can contain a maximum of twelve Front End Servers.</span></span> <span data-ttu-id="d720b-116">L’équilibrage de charge est requis pour plusieurs serveurs front-end.</span><span class="sxs-lookup"><span data-stu-id="d720b-116">Load balancing is required for multiple Front End Servers.</span></span> <span data-ttu-id="d720b-117">Pour le trafic SIP, nous vous recommandons d’utiliser l’équilibrage de charge DNS, mais l’équilibrage de charge matérielle est également pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d720b-117">For SIP traffic, we recommend DNS load balancing, but hardware load balancing is also supported.</span></span> <span data-ttu-id="d720b-118">Si vous utilisez l’équilibrage de charge DNS pour le trafic SIP, vous avez encore besoin d’un équilibreur de charge matérielle pour le trafic HTTP.</span><span class="sxs-lookup"><span data-stu-id="d720b-118">If you use DNS load balancing for SIP traffic, you still need a hardware load balancer for HTTP traffic.</span></span> <span data-ttu-id="d720b-119">Nous recommandons la mise en miroir SQL Server pour une haute disponibilité des bases de données.</span><span class="sxs-lookup"><span data-stu-id="d720b-119">We recommend SQL Server mirroring for high availability of databases.</span></span> <span data-ttu-id="d720b-120">La base de données principale nécessite une instance distincte, mais vous pouvez collocate la base de données d’archivage, la base de données de surveillance, la base de données de conversation permanente et la base de données de conformité aux conversations permanentes.</span><span class="sxs-lookup"><span data-stu-id="d720b-120">The back-end database requires a separate instance, but you can collocate the archiving database, monitoring database, persistent chat database, and persistent chat compliance database with it.</span></span> <span data-ttu-id="d720b-121">Lync Server 2013 prend en charge l’utilisation d’un cluster partagé pour les partages de fichiers dans votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="d720b-121">Lync Server 2013 supports the use of a shared cluster for the file shares in your deployment.</span></span> <span data-ttu-id="d720b-122">Pour plus d’informations sur les exigences de stockage de base de données, voir [prise en charge de logiciels de base de données dans Lync Server 2013](lync-server-2013-database-software-support.md).</span><span class="sxs-lookup"><span data-stu-id="d720b-122">For details about database storage requirements, see [Database software support in Lync Server 2013](lync-server-2013-database-software-support.md).</span></span> <span data-ttu-id="d720b-123">Pour plus d’informations sur les exigences en matière de stockage de fichiers, voir [prise en charge du stockage de fichiers dans Lync Server 2013](lync-server-2013-file-storage-support.md).</span><span class="sxs-lookup"><span data-stu-id="d720b-123">For details about file storage requirements, see [File storage support in Lync Server 2013](lync-server-2013-file-storage-support.md).</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="d720b-124">Si vous collocate les bases de données Lync Server, nous vous conseillons vivement d’évaluer tous les facteurs susceptibles d’affecter la disponibilité et les performances.</span><span class="sxs-lookup"><span data-stu-id="d720b-124">If you collocate Lync Server databases, we highly recommend assessing all factors that might affect availability and performance.</span></span> <span data-ttu-id="d720b-125">Pour vérifier les capacités de basculement, nous vous recommandons de tester tous les scénarios de basculement.</span><span class="sxs-lookup"><span data-stu-id="d720b-125">To verify failover capabilities, we recommend testing all failover scenarios.</span></span>

        
        </div>
    
      - <span data-ttu-id="d720b-126">Standard Edition Server, qui inclut une base de données SQL Server Express colocalisée.</span><span class="sxs-lookup"><span data-stu-id="d720b-126">Standard Edition server, which includes a collocated SQL Server Express database.</span></span>

  - <span data-ttu-id="d720b-127">Votre déploiement peut également avoir un ou plusieurs sites de succursale associés à un site central.</span><span class="sxs-lookup"><span data-stu-id="d720b-127">Your deployment can also have one or more branch sites associated with a central site.</span></span>

<span data-ttu-id="d720b-128">Cette section décrit les sites et composants d’un déploiement 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d720b-128">This section describes the sites and components of a Lync Server 2013 deployment.</span></span> <span data-ttu-id="d720b-129">Pour plus d’informations sur le site, la topologie et la planification des composants Lync Server 2013, voir [notions de base sur la topologie que vous devez connaître avant de planifier Lync server 2013](lync-server-2013-topology-basics-you-must-know-before-planning.md) et des [topologies de référence dans Lync Server 2013](lync-server-2013-reference-topologies.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="d720b-129">For details about Lync Server 2013 site, topology, and component planning, see [Topology basics you must know before planning for Lync Server 2013](lync-server-2013-topology-basics-you-must-know-before-planning.md) and [Reference topologies in Lync Server 2013](lync-server-2013-reference-topologies.md) in the Planning documentation.</span></span> <span data-ttu-id="d720b-130">Pour plus d’informations sur l’intégration des composants des versions précédentes, voir [les chemins de migration et les scénarios de coexistence pris en charge dans Lync Server 2013](lync-server-2013-supported-migration-paths-and-coexistence-scenarios.md).</span><span class="sxs-lookup"><span data-stu-id="d720b-130">For details about integration of components of previous releases, see [Supported migration paths and coexistence scenarios in Lync Server 2013](lync-server-2013-supported-migration-paths-and-coexistence-scenarios.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d720b-131">Les pools étirés ne sont pas pris en charge pour les rôles serveur frontal, Edge, médiation et directeur.</span><span class="sxs-lookup"><span data-stu-id="d720b-131">Stretched pools are not supported for the Front End, Edge, Mediation, and Director server roles.</span></span>



</div>

<div>

## <a name="central-site-topologies-and-components-on-premises"></a><span data-ttu-id="d720b-132">Topologies et composants de site central (en local)</span><span class="sxs-lookup"><span data-stu-id="d720b-132">Central Site Topologies and Components (On-Premises)</span></span>

<span data-ttu-id="d720b-133">Même si une topologie de site central doit inclure un pool frontal ou un serveur Standard Edition Server standard, chaque site central peut également contenir les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d720b-133">Although a central site topology must include one Front End pool or one Standard Edition server, each central site can also contain the following:</span></span>

  - <span data-ttu-id="d720b-134">Plusieurs listes frontales qui peuvent se trouver dans le même domaine ou dans des domaines différents.</span><span class="sxs-lookup"><span data-stu-id="d720b-134">Multiple Front End pools, which can be in the same domain or different domains.</span></span> <span data-ttu-id="d720b-135">Toutefois, tous les serveurs frontaux dans une liste frontale et le serveur principal pour ce pool doivent se trouver dans le même domaine.</span><span class="sxs-lookup"><span data-stu-id="d720b-135">However, all Front End Servers in a Front End pool, and the Back End Server for that pool, must be in the same domain.</span></span>

  - <span data-ttu-id="d720b-136">Plusieurs serveurs Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="d720b-136">Multiple Standard Edition servers.</span></span>

  - <span data-ttu-id="d720b-137">Office Web Apps Server, qui est utilisé avec les applications Office Web App dans Lync Server 2013 pour gérer le partage et le rendu des présentations Microsoft PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="d720b-137">Office Web Apps Server, which is used with Office Web Applications in Lync Server 2013 to handle the sharing and rendering of Microsoft PowerPoint presentations.</span></span>

  - <span data-ttu-id="d720b-138">Serveur Edge ou pool de périphérie dans votre réseau de périmètre, si vous souhaitez que votre déploiement prenne en charge les partenaires fédérés, la connectivité PIC (Public IM Connectivity), une passerelle de messagerie instantanée, un accès utilisateur à distance, la participation d’utilisateurs anonymes à des réunions ou la messagerie unifiée Exchange (UM).</span><span class="sxs-lookup"><span data-stu-id="d720b-138">Edge Server or Edge pool in your perimeter network, if you want your deployment to support federated partners, public IM connectivity, an extensible messaging and presence protocol (XMPP) gateway, remote user access, participation of anonymous users in meetings, or Exchange Unified Messaging (UM).</span></span> <span data-ttu-id="d720b-139">Vous ne pouvez pas collocate d’autres rôles de serveur avec un serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="d720b-139">You cannot collocate any other server role with an Edge Server.</span></span> <span data-ttu-id="d720b-140">Nous vous recommandons d’utiliser l’équilibrage de charge DNS, le cas échéant, mais l’équilibrage de charge matérielle est également pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d720b-140">We recommend DNS load balancing, where appropriate, but hardware load balancing is also supported.</span></span> <span data-ttu-id="d720b-141">L’interface Edge interne et l’interface Edge externe doivent utiliser le même type d’équilibrage de la charge.</span><span class="sxs-lookup"><span data-stu-id="d720b-141">The internal Edge interface and external Edge interface must use the same type of load balancing.</span></span> <span data-ttu-id="d720b-142">Vous ne pouvez pas utiliser l’équilibrage de la charge DNS sur une interface Edge et l’équilibrage de la charge matérielle sur l’autre interface Edge.</span><span class="sxs-lookup"><span data-stu-id="d720b-142">You cannot use DNS load balancing on one Edge interface and hardware load balancing on the other Edge interface.</span></span> <span data-ttu-id="d720b-143">Pour plus d’informations sur les exigences et la prise en charge de l’équilibrage de charge, voir [planification d’un accès utilisateur externe dans Lync server 2013](lync-server-2013-planning-for-external-user-access.md) dans la documentation de planification et déploiement d’un [accès utilisateur externe dans Lync Server 2013](lync-server-2013-deploying-external-user-access.md) dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="d720b-143">For details about load balancing requirements and support, see [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span></span>

  - <span data-ttu-id="d720b-144">Serveur de médiation ou pool, si vous souhaitez prendre en charge les conférences rendez-vous ou la Conférence rendez-vous dans un pool frontal sur le site central.</span><span class="sxs-lookup"><span data-stu-id="d720b-144">Mediation Server or pool, if you want to support Enterprise Voice or dial-in conferencing in a Front End pool at the central site.</span></span> <span data-ttu-id="d720b-145">En fonction du mode de déploiement de la prise en charge de voix entreprise, vous pouvez collocate le serveur de médiation dans un pool frontal (par défaut) ou déployer un serveur ou un pool de médiation autonome.</span><span class="sxs-lookup"><span data-stu-id="d720b-145">Depending on how you deploy Enterprise Voice support, you can collocate the Mediation Server in a Front End pool (the default) or deploy a stand-alone Mediation Server or pool.</span></span> <span data-ttu-id="d720b-146">Vous pouvez utiliser l’équilibrage de charge DNS, matériel ou de l’application (le cas échéant) pour distribuer le trafic à partir du poste de passerelle d’un pool de serveurs de médiation, y compris une passerelle RTC, un PBX IP ou un contrôle de bordure de session de type SIP Trunk (SBC). Pour plus d’informations sur la planification de la topologie du serveur de médiation appropriée, voir [recommandations de déploiement pour le serveur de médiation dans Lync server 2013](lync-server-2013-deployment-guidelines-for-mediation-server.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="d720b-146">You can use DNS, hardware, or application load balancing (when appropriate) to distribute traffic from a Mediation Server pool’s gateway peer, including a PSTN gateway, IP-PBX, or SIP trunk Session Border Control (SBC).For details about planning the appropriate Mediation Server topology, see [Deployment guidelines for Mediation Server in Lync Server 2013](lync-server-2013-deployment-guidelines-for-mediation-server.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="d720b-147">Serveur de chat permanent, si vous souhaitez que les utilisateurs puissent participer à des conversations à plusieurs sujets, qui persistent dans le temps.</span><span class="sxs-lookup"><span data-stu-id="d720b-147">Persistent Chat Server, if you want to users to be able to participate in multiparty, topic-based conversations that persist over time.</span></span> <span data-ttu-id="d720b-148">Pour offrir plus de capacité et une fiabilité accrue, votre topologie peut inclure plusieurs ordinateurs exécutant une conversation permanente sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="d720b-148">To provide more capacity and increased reliability, your topology can include multiple computers running Persistent Chat Server.</span></span> <span data-ttu-id="d720b-149">Vous ne pouvez pas collocate serveur Chat permanent avec d’autres rôles serveur dans un pool d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="d720b-149">You cannot collocate Persistent Chat Server with other server roles in an Enterprise pool.</span></span> <span data-ttu-id="d720b-150">Toutefois, vous pouvez collocate serveur de chat permanent sur un serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="d720b-150">However, you can collocate Persistent Chat Server on a Standard Edition server.</span></span> <span data-ttu-id="d720b-151">La conversation permanente nécessite une base de données et, si vous implémentez une mise en forme de la conversation persistante, une base de données de conformité de conversation permanente, mais les bases de données peuvent être colocalisées avec la base de données d’archivage, la base de données de surveillance ou sur le serveur principal d’une liste frontale Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="d720b-151">Persistent chat requires a database and, if you implement persistent chat compliance, a persistent chat compliance database, but the databases can be collocated with the Archiving database, Monitoring database, or on the Back End Server of an Enterprise Edition Front End pool.</span></span> <span data-ttu-id="d720b-152">Pour plus d’informations sur la planification de la topologie serveur de chat permanent appropriée, reportez-vous à la section [planification du serveur de chat permanent dans Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="d720b-152">For details about planning the appropriate Persistent Chat Server topology, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="d720b-153">Surveillance, si vous souhaitez prendre en charge la collecte de données pour l’audio et la vidéo de qualité d’appel (QoE) et l’enregistrement des détails des appels (CDR) pour les conférences voix et audiovisuelles dans votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="d720b-153">Monitoring, if you want to support data collection for audio/video Quality of Experience (QoE) and call detail recording (CDR) for Enterprise Voice and A/V conferences in your deployment.</span></span> <span data-ttu-id="d720b-154">Le cas échéant, vous pouvez installer Microsoft System Center Operations Manager (anciennement Microsoft Operations Manager), qui utilise la surveillance des données CDR et QoE pour générer des alertes en temps réel qui indiquent l’état de la fiabilité des appels et de la qualité des médias.</span><span class="sxs-lookup"><span data-stu-id="d720b-154">Optionally, you can install the Microsoft System Center Operations Manager (formerly Microsoft Operations Manager), which uses Monitoring CDR and QoE data to generate near real-time alerts that show the health of call reliability and media quality.</span></span> <span data-ttu-id="d720b-155">Le contrôle, lors de son déploiement, est colocalisé sur des serveurs frontaux ou un serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="d720b-155">Monitoring, when deployed, is collocated on Front End Servers or a Standard Edition server.</span></span> <span data-ttu-id="d720b-156">Le contrôle nécessite une base de données, mais la base de données peut être colocalisée avec la base de données d’archivage, la base de données de chat permanent, la base de données de conformité des conversations permanentles ou sur le serveur principal d’une liste frontale Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="d720b-156">Monitoring requires a database, but the database can be collocated with the Archiving database, persistent chat database, persistent chat compliance database, or on the Back End Server of an Enterprise Edition Front End pool.</span></span>

  - <span data-ttu-id="d720b-157">Archivage, si vous voulez archiver les communications par messagerie instantanée et le contenu de la réunion (pour des raisons de conformité) dans votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="d720b-157">Archiving, if you want to archive IM communications and meeting content (for compliance reasons) in your deployment.</span></span> <span data-ttu-id="d720b-158">L’archivage, lors de son déploiement, est colocalisé sur des serveurs frontaux ou un serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="d720b-158">Archiving, when deployed, is collocated on Front End Servers or a Standard Edition server.</span></span> <span data-ttu-id="d720b-159">Le stockage d’archivage nécessite soit le déploiement d’une base de données d’archivage, soit l’intégration avec le stockage 2013 Exchange.</span><span class="sxs-lookup"><span data-stu-id="d720b-159">Archiving storage requires either deployment of an Archiving database or integration with Exchange 2013 storage.</span></span> <span data-ttu-id="d720b-160">Si vous utilisez les deux, qui est connu sous le nom de *mode mixte*, le stockage Exchange 2013 est utilisé pour stocker les données d’archivage des utilisateurs hébergés sur Exchange 2013 et la base de données d’archivage est utilisée pour archiver des données pour tous les autres utilisateurs de votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="d720b-160">If you use both, which is known as *mixed mode*, Exchange 2013 storage is used to store archive data for users who are homed on Exchange 2013, and the Archiving database is used to archive data for all other users in your deployment.</span></span> <span data-ttu-id="d720b-161">Si vous avez besoin d’une base de données d’archivage, la base de données peut être désactivée sur la base de données de surveillance, la base de données de chat permanent, la base de données de conformité des conversations permanentes ou sur le serveur principal d’un pool frontal.</span><span class="sxs-lookup"><span data-stu-id="d720b-161">If you require an Archiving database, the database can be collocated on the Monitoring database, persistent chat database, persistent chat compliance database, or on the Back End Server of a Front End pool.</span></span> <span data-ttu-id="d720b-162">Pour plus d’informations sur la planification de la topologie de l’archivage appropriée, voir [planification de l’archivage dans Lync Server 2013](lync-server-2013-planning-for-archiving.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="d720b-162">For details about planning the appropriate Archiving topology, see [Planning for Archiving in Lync Server 2013](lync-server-2013-planning-for-archiving.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="d720b-163">Le réalisateur ou le pool de réalisateur, si vous voulez faciliter la résilience et la redirection des requêtes utilisateur de Lync Server 2013 vers le pool de famille de l’utilisateur, qui peut être un pool frontal Enterprise Edition ou un serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="d720b-163">Director or Director pool, if you want to facilitate resiliency and redirection of Lync Server 2013 user requests to the user’s home pool, which can be either an Enterprise Edition Front End pool or a Standard Edition server.</span></span> <span data-ttu-id="d720b-164">Nous vous recommandons de déployer un réalisateur ou un pool de réalisateurs dans chaque site central prenant en charge l’accès des utilisateurs externes et dans chaque site central dans lequel vous déployez une ou plusieurs listes frontales.</span><span class="sxs-lookup"><span data-stu-id="d720b-164">We recommend that you deploy a Director or Director pool in each central site that supports external user access and in each central site in which you deploy one or more Front End pools.</span></span> <span data-ttu-id="d720b-165">Chaque pool de Directors peut contenir un maximum de dix directeurs.</span><span class="sxs-lookup"><span data-stu-id="d720b-165">Each Director pool can contain a maximum of ten Directors.</span></span> <span data-ttu-id="d720b-166">Un Director ne peut pas être colocalisé avec un autre rôle serveur.</span><span class="sxs-lookup"><span data-stu-id="d720b-166">A Director cannot be collocated with any other server role.</span></span> <span data-ttu-id="d720b-167">Pour plus d’informations sur la planification de la topologie de réalisateur appropriée, reportez-vous à [la rubrique scénarios pour le directeur dans Lync Server 2013](lync-server-2013-scenarios-for-the-director.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="d720b-167">For details about planning the appropriate Director topology, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="d720b-168">Le proxy inverse, qui n’est pas un composant Lync Server 2013, est requis si vous souhaitez prendre en charge le partage de contenu Web pour les utilisateurs fédérés ou pour la prise en charge du trafic de mobilité.</span><span class="sxs-lookup"><span data-stu-id="d720b-168">Reverse proxy, which is not a Lync Server 2013 component, but is required if you want to support sharing of web content for federated users or to support Mobility traffic.</span></span> <span data-ttu-id="d720b-169">Vous ne pouvez pas collocate un serveur proxy inverse avec un rôle serveur Lync Server 2013, mais vous pouvez mettre en œuvre la prise en charge du proxy inverse pour un déploiement de Lync Server 2013 en configurant la prise en charge sur un serveur proxy inverse existant de votre organisation qui est utilisé pour d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="d720b-169">You cannot collocate a reverse proxy server with any Lync Server 2013 server role, but you can implement reverse proxy support for a Lync Server 2013 deployment by configuring the support on an existing reverse proxy server in your organization that is used for other applications.</span></span> <span data-ttu-id="d720b-170">Pour plus d’informations sur les serveurs proxy inverse, voir [configuration de serveurs proxy inverse pour Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md) dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="d720b-170">For details about reverse proxy servers, see [Setting up reverse proxy servers for Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md) in the Deployment documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d720b-171">Dans Lync Server 2013, les conférences, la surveillance et l’archivage A/V s’exécutent sur des serveurs frontaux et ne sont plus des rôles de serveur distincts.</span><span class="sxs-lookup"><span data-stu-id="d720b-171">In Lync Server 2013, A/V Conferencing, Monitoring, and Archiving run on Front End Servers and are no longer separate server roles.</span></span>



</div>

<span data-ttu-id="d720b-172">Toutes les listes frontales et les serveurs Standard Edition Server que vous déployez sur un site central partagent l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="d720b-172">All Front End pools and Standard Edition servers that you deploy at a central site share any of the following that you deploy for the central site:</span></span>

  - <span data-ttu-id="d720b-173">Pool de directeurs ou de réalisateurs</span><span class="sxs-lookup"><span data-stu-id="d720b-173">Director or Director pool</span></span>

  - <span data-ttu-id="d720b-174">Serveur de médiation autonome ou pool</span><span class="sxs-lookup"><span data-stu-id="d720b-174">Stand-alone Mediation Server or pool</span></span>

  - <span data-ttu-id="d720b-175">Office Web Apps Server</span><span class="sxs-lookup"><span data-stu-id="d720b-175">Office Web Apps Server</span></span>

  - <span data-ttu-id="d720b-176">Serveur Edge ou pool de bords</span><span class="sxs-lookup"><span data-stu-id="d720b-176">Edge Server or Edge pool</span></span>

  - <span data-ttu-id="d720b-177">Serveur de conversation permanent ou pool</span><span class="sxs-lookup"><span data-stu-id="d720b-177">Persistent Chat Server or pool</span></span>

  - <span data-ttu-id="d720b-178">Surveillance</span><span class="sxs-lookup"><span data-stu-id="d720b-178">Monitoring</span></span>

  - <span data-ttu-id="d720b-179">Archivage</span><span class="sxs-lookup"><span data-stu-id="d720b-179">Archiving</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d720b-180">Il est possible d’implémenter un serveur de messagerie unifiée Exchange avec le déploiement de Lync Server 2013 si vous souhaitez prendre en charge l’intégration de la messagerie unifiée Exchange 2013, mais qu’il ne s’agit pas d’un composant du site Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d720b-180">An Exchange UM Server can be implemented with your Lync Server 2013 deployment if you want to support integration of Exchange 2013 Unified Messaging, but it is not a component of the Lync Server 2013 site.</span></span>



</div>

<span data-ttu-id="d720b-181">Les sites centraux multiples peuvent également partager les éléments suivants du déploiement dans un site central :</span><span class="sxs-lookup"><span data-stu-id="d720b-181">Multiple central sites can also share any of the following that you deploy in one central site:</span></span>

  - <span data-ttu-id="d720b-182">Serveur de médiation autonome ou pool</span><span class="sxs-lookup"><span data-stu-id="d720b-182">Stand-alone Mediation Server or pool</span></span>

  - <span data-ttu-id="d720b-183">Serveur Edge ou pool de bords</span><span class="sxs-lookup"><span data-stu-id="d720b-183">Edge Server or Edge pool</span></span>

  - <span data-ttu-id="d720b-184">Serveur de conversation permanent ou pool</span><span class="sxs-lookup"><span data-stu-id="d720b-184">Persistent Chat Server or pool</span></span>

  - <span data-ttu-id="d720b-185">Archivage</span><span class="sxs-lookup"><span data-stu-id="d720b-185">Archiving</span></span>

  - <span data-ttu-id="d720b-186">Surveillance</span><span class="sxs-lookup"><span data-stu-id="d720b-186">Monitoring</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d720b-187">Il est possible d’implémenter un serveur de messagerie unifiée Exchange avec le déploiement de Lync Server 2013 et partagé par plusieurs sites centraux, mais il ne s’agit pas d’un composant du site 2013 du serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="d720b-187">An Exchange UM Server can be implemented with your Lync Server 2013 deployment and shared by multiple central sites, but it is not a component of the Lync Server 2013 site.</span></span>



</div>

<span data-ttu-id="d720b-188">Pour plus d’informations sur les rôles et les fonctionnalités du serveur Lync Server 2013, voir [rôles de serveur dans Lync Server 2013](lync-server-2013-server-roles.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="d720b-188">For details about Lync Server 2013 server roles and functionality, see [Server roles in Lync Server 2013](lync-server-2013-server-roles.md) in the Planning documentation.</span></span>

<span data-ttu-id="d720b-189">Pour obtenir un résumé de la prise en charge de la prise en charge des serveurs Lync Server 2013, voir [prise en charge des serveurs dans Lync server 2013](lync-server-2013-supported-server-collocation.md).</span><span class="sxs-lookup"><span data-stu-id="d720b-189">For a summary of Lync Server 2013 server collocation support, see [Supported server collocation in Lync Server 2013](lync-server-2013-supported-server-collocation.md).</span></span>

<span data-ttu-id="d720b-190">Outre les rôles de serveur et les fonctionnalités abordés dans cette section, Lync Server 2013 comporte des composants et des options supplémentaires, qui peuvent inclure tout ou partie des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d720b-190">In addition to the server roles and functionality covered previously in this section, Lync Server 2013 has additional components and options, which can include some or all of the following:</span></span>

  - <span data-ttu-id="d720b-191">Pare-feu</span><span class="sxs-lookup"><span data-stu-id="d720b-191">Firewalls</span></span>

  - <span data-ttu-id="d720b-192">Passerelles RTC (si vous déployez Enterprise Voice)</span><span class="sxs-lookup"><span data-stu-id="d720b-192">PSTN gateways (if deploying Enterprise Voice)</span></span>

  - <span data-ttu-id="d720b-193">Serveur de messagerie unifiée Exchange</span><span class="sxs-lookup"><span data-stu-id="d720b-193">Exchange UM Server</span></span>

  - <span data-ttu-id="d720b-194">Équilibrage de charge DNS</span><span class="sxs-lookup"><span data-stu-id="d720b-194">DNS load balancing</span></span>

  - <span data-ttu-id="d720b-195">Programmes d’équilibrage de la charge matérielle</span><span class="sxs-lookup"><span data-stu-id="d720b-195">Hardware load balancers</span></span>

  - <span data-ttu-id="d720b-196">Bases de données SQL Server</span><span class="sxs-lookup"><span data-stu-id="d720b-196">SQL Server databases</span></span>

  - <span data-ttu-id="d720b-197">Partages de fichiers</span><span class="sxs-lookup"><span data-stu-id="d720b-197">File shares</span></span>

<span data-ttu-id="d720b-198">Pour plus d’informations sur l’ensemble des fonctionnalités, composants et options de Lync Server 2013, voir la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="d720b-198">For details about all of the Lync Server 2013 features, components, and options, see the Planning documentation.</span></span>

</div>

<div>

## <a name="branch-site-topologies-and-components-on-premises"></a><span data-ttu-id="d720b-199">Composants et topologies de site de succursale (sur site)</span><span class="sxs-lookup"><span data-stu-id="d720b-199">Branch Site Topologies and Components (On-Premises)</span></span>

<span data-ttu-id="d720b-200">Un site de filiale est associé à un site central et chaque application de succursale Survivable dans un site de filiale est associée à un pool frontal Enterprise Edition ou un serveur Standard Edition Server dans le site central associé.</span><span class="sxs-lookup"><span data-stu-id="d720b-200">A branch site is associated with a central site, and each Survivable Branch Appliance in a branch site is associated with an Enterprise Edition Front End pool or a Standard Edition server in the associated central site.</span></span> <span data-ttu-id="d720b-201">Les sites de succursale dépendent du site central pour la plupart de leurs fonctionnalités, de sorte que les composants d’un site de succursale contiennent uniquement les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d720b-201">Branch sites depend on the central site for most of their functionality, so components at a branch site contain only the following:</span></span>

  - <span data-ttu-id="d720b-202">Une unité de branchement survivant qui combine une passerelle de réseau téléphonique commuté (PSTN) et certaines fonctionnalités de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d720b-202">A Survivable Branch Appliance, which combines a public switched telephone network (PSTN) gateway with some Lync Server functionality.</span></span> <span data-ttu-id="d720b-203">Un serveur de médiation peut être colocalisé avec l’instance du Bureau d’enregistrement sur l’appareil de succursale survivant et vous pouvez déployer un serveur de médiation autonome ou un pool de serveurs de médiation.</span><span class="sxs-lookup"><span data-stu-id="d720b-203">A Mediation Server can be collocated with the instance of the Registrar on the Survivable Branch Appliance, and you can deploy a stand-alone Mediation Server or pool of Mediation Servers.</span></span>

  - <span data-ttu-id="d720b-204">Un serveur de succursales survivant, qui est un serveur exécutant Windows Server sur lequel est installé le logiciel serveur d’inscriptions et de médiation Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d720b-204">A Survivable Branch Server, which is a server running Windows Server that has Lync Server 2013 Registrar and Mediation Server software installed.</span></span>

  - <span data-ttu-id="d720b-205">Passerelle RTC autonome (non incluse dans l’appareil de branchement survivant) et serveur de médiation autonome.</span><span class="sxs-lookup"><span data-stu-id="d720b-205">A stand-alone PSTN gateway (not part of the Survivable Branch Appliance) and a stand-alone Mediation Server.</span></span>

<span data-ttu-id="d720b-206">La configuration requise pour les serveurs de succursales Survivables est la même que celle des rôles serveur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d720b-206">The requirements for Survivable Branch Servers are the same as the requirements for any Lync Server 2013 server role.</span></span>

<span data-ttu-id="d720b-207"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d720b-207"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

