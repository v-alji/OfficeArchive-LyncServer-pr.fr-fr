---
title: Valider la réplication des paramètres de configuration
description: Valider la réplication des paramètres de configuration
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Validate replication of configuration settings
ms:assetid: 81a3c21d-b28a-4287-adac-11791e8db56d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205042(v=OCS.15)
ms:contentKeyID: 48184663
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26d8e9326da8b865f4e2ca3181975fb899300636
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446534"
---
# <a name="validate-replication-of-configuration-settings"></a>Valider la réplication des paramètres de configuration

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-19_

Vous pouvez valider la réplication des informations de configuration sur le serveur Edge en exécutant l’applet de contrôle Lync Server 2013 **Get-CsManagementStoreReplicationStatus** sur l’ordinateur interne sur lequel se trouve la Banque centrale de gestion ou n’importe quel ordinateur appartenant à un domaine sur lequel les composants principaux de Lync Server 2013 sont installés.

Les résultats initiaux risquent d’indiquer l’état « false » au lieu de « true » pour la réplication. Si tel est le cas, exécutez l’applet de connexion **Invoke-CsManagementStoreReplication** et attendez la fin de la réplication avant d’exécuter de nouveau l’applet de connexion **Get-CsManagementStoreReplicationStatus** .

</div>

<span> </span>

</div>

</div>

</div>

