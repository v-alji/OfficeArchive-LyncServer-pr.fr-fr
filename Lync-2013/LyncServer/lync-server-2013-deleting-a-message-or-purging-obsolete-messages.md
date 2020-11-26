---
title: 'Lync Server 2013 : Suppression d’un message ou purge de messages obsolètes'
description: 'Lync Server 2013 : suppression d’un message ou suppression définitive des messages obsolètes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting a message or purging obsolete messages
ms:assetid: 3f0c612d-6dfd-41a4-a5fe-5ff3448eb0ce
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215874(v=OCS.15)
ms:contentKeyID: 48706000
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 928e34d2ab52b02155568c7da96e4ac1d8154b7a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430405"
---
# <a name="deleting-a-message-or-purging-obsolete-messages-in-lync-server-2013"></a><span data-ttu-id="7b70f-103">Suppression d’un message ou purge de messages obsolètes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7b70f-103">Deleting a message or purging obsolete messages in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7b70f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7b70f-104">

<span> </span></span></span>

<span data-ttu-id="7b70f-105">_**Dernière modification de la rubrique :** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="7b70f-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="7b70f-106">Un administrateur de chat permanent peut supprimer un message d’une salle de conversation permanente (et peut éventuellement le remplacer par un autre).</span><span class="sxs-lookup"><span data-stu-id="7b70f-106">A Persistent Chat administrator can delete a message from a Persistent Chat room (and, optionally, can replace it with another message).</span></span> <span data-ttu-id="7b70f-107">Les administrateurs peuvent également effacer les messages obsolètes dans le cadre de la maintenance en cours afin de réduire la croissance de la base de données.</span><span class="sxs-lookup"><span data-stu-id="7b70f-107">Administrators can also purge obsolete messages as part of ongoing maintenance, to minimize growth of the database.</span></span> <span data-ttu-id="7b70f-108">Par exemple, la commande Windows PowerShell suivante entraîne la suppression de tous les messages de la salle de conversation ITChatRoom publiée par l’utilisateur kenmyer@litwareinc.com :</span><span class="sxs-lookup"><span data-stu-id="7b70f-108">For example, this Windows PowerShell command removes all the messages from the ITChatRoom chat room that were posted by the user kenmyer@litwareinc.com:</span></span>

    Remove-CsPersistentChatMessage -Identity "atl-persistentchat-001.litwareinc.com\ITChatRoom" -UserUri "sip:kenmyer@litwareinc.com"

<span data-ttu-id="7b70f-109">Dans cet exemple, vous remplacez les messages supprimés par la note que le message n’est plus disponible :</span><span class="sxs-lookup"><span data-stu-id="7b70f-109">And this example replaces any removed messages with the note that the message is no longer available:</span></span>

    Remove-CsPersistentChatMessage -Identity "atl-persistentchat-001.litwareinc.com\ITChatRoom" -UserUri "sip:kenmyer@litwareinc.com" -ReplaceMessage "This message is no longer available."

<span data-ttu-id="7b70f-110">Pour plus d’informations, reportez-vous à la rubrique d’aide relative à l’applet de passe [Remove-CsPersistentChatMessage](https://docs.microsoft.com/powershell/module/skype/Remove-CsPersistentChatMessage) .</span><span class="sxs-lookup"><span data-stu-id="7b70f-110">For more information, see the help topic for the [Remove-CsPersistentChatMessage](https://docs.microsoft.com/powershell/module/skype/Remove-CsPersistentChatMessage) cmdlet.</span></span>

<span data-ttu-id="7b70f-111"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7b70f-111"></div>

<span> </span>

</div>

</div>

</span></span></div>

