---
title: 'Lync Server 2013 : Planification de la haute disponibilité et de la récupération d’urgence'
description: 'Lync Server 2013 : planification d’une haute disponibilité et de récupération d’urgence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for high availability and disaster recovery
ms:assetid: 15a72073-0336-45dd-b2a0-35e7522c6000
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204703(v=OCS.15)
ms:contentKeyID: 48183497
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6bb5f430201c48738421c4fbe72151ca58173898
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442956"
---
# <a name="planning-for-high-availability-and-disaster-recovery-in-lync-server-2013"></a>Planification de la haute disponibilité et de la récupération d’urgence dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-10-31_

Comme dans Lync Server 2010, le principal schéma de haute disponibilité pour la plupart des rôles serveur dans Lync Server 2013 repose sur la redondance du serveur via le regroupement. Si un serveur exécutant un rôle serveur particulier rencontre une défaillance, les autres serveurs du pool qui exécutent le même rôle assument la charge de ce serveur. Cela s’applique aux serveurs frontaux, aux serveurs Edge, aux serveurs de médiation et aux directeurs.

Lync Server 2013 ajoute de nouvelles mesures de reprise après sinistre pour les pools front-end en introduisant la dispersion géographique de vos serveurs dans deux centres de données afin de garantir la continuation du service.

Lync Server 2013 améliore également la disponibilité élevée du serveur principal en prenant en charge la mise en miroir SQL synchrone pour vos bases de données principales.

Cette section décrit les principales fonctionnalités de haute disponibilité et de récupération d’urgence, ainsi que les actions que vous pouvez effectuer pour une disponibilité élevée et une reprise après sinistre pour vos autres rôles de serveur.

<div>

## <a name="in-this-section"></a>Dans cette section

  - [Récupération d’urgence de pool frontal dans Lync Server 2013](lync-server-2013-front-end-pool-disaster-recovery.md)

  - [Récupération d’urgence de serveur Edge dans Lync Server 2013](lync-server-2013-edge-server-disaster-recovery.md)

  - [Planification de la résistance Voix Entreprise dans Lync Server 2013](lync-server-2013-planning-for-enterprise-voice-resiliency.md)

  - [Fonctionnalités de gestion des appels pour la récupération d’urgence dans Lync Server 2013](lync-server-2013-call-management-features-for-disaster-recovery.md)

  - [Configuration d’un serveur de conversation permanente pour la haute disponibilité et la récupération d’urgence dans Lync Server 2013](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md)

  - [Résistance de sites métropolitains Lync Server 2010](lync-server-2013-compatibility-with-lync-server-2010-metropolitan-site-resiliency.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

