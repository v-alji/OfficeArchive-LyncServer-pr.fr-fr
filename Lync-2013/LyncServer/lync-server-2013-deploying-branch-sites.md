---
title: 'Lync Server 2013 : Déploiement de sites de succursale'
description: 'Lync Server 2013 : déploiement de sites de succursales.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying branch sites
ms:assetid: 1475dee0-66ae-4ee5-b6f1-7409b4bbff45
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398217(v=OCS.15)
ms:contentKeyID: 48183483
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d653e3f06de832693d97bfb229f122a67c28640e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430090"
---
# <a name="deploying-branch-sites-in-lync-server-2013"></a><span data-ttu-id="5444a-103">Déploiement de sites de succursale dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5444a-103">Deploying branch sites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5444a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5444a-104">

<span> </span></span></span>

<span data-ttu-id="5444a-105">_**Dernière modification de la rubrique :** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="5444a-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="5444a-106">Les utilisateurs du site de succursale obtiennent la plupart des fonctionnalités de Lync Server 2013 du serveur sur le site central auquel le site de succursale est associé.</span><span class="sxs-lookup"><span data-stu-id="5444a-106">Branch site users get most of their Lync Server 2013 functionality from the server at the central site that the branch site is associated with.</span></span> <span data-ttu-id="5444a-107">Chaque site de filiale est associé à un seul site central.</span><span class="sxs-lookup"><span data-stu-id="5444a-107">Each branch site is associated with exactly one central site.</span></span> <span data-ttu-id="5444a-108">Pour passer des appels vers et à partir du réseau téléphonique public commuté (RTC), un site de succursale peut comporter l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5444a-108">To provide calls to and from the public switched telephone network (PSTN), a branch site might contain any of the following:</span></span>

  - <span data-ttu-id="5444a-109">Passerelle RTC et éventuellement un serveur méditation</span><span class="sxs-lookup"><span data-stu-id="5444a-109">A PSTN gateway and possibly a Meditation Server</span></span>

  - <span data-ttu-id="5444a-110">Un Trunk SIP</span><span class="sxs-lookup"><span data-stu-id="5444a-110">A SIP trunk</span></span>

  - <span data-ttu-id="5444a-111">Une infrastructure vocale existante avec un échange de succursale privée (PBX)</span><span class="sxs-lookup"><span data-stu-id="5444a-111">An existing voice infrastructure with a private branch exchange (PBX)</span></span>

  - <span data-ttu-id="5444a-112">Appareil de branchement survivant</span><span class="sxs-lookup"><span data-stu-id="5444a-112">A Survivable Branch Appliance</span></span>

  - <span data-ttu-id="5444a-113">Serveur de succursales survivant</span><span class="sxs-lookup"><span data-stu-id="5444a-113">A Survivable Branch Server</span></span>

<span data-ttu-id="5444a-114">Les sites de succursales disposant d’une unité de branchement plus survivant ou d’un serveur de succursales survivant sont plus résilients en cas d’échecs de réseaux larges ou de sites de succursales sans l’une de ces solutions.</span><span class="sxs-lookup"><span data-stu-id="5444a-114">Branch sites with a Survivable Branch Appliance or a Survivable Branch Server are more resilient in times of wide-area network or central site failures than branch sites without one of these solutions.</span></span> <span data-ttu-id="5444a-115">Par exemple, dans le cas d’un site disposant d’une branche ou d’un serveur de succursale survivant, les utilisateurs peuvent toujours passer et recevoir des appels RTC si le réseau qui se connecte au site central est arrêté.</span><span class="sxs-lookup"><span data-stu-id="5444a-115">For example, in a site with a Survivable Branch Appliance or a Survivable Branch Server deployed, users can still make and receive PSTN calls if the network connecting the branch site to the central site is down.</span></span> <span data-ttu-id="5444a-116">Une autre méthode pour obtenir la résilience du site d’une succursale consiste à utiliser une passerelle PSTN ou une ligne SIP avec un déploiement de Lync Server à grande échelle sur le site de la succursale.</span><span class="sxs-lookup"><span data-stu-id="5444a-116">Another way to achieve branch-site resiliency is by using a PSTN gateway or a SIP trunk with a full-scale Lync Server deployment at the branch site.</span></span>

<span data-ttu-id="5444a-117">Pour en savoir plus sur le déploiement de sites de succursale approprié pour votre organisation, notamment les conditions préalables et d’autres considérations en matière de planification, voir [planification de la connectivité PSTN dans Lync server 2013](lync-server-2013-planning-for-pstn-connectivity.md) et [planification de la résilience vocale dans Lync Server 2013](lync-server-2013-planning-for-branch-site-voice-resiliency.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="5444a-117">For details about which branch site deployment is right for your organization, including prerequisites and other planning considerations, see [Planning for PSTN connectivity in Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md) and [Planning for branch-site voice resiliency in Lync Server 2013](lync-server-2013-planning-for-branch-site-voice-resiliency.md) in the Planning documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5444a-118">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="5444a-118">In This Section</span></span>

  - [<span data-ttu-id="5444a-119">Connectivité RTC sur un site de succursale dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5444a-119">Providing PSTN connectivity at a branch site in Lync Server 2013</span></span>](lync-server-2013-providing-pstn-connectivity-at-a-branch-site.md)

  - [<span data-ttu-id="5444a-120">Déploiement d’un Survivable Branch Appliance ou d’un serveur Survivable Branch Server avec Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5444a-120">Deploying a Survivable Branch Appliance or Server with Lync Server 2013</span></span>](lync-server-2013-deploying-a-survivable-branch-appliance-or-server.md)

<span data-ttu-id="5444a-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5444a-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

