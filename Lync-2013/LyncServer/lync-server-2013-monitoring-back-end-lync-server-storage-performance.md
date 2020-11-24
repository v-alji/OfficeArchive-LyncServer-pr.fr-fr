---
title: 'Lync Server 2013 : surveillance des performances du stockage principal de Lync Server'
description: 'Lync Server 2013 : surveillance des performances du stockage principal de Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring back end Lync Server 2013 storage performance
ms:assetid: 71627c70-1953-4ac2-afbe-f3ad85be0f44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720917(v=OCS.15)
ms:contentKeyID: 63969619
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7501418d3589b941b7e92d2b414492c1d27a3ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394172"
---
# <a name="monitoring-back-end-lync-server-2013-storage-performance"></a>Surveiller les performances de stockage de Lync Server 2013 en arrière-plan

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2014-05-02_

Les bases de données principales de Lync Server 2013 constituent un élément essentiel du déploiement de Lync Server 2013. Nous vous recommandons de surveiller en permanence les bases de données et les journaux de transactions correspondants pour vous assurer que le serveur Lync Server 2013 fonctionne de façon optimale.

Le tableau suivant identifie les compteurs de performance qui doivent être surveillés pour en savoir plus sur les performances de stockage. Les valeurs de référence de ces compteurs doivent d’abord être définies (lorsque le système se trouve à sa normale, charge attendue) pour comprendre les changements de performance lorsque le système est surchargé.

### <a name="performance-counters-to-be-monitored"></a>Compteurs de performance à surveiller

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Compteur de performance</th>
<th>Seuils de référence</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Transactions/s (RTC)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Transactions/s (RTCDyn)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Transactions/s (tempdb)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Vidages du journal/s (RTC)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Vidages du journal/s (RTCDyn)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Vidages du journal/s (tempdb)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Transferts de disque/s (lecture + écriture)-RTC DB</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Transferts de disque/s-journal RTC</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Transferts de disque/s-RTCDyn DB</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Transfert de disque/s-journal de RTCDyn</p></td>
<td></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

