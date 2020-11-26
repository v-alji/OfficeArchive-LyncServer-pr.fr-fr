---
title: 'Lync Server 2013 : Configuration du groupe Response Group'
description: 'Lync Server 2013 : configuration de Response Group.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Response Group
ms:assetid: c56db929-cb21-4af0-be3f-c8f807b78a5a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205249(v=OCS.15)
ms:contentKeyID: 48185359
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92674bb971ec5216051d75d788dc58b9c7ca641c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432687"
---
# <a name="configuring-response-group-in-lync-server-2013"></a><span data-ttu-id="50b74-103">Configuration du groupe Response Group dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50b74-103">Configuring Response Group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="50b74-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="50b74-104">

<span> </span></span></span>

<span data-ttu-id="50b74-105">_**Dernière modification de la rubrique :** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="50b74-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="50b74-106">Response Group est une fonctionnalité de voix entreprise qui achemine et met en file d’attente les appels entrants vers des groupes de personnes, appelés *agents*, tels qu’un service d’assistance ou un service clientèle.</span><span class="sxs-lookup"><span data-stu-id="50b74-106">Response Group is an Enterprise Voice feature that routes and queues incoming calls to groups of people, called *agents*, such as a help desk or a customer service desk.</span></span>

<span data-ttu-id="50b74-107">Les composants requis par le groupe de réponse sont installés et activés automatiquement sur le serveur frontal ou le serveur Standard Edition lors du déploiement de voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="50b74-107">The components that Response Group requires are installed and enabled automatically on the Front End Server or Standard Edition server when you deploy Enterprise Voice.</span></span> <span data-ttu-id="50b74-108">Pour rendre le groupe de réponses disponible pour les utilisateurs, vous devez configurer des groupes d’agents, des files d’attente, puis des flux de travail.</span><span class="sxs-lookup"><span data-stu-id="50b74-108">To make Response Group available to users, you must configure agent groups, then queues, and then workflows.</span></span> <span data-ttu-id="50b74-109">Par ailleurs, un administrateur de groupe de réponse peut déléguer la configuration d’un flux de travail existant à un gestionnaire de groupe de réponse, qui peut ensuite modifier et reconfigurer le flux de travail ainsi que ses groupes d’agents et files d’attente associés.</span><span class="sxs-lookup"><span data-stu-id="50b74-109">Additionally, a Response Group Administrator can delegate configuration of an existing workflow to a Response Group Manager, who can then modify and reconfigure the workflow and its associated agent groups and queues.</span></span>

<span data-ttu-id="50b74-110">Cette section vous guide dans la configuration du groupe de réponse Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="50b74-110">This section guides you through the configuration of Lync Server 2013 Response Group.</span></span> <span data-ttu-id="50b74-111">Il part du principe que vous avez déjà lu les sections de planification associées au Response Group et avez déployé un serveur Enterprise Edition ou un serveur Standard Edition avec Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="50b74-111">It assumes that you have already read the planning sections related to Response Group and have deployed an Enterprise Edition server or a Standard Edition server with Enterprise Voice.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="50b74-112">Pour plus d’informations sur la création d’un groupe de réponse à l’aide de Lync Server Management Shell, y compris un exemple de script, reportez-vous à la section « Création de votre premier groupe de réponse avec Lync Server Management Shell » <A href="https://go.microsoft.com/fwlink/p/?linkid=204108">https://go.microsoft.com/fwlink/p/?linkId=204108</A> .</span><span class="sxs-lookup"><span data-stu-id="50b74-112">For details about creating a Response Group by using Lync Server Management Shell, including a sample script, see "Creating Your First Response Group Using Lync Server Management Shell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=204108">https://go.microsoft.com/fwlink/p/?linkId=204108</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="50b74-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="50b74-113">In This Section</span></span>

  - [<span data-ttu-id="50b74-114">Autorisations et conditions prérequises pour la configuration de Response Group dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50b74-114">Response Group configuration permissions and prerequisites in Lync Server 2013</span></span>](lync-server-2013-response-group-configuration-permissions-and-prerequisites.md)

  - [<span data-ttu-id="50b74-115">Processus de déploiement pour Response Group dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50b74-115">Deployment process for Response Group in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-response-group.md)

  - [<span data-ttu-id="50b74-116">Vue d’ensemble des scénarios de création de flux de travail dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50b74-116">Overview of workflow creation scenarios in Lync Server 2013</span></span>](lync-server-2013-overview-of-workflow-creation-scenarios.md)

  - [<span data-ttu-id="50b74-117">Création des groupes d’agents Response Group Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50b74-117">Create Response Group agent groups Lync Server 2013</span></span>](lync-server-2013-create-response-group-agent-groups.md)

  - [<span data-ttu-id="50b74-118">Création des files d’attente Response Group dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50b74-118">Create Response Group queues in Lync Server 2013</span></span>](lync-server-2013-create-response-group-queues.md)

  - [<span data-ttu-id="50b74-119">Facultatif Définir les heures d’activité du groupe de réponses dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50b74-119">(Optional) Define Response Group business hours in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-business-hours.md)

  - [<span data-ttu-id="50b74-120">Facultatif Définir des jeux de vacances de groupe de réponse dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50b74-120">(Optional) Define Response Group holiday sets in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-holiday-sets.md)

  - [<span data-ttu-id="50b74-121">Création des flux de travail Response Group dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50b74-121">Create Response Group workflows in Lync Server 2013</span></span>](lync-server-2013-create-response-group-workflows.md)

  - [<span data-ttu-id="50b74-122">Facultatif Vérifier le déploiement de Response Group dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50b74-122">(Optional) Verify Response Group deployment in Lync Server 2013</span></span>](lync-server-2013-optional-verify-response-group-deployment.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="50b74-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50b74-123">See Also</span></span>


[<span data-ttu-id="50b74-124">Planifier les fonctionnalités de gestion des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50b74-124">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="50b74-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="50b74-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

