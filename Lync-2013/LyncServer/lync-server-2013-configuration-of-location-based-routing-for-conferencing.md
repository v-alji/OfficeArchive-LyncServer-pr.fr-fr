---
title: 'Lync Server 2013 : configuration du routage géodépendant pour les conférences'
description: 'Lync Server 2013 : configuration du routage Location-Based pour les conférences.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration of Location-Based Routing for conferencing
ms:assetid: d8c708cc-a1b1-48b1-808c-a64df15f7701
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362846(v=OCS.15)
ms:contentKeyID: 56335088
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a87f9c799e565f64b0dd30ce025a4e7a3174625
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395160"
---
# <a name="configuration-of-location-based-routing-for-conferencing-in-lync-server-2013"></a>Configuration du routage géodépendant pour les conférences dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-09-11_

L’application de conférence de routage de Location-Based repose sur la configuration de l' Location-Based routage Lync Server 2013. Les configurations principales suivantes sont disponibles :

  - L’emplacement des participants rejoignant une réunion est déterminé sur la base de leur site réseau. Un site réseau et ses sous-réseaux associés doivent être définis dans Lync Server afin de mettre en œuvre le routage Location-Based.

  - Pour appliquer Location-Based le routage des réunions, les participants de Lync doivent être activés pour le routage Location-Based.

  - Pour faire en sorte que Location-Based le routage de points de terminaison RTC qui rejoint des réunions, le Trunk SIP utilisé pour connecter les points de terminaison PSTN doit être configuré pour le routage de Location-Based.

Pour plus d’informations sur le déploiement et la configuration de Lync Server 2013 Location-Based le routage, consultez la rubrique Configuration du [routage en fonction](lync-server-2013-configuring-location-based-routing.md)de l’emplacement.

<div>

## <a name="enabling-the-location-based-routing-conferencing-application"></a>Activation de l’application de conférence de routage Location-Based

L’application de conférence de routage Location-Based est désactivée par défaut. Avant d’activer cette application, vous devez déterminer la priorité adaptée à affecter à l’application. Pour déterminer cette priorité, exécutez l’applet de commande suivante dans Lync Server Management Shell :

```powershell
Get-CsServerApplication -Identity Service:Registrar:<Pool FQDN>
```

Dans cette applet de \<Pool FQDN\> demande, est le pool dans lequel l’application de conférence de routage Location-Based doit être activée.

Ce cmdlet renverra la liste des applications hébergées par Lync Server et la valeur Priority (priorité) pour chacune d’elles. La Location-Based application de conférence de routage doit être attribuée à une valeur de priorité plus grande que l’application « UdcAgent » et inférieure aux applications « DefaultRouting », « ExumRouting » et « OutboundRouting ». Nous vous recommandons d’affecter à la Location-Based application de routage une valeur de priorité qui est un point plus élevé que la valeur de priorité de l’application « UdcAgent ».

Par exemple, si l’application « UdcAgent » a une valeur de priorité de « 2 », l’application « DefaultRouting » a une valeur de priorité de « 9 », l’application « ExumRouting » a une valeur de priorité de « 9 » et l’application « OutboundRouting » a une valeur de priorité de « 10 », alors vous devez attribuer à la Location-Based l’application de routage de routage. Ainsi, la priorité des applications est définie dans l’ordre suivant : autres applications (priorités : 0 à 1), « UdcAgent » (priorité : 2), application de conférence avec routage géodépendant (priorité : 3), autres applications (priorités : 4 à 8), « DefaultRouting » (priorité : 9), « ExumRouting » (priorité : 10) et « OutboundRouting » (priorité : 11).

Une fois que vous avez trouvé la valeur de priorité correcte pour l’application de conférence de routage Location-Based, tapez l’applet de commande suivante pour chaque pool Front-End ou un serveur Standard Edition sur lequel les utilisateurs ont activé le routage Location-Based :

```powershell
New-CsServerApplication -Identity Service:Registrar:<Pool FQDN>/LBRouting -Priority <Application Priority> -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

Par exemple :

```powershell
New-CsServerApplication -Identity Service:Registrar:LS2013CU2LBRPool.contoso.com/LBRouting -Priority 3 -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

Après avoir utilisé cette applet de demande, redémarrez tous les serveurs frontaux dans le pool ou les serveurs Standard Edition sur lesquels l’application de conférence de routage Location-Based est activée.

<div>


> [!IMPORTANT]  
> Location-Based le routage des mises en œuvre vers des conférences ou des transferts de consultation ne seront pas appliqués tant que tous les serveurs frontaux dans les pools applicables ou les serveurs Standard Edition n’ont pas été redémarrés.



</div>

Lorsque l’application de conférence de routage de Location-Based est activée et que tous les serveurs Lync en vigueur ont été redémarrés, toutes les conférences organisées par les utilisateurs de Lync activées pour le routage Location-Based seront surveillées de façon à éviter le contournement du numéro RTC

</div>

</div>

<span> </span>

</div>

</div>

</div>

