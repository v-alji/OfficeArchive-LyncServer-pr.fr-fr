---
title: 'Lync Server 2013 : vue d’ensemble des Location-Based routage'
description: 'Lync Server 2013 : vue d’ensemble du routage Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Location-Based Routing
ms:assetid: 4aa494bd-0d66-4335-b9e8-f758d44a7202
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994032(v=OCS.15)
ms:contentKeyID: 51803941
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b1e026791a8562629231b91b58d7e7eff569ffa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394980"
---
# <a name="overview-of-location-based-routing-in-lync-server-2013"></a>Vue d’ensemble du routage Location-Based dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-21_

Le routage géodépendant introduit de nouvelles règles modifiant le routage des appels RTC nationaux et internationaux pour empêcher le contournement des frais de réseau téléphonique commuté. Il offre la flexibilité nécessaire pour appliquer ces règles à certaines régions, passerelles ou groupes d’utilisateurs uniquement.

Les scénarios suivants illustrent les types principaux de restrictions Location-Based le routage peut appliquer :

  - Appels de sortie : Location-Based le routage peut imposer des appels sortants à partir d’une passerelle PSTN qui se trouve dans la même région que celle de l’appelant, qui empêche les appels entrants vers la sortie à partir d’une passerelle RTC située dans une région différente de celle de l’appelant.

  - Appels entrants : le routage Location-Based peut empêcher les appels RTC entrants de sonner sur des points de terminaison Lync si la passerelle RTC qui achemine l’appel entrant ne se trouve pas dans la même région que l’utilisateur appelé Lync.

  - Régions inconnues : Location-Based le routage limite les appels RTC entrants et sortants vers et depuis les utilisateurs situés dans des emplacements indéterminés (c’est-à-dire, des utilisateurs distants qui se connectent à partir d’Internet ou qui se trouvent dans des régions inconnues).

  - Régions internationales : le routage Location-Based applique le routage des appels sortants par le biais des passerelles RTC internationales s’il n’y a aucune passerelle locale vers l’emplacement de l’utilisateur.

<div>

## <a name="see-also"></a>Voir aussi


[Planification du routage géodépendant dans Lync Server 2013](lync-server-2013-planning-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

