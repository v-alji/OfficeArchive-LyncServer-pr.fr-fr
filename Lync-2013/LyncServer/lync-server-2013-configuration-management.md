---
title: 'Lync Server 2013 : gestion de la configuration'
description: 'Lync Server 2013 : gestion de la configuration.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration management
ms:assetid: 00ea1196-cb40-427f-99a4-5e8037cbf367
ms:mtpsurl: https://technet.microsoft.com/library/Dn720316(v=OCS.15)
ms:contentKeyID: 63969570
ms.date: 05/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5999708811cc4a34cf846a1ddd481ba38e07c62
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434248"
---
# <a name="configuration-management-in-lync-server-2013"></a><span data-ttu-id="614bb-103">Gestion de la configuration dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="614bb-103">Configuration management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="614bb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="614bb-104">

<span> </span></span></span>

<span data-ttu-id="614bb-105">_**Dernière modification de la rubrique :** 2015-05-15_</span><span class="sxs-lookup"><span data-stu-id="614bb-105">_**Topic Last Modified:** 2015-05-15_</span></span>

<span data-ttu-id="614bb-106">La gestion de la configuration est le processus d’enregistrement et de suivi des ressources matérielles et logicielles, ainsi que des informations sur la configuration du système.</span><span class="sxs-lookup"><span data-stu-id="614bb-106">Configuration management is the process of recording and tracking hardware and software assets and system configuration information.</span></span> <span data-ttu-id="614bb-107">Il est généralement utilisé pour effectuer le suivi des licences logicielles, de mettre à jour une build matérielle et logicielle standard pour les ordinateurs et serveurs clients et de définir des normes d’appellation pour les nouveaux ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="614bb-107">It is generally used to track software licenses, maintain a standard hardware and software build for client computers and servers, and define naming standards for new computers.</span></span> <span data-ttu-id="614bb-108">La gestion de la configuration couvre généralement les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="614bb-108">Configuration management generally covers the following categories:</span></span>

  - <span data-ttu-id="614bb-109">**Matériel**   Cette catégorie effectue le suivi des pièces d’équipement dont dispose l’organisation informatique, l’endroit où se trouve l’équipement et qui utilise des équipements.</span><span class="sxs-lookup"><span data-stu-id="614bb-109">**Hardware**   This category tracks the pieces of equipment that the IT organization owns, where equipment is located, and who uses equipment.</span></span> <span data-ttu-id="614bb-110">Grâce à ces informations, une organisation est en mesure de planifier et de budgétiser les mises à jour, de mettre à jour les builds matérielles standard, de signaler la valeur des ressources informatiques à des fins comptables et d’éviter le vol.</span><span class="sxs-lookup"><span data-stu-id="614bb-110">This information enables an organization to plan and budget for upgrades, maintain standard hardware builds, report on the value of IT assets for accounting purposes, and help prevent theft.</span></span>

  - <span data-ttu-id="614bb-111">Le **logiciel** ;   Cette catégorie effectue le suivi des logiciels installés sur chaque ordinateur, des numéros de version et de l’emplacement des licences.</span><span class="sxs-lookup"><span data-stu-id="614bb-111">**Software**   This category tracks software that is installed on each computer, the version numbers, and where the licenses are held.</span></span> <span data-ttu-id="614bb-112">Ces informations permettent de planifier les mises à niveau, de garantir que le logiciel est concédé sous licence et de détecter la présence de logiciels non autorisés (et sans licence).</span><span class="sxs-lookup"><span data-stu-id="614bb-112">This information helps plan upgrades, to ensure that software is licensed, and detect the presence of unauthorized (and unlicensed) software.</span></span>

  - <span data-ttu-id="614bb-113">**Builds standard**   Cette catégorie effectue le suivi de la build standard actuelle pour les ordinateurs et serveurs clients, et si les ordinateurs et serveurs clients répondent à cette norme.</span><span class="sxs-lookup"><span data-stu-id="614bb-113">**Standard Builds**   This category tracks the current standard build for the client computers and servers and whether the client computers and servers meet this standard.</span></span> <span data-ttu-id="614bb-114">La définition et l’application des builds standard permettent de soutenir le personnel, car le personnel est tenu de ne conserver qu’un nombre limité de versions de chaque logiciel.</span><span class="sxs-lookup"><span data-stu-id="614bb-114">Defining and enforcing standard builds helps support staff because the staff is required to maintain only a limited number of versions of each piece of software.</span></span>

  - <span data-ttu-id="614bb-115">**Mises à jour cumulées et correctifs**   Cette catégorie suit les service packs testés et approuvés pour une utilisation et les ordinateurs à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="614bb-115">**Cumulative Updates and Hotfixes**   This category tracks which service packs are tested and approved for use and which computers are up to date.</span></span> <span data-ttu-id="614bb-116">Ces informations sont importantes pour réduire le risque d’intrusion sur des ordinateurs et de détecter les utilisateurs qui ont installé des mises à jour non approuvées.</span><span class="sxs-lookup"><span data-stu-id="614bb-116">This information is important to reduce the risk of computers being compromised and to detect users who have installed unapproved updates.</span></span>

  - <span data-ttu-id="614bb-117">**Informations de configuration du système**   Cette catégorie effectue le suivi de la fonction d’un système, de l’interaction entre les éléments système et des processus qui dépendent d’un système qui s’exécute correctement.</span><span class="sxs-lookup"><span data-stu-id="614bb-117">**System Configuration Information**   This category tracks the function of a system, the interaction between system elements, and the processes that depend on a system that is running smoothly.</span></span> <span data-ttu-id="614bb-118">Par exemple, un serveur proxy tiers est configuré sur un serveur unique.</span><span class="sxs-lookup"><span data-stu-id="614bb-118">For example, third-party proxy server may be configured on a single server.</span></span> <span data-ttu-id="614bb-119">La dépendance du serveur proxy sur ce serveur doit être comprise et les plans d’urgence peuvent être requis en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="614bb-119">The proxy server’s dependence on this server should be understood and contingency plans may be required if there is a failure.</span></span> <span data-ttu-id="614bb-120">Si le serveur proxy peut être configuré pour communiquer avec un autre serveur frontal, les dépendances et les plans d’urgence seront probablement modifiés.</span><span class="sxs-lookup"><span data-stu-id="614bb-120">If the proxy server can be configured to also communicate with another front-end server, dependencies and contingency plans will probably change.</span></span>

