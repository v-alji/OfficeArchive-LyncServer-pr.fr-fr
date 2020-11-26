---
title: 'Lync Server 2013 : sauvegarder des bases de données de conversation persistante'
description: 'Lync Server 2013 : sauvegarder des bases de données de conversation persistante.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up Persistent Chat databases
ms:assetid: b99ebdc0-a025-44d7-9d74-37a7365f330d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945646(v=OCS.15)
ms:contentKeyID: 51541507
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9885eaf0065f5b558922c056fb1f669a5b821460
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438021"
---
# <a name="backing-up-persistent-chat-databases-in-lync-server-2013"></a><span data-ttu-id="4cb04-103">Sauvegarder des bases de données de chat permanent dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4cb04-103">Backing up Persistent Chat databases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4cb04-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4cb04-104">

<span> </span></span></span>

<span data-ttu-id="4cb04-105">_**Dernière modification de la rubrique :** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="4cb04-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="4cb04-106">Le contenu d’une salle de conversation permanente est stocké dans la base de données de chat permanent (MGC. mdf).</span><span class="sxs-lookup"><span data-stu-id="4cb04-106">Persistent Chat room content is stored in the Persistent Chat database (Mgc.mdf).</span></span> <span data-ttu-id="4cb04-107">Il s’agit de données vitales qui doivent être sauvegardées régulièrement.</span><span class="sxs-lookup"><span data-stu-id="4cb04-107">This is business-critical data that should be backed up regularly.</span></span> <span data-ttu-id="4cb04-108">Outre le contenu d’une salle de conversation, la base de données de conversation permanente stocke également des informations sur les principaux (par exemple, les utilisateurs et les groupes d’utilisateurs), ainsi que les rôles et l’accès à des salles de conversation et des salles de conversation.</span><span class="sxs-lookup"><span data-stu-id="4cb04-108">In addition to the chat room content, the Persistent Chat database also stores information about the principals (such as users and user groups), and the roles and access that they have to chat rooms and chat room.</span></span>

<span data-ttu-id="4cb04-109">Il existe deux méthodes pour sauvegarder les données de conversation permanente.</span><span class="sxs-lookup"><span data-stu-id="4cb04-109">There are two ways of backing up Persistent Chat data.</span></span>

  - <span data-ttu-id="4cb04-110">Sauvegarde SQL Server</span><span class="sxs-lookup"><span data-stu-id="4cb04-110">SQL Server Backup</span></span>

  - <span data-ttu-id="4cb04-111">L' `Export-CsPersistentChatData` applet de passe qui exporte les données de conversation permanente en tant que fichier</span><span class="sxs-lookup"><span data-stu-id="4cb04-111">The `Export-CsPersistentChatData` cmdlet, which exports Persistent Chat data as a file</span></span>

<span data-ttu-id="4cb04-112">Les données qui sont créées à l’aide de la sauvegarde SQL Server nécessitent considérablement plus d’espace disque, ce qui peut être plus de 20 fois plus important que ce qui est créé par `Export-CsPersistentChatData` la sauvegarde SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4cb04-112">Data that is created by using SQL Server backup requires significantly more disk space—possibly 20 times more—than that created by `Export-CsPersistentChatData`, but SQL Server backup is more likely to be a procedure that administrators are familiar with.</span></span>

<span data-ttu-id="4cb04-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4cb04-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

