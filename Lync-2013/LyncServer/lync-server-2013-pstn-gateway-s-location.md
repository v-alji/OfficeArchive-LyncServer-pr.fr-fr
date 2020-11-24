---
title: 'Lync Server 2013 : Emplacement de la passerelle RTC'
description: 'Lync Server 2013 : emplacement de la passerelle PSTN.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN gateway's location
ms:assetid: 49693a35-fad3-49ee-a71e-c7e4537b79aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994031(v=OCS.15)
ms:contentKeyID: 51803940
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f793249908bd1f064f9038ddd90c7f5b01a61d5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394589"
---
# <a name="pstn-gateways-location-in-lync-server-2013"></a>Emplacement de la passerelle RTC dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-03-09_

Les appels routés via des passerelles RTC et des PBX peuvent exiger des restrictions de routage de Location-Based en fonction de l’emplacement de ces systèmes. Location-Based le routage peut être activé en fonction du niveau de granularité par Trunk.

Location-Based le routage présente l’ensemble de règles suivant lorsqu’il est activé sur un Trunk :

  - Lorsque Location-Based routage est activé sur une base par Trunk, les règles définies sur ce Trunk s’appliquent uniquement aux appels routés via ce Trunk.

  - Pour éviter les péages RTC dans lesquels les appels proviennent d’un site réseau différent du site réseau sur lequel se trouve la passerelle RTC, Location-Based le routage introduit l’Association d’un site réseau à un Trunk donné. Cela permet de définir le site réseau qui permet l’acheminement des appels vers une jonction donnée.

Les types de Trunk peuvent être activés pour le routage Location-Based de deux manières :

  - La jonction est définie pour une passerelle RTC qui fait sortir les appels vers le réseau téléphonique commuté (RTC). Les appels entrants pris en charge par une jonction de ce type sont acheminés uniquement vers les points de terminaison situés au sein du même site réseau que la jonction.

  - Le Trunk est défini pour un homologue de serveur de médiation qui ne sort pas les appels vers les utilisateurs RTC et services avec des téléphones hérités dans des emplacements statiques (tels que les téléphones PBX). Pour cette configuration particulière, tous les appels entrants acheminés par une jonction de ce type sont considérés comme provenant du même site réseau que la jonction. Les appels des utilisateurs PBX auront la même Location-Based l’application du routage que les utilisateurs de Lync situés dans le même site réseau que le Trunk. Si deux systèmes PBX situés dans des sites réseau séparés sont connectés via Lync Server, Location-Based le routage autorise le routage à partir d’un point de terminaison PBX dans un site réseau à un autre point de terminaison PBX dans l’autre site du réseau. Ce scénario ne sera pas bloqué par le routage Location-Based. Outre ce scénario et de la même manière qu’un utilisateur Lync dans le même emplacement, les points de terminaison connectés à un homologue de serveur de médiation doté de cette configuration sont en mesure de passer ou de recevoir des appels vers et à partir d’autres homologues du serveur de médiation qui ne routent pas les appels vers le RTC Tous les appels entrants, les appels sortants, les transferts d’appel et les transferts d’appel impliquant des points de terminaison RTC sont soumis à un routage basé sur l’emplacement pour utiliser uniquement les passerelles RTC définies comme étant locales pour ce serveur de médiation.

<div>

## <a name="see-also"></a>Voir aussi


[Instructions de routage géodépendant dans Lync Server 2013](lync-server-2013-guidance-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

