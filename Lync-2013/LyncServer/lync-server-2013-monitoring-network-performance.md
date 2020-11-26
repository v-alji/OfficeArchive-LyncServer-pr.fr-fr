---
title: 'Skype Entreprise Server 2015 : surveillance des performances du réseau'
description: 'Lync Server 2013 : surveillance des performances du réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring network performance
ms:assetid: bc3a01da-91eb-4c0c-9598-35e5e46b00f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720923(v=OCS.15)
ms:contentKeyID: 63969647
ms.date: 04/27/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0ead7e3f9001b06c783c9b22327581e795a20322
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425345"
---
# <a name="monitoring-network-performance-in-lync-server-2013"></a><span data-ttu-id="22719-103">Surveillance des performances du réseau dans Skype Entreprise Server 2015</span><span class="sxs-lookup"><span data-stu-id="22719-103">Monitoring network performance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="22719-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="22719-104">

<span> </span></span></span>

<span data-ttu-id="22719-105">_**Dernière modification de la rubrique :** 2016-04-27_</span><span class="sxs-lookup"><span data-stu-id="22719-105">_**Topic Last Modified:** 2016-04-27_</span></span>

<span data-ttu-id="22719-106">Lync Server 2013 est une technologie de communication en temps réel dont le contenu repose essentiellement sur le réseau pour permettre la communication entre les utilisateurs (messagerie instantanée, messagerie instantanée, appels vocaux ou communication vidéo).</span><span class="sxs-lookup"><span data-stu-id="22719-106">Lync Server 2013 is a real-time communications technology that relies heavily on the network to enable communication between users—either through instant messaging (IM), voice calls, or video communication.</span></span> <span data-ttu-id="22719-107">Il est par conséquent important de surveiller les performances du réseau en continu pour garantir la meilleure utilisation possible de la modalité de communication choisie par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="22719-107">It is therefore important to monitor the network performance continuously to help guarantee that a user’s chosen communication modality provides the best possible experience.</span></span>

<span data-ttu-id="22719-108">Les performances du réseau peuvent être mesurées à deux niveaux :</span><span class="sxs-lookup"><span data-stu-id="22719-108">Network performance can be measured at two levels:</span></span>

  - <span data-ttu-id="22719-109">**Performances globales du réseau**   Ce niveau de mesure des performances permet à une organisation de créer une vue de grande image de son réseau et est généralement mise en œuvre par le biais de systèmes de surveillance réseau tiers.</span><span class="sxs-lookup"><span data-stu-id="22719-109">**Overall network performance**   This level of performance measurement will allow an organization to create a "big-picture" view of their network and is usually implemented through third-party network monitoring systems.</span></span> <span data-ttu-id="22719-110">Ces systèmes recevront des données de performances et de capacité provenant de périphériques réseau distants tels que des routeurs et commutés sur le réseau pour permettre aux administrateurs de déterminer l’état d’un composant réseau donné à tout moment.</span><span class="sxs-lookup"><span data-stu-id="22719-110">These systems will receive performance and capacity data from remote network devices such as routers and switched throughout the network to allow administrators to determine the health of any given network component at any time of day.</span></span>

  - <span data-ttu-id="22719-111">**Performances du serveur individuel**   Ce niveau de mesure des performances est limité à un serveur spécifique et permettra aux administrateurs d’évaluer les performances du réseau d’un serveur en particulier pour résoudre un problème de performance spécifique ou pour évaluer les performances de chaque serveur sur une période donnée dans le cadre d’un processus de planification de capacité.</span><span class="sxs-lookup"><span data-stu-id="22719-111">**Individual server performance**   This level of performance measurement is limited to a specific server and will help administrators with gauging the network performance of a specific server to either help with troubleshooting a specific performance issue or to gauge the respective server’s performance over a given period as part of a capacity planning process.</span></span>

<span data-ttu-id="22719-112">Vous pouvez surveiller le réseau en utilisant les outils décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="22719-112">You can monitor the network by using the tools described in the following sections.</span></span>

<div>

## <a name="tools-for-overall-network-performance-monitoring"></a><span data-ttu-id="22719-113">Outils d’analyse des performances globales du réseau</span><span class="sxs-lookup"><span data-stu-id="22719-113">Tools for Overall Network Performance Monitoring</span></span>

<div>

## <a name="system-center-operations-manager-2012"></a><span data-ttu-id="22719-114">System Center Operations Manager 2012</span><span class="sxs-lookup"><span data-stu-id="22719-114">System Center Operations Manager 2012</span></span>

