---
title: 'Lync Server 2013 : conditions DNS requises pour les pools frontaux'
description: 'Lync Server 2013 : conditions DNS requises pour les pools frontaux.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pools
ms:assetid: ba28919c-fbbe-4c54-8bf9-2b0cd3fa39c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412910(v=OCS.15)
ms:contentKeyID: 48185228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c0369e82bd8ed2ea63e2156728b41f9942b0148
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429069"
---
# <a name="dns-requirements-for-front-end-pools-in-lync-server-2013"></a>Conditions DNS requises pour les pools frontaux dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Rubrique dernière modification :** 11/11/2012_

Cette section décrit les enregistrements DNS (Domain Name System) requis pour le déploiement de pools frontaux.

<div>

## <a name="dns-records-for-front-end-pools"></a>Enregistrements DNS pour les pools frontaux

Le tableau suivant spécifie les exigences DNS requises pour un déploiement de pool frontal Lync Server 2013.

### <a name="dns-requirements-for-a-front-end-pool"></a>Conditions DNS requises pour un pool frontal

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
<td><p>Groupe frontal avec plusieurs serveurs frontaux et équilibrage de la charge matérielle (que l’équilibrage de charge DNS soit également déployé sur ce pool)</p></td>
<td><p>Lors de l’utilisation de l’équilibrage de charge DNS et d’un équilibrage de charge matérielle, vous devez utiliser les enregistrements Hôte (A). Créez un enregistrement A interne qui résout le nom de domaine complet (FQDN) du pool frontal pour l’équilibrage de charge du DNS. Créez un enregistrement hôte interne (A) pour les services web internes à l’adresse IP virtuelle (VIP) de l’équilibreur de charge. Vous devez utiliser le nom des services web internes, tel que défini dans le Générateur de topologie.</p>
<p>Par exemple, si vous utilisez à la fois l’équilibrage de charge DNS et l’équilibrage de charge matérielle, vous avez un enregistrement A pour chaque serveur frontal dans un pool pour l’équilibrage de charge DNS, et un enregistrement A pour les services Web internes pointant vers l’adresse IP virtuelle du balanceur de charge matérielle :</p>
<ul>
<li><p>Équilibrage de charge DNS : Pool01.contoso.net IP du pool 10.10.10.5</p>
<div>

> [!WARNING]  
> Chaque serveur frontal aura également un enregistrement A distinct :


</div>
<ol>
<li><p>FE01.contoso.net 10.10.10.1</p></li>
<li><p>FE02.contoso.net 10.10.10.2</p></li>
<li><p>FE03.contoso.net 10.10.10.3</p></li>
<li><p>FE04.contoso.net 10.10.10.4</p></li>
</ol></li>
<li><p>Équilibrage de charge matérielle : WebInternal.contoso.net IP de vip HLB 192.168.10.5</p></li>
</ul>
<p>Tout le trafic, à l’exception du trafic HTTP/HTTPS, utilisera Pool01.contoso.net enregistrement. Le trafic HTTP/HTTPS utilise l’adresse des services web internes définie 192.168.10.5</p></td>
</tr>
<tr class="even">
<td><p>Pool frontal avec équilibrage de charge DNS déployé</p></td>
<td><p>Un jeu d’enregistrements A internes qui résolvent le nom de source de données (FQDN) du pool sur l’adresse IP de chaque serveur du pool. Un enregistrement A doit être enregistré pour chaque serveur du pool.</p></td>
</tr>
<tr class="odd">
<td><p>Pool frontal avec équilibrage de charge DNS déployé</p></td>
<td><p>Un jeu d’enregistrements A internes qui résolvent le nom de source de données (FQDN) de chaque serveur du pool sur l’adresse IP de ce serveur. Pour plus d’informations, consultez la documentation Planification de l’équilibrage de charge <a href="lync-server-2013-dns-load-balancing.md">DNS dans Lync Server 2013.</a></p></td>
</tr>
<tr class="even">
<td><p>Pool frontal avec un serveur frontal unique et une base de données principale dédiée, mais sans équilibrage de charge</p></td>
<td><p>Enregistrement A interne qui résout le nom de bord du nom de bord (FQDN) du pool frontal sur l’adresse IP du serveur frontal d’entreprise édition unique.</p></td>
</tr>
<tr class="odd">
<td><p>Connectez-vous automatique au client</p></td>
<td><p>Pour chaque domaine SIP pris en charge, un enregistrement SRV pour _sipinternaltls._tcp. &lt; domain &gt; over port 5061 that maps to the FQDN of the Front End pool that authenticates and redirects client requests for sign-in. Pour plus d’informations, consultez la exigences DNS pour la signature automatique du client dans <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">Lync Server 2013.</a></p></td>
</tr>
<tr class="even">
<td><p>Découverte du service web de mise à jour des appareils par les appareils de communications unifiées</p></td>
<td><p>Enregistrement A interne avec le nom ucupdates-r2. &lt; Domaine SIP résolu à l’adresse IP du pool frontal qui héberge le service web De mise à jour &gt; des appareils. Dans la situation où un appareil de UC est allumé, mais qu’un utilisateur ne s’est jamais connecté à l’appareil, l’enregistrement A permet à l’appareil de découvrir le pool frontal hébergeant le service web De mise à jour des appareils et d’obtenir des mises à jour. Dans le cas contraire, les appareils obtiennent ces informations même si une provision à bande s’offre à vous la première fois qu’un utilisateur se connecte.</p>
<div>

