---
title: 'Lync Server 2013 : configuration requise pour le routage Location-Based pour les conférences'
description: 'Lync Server 2013 : configuration requise pour le routage Location-Based pour les conférences.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Requirements for Location-Based Routing for conferencing
ms:assetid: 766d9286-2c34-4faf-bb3e-f0ca478a70cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362806(v=OCS.15)
ms:contentKeyID: 56335085
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbaa1af2690c3148d2ecfb173b13be288a21d80f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442662"
---
# <a name="requirements-for-location-based-routing-for-conferencing-in-lync-server-2013"></a>Configuration requise pour le routage de Location-Based pour les conférences dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-07-19_

Voici les exigences requises pour l’installation et la configuration de l’application de conférence de routage Location-Based :

  - La mise à jour cumulative 2 Lync Server 2013 doit être déployée sur tous les serveurs ou pools de votre topologie.

<div>


> [!NOTE]  
> Si une mise à jour cumulative 2 ou une version ultérieure de Lync Server 2013 n’est pas installée sur un serveur ou un pool Lync dans votre topologie, il est possible de garantir le routage Location-Based de routage des réunions Lync.



</div>

  - Lync Server 2013 Location-Based le routage est une configuration requise pour Location-Based application de conférence de routage. Pour plus d’informations sur la configuration du routage de Lync Server 2013 Location-Based, voir [configuration du routage Location-Based](lync-server-2013-configuring-location-based-routing.md).

  - La configuration requise pour l’application conférences de routage Location-Based est la même que celle de Lync Server 2013 Location-Based routage. Pour plus d’informations, consultez [planification du routage Location-Based](lync-server-2013-planning-for-location-based-routing.md).

<div>

## <a name="supported-servers"></a>Serveurs pris en charge

L’application de conférence de routage de Location-Based nécessite que Lync Server 2013 cumulative Update 2 soit déployé sur tous les pools Front-End et les serveurs Standard Edition dans votre topologie. Si la mise à jour cumulative 2 de Lync Server 2013 n’est pas installée sur certains serveurs Lync dans votre topologie, Location-Based restrictions de routage ne peuvent pas être appliquées entièrement lors de réunions Lync et de transferts d’appels.

Le tableau suivant identifie la combinaison de rôles et de versions de serveur prenant en charge le routage Location-Based.


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Version de pool frontal</p></td>
<td><p>Version de serveur de médiation</p></td>
<td><p>Pris en charge</p></td>
</tr>
<tr class="even">
<td><p>Mise à jour cumulative 2 de Lync Server 2013</p></td>
<td><p>Mise à jour cumulative 2 de Lync Server 2013</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p>Mise à jour cumulative 2 de Lync Server 2013</p></td>
<td><p>Mise à jour cumulative 1 de Lync Server 2013</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Mise à jour cumulative 2 de Lync Server 2013</p></td>
<td><p>Lync Server 2010</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Mise à jour cumulative 2 de Lync Server 2013</p></td>
<td><p>Office Communications Server 2007 R2</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Mise à jour cumulative 1 de Lync Server 2013</p></td>
<td><p>Indifférente</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Lync Server 2010</p></td>
<td><p>Indifférente</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Office Communications Server 2007 R2</p></td>
<td><p>Indifférente</p></td>
<td><p>Non</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supported-clients"></a>Clients pris en charge

Les clients Lync qui prennent en charge Location-Based le routage des réunions Lync sont les mêmes que ceux prenant en charge le routage Location-Based serveur 2013. Pour plus d’informations, reportez-vous à la [prise en charge du routage Location-Based pour le client et le serveur](lync-server-2013-client-and-server-support-for-location-based-routing.md).

</div>

<div>

## <a name="mediation-server-requirements-for-consultative-call-transfers"></a>Configuration requise pour le serveur de médiation pour les transferts d’appels

L’application de conférence de routage de Location-Based nécessite le déploiement de serveurs de médiation autonomes pour appliquer des restrictions de routage Location-Based sur les transferts d’appel.

