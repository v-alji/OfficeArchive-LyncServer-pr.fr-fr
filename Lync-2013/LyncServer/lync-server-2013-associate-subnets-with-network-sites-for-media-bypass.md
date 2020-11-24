---
title: 'Lync Server 2013 : Association de sous-réseaux avec les sites réseau pour la dérivation multimédia'
description: 'Lync Server 2013 : associez des sous-réseaux avec les sites réseau pour une dérivation multimédia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Associate subnets with network sites for media bypass
ms:assetid: 5bc632b7-1446-470f-b332-48ea0ca4d1fd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398401(v=OCS.15)
ms:contentKeyID: 48184244
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee03b51d29a88ff634cb87385c5889c35acd8884
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395164"
---
# <a name="associate-subnets-with-network-sites-for-media-bypass-in-lync-server-2013"></a>Associez des sous-réseaux aux sites réseau pour une dérivation multimédia dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-09-12_

<div>


> [!NOTE]  
> Dans cette rubrique, nous partons du principe que vous avez configuré les paramètres globaux de contournement du média et que vous avez configuré la région du réseau et les sites réseau pour la dérivation multimédia.



</div>

Chaque sous-réseau de votre réseau doit être associé à un site réseau spécifique. En effet, les informations de sous-réseau permettent de déterminer le site réseau sur lequel se trouve un point de terminaison. Lorsque les deux parties d’une session sont connues, l’exclusion de média peut déterminer l’endroit où envoyer du contenu multimédia pour le traitement.

La dérivation multimédia n’a aucune configuration particulière requise pour l’Association de sous-réseaux aux sites réseau. Pour créer une association entre les sous-réseaux et les sites réseau dans votre topologie, suivez les procédures décrites dans [associer un sous-réseau à un site réseau dans Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).

<div>

## <a name="next-steps-create-bandwidth-policy-profiles"></a>Étapes suivantes : créer des profils de stratégie de bande passante

Après avoir associé des sous-réseaux aux sites réseau pour le contournement du contenu multimédia, vous devez créer un ou plusieurs profils de stratégie de bande passante pour les partitionner en réseaux avec une bonne connectivité et ceux qui ne le sont pas, aux fins de contournement de média. Tous les sous-réseaux au sein d’une région réseau qui n’ont pas de contraintes de bande passante disposent d’une bonne connectivité et, par conséquent, ces sous-réseaux peuvent utiliser une dérivation multimédia.

Pour plus d’instructions sur la configuration des profils de stratégie de bande passante, voir [créer des profils de stratégie de bande passante dans Lync Server 2013](lync-server-2013-create-bandwidth-policy-profiles.md).

</div>

</div>

<span> </span>

</div>

</div>

</div>

