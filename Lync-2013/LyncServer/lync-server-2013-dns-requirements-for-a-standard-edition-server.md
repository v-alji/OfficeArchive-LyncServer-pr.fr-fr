---
title: 'Lync Server 2013 : Enregistrements DNS requis pour un serveur Standard Edition'
description: 'Lync Server 2013 : conditions DNS requises pour un serveur Standard Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for a Standard Edition server
ms:assetid: 5d1daf54-6e60-4ce0-9254-7d57a0835fa4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204936(v=OCS.15)
ms:contentKeyID: 48184259
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea0c7219563d62a9d99bd85655b3d3fcb0c551f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395028"
---
# <a name="dns-requirements-for-a-standard-edition-server-in-lync-server-2013"></a>Enregistrements DNS requis pour un serveur Standard Edition dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Rubrique dernière modification :** 22/02/2013_

Cette section décrit les enregistrements DNS (Domain Name System) requis pour le déploiement de serveurs Standard Edition.

<div>

## <a name="dns-records-for-standard-edition-servers"></a>Enregistrements DNS pour les serveurs Standard Edition

Le tableau suivant spécifie les exigences DNS requises pour le déploiement de serveur Lync Server 2013 Standard Edition.


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scénario de déploiement</th>
<th>Enregistrement DNS requis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>serveur Standard Edition</p></td>
<td><p>Un enregistrement interne A qui associe le nom de domaine complet (FQDN) du serveur à son adresse IP.</p></td>
</tr>
<tr class="even">
<td><p>Connectez-vous automatique au client</p></td>
<td><p>Pour chaque domaine SIP pris en charge, un enregistrement SRV pour _sipinternaltls._tcp. &lt; domaine sur le port 5061 qui masique le nom de domaine (FQDN) du serveur Standard Edition qui authentifier et redirige les demandes de client pour &gt; la authentification. Pour plus d’informations, consultez la exigences DNS pour la signature automatique du client dans <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">Lync Server 2013.</a></p></td>
</tr>
<tr class="odd">
<td><p>Découverte du service web de mise à jour des appareils par les appareils de communications unifiées</p></td>
<td><p>Enregistrement A interne avec le nom ucupdates-r2. &lt; Domaine SIP résolu à l’adresse IP du service web de mise à jour d’appareil du serveur &gt; Standard Edition. Dans la situation où un appareil de UC est allumé, mais qu’un utilisateur ne s’est jamais connecté à l’appareil, l’enregistrement A permet à l’appareil de découvrir le service web de mise à jour de l’appareil hébergeant le serveur et d’obtenir des mises à jour. Les périphériques peuvent autrement se procurer ces informations via une mise en service de la bande entrante la première fois qu’un utilisateur se connecte. Pour plus d’informations, consultez le service web de mise à jour de <a href="lync-server-2013-device-update-web-service.md">l’appareil dans Lync Server 2013</a> dans la documentation operations.</p></td>
</tr>
<tr class="even">
<td><p>Proxy inverse pour prendre en charge le trafic HTTP</p></td>
<td><p>Enregistrement A externe qui résout le FQDN de la batterie de serveurs web externe sur l’adresse IP externe du proxy inverse. Les clients et appareils de lauc utilisent cet enregistrement pour se connecter au proxy inverse. Pour plus d’informations, voir <a href="lync-server-2013-determine-dns-requirements.md">Déterminer les exigences DNS pour Lync Server 2013</a> dans la documentation de planification.</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a>Voir aussi


[DNS requirements for automatic client sign-in in Lync Server 2013](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md)  
[Détermination de la configuration requise pour DNS pour Lync Server 2013](lync-server-2013-determine-dns-requirements.md)  


[Service web de mise à jour des dispositifs dans Lync Server 2013](lync-server-2013-device-update-web-service.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

