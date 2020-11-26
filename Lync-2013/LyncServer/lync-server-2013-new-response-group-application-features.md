---
title: 'Lync Server 2013 : Nouvelles fonctionnalités de l’application Response Group'
description: 'Lync Server 2013 : nouvelles fonctionnalités d’application de groupe de réponse.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New Response Group application features
ms:assetid: 569544b4-fa97-429b-97e6-568afab6c19b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398373(v=OCS.15)
ms:contentKeyID: 48184196
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 191d3867758da427ade3470e78abfd417f6f00de
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424995"
---
# <a name="new-response-group-application-features-in-lync-server-2013"></a><span data-ttu-id="21f4b-103">Nouvelles fonctionnalités de l’application Response Group dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21f4b-103">New Response Group application features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="21f4b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="21f4b-104">

<span> </span></span></span>

<span data-ttu-id="21f4b-105">_**Dernière modification de la rubrique :** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="21f4b-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="21f4b-106">L’application Response Group vous permet d’acheminer et de traiter en file d’attente les appels entrants vers des personnes disposant de personnes spécifiques, comme le service clientèle, le support technique interne ou l’assistance téléphonique générale pour un service.</span><span class="sxs-lookup"><span data-stu-id="21f4b-106">With the Response Group application, you can route and queue incoming calls to designated persons for special purposes, such as customer service, an internal help desk, or general telephone support for a department.</span></span>

<span data-ttu-id="21f4b-107">Les fonctionnalités d’application de groupe de réponse suivantes sont une nouveauté de Lync Server 2013 :</span><span class="sxs-lookup"><span data-stu-id="21f4b-107">The following Response Group application features are new in Lync Server 2013:</span></span>

  - <span data-ttu-id="21f4b-108">**Rôle du responsable**</span><span class="sxs-lookup"><span data-stu-id="21f4b-108">**Manager role**</span></span>
    
    <span data-ttu-id="21f4b-109">Lync Server 2013 introduit un nouveau rôle responsable de groupe de réponse.</span><span class="sxs-lookup"><span data-stu-id="21f4b-109">Lync Server 2013 introduces a new Response Group Manager role.</span></span> <span data-ttu-id="21f4b-110">Il existe désormais deux rôles de gestion pour les groupes de réponse : responsable de groupe de réponse et administrateur de groupe de réponse.</span><span class="sxs-lookup"><span data-stu-id="21f4b-110">Now there are two management roles for response groups: Response Group Manager and Response Group Administrator.</span></span> <span data-ttu-id="21f4b-111">Si les administrateurs de groupe de réponse peuvent tout de même configurer tous les éléments pour n’importe quel groupe de réponse, les responsables peuvent configurer uniquement certains éléments, uniquement pour les groupes de réponse qu’ils possèdent.</span><span class="sxs-lookup"><span data-stu-id="21f4b-111">While Response Group Administrators can still configure any element for any response group, Managers can configure only certain elements, only for response groups they own.</span></span>
    
    <span data-ttu-id="21f4b-112">Cette amélioration apportée au modèle d’administration offre une évolutivité du groupe de réponse, en particulier pour des scénarios de déploiement importants.</span><span class="sxs-lookup"><span data-stu-id="21f4b-112">This improvement in the administration model benefits Response Group scalability, especially for large deployment scenarios.</span></span>

  - <span data-ttu-id="21f4b-113">**Haute disponibilité**</span><span class="sxs-lookup"><span data-stu-id="21f4b-113">**High availability**</span></span>
    
    <span data-ttu-id="21f4b-114">La prise en charge de la haute disponibilité pour l’application Response Group, sous la forme de la mise en miroir SQL Server, est activée dans le cadre de la configuration générale et du déploiement de la haute disponibilité pour Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="21f4b-114">High availability support for the Response Group application, in the form of SQL Server mirroring, is enabled as part of the overall configuration and deployment of high availability for Lync Server 2013.</span></span> <span data-ttu-id="21f4b-115">Si vous configurez pour une haute disponibilité et perdez votre connectivité au serveur principal principal, la fonctionnalité de groupe de réponse n’est pas affectée par l’utilisation du serveur principal en miroir.</span><span class="sxs-lookup"><span data-stu-id="21f4b-115">If you configure for high availability and lose connectivity to the primary back-end server, Response Group functionality is not affected by leveraging the mirrored back-end server.</span></span>
    
    <span data-ttu-id="21f4b-116">La prise en charge de la mise en miroir SQL Server pour l’application Response Group ne peut pas être activée ou configurée en dehors de la configuration globale de haute disponibilité Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="21f4b-116">Support for SQL Server mirroring for the Response Group application can’t be individually enabled or configured outside of the overall Lync Server 2013 high availability configuration.</span></span>

  - <span data-ttu-id="21f4b-117">**Récupération d’urgence**</span><span class="sxs-lookup"><span data-stu-id="21f4b-117">**Disaster recovery**</span></span>
    
    <span data-ttu-id="21f4b-118">La prise en charge du reprise après sinistre pour l’application Response Group est activée dans le cadre de la configuration et du déploiement des pools frontaux couplés, qui font partie de la configuration globale de reprise après sinistre de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="21f4b-118">Disaster recovery support for the Response Group application is enabled as part of the configuration and deployment of the paired Front End pools, which are part of the overall Lync Server 2013 disaster recovery configuration.</span></span> <span data-ttu-id="21f4b-119">De plus, les cmdlets d’importation et d’exportation de groupe de réponse prennent en charge le processus de basculement vers le pool de sauvegarde et le processus de restauration vers le pool principal ou vers un nouveau pool.</span><span class="sxs-lookup"><span data-stu-id="21f4b-119">In addition, Response Group import and export cmdlets support the failover process to the backup pool and the failback process to the primary pool or to a new pool.</span></span> <span data-ttu-id="21f4b-120">Si une interruption se produit dans le pool principal, les groupes de réponses peuvent être basculés vers le pool de sauvegardes, puis restaurés au pool principal ou à un nouveau pool lorsque l’interruption est terminée.</span><span class="sxs-lookup"><span data-stu-id="21f4b-120">If an outage occurs in the primary pool, response groups can be failed over to the backup pool, and then failed back to the primary pool or to a new pool when the outage is over.</span></span>

<div id="sectionSection0" class="section">

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="21f4b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21f4b-121">See Also</span></span>


[<span data-ttu-id="21f4b-122">Planification des groupes Response Group dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21f4b-122">Planning for response groups in Lync Server 2013</span></span>](lync-server-2013-planning-for-response-groups.md)  
  

<span data-ttu-id="21f4b-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="21f4b-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

