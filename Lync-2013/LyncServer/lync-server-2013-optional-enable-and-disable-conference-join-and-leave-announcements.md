---
title: (Facultatif) Activation et désactivation des annonces indiquant qu’un utilisateur rejoint ou quitte une conférence
description: Facultatif Activez et désactivez l’Association de conférences et quittez les annonces.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Enable and disable conference join and leave announcements
ms:assetid: c9529568-e66c-48d8-aef2-9072f9c336ff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398834(v=OCS.15)
ms:contentKeyID: 48185403
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 70cd6b452a44d7d40f23d5ca96b6e4b7b063d2ec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445238"
---
# <a name="optional-enable-and-disable-conference-join-and-leave-announcements-in-lync-server-2013"></a>(Facultatif) Activation et désactivation des annonces indiquant qu’un utilisateur rejoint ou quitte une conférence dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-09-30_

Lorsque des utilisateurs d’appels entrants rejoignent ou quittent une conférence, l’application d’annonce d’annonce peut annoncer leur ouverture ou leur sortie en jouant un message ou en prononçant leurs noms. Vous pouvez modifier le fonctionnement des annonces en exécutant des cmdlets. Cette étape est facultative.

<div>

## <a name="to-modify-the-conference-join-and-leave-announcement-behavior"></a>Pour modifier le comportement des annonces indiquant qu’un utilisateur rejoint ou quitte une conférence

1.  Connectez-vous à l’ordinateur en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre du rôle **CS-ServerAdministrator** ou **CsAdministrator** .

2.  Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.

3.  Exécutez la commande suivante dans l’invite de commandes :
    
        Get-CsDialinConferencingConfiguration
    
    Cette applet de connexion récupère des informations sur la nécessité pour les participants d’enregistrer leur nom lorsqu’ils rejoignent une conférence et de la manière dont Lync Server répond lorsque les participants rejoignent ou quittent une conférence rendez-vous.

4.  Exécutez la commande suivante dans l’invite de commandes :
    
        Set-CsDialinConferencingConfiguration -Identity <identity of dial-in conferencing settings to be modified>
        [-EnableNameRecording <$true | $false>]
        [-EntryExitAnnouncementsEnabledByDefault <$true | $false>]
        [-EntryExitAnnouncementsType <UseNames | ToneOnly]
    
    **EnableNameRecording**   Détermine si les participants anonymes sont invités à enregistrer leur nom avant de participer à la Conférence. La valeur par défaut est « $true », ce qui signifie que les participants anonymes sont invités à donner leur nom avant de participer à une conférence. (Les participants authentifiés ne sont pas tenus d’indiquer leur nom, car leur nom complet est utilisé.)
    
    **EntryExitAnnouncementsEnabledByDefault**   Indique si l’annonce est activée ou désactivée par défaut. La valeur par défaut est « $false », ce qui signifie qu’aucune annonce n’est effectuée lorsque les participants rejoignent ou quittent une conférence. Lorsqu’il planifie une réunion, l’organisateur peut ignorer ce paramètre.
    
    **EntryExitAnnouncementsType**   Indique l’action effectuée dès qu’un participant rejoint ou quitte une conférence pour laquelle les annonces sont activées. La valeur par défaut est « UseNames », ce qui signifie qu’une annonce similaire à la suivante est effectuée : « Ken Myer a rejoint la conférence » lorsque les annonces sont activées.
    
    Vous pouvez configurer ces paramètres globalement ou au niveau d’un site. (Les paramètres configurés au niveau du site sont prioritaires sur les paramètres configurés au niveau global.)
    
    Par exemple :
    
        Set-CsDialinConferencingConfiguration -Identity site:Redmond
        -EnableNameRecording $false
        -EntryExitAnnouncementsEnabledByDefault $true
        -EntryExitAnnouncementsType ToneOnly
    
    Dans cet exemple, les paramètres sont configurés dans l’étendue du site de Redmond. Les annonces sont activées, mais les participants ne sont pas invités à donner leur nom lorsqu’ils rejoignent une conférence. Une tonalité est lue lorsque les participants entrent ou quittent une conférence.

</div>

</div>

<span> </span>

</div>

</div>

</div>

