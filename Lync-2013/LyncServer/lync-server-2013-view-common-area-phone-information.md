---
title: 'Lync Server 2013 : afficher les informations sur le téléphone de la zone commune'
description: 'Lync Server 2013 : afficher les informations sur le téléphone de zone commune.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View common area phone information
ms:assetid: e652240c-6a3f-4be7-a083-32f24c08e655
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994081(v=OCS.15)
ms:contentKeyID: 51803992
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e4debe9a76118ac0bf1ca711426ce5487009a053
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443376"
---
# <a name="view-common-area-phone-information-in-lync-server-2013"></a>Afficher des informations sur le téléphone de zone commune dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-20_

Vous pouvez afficher des informations sur les téléphones communs configurés pour une utilisation au sein de votre organisation à l’aide de l’applet de passe **Get-CsCommonAreaPhone** . Utilisé sans paramètre, cette applet de méthode renvoie des informations sur tous les téléphones communs. Les paramètres facultatifs permettent de filtrer les informations de différentes manières. Par exemple, vous pouvez retourner tous les téléphones de zone commune qui possèdent des objets de contact dans une unité d’organisation (UO) spécifiée, ou tous les objets de contact situés dans un immeuble spécifié. Pour plus d’informations sur les paramètres **Get-CsCommonAreaPhone** , voir [Get-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone).

Exécutez **Get-CsCommonAreaPhone** à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.

<div>


<div>

## <a name="viewing-information-about-all-your-common-area-phones"></a>Affichage d’informations sur tous les téléphones de votre zone commune

  - Pour afficher des informations sur tous les téléphones communs, tapez la commande suivante dans Lync Server Management Shell, puis appuyez sur entrée :
    
        Get-CsCommonAreaPhone
    
    Vous obtiendrez des informations similaires à ce qui suit :
    
        Identity           : CN=Building 14 Lobby,OU=Redmond,
                             DC=litwareinc,DC=com
        RegistrarPool      : atl-cs-001.litwareinc.com
        Enabled            : True
        SipAddress         : sip:4714e34b-9781-421d-b07a-
                             52056b5b4a56@litwareinc.com
        ClientPolicy       :
        PinPolicy          :
        VoicePolicy        :
        MobilityPolicy     :
        GroupChatPolicy    :
        ConferencingPolicy :
        LineURI            : tel:+14255550712
        DisplayNumber      : 1-425-555-0712
        DisplayName        : Building 14 Lobby
        Description        :
        ExUmEnabled        : False

</div>

Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de connexion [Get-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

