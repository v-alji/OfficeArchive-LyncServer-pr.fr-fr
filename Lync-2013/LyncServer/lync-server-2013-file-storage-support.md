---
title: Prise en charge du stockage des fichiers dans Lync Server 2013
description: Prise en charge du stockage de fichiers Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: File storage support
ms:assetid: ed66430d-3c19-4267-938c-956a51005073
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399073(v=OCS.15)
ms:contentKeyID: 48185743
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 03b7c3379c6aad6283f6a55b991ebaec50044bda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428180"
---
# <a name="file-storage-support-in-lync-server-2013"></a>Prise en charge du stockage des fichiers dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-16_

Lync Server 2013 utilise le même magasin de fichiers pour tout le stockage de fichiers. La prise en charge du stockage de fichiers comprend les éléments suivants :

  - Un partage de fichiers sur un réseau de stockage (DAS) ou un réseau de stockage (SAN), y compris le système de fichiers DFS et sur une baie redondante de disques indépendants (RAID) pour les magasins de fichiers. Pour plus d’informations sur la configuration requise, voir Configuration logicielle requise [pour les serveurs frontaux, la messagerie instantanée et la présence dans Lync server 2013](lync-server-2013-technical-requirements-for-front-end-servers-instant-messaging-and-presence.md) et la [Configuration matérielle et logicielle requise pour le directeur dans Lync Server 2013](lync-server-2013-hardware-and-software-requirements-for-the-director.md) dans la documentation de planification. Pour plus d’informations sur le système d’exploitation DFS pour Windows Server 2008, voir le guide détaillé pour Windows Server 2008 à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=202835](https://go.microsoft.com/fwlink/p/?linkid=202835) .

  - Un cluster partagé pour le partage de fichiers. Si vous utilisez un cluster partagé, vous devez utiliser des serveurs de cluster exécutant Windows Server 2008 ou Windows Server 2008 R2. L’utilisation de serveurs de cluster exécutant une version antérieure de Windows peut provoquer des problèmes d’autorisation qui empêchent la disponibilité de certaines fonctionnalités. Utilisez l’administrateur de cluster pour créer le partage de fichiers. Pour plus d’informations sur l’utilisation de l’administrateur de cluster, voir l’article de la base de connaissances Microsoft 284838, « création d’un partage de fichiers de cluster de serveurs avec Cluster.exe » [https://go.microsoft.com/fwlink/p/?linkId=140899](https://go.microsoft.com/fwlink/p/?linkid=140899) .

</div>

<span> </span>

</div>

</div>

</div>

