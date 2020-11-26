---
title: 'Lync Server 2013 : gestion des groupes de réponse'
description: 'Lync Server 2013 : gestion des groupes de réponse.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing response groups
ms:assetid: 5a804d7d-3c1a-4647-a0e0-d5c4c8c23b73
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520996(v=OCS.15)
ms:contentKeyID: 48184222
ms.date: 02/01/2018
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 138ece386d55895893402e5a1fdead58790504f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437209"
---
# <a name="managing-response-groups-in-lync-server-2013"></a>Gestion des groupes de réponses dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2018-02-01_

Les Response Groups sont une fonctionnalité de gestion des appels qui vous permet d’effectuer la mise en file d’attente d’appels passés vers une zone spécifique, par exemple un support technique, puis diriger les appels vers un groupe de personnes désignés, appelé *agents*.

Pour gérer les groupes de réponse, vous configurez des groupes d’agents, des files d’attente et des flux de travail, qui définissent ce qu’il advient de l’appel jusqu’à ce qu’un agent réponde.

<div>


> [!NOTE]  
> Si vous avez plus de flux de travail 300 dans un seul pool dans le déploiement de votre groupe de réponse, il est préférable d’utiliser les applets de cmdlet Lync Server Management Shell pour créer les flux de travail. Si vous utilisez l’outil de configuration de Response Group pour créer des flux de travail pour un pool qui comporte plus de flux de travail 300, le chargement de la page Web prend du temps. Le nombre d’agents indirectement associés à des flux de travail par le biais des files d’attente a également un effet proportionnel sur le chargement de la page.



</div>

Les rubriques de cette section fournissent des procédures pas à pas pour les tâches que vous pouvez effectuer pour personnaliser et mettre à jour l’application Response Group dans votre déploiement.

<div>

## <a name="in-this-section"></a>Dans cette section

  - [Gestion des groupes d’agents de Response Group dans Lync Server 2013](lync-server-2013-managing-response-group-agent-groups.md)

  - [Gestion des files d’attente de groupe de réponses dans Lync Server 2013](lync-server-2013-managing-response-group-queues.md)

  - [Gestion des flux de travail de groupe de réponses dans Lync Server 2013](lync-server-2013-managing-response-group-workflows.md)

  - [Gestion des paramètres du groupe de réponses au niveau de l’application dans Lync Server 2013](lync-server-2013-managing-application-level-response-group-settings.md)

  - [Déplacer des groupes de réponse vers un nouveau pool dans Lync Server 2013](lync-server-2013-moving-response-groups-to-a-new-pool.md)

  - [Gestion des groupes Response Group dans Lync Server 2013 lors d’un sinistre](lync-server-2013-managing-response-groups-during-a-disaster.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

