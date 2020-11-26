---
title: 'Lync Server 2013 : affichage des informations relatives au site réseau'
description: 'Lync Server 2013 : affichage des informations relatives au site réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network site information
ms:assetid: 24a97d98-b168-4016-81bf-c2c478092b87
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687996(v=OCS.15)
ms:contentKeyID: 49733586
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b46dc91510cb5ff737977871470033374573ba8c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440401"
---
# <a name="viewing-network-site-information-in-lync-server-2013"></a>Affichage des informations sur le site réseau dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-23_

Les sites réseau sont les bureaux ou les emplacements configurés dans chaque région d’un contrôle d’admission des appels (CAC) ou un déploiement 9-1-1 amélioré. Vous pouvez consulter les informations relatives à un site réseau dans Lync Server 2013 Control Panel ou Lync Server Management Shell. Pour plus d’informations sur la création et la modification de sites réseau, voir [création ou modification de sites réseau dans Lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md).

<div>

## <a name="to-view-network-site-information-in-lync-server-control-panel"></a>Pour afficher les informations de site réseau dans le panneau de configuration de Lync Server

1.  À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.

2.  Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server. Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis cliquez sur **site**.

4.  Sur la page du **site** , cliquez sur le site que vous voulez afficher.
    
    <div>
    

    > [!NOTE]  
    > Vous ne pouvez afficher que les informations relatives à un site à la fois.

    
    </div>

5.  Dans le menu **Edition**, cliquez sur **Afficher les détails**.

</div>

<div>

## <a name="viewing-network-site-information-by-using-windows-powershell-cmdlets"></a>Affichage des informations sur le site réseau à l’aide des cmdlets Windows PowerShell

Vous pouvez afficher les informations sur le site réseau à l’aide de Windows PowerShell et de l’applet de connexion Get-CsNetworkSite. Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell. Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-view-network-site-information"></a>Pour afficher les informations relatives au site réseau

  - Pour afficher des informations sur tous les sites de votre réseau, tapez la commande suivante dans Lync Server Management Shell, puis appuyez sur entrée :
    
        Get-CsNetworkSite
    
    Vous obtiendrez des indications semblables à ceci :
    
        Identity          : Redmond
        NetworkSiteID     : Redmond
        Description       :
        NetworkRegionID   : Pacific Northwest
        BypassID          : 3b232b84-2c1d-4da2-8181-e9330bafebe9
        BWPolicyProfileID :
        LocationPolicy    :

</div>

Pour plus d’informations, consultez la rubrique d’aide de l’applet de passe [Get-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSite) .

</div>

<div>

## <a name="see-also"></a>Voir aussi


[Création ou modification de sites réseau dans Lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md)  
[Suppression d’un site réseau existant dans Lync Server 2013](lync-server-2013-deleting-an-existing-network-site.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

