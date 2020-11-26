---
title: Migration des réunions existantes et du contenu des réunions
description: Migration de conférences et de contenus de réunion existants.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate existing meetings and meeting content
ms:assetid: 30516731-2ae1-4a6d-a7e1-d3f05778c954
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688011(v=OCS.15)
ms:contentKeyID: 49733599
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d94dd35063a121a057a218c27fdb36e42a155b77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443803"
---
# <a name="migrate-existing-meetings-and-meeting-content"></a>Migration des réunions existantes et du contenu des réunions

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-22_

Lorsqu’un compte d’utilisateur est déplacé de Lync Server 2010 vers un serveur Lync Server 2013, les informations suivantes sont déplacées à l’aide de ce compte d’utilisateur :

  - **Réunions déjà planifiées par l’utilisateur**. Cela inclut le déplacement des répertoires de conférences et des données de conférence.

  - **Code confidentiel (pin) de l’utilisateur**. Le code confidentiel actuel de l’utilisateur continue de fonctionner tant qu’il n’a pas expiré ou que l’utilisateur ne demande pas de nouveau code secret.

Les informations de compte d’utilisateur suivantes ne sont pas déplacées vers le nouveau serveur.

  - **Contenu** de la réunion. Pour déplacer le contenu partagé pendant une réunion (par exemple, PowerPoint, tableau blanc, pièces jointes ou interrogation), utilisez le paramètre **-MoveConferenceData** dans le cadre de l’applet de commande **Move-Csuser** .

</div>

<span> </span>

</div>

</div>

</div>

