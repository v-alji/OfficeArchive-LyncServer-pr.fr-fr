---
title: 'Lync Server 2013 : Gestion des catégories, des salles et des compléments'
description: 'Lync Server 2013 : gestion des catégories, des salles et des compléments.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing categories, rooms, and add-ins
ms:assetid: a9807031-7369-4a51-9369-6f09bec24141
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412799(v=OCS.15)
ms:contentKeyID: 48185100
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba09ed3e021ba24f424d28bbb2c5c379ab975741
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425954"
---
# <a name="managing-categories-rooms-and-add-ins-in-lync-server-2013"></a><span data-ttu-id="68927-103">Gestion des catégories, des salles et des compléments dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68927-103">Managing categories, rooms, and add-ins in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="68927-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="68927-104">

<span> </span></span></span>

<span data-ttu-id="68927-105">_**Dernière modification de la rubrique :** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="68927-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="68927-106">Dans Lync Server 2013 panneau de configuration, ou à l’aide des applets de commande Windows PowerShell, les administrateurs de discussions permanentes peuvent utiliser la page de **conversation permanente** pour créer des catégories et des compléments. Pour la gestion des salles de conversation permanentes, les administrateurs peuvent utiliser les applets de cmdlet Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="68927-106">In Lync Server 2013 Control Panel, or by using Windows PowerShell cmdlets, Persistent Chat Administrators can use the **Persistent Chat** page to create categories and add-ins. For managing Persistent Chat rooms, Administrators can use Windows PowerShell cmdlets.</span></span> <span data-ttu-id="68927-107">Par ailleurs, si l’administrateur de chat permanent est compatible SIP, il peut utiliser le client Lync pour lancer une page Web afin de créer et gérer des salles de conversation.</span><span class="sxs-lookup"><span data-stu-id="68927-107">Alternatively, if the Persistent Chat administrator is also SIP-enabled, they can use the Lync client to launch a web page to create and manage chat rooms.</span></span>

<span data-ttu-id="68927-108">Les rubriques suivantes expliquent comment créer et utiliser des catégories et des salles de conversation.</span><span class="sxs-lookup"><span data-stu-id="68927-108">The following topics describe how to create and work with categories and chat rooms.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="68927-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="68927-109">In This Section</span></span>

  - [<span data-ttu-id="68927-110">Création ou modification d’une catégorie dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68927-110">Creating or editing a new category in Lync Server 2013</span></span>](lync-server-2013-creating-or-editing-a-new-category.md)

  - [<span data-ttu-id="68927-111">Création ou modification d’une salle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68927-111">Creating or editing a new room in Lync Server 2013</span></span>](lync-server-2013-creating-or-editing-a-new-room.md)

  - [<span data-ttu-id="68927-112">Création de compléments pour les salles dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68927-112">Creating new add-ins for rooms in Lync Server 2013</span></span>](lync-server-2013-creating-new-add-ins-for-rooms.md)

  - [<span data-ttu-id="68927-113">Définition des utilisateurs pouvant publier des messages dans une salle de conversation de type auditorium dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68927-113">Setting who can post messages in an auditorium chat room in Lync Server 2013</span></span>](lync-server-2013-setting-who-can-post-messages-in-an-auditorium-chat-room.md)

  - [<span data-ttu-id="68927-114">Désactivation ou activation d’une salle de conversation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68927-114">Disabling or enabling a chat room in Lync Server 2013</span></span>](lync-server-2013-disabling-or-enabling-a-chat-room.md)

  - [<span data-ttu-id="68927-115">Déplacement d’une salle de conversation d’une catégorie vers une autre dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68927-115">Moving a chat room from one category to another in Lync Server 2013</span></span>](lync-server-2013-moving-a-chat-room-from-one-category-to-another.md)

  - [<span data-ttu-id="68927-116">Suppression d’une catégorie ou d’une salle de conversation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68927-116">Deleting a chat room or category in Lync Server 2013</span></span>](lync-server-2013-deleting-a-chat-room-or-category.md)

  - [<span data-ttu-id="68927-117">Suppression d’un message ou purge de messages obsolètes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68927-117">Deleting a message or purging obsolete messages in Lync Server 2013</span></span>](lync-server-2013-deleting-a-message-or-purging-obsolete-messages.md)

<span data-ttu-id="68927-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="68927-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

