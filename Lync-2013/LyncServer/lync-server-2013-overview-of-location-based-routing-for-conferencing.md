---
title: 'Lync Server 2013 : vue d’ensemble des Location-Based routage des conférences'
description: 'Lync Server 2013 : vue d’ensemble des Location-Based routage des conférences.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Location-Based Routing for conferencing
ms:assetid: 8b86740e-db95-4304-bb83-64d0cbb91d47
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362815(v=OCS.15)
ms:contentKeyID: 56335084
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a8fe9cdf4a797243c3ec04b3466011f374fb0d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394981"
---
# <a name="overview-of-location-based-routing-for-conferencing-in-lync-server-2013"></a>Vue d’ensemble du routage de Location-Based pour les conférences dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-07-19_

L’application de conférence de routage de Location-Based fournit aux conférences Lync un mécanisme de prévention du contournement du numéro RTC. L’application surveille les conférences actives et applique Location-Based restrictions de routage en fonction de l’emplacement des utilisateurs de Lync qui participent.

L’application de conférence de routage de Location-Based détermine si le routage de Location-Based doit être appliqué sur une réunion Lync si les critères suivants sont satisfaits :

  - L’organisateur de la réunion est activé pour le routage de Location-Based. Location-Based restrictions de routage sera appliquée uniquement aux conférences organisées par des utilisateurs qui sont activés pour le routage Location-Based.

  - Au moins un participant à la réunion est un point de terminaison PSTN. Location-Based restrictions de routage s’appliquent uniquement aux conférences qui incluent des points de terminaison PSTN.

  - Le site réseau sur lequel la passerelle PSTN utilisée pour relier la conférence au réseau téléphonique commuté est localisée, de même que les sites réseau depuis lesquels les organisateurs et les participants se connectent.

L’application de conférence de routage Location-Based empêche la participation d’utilisateurs Lync et de points de terminaison RTC provenant de différents sites réseau à la même conférence. Si l’organisateur d’une réunion est activé pour le routage Location-Based, l’application de conférence applique les restrictions suivantes :

  - Les points de terminaison qui peuvent participer à une réunion Lync varient en fonction des points de terminaison qui ont déjà rejoint la Conférence, et cette restriction s’ajuste en tant que points de terminaison joints et de nouveaux points de terminaison rejoindre la Conférence. Si les organisateurs et les participants se connectent à une réunion Lync à partir du même site réseau, un point de terminaison PSTN, un autre participant du même site réseau, un autre participant d’un site de réseau différent ou un participant d’un site réseau inconnu peuvent être affiliés.

  - Si les organisateurs et les participants rejoignent la réunion à partir d’autres sites réseaux ou de sites réseau inconnus, un point de terminaison PSTN n’est pas autorisé à rejoindre la réunion si l’appel PSTN provient d’une jonction SIP pour laquelle le routage géodépendant est activé.

  - Si les organisateurs et les participants se connectent à la réunion à partir du même site réseau et qu’il y a des participants qui rejoignent la même réunion à partir du RTC, un point de terminaison Lync d’un site réseau différent n’est pas autorisé à rejoindre la réunion.

Les restrictions de routage Location-Based de conférences sont résumées dans le tableau suivant.


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Utilisateur(s) dans une conférence à un moment donné</p></td>
<td><p>Utilisateur(s) autorisés à rejoindre la conférence</p></td>
<td><p>Utilisateur(s) non autorisés à rejoindre la conférence</p></td>
</tr>
<tr class="even">
<td><p>Utilisateurs du client VoIP Lync à partir d’un site réseau unique</p></td>
<td><p>Utilisateur du client VoIP Lync à partir du même site réseau</p>
<p>Utilisateur du client VoIP Lync sur un autre site réseau</p>
<p>Utilisateur du client VoIP Lync à partir d’un site réseau inconnu</p>
<p>Utilisateur fédéré du client VoIP Lync</p>
<p>Utilisateur rejoignant la conférence à partir d’un point de terminaison PSTN</p></td>
<td><p>Aucune</p></td>
</tr>
<tr class="odd">
<td><p>Utilisateur (s) client VoIP Lync à partir d’un site réseau inconnu</p></td>
<td><p>Client VoIP Lync sur n’importe quel site</p>
<p>Utilisateur du client VoIP Lync d’un site inconnu</p>
<p>Utilisateur fédéré du client VoIP Lync</p></td>
<td><p>Utilisateur rejoignant la conférence via un point de terminaison PSTN</p></td>
</tr>
<tr class="even">
<td><p>Utilisateurs du client VoIP Lync provenant de différents sites réseau</p></td>
<td><p>Utilisateur du client VoIP Lync de n’importe quel site réseau</p>
<p>Utilisateur du client VoIP Lync à partir d’un site réseau inconnu</p>
<p>Utilisateur fédéré du client VoIP Lync</p></td>
<td><p>Utilisateur rejoignant la conférence via un point de terminaison PSTN</p></td>
</tr>
<tr class="odd">
<td><p>Utilisateurs du client VoIP Lync à partir d’un site réseau unique et utilisateurs qui se connectent à partir d’un point de terminaison RTC</p></td>
<td><p>Utilisateur du client VoIP Lync à partir du même site réseau</p></td>
<td><p>Utilisateur du client VoIP Lync sur un autre site réseau</p>
<p>Utilisateur du client VoIP Lync à partir d’un site réseau inconnu</p>
<p>Utilisateur fédéré du client VoIP Lync</p></td>
</tr>
</tbody>
</table>


Voici les caractéristiques supplémentaires de l’application de conférence de routage de Location-Based :

  - Lorsqu’un utilisateur n’est pas autorisé à rejoindre une conférence fournie Location-Based restrictions de routage, les utilisateurs qui participent à la Conférence seront rejetés et son client Lync signalera que l’appel n’a pas abouti ou a pris fin.

  - Un point de terminaison RTC rejoignant une conférence à l’aide de Location-Based les application de routage ne sera pas limité à la réunion, quel que soit son état, si le point de terminaison est joint par le biais d’un Trunk qui n’est pas activé pour le routage de Location-Based.

  - Un système PBX connecté à un serveur de médiation par le biais d’un réseau SIP qui ne dépose aucun appel vers le RTC aura les mêmes conséquences que les utilisateurs de Lync situés sur le même site réseau où le Trunk SIP est défini. Par exemple, un point de terminaison PSTN peut participer à une conférence avec un utilisateur PBX et un utilisateur Lync s’il se trouve sur le même site réseau. dans le cas contraire, le point de terminaison PSTN ne sera pas autorisé à rejoindre la Conférence si l’utilisateur PBX se trouve sur un autre site réseau que l’utilisateur Lync.

</div>

<span> </span>

</div>

</div>

</div>

