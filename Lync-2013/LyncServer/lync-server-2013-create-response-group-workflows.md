---
title: 'Lync Server 2013 : Création des flux de travail Response Group'
description: 'Lync Server 2013 : créer des flux de travail de groupe réponse.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create Response Group workflows
ms:assetid: 41272258-728d-42bd-b4d4-2a499734c720
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425918(v=OCS.15)
ms:contentKeyID: 48183954
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7082295eeca45c4dac76d68ef54b5c32fafb25d7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431588"
---
# <a name="create-response-group-workflows-in-lync-server-2013"></a><span data-ttu-id="a9ef8-103">Création des flux de travail Response Group dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a9ef8-103">Create Response Group workflows in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a9ef8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a9ef8-104">

<span> </span></span></span>

<span data-ttu-id="a9ef8-105">_**Dernière modification de la rubrique :** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="a9ef8-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="a9ef8-p101">Un flux de travail définit le comportement d’un appel, du déclenchement de la sonnerie du téléphone jusqu’au moment où une personne répond à l’appel. Le flux de travail spécifie la file d’attente à utiliser pour la mise en attente de l’appel et indique la méthode de routage à appliquer aux groupes de recherche ou les questions et les réponses à utiliser pour les groupes Response Group interactifs. Un flux de travail définit également des paramètres, comme un message d’accueil, l’attente musicale, les heures de bureau et les congés.</span><span class="sxs-lookup"><span data-stu-id="a9ef8-p101">A workflow defines the behavior of a call from the time that the phone rings to the time that someone answers the call. The workflow specifies the queue to use for holding the call, and specifies the routing method to use for hunt groups or the questions and answers to use for interactive response groups. A workflow also defines settings such as a welcome message, music on hold, business hours, and holidays.</span></span>

<span data-ttu-id="a9ef8-109">Pour créer des flux de travail, vous devez utiliser l’outil de configuration de Response Group.</span><span class="sxs-lookup"><span data-stu-id="a9ef8-109">You use the Response Group Configuration Tool to create workflows.</span></span> <span data-ttu-id="a9ef8-110">Vous pouvez accéder à l’outil de configuration de Response Group à partir de la page Response Group du panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a9ef8-110">You can access the Response Group Configuration Tool from the Response Group page of Lync Server Control Panel.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a9ef8-111">Vous devez créer des groupes d’agents et des files d’attente avant de créer un flux de travail qui les utilise.</span><span class="sxs-lookup"><span data-stu-id="a9ef8-111">You must create agent groups and queues before you create a workflow that uses them.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a9ef8-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a9ef8-112">In This Section</span></span>

  - [<span data-ttu-id="a9ef8-113">Création ou modification d’un flux de travail de groupe de recherche dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a9ef8-113">Create or modify a hunt group workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-hunt-group-workflow.md)

  - [<span data-ttu-id="a9ef8-114">Conception des flux d’appels du système de réponse vocale interactive dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a9ef8-114">Design interactive voice response call flows in Lync Server 2013</span></span>](lync-server-2013-design-interactive-voice-response-call-flows.md)

  - [<span data-ttu-id="a9ef8-115">Création ou modification d’un flux de travail interactif dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a9ef8-115">Create or modify an interactive workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-interactive-workflow.md)

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="a9ef8-116">Sections associées</span><span class="sxs-lookup"><span data-stu-id="a9ef8-116">Related Sections</span></span>

  - [<span data-ttu-id="a9ef8-117">Création des groupes d’agents Response Group Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a9ef8-117">Create Response Group agent groups Lync Server 2013</span></span>](lync-server-2013-create-response-group-agent-groups.md)

  - [<span data-ttu-id="a9ef8-118">Création des files d’attente Response Group dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a9ef8-118">Create Response Group queues in Lync Server 2013</span></span>](lync-server-2013-create-response-group-queues.md)

<span data-ttu-id="a9ef8-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a9ef8-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

