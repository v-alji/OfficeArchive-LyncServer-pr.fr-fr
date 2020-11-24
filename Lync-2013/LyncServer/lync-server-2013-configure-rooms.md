---
title: 'Lync Server 2013 : Configuration des salles'
description: 'Lync Server 2013 : configurer des salles.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure rooms
ms:assetid: 8956bd2c-c863-4704-bc65-5c0d83556258
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205067(v=OCS.15)
ms:contentKeyID: 48184750
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e9f5b2ece8cf436fe69c000da73871cb92686d82
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394768"
---
# <a name="configure-rooms-in-lync-server-2013"></a><span data-ttu-id="d5045-103">Configuration des salles dans in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d5045-103">Configure rooms in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d5045-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d5045-104">

<span> </span></span></span>

<span data-ttu-id="d5045-105">_**Dernière modification de la rubrique :** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="d5045-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="d5045-106">La configuration des salles de conversation permanente est généralement gérée par des utilisateurs ou d’autres équipes centrales en utilisant l’interface de ligne de commande Windows PowerShell ; en règle générale, un administrateur ne gère pas les salles de conversation.</span><span class="sxs-lookup"><span data-stu-id="d5045-106">Configuring Persistent Chat rooms is commonly handled by users or other central teams by using Windows PowerShell command-line interface; an administrator typically does not manage chat rooms.</span></span> <span data-ttu-id="d5045-107">Toutefois, si vous devez créer et gérer des salles de conversation, vous pouvez utiliser l’interface de ligne de commande Windows PowerShell ou vous ajouter vous-même en tant que membre d’une salle de conversation et utiliser le client 2013 Lync.</span><span class="sxs-lookup"><span data-stu-id="d5045-107">However, if you have to create and manage chat rooms, you can use the Windows PowerShell command-line interface, or add yourself as a member to a chat room and use the Lync 2013 client.</span></span>

<span data-ttu-id="d5045-108">Pour plus d’informations sur la configuration des salles de conversation à l’aide de l’interface de ligne de commande Windows PowerShell, voir « gestion des salles » dans [configuration du serveur de chat permanent à l’aide d’applets de commande Windows PowerShell](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span><span class="sxs-lookup"><span data-stu-id="d5045-108">For details about configuring chat rooms by using the Windows PowerShell command-line interface, see "Room Management" in [Configuring Persistent Chat Server by using Windows PowerShell cmdlets](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span></span>

<div>

## <a name="managing-data-in-chat-rooms"></a><span data-ttu-id="d5045-109">Gestion des données dans des salles de conversation</span><span class="sxs-lookup"><span data-stu-id="d5045-109">Managing Data in Chat Rooms</span></span>

<span data-ttu-id="d5045-110">Le serveur Chat permanent permet aux utilisateurs de collaborer en publiant des messages dans des salles de conversation permanentes.</span><span class="sxs-lookup"><span data-stu-id="d5045-110">Persistent Chat Server lets users collaborate by posting messages into Persistent Chat rooms.</span></span> <span data-ttu-id="d5045-111">Les données sont conservées sur le serveur, et les membres de la salle peuvent avoir accès aux données, y compris les données historiques.</span><span class="sxs-lookup"><span data-stu-id="d5045-111">The data is persisted on the server, and members of the room can have access to the data, including historical data.</span></span> <span data-ttu-id="d5045-112">Toutefois, les utilisateurs dotés de rôles différents disposent d’un accès différent aux données persistantes, comme indiqué dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="d5045-112">However, users with different roles have different access to the persisted data, as outlined in the following list.</span></span>

  - <span data-ttu-id="d5045-113">Les administrateurs peuvent supprimer un contenu précédant (par exemple, du contenu publié avant une certaine date) d’une salle de conversation afin de conserver une taille de base de données raisonnable.</span><span class="sxs-lookup"><span data-stu-id="d5045-113">Administrators can delete earlier content (for example, content that was posted before a certain date) from any chat room to keep the database from growing too large.</span></span> <span data-ttu-id="d5045-114">Ils peuvent ainsi supprimer ou remplacer les messages qui sont considérés comme inappropriés pour une salle de conversation particulière.</span><span class="sxs-lookup"><span data-stu-id="d5045-114">Or, they can remove or replace messages that are considered inappropriate for a particular chat room.</span></span>

  - <span data-ttu-id="d5045-115">Les utilisateurs finaux, y compris les auteurs de messages, ne peuvent pas supprimer du contenu de salle de conversation.</span><span class="sxs-lookup"><span data-stu-id="d5045-115">End users, including message authors, cannot delete content from any chat room.</span></span>

  - <span data-ttu-id="d5045-116">Les gestionnaires de salle de conversation peuvent désactiver des salles, mais ne peuvent pas les supprimer.</span><span class="sxs-lookup"><span data-stu-id="d5045-116">Chat room managers can disable rooms, but cannot delete rooms.</span></span> <span data-ttu-id="d5045-117">Seuls les administrateurs peuvent supprimer une salle de conversation après la création de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="d5045-117">Only administrators can delete a chat room after it has been created.</span></span>

<span data-ttu-id="d5045-118">Quand un message est supprimé, vous ne pouvez pas annuler l’action.</span><span class="sxs-lookup"><span data-stu-id="d5045-118">When a message is deleted, you cannot undo the action.</span></span> <span data-ttu-id="d5045-119">Toutefois, les messages supprimés peuvent être restaurés s’il y a une sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="d5045-119">However, deleted messages can be restored if there is a backup.</span></span> <span data-ttu-id="d5045-120">Si un serveur de conformité des conversations permanent est activé, les anciens messages sont conservés dans la base de données de conformité.</span><span class="sxs-lookup"><span data-stu-id="d5045-120">If a Persistent Chat Compliance server is enabled, old messages are persisted in the compliance database.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d5045-121">L’utilisation des données de salle de conversation s’applique aux applications Lync Server 2013 et aux API serveur de chat permanent, sauf si le rôle d’administrateur est impliqué.</span><span class="sxs-lookup"><span data-stu-id="d5045-121">This chat room data usage applies to the Lync Server 2013, Persistent Chat Server API application, except for the case when the administrator role is involved.</span></span> <span data-ttu-id="d5045-122">L’API serveur Chat permanent ne peut pas être utilisée pour effectuer les opérations de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d5045-122">The Persistent Chat Server API cannot be used to do any of the administrator’s operations.</span></span> <span data-ttu-id="d5045-123">Vous devez effectuer ces opérations dans Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="d5045-123">You must perform these operations in the Lync Server Management Shell.</span></span>



<span data-ttu-id="d5045-124"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d5045-124"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

