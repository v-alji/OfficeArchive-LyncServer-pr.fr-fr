---
title: 'Lync Server 2013 : afficher les paramètres de configuration de la version du client'
description: 'Lync Server 2013 : afficher les paramètres de configuration de la version du client.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View client version configuration settings
ms:assetid: c72df4e6-a889-4cb6-86f7-8334d7774c6e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ923062(v=OCS.15)
ms:contentKeyID: 50675353
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 04fc25a1ab4904cbc6ca7871e1568ac8bc488bdf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443418"
---
# <a name="view-client-version-configuration-settings-in-lync-server-2013"></a>Afficher les paramètres de configuration de la version du client dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-23_

Les paramètres de configuration de version du client sont utilisés pour activer ou désactiver le contrôle de version du client. La configuration de la version du client global s’installe avec Lync Server 2013 et est utilisée pour activer ou désactiver le contrôle de version du client pour le déploiement complet du serveur. Lorsque la configuration globale est activée, toutes les stratégies de version du client en place prendront effet lorsque les utilisateurs tenteront de se connecter. Vous pouvez afficher les paramètres de configuration de la version du client à partir du panneau de configuration de Lync Server 2013 ou de Lync Server 2013 Management Shell.

<div>


> [!NOTE]  
> Comme ils ne sont pas associés à un utilisateur, un site ou un service spécifiques, les utilisateurs anonymes ne sont affectés que par les stratégies globales.



</div>

<div>

## <a name="to-view-client-version-configuration-settings-by-using-lync-server-control-panel"></a>Pour afficher les paramètres de configuration de la version du client à l’aide du panneau de configuration de Lync Server

1.  À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.

2.  Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server. Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Dans la barre de navigation de gauche, cliquez sur **clients**, puis sur le bouton de navigation configuration de la **version du client** .

4.  Double-cliquez sur le nom de la version de client que vous voulez afficher.

</div>

<div>

## <a name="viewing-client-version-configuration-settings-by-using-windows-powershell-cmdlets"></a>Affichage des paramètres de configuration de la version du client à l’aide des cmdlets Windows PowerShell

Vous pouvez afficher les paramètres de configuration de la version du client à l’aide de l’applet de contrôle **Get-CsClientVersionConfiguration** . Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell. Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-view-client-version-configuration-information"></a>Pour afficher les informations de configuration de la version du client

  - Pour afficher des informations sur les paramètres de configuration de la version de votre client, tapez la commande suivante dans Lync Server Management Shell, puis appuyez sur entrée :
    
        Get-CsClientVersionConfiguration
    
    Vous obtiendrez des indications semblables à ceci :
    
        Identity      : Global
        DefaultAction : Allow
        DefaultURL    :
        Enabled       : True

</div>

Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de connexion [Get-CsClientVersionConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsClientVersionConfiguration) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

