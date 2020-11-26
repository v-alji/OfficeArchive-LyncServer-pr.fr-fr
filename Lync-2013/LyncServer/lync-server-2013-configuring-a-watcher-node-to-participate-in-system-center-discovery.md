---
title: Configuration d’un nœud FileSystemWatcher pour participer à la découverte de System Center
description: Configuration d’un nœud FileSystemWatcher pour participer à la découverte de System Center.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a watcher node to participate in System Center discovery
ms:assetid: 15c5dcfd-603b-47ea-af1b-8714c2ec08af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204704(v=OCS.15)
ms:contentKeyID: 48183500
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d6a42ae77e0c8bde8b8e4de4461180ad00380a5d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433467"
---
# <a name="configuring-a-watcher-node-in-lync-server-2013-to-participate-in-system-center-discovery"></a>Configuration d’un nœud FileSystemWatcher dans Lync Server 2013 pour participer à la découverte de System Center

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-22_

Pour vous assurer que votre nœud FileSystemWatcher participe au processus de découverte de System Center Operations Manager, vous devez effectuer la procédure suivante sur un ordinateur sur lequel la console System Center Operations Manager a été installée :

1.  Dans l’onglet **administration** , cliquez sur **géré par l’agent**.

2.  Cliquez avec le bouton droit sur le nom de l’ordinateur du nœud d’observation, puis cliquez sur **Propriétés**. Dans la boîte de dialogue **Propriétés** , sous l’onglet **sécurité** , sélectionnez **Autoriser cet agent à agir en tant que proxy et détecter les objets gérés sur d’autres ordinateurs**, puis cliquez sur **OK**.

Après avoir configuré le nœud FileSystemWatcher pour qu’il serve de proxy, redémarrez l’ordinateur de nœud d’observation. Après le redémarrage de l’ordinateur, vérifiez qu’aucun événement d’erreur n’est enregistré dans le journal des événements Operations Manager sur cet ordinateur. Une fois que l’ordinateur est en cours d’exécution pendant 15 minutes, utilisez la console Operations Manager pour vérifier que votre ordinateur serveur Lync figure dans la catégorie **Lync** .

</div>

<span> </span>

</div>

</div>

</div>

