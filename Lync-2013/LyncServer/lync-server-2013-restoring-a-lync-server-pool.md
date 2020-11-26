---
title: 'Lync Server 2013 : restauration d’un pool de serveurs Lync'
description: 'Lync Server 2013 : restauration d’un pool de serveurs Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a Lync Server pool
ms:assetid: 6fe80fb3-38ad-4931-a07b-1763b61aa448
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202176(v=OCS.15)
ms:contentKeyID: 51541488
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 02e92b4e7af9cf782d49c265425006e0118b9161
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442599"
---
# <a name="restoring-a-lync-server-pool-in-lync-server-2013"></a>Restauration d’un pool de serveurs Lync dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-18_

Votre déploiement de Lync Server est susceptible de comprendre les types de pools suivants :

  - serveur frontal

  - serveur de médiation

  - serveur de conversations permanentes

  - serveur Edge

Si un pool entier rencontre une panne, procédez comme suit pour chaque serveur membre du pool.

  - Dans le cas d’une réserve frontale, restaurez d’abord le serveur principal, puis restaurez chaque serveur frontal. Pour plus d’informations, reportez-vous à la rubrique [restauration d’un serveur principal Enterprise Edition dans Lync server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md) et [restauration d’un serveur membre Enterprise Edition dans Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).

  - Pour tous les autres types de pools, restaurez chaque serveur membre. Pour plus d’informations, reportez-vous à la rubrique [restauration d’un serveur membre Enterprise Edition dans Lync server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).

</div>

<span> </span>

</div>

</div>

</div>

