---
title: 'Lync Server 2013 : Configuration matérielle'
description: 'Lync Server 2013 : configuration matérielle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardware setup
ms:assetid: 37a9f295-cde3-4beb-9a6a-2580082798ab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425852(v=OCS.15)
ms:contentKeyID: 48183834
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e798ce32c1f89bba40ad9245426492b0489e7b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427690"
---
# <a name="hardware-setup-for-lync-server-2013"></a><span data-ttu-id="5dc16-103">Configuration matérielle pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5dc16-103">Hardware setup for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5dc16-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5dc16-104">

<span> </span></span></span>

<span data-ttu-id="5dc16-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="5dc16-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="5dc16-106">Pour configurer le matériel et d’autres composants requis dans l’infrastructure dont vous avez besoin pour implémenter votre topologie, avant de publier votre topologie dans le générateur de topologie, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5dc16-106">Setting up the hardware and other components required in the infrastructure that you need to implement your topology requires that, prior to publishing your topology in Topology Builder, you do the following:</span></span>

  - <span data-ttu-id="5dc16-107">Installez le matériel de chaque composant de la conception topologique que vous avez créé et enregistré à l’aide du générateur de topologie, y compris tous les ordinateurs requis (serveurs exécutant Lync Server 2013, serveurs de base de données, serveurs exécutant Internet Information Services (IIS) et serveurs de proxy (par exemple, serveurs de fichiers).</span><span class="sxs-lookup"><span data-stu-id="5dc16-107">Install the hardware for each component in the topology design that you created and saved by using Topology Builder, including all required computers (servers running Lync Server 2013, database servers, servers running Internet Information Services (IIS), and reverse proxy servers, as appropriate), network adapters, hardware load balancers, and storage devices (such as file servers).</span></span> <span data-ttu-id="5dc16-108">Vérifiez que vous avez suivi les recommandations en matière de nombre et de vitesse pour les cartes réseau.</span><span class="sxs-lookup"><span data-stu-id="5dc16-108">Confirm that you have followed the recommendations for the number and speed for network adapters.</span></span> <span data-ttu-id="5dc16-109">Si vous utilisez des équilibreurs de charge matérielle, assurez-vous que vous disposez des informations appropriées du fournisseur pour les configurer pour une utilisation avec Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5dc16-109">If you will be using hardware load balancers, make sure that you have the proper information from the vendor to configure them for use with Lync Server 2013.</span></span> <span data-ttu-id="5dc16-110">Si vous utilisez un serveur de fichiers ou un autre serveur pour mettre en place le partage de fichiers requis par Lync Server, assurez-vous que le serveur est disponible et qu’il est prêt pour la configuration du partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="5dc16-110">If you will be using a file server or other server to house the file share required by Lync Server, make sure that the server is available and ready for the configuration of the file share.</span></span> <span data-ttu-id="5dc16-111">Pour plus d’informations sur la définition d’une topologie spécifiant les composants nécessaires à votre déploiement, reportez-vous à la rubrique [définition et configuration de la topologie dans Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span><span class="sxs-lookup"><span data-stu-id="5dc16-111">For details about how to define a topology that specifies the components needed for your deployment, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span></span> <span data-ttu-id="5dc16-112">Pour plus d’informations sur la configuration matérielle requise pour les serveurs, voir [matériel compatible pour Lync Server 2013](lync-server-2013-supported-hardware.md) dans la documentation relative à la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5dc16-112">For details about hardware requirements for servers, see [Supported hardware for Lync Server 2013](lync-server-2013-supported-hardware.md) in the Supportability documentation.</span></span>

  - <span data-ttu-id="5dc16-113">Assurez-vous que l’infrastructure réseau répond à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="5dc16-113">Make sure that the networking infrastructure meets requirements.</span></span> <span data-ttu-id="5dc16-114">Pour plus d’informations, voir [Configuration requise pour l’infrastructure réseau pour Lync Server 2013](lync-server-2013-network-infrastructure-requirements.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="5dc16-114">For details, see [Network infrastructure requirements for Lync Server 2013](lync-server-2013-network-infrastructure-requirements.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="5dc16-115">Configurez les services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5dc16-115">Set up Active Directory Domain Services.</span></span> <span data-ttu-id="5dc16-116">La configuration de AD DS inclut la préparation de AD DS et la définition de tous les composants que vous voulez déployer dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="5dc16-116">Setting up AD DS includes preparing AD DS and defining all components that you want to deploy in AD DS.</span></span> <span data-ttu-id="5dc16-117">Pour plus d’informations sur la préparation d’AD DS, voir [préparation des services de domaine Active Directory pour Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md) dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="5dc16-117">For details about preparing AD DS, see [Preparing Active Directory Domain Services for Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md) in the Deployment documentation.</span></span>

  - <span data-ttu-id="5dc16-118">Définissez les autorisations requises pour la création du partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="5dc16-118">Set up the required permissions for creating the file share.</span></span> <span data-ttu-id="5dc16-119">Les autorisations d’utilisation des partages de fichiers par Lync Server 2013 sont automatiquement configurées par le générateur de topologie lors de la publication de votre topologie.</span><span class="sxs-lookup"><span data-stu-id="5dc16-119">Permissions for use of file shares by Lync Server 2013 are automatically configured by Topology Builder when you publish your topology.</span></span> <span data-ttu-id="5dc16-120">Toutefois, le compte d’utilisateur utilisé pour publier la topologie doit avoir le contrôle total (lecture/écriture/modification) sur le partage de fichiers pour permettre au générateur de topologie de configurer les autorisations requises.</span><span class="sxs-lookup"><span data-stu-id="5dc16-120">However, the user account used to publish the topology must have full control (read/write/modify) on the file share in order for Topology Builder to configure the required permissions.</span></span> <span data-ttu-id="5dc16-121">Pour vous assurer que le partage de fichiers peut être géré correctement lors du processus de publication du générateur de topologie, le groupe d’utilisateurs ou de domaines dont l’utilisateur est membre doit être membre du groupe Administrateurs local sur l’ordinateur où se trouve le partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="5dc16-121">To make sure that the file share can be managed properly during the Topology Builder publishing process, the user or domain group that the user is a member of should be made a member of the local Administrators group on the machine where the file share is located.</span></span> <span data-ttu-id="5dc16-122">Dans un scénario multi-domaine, le domaine d’un utilisateur ou d’un groupe doit être membre du groupe Administrateurs local sur l’ordinateur du domaine B où se trouve le partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="5dc16-122">In a multi-domain scenario, Domain A user or group should be made a member of the local Administrators group on the machine in Domain B where the file share will be located.</span></span>
    
    <span data-ttu-id="5dc16-123">Pour plus d’informations sur la mise à jour de l’utilisation des partages de fichiers dans un système de fichiers DFS, voir [configurer le stockage de fichiers pour Lync Server 2013](lync-server-2013-configure-dfs-file-storage.md).</span><span class="sxs-lookup"><span data-stu-id="5dc16-123">For details about updating using file shares in a Distributed File System (DFS), see [Configure file storage for Lync Server 2013](lync-server-2013-configure-dfs-file-storage.md).</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="5dc16-124">Le partage de fichiers pour Lync Server 2013 entreprise Edition ne peut pas être localisé sur le serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="5dc16-124">The file share for Lync Server 2013, Enterprise Edition cannot be located on the Front End Server.</span></span>

    
    </div>

  - <span data-ttu-id="5dc16-125">Installer et configurer l’équilibrage de charge matérielle pour les services Web.</span><span class="sxs-lookup"><span data-stu-id="5dc16-125">Install and set up the hardware load balancer for Web Services.</span></span> <span data-ttu-id="5dc16-126">Après le déploiement de l’équilibrage de charge DNS (Domain Name System), vous devez également utiliser des équilibreurs de charge matérielle pour ces pools, mais uniquement pour le trafic HTTP/HTTPs.</span><span class="sxs-lookup"><span data-stu-id="5dc16-126">With Domain Name System (DNS) load balancing deployed, you still need to also use hardware load balancers for these pools, but only for HTTP/HTTPS traffic.</span></span> <span data-ttu-id="5dc16-127">L’équilibrage de charge matérielle est utilisé pour le trafic HTTPs des clients sur les ports 443 et 80.</span><span class="sxs-lookup"><span data-stu-id="5dc16-127">The hardware load balancer is used for HTTPS traffic from clients over ports 443 and 80.</span></span> <span data-ttu-id="5dc16-128">Même si vous avez encore besoin d’équilibreurs de charge matérielle pour ces pools, leur configuration et leur administration seront essentiellement destinées au trafic HTTP/HTTPs, que les administrateurs des équilibreurs de charge matérielle sont habitués.</span><span class="sxs-lookup"><span data-stu-id="5dc16-128">Although you still need hardware load balancers for these pools, their setup and administration will be primarily for HTTP/HTTPS traffic, which the administrators of the hardware load balancers are accustomed to.</span></span>

<span data-ttu-id="5dc16-129">Une fois toutes les tâches de préparation effectuées comme décrit dans cette rubrique, vous devez également procéder comme suit :</span><span class="sxs-lookup"><span data-stu-id="5dc16-129">After you complete all of the preparation tasks as described in this topic, but prior to publishing the topology, you also need to:</span></span>

  - [<span data-ttu-id="5dc16-130">Installation des systèmes d’exploitaition et des logiciels prérequis sur les serveurs pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5dc16-130">Install operating systems and prerequisite software on servers for Lync Server 2013</span></span>](lync-server-2013-install-operating-systems-and-prerequisite-software-on-servers.md)

  - [<span data-ttu-id="5dc16-131">Configuration des services Internet (IIS) pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5dc16-131">Configure IIS for Lync Server 2013</span></span>](lync-server-2013-configure-iis.md)

  - [<span data-ttu-id="5dc16-132">Configuration de SQL Server pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5dc16-132">Configure SQL Server for Lync Server 2013</span></span>](lync-server-2013-configure-sql-server-for-lync-server.md)

  - [<span data-ttu-id="5dc16-133">Configuration des enregistrements DNS dans Lync Server 2013 pour un pool frontal ou un serveur Standard Edition</span><span class="sxs-lookup"><span data-stu-id="5dc16-133">Configure DNS records in Lync Server 2013 for a Front End pool or Standard Edition server</span></span>](lync-server-2013-configure-dns-records-for-a-front-end-pool-or-standard-edition-server.md)

<span data-ttu-id="5dc16-134"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5dc16-134"></div>

<span> </span>

</div>

</div>

</span></span></div>

