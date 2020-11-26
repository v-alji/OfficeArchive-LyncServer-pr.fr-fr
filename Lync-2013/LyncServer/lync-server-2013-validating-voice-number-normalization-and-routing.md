---
title: 'Lync Server 2013 : validation de la normalisation et du routage des numéros vocaux'
description: 'Lync Server 2013 : validation de la normalisation et du routage des numéros vocaux.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating voice number normalization and routing
ms:assetid: a6a825c7-6928-4e80-b7e9-803b7f7ebd13
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720922(v=OCS.15)
ms:contentKeyID: 63969633
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5f28f679cbb991bdb90362eb61c9c7b68879791e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438623"
---
# <a name="validating-voice-number-normalization-and-routing-in-lync-server-2013"></a>Validation de la normalisation et du routage des numéros vocaux dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2014-05-19_

Le bon fonctionnement de la normalisation et du routage des numéros est essentiel pour l’environnement d’entreprise voix. En particulier lors des migrations du système PBX vers un environnement Lync Server autonome, l’une des clés de la migration réussie consiste à afficher et à documenter toutes les règles de numérotation existantes, et à créer des règles de normalisation appropriées, des politiques vocales, des utilisations de téléphone et des itinéraires.

La validation de la normalisation et de l’acheminement des numéros est important non seulement pendant les migrations, mais également dans le cadre du fonctionnement normal et stable du système.

Nous vous recommandons d’effectuer cette validation quotidiennement en utilisant le panneau de configuration de Lync Server, en commençant par le développement d’un ensemble de scénarios de test puissants par rapport à l’ensemble actuel de règles de normalisation publiées dans les paramètres globaux de Lync Server. Ces cas de test doivent être exécutés quotidiennement pour mettre en évidence les modifications indésirables apportées et validées au plan de numérotation.

Le panneau de configuration de Lync Server vous permet également de visualiser, de tester, de modifier, d’archiver et de partager des informations de configuration sur le routage de la voix et de modifier les règles de normalisation des numéros vocaux d’entreprise, les plans de numérotation, la politique vocale et les itinéraires. Les fonctionnalités suivantes sont disponibles pour effectuer les opérations suivantes :

  - Exportation et importation ou sauvegarde de données de routage de la voix entre systèmes ;

  - Test de la configuration avant de les télécharger sur un système en direct.

  - Création et exécution de cas de test de configuration pour garantir la facilité d’utilisation du routage des données après avoir apporté des modifications à celui-ci, mais avant de les valider.

  - La création et la modification des règles de normalisation des numéros, des profils d’emplacement, de la stratégie vocale et des données de routage sans écrire les expressions régulières nécessaires.

  - Analyse d’un profil d’emplacement à des fins de compatibilité avec Lync Server Phone Edition.

  - Vous trouverez des informations supplémentaires sur les tests de routage [de voix dans la boîte de test routage de la voix dans Lync Server 2013](lync-server-2013-test-voice-routing.md)

<div>

## <a name="see-also"></a>Voir aussi


[Test du routage des communications vocales dans Lync Server 2013](lync-server-2013-test-voice-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