<div>

## <a name="implementing-configuration-management"></a><span data-ttu-id="614bb-121">Mise en œuvre de la gestion de la configuration</span><span class="sxs-lookup"><span data-stu-id="614bb-121">Implementing configuration management</span></span>

<span data-ttu-id="614bb-122">Lorsque vous déterminez les éléments qui doivent être gérés, implémentez la gestion de la configuration en collectant des données et en rapportant des données.</span><span class="sxs-lookup"><span data-stu-id="614bb-122">After you determine what items need managing, implement configuration management by collecting data and reporting data.</span></span> <span data-ttu-id="614bb-123">Pour les petites entreprises, l’approche la plus simple consiste à collecter les données manuellement (nombre et modèle d’ordinateurs clients, de systèmes d’exploitation, de logiciels installés) et de les enregistrer dans un document Office Word ou Office Excel.</span><span class="sxs-lookup"><span data-stu-id="614bb-123">The simplest approach for small organizations is to collect data manually (number and model of client computers, operating system, installed software) and save it in an Office Word or Office Excel document.</span></span> <span data-ttu-id="614bb-124">Pour les systèmes plus volumineux, plus complexes et en perpétuelle évolution, la découverte des ressources et la collecte des informations détaillées doit être automatisée.</span><span class="sxs-lookup"><span data-stu-id="614bb-124">For larger, more complex, and constantly changing systems, the discovery of assets and collection of detailed information must be automated.</span></span> <span data-ttu-id="614bb-125">Déterminez les informations pertinentes pour votre organisation et enregistrez-les dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="614bb-125">Decide what information is relevant to your organization and record it in a database.</span></span>