> [!IMPORTANT]  
> Si vous avez déjà déployé un service web de mise à jour de l’appareil dans Lync Server 2010, vous avez déjà créé un enregistrement A interne avec le nom « ucupdates ». &lt; Domaine &gt; SIP. Pour Microsoft Office Communications Server 2007 R2, vous devez créer un enregistrement DNS A supplémentaire avec le nom ucupdates-r2. &lt; Domaine &gt; SIP.


</div></td>
</tr>
<tr class="odd">
<td><p>Proxy inverse pour prendre en charge le trafic HTTP</p></td>
<td><p>Enregistrement A externe qui résout le FQDN de la batterie de serveurs web externe sur l’adresse IP externe du proxy inverse. Les clients et appareils de lauc utilisent cet enregistrement pour se connecter au proxy inverse. Pour plus d’informations, voir <a href="lync-server-2013-determine-dns-requirements.md">Déterminer les exigences DNS pour Lync Server 2013</a> dans la documentation de planification.</p></td>
</tr>
</tbody>
</table>


Le tableau suivant montre un exemple des enregistrements DNS requis pour le FQDN de la batterie de serveurs web interne.

### <a name="example-dns-records-for-internal-web-farm-fqdn"></a>Exemples d’enregistrements DNS pour le FQDN de batterie de serveurs web internes

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>FQDN de batterie de serveurs web interne</th>
<th>FQDN du pool</th>
<th>DNS A record(s)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>webcon.contoso.com</p></td>
<td><p>ee-pool.contoso.com</p></td>
<td><p>Enregistrement DNS A pour la ee-pool.contoso.com qui résout l’adresse VIP de l’équilibreur de charge utilisé par les serveurs frontaux.</p>
<p>Enregistrement DNS A pour les webcon.contoso.com résoudre à l’adresse VIP de l’équilibreur de charge utilisé par les serveurs frontaux.</p></td>
</tr>
<tr class="even">
<td><p>ee-pool.contoso.com</p></td>
<td><p>ee-pool.contoso.com</p></td>
<td><p>Enregistrement DNS A pour ee-pool.contoso.com qui résout l’adresse IP virtuelle (VIP) de l’équilibreur de charge utilisé par les serveurs frontaux Enterprise Edition du pool frontal.</p>
<p>Notez que si vous utilisez l’équilibrage de charge DNS sur ce pool, votre pool frontal et votre batterie de serveurs web interne ne peuvent pas avoir le même nom de source de données (FQDN).</p></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</div>