<span data-ttu-id="22719-115">System Center Operations Manager fournit une gestion des services de bout en bout, facile à personnaliser et à prolonger pour améliorer les niveaux de service au sein d’un environnement informatique.</span><span class="sxs-lookup"><span data-stu-id="22719-115">System Center Operations Manager provides end-to-end service management that is easy to customize and extend for improved service levels across an IT environment.</span></span> <span data-ttu-id="22719-116">Cela permet aux opérations et aux équipes de gestion informatiques d’identifier les problèmes et de résoudre les problèmes affectant l’état des services informatiques distribués.</span><span class="sxs-lookup"><span data-stu-id="22719-116">This enables Operations and IT Management teams to identify, and resolve issues affecting the health of distributed IT services.</span></span> <span data-ttu-id="22719-117">La gestion de service de bout en bout n’est pas limitée aux environnements Microsoft.</span><span class="sxs-lookup"><span data-stu-id="22719-117">End-to-end service management is not restricted to Microsoft-based environments.</span></span> <span data-ttu-id="22719-118">La prise en charge des services Web pour la gestion (WS-Management), le protocole SNMP (simple Network Management Protocol) et les solutions de partenariat permettent aux systèmes qui n’exécutent pas de systèmes d’exploitation et de matériel Microsoft d’être inclus dans l’analyse du service System Center Operations Manager 2012.</span><span class="sxs-lookup"><span data-stu-id="22719-118">Support for Web Services for Management (WS-Management), Simple Network Management Protocol (SNMP), and partner solutions allow for systems that do not run Microsoft operating systems and hardware to be included in service monitoring within System Center Operations Manager 2012.</span></span>

</div>

<div>

## <a name="system-center-operations-manager-2012-and-third-party-network-management-solutions"></a><span data-ttu-id="22719-119">Les solutions de gestion de réseau de System Center Operations Manager 2012 et tierces</span><span class="sxs-lookup"><span data-stu-id="22719-119">System Center Operations Manager 2012 and Third-Party Network Management Solutions</span></span>

<span data-ttu-id="22719-120">**EMC Smarts**   EMC Solutions for Operations Manager vous aide à résoudre les problèmes liés aux niveaux de service.</span><span class="sxs-lookup"><span data-stu-id="22719-120">**EMC Smarts**   EMC Solutions for Operations Manager help you quickly resolve issues affecting service levels throughout.</span></span> <span data-ttu-id="22719-121">À l’aide d’EMC Solutions for Operations Manager, vous pouvez gérer et surveiller votre chaîne de services informatiques en une solution intégrée et automatisée.</span><span class="sxs-lookup"><span data-stu-id="22719-121">By using EMC Solutions for Operations Manager, you can manage and monitor your whole IT service chain with one integrated, automated solution.</span></span> <span data-ttu-id="22719-122">Vous identifierez facilement les causes racines des problèmes de performances et de disponibilité, et vous pouvez les résoudre plus rapidement pour réduire les effets et les coûts.</span><span class="sxs-lookup"><span data-stu-id="22719-122">You'll easily identify the root causes of performance and availability issues, and resolve them faster which reduces effects and costs.</span></span> <span data-ttu-id="22719-123">Les principaux avantages sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="22719-123">Key benefits include the following:</span></span>

  - <span data-ttu-id="22719-124">Une gestion avancée et facile à utiliser, qui vous permet de fournir une valeur stratégique commerciale au lieu de trier et de filtrer manuellement des alertes confuses.</span><span class="sxs-lookup"><span data-stu-id="22719-124">Advanced, easy-to-use management   Focus on delivering strategic business value instead of manually sorting and filtering confusing alerts.</span></span>

  - <span data-ttu-id="22719-125">**Résolution plus rapide**   Résoudre les problèmes liés à l’application et répondre aux besoins de votre entreprise plus rapidement et réduire l’impact et le coût.</span><span class="sxs-lookup"><span data-stu-id="22719-125">**Faster resolution**   Solve IT issues and respond to business needs faster, reducing effect and cost.</span></span>

  - <span data-ttu-id="22719-126">**Opérations rationalisées**   Evitez de simplifier l’informatique en combinant plusieurs outils de gestion, applications et terminaux.</span><span class="sxs-lookup"><span data-stu-id="22719-126">**Streamlined operations**   Avoid IT complexity by combining multiple management tools, applications, and terminals.</span></span>

<span data-ttu-id="22719-127">Pour plus d’informations, consultez la page suivante :</span><span class="sxs-lookup"><span data-stu-id="22719-127">More information can be found here:</span></span>