<span data-ttu-id="614bb-126">La base de données de gestion de la configuration est un outil utile pour le personnel d’assistance et la gestion des domaines suivants :</span><span class="sxs-lookup"><span data-stu-id="614bb-126">The configuration management database is a useful tool for support staff and management in the following areas:</span></span>

  - <span data-ttu-id="614bb-127">**Audits de sécurité**   La base de données vous permet d’identifier les serveurs exécutant Lync Server et les systèmes d’ordinateur client pour lesquels il est nécessaire d’appliquer des correctifs ou qui n’ont pas pu installer un service pack ou les dernières mises à jour antivirus.</span><span class="sxs-lookup"><span data-stu-id="614bb-127">**Security Audits**   The database enables you to identify servers that are running Lync Server and client computer systems that must have hotfixes applied or that have missed the installation of a service pack or the latest antivirus updates.</span></span>

  - <span data-ttu-id="614bb-128">**Installation de logiciels**   Identifier les versions des logiciels clients et en assurer le suivi permet aux administrateurs de planifier les mises à jour de la version et de nouvelles installations, et en vous aidant également à la documentation et à la conformité des licences.</span><span class="sxs-lookup"><span data-stu-id="614bb-128">**Software Installation**   Identifying client software versions and tracking them will aid administrators in planning version updates and new installs and also by helping with licensing documentation and compliance.</span></span>

  - <span data-ttu-id="614bb-129">**Informations de configuration**   Si vous conservez une liste à jour de tous les paramètres qui ont été modifiés par défaut, vous serez en mesure de résoudre les problèmes de manière rapide et efficace.</span><span class="sxs-lookup"><span data-stu-id="614bb-129">**Configuration Information**   If you maintain an up-to-date list of all settings that were changed from their default, then you'll be able to troubleshoot issues quickly and more effectively.</span></span>

  - <span data-ttu-id="614bb-130">**Planification des mises à niveau**   Si un avis de capacité révèle que de l’espace de stockage supplémentaire est requis sur votre serveur de base de données Lync, il est important de savoir si chaque serveur possède un contrôleur RAID interne.</span><span class="sxs-lookup"><span data-stu-id="614bb-130">**Planning Upgrades**   If a capacity review reveals that additional storage space is required on your Lync database servers, it’s important to know whether each server has an internal RAID controller.</span></span> <span data-ttu-id="614bb-131">Si tel est le cas, sont-ils le même modèle ?</span><span class="sxs-lookup"><span data-stu-id="614bb-131">If they do, then are they the same model?</span></span> <span data-ttu-id="614bb-132">Est-ce que le nombre de disques est déjà installé ?</span><span class="sxs-lookup"><span data-stu-id="614bb-132">Do they have the same number of disks installed?</span></span> <span data-ttu-id="614bb-133">La base de données de gestion de la configuration indique le type de disque qui peut être installé, le numéro et le chemin de mise à niveau dans chaque cas.</span><span class="sxs-lookup"><span data-stu-id="614bb-133">The configuration management database will indicate the type of disk that can be installed, the number, and the upgrade path in each case.</span></span>

</div>

<div>

## <a name="tools-used-for-configuration-management"></a><span data-ttu-id="614bb-134">Outils utilisés pour la gestion de la configuration</span><span class="sxs-lookup"><span data-stu-id="614bb-134">Tools used for configuration management</span></span>

