---
title: 'Lync Server 2013 : Conditions prérequises et rôles de configuration d’annonce'
description: 'Lync Server 2013 : conditions préalables et rôles de configuration d’annonce.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Announcement configuration prerequisites and roles
ms:assetid: 82f2dfe9-4c5e-4d65-96a1-96495d506ea4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398658(v=OCS.15)
ms:contentKeyID: 48184674
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8e6e7009adc6826c255e28ddda925b0e9be5fd6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439967"
---
# <a name="announcement-configuration-prerequisites-and-roles-in-lync-server-2013"></a>Conditions prérequises et rôles de configuration d’annonce dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-25_

Annonce est une fonction de gestion des appels voix entreprise. Cette rubrique décrit ce que vous devez mettre en place avant de pouvoir configurer l’annonce et les affectations de rôles nécessaires à l’exécution de tâches de configuration.

Cette section suppose que vous avez lu la documentation de planification liée à l’annonce (voir [planification des fonctionnalités de gestion des appels dans Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).

<div>

## <a name="announcement-configuration-prerequisites"></a>Conditions préalables à la configuration de l’annonce

L’application d’annonce nécessite les composants suivants :

  - service d’application

  - application Response Group

  - Magasin de fichiers, pour contenir des fichiers audio

Tous ces composants sont installés par défaut lorsque vous déployez Enterprise Voice.

</div>

<div>

## <a name="announcement-configuration-roles"></a>Rôles de configuration d’annonce

Pour configurer des annonces, vous pouvez utiliser les outils d’administration suivants :

  - Panneau de configuration Lync Server

  - Lync Server Management Shell

La configuration de l’application d’annonce nécessite l’un des rôles d’administration suivants :

  - **CsVoiceAdministrator**   Ce rôle d’administrateur peut créer, configurer et gérer l’ensemble des stratégies et paramètres relatifs à la voix, y compris les paramètres d’annonce.

  - **CsServerAdministrator**   Ce rôle d’administrateur peut gérer, surveiller et résoudre les problèmes liés aux serveurs et services, et configurer tous les paramètres d’annonce.

  - **CsAdministrator**   Ce rôle d’administrateur peut effectuer toutes les tâches administratives et modifier tous les paramètres.

  - **CsViewOnlyAdministrator**   Ce rôle d’administrateur peut voir le déploiement pour contrôler l’intégrité du déploiement.

<div>


> [!NOTE]  
> Pour plus d’informations sur les privilèges des utilisateurs d’administration, voir <A href="lync-server-2013-planning-for-role-based-access-control.md">planification du contrôle d’accès basé sur les rôles dans Lync Server 2013</A> dans la documentation de planification.



</div>

</div>

<div>

## <a name="see-also"></a>Voir aussi


[Déploiement d’Enterprise Voice dans Lync Server 2013](lync-server-2013-deploying-enterprise-voice.md)  


[Planifier les fonctionnalités de gestion des appels dans Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

