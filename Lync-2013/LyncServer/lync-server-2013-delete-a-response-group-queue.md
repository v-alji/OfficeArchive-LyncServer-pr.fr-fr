---
title: 'Lync Server 2013 : suppression d’une file d’attente de groupe de réponses'
description: 'Lync Server 2013 : supprimer une file d’attente de groupe de réponses.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a Response Group queue
ms:assetid: 67c7a489-8c5f-4c6b-9387-9d4c11d43695
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521008(v=OCS.15)
ms:contentKeyID: 48184356
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 76b00257a12b872615ebc124abff595268b120e1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430685"
---
# <a name="delete-a-response-group-queue-in-lync-server-2013"></a>Supprimer une file d’attente de groupe de réponses dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-11-01_

Pour supprimer une file d’attente, utilisez l’une des procédures suivantes.

<div>

## <a name="to-use-lync-server-control-panel-to-delete-a-queue"></a>Pour supprimer une file d’attente à l’aide du panneau de configuration de Lync Server

1.  Ouvrez une session en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre de l’un des rôles d’administration prédéfinis prenant en charge Response Group.

2.  Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server. Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Dans la barre de navigation de gauche, cliquez sur **Services Response Group**, puis sur **File d’attente**.

4.  Dans le champ de recherche, tapez tout ou partie du nom de la file d’attente que vous voulez supprimer.

5.  Dans la liste des files d’attente, cliquez sur la file d’attente de votre choix, cliquez sur **modifier**, puis cliquez sur **supprimer**.

6.  Cliquez sur **OK**.

</div>

<div>

## <a name="to-use-windows-powershell-to-delete-a-queue"></a>Pour utiliser Windows PowerShell pour supprimer une file d’attente

1.  Ouvrez une session en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre de l’un des rôles d’administration prédéfinis prenant en charge Response Group.

2.  Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.

3.  Dans la ligne de commande, exécutez la commande suivante :
    
        Get-CsRgsQueue -Identity <Application Server service> -Name "<name of queue>" | Remove-CsRgsQueue
    
    Exemple :
    
        Get-CsRgsQueue -Identity service:ApplicationServer:redmond.contoso.com -Name "Help Desk" | Remove-CsRgsQueue

</div>

</div>

<span> </span>

</div>

</div>

</div>

