---
title: 'Lync Server 2013 : restauration des données et des paramètres'
description: 'Lync Server 2013 : restauration des données et des paramètres.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring data and settings
ms:assetid: b07f5dd7-7bed-4819-8cb5-617f5acd478e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202185(v=OCS.15)
ms:contentKeyID: 51541503
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 694b1e362d729d354b08367d31c47e8ca866dd91
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442529"
---
# <a name="restoring-data-and-settings-in-lync-server-2013"></a><span data-ttu-id="8e578-103">Restauration de données et de paramètres dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e578-103">Restoring data and settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8e578-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8e578-104">

<span> </span></span></span>

<span data-ttu-id="8e578-105">_**Dernière modification de la rubrique :** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="8e578-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="8e578-106">Si vous avez implémenté une topologie de récupération d’urgence avec des pools couplés, et que l’un de ces pools frontals a disparu et que vous avez besoin de restaurer rapidement le service auprès de vos utilisateurs, voir [échec d’un pool dans Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span><span class="sxs-lookup"><span data-stu-id="8e578-106">If you have implemented a disaster recovery topology with paired pools, and one of those Front End pools has gone down and you need to quickly restore service to your users, see [Failing over a pool in Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span></span> <span data-ttu-id="8e578-107">Dans le cas contraire, utilisez les informations des rubriques suivantes, ainsi que les feuilles de calcul dans les [feuilles de calcul de sauvegarde et de restauration pour Lync server 2013](lync-server-2013-backup-and-restoration-worksheets.md), pour restaurer Lync Server suite à un échec ou une panne.</span><span class="sxs-lookup"><span data-stu-id="8e578-107">Otherwise, use the information in the following topics, along with the worksheets in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md), to restore Lync Server after a failure or outage.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8e578-108">Pour réduire les temps d’arrêt et la perte de données potentielle, effectuez les procédures de restauration décrites dans ce document uniquement si les procédures de dépannage ne sont pas efficaces pour identifier et corriger le problème.</span><span class="sxs-lookup"><span data-stu-id="8e578-108">To reduce downtime and potential data loss, perform the restoration procedures described in this document only if troubleshooting procedures are not effective in identifying and correcting the problem.</span></span> <span data-ttu-id="8e578-109">Lors de la résolution des problèmes, essayez de réduire l’impact sur les autres serveurs et composants à mesure que vous arrêtez et redémarrez les serveurs.</span><span class="sxs-lookup"><span data-stu-id="8e578-109">During troubleshooting, try to minimize the impact on other servers and components as you shut down and restart servers.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="8e578-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="8e578-110">In This Section</span></span>

  - [<span data-ttu-id="8e578-111">Préparation de la restauration de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e578-111">Preparing to restore Lync Server 2013</span></span>](lync-server-2013-preparing-to-restore-lync-server.md)

  - [<span data-ttu-id="8e578-112">Restauration d’un serveur Standard Edition Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e578-112">Restoring a Standard Edition server in Lync Server 2013</span></span>](lync-server-2013-restoring-a-standard-edition-server.md)

  - [<span data-ttu-id="8e578-113">Restauration du serveur qui héberge le magasin de gestion central dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e578-113">Restoring the server hosting the Central Management store in Lync Server 2013</span></span>](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md)

  - [<span data-ttu-id="8e578-114">Restauration d’un serveur principal Enterprise Edition dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e578-114">Restoring an Enterprise Edition Back End Server in Lync Server 2013</span></span>](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md)

  - [<span data-ttu-id="8e578-115">Restauration d’un serveur membre Enterprise Edition dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e578-115">Restoring an Enterprise Edition member server in Lync Server 2013</span></span>](lync-server-2013-restoring-an-enterprise-edition-member-server.md)

  - [<span data-ttu-id="8e578-116">Restauration d’un pool de serveurs Lync dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e578-116">Restoring a Lync Server pool in Lync Server 2013</span></span>](lync-server-2013-restoring-a-lync-server-pool.md)

  - [<span data-ttu-id="8e578-117">Exécution d’un basculement de pool frontal ABC dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e578-117">Performing an ABC Front End pool failover in Lync Server 2013</span></span>](lync-server-2013-performing-an-abc-front-end-pool-failover.md)

  - [<span data-ttu-id="8e578-118">Restauration d’un magasin de fichiers dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e578-118">Restoring a file store in Lync Server 2013</span></span>](lync-server-2013-restoring-a-file-store.md)

  - [<span data-ttu-id="8e578-119">Restauration de données d’analyse ou d’archivage dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e578-119">Restoring monitoring or archiving data in Lync Server 2013</span></span>](lync-server-2013-restoring-monitoring-or-archiving-data.md)

  - [<span data-ttu-id="8e578-120">Restauration de données de conversations permanentes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e578-120">Restoring Persistent Chat data in Lync Server 2013</span></span>](lync-server-2013-restoring-persistent-chat-data.md)

<span data-ttu-id="8e578-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8e578-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

