---
title: 'Lync Server 2013 : meilleures pratiques pour votre infrastructure principale'
description: 'Lync Server 2013 : meilleures pratiques pour votre infrastructure de base.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for your core infrastructure in Lync Server 2013
ms:assetid: 44aff88d-536c-4613-a81e-5398c9c6a648
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518328(v=OCS.15)
ms:contentKeyID: 61071242
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0ea7cb9c7685a3b6f7c04146ec5631bbac10fe6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436040"
---
# <a name="best-practices-for-your-core-infrastructure-in-lync-server-2013"></a>Recommandations en matière d’infrastructure de base dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2014-01-27_

Vous avez probablement déjà pris des mesures pour intégrer la tolérance de pannes dans votre système, en utilisant des pratiques telles que la garantie de la redondance matérielle, la prévention de la perte d'alimentation, l'installation régulière des mises à jour, l'établissement des mesures de sécurité antivirus et la surveillance de l'activité du serveur. Ces pratiques profitent non seulement de votre infrastructure Microsoft Lync Server 2013, mais aussi de votre réseau entier. Si vous n’avez pas implémenté ces pratiques, nous vous conseillons de le faire avant de déployer Lync Server 2013.

Pour vous aider à protéger les serveurs dans votre déploiement de Lync Server 2013 contre les dommages accidentels ou intentionnelles susceptibles d’entraîner un temps d’arrêt, prenez les précautions suivantes :

  - Maintenez vos serveurs à jour avec les mises à jour de sécurité. En vous abonnant au service de notification de sécurité de Microsoft, vous recevez la notification immédiate des bulletins de sécurité pour les produits Microsoft. Pour vous abonner, accédez au site Web Microsoft Technical Security notifications à l’adresse [https://go.microsoft.com/fwlink/p/?LinkId=145202](https://go.microsoft.com/fwlink/p/?linkid=145202) .

  - Assurez-vous que les droits d'accès sont configurés correctement.

  - Conservez vos serveurs dans un environnement physique qui empêche l'accès non autorisé. Assurez-vous que le logiciel antivirus adéquat est installé sur tous vos serveurs. Maintenez le logiciel à jour avec les derniers fichiers de signatures de virus. Utilisez la fonction de mise à jour automatique de votre application antivirus pour maintenir à jour les signatures de virus.

  - Nous vous recommandons de désactiver les services du système d’exploitation Windows Server qui ne sont pas nécessaires sur les ordinateurs sur lesquels vous installez Lync Server 2013.

  - Chiffrez les systèmes d'exploitation et les lecteurs de disques où les données sont stockées à l'aide d'un système de chiffrement de volume complet, sauf si vous pouvez garantir un contrôle constant et total des serveurs, l'isolement physique complet et la désaffectation adéquate et sûre des disques remplacés ou défaillants.

  - Désactivez tous les ports DMA (Direct Memory Access) externes du serveur, sauf si vous pouvez garantir un contrôle très strict de l'accès physique aux serveurs. Les attaques basées sur DMA, qui peuvent être lancées assez facilement, risquent d'exposer des informations très sensibles, telles que les clés de chiffrement privées.

</div>

<span> </span>

</div>

</div>

</div>

