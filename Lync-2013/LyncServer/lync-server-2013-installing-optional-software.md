---
title: 'Lync Server 2013 : installation de logiciels facultatifs'
description: 'Lync Server 2013 : installation de logiciels facultatifs.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing optional software
ms:assetid: b95b3301-fa1e-4b96-9af4-05b43d39db8d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615032(v=OCS.15)
ms:contentKeyID: 51541509
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7423c0d54b762fb4af7cedc8d7ba8745fd94bdf7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427025"
---
# <a name="installing-optional-software-in-lync-server-2013"></a><span data-ttu-id="ad082-103">Installer un logiciel facultatif dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ad082-103">Installing optional software in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ad082-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ad082-104">

<span> </span></span></span>

<span data-ttu-id="ad082-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="ad082-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="ad082-106">L’outil de planification Microsoft Lync Server 2013 est conçu pour être exporté vers Microsoft Excel et Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="ad082-106">The Microsoft Lync Server 2013, Planning Tool is designed to export to Microsoft Excel and Microsoft Visio.</span></span> <span data-ttu-id="ad082-107">Même si ces applications ne sont pas nécessaires pour l’utilisation de l’outil de planification, elles ajoutent une valeur importante au déploiement et à la documentation de votre conception.</span><span class="sxs-lookup"><span data-stu-id="ad082-107">While these applications are not required for the operation of the Planning Tool, they do add significant value to the deployment and documentation of your design.</span></span>

<div>

## <a name="optional-software"></a><span data-ttu-id="ad082-108">Logiciels facultatifs</span><span class="sxs-lookup"><span data-stu-id="ad082-108">Optional Software</span></span>

<div>

## <a name="microsoft-excel"></a><span data-ttu-id="ad082-109">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="ad082-109">Microsoft Excel</span></span>

<span data-ttu-id="ad082-110">L’exportation de votre conception vers Microsoft Excel permet de créer un rapport sous forme de feuille de calcul à quatre onglets :</span><span class="sxs-lookup"><span data-stu-id="ad082-110">Exporting your design to Microsoft Excel creates a report that displays seven tabs in the spreadsheet:</span></span>

  - <span data-ttu-id="ad082-111">Synthèse : affiche des informations sur la configuration du site, notamment le nombre d’utilisateurs, les paramètres de capacité et les informations de profil du serveur.</span><span class="sxs-lookup"><span data-stu-id="ad082-111">Summary – Displays information on site configuration, including user count, capacity settings, and server profile information.</span></span>

  - <span data-ttu-id="ad082-p102">Profil matériel : affiche un rapport détaillant les configurations matérielles recommandées pour les serveurs spécifiés dans la topologie, y compris le processeur, la mémoire, le disque et l’interface réseau. La quantité et les caractéristiques conseillées pour les composants serveur y figurent également. Par ailleurs, chaque serveur est défini par site afin de fournir une représentation complète de la configuration serveur requise pour chaque site.</span><span class="sxs-lookup"><span data-stu-id="ad082-p102">Hardware Profile – Displays a report on the recommended hardware configurations for servers that are specified in the topology, including CPU, memory, disk, and network interface. The quantity and recommended specifications for the server components are also included. In addition, each server is defined by site to provide a complete representation of server requirements by site.</span></span>

  - <span data-ttu-id="ad082-p103">Configuration requise pour les ports : affiche un rapport de tous les ports activés et l’association entre l’équilibrage de la charge DNS et les programmes d’équilibrage de la charge matérielle. Vous devez utiliser ce rapport pour planifier votre pare-feu et les configurations de l’équilibrage de la charge DNS et des programmes d’équilibrage de la charge matérielle.</span><span class="sxs-lookup"><span data-stu-id="ad082-p103">Ports Requirements – Displays a report of all ports that are enabled, and the association to Domain Name System load balancing (DNS LB) and hardware load balancers (HLB). You should use this report to plan your firewall and DNS LB and HLB configurations.</span></span>

  - <span data-ttu-id="ad082-117">Rapport de synthèse : affiche la synthèse générale des paramètres nécessaires à la configuration de votre réseau Edge Server.</span><span class="sxs-lookup"><span data-stu-id="ad082-117">Summary Report – Displays the general summary of the settings that are required to set up your Edge Server network.</span></span>

  - <span data-ttu-id="ad082-118">Rapport sur les certificats : affiche le nom du sujet et les noms de domaine alternatifs requis pour les certificats nécessaires à l’exécution des serveurs Edge.</span><span class="sxs-lookup"><span data-stu-id="ad082-118">Certificates Report – Displays the subject name and subject alternate names that are required for the certificates needed to get the Edge Servers running.</span></span>

  - <span data-ttu-id="ad082-119">Rapport de pare-feu : affiche les adresses IP et ports sources et de destination des interfaces internes et externes.</span><span class="sxs-lookup"><span data-stu-id="ad082-119">Firewall Report – Displays the source and destination ports and IP addresses for both External and Internal interfaces.</span></span>

  - <span data-ttu-id="ad082-120">Rapport DNS : affiche le nom de domaine complet et les adresses IP/VIP requises pour chaque entrée DNS que vous créez.</span><span class="sxs-lookup"><span data-stu-id="ad082-120">DNS Report – Displays the fully qualified domain name (FQDN) and IP/VIP addresses required for each DNS entry that you create.</span></span>

