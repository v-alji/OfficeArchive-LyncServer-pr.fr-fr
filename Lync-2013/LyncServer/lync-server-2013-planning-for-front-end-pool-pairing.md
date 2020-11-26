---
title: 'Lync Server 2013 : Planification du jumelage de pools frontaux'
description: 'Lync Server 2013 : planification pour le jumelage du pool frontal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Front End pool pairing
ms:assetid: cca5773d-57ff-45ce-a7b4-f82ae697c477
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205293(v=OCS.15)
ms:contentKeyID: 48185508
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ac235cf682e286132836e13b34b457adf2bfc233
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424561"
---
# <a name="planning-for-front-end-pool-pairing-in-lync-server-2013"></a><span data-ttu-id="d80a8-103">Planification du jumelage de pools frontaux dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d80a8-103">Planning for Front End pool pairing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d80a8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d80a8-104">

<span> </span></span></span>

<span data-ttu-id="d80a8-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="d80a8-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="d80a8-106">Pour les meilleures capacités de reprise après sinistre dans Lync Server 2013, le déploiement de paires de pools front-end sur deux sites à dispersion géographique.</span><span class="sxs-lookup"><span data-stu-id="d80a8-106">For the best disaster recovery abilities in Lync Server 2013, deploy pairs of Front End pools across two geographically dispersed sites.</span></span> <span data-ttu-id="d80a8-107">Chaque site comporte une réserve frontale associée à un pool frontal correspondant dans l’autre site.</span><span class="sxs-lookup"><span data-stu-id="d80a8-107">Each site contains a Front End pool which is paired with a corresponding Front End pool in the other site.</span></span> <span data-ttu-id="d80a8-108">Les deux sites sont actifs et le service de sauvegarde de Lync Server fournit la réplication des données en temps réel pour que les pools restent synchronisés.</span><span class="sxs-lookup"><span data-stu-id="d80a8-108">Both sites are active, and the Lync Server Backup Service provides real-time data replication to keep the pools synchronized.</span></span> <span data-ttu-id="d80a8-109">Le service de sauvegarde est une nouvelle fonctionnalité de Lync Server 2013 conçue pour prendre en charge la solution de reprise après sinistre.</span><span class="sxs-lookup"><span data-stu-id="d80a8-109">The Backup Service is a new feature in Lync Server 2013, designed to support the disaster recovery solution.</span></span> <span data-ttu-id="d80a8-110">Elle est installée sur un pool frontal lorsque vous jumelez la liste avec un autre pool frontal.</span><span class="sxs-lookup"><span data-stu-id="d80a8-110">It is installed on a Front End pool when you pair the pool with another Front End pool.</span></span>

<span data-ttu-id="d80a8-111">En cas d’échec du pool dans un site, vous pouvez faire basculer les utilisateurs de ce groupe vers le pool dans l’autre site, qui fournit ensuite les services à tous les utilisateurs des deux groupes.</span><span class="sxs-lookup"><span data-stu-id="d80a8-111">If the pool in one site fails, you can fail over the users from that pool to the pool in the other site, which then provides services to all the users in both pools.</span></span> <span data-ttu-id="d80a8-112">Dans le cadre de la planification de la capacité, chaque pool doit être conçu pour gérer les charges de travail de tous les utilisateurs dans les deux pools en cas de sinistre.</span><span class="sxs-lookup"><span data-stu-id="d80a8-112">For capacity planning purposes, each pool should be designed to handle the workloads of all users in both pools in the event of a disaster.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d80a8-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d80a8-113">In This Section</span></span>

  - [<span data-ttu-id="d80a8-114">Options de jumelage de pool prises en charge et meilleures pratiques pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d80a8-114">Supported pool pairing options and best practices for Lync Server 2013</span></span>](lync-server-2013-supported-pool-pairing-options-and-best-practices.md)

  - [<span data-ttu-id="d80a8-115">Relations des serveurs d’inscriptions de sauvegarde dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d80a8-115">Backup Registrar relationships in Lync Server 2013</span></span>](lync-server-2013-backup-registrar-relationships.md)

  - [<span data-ttu-id="d80a8-116">Temps de récupération nécessaire pour basculer et restaurer les pools dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d80a8-116">Recovery time for pool failover and pool failback in Lync Server 2013</span></span>](lync-server-2013-recovery-time-for-pool-failover-and-pool-failback.md)

  - [<span data-ttu-id="d80a8-117">Basculement du magasin central de gestion dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d80a8-117">Central Management store failover in Lync Server 2013</span></span>](lync-server-2013-central-management-store-failover.md)

  - [<span data-ttu-id="d80a8-118">Sécurité des données d’appariement de pools frontaux dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d80a8-118">Front End pool pairing data security in Lync Server 2013</span></span>](lync-server-2013-front-end-pool-pairing-data-security.md)

<span data-ttu-id="d80a8-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d80a8-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

