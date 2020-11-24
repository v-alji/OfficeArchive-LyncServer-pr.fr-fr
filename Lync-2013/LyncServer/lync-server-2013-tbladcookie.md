---
title: 'Lync Server 2013 : tblADCookie'
description: 'Lync Server 2013 : tblADCookie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblADCookie
ms:assetid: 0a9102c4-47aa-40ea-8a0d-20e72ab09848
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558610(v=OCS.15)
ms:contentKeyID: 48183366
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 41c3dde3730ede07b204a473c7fe0a5ab68054d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394345"
---
# <a name="tbladcookie-in-lync-server-2013"></a>tblADCookie dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-06-25_

tblADCookie contient les cookies de synchronisation LDAP (Lightweight Directory Access Protocol) actuels.

### <a name="columns"></a>Celles

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Colonne</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>prinGuid</p></td>
<td><p>GUID, pas null</p></td>
<td><p>GUID principal du domaine qui est surveillé.</p></td>
</tr>
<tr class="even">
<td><p>prinDCHost</p></td>
<td><p>nvarchar (255)</p></td>
<td><p>Nom de domaine complet (FQDN) du contrôleur de domaine actuel utilisé pour la synchronisation des services de domaine Active Directory (AD DS). A une valeur d’information.</p></td>
</tr>
<tr class="odd">
<td><p>adcContent</p></td>
<td><p>image (binaire)</p></td>
<td><p>Cookie de synchronisation Active Directory.</p></td>
</tr>
<tr class="even">
<td><p>lastUpdated</p></td>
<td><p>DateHeure</p></td>
<td><p>Date et heure de la mise à jour de ligne.</p></td>
</tr>
<tr class="odd">
<td><p>lockedUntil</p></td>
<td><p>DateHeure</p></td>
<td><p>Temps nécessaire au verrouillage de la ligne pour les modifications. Il s’agit d’une partie d’un mécanisme de verrouillage de logiciels qui garantit que seul l’un des services de chat effectue la synchronisation Active Directory à la fois.</p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a>Permettent

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Colonne (s)</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>prinGuid</p></td>
<td><p>Clé primaire.</p></td>
</tr>
<tr class="even">
<td><p>prinGuid</p></td>
<td><p>Clé étrangère avec recherche dans la table principale. prinGuid.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

