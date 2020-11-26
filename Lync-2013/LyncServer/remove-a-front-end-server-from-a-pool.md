---
title: Supprimer un serveur frontal d’un pool
description: Supprimer un serveur frontal d’un pool.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove a Front End Server from a pool
ms:assetid: 767225c9-7c0b-4d54-a407-d77134ba2abe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688095(v=OCS.15)
ms:contentKeyID: 49733694
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45560a6f43288b47c0f85f880a190e31f2c8c04d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440324"
---
# <a name="remove-a-front-end-server-from-a-pool"></a>Supprimer un serveur frontal d’un pool

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-04_

Le serveur principal Microsoft Lync Server 2010 Enterprise Edition ne peut pas exister en tant qu’ordinateur autonome. Elle doit être définie en tant que pool frontal, même s’il n’y a qu’un seul ordinateur dans le pool.

Cette rubrique vous guide tout au long du processus de suppression d’un serveur frontal individuel d’un pool frontal existant. Si le serveur frontal est le dernier serveur du pool ou si vous supprimez entièrement le pool, voir supprimer le [pool frontal ou le serveur Standard Edition Server](remove-front-end-pool-or-standard-edition-server.md). Il n’est pas nécessaire de supprimer les serveurs front-end individuels avant de supprimer le pool frontal. Lorsque vous supprimez le pool, vous supprimez chaque serveur frontal.

<div>

## <a name="to-remove-a-front-end-server-from-a-pool"></a>Pour supprimer un serveur frontal d’un pool

1.  Ouvrez le serveur frontal Lync Server 2013, ouvrez le générateur de topologie.

2.  Accédez au nœud Lync Server 2010.

3.  Développez **Pools front-end Enterprise Edition**, développez le pool frontal du serveur frontal que vous voulez supprimer, cliquez avec le bouton droit sur le serveur frontal que vous voulez supprimer, puis cliquez sur **supprimer**.

</div>

</div>

<span> </span>

</div>

</div>

</div>

