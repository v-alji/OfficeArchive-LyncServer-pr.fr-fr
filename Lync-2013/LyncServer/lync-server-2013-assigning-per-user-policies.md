---
title: 'Lync Server 2013 : attribution de stratégies par utilisateur'
description: 'Lync Server 2013 : attribution de stratégies par utilisateur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assigning per-user policies
ms:assetid: a4ed0120-d9e5-4eb2-acfd-8de2cb503652
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182561(v=OCS.15)
ms:contentKeyID: 48184971
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a99156f9413926251c27dfee40677976b80b7ea
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438294"
---
# <a name="assigning-per-user-policies-in-lync-server-2013"></a><span data-ttu-id="5a1d8-103">Attribution de stratégies par utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1d8-103">Assigning per-user policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5a1d8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5a1d8-104">

<span> </span></span></span>

<span data-ttu-id="5a1d8-105">_**Dernière modification de la rubrique :** 2012-10-14_</span><span class="sxs-lookup"><span data-stu-id="5a1d8-105">_**Topic Last Modified:** 2012-10-14_</span></span>

<span data-ttu-id="5a1d8-106">Vous pouvez affecter certaines stratégies à un utilisateur ou à un groupe d’utilisateurs afin de spécifier des paramètres spécifiques qui s’écartent des paramètres définis dans les stratégies affectées à d’autres utilisateurs, telles que les stratégies globales.</span><span class="sxs-lookup"><span data-stu-id="5a1d8-106">You can assign certain policies to a user or a group of users in order to specify particular settings that deviate from the settings defined in policies assigned to other users, such as global policies.</span></span> <span data-ttu-id="5a1d8-107">Ces stratégies s’appellent des politiques par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5a1d8-107">These policies are called per-user policies.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5a1d8-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="5a1d8-108">In This Section</span></span>

  - [<span data-ttu-id="5a1d8-109">Affecter une stratégie de conférence par utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1d8-109">Assign a per-user conferencing policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-conferencing-policy.md)

  - [<span data-ttu-id="5a1d8-110">Affecter une stratégie de version de client par utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1d8-110">Assign a per-user client version policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-client-version-policy.md)

  - [<span data-ttu-id="5a1d8-111">Affecter une stratégie de code confidentiel par utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1d8-111">Assign a per-user PIN policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-pin-policy.md)

  - [<span data-ttu-id="5a1d8-112">Attribution d’une stratégie d’accès des utilisateurs externes à un utilisateur activé pour Lync dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1d8-112">Assign an external user access policy to a Lync enabled user in Lync Server 2013</span></span>](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md)

  - [<span data-ttu-id="5a1d8-113">Affecter une stratégie d’archivage par utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1d8-113">Assign a per-user archiving policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-archiving-policy.md)

  - [<span data-ttu-id="5a1d8-114">Affecter une stratégie d’emplacement par utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1d8-114">Assign a per-user location policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-location-policy.md)

  - [<span data-ttu-id="5a1d8-115">Affecter une stratégie de mobilité par utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1d8-115">Assign a per-user mobility policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-mobility-policy.md)

  - [<span data-ttu-id="5a1d8-116">Assigner une stratégie de discussion persistante par utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1d8-116">Assign a per-user Persistent Chat policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-persistent-chat-policy.md)

  - [<span data-ttu-id="5a1d8-117">Affecter une stratégie de plan de numérotation par utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1d8-117">Assign a per-user dial plan policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-dial-plan-policy.md)

  - [<span data-ttu-id="5a1d8-118">Affecter une stratégie vocale par utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1d8-118">Assign a per-user voice policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-voice-policy.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5a1d8-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a1d8-119">See Also</span></span>


[<span data-ttu-id="5a1d8-120">Gestion des utilisateurs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1d8-120">Managing users in Lync Server 2013</span></span>](lync-server-2013-managing-users-in-lync-server.md)  
  

<span data-ttu-id="5a1d8-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5a1d8-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