</div>

<div>

## <a name="microsoft-visio"></a><span data-ttu-id="ad082-121">Microsoft Visio</span><span class="sxs-lookup"><span data-stu-id="ad082-121">Microsoft Visio</span></span>

<span data-ttu-id="ad082-p104">L’exportation de votre conception vers Microsoft Visio crée un diagramme à utiliser dans la documentation de votre topologie et infrastructure configurée. Le diagramme importé peut être modifié et réorganisé pour répondre aux besoins de votre documentation. Un diagramme Visio classique inclut les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="ad082-p104">Exporting your design to Microsoft Visio creates a diagram for use in your documentation purposes of your configured topology and infrastructure. The imported diagram can be edited and rearranged to meet your documentation needs. The typical Visio diagram will include:</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ad082-125">Si votre conception est suffisamment grande pour nécessiter plus de trois serveurs frontaux, une page supplémentaire est créée pour le pool frontal, les serveurs frontaux, l’ordinateur exécutant SQL Server, les adresses IP et les noms de domaine complets.</span><span class="sxs-lookup"><span data-stu-id="ad082-125">If your design is large enough to require more than three Front End Servers, an additional page will be created for the Front End pool, Front End Servers, the computer running SQL Server, IP addresses, and FQDNs.</span></span>



</div>

  - <span data-ttu-id="ad082-126">Topologie globale : diagramme des sites Lync Server 2013 configurés.</span><span class="sxs-lookup"><span data-stu-id="ad082-126">Global Topology – Diagram of configured Lync Server 2013 sites.</span></span>

  - <span data-ttu-id="ad082-127">Onglet nom du site : affiche la topologie de configuration de site avec serveur de périmètre, pare-feu, réseau téléphonique public commuté (RTC) avec passerelles et le déploiement de serveur interne.</span><span class="sxs-lookup"><span data-stu-id="ad082-127">Site Name tab – Displays the site configuration topology with Edge Server, firewall, public switched telephone network (PSTN) with gateways, and the internal server deployment.</span></span> <span data-ttu-id="ad082-128">Le déploiement interne se compose de serveurs et de pools configurés, y compris les pools front end, serveurs SQL Server, services de domaine Active Directory, directeurs, serveurs de messagerie unifiée Exchange, serveurs de boîtes aux lettres Exchange, serveurs Office Web Apps, serveurs de médiation et serveurs de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="ad082-128">Internal deployment consists of configured servers and pools, including the Front End pools, SQL Server-based servers, Active Directory Domain Services, Directors, Exchange Unified Messaging (UM) servers, Exchange Mailbox Servers, Office Web Apps Servers, Mediation Servers, and Persistent Chat Servers.</span></span>

  - <span data-ttu-id="ad082-129">Cartographie de réseaux de réseaux latéraux : diagramme détaillant la configuration du serveur Edge avec les adresses IP et noms de domaine complets associés.</span><span class="sxs-lookup"><span data-stu-id="ad082-129">Edge Network Diagram – Diagram detailing the Edge Server configuration with associated IP addresses and FQDNs.</span></span> <span data-ttu-id="ad082-130">L’équilibrage de la charge DNS et les programmes d’équilibrage de la charge matérielle sont également inclus.</span><span class="sxs-lookup"><span data-stu-id="ad082-130">DNS load balancing and hardware load balancers are also included.</span></span> <span data-ttu-id="ad082-131">De plus, les directeurs et le serveur frontal ou le pool frontal sont affichés, avec DNS ou HLB associé et l’adresse IP attribuée (l’outil de planification prend en charge à la fois les adresses IPv4 et IPv6) et le FQDN.</span><span class="sxs-lookup"><span data-stu-id="ad082-131">Additionally, Directors and the Front End Server or Front End pool are displayed, with associated DNS LB or HLB and the assigned IP address (the Planning Tool supports both IPv4 and IPv6 addresses) and FQDN.</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ad082-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad082-132">See Also</span></span>


[<span data-ttu-id="ad082-133">Installation de l’outil de planification dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ad082-133">Installing the Planning Tool in Lync Server 2013</span></span>](lync-server-2013-installing-the-planning-tool.md)  
  

<span data-ttu-id="ad082-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ad082-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

