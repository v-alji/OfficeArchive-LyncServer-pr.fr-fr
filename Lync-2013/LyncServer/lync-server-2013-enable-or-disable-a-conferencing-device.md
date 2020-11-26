---
title: 'Lync Server 2013 : activation ou désactivation d’un appareil de conférence'
description: 'Lync Server 2013 : activation ou désactivation d’un appareil de conférence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable a conferencing device
ms:assetid: d5140e38-d015-4706-9bde-cf2fa748c36b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994070(v=OCS.15)
ms:contentKeyID: 51803981
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 761bc19536c889cced68ff586753f6800df0da59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437573"
---
# <a name="enable-or-disable-a-conferencing-device-in-lync-server-2013"></a>Activer ou désactiver un appareil de conférence dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-20_

Activez et désactivez un appareil de conférence à l’aide de l’applet de passe **Enable-CsMeetingRoom** et de l’applet **de passe CsMeetingRoom** . Ces applets de commande peuvent être exécutées à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.

<div>


> [!NOTE]  
> Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .



</div>

<div>


<div>

## <a name="enabling-a-conferencing-device"></a>Activation d’un appareil de conférence

  - Pour activer un appareil de conférence, vous pouvez utiliser l’applet de passe **Enable-CsMeetingRoom** . Dans le cadre de l’activation d’un appareil de conférence, vous devez inclure a) l’identité de l’appareil de conférence, b) le pool d’inscriptions dans lequel le compte de la salle sera hébergé et c) l’adresse SIP à attribuer à ce compte.
    
        Enable-CsMeetingRoom -Identity "Redmond Conferencing device" -RegistrarPool "atl-cs-001.litwareinc.com" -SipAddress "sip:RedmondMeetingRoom@litwareinc.com"

</div>

<div>

## <a name="disabling-a-conferencing-device"></a>Désactivation d’un appareil de conférence

  - Pour désactiver un appareil de conférence, vous pouvez utiliser l’applet de vue **Disable-CsMeetingRoom** . Veillez à spécifier l’identité de l’appareil de conférence à désactiver :
    
        Disable-CsMeetingRoom -Identity "sip:RedmondMeetingRoom@litwareinc.com"

</div>

Pour plus d’informations, consultez les rubriques d’aide de l’applet de connexion [Enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) et de l’applet de connexion [Disable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Disable-CsMeetingRoom) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

