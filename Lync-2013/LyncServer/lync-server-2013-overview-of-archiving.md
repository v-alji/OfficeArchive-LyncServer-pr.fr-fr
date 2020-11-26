---
title: 'Lync Server 2013 : Vue d’ensemble de l’archivage'
description: 'Lync Server 2013 : vue d’ensemble de l’archivage.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Archiving
ms:assetid: 1e3c2ef1-f561-4f57-8b6a-7d78addc1ed1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204729(v=OCS.15)
ms:contentKeyID: 48183570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 548d82d6731fd28fafbde5816a7a0dc77a1fcc02
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424827"
---
# <a name="overview-of-archiving-in-lync-server-2013"></a><span data-ttu-id="932e1-103">Vue d’ensemble de l’archivage dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="932e1-103">Overview of Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="932e1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="932e1-104">

<span> </span></span></span>

<span data-ttu-id="932e1-105">_**Dernière modification de la rubrique :** 2013-09-30_</span><span class="sxs-lookup"><span data-stu-id="932e1-105">_**Topic Last Modified:** 2013-09-30_</span></span>

<span data-ttu-id="932e1-106">L’archivage dans Lync Server 2013 offre un moyen d’archiver les communications envoyées via Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="932e1-106">Archiving in Lync Server 2013 provides a way for you to archive communications that are sent through Lync Server 2013.</span></span>

<span data-ttu-id="932e1-107">Vous pouvez implémenter l’archivage dans le cadre de votre déploiement initial de Lync Server 2013 ou vous pouvez l’ajouter à un déploiement existant.</span><span class="sxs-lookup"><span data-stu-id="932e1-107">You can implement Archiving as part of your initial Lync Server 2013 deployment, or you can add it to an existing deployment.</span></span> <span data-ttu-id="932e1-108">Pour utiliser les bases de données d’archivage de Lync Server 2013 (bases de données SQL Server) pour le stockage des données d’archivage, vous devez utiliser le générateur de topologie pour ajouter les bases de données à votre topologie, puis publier une nouvelle topologie.</span><span class="sxs-lookup"><span data-stu-id="932e1-108">To use Lync Server 2013 Archiving databases (SQL Server databases) for storage of archiving data, you use Topology Builder to add the databases to your topology, and then publish the topology again.</span></span> <span data-ttu-id="932e1-109">Si tous vos utilisateurs sont hébergés sur Exchange 2013 et que leurs boîtes aux lettres sont placées sur In-Place attente, il n’est pas nécessaire de mettre à jour votre topologie, mais vous n’avez besoin de configurer l’intégration de Microsoft Exchange pour le stockage des données archivées dans Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="932e1-109">If all your users are homed on Exchange 2013 and have their mailboxes put on In-Place Hold, you do not have to update your topology, but only need to enable Microsoft Exchange integration to store archived data in Exchange 2013.</span></span>

<span data-ttu-id="932e1-110">Lors de l’implémentation de l’archivage, vous devez le configurer pour spécifier ce qui est archivé.</span><span class="sxs-lookup"><span data-stu-id="932e1-110">When you implement Archiving, you configure it to specify what is archived.</span></span> <span data-ttu-id="932e1-111">Par défaut, rien n’est archivé.</span><span class="sxs-lookup"><span data-stu-id="932e1-111">By default, nothing is archived.</span></span> <span data-ttu-id="932e1-112">Vous pouvez configurer et gérer l’archivage à l’aide du panneau de configuration de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="932e1-112">You configure and manage Archiving by using Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="932e1-113">Vous pouvez implémenter l’archivage des communications internes, des communications externes ou les deux.</span><span class="sxs-lookup"><span data-stu-id="932e1-113">You can implement Archiving for internal communications, external communications, or both.</span></span> <span data-ttu-id="932e1-114">Vous pouvez configurer les paramètres d’archivage de votre organisation entière et, si vous le souhaitez, pour des sites et des groupes d’utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="932e1-114">You can configure archiving settings your entire organization and, optionally, for specific sites, specific pools, and specific users and user groups.</span></span> <span data-ttu-id="932e1-115">Pour plus d’informations sur la définition des options appropriées pour votre organisation, reportez-vous à la rubrique [définition de vos exigences d’archivage dans Lync Server 2013](lync-server-2013-defining-your-requirements-for-archiving.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="932e1-115">For details about determining the appropriate options for your organization, see [Defining your requirements for Archiving in Lync Server 2013](lync-server-2013-defining-your-requirements-for-archiving.md) in the Planning documentation.</span></span> <span data-ttu-id="932e1-116">Pour plus d’informations sur l’implémentation de stratégies d’archivage et de configurations et sur les informations qui peuvent ou ne peuvent pas être archivées, voir fonctionnement [de l’archivage dans Lync Server 2013](lync-server-2013-how-archiving-works.md) dans la documentation de planification, la documentation de déploiement ou les opérations.</span><span class="sxs-lookup"><span data-stu-id="932e1-116">For details about how Archiving policies and configurations are implemented, and details about what information can or cannot be archived, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<span data-ttu-id="932e1-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="932e1-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

