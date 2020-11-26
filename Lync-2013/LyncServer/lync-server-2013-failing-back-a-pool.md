---
title: 'Lync Server 2013 : Basculement vers un pool'
description: 'Lync Server 2013 : échec de la restauration d’un pool.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing back a pool
ms:assetid: 6232b644-ef57-4c9c-abec-14ff8ffc9fe7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204945(v=OCS.15)
ms:contentKeyID: 48184289
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1c1fc0ea4514d2f951dd936521590d47b809db38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428327"
---
# <a name="failing-back-a-pool-in-lync-server-2013"></a>Basculement vers un pool dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-11-01_

Une fois que le regroupement qui a expérimenté le désastre est en ligne (à savoir Pool1 dans cet exemple), procédez comme suit pour restaurer le statut de travail normal de votre déploiement.

Notez que le processus de restauration automatique prend quelques minutes.  À titre de référence, il devrait prendre jusqu’à 60 minutes pour un pool de 20 000 utilisateurs.

1.  Restaurez les utilisateurs qui ont été initialement hébergés dans Pool1 et qui ont échoué sur Pool2 en tapant l’applet de commande suivante :
    
        Invoke-CsPoolFailback -PoolFQDN <Pool1 FQDN> -Verbose

Aucune autre étape n’est nécessaire. Si vous avez échoué sur le serveur de gestion central, vous pouvez le laisser dans Pool2.

</div>

<span> </span>

</div>

</div>

</div>

