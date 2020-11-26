---
title: 'Lync Server 2013 : Nouvelles fonctionnalités de haute disponibilité et de récupération d’urgence'
description: 'Lync Server 2013 : nouvelles fonctionnalités de reprise après sinistre et de haute disponibilité.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New disaster recovery and high availability features
ms:assetid: 4fa7cd0f-784b-4d3f-b839-432c2ecaf7c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204892(v=OCS.15)
ms:contentKeyID: 48184130
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92816f61b66d9eed76c16286aaa6c7392dca7708
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425113"
---
# <a name="new-disaster-recovery-and-high-availability-features-in-lync-server-2013"></a>Nouvelles fonctionnalités de haute disponibilité et de récupération d’urgence dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-09-20_

Comme dans Lync Server 2010, le schéma principal de haute disponibilité pour Lync Server 2013 repose sur la redondance du serveur via le regroupement. Si un serveur exécutant un rôle serveur particulier rencontre une défaillance, les autres serveurs du pool qui exécutent le même rôle assument la charge de ce serveur. Cela s’applique aux serveurs frontaux, aux serveurs Edge, aux serveurs de médiation et aux directeurs.

Lync Server 2013 ajoute de nouvelles mesures de reprise après sinistre en vous permettant de jumeler les pools front-end situés dans deux centres de données. Si l’une des listes de réserve s’affiche, un administrateur peut basculer sur les utilisateurs de ce pool vers l’autre pool de la paire pour garantir la continuation du service. Cette fonctionnalité n’exige pas de solutions réseau ou matérielles onéreuses, telles que les réseaux de stockage ou les disques partagés.

Lync Server 2013 ajoute également la haute disponibilité du serveur principal. Il s’agit d’une topologie facultative dans laquelle vous déployez deux serveurs dorsaux pour un pool frontal, et configurez la mise en miroir SQL synchrone pour toutes les bases de données Lync exécutées sur les serveurs dorsaux. Vous pouvez décider de déployer un témoin pour le miroir.

<div>

## <a name="see-also"></a>Voir aussi


[Planification de la haute disponibilité et de la récupération d’urgence dans Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