<span data-ttu-id="614bb-135">De nombreux outils permettent de détecter, d’auditer et de signaler des ressources.</span><span class="sxs-lookup"><span data-stu-id="614bb-135">There are many tools to discover, audit, and report assets.</span></span> <span data-ttu-id="614bb-136">Certains de ces outils sont abordés dans cette section.</span><span class="sxs-lookup"><span data-stu-id="614bb-136">Some of these tools are discussed in this section.</span></span>

  - <span data-ttu-id="614bb-137">**Scripts automatisés**   Vous pouvez écrire des scripts simples pour signaler des éléments tels que le système d’exploitation, le niveau du Service Pack et la présence de logiciels sur un ensemble spécifique d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="614bb-137">**Automated Scripts**   You can write simple scripts to report items such as the operating system, service pack level, and whether software exists on a specific set of computers.</span></span> <span data-ttu-id="614bb-138">Vous pouvez écrire ces scripts dans la configuration requise exacte d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="614bb-138">You can write these scripts to an organization’s exact requirements.</span></span> <span data-ttu-id="614bb-139">Toutefois, le nombre requis de scripts et leur complexité peuvent compliquer la création et la gestion des scripts.</span><span class="sxs-lookup"><span data-stu-id="614bb-139">However, the required number of scripts and their complexity can make scripts expensive to create and maintain.</span></span>

  - <span data-ttu-id="614bb-140">**Outils automatisés**   En fonction de la taille de votre entreprise et des besoins de votre organisation, il peut être préférable d’utiliser des outils automatisés.</span><span class="sxs-lookup"><span data-stu-id="614bb-140">**Automated Tools**   Depending on the size of your business and your organizational needs, you may want to consider using automated tools.</span></span> <span data-ttu-id="614bb-141">Les outils tels que Microsoft Endpoint Configuration Manager contiennent des modèles de rapports standard (par exemple, le niveau de Service Pack) et vous permettent également de créer des rapports personnalisés, par exemple pour une application personnalisée.</span><span class="sxs-lookup"><span data-stu-id="614bb-141">Tools such as Microsoft Endpoint Configuration Manager incorporate standard report templates (such as service pack level) and also enable you to create customized reports, for example, for a custom application.</span></span> <span data-ttu-id="614bb-142">Le gestionnaire de configuration de point de terminaison Microsoft peut également être utilisé pour signaler des configurations matérielle et logicielle.</span><span class="sxs-lookup"><span data-stu-id="614bb-142">The Microsoft Endpoint Configuration Manager can also be used to report on hardware and software configurations.</span></span>

</div>

<div>

## <a name="relationship-with-change-management"></a><span data-ttu-id="614bb-143">Relation avec la gestion des modifications</span><span class="sxs-lookup"><span data-stu-id="614bb-143">Relationship with change management</span></span>

<span data-ttu-id="614bb-144">La gestion de la configuration est étroitement liée à la gestion des modifications.</span><span class="sxs-lookup"><span data-stu-id="614bb-144">Configuration management is closely related to change management.</span></span> <span data-ttu-id="614bb-145">La gestion de la configuration identifie le besoin de modifier et d’identifier les modifications apportées aux enregistrements.</span><span class="sxs-lookup"><span data-stu-id="614bb-145">Configuration management identifies the need for change and identifies and records that a change has occurred.</span></span> <span data-ttu-id="614bb-146">Par exemple, la base de données de gestion de la configuration peut être utilisée pour identifier les serveurs qui nécessitent un correctif.</span><span class="sxs-lookup"><span data-stu-id="614bb-146">For example, the configuration management database can be used to identify servers that require a hotfix.</span></span> <span data-ttu-id="614bb-147">La gestion des modifications définit alors le processus d’application du correctif.</span><span class="sxs-lookup"><span data-stu-id="614bb-147">Change management then defines the process for applying the hotfix.</span></span>

<span data-ttu-id="614bb-148">À l’inverse, si une nouvelle mise à jour cumulative est déployée, le processus de gestion des modifications doit fournir ces informations au système de gestion de la configuration.</span><span class="sxs-lookup"><span data-stu-id="614bb-148">Conversely, if a new cumulative update is rolled out, the change management process should supply this information to the configuration management system.</span></span> <span data-ttu-id="614bb-149">Il est probable que les outils de gestion de la configuration doivent être configurés pour identifier le nouveau logiciel de sorte qu’ils puissent détecter et suivre l’emplacement et le moment de déploiement du logiciel.</span><span class="sxs-lookup"><span data-stu-id="614bb-149">The configuration management tools will probably need to be configured to identify the new software so that they can discover and track where and when the software is deployed.</span></span>

<span data-ttu-id="614bb-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="614bb-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

