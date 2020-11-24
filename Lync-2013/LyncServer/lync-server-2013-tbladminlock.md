---
title: 'Lync Server 2013 : tblAdminLock'
description: 'Lync Server 2013 : tblAdminLock.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblAdminLock
ms:assetid: 785a43c0-6892-474c-821c-fa9cdbeb99d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558665(v=OCS.15)
ms:contentKeyID: 48184560
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c3313826b2c0d578c515fb25f83e713b8978ae63
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394341"
---
# <a name="tbladminlock-in-lync-server-2013"></a>tblAdminLock dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-06-25_

tblAdminLock contient le verrouillage de l’administrateur requis pour exécuter certaines commandes administrateur.

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
<td><p>lockExpiresTime</p></td>
<td><p>DATEHEURE, pas null</p></td>
<td><p>Verrouillage de la date et de l’heure d’expiration. Le propriétaire peut prolonger cette valeur périodiquement.</p></td>
</tr>
<tr class="even">
<td><p>lockServerID</p></td>
<td><p>ent, non null</p></td>
<td><p>ID du serveur propriétaire du verrou.</p></td>
</tr>
<tr class="odd">
<td><p>lockActorID</p></td>
<td><p>ent, non null</p></td>
<td><p>ID de l’entité propriétaire du verrou.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

