---
title: Relations des serveurs d’inscriptions de sauvegarde dans Lync Server 2013
description: Lync Server 2013 Backup Registrar relations.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backup Registrar relationships
ms:assetid: 7e078271-84b9-4666-989c-c4507a0cdf4a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205033(v=OCS.15)
ms:contentKeyID: 48184631
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7b0bfce6444ae78c2fb792a6d63dba4bf36b1791
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437916"
---
# <a name="backup-registrar-relationships-in-lync-server-2013"></a><span data-ttu-id="3f066-103">Relations des serveurs d’inscriptions de sauvegarde dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f066-103">Backup Registrar relationships in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f066-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f066-104">

<span> </span></span></span>

<span data-ttu-id="3f066-105">_**Dernière modification de la rubrique :** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="3f066-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="3f066-106">En plus de fournir une fonctionnalité de récupération d’urgence, deux pools associés jouent le rôle de serveur d’inscriptions de sauvegarde l’un pour l’autre.</span><span class="sxs-lookup"><span data-stu-id="3f066-106">In addition to providing disaster recovery ability, two paired pools serve as the backup Registrars for each other.</span></span> <span data-ttu-id="3f066-107">Dans Lync Server 2013, les relations de registre de secours entre les pools frontal sont toujours 1:1 et réciproques.</span><span class="sxs-lookup"><span data-stu-id="3f066-107">In Lync Server 2013, backup Registrar relationships between Front End pools are always 1:1 and reciprocal.</span></span> <span data-ttu-id="3f066-108">En d’autres termes, si P1 est la sauvegarde pour P2, P2 doit être la sauvegarde de P1, et aucune de ses autres listes frontales ne peut être sauvegardée.</span><span class="sxs-lookup"><span data-stu-id="3f066-108">This means that if P1 is the backup for P2, then P2 must be the backup for P1, and neither can be the backup for any other Front End pool.</span></span> <span data-ttu-id="3f066-109">Il s’agit d’une modification de Lync Server 2010, qui peut être un grand nombre d’une relation de sauvegarde de pool frontal.</span><span class="sxs-lookup"><span data-stu-id="3f066-109">This is a change from Lync Server 2010, in which Front End pool backup relationships could be many to one.</span></span>

<span data-ttu-id="3f066-110">Même si les relations de sauvegarde entre les deux pools front-end doivent être 1:1 et symétriques, chaque pool frontal peut également être le Bureau d’enregistrement de sauvegarde pour n’importe quel nombre d’appareils plus survivant, comme dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3f066-110">Even though backup relationships between two Front End pools must be 1:1 and symmetrical, each Front End pool can still also be the backup registrar for any number of Survivable Branch Appliances, just as in Lync Server 2010.</span></span>

<span data-ttu-id="3f066-111">Notez que Lync Server 2013 n’étend pas l’assistance de reprise après sinistre aux utilisateurs hébergés sur un appareil de succursales survivant.</span><span class="sxs-lookup"><span data-stu-id="3f066-111">Note that Lync Server 2013 does not extend disaster recovery support to users homed on a Survivable Branch Appliance.</span></span> <span data-ttu-id="3f066-112">Dans le cas d’un pool frontal qui sert de sauvegarde pour une unité de branchement Survivable, les utilisateurs connectés à l’unité de branchement Survivable peuvent passer en mode de résilience, même si les utilisateurs hébergés sur le pool frontal ont basculé vers le pool frontal de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="3f066-112">If a Front End pool that serves as the backup for a Survivable Branch Appliance goes down, users signed into the Survivable Branch Appliance fall into resiliency mode even after users homed on the Front End pool are failed over to the backup Front End pool.</span></span>

<span data-ttu-id="3f066-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f066-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

