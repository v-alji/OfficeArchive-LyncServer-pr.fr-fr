---
title: 'Lync Server 2013 : afficher les informations sur les paramètres de configuration de Lync Phone Edition'
description: 'Lync Server 2013 : afficher les informations sur les paramètres de configuration de Lync Phone Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View Lync Phone Edition configuration settings information
ms:assetid: 15f94478-651f-4063-9918-6a059f98df16
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687976(v=OCS.15)
ms:contentKeyID: 49733564
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 62719b24920ee72a92b2f80498d5ea2a59288c2e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440415"
---
# <a name="view-lync-phone-edition-configuration-settings-information-in-lync-server-2013"></a>Afficher les informations sur les paramètres de configuration de Lync Phone Edition dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-23_

Vous pouvez consulter les informations de configuration des appareils exécutant Lync Phone Edition. Les informations sont organisées en collections. Lorsque vous installez Lync Server, vous obtenez un ensemble de paramètres Lync Phone Edition qui s’appliquent à tous les appareils exécutant Lync Phone Edition dans votre déploiement. Vous pouvez également créer de nouvelles collections de paramètres pour un site spécifique. Les paramètres de site sont prioritaires par rapport aux paramètres globaux. Chaque collection de paramètres est composée d’un nom, de l’étendue (globale ou d’un site), du paramètre de sécurité SIP, du niveau de journalisation, du niveau de qualité de service (QoS), du paramètre de verrouillage du téléphone et des détails du verrouillage du téléphone, c’est-à-dire de la longueur minimale du code confidentiel (PIN) et du temps avant que le téléphone se verrouille.

<div>

## <a name="to-view-configuration-information-about-devices-running-lync-phone-edition"></a>Pour afficher des informations de configuration sur les appareils exécutant Lync Phone Edition

1.  À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.

2.  Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server. Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Dans la barre de navigation de gauche, cliquez sur **clients**, puis sur le bouton navigation de **configuration d’appareil** .

4.  Dans la page **Configuration des appareils** , cliquez sur l’ensemble de paramètres pour lesquels vous souhaitez afficher les informations. Le nom, l’étendue, le paramètre de sécurité SIP, le niveau de qualité de la voix et les paramètres de verrouillage du téléphone apparaissent dans la page principale. Pour afficher le niveau de journalisation et les détails de verrouillage du téléphone, cliquez sur le menu **modifier** , puis sur **afficher les détails**.

</div>

<div>

## <a name="viewing-lync-phone-edition-configuration-information-by-using-windows-powershell-cmdlets"></a>Affichage des informations de configuration de Lync Phone Edition à l’aide des cmdlets Windows PowerShell

Vous pouvez afficher les paramètres de configuration de Lync Phone Edition à l’aide de Lync Server Management Shell et de l’applet **de passe Get-CsUCPhoneConfiguration** . Vous pouvez exécuter cette applet de commande sur Lync Server 2013 Management Shell ou à partir d’une session distante de Windows PowerShell. Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-view-lync-phone-edition-configuration-information"></a>Pour afficher les informations de configuration de Lync Phone Edition

  - Pour afficher des informations sur les paramètres de configuration de Lync Phone Edition, tapez la commande suivante dans Lync Server Management Shell, puis appuyez sur entrée :
    
        Get-CsUCPhoneConfiguration
    
    La commande renvoie des informations similaires à ce qui suit :
    
        Identity             : Global
        CalendarPollInterval : 00:03:00
        EnforcePhoneLock     : True
        PhoneLockTimeout     : 00:10:00
        MinPhonePinLength    : 6
        SIPSecurityMode      : High
        VoiceDiffServTag     : 40
        Voice8021p           : 0
        LoggingLevel         : Off

</div>

Pour plus d’informations, consultez la rubrique [Get-CsUCPhoneConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsUCPhoneConfiguration).

</div>

<div>

## <a name="see-also"></a>Voir aussi


[Créer ou modifier un ensemble de paramètres de configuration de Lync Phone Edition dans Lync Server 2013](lync-server-2013-create-or-modify-a-collection-of-lync-phone-edition-configuration-settings.md)  
[Supprimer une collection existante de paramètres de configuration de Lync Phone Edition dans Lync Server 2013](lync-server-2013-delete-an-existing-collection-of-lync-phone-edition-configuration-settings.md)  
[Configurer les paramètres de sécurité de Lync Phone Edition dans Lync Server 2013](lync-server-2013-configure-security-settings-for-lync-phone-edition.md)  
[Renforcer le verrouillage du téléphone dans Lync Server 2013](lync-server-2013-enforce-phone-locking.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

