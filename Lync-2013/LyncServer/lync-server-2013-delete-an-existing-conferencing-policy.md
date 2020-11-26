---
title: 'Lync Server 2013 : supprimer une stratégie de conférence existante'
description: 'Lync Server 2013 : supprimez une stratégie de conférence existante.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing conferencing policy
ms:assetid: 709ed771-790f-4bf1-a4de-b37ca5168688
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688089(v=OCS.15)
ms:contentKeyID: 49733688
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b64e51acc6e6dc91b938244da28057b01957069
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430503"
---
# <a name="delete-an-existing-conferencing-policy-in-lync-server-2013"></a>Supprimer une stratégie de conférence existante dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-23_

Suivez ces étapes pour supprimer un utilisateur ou une stratégie de conférence au niveau du site.

<div>


> [!NOTE]  
> Vous ne pouvez pas supprimer la stratégie de conférence globale.



</div>

<div>

## <a name="to-delete-a-site-or-user-conferencing-policy"></a>Pour supprimer une stratégie de site ou de conférence utilisateur

1.  À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.

2.  Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server. Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Dans la barre de navigation de gauche, cliquez sur **Conférence** , puis sur **stratégie de conférence**.

4.  Dans la liste des stratégies de conférence, cliquez sur la stratégie de site ou d’utilisateur à supprimer, cliquez sur **Modifier**, puis sur **Supprimer**.

</div>

<div>

## <a name="removing-conferencing-policies-by-using-windows-powershell-cmdlets"></a>Suppression de stratégies de conférence à l’aide d’applets de cmdlet Windows PowerShell

Vous pouvez supprimer des stratégies de conférence à l’aide de Lync Server Management Shell et de l’applet de passe **Remove-CsConferencingPolicy** . Vous pouvez exécuter cette applet de commande sur Lync Server 2013 Management Shell ou à partir d’une session distante de Windows PowerShell. Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-remove-a-specified-conferencing-policy"></a>Pour supprimer une stratégie de conférence spécifiée

  - La commande suivante permet de supprimer la stratégie de conférence dont le paramètre Identity a la valeur RedmondConferencingPolicy :
    
        Remove-CsConferencingPolicy -Identity "RedmondConferencingPolicy"

</div>

<div>

## <a name="to-remove-all-of-the-conferencing-policies-applied-to-the-per-user-scope"></a>Pour supprimer toutes les stratégies de conférence appliquées à l’étendue par utilisateur

  - La commande suivante supprime toutes les stratégies de conférence configurées pour l’étendue par utilisateur :
    
        Get-CsConferencingPolicy -Filter "tag:*" | Remove-CsConferencingPolicy

</div>

<div>

## <a name="to-remove-all-of-the-conferencing-polices-that-allow-recording-by-external-users"></a>Pour supprimer toutes les stratégies de conférence autorisant l’enregistrement par des utilisateurs externes

  - La commande suivante supprime toutes les stratégies de conférence qui permettent aux utilisateurs externes d’enregistrer la Conférence :
    
        Get-CsConferencingPolicy | Where-Object {$_.AllowExternalUsersToRecordMeetings -eq $True} | Remove-CsConferencingPolicy

</div>

Pour plus d’informations, consultez la rubrique [Remove-CsConferencingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsConferencingPolicy).

</div>

</div>

<span> </span>

</div>

</div>

</div>

