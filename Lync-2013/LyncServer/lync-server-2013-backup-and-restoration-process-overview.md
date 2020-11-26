---
title: Présentation du processus de sauvegarde et de restauration Lync Server 2013
description: 'Présentation de Lync Server 2013 : vue d’ensemble du processus de sauvegarde et de restauration.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backup and restoration process overview
ms:assetid: e0f23b21-070f-4df5-b795-cea2f5338d85
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202192(v=OCS.15)
ms:contentKeyID: 51541524
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 77b833a05021d3a848e9de1ee8768f7daa194c6a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437993"
---
# <a name="backup-and-restoration-process-overview-for-lync-server-2013"></a><span data-ttu-id="dbae1-103">Présentation du processus de sauvegarde et de restauration pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dbae1-103">Backup and restoration process overview for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dbae1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dbae1-104">

<span> </span></span></span>

<span data-ttu-id="dbae1-105">_**Dernière modification de la rubrique :** 2013-03-26_</span><span class="sxs-lookup"><span data-stu-id="dbae1-105">_**Topic Last Modified:** 2013-03-26_</span></span>

<span data-ttu-id="dbae1-106">Cette section fournit une vue d’ensemble du fonctionnement du processus de sauvegarde et de restauration pour Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dbae1-106">This section provides an overview of how the backup and restoration process works for Lync Server 2013.</span></span> <span data-ttu-id="dbae1-107">Vous utilisez le même processus pour tous les serveurs Standard Edition Server et les serveurs Enterprise Edition, quel que soit leur emplacement.</span><span class="sxs-lookup"><span data-stu-id="dbae1-107">You use the same process for all Standard Edition servers and Enterprise Edition servers, regardless of their location.</span></span>

<span data-ttu-id="dbae1-108">En règle générale, le processus de sauvegarde fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="dbae1-108">In general, the backup process works as follows:</span></span>

  - <span data-ttu-id="dbae1-109">Vous pouvez créer un emplacement de sauvegarde en tant que dossier partagé sur un ordinateur autonome qui ne fait pas partie d’un pool.</span><span class="sxs-lookup"><span data-stu-id="dbae1-109">You create a backup location as a shared folder on a stand-alone computer that is not part of any pool.</span></span> <span data-ttu-id="dbae1-110">L’emplacement de la sauvegarde est référencé dans **$Backup**.</span><span class="sxs-lookup"><span data-stu-id="dbae1-110">The location of the backup is referenced in **$Backup**.</span></span>

  - <span data-ttu-id="dbae1-111">D’un point de vue régulier, vous sauvegardez toutes les bases de données du serveur Lync et tous les magasins de fichiers décrits dans les [exigences de sauvegarde et de restauration de Lync server 2013 : données](lync-server-2013-backup-and-restoration-requirements-data.md) en suivant les procédures décrites dans la rubrique [sauvegarde de Lync Server 2013](lync-server-2013-backing-up-lync-server.md) le centre de gestion central inclut tous les paramètres et configurations du serveur.</span><span class="sxs-lookup"><span data-stu-id="dbae1-111">On a regular, scheduled basis, you back up all the Lync Server databases and all the file stores that are described in [Backup and restoration requirements in Lync Server 2013: data](lync-server-2013-backup-and-restoration-requirements-data.md) by following the procedures described in [Backing up Lync Server 2013](lync-server-2013-backing-up-lync-server.md) The Central Management store includes all the server settings and configurations.</span></span>

  - <span data-ttu-id="dbae1-112">Chaque fois que vous exécutez une sauvegarde ultérieure, vous devez créer un dossier partagé et changer le chemin d’accès **$Backup** références.</span><span class="sxs-lookup"><span data-stu-id="dbae1-112">Each time you run a subsequent backup, you create a new shared folder and change the path that **$Backup** references.</span></span>

