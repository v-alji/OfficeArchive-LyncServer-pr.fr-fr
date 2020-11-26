---
title: 'Lync Server 2013 : développement d’une stratégie de sauvegarde et de restauration'
description: 'Lync Server 2013 : développement d’une stratégie et d’un plan de sauvegarde et de restauration.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Developing a backup and restoration strategy and plan
ms:assetid: 17599b76-1a84-4dd6-b695-c19637deb8a6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202164(v=OCS.15)
ms:contentKeyID: 51541447
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3d55eeb541cdde5c43d7d680ceb212d87da0d517
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429448"
---
# <a name="developing-a-backup-and-restoration-strategy-and-plan-for-lync-server-2013"></a><span data-ttu-id="30e7f-103">Développement d’une stratégie de sauvegarde et de restauration et planification pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30e7f-103">Developing a backup and restoration strategy and plan for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="30e7f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="30e7f-104">

<span> </span></span></span>

<span data-ttu-id="30e7f-105">_**Dernière modification de la rubrique :** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="30e7f-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="30e7f-106">L’efficacité de vos opérations de sauvegarde et de restauration de Lync Server dépend de la stratégie et de la planification de la sauvegarde et de la restauration.</span><span class="sxs-lookup"><span data-stu-id="30e7f-106">The effectiveness of your Lync Server backup and restoration operations depends on your backup and restoration strategy and plan.</span></span> <span data-ttu-id="30e7f-107">Vous devez établir une stratégie de sauvegarde et de restauration d’un serveur Lync qui s’adapte à la stratégie globale de votre organisation, ainsi qu’un plan complet et concis pour la sauvegarde des données et des paramètres, et, en cas de panne, un plan de restauration des services.</span><span class="sxs-lookup"><span data-stu-id="30e7f-107">You should establish a strategy for backing up and restoring Lync Server that fits with your organization's overall strategy, and a comprehensive, concise plan for backing up data and settings, and, in the event of an outage, a plan for restoring service.</span></span>

<span data-ttu-id="30e7f-108">Dans le cas d’une reprise après sinistre plus fiable d’un pool frontal, utilisez la topologie de reprise de sinistre de réserve de réserve introduite dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="30e7f-108">For the most robust disaster recovery of a Front End Pool, use the paired-pool disaster recovery topology introduced in Lync Server 2013.</span></span> <span data-ttu-id="30e7f-109">Pour plus d’informations, reportez-vous à [planification d’une haute disponibilité et reprise après sinistre dans Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="30e7f-109">For more information, see [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="30e7f-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="30e7f-110">In This Section</span></span>

  - [<span data-ttu-id="30e7f-111">Établissement d’une stratégie de sauvegarde et de restauration pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30e7f-111">Establishing a backup and restoration strategy for Lync Server 2013</span></span>](lync-server-2013-establishing-a-backup-and-restoration-strategy.md)

  - [<span data-ttu-id="30e7f-112">Établissement d’un plan de sauvegarde et de restauration pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30e7f-112">Establishing a backup and restoration plan for Lync Server 2013</span></span>](lync-server-2013-establishing-a-backup-and-restoration-plan.md)

  - [<span data-ttu-id="30e7f-113">Configuration d’un emplacement de sauvegarde pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30e7f-113">Setting up a backup location for Lync Server 2013</span></span>](lync-server-2013-setting-up-a-backup-location.md)

<span data-ttu-id="30e7f-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="30e7f-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

