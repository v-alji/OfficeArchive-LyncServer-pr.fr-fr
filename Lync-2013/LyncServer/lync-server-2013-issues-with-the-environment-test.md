---
title: 'Lync Server 2013 : problèmes liés au test de l’environnement'
description: 'Lync Server 2013 : problèmes liés au test de l’environnement.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Issues with the environment test
ms:assetid: ff1fe0d3-35b2-41ef-87e7-6a61e9e1d2ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205421(v=OCS.15)
ms:contentKeyID: 48185970
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 551d7e914480e178e0558c1d17eefcf060c0688e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426717"
---
# <a name="issues-with-the-environment-test-in-lync-server-2013"></a>Problèmes liés au test de l’environnement dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-09-21_

Le mode d’analyse des pratiques recommandées vous permet de vérifier que votre environnement Lync Server 2013 est une configuration prise en charge. Dans le cadre de la vérification des services de domaine Active Directory (AD FS), l’analyseur des recommandations est le suivant :

  - Vérifie la forêt et la préparation du schéma des services de domaine Active Directory.

  - Identifie le nombre de sites et de domaines services de domaine Active Directory du déploiement.

  - Vérifie les niveaux de forêt et de domaine.

  - Vérifie la version du contrôleur de domaine.

  - Identifie le contexte de nom de domaine, de configuration et de schéma.

  - Identifie le nombre d’utilisateurs activés.

  - Vérifie l’emplacement de stockage des paramètres globaux des services de domaine Active Directory.

  - Recherche les points de connexion de service de Lync Server.

  - Identifie la version de la base de données.

<div>

## <a name="resolving-issues-with-the-environment"></a>Résolution des problèmes liés à l’environnement

Si le test de l’environnement a détecté des problèmes avec votre environnement, il est probable que les problèmes liés à votre configuration Active Directory ou au niveau de logiciel exécuté sur des serveurs spécifiques apparaissent. Par exemple, si le service d’analyse des pratiques recommandées identifie tout contrôleur de domaine dans votre environnement exécutant Windows Server 2000, il émet un avertissement et vous devrez mettre à niveau ces contrôleurs de domaine vers une version prise en charge de Windows Server.

</div>

</div>

<span> </span>

</div>

</div>

</div>

