---
title: 'Lync Server 2013 : configuration du serveur de gestion principal'
description: 'Lync Server 2013 : configuration du serveur de gestion principal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the primary management server
ms:assetid: 44e2e9a8-c130-4c66-9871-80b1ff11b27c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204844(v=OCS.15)
ms:contentKeyID: 48183986
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 43f986f4f03e96cafa27dfdd302bb98a00d8b2ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395217"
---
# <a name="configuring-the-primary-management-server-in-lync-server-2013"></a>Configuration du serveur de gestion principal dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2014-03-19_

Pour tirer pleinement parti des nouvelles fonctionnalités de l’analyse de l’intégrité intégrées aux administrateurs Microsoft Lync Server 2013, vous devez commencer par désigner un ordinateur pour agir en tant que serveur d’administration principal. sur cet ordinateur, vous devez ensuite installer System Center Operations Manager 2007 R2 ou System Center Operations Manager 2012. Par ailleurs, vous devez installer une version prise en charge de SQL Server pour pouvoir fonctionner en tant que base de données principale Operations Manager. Si vous utilisez System Center Operations Manager 2012, vous pouvez utiliser l’une des versions suivantes de SQL Server comme base de données principale :

  - SQL Server 2008 R2 Service Pack 1

  - SQL Server 2008 R2 Service Pack 2

Si vous utilisez System Center Operations Manager 2007 R2, il est recommandé d’installer SQL Server 2005 Service Pack 4 ou SQL Server 2008 Service Pack 3. Vous pouvez également utiliser SQL Server 2008 R2 en tant que base de données principale pour System Center Operations Manager 2007 R2. Pour plus d’informations sur la configuration de SQL Server 2008 R2 pour l’utilisation de System Center Operations Manager 2007 R2, voir l’annexe 1 de cette documentation.

Lorsque vous installez System Center Operations Manager 2012 ou System Center Operations Manager 2007 R2, vous devez installer tous les composants de ce produit, y compris :

  - Base de données opérationnelle

  - Serveur

  - Console

  - Cmdlets Windows PowerShell

  - Console web

  - Créateur de rapports

  - Entrepôt de données

Ces composants et leur installation ne seront pas abordés en détail dans ce document. Pour plus d’informations sur System Center Operations Manager 2007 R2, voir la documentation Operations Manager 2007 R2 sur <https://go.microsoft.com/fwlink/p/?linkid=257526> le document System Center Operations manager 2012 <https://go.microsoft.com/fwlink/p/?linkid=257527> . Suivez ces instructions si vous envisagez d’utiliser SQL Server 2005 ou SQL Server 2008 Service Pack 1 comme base de données principale.

Si vous utilisez System Center Operations Manager 2012, vous pouvez utiliser SQL Server 2012 comme base de données principale. Pour plus d’informations sur SQL Server 2012, voir la documentation en ligne pour SQL Server 2012 à l’adresse [https://go.microsoft.com/fwlink/p/?LinkId=257528](https://go.microsoft.com/fwlink/p/?linkid=257528) .

Gardez à l’esprit que vous ne pouvez avoir qu’un seul serveur de gestion principal par déploiement de Lync Server. Par ailleurs, si vous pouvez utiliser System Center Operations Manager 2012 ou System Center Operations Manager 2007 R2, vous ne pouvez pas exécuter les deux applications en même temps, vous devez en choisir une. Par exemple, si vous exécutez System Center Operations Manager 2012, tous vos agents System Center doivent également exécuter System Center Operations Manager 2012. Vous ne pouvez pas disposer de certains agents exécutant System Center Operations Manager 2012 et d’autres agents exécutant System Center Operations Manager 2007 R2.

</div>

<span> </span>

</div>

</div>

</div>

