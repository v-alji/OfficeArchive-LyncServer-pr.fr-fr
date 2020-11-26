---
title: 'Lync Server 2013 : Suppression d’une catégorie ou d’une salle de conversation'
description: 'Lync Server 2013 : suppression d’une salle de conversation ou d’une catégorie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting a chat room or category
ms:assetid: adccb869-0015-4eba-ac73-718bac7843b5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215881(v=OCS.15)
ms:contentKeyID: 48706009
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3ef89802171a1eeca7de18ff0a4eb8eb3895f1b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430412"
---
# <a name="deleting-a-chat-room-or-category-in-lync-server-2013"></a><span data-ttu-id="4d6a5-103">Suppression d’une catégorie ou d’une salle de conversation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4d6a5-103">Deleting a chat room or category in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4d6a5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4d6a5-104">

<span> </span></span></span>

<span data-ttu-id="4d6a5-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="4d6a5-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="4d6a5-106">Les salles de conversation permanente peuvent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="4d6a5-106">Persistent Chat rooms can be deleted.</span></span> <span data-ttu-id="4d6a5-107">Si vous disposez d’une salle de conversation qui n’est plus utilisée, vous pouvez la désactiver.</span><span class="sxs-lookup"><span data-stu-id="4d6a5-107">If you have a chat room that is no longer being used, you can disable it.</span></span> <span data-ttu-id="4d6a5-108">Pour plus d’informations, reportez-vous à [désactivation ou activation d’une salle de conversation dans Lync Server 2013](lync-server-2013-disabling-or-enabling-a-chat-room.md).</span><span class="sxs-lookup"><span data-stu-id="4d6a5-108">For details, see [Disabling or enabling a chat room in Lync Server 2013](lync-server-2013-disabling-or-enabling-a-chat-room.md).</span></span>

<span data-ttu-id="4d6a5-109">Un administrateur de chat permanent peut interroger des salles de conversation désactivées et peut périodiquement effacer et supprimer définitivement les salles de conversation, à l’aide de l’applet de requête Windows PowerShell, **Remove-CsPersistentChatRoom**.</span><span class="sxs-lookup"><span data-stu-id="4d6a5-109">A Persistent Chat administrator can query for disabled chat rooms, and can periodically purge and permanently delete the chat rooms, by using the Windows PowerShell cmdlet, **Remove-CsPersistentChatRoom**.</span></span>

<span data-ttu-id="4d6a5-110">Les catégories peuvent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="4d6a5-110">Categories can be deleted.</span></span> <span data-ttu-id="4d6a5-111">Toutefois, pour supprimer une catégorie, vous devez d’abord supprimer toutes les salles de conversation ou les déplacer vers une nouvelle catégorie, en laissant une catégorie vide pour suppression.</span><span class="sxs-lookup"><span data-stu-id="4d6a5-111">However, to delete a category, you must first either delete all chat rooms under it or move the chat rooms to a new category, leaving an empty category for deletion.</span></span> <span data-ttu-id="4d6a5-112">Le serveur Chat permanent ne vous permet pas de supprimer une catégorie contenant des salles de conversation.</span><span class="sxs-lookup"><span data-stu-id="4d6a5-112">Persistent Chat Server does not allow you to delete a category that contains chat rooms.</span></span> <span data-ttu-id="4d6a5-113">Pour plus d’informations, reportez-vous à [déplacement d’une salle de conversation d’une catégorie à une autre dans Lync Server 2013](lync-server-2013-moving-a-chat-room-from-one-category-to-another.md).</span><span class="sxs-lookup"><span data-stu-id="4d6a5-113">For details, see [Moving a chat room from one category to another in Lync Server 2013](lync-server-2013-moving-a-chat-room-from-one-category-to-another.md).</span></span>

<span data-ttu-id="4d6a5-114">Pour plus d’informations sur la suppression des catégories vides à l’aide de l’interface de ligne de commande Windows PowerShell, voir « gestion des salles » dans [configuration du serveur de chat permanent à l’aide d’applets de commande Windows PowerShell](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span><span class="sxs-lookup"><span data-stu-id="4d6a5-114">For details about deleting empty categories by using the Windows PowerShell command-line interface, see "Room Management" in [Configuring Persistent Chat Server by using Windows PowerShell cmdlets](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span></span>

<span data-ttu-id="4d6a5-115">Pour plus d’informations sur les salles de conversation et les catégories, voir [configurer des salles dans Lync server 2013](lync-server-2013-configure-rooms.md) et [configurer les catégories dans Lync Server 2013](lync-server-2013-configure-categories.md) dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="4d6a5-115">For details about chat rooms and categories, see [Configure rooms in Lync Server 2013](lync-server-2013-configure-rooms.md) and [Configure categories in Lync Server 2013](lync-server-2013-configure-categories.md) in the Deployment documentation.</span></span>

<span data-ttu-id="4d6a5-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4d6a5-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

