---
title: 'Lync Server 2013 : Gestion des stratégies de messagerie vocale hébergée'
description: 'Lync Server 2013 : gérer les stratégies de messagerie vocale hébergées.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage hosted voice mail policies
ms:assetid: 50ff22e3-9c8b-4a33-a72f-d149892acf53
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398332(v=OCS.15)
ms:contentKeyID: 48184139
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fcb5e98884d37540d5e75cc8cb6b1b419e4e75e6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426094"
---
# <a name="manage-hosted-voice-mail-policies-in-lync-server-2013"></a><span data-ttu-id="897da-103">Gestion des stratégies de messagerie vocale hébergée dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="897da-103">Manage hosted voice mail policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="897da-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="897da-104">

<span> </span></span></span>

<span data-ttu-id="897da-105">_**Dernière modification de la rubrique :** 2012-09-20_</span><span class="sxs-lookup"><span data-stu-id="897da-105">_**Topic Last Modified:** 2012-09-20_</span></span>

<span data-ttu-id="897da-106">Une *stratégie de messagerie vocale hébergée* fournit des informations à l’application de routage de l’ExUM de Lync Server 2013 sur l’emplacement de routage des appels pour les utilisateurs dont la boîte aux lettres est située sur un service Exchange hébergé.</span><span class="sxs-lookup"><span data-stu-id="897da-106">A *hosted voice mail policy* provides information to the Lync Server 2013 ExUM Routing application about where to route calls for users whose mailboxes are located on a hosted Exchange service.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="897da-107">En règle générale, une seule stratégie de messagerie vocale hébergée est requise.</span><span class="sxs-lookup"><span data-stu-id="897da-107">Typically, only one hosted voice mail policy is required.</span></span> <span data-ttu-id="897da-108">Dans de nombreux cas, vous pouvez modifier la stratégie globale en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="897da-108">In many cases, you can modify the global policy to meet all your needs.</span></span> <span data-ttu-id="897da-109">Si vous créez une stratégie avec l’étendue du site, elle est affectée automatiquement à tous les utilisateurs hébergés sur le site spécifié.</span><span class="sxs-lookup"><span data-stu-id="897da-109">If you create a policy with site scope, it is assigned automatically to all users homed at the specified site.</span></span> <span data-ttu-id="897da-110">Si vous créez une stratégie avec une étendue par utilisateur, vous devez l’attribuer explicitement à des utilisateurs, des groupes et des objets de contact.</span><span class="sxs-lookup"><span data-stu-id="897da-110">If you create a policy with per-user scope, you must explicitly assign it to users, groups, and contact objects.</span></span> <span data-ttu-id="897da-111">Il est possible de déployer plusieurs stratégies de messagerie vocale hébergées, mais dans ce cas, les stratégies doivent être attribuées en fonction de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="897da-111">It is possible to deploy multiple hosted voice mail policies, but in that case the policies must be assigned on a per-user basis.</span></span>



</div>

<span data-ttu-id="897da-112">Pour plus d’informations sur la planification des stratégies de messagerie vocale hébergées, voir [stratégies de messagerie vocale hébergées dans Lync Server 2013](lync-server-2013-hosted-voice-mail-policies.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="897da-112">For details about planning hosted voice mail policies, see [Hosted voice mail policies in Lync Server 2013](lync-server-2013-hosted-voice-mail-policies.md) in the Planning documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="897da-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="897da-113">In This Section</span></span>

  - [<span data-ttu-id="897da-114">Modifier la stratégie globale de messagerie vocale hébergée dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="897da-114">Modify the global hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-modify-the-global-hosted-voice-mail-policy.md)

  - [<span data-ttu-id="897da-115">Créer une stratégie de messagerie vocale hébergée au niveau du site dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="897da-115">Create a site-level hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-create-a-site-level-hosted-voice-mail-policy.md)

  - [<span data-ttu-id="897da-116">Créer une stratégie de messagerie vocale hébergée par utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="897da-116">Create a per-user hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-create-a-per-user-hosted-voice-mail-policy.md)

  - [<span data-ttu-id="897da-117">Affecter une stratégie de messagerie vocale hébergée par utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="897da-117">Assign a per-user hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-hosted-voice-mail-policy.md)

<span data-ttu-id="897da-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="897da-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

