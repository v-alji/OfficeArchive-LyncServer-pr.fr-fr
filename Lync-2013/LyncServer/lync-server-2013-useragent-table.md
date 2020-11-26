---
title: 'Lync Server 2013 : Table UserAgent'
description: 'Tableau Lync Server 2013 : UserAgent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserAgent table
ms:assetid: d6bda1c0-b053-457a-9ffa-2ae859788775
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398939(v=OCS.15)
ms:contentKeyID: 48185582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b701d8384313d0267dd566e0c32242f6cc077472
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439127"
---
# <a name="useragent-table-in-lync-server-2013"></a>Table UserAgent dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-05-25_

La table UserAgent est une table qui contient une liste des différents agents utilisateurs ayant participé à des sessions enregistrées dans la base de données. Chaque enregistrement de la table représente un agent utilisateur


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Colonne</strong></th>
<th><strong>Type de données</strong></th>
<th><strong>Clé/Index</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>UserAgentKey</strong></p></td>
<td><p>int</p></td>
<td><p>Principal</p></td>
<td><p>Numéro unique identifiant cet agent utilisateur.</p></td>
</tr>
<tr class="even">
<td><p><strong>UserAgent</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Différent</p></td>
<td><p>Chaîne de l’agent utilisateur.</p></td>
</tr>
<tr class="odd">
<td><p><strong>UAType</strong></p></td>
<td><p>type</p></td>
<td><p> </p></td>
<td><p>1 est un serveur de médiation.</p>
<p>2 est un serveur de conférence A/V.</p>
<p>4 est Lync.</p>
<p>8 est le téléphone IP.</p>
<p>16 est la console Live Meeting.</p>
<p>32 est l’outil de validation du déploiement (DVT).</p>
<p>64 est Lync sur les ordinateurs Macintosh.</p>
<p>128 est Office Communications Server 2007 R2 attendant.</p>
<p>256 est le service d’annonce de conférence.</p>
<p>512 est le standard automatique de conférence.</p>
<p>1024 est une application de Response Group.</p>
<p>2048 est hors du contrôle vocal.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

