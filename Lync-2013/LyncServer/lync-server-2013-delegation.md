---
title: 'Lync Server 2013 : Délégation'
description: 'Lync Server 2013 : délégation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delegation
ms:assetid: 89e76e5c-3cfb-4504-8d0d-7509c8ba9815
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994045(v=OCS.15)
ms:contentKeyID: 51803956
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6dc25d0ea3dfd64ee1b71677e6bac55c1cb1ca32
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430741"
---
# <a name="delegation-in-lync-server-2013"></a>Délégation dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-03-09_

Les fonctionnalités de délégation de Lync sont affectées par le routage Location-Based de la façon suivante :

  - Lorsqu’un délégué activé pour le routage de Location-Based place un appel au nom d’un responsable, la stratégie vocale du délégué est utilisée pour autoriser l’appel et la stratégie de routage de la voix du site du délégué sera utilisée pour diriger l’appel.

  - Pour les appels RTC passés à un responsable, les règles applicables au transfert d’appel ou à la sonnerie simultanée sont utilisées, comme décrit dans les rubriques « Transfert et renvoi des appels » et « Sonnerie simultanée ».

  - Si un délégué définit un point de terminaison RTC comme cible de sonnerie simultanée, pour un appel entrant passé à un responsable, la stratégie de routage des communications vocales du site associé à la jonction entrante est utilisée pour acheminer l‘appel vers le point de terminaison RTC du délégué.

  - Pour la délégation, il est recommandé que le responsable et ses délégués soient situés dans le même site réseau.

<div>

## <a name="see-also"></a>Voir aussi


[Scénarios de routage géodépendant dans Lync Server 2013](lync-server-2013-scenarios-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

