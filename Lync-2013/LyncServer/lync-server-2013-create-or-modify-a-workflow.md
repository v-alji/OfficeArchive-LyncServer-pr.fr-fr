---
title: 'Lync Server 2013 : création ou modification d’un flux de travail'
description: 'Lync Server 2013 : création ou modification d’un flux de travail.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a workflow
ms:assetid: 5ac1c0f3-e82f-40ca-b972-91950e38c05b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520997(v=OCS.15)
ms:contentKeyID: 48184225
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 053b80e313e497313e613a5f8b16bd5beeabf7ac
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431728"
---
# <a name="create-or-modify-a-workflow-in-lync-server-2013"></a><span data-ttu-id="d984b-103">Créer ou modifier un flux de travail dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d984b-103">Create or modify a workflow in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d984b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d984b-104">

<span> </span></span></span>

<span data-ttu-id="d984b-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="d984b-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="d984b-106">Lync Server 2013 prend en charge deux types de flux de travail : le groupe de recherche et la réponse vocale interactive (IVR).</span><span class="sxs-lookup"><span data-stu-id="d984b-106">Lync Server 2013 supports two types of workflows: hunt group and interactive voice response (IVR).</span></span> <span data-ttu-id="d984b-107">Lorsque vous créez un flux de travail, vous devez utiliser l’outil de configuration de groupe de réponse pour spécifier la file d’attente à utiliser et d’autres paramètres, tels qu’un message d’accueil, de la musique en suspens, des heures d’ouverture et des questions que l’application Response Group demande à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="d984b-107">When you create a workflow, you use the Response Group Configuration Tool to specify the queue to use and other settings, such as a welcome message, music on hold, business hours, and questions that the Response Group application asks the caller.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d984b-108">Vous devez créer des groupes d’agents et des files d’attente avant de créer un flux de travail qui les utilise.</span><span class="sxs-lookup"><span data-stu-id="d984b-108">You must create agent groups and queues before you create a workflow that uses them.</span></span> <span data-ttu-id="d984b-109">Si vous voulez créer des heures et des jours fériés prédéfinis que vous pouvez utiliser pour plusieurs flux de travail, vous devez également définir ces heures et jours fériés avant de créer un flux de travail qui les utilise.</span><span class="sxs-lookup"><span data-stu-id="d984b-109">If you want to create predefined business hours and holidays that you can use for multiple workflows, you must also define these hours and holidays before you create a workflow that uses them.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d984b-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d984b-110">In This Section</span></span>

  - [<span data-ttu-id="d984b-111">Création ou modification d’un flux de travail de groupe de recherche dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d984b-111">Create or modify a hunt group workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-hunt-group-workflow.md)

  - [<span data-ttu-id="d984b-112">Création ou modification d’un flux de travail interactif dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d984b-112">Create or modify an interactive workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-interactive-workflow.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d984b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d984b-113">See Also</span></span>


[<span data-ttu-id="d984b-114">Créer ou modifier un groupe d’agents dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d984b-114">Create or modify an agent group in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-agent-group.md)  
[<span data-ttu-id="d984b-115">Créer ou modifier une file d’attente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d984b-115">Create or modify a queue in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-queue.md)  
[<span data-ttu-id="d984b-116">Facultatif Définir des jeux de vacances de groupe de réponse dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d984b-116">(Optional) Define Response Group holiday sets in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-holiday-sets.md)  


[<span data-ttu-id="d984b-117">Facultatif Définir les heures d’activité du groupe de réponses dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d984b-117">(Optional) Define Response Group business hours in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-business-hours.md)  
  

<span data-ttu-id="d984b-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d984b-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

