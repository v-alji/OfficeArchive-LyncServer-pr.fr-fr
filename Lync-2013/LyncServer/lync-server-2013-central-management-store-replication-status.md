---
title: 'Skype Entreprise Server 2015 : statut de réplication du magasin central de gestion'
description: 'Lync Server 2013 : état de réplication du magasin de gestion central.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Central management store replication status
ms:assetid: f514f88d-986b-4e45-b79b-e04a7616c1fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720926(v=OCS.15)
ms:contentKeyID: 63969663
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5f1f9008a966040cf34ac0499c023f9dbe53a541
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435459"
---
# <a name="central-management-store-replication-status-in-lync-server-2013"></a>Statut de réplication du magasin central de gestion dans Skype Entreprise Server 2015

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2015-01-26_

Lorsqu’un administrateur apporte une modification d’une sorte à Lync Server (par exemple, lorsqu’un administrateur crée une nouvelle stratégie vocale ou change les paramètres de configuration du serveur du carnet d’adresses), cette modification est enregistrée dans le magasin central de gestion. À son tour, la modification doit alors être répliquée sur tous les ordinateurs qui exécutent des services ou rôles de serveur Lync Server.

Pour répliquer des données, le réplicateur principal (exécuté sur le serveur central de gestion) crée un instantané des données de configuration modifiées. Une copie de cette capture d’image est alors envoyée à chaque ordinateur exécutant Lync Server services ou rôles de serveur. Sur ces ordinateurs, un agent de réplication reçoit l’instantané et transfère les données modifiées. L’agent envoie ensuite au réplicateur principal un message signalant le dernier statut de réplication.

L’applet de connexion Get-CsManagementStoreReplicationStatus permet de vérifier l’état de réplication de tout ou partie des ordinateurs serveur Lync au sein de votre organisation.

Qui peut exécuter cette applet de commande ? Par défaut, les membres des groupes ci-dessous ont l’autorisation d’exécuter localement l’applet de commande Get-CsManagementStoreReplicationStatus : RTCUniversalUserAdmins, RTCUniversalServerAdmins.

Pour renvoyer la liste de tous les rôles RBAC attribués à cette applet de commande (y compris les rôles RBAC personnalisés que vous avez créés vous-même), exécutez la commande suivante à partir de l’invite Windows PowerShell :

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsManagementStoreReplicationStatus"}

<div>

## <a name="see-also"></a>Voir aussi


[Get-CsManagementStoreReplicationStatus](https://docs.microsoft.com/powershell/module/skype/Get-CsManagementStoreReplicationStatus)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

