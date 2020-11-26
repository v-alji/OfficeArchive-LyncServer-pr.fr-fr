---
title: 'Lync Server 2013 : Choix des modalités de déploiement de Microsoft Lync'
description: 'Lync Server 2013 : choix du déploiement de Microsoft Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deciding how to deploy Microsoft Lync
ms:assetid: 6ca677d3-745d-4935-8f05-19274a8bccf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204979(v=OCS.15)
ms:contentKeyID: 48184423
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a800b51dfddc6f2c99e42c8f117056ed4091b6a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431231"
---
# <a name="deciding-how-to-deploy-lync-server-2013"></a>Choix des modalités de déploiement de Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-03_

Lors de la planification de Lync, la première décision majeure consiste à déployer Microsoft Lync : comme Lync Server 2013 en local, ou Lync Online avec Microsoft 365 ou Office 365 dans le Cloud.

  - **Lync Server 2013 local** : ce choix fournit l’ensemble des fonctionnalités Lync complètes et offre une souplesse de configuration, de personnalisation et d’utilisation de votre déploiement. Tous les serveurs sont installés sur site et gérés par votre organisation. Un déploiement local fournit une gamme complète de fonctionnalités de serveur Lync.

  - **Lync Online dans le Cloud** Lync Online est conçu pour les organisations qui souhaitent bénéficier de coûts et de compétences en matière de messagerie instantanée, de présence et de réunions dans le Cloud sans sacrifier les fonctionnalités de niveau professionnel de Lync Server. Avec Lync Online, Microsoft déploie et met à jour l’infrastructure de serveur requise, ainsi que les mises à jour, les correctifs et les mises à niveau en continu. Certaines fonctionnalités disponibles dans un déploiement local ne sont pas disponibles dans Lync Online.

Le type de déploiement le plus approprié dépend des charges de travail que vous voulez déployer et du statut géographique et commercial de votre organisation.

<div>

## <a name="lync-server"></a>Lync Server

Le déploiement de Lync Server local est préférable pour les scénarios suivants :

  - **Fonctionnalités voix entreprise complètes**   Si vous envisagez de déployer une solution voix entreprise complète pour remplacer votre PBX ou utiliser des fonctionnalités d’appel avancées, un déploiement Lync Server local est requis. Locale prend en charge la connectivité directe avec les systèmes et les Trunks PBX, ainsi que les fonctionnalités de téléphone avancées telles que les Response Groups et le parc d’appels. Pour le moment, Lync Online ne prend pas en charge ces fonctionnalités.

  - **Contrôles de qualité multimédia**   Si vous souhaitez bénéficier de toutes les fonctionnalités d’assurance qualité multimédia, telles que les fonctionnalités de contrôle d’admission des appels (CAC) et de qualité de service (QoS), vous devez disposer d’un déploiement local.

  - **Conversation permanente**   Si vous devez déployer une conversation permanente pour votre organisation, vous devez choisir un déploiement local.

  - **applications serveur tierces**   Seuls les déploiements locaux peuvent fonctionner avec des applications tierces approuvées qui utilisent l’API Microsoft Unified Communications Managed API (UCMA).

  - La **prise en charge de l’assistance régionale est une entreprise multi-nationale/régionale** .   Si vous disposez de centres de donnees dans plusieurs pays ou régions et que vous avez besoin de déployer et de gérer des serveurs sur une base régionale, il est préférable d’utiliser un déploiement local, dans la mesure où il fournit ce type de fonctionnalité de gestion régionale.

  - **Contrôle total des stratégies, des rapports et des mises à niveau**   Le déploiement de Lync Server sur site vous permet d’accéder à l’ensemble des stratégies du serveur et du client, de la surveillance ainsi que d’autres rapports et de la synchronisation des mises à niveau. Lync Online fournit un sous-ensemble du paramètre de stratégie et des rapports, et fournit une fenêtre limitée, même importante, pour accepter les mises à niveau.

</div>

<div>

## <a name="lync-online"></a>Lync Online

Si aucun des facteurs de la liste précédente n’est essentiel pour vous, vous pouvez choisir Lync Online pour faciliter le déploiement et la gestion. Lync Online fournit un ensemble de fonctionnalités de messagerie instantanée, de présence et de conférence puissantes, ainsi que des appels audio et vidéo sur IP entre les utilisateurs de votre organisation.

</div>

</div>

<span> </span>

</div>

</div>

</div>
