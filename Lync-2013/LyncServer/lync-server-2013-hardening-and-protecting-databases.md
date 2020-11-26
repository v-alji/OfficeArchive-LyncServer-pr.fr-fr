---
title: 'Lync Server 2013 : renforcement et protection des bases de données'
description: 'Lync Server 2013 : renforcer et protéger des bases de données.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardening and protecting the databases of Lync Server 2013
ms:assetid: 6953e721-3511-4235-b848-51bab093dc89
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518330(v=OCS.15)
ms:contentKeyID: 62625490
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af1ed8f54384e8ecac3b1e4ce6a4253a10bcc2c6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427760"
---
# <a name="hardening-and-protecting-the-databases-of-lync-server-2013"></a><span data-ttu-id="34927-103">Renforcement et protection des bases de données de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="34927-103">Hardening and protecting the databases of Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="34927-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="34927-104">

<span> </span></span></span>

<span data-ttu-id="34927-105">_**Dernière modification de la rubrique :** 2013-12-05_</span><span class="sxs-lookup"><span data-stu-id="34927-105">_**Topic Last Modified:** 2013-12-05_</span></span>

<span data-ttu-id="34927-106">Microsoft Lync Server 2013 dépend également de bases de données SQL Server pour le stockage des informations utilisateur, de l’état de conférences, des données d’archivage et des enregistrements des détails des appels.</span><span class="sxs-lookup"><span data-stu-id="34927-106">Microsoft Lync Server 2013 also depends on SQL Server databases for storing user information, conference state, archiving data, and Call Detail Records (CDRs).</span></span> <span data-ttu-id="34927-107">Vous pouvez optimiser la disponibilité des données Lync Server 2013 sur les bases de données principales de Lync Server en partitionnant les données d’application d’une façon qui améliore la tolérance de panne et simplifie la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="34927-107">You can maximize the availability of Lync Server 2013 data on Lync Server back-end databases, by partitioning the application data in a way that improves fault tolerance and simplifies troubleshooting.</span></span> <span data-ttu-id="34927-108">Pour ce faire, vous pouvez partitionner les données d’application de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="34927-108">To achieve these goals, partition the application data by:</span></span>

  - <span data-ttu-id="34927-109">Recommandations **en matière de partitions de serveur**   Séparez les fichiers de votre système d’exploitation, application et programme de vos fichiers de données.</span><span class="sxs-lookup"><span data-stu-id="34927-109">**Using server partitioning best practices**   Separate your operating system, application, and program files from your data files.</span></span>

  - <span data-ttu-id="34927-110">**Stockage de fichiers journaux de transactions et de fichiers de base de données**   Stockez ces fichiers séparément pour améliorer la tolérance de pannes et optimiser la récupération, et stockez-les sur un disque ou un volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="34927-110">**Storing transaction log files and database files**   Store these files separately to increase fault tolerance and optimize recovery, and store them on an encrypted disk or volume.</span></span>

  - <span data-ttu-id="34927-111">**Utiliser la mise en cluster de serveurs**   Groupez les serveurs principaux pour optimiser la disponibilité du système Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="34927-111">**Using server clustering**   Cluster the back-end servers to optimize Lync Server 2013 system availability.</span></span>

  - <span data-ttu-id="34927-112">**Assurez-vous que toutes les sauvegardes de données sont chiffrées et correctement gérées**   Les médias de sauvegarde perdus, supprimés ou déplacés peuvent constituer une menace significative pour la sécurité des données pour les déploiements de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="34927-112">**Ensure that all data backups are encrypted and properly handled**   Lost, discarded, or misplaced backup media can pose a significant threat to data security for Lync Server 2013 deployments</span></span>

