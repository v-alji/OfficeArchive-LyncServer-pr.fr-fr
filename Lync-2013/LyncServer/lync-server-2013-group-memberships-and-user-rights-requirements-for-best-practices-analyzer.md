---
title: Exigences en matière d’appartenance aux groupes et de droits d’utilisateur pour les meilleures pratiques Analyzer
description: Exigences en matière d’appartenance aux groupes et de droits d’utilisateur pour l’analyseur de meilleures pratiques.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group memberships and user rights requirements for Best Practices Analyzer
ms:assetid: f812e343-8f75-454e-b7a8-1b404e32071a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg591354(v=OCS.15)
ms:contentKeyID: 48185869
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 64a7d785a77701c6796488178a7cce10caf54f42
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427823"
---
# <a name="group-memberships-and-user-rights-requirements-for-best-practices-analyzer-in-lync-server-2013"></a>Exigences en matière d’appartenance aux groupes et de droits d’utilisateur pour les meilleurs analyseurs dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-21_

Pour exécuter correctement le BPA, le compte d’utilisateur que vous utilisez pour vous connecter doit être membre du groupe Administrateurs sur l’ordinateur local. De plus, pour analyser votre environnement, le compte d’utilisateur doit être membre des groupes suivants :

  - **Administrateurs de domaine**   Pour énumérer les informations sur les services de domaine Active Directory et appeler les fournisseurs WMI sur les contrôleurs de domaine et les serveurs de catalogue global.

  - **Administrateurs**   Requis sur chaque ordinateur interne Lync Server 2013 et chaque serveur Edge pour appeler les fournisseurs WMI (Windows Management Instrumentation) et accéder au registre.

  - **RTCUniversalReadOnlyAdmins**   Droits d’administration complets en lecture seule de Lync Server 2013.

  - **Administrateur Exchange-Affichage seul**   Administrateur Exchange Affichage seul ou entièrement délégué dans l’organisation Microsoft Exchange.

Si votre compte d’utilisateur ne dispose pas des droits d’utilisateur suffisants, vous avez deux possibilités :

  - À l’invite de commandes, utilisez la commande **runas** pour exécuter l’outil sous un compte disposant de droits d’utilisateur suffisants. La syntaxe est la suivante :
    
        runas /netonly /user:<domain>\<userName> rtcbpa.exe

  - Dans la page **se connecter à Active Directory** , définissez les informations d’identification des comptes que vous envisagez d’utiliser pour exécuter les meilleurs analyseurs. Cliquez sur **afficher les options de connexion avancées**. Vous pouvez entrer trois comptes : un pour la connexion aux services de domaine Active Directory (AD FS), un pour la connexion aux serveurs Edge Lync Server 2013 et un pour la connexion aux serveurs Exchange. Si vous ne spécifiez aucun de ces comptes, le compte d’utilisateur que vous avez utilisé pour vous connecter et exécuter l’analyseur de meilleures pratiques est utilisé.

</div>

<span> </span>

</div>

</div>

</div>

