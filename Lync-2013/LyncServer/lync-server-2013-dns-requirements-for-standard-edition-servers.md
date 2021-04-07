---
title: 'Lync Server 2013 : exigences DNS pour les serveurs Standard Edition'
description: 'Lync Server 2013 : exigences DNS pour les serveurs Standard Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Standard Edition servers
ms:assetid: 3d6bbe65-e7ce-491b-a0bd-d2f7197f240d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425900(v=OCS.15)
ms:contentKeyID: 48183920
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cc93549e07fb82304ad76b051730eab972530764
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393984"
---
# <a name="dns-requirements-for-standard-edition-servers-in-lync-server-2013"></a>Conditions DNS requises pour les serveurs Standard Edition dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Rubrique dernière modification :** 19/06/2012_

Cette section décrit les enregistrements DNS (Domain Name System) requis pour le déploiement de serveurs Standard Edition.

<div>

## <a name="dns-records-for-standard-edition-servers"></a>Enregistrements DNS pour les serveurs Standard Edition

Le tableau suivant spécifie les exigences DNS requises pour le déploiement de serveur Lync Server 2013 Standard Edition.

### <a name="dns-requirements-for-a-standard-edition-server"></a>Conditions DNS requises pour un serveur Standard Edition Server

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
<td><p>Enregistrement A interne avec le nom ucupdates-r2. &lt; Domaine SIP résolu à l’adresse IP du service web de mise à jour d’appareil du serveur &gt; Standard Edition. Dans la situation où un appareil de UC est allumé, mais qu’un utilisateur ne s’est jamais connecté à l’appareil, l’enregistrement A permet à l’appareil de découvrir le service web de mise à jour de l’appareil hébergeant le serveur et d’obtenir des mises à jour. Les périphériques peuvent autrement se procurer ces informations via une mise en service de la bande entrante la première fois qu’un utilisateur se connecte.</p></td>
</tr>
<tr class="even">
<td><p>Proxy inverse pour prendre en charge le trafic HTTP</p></td>
<td><p>Enregistrement A externe qui résout le FQDN de la batterie de serveurs web externe sur l’adresse IP externe du proxy inverse. Les clients et appareils de lauc utilisent cet enregistrement pour se connecter au proxy inverse. Pour plus d’informations, voir <a href="lync-server-2013-determine-dns-requirements.md">Déterminer les exigences DNS pour Lync Server 2013</a> dans la documentation de planification.</p></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</div>