<span data-ttu-id="34927-113">Sur tout serveur Lync Server 2013, à l’exception de Standard Edition Server, l’instance SQL Server Express (instance RTCLOCAL) n’est pas accessible à distance et aucune exception de pare-feu local n’est créée, à l’exception de SQL Server Express sur un serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="34927-113">On any Lync Server 2013 server except Standard Edition server, the SQL Server Express instance (RTCLOCAL instance) is not remotely accessible, and no local firewall exceptions are created, except for SQL Server Express on a Standard Edition server.</span></span> <span data-ttu-id="34927-114">Sur un serveur Standard Edition Server, la base de données principale et la Banque centrale de gestion (CMS) sont configurées pour être accessibles à distance.</span><span class="sxs-lookup"><span data-stu-id="34927-114">On a Standard Edition server, both the back-end database and the Central Management store (CMS) are set up to be remotely accessible.</span></span> <span data-ttu-id="34927-115">Pour renforcer les bases de données SQL Server, vous pouvez procéder comme suit :</span><span class="sxs-lookup"><span data-stu-id="34927-115">To harden SQL Server databases, you can do the following:</span></span>

  - <span data-ttu-id="34927-116">Personnalisez le pare-feu SQL Server Express sur les serveurs Standard Edition afin de limiter l’étendue des serveurs qui peuvent accéder à distance à la base de données.</span><span class="sxs-lookup"><span data-stu-id="34927-116">Customize the SQL Server Express firewall on Standard Edition servers, limiting the scope of servers that can remotely access the database.</span></span> <span data-ttu-id="34927-117">Par défaut, toute adresse IP peut accéder à distance à la base de données.</span><span class="sxs-lookup"><span data-stu-id="34927-117">By default, any IP address can remotely access the database.</span></span>

  - <span data-ttu-id="34927-118">Utilisez SQL Server Configuration Manager pour spécifier les protocoles, adresses IP et ports pour l’accès distant SQL Server :</span><span class="sxs-lookup"><span data-stu-id="34927-118">Use SQL Server Configuration Manager to specify the protocols, IP addresses, and ports for SQL Server remote access:</span></span>
    
      - <span data-ttu-id="34927-119">Lync Server 2013 utilise le protocole TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="34927-119">Lync Server 2013 uses the TCP/IP protocol.</span></span> <span data-ttu-id="34927-120">Il prend en charge le protocole IP version 4 (IPv4), mais pas le protocole IP version 6 (IPv6).</span><span class="sxs-lookup"><span data-stu-id="34927-120">It supports IP version 4 (IPv4), but not IP version 6 (IPv6).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="34927-121">Lync Server 2013 peut fonctionner dans un réseau doté d’une pile IP double activée.</span><span class="sxs-lookup"><span data-stu-id="34927-121">Lync Server 2013 can function in a network with dual IP stack enabled.</span></span>

        
        </div>
    
      - <span data-ttu-id="34927-122">Lync Server 2013 prend en charge plusieurs adresses IP (cartes d’adresses réseau multi-résidentes).</span><span class="sxs-lookup"><span data-stu-id="34927-122">Lync Server 2013 supports multiple IP address (multi-homed network address cards).</span></span> <span data-ttu-id="34927-123">Vous pouvez spécifier que SQL Server écoute uniquement les adresses IP spécifiques (adresse individuelle ou sous-réseau) et utiliser des protocoles spécifiques uniquement.</span><span class="sxs-lookup"><span data-stu-id="34927-123">You can specify that SQL Server listen only to specific IP addresses (individual address or by subnet) and only use specific protocols.</span></span>
    
      - <span data-ttu-id="34927-124">Lync Server 2013 prend en charge les ports SQL Server statiques et dynamiques.</span><span class="sxs-lookup"><span data-stu-id="34927-124">Lync Server 2013 supports static and dynamic SQL Server ports.</span></span>

  - <span data-ttu-id="34927-125">Exécutez SQL Server sur un port statique (non défini par défaut) et n’exécutez pas le navigateur SQL Server (de sorte qu’il ne puisse pas signaler le port d’écoute au client).</span><span class="sxs-lookup"><span data-stu-id="34927-125">Run SQL Server on a static (non-default) port, and do not run SQL Server Browser (so it cannot report the listening port to the client).</span></span> <span data-ttu-id="34927-126">Pour cela, il est nécessaire de disposer d’une configuration personnalisée sur chaque client SQL Server, y compris sur les serveurs frontaux, le serveur de surveillance, le serveur d’archivage et les consoles d’administration (exécutant Lync Server Management Shell, le panneau de configuration de Lync Server ou le générateur de topologie) et tous les autres serveurs exécutant des bases de données Lync Server.</span><span class="sxs-lookup"><span data-stu-id="34927-126">This requires a custom configuration on each SQL Server client, including Front End Servers, Monitoring Server, Archiving Server, and administrative consoles (running Lync Server Management Shell, Lync Server Control Panel, or Topology Builder), and all other servers running Lync Server databases).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="34927-127">L’accès aux bases de données doit être limité aux administrateurs de base de données approuvés.</span><span class="sxs-lookup"><span data-stu-id="34927-127">Access to databases must be limited to trusted database administrators.</span></span> <span data-ttu-id="34927-128">Un administrateur de base de données malveillant a pu insérer ou modifier des données dans les bases de données pour obtenir des privilèges sur les serveurs Lync Server 2013 ou obtenir des informations sensibles de ces services, même si l’administrateur de la base de données n’a pas reçu un accès direct ou le contrôle des serveurs 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="34927-128">A malicious database administrator could insert or modify data into the databases to acquire privileges over the Lync Server 2013 servers or obtain sensitive information from the services, even if the database administrator has not been granted direct access or control of the Lync Server 2013 servers.</span></span>



</div>

<span data-ttu-id="34927-129">Pour plus d’informations sur les configurations personnalisées et le renforcement de bases de données SQL Server, voir l’article de blog NextHop intitulé « utilisation de Lync Server 2010 avec une configuration réseau SQL Server personnalisée » [https://go.microsoft.com/fwlink/p/?LinkId=214008](https://go.microsoft.com/fwlink/p/?linkid=214008) .</span><span class="sxs-lookup"><span data-stu-id="34927-129">For details about custom configurations and hardening SQL Server databases, see the NextHop blog article, "Using Lync Server 2010 with a Custom SQL Server Network Configuration," at [https://go.microsoft.com/fwlink/p/?LinkId=214008](https://go.microsoft.com/fwlink/p/?linkid=214008).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="34927-130">Vous pouvez également renforcer la protection des serveurs d’applications et des systèmes d’exploitation, mais vous pouvez utiliser une stratégie de groupe pour mettre en œuvre les verrouillages de sécurité dans le déploiement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="34927-130">You can also harden operating systems and applications servers, and you can use Group Policy to implement security lockdowns in your Lync Server deployment.</span></span> <span data-ttu-id="34927-131">Pour plus d’informations, reportez-vous à la rubrique <A href="lync-server-2013-hardening-and-protecting-servers-and-applications.md">renforcement et protection des serveurs et applications pour Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="34927-131">For details, see <A href="lync-server-2013-hardening-and-protecting-servers-and-applications.md">Hardening and protecting servers and applications for Lync Server 2013</A>.</span></span>



<span data-ttu-id="34927-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="34927-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

