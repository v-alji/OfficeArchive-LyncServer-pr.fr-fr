---
title: 'Lync Server 2013 : configuration de plates-formes système pour l’archivage'
description: 'Lync Server 2013 : configuration de plates-formes système pour l’archivage.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up system platforms for Archiving
ms:assetid: 2df40fdf-0e32-46d4-9fb2-1ce1d7bfa328
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204768(v=OCS.15)
ms:contentKeyID: 48183716
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2f210083451ae8fcb87c53e52b5512de6f1f18d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441675"
---
# <a name="setting-up-system-platforms-for-archiving-in-lync-server-2013"></a><span data-ttu-id="4a1eb-103">Configuration de plates-formes système pour l’archivage dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4a1eb-103">Setting up system platforms for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4a1eb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4a1eb-104">

<span> </span></span></span>

<span data-ttu-id="4a1eb-105">_**Dernière modification de la rubrique :** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="4a1eb-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="4a1eb-106">Avant de commencer le déploiement de l’archivage, vous devez installer le système d’exploitation requis et tout autre logiciel requis sur le matériel qui répond à la configuration système requise :</span><span class="sxs-lookup"><span data-stu-id="4a1eb-106">Before starting the deployment of Archiving, you must install the required operating system and any other prerequisite software on hardware that meets system requirements:</span></span>

  - <span data-ttu-id="4a1eb-107">**Plateforme Lync Server 2013**   Les déploiements de Lync Server 2013 ne disposent pas de serveurs d’archivage.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-107">**Lync Server 2013 platform**   Lync Server 2013 deployments do not have Archiving Servers.</span></span> <span data-ttu-id="4a1eb-108">À la place, les agents de collection de données unifiés s’exécutent sur des serveurs frontaux et sur les serveurs Standard Edition pour capturer les données pour l’archivage, de sorte qu’aucune plateforme système distincte n’est requise pour l’archivage.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-108">Instead, Unified Data Collection Agents run on Front End Servers and Standard Edition servers to capture data for archiving, so no separate system platform is required to host Archiving.</span></span>

  - <span data-ttu-id="4a1eb-109">**Plateforme de stockage de données**   Dans Lync Server 2013, vous pouvez stocker des données à l’aide de l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4a1eb-109">**Data storage platform**   In Lync Server 2013, you can store data by using either of the following:</span></span>
    
      - <span data-ttu-id="4a1eb-110">**Intégration de Microsoft Exchange**   Si vous voulez stocker les données d’archivage de Lync Server 2013 en utilisant votre déploiement Exchange 2013, au lieu d’une base de données séparée pour le stockage des données d’archivage, votre déploiement Exchange doit exécuter Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-110">**Microsoft Exchange integration**   If you want to store Lync Server 2013 Archiving data by using your Exchange 2013 deployment, instead of or in addition to setting up a separate database for storage of Archiving data, your Exchange deployment must be running Exchange 2013.</span></span> <span data-ttu-id="4a1eb-111">Pour plus d’informations sur la configuration des plates-formes système pour Exchange 2013, voir la documentation du produit Exchange.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-111">For details about setting up system platforms for Exchange 2013, see the Exchange product documentation.</span></span>
    
      - <span data-ttu-id="4a1eb-112">**SQL Server**   Si vous souhaitez utiliser une base de données SQL Server distincte pour le stockage des données d’archivage, au lieu de ou en plus de l’intégration de Microsoft Exchange, vous devez configurer la plateforme système de la base de données avant le déploiement de l’archivage.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-112">**SQL Server**   If you want to use a separate SQL Server database for storage of archiving data, instead of or in addition to using Microsoft Exchange integration, you must set up the system platform for the database prior to deployment of Archiving.</span></span> <span data-ttu-id="4a1eb-113">La configuration requise pour la plateforme système spécifique dépend de l’utilisation de Microsoft SQL Server 2008 R2 ou de Microsoft SQL Server 2012 pour la base de données d’archivage.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-113">The specific system platform requirements depend on whether you use Microsoft SQL Server 2008 R2 or Microsoft SQL Server 2012 for the Archiving database.</span></span> <span data-ttu-id="4a1eb-114">Pour plus d’informations sur la configuration de plates-formes système pour ces bases de données, consultez la documentation du produit Microsoft SQL Server 2008 R2 et Microsoft SQL Server 2012.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-114">For details about setting up system platforms for these databases, see the Microsoft SQL Server 2008 R2 and Microsoft SQL Server 2012 product documentation.</span></span>

  - <span data-ttu-id="4a1eb-115">**Plateforme du serveur de fichiers**   Lync Server 2013 stocke les fichiers d’archivage de Lync Server dans le même emplacement que celui que vous spécifiez pour le stockage de fichiers lorsque vous configurez votre serveur frontal ou les serveurs Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-115">**File server platform**   Lync Server 2013 stores Lync Server archiving files in the same location that you specify for file storage when you set up your Front End Servers or Standard Edition servers.</span></span> <span data-ttu-id="4a1eb-116">Dans le cas contraire, vous ne pouvez pas spécifier d’emplacement distinct pour l’archivage des fichiers.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-116">You cannot specify a separate location for archiving file storage, so no separate system platform is required for Archiving file storage.</span></span> <span data-ttu-id="4a1eb-117">Si vous utilisez l’intégration de Microsoft Exchange, Exchange 2013 les fichiers pour les communications Lync archivées sont stockés sur les serveurs Exchange 2013 pour les utilisateurs hébergés sur les serveurs Exchange.</span><span class="sxs-lookup"><span data-stu-id="4a1eb-117">If you use Microsoft Exchange integration, Exchange 2013 the files for archived Lync communications are stored on Exchange 2013 servers for users homed on those Exchange servers.</span></span>

<span data-ttu-id="4a1eb-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4a1eb-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