[<span data-ttu-id="22719-128">Microsoft System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="22719-128">Microsoft System Center Operations Manager</span></span>](https://go.microsoft.com/fwlink/p/?linkid=243651)

[<span data-ttu-id="22719-129">Solutions pour Microsoft System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="22719-129">Solutions for Microsoft System Center Operations Manager</span></span>](http://www.emc.com/collateral/software/data-sheet/h6135-server-manager-ds.pdf)

</div>

<div>

## <a name="third-party-solutions"></a><span data-ttu-id="22719-130">Solutions tierces</span><span class="sxs-lookup"><span data-stu-id="22719-130">Third-Party Solutions</span></span>

<span data-ttu-id="22719-131">HP Network **Management Center (anciennement HP OpenView)**[HP Network Management Center](http://www8.hp.com/us/en/software-solutions/network-management/index.html?%26zn=bto%26cp=1-11-15-119_4000_100__) fournit une gestion intégrée des pannes et des performances pour améliorer la disponibilité et les performances du réseau.   </span><span class="sxs-lookup"><span data-stu-id="22719-131">**HP Network Management Center (previously known as HP OpenView)**   [HP Network Management Center](http://www8.hp.com/us/en/software-solutions/network-management/index.html?%26zn=bto%26cp=1-11-15-119_4000_100__) provides integrated fault and performance management to improve network availability and performance.</span></span> <span data-ttu-id="22719-132">Le centre de gestion réseau fait partie de la solution de gestion de réseau automatisé HP qui unifie la gestion des erreurs, des performances, de la configuration et de la gestion des modifications.</span><span class="sxs-lookup"><span data-stu-id="22719-132">Network Management Center is part of the HP automated network management solution that unifies fault, performance, configuration, and change management.</span></span>

<span data-ttu-id="22719-133">**Produits d’automatisation et de gestion réseau Cisco**   Pour l’entreprise, Cisco dispose de plusieurs produits de gestion dont la solution de gestion LAN CiscoWorks et le module Cisco Network Analysis module pour améliorer l’efficacité opérationnelle et réduire les temps d’arrêt du réseau.</span><span class="sxs-lookup"><span data-stu-id="22719-133">**Cisco Network Management and Automation products**   For the Enterprise, Cisco has several management products available including CiscoWorks LAN Management Solution and Cisco Network Analysis Module, to help improve operational efficiency and reduce network downtime.</span></span> <span data-ttu-id="22719-134">Pour obtenir des données supplémentaires sur ces produits, consultez le site Web Cisco à l’adresse [https://www.cisco.com/en/US/products/sw/netmgtsw/index.html](https://www.cisco.com/en/us/products/sw/netmgtsw/index.html) .</span><span class="sxs-lookup"><span data-stu-id="22719-134">For additional data on these products, refer to the Cisco website at [https://www.cisco.com/en/US/products/sw/netmgtsw/index.html](https://www.cisco.com/en/us/products/sw/netmgtsw/index.html).</span></span>

<span data-ttu-id="22719-135">SNMP (simple Network Management Protocol) est une norme de gestion de réseau qui définit une stratégie de gestion des réseaux TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="22719-135">Simple Network Management Protocol (SNMP)   Simple Network Management Protocol (SNMP) is a network management standard that defines a strategy for managing TCP/IP networks.</span></span> <span data-ttu-id="22719-136">SNMP vous permet de capturer les informations de configuration et d’État relatives au réseau, et d’envoyer les informations à un ordinateur désigné pour le suivi des événements.</span><span class="sxs-lookup"><span data-stu-id="22719-136">SNMP enables you to capture configuration and status information about the network, and send the information to a designated computer for event monitoring.</span></span> <span data-ttu-id="22719-137">Ce protocole de gestion de réseau standard utilise une architecture distribuée qui inclut les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="22719-137">This standards based network management protocol uses a distributed architecture that includes the following:</span></span>

  - <span data-ttu-id="22719-138">Plusieurs nœuds gérés, chacun avec une entité SNMP appelé agent assurant l’accès à distance à l’instrumentation de gestion.</span><span class="sxs-lookup"><span data-stu-id="22719-138">Multiple managed nodes, each with an SNMP entity called an agent which provides remote access to management instrumentation.</span></span>

  - <span data-ttu-id="22719-139">Au moins une entité SNMP désignée sous le nom de responsable qui exécute des applications de gestion pour surveiller et contrôler les éléments gérés.</span><span class="sxs-lookup"><span data-stu-id="22719-139">At least one SNMP entity known as a manager which runs management applications to monitor and control managed elements.</span></span> <span data-ttu-id="22719-140">Les éléments managés sont des appareils tels que des hôtes, des routeurs, etc.</span><span class="sxs-lookup"><span data-stu-id="22719-140">Managed elements are devices such as hosts, routers, and so on.</span></span> <span data-ttu-id="22719-141">Ils sont surveillés et contrôlés en accédant à leurs informations de gestion.</span><span class="sxs-lookup"><span data-stu-id="22719-141">They are monitored and controlled by accessing their management information.</span></span>

  - <span data-ttu-id="22719-142">Le protocole de gestion SNMP est utilisé pour communiquer des informations de gestion entre les stations de gestion et les agents.</span><span class="sxs-lookup"><span data-stu-id="22719-142">A management protocol, SNMP, is used to communicate management information between the management stations and agents.</span></span> <span data-ttu-id="22719-143">Les informations de gestion font référence à une collection d’objets gérés qui résident dans un magasin d’informations virtuel appelé base de données de gestion (MIB).</span><span class="sxs-lookup"><span data-stu-id="22719-143">Management information refers to a collection of managed objects that live in a virtual information store called a Management Information Base (MIB).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="22719-144">Vous trouverez ci-dessous des exemples de solutions de contrôle de réseau tierces.</span><span class="sxs-lookup"><span data-stu-id="22719-144">Examples of third-party network monitoring solutions are provided above.</span></span> <span data-ttu-id="22719-145">Cette liste n’est pas définitive et Microsoft ne favorise pas une solution de fournisseur spécifique.</span><span class="sxs-lookup"><span data-stu-id="22719-145">This list is not definitive and Microsoft does not favor any specific vendor solution.</span></span> <span data-ttu-id="22719-146">Contactez un fournisseur de services réseau et votre fournisseur de technologie pour déterminer la meilleure solution de surveillance réseau pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="22719-146">Consult with a network service provider and or your respective technology provider to determine the best network monitoring solution for your organization.</span></span>



</div>

</div>

</div>

<div>

## <a name="tools-for-monitoring-individual-server-network-performance"></a><span data-ttu-id="22719-147">Outils d’analyse des performances du réseau d’un serveur individuel</span><span class="sxs-lookup"><span data-stu-id="22719-147">Tools for Monitoring Individual Server Network Performance</span></span>

<div>

## <a name="system-center-operations-manager-2012"></a><span data-ttu-id="22719-148">System Center Operations Manager 2012</span><span class="sxs-lookup"><span data-stu-id="22719-148">System Center Operations Manager 2012</span></span>

<span data-ttu-id="22719-149">System Center Operations Manager 2012 permettra aux administrateurs d’afficher les performances réseau de chaque serveur par le biais du pack d’administration Windows Server 2012 : le Pack de gestion du système d’exploitation Windows Server inclut un module de gestion des performances qui permettra aux administrateurs de surveiller les performances de carte réseau et l’intégrité de la carte.</span><span class="sxs-lookup"><span data-stu-id="22719-149">System Center Operations Manager 2012 would allow administrators to view network performance of individual servers through the Windows Server 2012 Management Pack: The Windows Server operating system management pack includes a "Performance" management pack that would allow administrators to monitor Network Adapter performance and adapter health.</span></span>

</div>

<div>

## <a name="windows-network-monitor"></a><span data-ttu-id="22719-150">Moniteur réseau Windows</span><span class="sxs-lookup"><span data-stu-id="22719-150">Windows Network Monitor</span></span>

<span data-ttu-id="22719-151">Recueille, affiche, analyse l’utilisation des ressources sur un serveur et mesure le trafic réseau.</span><span class="sxs-lookup"><span data-stu-id="22719-151">Collects, displays, analyzes resource usage on a server, and measures network traffic.</span></span> <span data-ttu-id="22719-152">Le moniteur réseau vérifie uniquement l’activité du réseau.</span><span class="sxs-lookup"><span data-stu-id="22719-152">Network Monitor exclusively monitors network activity.</span></span> <span data-ttu-id="22719-153">En capturant et en analysant les données du réseau et en utilisant ces données avec les journaux de performance, vous pouvez déterminer l’utilisation du réseau, identifier les problèmes du réseau et prévoir les besoins futurs du réseau.</span><span class="sxs-lookup"><span data-stu-id="22719-153">By capturing and analyzing network data, and using this data with performance logs, you can determine the network usage, identify network issues, and forecast future network needs.</span></span>

<span data-ttu-id="22719-154">Pour plus d’informations sur le moniteur réseau 3,4 et sur l’installation et la configuration de l’analyse réseau et la capture et l’analyse des données, reportez-vous à la section vue d’ensemble du moniteur réseau 3,3.</span><span class="sxs-lookup"><span data-stu-id="22719-154">For more information about Network Monitor 3.4, and to learn how to install and configure Network Monitor and capture and analyze data, review this session: Network Monitor 3.3 Overview.</span></span> <span data-ttu-id="22719-155">Consultez également le [blog Moniteur réseau](https://blogs.technet.com/b/netmon/).</span><span class="sxs-lookup"><span data-stu-id="22719-155">Also, review the [Network Monitor blog](https://blogs.technet.com/b/netmon/).</span></span>

<span data-ttu-id="22719-156"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="22719-156"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

