---
title: (Recommandé) Création d’annuaires de conférences
description: Recommande Créer des annuaires de conférences.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: (Recommended) Create Conference Directories
ms:assetid: 787f4c94-1c96-468a-a74d-e06b7bd4b8a3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn832056(v=OCS.15)
ms:contentKeyID: 63146389
ms.date: 10/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b14982893fbc14a87818875a787d0f776da84ae3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443264"
---
# <a name="recommended-create-conference-directories"></a>(Recommandé) Création d’annuaires de conférences

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2014-10-03_

Les annuaires de conférences maintiennent un mappage entre l’ID de réunion alphanumérique qu’un participant utilise pour participer à une conférence lors de l’utilisation de la 2013 Lync et l’ID de conférence numérique uniquement qu’un participant à la Conférence rendez-vous utilise pour rejoindre la Conférence. Le format de l’ID de conférence est le suivant :

    <housekeeping digit (1 digit)><conference directory (usually 1-2 digits)><conference number (variable number of digits><check digit (1 digit)>

La création de différents annuaires des conférences permet de s’assurer que les ID de conférences restent courts jusqu’à ce qu’une quantité importante de conférences ait été créée. Dans une organisation avec un nombre type de conférences par utilisateur, il est recommandé de créer un annuaire des conférences ne dépassant pas 999 utilisateurs dans le pool. Dans cette règle, les ID de conférence peuvent généralement être conservés de petite taille. Toutefois, dès que le nombre d’annuaires de conférences (pour les pools) dépasse 9, la longueur de l’ID de conférence augmente pour prendre en charge d’autres conférences.

<div>

## <a name="creating-a-conference-directory"></a>Création d’un annuaire de conférences

1.  Dans Lync Server Management Shell, tapez l’applet de commande suivante :
    
        New-CsConferenceDirectory -Identity <XdsGlobalRelativeIdentity> -HomePool <String> [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
    
    Par exemple, l’exemple suivant crée un annuaire de conférences avec l’Identity 42, hébergé sur le pool atl-cs-001.litwareinc.com :
    
        New-CsConferenceDirectory -Identity 42 -HomePool "atl-cs-001.litwareinc.com"

</div>

<div>

## <a name="see-also"></a>Voir aussi


[Configuration requise pour les conférences rendez-vous dans Lync Server 2013](lync-server-2013-dial-in-conferencing-requirements.md)  


[New-CsConferenceDirectory](https://docs.microsoft.com/powershell/module/skype/New-CsConferenceDirectory)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

