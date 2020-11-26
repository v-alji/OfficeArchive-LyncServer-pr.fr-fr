---
title: 'Lync Server 2013 : Déploiement d’un Survivable Branch Appliance ou d’un serveur Survivable Branch Server'
description: 'Lync Server 2013 : déploiement d’une unité ou d’un serveur de succursales survivant.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying a Survivable Branch Appliance or Server
ms:assetid: cb780c14-dc5f-41ba-8092-f20ae905bd16
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398849(v=OCS.15)
ms:contentKeyID: 48185643
ms.date: 12/11/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b8c8610ab85b61d33a5f181f1d5f51d0e5095f49
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430118"
---
# <a name="deploying-a-survivable-branch-appliance-or-server-with-lync-server-2013"></a><span data-ttu-id="db264-103">Déploiement d’un Survivable Branch Appliance ou d’un serveur Survivable Branch Server avec Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="db264-103">Deploying a Survivable Branch Appliance or Server with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="db264-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="db264-104">

<span> </span></span></span>

<span data-ttu-id="db264-105">_**Dernière modification de la rubrique :** 2014-12-10_</span><span class="sxs-lookup"><span data-stu-id="db264-105">_**Topic Last Modified:** 2014-12-10_</span></span>

<span data-ttu-id="db264-106">Le mode de résilience d’entreprise résilient désigne la résilience du site de succursale, c’est-à-dire la possibilité de fournir un service voix entreprise continu aux utilisateurs de sites de succursales en cas d’indisponibilité du lien vers le site central.</span><span class="sxs-lookup"><span data-stu-id="db264-106">Resilient Enterprise Voice refers to branch-site resiliency, that is, the ability to provide continuous Enterprise Voice service to branch site users in the event that the link to the central site becomes unavailable.</span></span>

<span data-ttu-id="db264-107">Pour les sites de petites et moyennes succursales (sites de succursales avec 25 à 1 000 utilisateurs), nous vous recommandons de déployer une application de succursales survivant qui arrêtera les appels de réseau téléphonique commuté (PSTN) à l’aide de sa passerelle PSTN intégrée ou d’un Trunk SIP à un fournisseur de services de téléphonie.</span><span class="sxs-lookup"><span data-stu-id="db264-107">For small and medium-sized branch sites (branch sites with 25 to 1,000 users), we recommend deploying a Survivable Branch Appliance, which will terminate public switched telephone network (PSTN) calls by using its built-in PSTN gateway or a SIP trunk to a telephone service provider.</span></span> <span data-ttu-id="db264-108">Une branche Survivable est un périphérique tiers qui inclut un serveur Blade exécutant le système d’exploitation Windows Server 2008 R2, le Bureau d’enregistrement Lync Server 2013, le logiciel serveur de médiation et une passerelle RTC, le tout dans un seul châssis d’appareil.</span><span class="sxs-lookup"><span data-stu-id="db264-108">A Survivable Branch Appliance is a third-party device that includes a blade server running the Windows Server 2008 R2 operating system, Lync Server 2013 Registrar, Mediation Server software, and a PSTN gateway, all in a single appliance chassis.</span></span>

<span data-ttu-id="db264-109">Pour les sites de succursales avec 1 000 à 5 000 et sans réseau étendu fiable, nous recommandons un serveur de succursale survivant connecté à une passerelle PSTN ou un Trunk SIP à un fournisseur de services de téléphonie.</span><span class="sxs-lookup"><span data-stu-id="db264-109">For branch sites with 1,000 to 5,000 users and no resilient WAN, we recommend a Survivable Branch Server connected to either a PSTN gateway or a SIP trunk to a telephone service provider.</span></span> <span data-ttu-id="db264-110">Un serveur de succursales survivant est un ordinateur Windows Server sur lequel est installé le logiciel de bureau d’enregistrement et de médiation.</span><span class="sxs-lookup"><span data-stu-id="db264-110">A Survivable Branch Server is a Windows Server-based computer that has Registrar and Mediation Server software installed on it.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="db264-111">Pour les sites de succursales ayant plus de 5 000 utilisateurs et les administrateurs Lync Server dédiés, nous vous recommandons d’utiliser un déploiement complet de Lync Server 2013, distinct de celui du site central.</span><span class="sxs-lookup"><span data-stu-id="db264-111">For branch sites with more than 5,000 users and dedicated Lync Server administrators, we recommend a full Lync Server 2013 deployment, separate from that of the central site.</span></span><BR><span data-ttu-id="db264-112">Pour plus d’informations sur le choix de la meilleure solution de résilience pour les sites de succursales au sein de votre organisation, notamment la configuration requise et les considérations en matière de planification, voir <A href="lync-server-2013-branch-site-resiliency-requirements.md">exigences de résilience de succursale pour Lync Server 2013</A> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="db264-112">For details about choosing the best resiliency solution for the branch sites in your organization, including prerequisites and planning considerations, see <A href="lync-server-2013-branch-site-resiliency-requirements.md">Branch-site resiliency requirements for Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="db264-113">Les utilisateurs qui sont hébergés sur une unité de branchement Survivable Lync Server ne peuvent pas créer de nouvelles salles de conversation ou afficher la carte de la salle pour les salles existantes.</span><span class="sxs-lookup"><span data-stu-id="db264-113">Users who are homed on a Lync Server Survivable Branch Appliance are unable to create new chat rooms or view the room card for existing rooms.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="db264-114">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="db264-114">In This Section</span></span>

  - [<span data-ttu-id="db264-115">Déploiement d’un Survivable Branch Appliance ou d’un serveur Survivable Branch Server avec Lync Server 2013 - Tâches pour un site central</span><span class="sxs-lookup"><span data-stu-id="db264-115">Deploying a Survivable Branch Appliance or Server with Lync Server 2013 - central site tasks</span></span>](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md)

  - [<span data-ttu-id="db264-116">Déploiement d’un Survivable Branch Appliance ou d’un serveur Survivable Branch Server sur un site de succursale avec Lync Server 2013 - tâche de site de succursale</span><span class="sxs-lookup"><span data-stu-id="db264-116">Deploy a Survivable Branch Appliance or Server with Lync Server 2013 - branch site task</span></span>](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md)

  - [<span data-ttu-id="db264-117">Configuration des utilisateurs pour la résistance de sites de succursale dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="db264-117">Configuring users for branch site resiliency in Lync Server 2013</span></span>](lync-server-2013-configuring-users-for-branch-site-resiliency.md)

  - [<span data-ttu-id="db264-118">Hébergement des utilisateurs sur un Survivable Branch Appliance ou un serveur Survivable Branch Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="db264-118">Home users on a Survivable Branch Appliance or Server in Lync Server 2013</span></span>](lync-server-2013-home-users-on-a-survivable-branch-appliance-or-server.md)

  - [<span data-ttu-id="db264-119">Annexes : Survivable Branch Appliances et serveurs Survivable Branch Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="db264-119">Appendices: Survivable Branch Appliances and Servers in Lync Server 2013</span></span>](lync-server-2013-appendices-survivable-branch-appliances-and-servers.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="db264-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db264-120">See Also</span></span>


[<span data-ttu-id="db264-121">Déploiement de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="db264-121">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)  
  

<span data-ttu-id="db264-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="db264-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

