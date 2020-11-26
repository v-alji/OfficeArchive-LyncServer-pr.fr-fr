---
title: 'Lync Server 2013 : Planification de la déviation du trafic multimédia'
description: 'Lync Server 2013 : planification d’une dérivation de médias.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for media bypass
ms:assetid: 8ac732b6-8538-4d7b-b1a9-2035e419dac2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398703(v=OCS.15)
ms:contentKeyID: 48184768
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d92a50d9d838b0f13fd6837cbfadee1c48712f0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424479"
---
# <a name="planning-for-media-bypass-in-lync-server-2013"></a>Planification de la déviation du trafic multimédia dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-09-21_

La dérivation multimédia désigne la suppression du serveur de médiation du chemin multimédia dans la mesure du possible pour les appels dont le signalement traverse le serveur de médiation.

La déviation du trafic multimédia peut améliorer la qualité de la voix en diminuant la latence, les conversions inutiles, la perte de paquets possible et le nombre de points de défaillance éventuels. L’évolutivité peut être améliorée, car la suppression du traitement multimédia pour les appels ignorés réduit la charge sur le serveur de médiation. Cette réduction du chargement complète les fonctionnalités du serveur de médiation pour contrôler plusieurs passerelles.

Dans le cas où un site de succursale ne disposant pas d’un serveur de médiation est connecté à un site central par le biais d’un ou de plusieurs liens réseau étendu avec une bande passante limitée, le contournement de média a pour effet de limiter la bande passante en autorisant les contenus multimédias à partir d’un client sur le site central et en arrière-plan.

Le fait de soulager le serveur de médiation contre la transformation de média, le contournement de médias risque également de réduire le nombre de serveurs de médiation requis par une infrastructure vocale d’entreprise.

La figure suivante montre des médias de base et des voies de signalisation dans des topologies avec et sans déviation du trafic multimédia.

**Médias et voies de signalisation avec et sans déviation du trafic multimédia**

![Application de connexion de contournement de média CAC vocal](images/Gg398703.4d66d529-0912-4de1-abec-266f54272eb3(OCS.15).jpg "Application de connexion de contournement de média CAC vocal")

En règle générale, essayez d’activer la déviation du trafic multimédia quand cela est possible.

<div>

## <a name="in-this-section"></a>Dans cette section

  - [Présentation de l’exclusion de médias dans Lync Server 2013](lync-server-2013-overview-of-media-bypass.md)

  - [Modes de déviation du trafic multimédia dans Lync Server 2013](lync-server-2013-media-bypass-modes.md)

  - [Déviation du trafic multimédia et contrôle d’admission des appels dans Lync Server 2013](lync-server-2013-media-bypass-and-call-admission-control.md)

  - [Configuration technique requise pour la déviation du trafic multimédia dans Lync Server 2013](lync-server-2013-technical-requirements-for-media-bypass.md)

</div>

<div>

## <a name="related-sections"></a>Sections associées

[Déploiement de fonctionnalités avancées d’entreprise voix dans Lync Server 2013](lync-server-2013-deploying-advanced-enterprise-voice-features.md)

</div>

<div>

## <a name="see-also"></a>Voir aussi


[Configure a trunk with media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-with-media-bypass.md)  


[Options de contournement global de médias dans Lync Server 2013](lync-server-2013-global-media-bypass-options.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

