---
title: 'Lync Server 2013 : Table DeRegisterType'
description: 'Tableau Lync Server 2013 : DeRegisterType'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DeRegisterType table
ms:assetid: 09148118-6209-4fd7-a494-99118689a245
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398142(v=OCS.15)
ms:contentKeyID: 48183346
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: afad63c2abeba3e91565e07dac75d0ac6c96ca3a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429558"
---
# <a name="deregistertype-table-in-lync-server-2013"></a>Table DeRegisterType dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-09-28_

La table DeRegisterType est une table statique qui stocke la liste de types de déregistreurs d’utilisateurs possibles, par exemple « client lancé », « inscription expirée » ou « le client a cessé de répondre ».


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Colonne</th>
<th>Type de données</th>
<th>Clé/Index</th>
<th>Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>DeRegisterTypeId</strong></p></td>
<td><p>tinyint</p></td>
<td><p>Principal</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><strong>DeRegisterReason</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td></td>
<td><p>Valeurs autorisées :</p>
<ul>
<li><p>0--Inconnu</p></li>
<li><p>1--le client a démarré la suppression</p></li>
<li><p>2--inscription expirée</p></li>
<li><p>3-client bloqué</p></li>
<li><p>4--attributs utilisateur modifiés</p></li>
<li><p>5 – Bureau d’enregistrement préféré modifié</p></li>
<li><p>6--client hérité en mode de survie</p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

