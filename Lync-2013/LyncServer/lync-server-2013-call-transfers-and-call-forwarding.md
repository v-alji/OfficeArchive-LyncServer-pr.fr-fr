---
title: 'Lync Server 2013 : Transferts et renvois d’appels'
description: 'Lync Server 2013 : transfert d’appel et transfert d’appel.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call transfers and call forwarding
ms:assetid: 978610ec-63c7-4cf6-ad7a-9ef91559bf12
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994051(v=OCS.15)
ms:contentKeyID: 51803962
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9359cb64b386d022eab33e4523dfaccf784075b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435683"
---
# <a name="call-transfers-and-call-forwarding-in-lync-server-2013"></a>Transferts et renvois d’appels dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-03-09_

Lorsqu’un point de terminaison PSTN est impliqué, Location-Based le routage analyse l’emplacement du point de terminaison de 134 et le point de terminaison de transfert ou de transfert de l’appel vers (c.-à-d. transférer/transférer la cible). Location-Based le routage détermine si l’appel doit être transféré ou transféré en fonction de l’emplacement des deux points de terminaison.

Le tableau suivant illustre le scénario d’un utilisateur Lync dans un appel avec un point de terminaison PSTN et l’utilisateur de Lync transfère l’appel vers un autre utilisateur Lync. En fonction de l’emplacement du site du réseau du point de terminaison du destinataire, Location-Based le routage affecte le routage du transfert ou du transfert d’appel.

### <a name="initiating-call-transfer-or-forward"></a>Lancement du transfert ou du renvoi d’appel

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Utilisateur à l’origine du transfert/renvoi d’appel</th>
<th>Point de terminaison cible dans le même site réseau que l’utilisateur à l’origine du transfert ou du renvoi d’appel</th>
<th>Point de terminaison cible dans un autre site réseau que l’utilisateur à l’origine du transfert ou du renvoi d’appel</th>
<th>Le point de terminaison cible est dans un site réseau inconnu ou un site réseau non activé pour le routage de Location-Based</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Utilisateur Lync</p></td>
<td><p>Le transfert ou renvoi de l’appel est autorisé</p></td>
<td><p>Le transfert ou renvoi de l’appel n’est pas autorisé</p></td>
<td><p>Le transfert ou renvoi de l’appel n’est pas autorisé</p></td>
</tr>
</tbody>
</table>

  

Par exemple, un utilisateur Lync dans un appel avec un point de terminaison PSTN transfère l’appel vers un autre utilisateur Lync qui se trouve sur le même site réseau. Dans ce cas, le transfert de l’appel est autorisé.

Le tableau suivant illustre le scénario d’un utilisateur Lync dans un appel d’un autre utilisateur Lync et l’un d’entre eux transfère l’appel à un point de terminaison PSTN. En fonction de l’emplacement de l’utilisateur sur lequel l’appel est transféré, le tableau décrit la façon dont Location-Based le routage affecte l’appel.

### <a name="call-transfer-or-forward-to-pstn-endpoint"></a>Transfert ou renvoi de l’appel vers le point de terminaison RTC

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Point de terminaison cible du transfert/renvoi de l’appel</th>
<th>Utilisateurs de Lync sur le même site réseau</th>
<th>Utilisateurs de Lync dans différents sites réseau</th>
<th>L’un ou les deux utilisateurs de Lync sur un site réseau ou un site réseau inconnu n’ont pas été activés pour le routage Location-Based</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Point de terminaison RTC</p></td>
<td><p>Le transfert ou le renvoi de l’appel est autorisé par la stratégie de routage des communications vocales du site du cessionnaire</p></td>
<td><p>Le transfert ou le renvoi de l’appel est autorisé par la stratégie de routage des communications vocales du site du cessionnaire</p></td>
<td><p>Le transfert ou le renvoi de l’appel est autorisé par la stratégie de voix du cessionnaire, uniquement via des jonctions pour lesquelles le routage géodépendant n’est pas activé</p></td>
</tr>
</tbody>
</table>

  
Par exemple, un utilisateur Lync dans un appel avec un autre utilisateur Lync figurant dans le même site réseau transfère l’appel vers un point de terminaison PSTN et le transfert d’appel est autorisé.

<div>

## <a name="see-also"></a>Voir aussi


[Scénarios de routage géodépendant dans Lync Server 2013](lync-server-2013-scenarios-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

