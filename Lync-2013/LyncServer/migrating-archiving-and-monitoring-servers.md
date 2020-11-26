---
title: Migration des serveurs d’archivage et de surveillance
description: Migration des serveurs d’archivage et de surveillance.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrating Archiving and Monitoring servers
ms:assetid: 77831579-df45-4697-b8c5-207b74a07a40
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205015(v=OCS.15)
ms:contentKeyID: 48184550
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2dabd16fd38dbf463a4bc608fe77368e781571fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443747"
---
# <a name="migrating-archiving-and-monitoring-servers"></a><span data-ttu-id="c8a16-103">Migration des serveurs d’archivage et de surveillance</span><span class="sxs-lookup"><span data-stu-id="c8a16-103">Migrating Archiving and Monitoring servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c8a16-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c8a16-104">

<span> </span></span></span>

<span data-ttu-id="c8a16-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="c8a16-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="c8a16-106">Si vous avez déployé le serveur d’archivage et le serveur de surveillance dans votre environnement Lync Server 2010, vous pouvez déployer ces serveurs dans votre environnement Lync Server 2013 après la migration de vos pools front-end.</span><span class="sxs-lookup"><span data-stu-id="c8a16-106">If you deployed Archiving Server and Monitoring Server in your Lync Server 2010 environment, you can deploy these servers in your Lync Server 2013 environment after you migrate your Front End pools.</span></span> <span data-ttu-id="c8a16-107">En revanche, si la fonctionnalité d’archivage et de surveillance est essentielle pour votre organisation, il est préférable d’ajouter un archivage et une analyse à votre pool de pilotes 2013 Lync Server avant de procéder à la migration de manière à ce que la fonctionnalité soit disponible pendant le processus de migration.</span><span class="sxs-lookup"><span data-stu-id="c8a16-107">If archiving and monitoring functionality are critical to your organization, however, you should add archiving and monitoring to your Lync Server 2013 pilot pool before you migrate so that the functionality is available during the migration process.</span></span>

<span data-ttu-id="c8a16-108">Si vous voulez utiliser les fonctionnalités d’archivage et de surveillance pendant le processus de migration, tenez compte des points suivants :</span><span class="sxs-lookup"><span data-stu-id="c8a16-108">If you want archiving and monitoring functionality during the migration process, keep the following considerations in mind:</span></span>

  - <span data-ttu-id="c8a16-109">L’archivage de données et le contrôle des données ne sont pas déplacés vers le déploiement Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c8a16-109">Archiving data and monitoring data are not moved to the Lync Server 2013 deployment.</span></span> <span data-ttu-id="c8a16-110">Les données que vous sauvegardez avant de désaffecter l’environnement hérité seront votre historique d’activités dans l’environnement Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c8a16-110">The data you back up prior to decommissioning the legacy environment will be your history of activity in the Lync Server 2010 environment.</span></span>

  - <span data-ttu-id="c8a16-111">La version 2010 de Lync Server du serveur d’archivage et de surveillance Server peut être associée uniquement à un pool frontal Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c8a16-111">The Lync Server 2010 version of Archiving Server and Monitoring Server can be associated only with a Lync Server 2010 Front End pool.</span></span> <span data-ttu-id="c8a16-112">Dans Lync Server 2013, l’archivage et la surveillance ne sont plus des rôles de serveur, mais les services intégrés au pool de serveurs front end 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c8a16-112">In Lync Server 2013, Archiving and Monitoring are no longer server roles, but services integrated into the Lync Server 2013 Front End pool.</span></span>

  - <span data-ttu-id="c8a16-113">Pendant la période de coexistence des déploiements d’anciens et de Lync Server 2013, la version Lync Server 2010 du serveur d’archivage et de surveillance du serveur de surveillance recueille des données destinées aux utilisateurs hébergés sur des pools Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c8a16-113">During the time that your legacy and Lync Server 2013 deployments coexist, the Lync Server 2010 version of Archiving Server and Monitoring Server gather data for users homed on Lync Server 2010 pools.</span></span> <span data-ttu-id="c8a16-114">Archivage et surveillance dans Lync Server 2013 rassemblez les données des utilisateurs hébergés sur les pools 2013 du serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="c8a16-114">Archiving and Monitoring in Lync Server 2013 gather data for users homed on Lync Server 2013 pools.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c8a16-115">Pendant la phase de migration lorsque vous utilisez toujours votre serveur de bord traditionnel avec le nouveau pool de pilotes Lync Server 2013, la version du serveur d’archivage de Lync Server 2010 continue de rassembler les données destinées aux utilisateurs hébergés sur les serveurs Lync Server 2010 pools et archivage dans Lync Server 2013 2013.</span><span class="sxs-lookup"><span data-stu-id="c8a16-115">During the phase of migration when you are still using your legacy Edge server with the new Lync Server 2013 pilot pool, the Lync Server 2010 version of Archiving Server continues to gather data for users homed on Lync Server 2010 pools and Archiving in Lync Server 2013 gathers data for users homed on Lync Server 2013 pools.</span></span>

    
    </div>

  - <span data-ttu-id="c8a16-116">Si vous utilisez une solution tierce d’archivage et de surveillance conjointement avec l’archivage et l’analyse dans Lync Server 2013, contactez votre vendeur pour savoir quand et comment vous devez intégrer la solution tierce sur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c8a16-116">If you use a third-party archiving and monitoring solution in conjunction with Archiving and Monitoring in Lync Server 2013, consult with your vendor about when and how you need to integrate the third-party solution with Lync Server 2013.</span></span>

<span data-ttu-id="c8a16-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c8a16-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

