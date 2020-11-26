---
title: Vérifier que la réplication utilisateur est terminée
description: Vérifiez que la réplication des utilisateurs est terminée.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify user replication has completed
ms:assetid: 119e9896-45e5-4f8b-af43-7b09360ada0b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204680(v=OCS.15)
ms:contentKeyID: 48183441
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 60bca44fcce811c29b1633bd4d3a39f832851885
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446071"
---
# <a name="verify-user-replication-has-completed"></a>Vérifier que la réplication utilisateur est terminée

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-09-17_

Lorsque vous exécutez l’applet de contrôle **Move-Csuser** , il est possible que vous constatiez un échec en raison du fait que les informations utilisateur entre les services de domaine Active Directory (AD DS) et celles de Lync Server 2013 ne sont pas synchronisées, car la réplication initiale est incomplète. Le temps nécessaire à la réussite de la synchronisation initiale du service Réplicateur d’utilisateurs de Lync Server 2013 dépend du nombre de contrôleurs de domaine hébergés dans la forêt Active Directory qui héberge le pool 2013 Server. Le processus de synchronisation initiale du service Réplicateur d’utilisateurs de Lync Server 2013 se produit lorsque le serveur frontal de Lync Server 2013 est démarré pour la première fois. Après cela, la synchronisation est alors basée sur l’intervalle du réplicateur d’utilisateurs. Suivez les étapes ci-dessous pour vérifier que la réplication des utilisateurs a abouti avant d’exécuter l’applet **de commande Move-Csuser** .

<div>

## <a name="to-verify-user-replication-has-completed"></a>Pour vérifier la fin de la réplication des utilisateurs

1.  Ouvrez une session sur l’ordinateur sur lequel le générateur de topologie est installé en tant que membre du groupe administrateurs de domaine et du groupe RTCUniversalServerAdmins.

2.  Cliquez sur le menu **Démarrer** , puis sur **exécuter**.

3.  Entrez **eventvwr.exe** puis cliquez sur **OK**.

4.  Dans l’observateur d’événements, cliquez sur **journaux des applications et des services** pour le développer, puis sélectionnez Lync Server.

5.  Dans le volet **actions** , cliquez sur **filtrer le journal actuel**.

6.  Dans la liste **sources d’événements** , cliquez sur réplicateur d' **utilisateurs LS**.

7.  Dans **\<All Event IDs\>** entrer **30024** , puis cliquez sur **OK**.

8.  Dans la liste des événements filtrés, sous l’onglet **général** , recherchez une entrée qui indique que la réplication des utilisateurs s’est déroulée correctement.

</div>

</div>

<span> </span>

</div>

</div>

</div>

