---
title: Utilisation du générateur de topologie pour configurer la haute disponibilité et la récupération d’urgence
description: Utilisation du générateur de topologie pour configurer une haute disponibilité et une reprise après sinistre.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Topology Builder to configure high availability and disaster recovery
ms:assetid: abc1a25d-1f5e-46ef-91d2-0144fc847206
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205172(v=OCS.15)
ms:contentKeyID: 48185113
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 04764a58ac3ae1bbe0df97aadeabb03158ce8100
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395272"
---
# <a name="using-topology-builder-to-configure-high-availability-and-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="4efa0-103">Utilisation du générateur de topologie pour configurer la haute disponibilité et la récupération d’urgence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4efa0-103">Using Topology Builder to configure high availability and disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4efa0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4efa0-104">

<span> </span></span></span>

<span data-ttu-id="4efa0-105">_**Dernière modification de la rubrique :** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="4efa0-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="4efa0-106">Dans le générateur de topologie, effectuez les étapes suivantes pour configurer une haute disponibilité et une reprise après sinistre pour le serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="4efa0-106">Perform the following steps within Topology Builder to configure high availability and disaster recovery for Persistent Chat Server.</span></span>

1.  <span data-ttu-id="4efa0-107">Ajoutez les bases de données miroir et les magasins de données secondaires SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4efa0-107">Add the mirror databases and the log shipping secondary database SQL Server stores.</span></span>

2.  <span data-ttu-id="4efa0-108">Modifiez les propriétés du service de chat permanent serveur pour :</span><span class="sxs-lookup"><span data-stu-id="4efa0-108">Edit the Persistent Chat Server service properties to:</span></span>
    
    1.  <span data-ttu-id="4efa0-109">activer la mise en miroir pour la base de données primaire ;</span><span class="sxs-lookup"><span data-stu-id="4efa0-109">Enable mirroring for the primary database.</span></span>
    
    2.  <span data-ttu-id="4efa0-110">Ajoutez le magasin SQL Server en miroir principal.</span><span class="sxs-lookup"><span data-stu-id="4efa0-110">Add the primary mirror SQL Server store.</span></span>
    
    3.  <span data-ttu-id="4efa0-111">Activez la base de données d’envoi de journaux de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4efa0-111">Enable the SQL Server Log Shipping database.</span></span>
    
    4.  <span data-ttu-id="4efa0-112">Ajoutez la banque SQL Server secondaire pour l’envoi du journal SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4efa0-112">Add the SQL Server Log Shipping secondary SQL Server store.</span></span>
    
    5.  <span data-ttu-id="4efa0-113">Ajoutez le miroir SQL Server Store pour la base de données secondaire.</span><span class="sxs-lookup"><span data-stu-id="4efa0-113">Add the SQL Server store mirror for the secondary database.</span></span>
    
    6.  <span data-ttu-id="4efa0-114">Publiez la topologie.</span><span class="sxs-lookup"><span data-stu-id="4efa0-114">Publish the topology.</span></span>

<span data-ttu-id="4efa0-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4efa0-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

