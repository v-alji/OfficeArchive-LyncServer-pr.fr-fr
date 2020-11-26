---
title: 'Lync Server 2013 : approuver une règle de mise à jour de l’appareil'
description: 'Lync Server 2013 : approuver une règle de mise à jour d’appareil.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Approve a Device Update rule
ms:assetid: 9dbb1c9a-be0f-4e13-9234-05501ab43ac5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994053(v=OCS.15)
ms:contentKeyID: 51803964
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 127d16dad6329e952b9033db07ac2f4a4fe9112c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440562"
---
# <a name="approve-a-device-update-rule-in-lync-server-2013"></a>Approuver une règle de mise à jour d’appareil dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-23_

Une fois que vous avez importé une règle de mise à jour de l’appareil, celle-ci est installée sur vos appareils de test. Si le test est concluant et que vous souhaitez déployer la mise à jour de votre organisation, approuvez-la à l’aide du panneau de configuration de Lync Server ou de Windows PowerShell.

<div>

## <a name="to-approve-a-device-update-rule-by-using-lync-server-control-panel"></a>Pour approuver une règle de mise à jour de l’appareil à l’aide du panneau de configuration de Lync Server

1.  À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.

2.  Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server. Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Dans la page **mise à jour** de l’appareil, effectuez l’une des opérations suivantes :
    
      - Pour approuver une règle, sélectionnez cette règle.
    
      - Pour approuver toutes les règles, cliquez sur **modifier**, puis sur **Sélectionner tout**.

4.  Cliquez sur **action**, puis cliquez sur **approuver**.

</div>

<div>

## <a name="approving-a-device-update-rule-by-using-windows-powershell-cmdlets"></a>Approbation d’une règle de mise à jour de l’appareil à l’aide des applets de cmdlet Windows PowerShell

Les règles de mise à jour d’appareils peuvent également être approuvées à l’aide de Windows PowerShell et de l’applet de passe **approbateur-CsDeviceUpdateRule** . Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.

<div>


> [!NOTE]  
> Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .



</div>

<div>

## <a name="to-approve-a-single-device-update-rule"></a>Pour approuver une seule règle de mise à jour de l’appareil

  - La commande suivante approuve la règle de mise à jour de l’appareil d5ce3c10-2588-420a-82ac-dc2d9b1222ff9 trouvée sur le serveur Web atl-cs-001.litwareinc.com :
    
        Approve-CsDeviceUpdateRule -Identity service:WebServer:atl-cs-001.litwareinc.com/d5ce3c10-2588-420a-82ac-dc2d9b1222ff9

</div>

<div>

## <a name="to-approve-multiple-device-update-rules"></a>Pour approuver plusieurs règles de mise à jour de l’appareil

  - Cette commande approuve toutes les règles de mise à jour d’appareils pour les appareils de marque Microsoft :
    
        Get-CsDeviceUpdateRule | Where-Object {$_.Brand -eq "Microsoft"} | Approve-CsDeviceUpdateRule

</div>

Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de connexion [approbateur-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Approve-CsDeviceUpdateRule) .

</div>

<div>

## <a name="see-also"></a>Voir aussi


[Importer des règles de mise à jour de périphériques dans Lync Server 2013](lync-server-2013-import-device-update-rules.md)  
[Restaurer une règle de mise à jour d’appareil dans Lync Server 2013](lync-server-2013-restore-a-device-update-rule.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

