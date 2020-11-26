---
title: 'Lync Server 2013 : installation du portail Web d’administration du système de salle Lync'
description: 'Lync Server 2013 : installation du portail Web d’administration du système de salle Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing the Lync Room System Administrative Web Portal
ms:assetid: dd19e368-c338-4e21-a40d-6439d46a9748
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn436326(v=OCS.15)
ms:contentKeyID: 56737622
ms.date: 04/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0fba239346d75142bb4009c58e0ac67e8e1f3bcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427004"
---
# <a name="installing-the-lync-room-system-administrative-web-portal-in-lync-server-2013"></a>Installing the Lync Room System Administrative Web Portal in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2015-04-09_

Vous pouvez télécharger le portail Web d’administration du système de salle Microsoft Lync à partir du centre de téléchargement Microsoft [https://go.microsoft.com/fwlink/p/?LinkId=324044](https://go.microsoft.com/fwlink/p/?linkid=324044) .

Pour installer le portail Web d’administration du système de salle Lync, procédez comme suit.

1.  Configurez le port d’application fiable en exécutant l’applet de commande suivante dans Lync Server Management Shell :
    
        Set-CsWebServer -Identity POOLFQDN -MeetingRoomAdminPortalInternalListeningPort 4456 -MeetingRoomAdminPortalExternalListeningPort 4457

2.  Pour installer le portail de salle de réunion, téléchargez **LyncRoomAdminPortal.exe** puis exécutez-le en tant qu’administrateur.

3.  Ouvrez le fichier Web.config à partir de l’emplacement suivant :
    
    % Program Files% \\ Microsoft Lync Server 2013 \\ composants WebPart \\ réunion portail de salle de réunion \\ \\\\

4.  Dans le fichier Web.Config, remplacez PortalUserName par le nom d’utilisateur créé à l’étape 2 de la section « Configuration des conditions préalables pour le portail d’administration du système de salle Lync » (le nom recommandé pour l’étape est LRSApp) :
    
        <add key="PortalUserName" value="sip:LRSApp@domain.com" />

5.  Le portail d’administration LRS étant une application fiable, vous n’avez pas besoin de fournir le mot de passe dans la configuration du portail. Si cet utilisateur utilise un autre serveur d’inscriptions que le serveur d’inscriptions local, vous devez le spécifier en ajoutant la ligne suivante dans le fichier Web.Config :
    
        <add key="PortalUserRegistrarFQDN" value="pool-xxxx.domain.com" />

6.  Si le port utilisé n’est pas le port 5061, ajoutez la ligne suivante dans le fichier Web.Config : 
    
        <add key="PortalUserRegistrarPort" value="5061" />

<div>

## <a name="verifying-installation-of-the-lync-room-system-administrative-web-portal"></a>Vérification de l’installation du portail Web d’administration du système de salle Lync

Pour vérifier l’installation du portail Web d’administration du système de salle Lync, procédez comme suit :


1.  Sur un serveur frontal, accédez à l’URL suivante :
    
    https:// \<fe-server\> /LRS
    
    Aucune erreur ne doit s’afficher, comme dans l’image suivante :
    
    ![Écran Connexion au portail d’administration Lync Room System](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Écran Connexion au portail d’administration Lync Room System")

2.  Si aucune erreur ne s’affiche, essayez d’accéder à l’URL suivante à partir d’un autre ordinateur dans la topologie :
    
    https:// \<fe-server\> /LRS
    
    Pour accéder à la page, vous devez ajouter les enregistrements DNS comme décrit dans la section « enregistrements DNS requis pour la connexion automatique au client » [https://go.microsoft.com/fwlink/p/?LinkId=318056](https://go.microsoft.com/fwlink/p/?linkid=318056) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

