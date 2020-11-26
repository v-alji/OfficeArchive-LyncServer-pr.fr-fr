---
title: 'Lync Server 2013 : sauvegarde et restauration de Lync Server'
description: 'Lync Server 2013 : sauvegarde et restauration de Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up and restoring Lync Server 2013
ms:assetid: 07dc1f5e-af66-4e18-bf39-881dceff8bc3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202160(v=OCS.15)
ms:contentKeyID: 51541443
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1a7024b2264fb895d1562a6da0775f9397644b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438140"
---
# <a name="backing-up-and-restoring-lync-server-2013"></a><span data-ttu-id="4b2e5-103">Sauvegarde et restauration de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4b2e5-103">Backing up and restoring Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4b2e5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4b2e5-104">

<span> </span></span></span>

<span data-ttu-id="4b2e5-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="4b2e5-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="4b2e5-106">Cette section présente les meilleures pratiques en matière de sauvegarde de vos données 2013 Lync Server et de restauration en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="4b2e5-106">In this section, you’ll find the best practices for backing up your Lync Server 2013 data, and for restoring it if you have a failure.</span></span> <span data-ttu-id="4b2e5-107">Ces bonnes pratiques s’appliquent aux situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4b2e5-107">These best practices apply to the following situations:</span></span>

  - <span data-ttu-id="4b2e5-108">Un pool de serveurs Lync de n’importe quel type (serveur frontal, serveur Edge, serveur de médiation, serveur de chat permanent ou directeur), ou un serveur individuel dans l’un de ces groupes.</span><span class="sxs-lookup"><span data-stu-id="4b2e5-108">An entire Lync Server pool of any type (Front End Server, Edge Server, Mediation Server, Persistent Chat Server, or Director), or an individual server in one of these pools.</span></span>

  - <span data-ttu-id="4b2e5-109">Serveur de gestion central</span><span class="sxs-lookup"><span data-stu-id="4b2e5-109">The Central Management Server</span></span>

  - <span data-ttu-id="4b2e5-110">Un serveur Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="4b2e5-110">A Standard Edition server</span></span>

  - <span data-ttu-id="4b2e5-111">Serveur principal d’Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="4b2e5-111">An Enterprise Edition Back End Server</span></span>

  - <span data-ttu-id="4b2e5-112">Magasin de fichiers</span><span class="sxs-lookup"><span data-stu-id="4b2e5-112">A File Store</span></span>

  - <span data-ttu-id="4b2e5-113">Une base de données d’archivage, une base de données de surveillance ou une base de données de chat permanent</span><span class="sxs-lookup"><span data-stu-id="4b2e5-113">An Archiving database, Monitoring database, or Persistent Chat database</span></span>

<span data-ttu-id="4b2e5-114">Cette section n’inclut pas d’informations sur la restauration d’un site entier ou sur le développement d’un site de secours.</span><span class="sxs-lookup"><span data-stu-id="4b2e5-114">This section does not include information about restoring an entire site or for developing a standby site.</span></span> <span data-ttu-id="4b2e5-115">Pour plus d’informations sur le développement d’une solution de reprise après sinistre avec des listes frontales couplées, voir [planification d’une haute disponibilité et reprise après sinistre dans Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="4b2e5-115">For details about developing a disaster recovery solution with paired Front End pools, see [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span> <span data-ttu-id="4b2e5-116">Il s’agit de la méthode recommandée pour la planification de la reprise après sinistre.</span><span class="sxs-lookup"><span data-stu-id="4b2e5-116">This is the recommended method for planning for disaster recovery.</span></span>

<span data-ttu-id="4b2e5-117">Si vous avez déployé des pools frontaux couplés, si l’un de ces groupes échoue et devient irrécupérable, vous pouvez restaurer ce pool avec un nouveau nom de domaine complet (FQDN) du pool couplé.</span><span class="sxs-lookup"><span data-stu-id="4b2e5-117">If you have deployed paired Front End pools, if one of these pools fails and becomes unrecoverable, you can restore this pool with a new fully qualified domain name (FQDN) from its paired pool.</span></span> <span data-ttu-id="4b2e5-118">Pour plus d’informations sur la procédure d’exécution de cette récupération, voir [échec d’un pool dans Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span><span class="sxs-lookup"><span data-stu-id="4b2e5-118">For details on the steps to perform this recovery, see [Failing over a pool in Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span></span> <span data-ttu-id="4b2e5-119">Par ailleurs, si vous voulez recréer un pool failed et unrécupérable qui faisait partie d’une paire frontale, vous pouvez suivre la procédure décrite dans la section [exécution d’un basculement de pool frontal ABC dans Lync Server 2013](lync-server-2013-performing-an-abc-front-end-pool-failover.md).</span><span class="sxs-lookup"><span data-stu-id="4b2e5-119">Additionally, if you later want to recreate a failed and unrecoverable pool that was part of a Front End pair, you can use the steps in [Performing an ABC Front End pool failover in Lync Server 2013](lync-server-2013-performing-an-abc-front-end-pool-failover.md).</span></span>

<span data-ttu-id="4b2e5-120">La méthodologie décrite dans ce document implique des considérations spéciales lors de la phase de planification.</span><span class="sxs-lookup"><span data-stu-id="4b2e5-120">The methodology described in this document involves special considerations during the planning phase.</span></span> <span data-ttu-id="4b2e5-121">Pour plus d’informations, reportez-vous à [la rubrique établissement d’un plan de sauvegarde et de restauration pour Lync Server 2013](lync-server-2013-establishing-a-backup-and-restoration-plan.md).</span><span class="sxs-lookup"><span data-stu-id="4b2e5-121">For details, see [Establishing a backup and restoration plan for Lync Server 2013](lync-server-2013-establishing-a-backup-and-restoration-plan.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="4b2e5-122">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="4b2e5-122">In This Section</span></span>

  - [<span data-ttu-id="4b2e5-123">Préparation pour la sauvegarde et la restauration de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4b2e5-123">Preparing for Lync Server 2013 backup and restoration</span></span>](lync-server-2013-preparing-for-lync-server-backup-and-restoration.md)

  - [<span data-ttu-id="4b2e5-124">Sauvegarder des données et des paramètres dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4b2e5-124">Backing up data and settings in Lync Server 2013</span></span>](lync-server-2013-backing-up-data-and-settings.md)

  - [<span data-ttu-id="4b2e5-125">Restauration de données et de paramètres dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4b2e5-125">Restoring data and settings in Lync Server 2013</span></span>](lync-server-2013-restoring-data-and-settings.md)

  - [<span data-ttu-id="4b2e5-126">Sauvegarder et restaurer des feuilles de calcul pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4b2e5-126">Backup and restoration worksheets for Lync Server 2013</span></span>](lync-server-2013-backup-and-restoration-worksheets.md)

<span data-ttu-id="4b2e5-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4b2e5-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

