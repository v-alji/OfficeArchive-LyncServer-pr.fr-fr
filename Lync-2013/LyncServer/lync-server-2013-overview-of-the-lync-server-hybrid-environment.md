---
title: 'Lync Server 2013 : vue d’ensemble de l’environnement Lync Server hybride'
description: 'Lync Server 2013 : vue d’ensemble de l’environnement Lync Server hybride.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of the Lync Server 2013 hybrid environment
ms:assetid: 0d16ec3a-28f0-4483-96e7-8e68f30398fa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204669(v=OCS.15)
ms:contentKeyID: 48183399
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 95b0ae433dafad349d7ef9b6328e43dbc308579c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445042"
---
# <a name="overview-of-the-lync-server-2013-hybrid-environment"></a>Vue d’ensemble de l’environnement hybride Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2014-05-28_

L’environnement hybride Lync Server 2013 fait référence à un déploiement dans lequel certains utilisateurs sont hébergés sur le serveur Lync Server 2013 local et d’autres utilisateurs hébergés sur Lync Online, mais les utilisateurs partagent le même domaine, tel que user@contoso.com.

<div>

## <a name="about-this-guide"></a>À propos de ce guide

Ce guide décrit les tâches nécessaires à la configuration de votre environnement Lync Server 2013 pour l’interopérabilité avec Lync Online, et la migration des utilisateurs de votre déploiement local vers Lync Online.

</div>

<div>

## <a name="prerequisites"></a>Conditions préalables

Pour effectuer les tâches de configuration d’un déploiement pour la configuration hybride, vous devez avoir installé les applications et utilitaires suivants. Les programmes d’installation de ces fichiers sont inclus sur le support d’installation fourni pour votre déploiement, ainsi que sur les liens inclus dans la liste suivante.

  - [Services AD FS (Active Directory Federation Services) 2,0](https://go.microsoft.com/fwlink/p/?linkid=257305)

  - [Outil de synchronisation d’annuaires 9,1](https://go.microsoft.com/fwlink/p/?linkid=257307)

  - [Installer Windows PowerShell pour l’authentification unique avec AD FS](https://go.microsoft.com/fwlink/p/?linkid=398710)

  - L’Assistant de connexion de Microsoft Online Services (msoidcli-7.0.msi) est inclus dans la configuration du Bureau pour Microsoft 365, qui peut être obtenue à partir de la page téléchargements liée à partir du centre d’administration Microsoft 365.

</div>

<div>

## <a name="administrator-credentials"></a>Informations d’identification d’administrateur

Lorsque vous êtes invité à fournir vos informations d’identification d’administrateur, utilisez le nom d’utilisateur et le mot de passe du compte d’administrateur de votre organisation Microsoft 365 ou Office 365. Vous pouvez également utiliser ces informations d’identification lorsque vous configurez les services AD FS (Active Directory Federation Services) 2,0, la synchronisation d’annuaires, l’authentification unique, la Fédération et le déplacement des utilisateurs vers Lync Online.

</div>

<div>

## <a name="connecting-to-lync-online-powershell"></a>Connexion à Lync Online PowerShell

Les administrateurs ont désormais la possibilité d’utiliser Windows PowerShell pour gérer Lync Online et leurs comptes d’utilisateurs Lync Online. Pour cela, vous devez d’abord télécharger et installer le module Lync Online Connector à partir du centre de téléchargement Microsoft ( https://go.microsoft.com/fwlink/?LinkId=294688) . Pour plus d’informations sur le téléchargement, l’installation et l’utilisation du module Lync Online Connector et pour obtenir des informations détaillées sur l’utilisation de Windows PowerShell pour gérer Lync Online, voir [utilisation de Windows PowerShell pour gérer Lync Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).

</div>

</div>

<span> </span>

</div>

</div>

</div>

