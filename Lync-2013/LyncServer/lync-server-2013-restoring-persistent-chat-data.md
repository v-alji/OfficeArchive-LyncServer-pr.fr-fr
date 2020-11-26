---
title: 'Lync Server 2013 : restauration des données de conversation permanente'
description: 'Lync Server 2013 : restauration des données de conversation permanente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring Persistent Chat data
ms:assetid: c251a7fa-50da-434b-b39a-17f5978ce736
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945649(v=OCS.15)
ms:contentKeyID: 51541516
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7c75683e151daaadab8374ed5b41886da9a3aea3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442508"
---
# <a name="restoring-persistent-chat-data-in-lync-server-2013"></a>Restauration de données de conversations permanentes dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-18_

Le contenu d’une salle de conversation permanente est stocké dans la base de données de chat permanent (MGC. mdf). Il s’agit de données vitales qui doivent être sauvegardées régulièrement. Outre le contenu d’une salle de conversation, les principaux (tels que les utilisateurs et les groupes) ainsi que les rôles et les autorisations qu’ils doivent utiliser pour discuter des salles de conversation et du contenu des salles de conversation, sont également stockés dans la base de données de chat permanent.

Le mode de restauration des données de conversation persistante dépend de la méthode que vous avez utilisée pour les sauvegarder.

  - Si vous avez utilisé des procédures de sauvegarde SQL Server, vous devez utiliser des procédures de restauration SQL Server.

  - Si vous avez utilisé l’applet de cmdlet **Export-CsPersistentChatData** pour sauvegarder les données de conversation permanente, vous devez utiliser l’applet de passe **Import-CsPersistentChatData** pour restaurer les données.

</div>

<span> </span>

</div>

</div>

</div>

