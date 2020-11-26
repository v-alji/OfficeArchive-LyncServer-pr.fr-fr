---
title: 'Lync Server 2013 : suppression d’une stratégie d’archivage'
description: 'Lync Server 2013 : suppression d’une stratégie d’archivage.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting an Archiving policy
ms:assetid: 4739a691-41cc-4128-8bb8-6d5a4c02107a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520989(v=OCS.15)
ms:contentKeyID: 48184043
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ecf465a62cf8f54777b03a1634d9a95f1b565c9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430363"
---
# <a name="deleting-an-archiving-policy-in-lync-server-2013"></a>Suppression d’une stratégie d’archivage dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-23_

Vous pouvez supprimer une stratégie d’utilisateur ou une stratégie de site. La stratégie globale ne peut pas être supprimée. Si vous tentez de supprimer la stratégie globale, Lync Server 2013 réinitialise automatiquement la stratégie aux valeurs par défaut.

<div>


> [!NOTE]  
> Si vous avez activé l’intégration de Microsoft Exchange pour votre déploiement, les stratégies Exchange contrôlent la mise en place de l’archivage pour les utilisateurs hébergés sur Exchange 2013 et disposant de leurs boîtes aux lettres dans In-Place attente. Pour plus d’informations, reportez-vous à la rubrique <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">configuration de stratégies d’archivage dans Lync server 2013 lors de l’utilisation d’une intégration Exchange Server</A> dans la documentation de déploiement.



</div>

<div>

## <a name="to-delete-a-user-or-site-policy-for-archiving"></a>Pour supprimer une stratégie d’utilisateur ou de site pour l’archivage

1.  À partir d’un compte d’utilisateur auquel est affecté un des rôles CsArchivingAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.

2.  Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server. Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Dans la barre de navigation gauche, cliquez sur **surveillance et archivage**, puis cliquez sur **stratégie d’archivage**.

4.  Dans la liste des stratégies d’archivage, cliquez sur la stratégie utilisateur ou la stratégie de site que vous souhaitez supprimer, cliquez sur **Modifier**, puis sur **Supprimer**.

5.  Cliquez sur **Valider**.

</div>

<div>

## <a name="removing-archiving-policies-by-using-windows-powershell-cmdlets"></a>Suppression de stratégies d’archivage à l’aide des cmdlets Windows PowerShell

Les stratégies d’archivage peuvent être supprimées à l’aide de Windows PowerShell et de l’applet de passe **Remove-CsArchivingPolicy** . Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell. Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-remove-a-specified-archiving-policy"></a>Pour supprimer une stratégie d’archivage spécifiée

  - Par exemple, **Remove-CsArchivingPolicy** supprime la stratégie avec le site identité : Redmond. Notez qu’en cas de suppression d’une stratégie configurée sur l’étendue du site, les utilisateurs gérés par cette stratégie de site seront automatiquement gouvernés par la stratégie d’archivage globale. La commande suivante supprime l’archivage appliqué au site de Redmond :
    
        Remove-CsArchivingPolicy -Identity site:Redmond

</div>

<div>

## <a name="to-remove-all-the-archiving-policies-applied-to-the-per-user-scope"></a>Pour supprimer toutes les stratégies d’archivage appliquées à l’étendue par utilisateur

  - Cette commande supprime toutes les stratégies d’archivage appliquées à l’étendue par utilisateur :
    
        Get-CsArchivingPolicy -Filter "tag:*" | Remove-CsArchivingPolicy

</div>

<div>

## <a name="to-remove-all-the-archiving-policies-that-disable-internal-archiving"></a>Pour supprimer toutes les stratégies d’archivage qui désactivent l’archivage interne

  - Cette commande permet de supprimer toutes les stratégies d’archivage où l’archivage interne a été désactivé :
    
        Get-CsArchivingPolicy | Where-Object {$_.ArchiveInternal -eq $False} | Remove-CsArchivingPolicy

</div>

Pour plus d’informations, reportez-vous à la rubrique d’aide relative à l’applet de passe [Remove-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsArchivingPolicy) .

</div>

<div>

## <a name="see-also"></a>Voir aussi


[Gestion de l’archivage des communications internes et externes dans Lync Server 2013](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

