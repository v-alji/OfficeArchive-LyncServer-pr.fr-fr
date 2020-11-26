---
title: 'Lync Server 2013 : Fonctionnalités non prises en charge par le routage géodépendant'
description: 'Lync Server 2013 : les fonctionnalités ne sont pas prises en charge par le routage Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capabilities not supported by Location-Based Routing
ms:assetid: c3d54953-a7d6-4465-a6c3-ae411b2d8ea9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994071(v=OCS.15)
ms:contentKeyID: 51803982
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf9cd03a8cbdd50e136605c4f172598b2ad3f523
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435606"
---
# <a name="capabilities-not-supported-by-location-based-routing-in-lync-server-2013"></a>Fonctionnalités non prises en charge par le routage géodépendant dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2014-03-12_

Location-Based le routage n’est pas applicable aux types d’interactions suivants. Location-Based le routage n’est pas appliqué lorsque les points de terminaison Lync interagissent avec les points de terminaison RTC grâce à ces fonctionnalités.

  - Appels RTC entrants pour les conférences

  - Appels RTC entrants et sortants via le groupe de réponse

  - Parcage d’appel ou récupération des appels via le parcage d’appels

  - Appels RTC entrants pour le service d’annonce

  - Appels RTC entrants récupérés via la prise d’appel de groupe

Pour appliquer les règles de routage de Location-Based aux types d’interactions dans la liste suivante, vous devez activer le routage Location-Based pour les conférences :

  - Appels RTC sortants à partir des conférences

  - Escalades à partir de conversations audio d’P2P vers des conférences impliquant des points de terminaison RTC

  - Transferts consultatifs impliquant les points de terminaison RTC

Pour activer Location-Based le routage des conférences, voir [routage basé sur l’emplacement pour les conférences dans Lync Server 2013](lync-server-2013-location-based-routing-for-conferencing.md).

<div>

## <a name="see-also"></a>Voir aussi


[Planification du routage géodépendant dans Lync Server 2013](lync-server-2013-planning-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

