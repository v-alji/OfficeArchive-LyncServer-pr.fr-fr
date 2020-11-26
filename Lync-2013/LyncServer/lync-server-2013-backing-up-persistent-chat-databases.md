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
# <a name="backing-up-persistent-chat-databases-in-lync-server-2013"></a>Sauvegarder des bases de données de chat permanent dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-17_

Le contenu d’une salle de conversation permanente est stocké dans la base de données de chat permanent (MGC. mdf). Il s’agit de données vitales qui doivent être sauvegardées régulièrement. Outre le contenu d’une salle de conversation, la base de données de conversation permanente stocke également des informations sur les principaux (par exemple, les utilisateurs et les groupes d’utilisateurs), ainsi que les rôles et l’accès à des salles de conversation et des salles de conversation.

Il existe deux méthodes pour sauvegarder les données de conversation permanente.

  - Sauvegarde SQL Server

  - L' `Export-CsPersistentChatData` applet de passe qui exporte les données de conversation permanente en tant que fichier

Les données qui sont créées à l’aide de la sauvegarde SQL Server nécessitent considérablement plus d’espace disque, ce qui peut être plus de 20 fois plus important que ce qui est créé par `Export-CsPersistentChatData` la sauvegarde SQL Server.

</div>

<span> </span>

</div>

</div>

</div>