Pour faire en sorte qu’il soit nécessaire de mettre en place Location-Based le routage des transferts d’appel, le serveur de médiation doit être associé à un seul homologue du serveur de médiation (PBX, passerelle SIP, etc.) dans les régions réseau où Location-Based routage est requis. Si d’autres homologues du serveur de médiation sont déployés dans la même région réseau, l’homologue du serveur de médiation doit être associé à un serveur de médiation différent. Cette obligation est détaillée comme suit :

  - Serveur de médiation unique par plusieurs homologues du serveur de médiation lorsque le transfert d’appel d’un service de médiation est acheminé vers un serveur de médiation par le biais d’un serveur de médiation configuré avec plusieurs Trunks SIP (par exemple, PBX et passerelles), le transfert d’appel consultatif est bloqué en cas d’annulation du transfert d’appel sur des ISL SIP.
    
    Par exemple, dans le cas d’un serveur de médiation unique qui dessert un homologue du serveur de médiation de la passerelle RTC et un homologue du serveur de médiation PBX, le comportement suivant est observé :
    
      - Lorsqu’un utilisateur Lync à partir d’un site donné (par exemple, le site 1) tente de transférer un appel avec un point de terminaison RTC à un utilisateur Lync à partir d’un site différent (par exemple, site 2) par le biais du transfert de consultation, l’appel n’est pas autorisé à éviter le contournement du numéro RTC.
    
      - Lorsqu’un utilisateur de Lync à partir d’un site donné (par exemple, le site 1) tente de transférer un appel avec un point de terminaison PBX dans le même site (site 1) pour un utilisateur Lync à partir d’un autre site (par exemple, site 2) via le transfert de consultation, l’appel n’est pas autorisé, même s’il n’est pas en contournement potentiel de péage

  - Séparation des serveurs de médiation par le pair du serveur de médiation
    
    Lorsque le transfert consultatif est ciblé auprès d’un homologue de serveur de médiation, le transfert de la consultation est évalué par rapport à l’homologue du serveur de médiation unique desservi par le serveur de médiation. L’appel sera interdit ou autorisé en fonction de son potentiel dans le cadre du contournement du numéro RTC, quels que soient les autres homologues du site dans le cadre de leur service par des serveurs de médiation distincts.
    
    Par exemple, dans le cas d’un serveur de médiation distinct prenant en service un homologue de serveur de médiation de passerelle RTC et un homologue de serveur de médiation PBX, le comportement suivant est observé :
    
      - Lorsqu’un utilisateur Lync à partir d’un site donné (par exemple, le site 1) tente de transférer un appel avec un point de terminaison RTC à un utilisateur Lync à partir d’un site différent (par exemple, site 2) par le biais du transfert de consultation, l’appel n’est pas autorisé à éviter le contournement du numéro RTC.
    
      - Lorsqu’un utilisateur Lync à partir d’un site donné (par exemple, le site 1) tente de transférer un appel avec un point de terminaison PBX au sein d’un même site (site 1) pour un utilisateur Lync à partir d’un site différent (par exemple, site 2) par le biais d’un transfert de consultation, l’appel n’est pas soumis à un problème de péage RTC potentiel.

</div>

<div>

## <a name="capabilities-not-supported-by-the-location-based-routing-conferencing-application"></a>Fonctionnalités non prises en charge par l’application de conférence de routage Location-Based

Les fonctionnalités suivantes ne sont pas prises en charge par l’application de conférence de routage Location-Based :

  - Conférence rendez-vous. Location-Based routage ne peut pas être appliqué pour la Conférence rendez-vous. Toute demande d’accès à une conférence donnée n’est pas limitée par Location-Based routage, même si l’organisateur de la Conférence est un utilisateur de Lync activé pour le routage Location-Based.

  - Nous vous conseillons de ne pas mettre en place des numéros d’accès aux conférences dans les régions où Location-Based restrictions de routage doivent être appliquées.

</div>

</div>

<span> </span>

</div>

</div>

</div>

