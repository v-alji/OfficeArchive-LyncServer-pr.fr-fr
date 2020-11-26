---
title: Prise en charge du matériel de périphérique dans Lync Server 2013
description: Prise en charge du matériel du périphérique Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device hardware support
ms:assetid: ba07ca91-32b4-49cf-801c-47a2d1d96e18
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412908(v=OCS.15)
ms:contentKeyID: 48185222
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cd03936d35fbc3a639a3ba4596a4357e8e379719
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429449"
---
# <a name="device-hardware-support-in-lync-server-2013"></a>Prise en charge du matériel de périphérique dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-12-14_

Des configurations matérielles spécifiques doivent être en place avant le déploiement de téléphones IP et d’appareils analogiques.

Les téléphones IP exécutant Lync Phone Edition prennent en charge la découverte des couches de liaison Protocol-Media point de terminaison (LLDP-MED) et Power over Ethernet (PoE). Pour tirer parti de LLDP-MED, le commutateur doit prendre en charge les normes IEEE 802.1 AB et ANSI/TIA-1057. Pour tirer parti de la PoE, le commutateur doit prendre en charge le mode PoE 802.3 AF ou 802.3 au.

Pour activer LLDP-MED, l’administrateur doit activer LLDP en utilisant la fenêtre console de basculement et définir la stratégie réseau LLDP-MED avec l’ID VLAN valide.

De plus, si votre déploiement inclut des appareils analogiques, vous devez configurer la passerelle analogique pour utiliser Lync Server et la passerelle doit être l’un des éléments suivants :

  - Un adaptateur de téléphone analogique (ATA)

  - Passerelle analogique PSTN

  - Une unité de branchement Survivable qui inclut une passerelle analogique PSTN

  - Une unité de branchement Survivable qui inclut une passerelle RTC qui communique avec un disque ATA

Pour plus d’informations sur la configuration d’une passerelle analogique, voir la section « planification de déploiement de périphériques analogiques » [https://go.microsoft.com/fwlink/p/?LinkId=268537](https://go.microsoft.com/fwlink/p/?linkid=268537) dans la bibliothèque TechNet de Lync Server 2010. (Les appareils analogiques fonctionnent de la même manière dans Lync Server 2013 que dans Lync Server 2010.)

<div>


> [!IMPORTANT]  
> Si le commutateur prend en charge cette option, vous pouvez configurer le commutateur pour Enhanced 9-1-1 (E9-1-1).



</div>

</div>

<span> </span>

</div>

</div>

</div>

