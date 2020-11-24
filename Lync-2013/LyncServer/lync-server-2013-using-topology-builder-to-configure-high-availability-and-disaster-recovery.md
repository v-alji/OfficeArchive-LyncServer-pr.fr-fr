---
title: Utilisation du générateur de topologie pour configurer la haute disponibilité et la récupération d’urgence
description: Utilisation du générateur de topologie pour configurer une haute disponibilité et une reprise après sinistre.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Topology Builder to configure high availability and disaster recovery
ms:assetid: abc1a25d-1f5e-46ef-91d2-0144fc847206
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205172(v=OCS.15)
ms:contentKeyID: 48185113
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 04764a58ac3ae1bbe0df97aadeabb03158ce8100
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395272"
---
# <a name="using-topology-builder-to-configure-high-availability-and-disaster-recovery-in-lync-server-2013"></a>Utilisation du générateur de topologie pour configurer la haute disponibilité et la récupération d’urgence dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-06_

Dans le générateur de topologie, effectuez les étapes suivantes pour configurer une haute disponibilité et une reprise après sinistre pour le serveur de chat permanent.

1.  Ajoutez les bases de données miroir et les magasins de données secondaires SQL Server.

2.  Modifiez les propriétés du service de chat permanent serveur pour :
    
    1.  activer la mise en miroir pour la base de données primaire ;
    
    2.  Ajoutez le magasin SQL Server en miroir principal.
    
    3.  Activez la base de données d’envoi de journaux de SQL Server.
    
    4.  Ajoutez la banque SQL Server secondaire pour l’envoi du journal SQL Server.
    
    5.  Ajoutez le miroir SQL Server Store pour la base de données secondaire.
    
    6.  Publiez la topologie.

</div>

<span> </span>

</div>

</div>

</div>

