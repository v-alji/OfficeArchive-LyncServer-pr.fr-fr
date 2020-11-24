---
title: 'Lync Server 2013 : planification des fonctionnalités de gestion des appels'
description: 'Lync Server 2013 : planification des fonctionnalités de gestion des appels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for call management features
ms:assetid: 5f557345-5a04-45d6-b274-c02dbfe41b33
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398421(v=OCS.15)
ms:contentKeyID: 48184298
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ec990aad40baf33365e92e78ee8071216a2add1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393780"
---
# <a name="planning-for-call-management-features-in-lync-server-2013"></a><span data-ttu-id="3134a-103">Planifier les fonctionnalités de gestion des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3134a-103">Planning for call management features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3134a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3134a-104">

<span> </span></span></span>

<span data-ttu-id="3134a-105">_**Dernière modification de la rubrique :** 2012-12-17_</span><span class="sxs-lookup"><span data-stu-id="3134a-105">_**Topic Last Modified:** 2012-12-17_</span></span>

<span data-ttu-id="3134a-106">Les fonctionnalités de gestion des appels voix entreprise contrôlent la façon dont les appels entrants sont routés et répondent.</span><span class="sxs-lookup"><span data-stu-id="3134a-106">Enterprise Voice call management features control how incoming calls are routed and answered.</span></span> <span data-ttu-id="3134a-107">Lync Server 2013 fournit les fonctionnalités de gestion des appels suivantes :</span><span class="sxs-lookup"><span data-stu-id="3134a-107">Lync Server 2013 provides the following call management features:</span></span>

  - <span data-ttu-id="3134a-108">**Parcage d’appel** : permet aux utilisateurs des communications vocales de parquer temporairement un appel, puis de le reprendre sur le même téléphone ou un autre téléphone.</span><span class="sxs-lookup"><span data-stu-id="3134a-108">**Call Park**:   Enables voice users to temporarily park a call and then pick it up from the same or another phone.</span></span>

  - <span data-ttu-id="3134a-109">**Prise d’appel de groupe** : permet à un utilisateur de la fonctionnalité audio de prendre un appel qui sonne pour un autre utilisateur de la fonctionnalité audio membre d’un groupe de prise d’appel.</span><span class="sxs-lookup"><span data-stu-id="3134a-109">**Group Pickup**:   Enables voice users to pick up calls that are ringing for other voice users who are assigned to call pickup groups.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3134a-110">La cueillette de groupe est une nouveauté avec des mises à jour cumulatives pour Lync Server 2013:2013 février.</span><span class="sxs-lookup"><span data-stu-id="3134a-110">Group Pickup is new with Cumulative Updates for Lync Server 2013: February 2013.</span></span>

    
    </div>

  - <span data-ttu-id="3134a-111">**Response Group** : achemine les appels entrants vers des groupes d’agents à l’aide de groupes de recherche, ou de questions et réponses IVR (réponse vocale interactive).</span><span class="sxs-lookup"><span data-stu-id="3134a-111">**Response Group**:   Routes incoming calls to groups of agents by using hunt groups or interactive voice response (IVR) questions and answers.</span></span>

  - <span data-ttu-id="3134a-112">**Annonce :**    Lit un message pour les appels passés vers un numéro non attribué, ou route l’appel à un autre endroit, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="3134a-112">**Announcement:**    Plays a message for calls made to an unassigned number, or routes the call elsewhere, or both.</span></span>

<span data-ttu-id="3134a-113">Si vous prévoyez de déployer Voix Entreprise, vous pouvez choisir d’implémenter une partie ou l’ensemble de ces fonctionnalités de gestion des appels.</span><span class="sxs-lookup"><span data-stu-id="3134a-113">If you plan to deploy Enterprise Voice, you can choose to implement any or all of these call management features.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3134a-114">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="3134a-114">In This Section</span></span>

  - [<span data-ttu-id="3134a-115">Planification du parcage d’appel dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3134a-115">Planning for Call Park in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-park.md)

  - [<span data-ttu-id="3134a-116">Planification de la capture des appels de groupe dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3134a-116">Planning for Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-planning-for-group-call-pickup.md)

  - [<span data-ttu-id="3134a-117">Planification des groupes Response Group dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3134a-117">Planning for response groups in Lync Server 2013</span></span>](lync-server-2013-planning-for-response-groups.md)

  - [<span data-ttu-id="3134a-118">Planification des annonces dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3134a-118">Planning for announcements in Lync Server 2013</span></span>](lync-server-2013-planning-for-announcements.md)

<span data-ttu-id="3134a-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3134a-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

