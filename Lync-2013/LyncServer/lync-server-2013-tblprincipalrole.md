---
title: 'Lync Server 2013 : tblPrincipalRole'
description: 'Lync Server 2013 : tblPrincipalRole.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalRole
ms:assetid: dcd16dc1-a66c-4720-a48f-ec8b28337383
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615039(v=OCS.15)
ms:contentKeyID: 48185597
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f58ffda3136c254ee77f14d33dcb42af5d172c4a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393917"
---
# <a name="tblprincipalrole-in-lync-server-2013"></a>tblPrincipalRole dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-09-12_

tblPrincipalRole contient des rôles explicites attribués aux nœuds.

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
<td><p>prinRoleNodeID</p></td>
<td><p>ent, non null</p></td>
<td><p>ID du nœud auquel le rôle s’applique.</p></td>
</tr>
<tr class="even">
<td><p>prinRolePrinID</p></td>
<td><p>ent, non null</p></td>
<td><p>ID du principal.</p></td>
</tr>
<tr class="odd">
<td><p>prinRoleTypeID</p></td>
<td><p>ent, non null</p></td>
<td><p>ID du type de rôle (de tblRoleType)</p></td>
</tr>
<tr class="even">
<td><p>prinRoleUpdatedBy</p></td>
<td><p>ent, non null</p></td>
<td><p>ID de l’élément principal qui a mis à jour cette entrée.</p></td>
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
<th>Colonne</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;prinRoleNodeID, prinRolePrinID, prinRoleTypeID&gt;</p></td>
<td><p>Clé primaire.</p></td>
</tr>
<tr class="even">
<td><p>prinRoleNodeID</p></td>
<td><p>Clé étrangère avec recherche dans la table tblNode. nodeID.</p></td>
</tr>
<tr class="odd">
<td><p>prinRolePrinID</p></td>
<td><p>Clé étrangère avec recherche dans la table tblPrincipal. prinID.</p></td>
</tr>
<tr class="even">
<td><p>prinRoleTypeID</p></td>
<td><p>Clé étrangère avec recherche dans la table tblRoleType. rtypeID.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

