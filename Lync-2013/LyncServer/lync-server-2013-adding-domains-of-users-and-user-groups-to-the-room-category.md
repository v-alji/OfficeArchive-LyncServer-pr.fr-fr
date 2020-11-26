---
title: 'Lync Server 2013 : Ajout de domaines d’utilisateurs et de groupes d’utilisateurs à la catégorie de salles'
description: 'Lync Server 2013 : ajout de domaines d’utilisateurs et de groupes d’utilisateurs à la catégorie de salle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding domains of users and user groups to the room category
ms:assetid: ee03f2cf-1c84-41c4-b524-d0729be33b8c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215884(v=OCS.15)
ms:contentKeyID: 48706013
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 196a795547d5caa6dfd1732c3d6b4630ef79438a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439211"
---
# <a name="adding-domains-of-users-and-user-groups-to-the-room-category-in-lync-server-2013"></a>Ajout de domaines d’utilisateurs et de groupes d’utilisateurs à la catégorie de salles dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2014-02-07_

Pour ajouter des groupes de personnes plus importants à une salle de conversation, voir [configurer les catégories dans Lync Server 2013](lync-server-2013-configure-categories.md) et [gérer les catégories](manage-categories.md) dans la documentation de déploiement. Par exemple, la commande suivante permet d’ajouter tous les utilisateurs de l’unité d’organisation NorthAmericaUsers dans Active Directory à la salle de conversation du Nord :

    Set-CsPersistentChatRoom -PersistentChatPoolFqdn "atl-cs-001.litwareinc.com\NorthAmerica" -Members @{Add="OU=NorthAmericaUsers,DC=litwareinc,DC=com"}

Sa commande permet d’ajouter tous les membres du groupe de distribution finance à la même salle de conversation :

    Set-CsPersistentChatRoom -PersistentChatPoolFqdn "atl-cs-001.litwareinc.com\NorthAmerica" -Members @{Add="CN=Finance,OU=ExternalUsers,DC=litwareinc,DC=com"}

</div>

<span> </span>

</div>

</div>

</div>