<span data-ttu-id="dbae1-113">En règle générale, le processus de restauration fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="dbae1-113">In general, the restoration process works as follows:</span></span>

  - <span data-ttu-id="dbae1-114">Dans le cas d’une panne ou d’une panne, vous restaurez les données à l’emplacement référencé par **$Backup** sur des ordinateurs nouveaux ou sains.</span><span class="sxs-lookup"><span data-stu-id="dbae1-114">When a failure or outage occurs, you restore the data in the location referenced by **$Backup** to new or clean computers.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="dbae1-115">Ce processus de restauration ne restaure pas les données sur un État serveur existant.</span><span class="sxs-lookup"><span data-stu-id="dbae1-115">This restoration process does not restore data onto an existing server state.</span></span> <span data-ttu-id="dbae1-116">Autrement dit, ce processus nécessite une nouvelle installation du serveur.</span><span class="sxs-lookup"><span data-stu-id="dbae1-116">That is, this process requires that the server is clean or new.</span></span>

    
    </div>

  - <span data-ttu-id="dbae1-117">Pour permettre à l’utilisateur et aux informations de votre conférence d’être récupérable au point de défaillance, vous pouvez implémenter une topologie de récupération d’urgence avec des pools frontaux couplés, comme décrit dans la section [planification de la haute disponibilité et reprise après sinistre dans Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="dbae1-117">To enable your user and conference information to be recoverable to the point of failure, you can implement a disaster recovery topology with paired Front End pools, as described in [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span>

  - <span data-ttu-id="dbae1-118">La configuration de votre système de noms de domaine (DNS), de la configuration du protocole DHCP (Dynamic Host Configuration Protocol), des noms de domaine, des noms de domaine complets de l’ordinateur (FQDN), des chemins d’accès au magasin de fichiers, etc. doivent être identiques au moment de la restauration.</span><span class="sxs-lookup"><span data-stu-id="dbae1-118">All Domain Name System (DNS) configuration, Dynamic Host Configuration Protocol (DHCP) configuration, domain names, computer fully qualified domain names (FQDNs), file store paths, and so on must be the same at the time of restoration that they were at the time of back up.</span></span>

<span data-ttu-id="dbae1-119">Si un serveur exécutant Lync Server tombe en panne, la récupération inclut les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbae1-119">If a server running Lync Server fails, recovery includes the following steps:</span></span>

  - <span data-ttu-id="dbae1-120">Installez le système d’exploitation sur un nouvel ordinateur ou un ordinateur qui a le même nom de domaine complet que l’ordinateur en panne.</span><span class="sxs-lookup"><span data-stu-id="dbae1-120">Install the operating system on a new or clean computer with the same FQDN as the failed computer.</span></span>

  - <span data-ttu-id="dbae1-121">Réinstallez les certificats.</span><span class="sxs-lookup"><span data-stu-id="dbae1-121">Reinstall certificates.</span></span>

  - <span data-ttu-id="dbae1-122">Si le serveur a hébergé une base de données, installez Microsoft SQL Server 2012 ou Microsoft SQL Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="dbae1-122">If the server hosted a database, install Microsoft SQL Server 2012 or Microsoft SQL Server 2008 R2.</span></span>

  - <span data-ttu-id="dbae1-123">En règle générale, si le serveur a hébergé une base de données, exécutez le générateur de topologie pour créer et installer la base de données et configurer les listes de contrôle d’accès (ACL).</span><span class="sxs-lookup"><span data-stu-id="dbae1-123">In general, if the server hosted a database, run Topology Builder to create and install the database and set up access control lists (ACLs).</span></span>

  - <span data-ttu-id="dbae1-124">En règle générale, si le serveur héberge un rôle serveur, exécutez les étapes 1 à 4 de l’Assistant Déploiement de Lync Server pour installer les fichiers de configuration locaux, installer les composants du rôle de serveur, attribuer des certificats et démarrer les services.</span><span class="sxs-lookup"><span data-stu-id="dbae1-124">In general, if the server hosted a server role, run step 1 through step 4 of the Lync Server Deployment Wizard to install the local configuration files, install the server role components, assign certificates, and start the services.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="dbae1-125">Si le serveur a hébergé une base de données avec le rôle serveur, l’exécution de l’étape 2 de l’Assistant Déploiement de Lync Server recrée la base de données.</span><span class="sxs-lookup"><span data-stu-id="dbae1-125">If the server hosted a database collocated with the server role, running step 2 of the Lync Server Deployment Wizard recreates the database.</span></span>

    
    </div>

  - <span data-ttu-id="dbae1-126">Si le serveur a hébergé une base de données, restaurez les données sauvegardées.</span><span class="sxs-lookup"><span data-stu-id="dbae1-126">If the server hosted a database, restore the backed up data.</span></span>

<span data-ttu-id="dbae1-127"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dbae1-127"></div>

<span> </span>

</div>

</div>

</span></span></div>

