---
title: Migration de Lync Server 2010, conversation de groupe ou de la conversation de groupe Office Communications Server 2007 R2 vers Lync Server 2013, serveur de conversation permanente
description: Migration à partir de Lync Server 2010, d’une conversation de groupe ou d’une conversation de groupe Office Communications Server 2007 R2 vers Lync Server 2013, serveur de conversation permanente.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server
ms:assetid: 5b4d3db1-6eba-4932-b49c-f60bcf9488f9
ms:mtpsurl: https://technet.microsoft.com/library/Gg615442(v=OCS.15)
ms:contentKeyID: 48184240
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6090d5924a203a960444d9a10700fd178d038887
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446856"
---
# <a name="migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server"></a>Migration de Lync Server 2010, conversation de groupe ou de la conversation de groupe Office Communications Server 2007 R2 vers Lync Server 2013, serveur de conversation permanente

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-06_

Les rubriques de cette section vous guident tout au long du processus de migration de Lync Server 2010, d’une conversation de groupe ou d’une conversation de groupe Microsoft Office Communications Server 2007 R2 vers Lync Server 2013, serveur de chat permanent. Si vous envisagez d’utiliser Lync Server 2013, le déploiement permanent de Chat Server pour une coexistence avec un serveur Lync Server 2010, une conversation de groupe ou un déploiement d’Office Communications Server 2007 R2 en conversation de groupe, ce guide inclut également des informations essentielles pour l’utilisation de cet environnement mixte. Ce guide porte essentiellement sur la migration des données pour le serveur de chat permanent. Pour les utilisateurs migrant d’une version héritée de Lync Server vers Lync Server 2013, voir [migration de Lync server 2010 vers Lync server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) et [migration d’Office Communications Server 2007 R2 vers Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md).

<div>


> [!IMPORTANT]  
> Cette rubrique part du principe que vous avez déjà installé Lync Server 2013 dans la coexistence avec Lync Server 2010 ou Office Communications Server 2007 R2.



</div>

<div>


> [!IMPORTANT]  
> Ce guide décrit les étapes généralement requises pour effectuer chaque phase de migration. Elle ne traite pas chaque topologie de déploiement hérité possible ou chaque scénario de migration possible. Par conséquent, vous n’aurez peut-être pas besoin d’effectuer toutes les étapes décrites, ou vous devrez peut-être effectuer des étapes supplémentaires selon votre déploiement. Ce guide fournit également des exemples de procédure de vérification. Ces étapes de vérification sont fournies pour vous aider à comprendre ce que vous devez savoir pour vous assurer que chaque phase se termine correctement lors de la migration. Vous pouvez modifier ces étapes de vérification pour votre processus de migration spécifique.



</div>

Ce guide fournit des informations spécifiques à la mise à niveau de votre déploiement existant. Il n’explique pas comment modifier votre topologie existante. Ce guide ne traite pas de l’implémentation des nouvelles fonctionnalités. Lorsqu’une procédure détaillée est documentée à un autre emplacement, ce guide vous dirige vers la section document ou document appropriée.

Ce document définit les termes indiqués dans la liste suivante.

  - *vers*  
    Le déplacement de votre déploiement à partir d’une version précédente de chat permanent du serveur, auparavant appelé serveur de discussion de groupe, vers Lync Server 2013, serveur de chat permanent.

<!-- end list -->

  - *installation*  
    Installation d’une nouvelle version du logiciel sur un ordinateur client ou serveur.

<!-- end list -->

  - *coexistence*  
    L’environnement temporaire qui existe lors de la migration, lorsque certaines fonctionnalités ont été migrées vers Lync Server 2013, le serveur de conversations permanentes et d’autres fonctionnalités continuent de subsister sur une version antérieure du serveur de discussion de groupe.

Le serveur Chat permanent est une extension de l’infrastructure 2013 de Lync Server. En fonction de votre topologie, vous pouvez migrer Lync Server 2010, une conversation de groupe ou une conversation de groupe Office Communications Server 2007 R2 vers Lync Server 2013 permanent Chat Server. Pour plus d’informations sur les topologies disponibles et la configuration logicielle requise pour la migration du serveur de discussion de groupe, reportez-vous à la section [planification du serveur de chat permanent dans Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) dans la documentation de planification.

Si votre organisation nécessite une prise en charge de la conformité, celle-ci est désormais automatiquement installée sur chaque serveur de chat permanent. Un serveur distinct n’est plus nécessaire pour la conformité.

<div>


> [!IMPORTANT]  
> Le serveur de chat permanent doit être installé sur un système de fichiers NTFS pour garantir la sécurité du système de fichiers. FAT32 n’est pas un système de fichiers pris en charge pour le serveur de chat permanent.<BR>Si votre organisation nécessite une prise en charge de la conformité, celle-ci est désormais automatiquement installée sur chaque serveur de chat permanent. Un serveur distinct n’est plus nécessaire pour la conformité. Pour plus d’informations sur les modifications dans Lync Server 2013 &nbsp; persistent Chat Server, reportez-vous à la rubrique <A href="lync-server-2013-new-persistent-chat-server-features.md">nouvelles fonctionnalités du serveur de chat permanent de lync Server 2013</A> dans la documentation de mise en route.



</div>

<div>

## <a name="in-this-section"></a>Dans cette section

  - [Scénario de migration standard - Haut niveau](standard-migration-scenario-high-level.md)

  - [Processus de migration - Détails](migration-process-details.md)

  - [Remarques liées à la coexistence](coexistence-considerations.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

