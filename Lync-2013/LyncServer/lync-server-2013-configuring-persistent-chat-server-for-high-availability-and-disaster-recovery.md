---
title: Configuration d’un serveur de conversation permanente pour la haute disponibilité et la récupération d’urgence
description: Configuration du serveur de chat permanent pour une haute disponibilité et une reprise après sinistre.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Persistent Chat Server for high availability and disaster recovery
ms:assetid: eebc581c-e3a0-4b69-8a43-80b607b4d8f2
ms:mtpsurl: https://technet.microsoft.com/library/JJ205364(v=OCS.15)
ms:contentKeyID: 48185760
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 13935f2ec690deb7f896c13d185680ce1122a892
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432785"
---
# <a name="configuring-persistent-chat-server-for-high-availability-and-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="25248-103">Configuration d’un serveur de conversation permanente pour la haute disponibilité et la récupération d’urgence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25248-103">Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="25248-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="25248-104">

<span> </span></span></span>

<span data-ttu-id="25248-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="25248-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="25248-106">Le serveur Lync Server 2013, les services de chat permanent utilisent une configuration de *pool ambitieuse* pour la récupération d’urgence.</span><span class="sxs-lookup"><span data-stu-id="25248-106">The Lync Server 2013, Persistent Chat Server services use a *stretched pool* configuration for disaster recovery.</span></span> <span data-ttu-id="25248-107">Un pool étiré est un pool qui comporte des ordinateurs qui sont répartis entre deux centres de données physiques, mais qui se trouvent au sein d’un seul site de serveur Lync logique.</span><span class="sxs-lookup"><span data-stu-id="25248-107">A stretched pool is a pool that has computers that are distributed between two physical data centers, but are within a single logical Lync Server site.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="25248-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="25248-108">In This Section</span></span>

  - [<span data-ttu-id="25248-109">Ressources requises pour le serveur de conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25248-109">Required resources for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-required-resources-for-persistent-chat-server.md)

  - [<span data-ttu-id="25248-110">Utilisation du générateur de topologie pour configurer la haute disponibilité et la récupération d’urgence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25248-110">Using Topology Builder to configure high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-using-topology-builder-to-configure-high-availability-and-disaster-recovery.md)

  - [<span data-ttu-id="25248-111">Utilisation d’un pool de serveurs de conversation permanente élargi pour la récupération d’urgence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25248-111">Using a stretched Persistent Chat Server pool for disaster recovery in Lync Server 2013</span></span>](lync-server-2013-using-a-stretched-persistent-chat-server-pool-for-disaster-recovery.md)

  - [<span data-ttu-id="25248-112">Mise en miroir SQL Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25248-112">SQL Server mirroring in Lync Server 2013</span></span>](lync-server-2013-sql-server-mirroring.md)

  - [<span data-ttu-id="25248-113">Configuration de la copie des journaux de transaction SQL Server dans Lync Server 2013 pour la base de données principale du serveur de conversation permanente</span><span class="sxs-lookup"><span data-stu-id="25248-113">Setting up SQL Server Log Shipping in Lync Server 2013 for the Persistent Chat Server primary database</span></span>](lync-server-2013-setting-up-sql-server-log-shipping-for-the-persistent-chat-server-primary-database.md)

  - [<span data-ttu-id="25248-114">Définition de la copie des journaux de transaction SQL Server entre la base de données miroir principale et la base de données secondaire de copie des journaux de transaction dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25248-114">Setting up SQL Server Log Shipping between the primary mirror and the Log Shipping secondary database in Lync Server 2013</span></span>](lync-server-2013-set-up-log-shipping-secondary-database.md)

<span data-ttu-id="25248-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="25248-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

