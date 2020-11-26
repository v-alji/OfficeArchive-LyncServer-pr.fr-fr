---
title: 'Lync Server 2013 : configuration d’un service de mobilité pour des performances élevées'
description: 'Lync Server 2013 : configuration d’un service de mobilité pour des performances optimales.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Mobility Service for high performance
ms:assetid: c2b8aadb-cffb-49f0-ba7a-e8541a1ff475
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690042(v=OCS.15)
ms:contentKeyID: 48185332
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4732d9f6a92c383a105a6f0d7162c9b6c798de24
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432883"
---
# <a name="configuring-mobility-service-for-high-performance-in-lync-server-2013"></a>Configuration d’un service de mobilité pour des performances élevées dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-17_

<div>


> [!IMPORTANT]  
> Cette rubrique s’applique uniquement au service de mobilité Lync Server 2013 (MCX) et ne s’applique pas à l’API Unified Communications Web API (UCWA), comme il est fourni dans les mises à jour cumulatives de Lync Server 2013:2013 février.



</div>

Lorsque vous installez le service de mobilité (MCX) sur Internet Information Services (IIS) 7,5, le programme d’installation de service de mobilité configure certains paramètres de performance sur le serveur frontal. Nous vous recommandons d’utiliser les services Internet (IIS) 7.5 pour la mobilité. Ceux-ci affectent la quantité maximale de demandes utilisateur simultanées et la quantité maximale de threads autorisés pour le service de mobilité.

Voici les paramètres de performances :

<div>

## <a name="settings-for-mcx-on-iis-75"></a>Paramètres pour Mcx sur IIS 7.5

1.  **maxConcurrentThreadsPerCPU** est fixé sur zéro (0).

2.  **maxConcurrentRequestsPerCPU** est fixé sur zéro (0).

3.  Le modèle de processus ASP.NET est AutoConfig (pour les services Internet (IIS) 7.5 uniquement).

4.  La limite de file d’attente HTTP.sys a la valeur 1 000 (par défaut).

</div>

</div>

<span> </span>

</div>

</div>

</div>

