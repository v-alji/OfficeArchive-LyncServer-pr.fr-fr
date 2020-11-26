---
title: 'Lync Server 2013 : afficher les informations de périphérique de conférence'
description: 'Lync Server 2013 : afficher des informations sur l’appareil de conférence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View conferencing device information
ms:assetid: 838bdbf8-8b68-4eb6-8fa3-45bfd5b0b1cd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994043(v=OCS.15)
ms:contentKeyID: 51803954
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9bbbdcecbc15ef59b2b9e22ffd2b28ff745d67a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443369"
---
# <a name="view-conferencing-device-information-in-lync-server-2013"></a>Afficher les informations de périphérique de conférence dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-20_

Vous pouvez afficher des informations sur les appareils de conférence configurés pour une utilisation au sein de votre organisation à l’aide de Windows PowerShell et de l’applet **de passe Get-CsMeetingRoom** . Exécutez l’applet de commande **Get-CsMeetingRoom** à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.

<div>


> [!NOTE]  
> Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .



</div>

Si vous utilisez l’applet de passe **Get-CsMeetingRoom** sans aucun paramètre, elle renvoie des informations sur tous vos périphériques de conférence. Les paramètres facultatifs permettent de filtrer les informations de différentes manières. Pour plus d’informations, consultez la section paramètres de [Get-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingRoom).

<div>


<div>

## <a name="viewing-information-about-all-your-conferencing-devices"></a>Affichage d’informations sur tous vos périphériques de conférence

  - Pour afficher les détails de tous vos appareils de conférence, tapez la commande suivante dans Lync Server Management Shell, puis appuyez sur entrée :
    
        Get-CsMeetingRoom
    
    Cette applet de commande renvoie des informations similaires à ce qui suit pour chaque appareil de conférence. Notez que l’exemple ci-après illustre les informations que vous verrez lors de l’exécution de cette cmdlet :
    
        ContactOptionFlags                : 64
        OwnerUrn                          : urn:device:roomsystem
        OriginatorSid                     :
        SamAccountName                    : room12129
        UserPrincipalName                 : room1219@litwareinc.com
        FirstName                         : 
        LastName                          :
        WindowsEmailAddress               :
        Sid                               : S-1-5-21-2831376166-2963252556-2165051629-1257
        LineServerURI                     :
        AudioVideoDisabled                : False
        IPPBXSoftPhoneRoutingEnabled      : False
        RemoteCallControlTelephonyEnabled : False
        PrivateLine                       :
        AcpInfo                           : {}
        HostedVoiceMail                   :
        DisplayName                       : Room 1219

</div>

<div>

## <a name="viewing-information-about-a-specific-conferencing-device"></a>Affichage d’informations sur un appareil de conférence spécifique

  - Pour afficher des informations pour un appareil de conférence spécifique, incluez le paramètre Identity suivi de l’identité de l’appareil de conférence (en général, le nom d’affichage Active Directory). Par exemple :
    
        Get-CsMeetingRoom -Identity "Room 1219"

</div>

Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de connexion [Get-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingRoom) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

