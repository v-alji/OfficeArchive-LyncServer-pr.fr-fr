---
title: Déplacement des annuaires de conférences Lync Server 2010 vers Lync Server 2013
description: Déplacer des répertoires de conférences Lync Server 2010 vers Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Move Conference Directories
ms:assetid: 659867e0-ce91-4a95-9787-b1c1566460a8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727126(v=OCS.15)
ms:contentKeyID: 62387565
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12ac58ac0ab6f1908e7eac3e5824bf2304256632
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440345"
---
# <a name="move-conference-directories"></a>Déplacement des annuaires de conférences

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2014-05-28_

Avant de désaffecter un pool, vous devez effectuer la procédure suivante pour chaque annuaire de conférences de votre pool Lync Server 2010.

<div>

## <a name="to-move-a-conference-directory-to-lync-server-2013"></a>Pour déplacer un annuaire de conférences vers Lync Server 2013

1.  Ouvrez Lync Server Management Shell.

2.  Pour obtenir l’identité des annuaires de conférences au sein de votre organisation, exécutez la commande suivante :
    
        Get-CsConferenceDirectory
    
    La commande précédente renvoie tous les annuaires de conférences de votre organisation. Pour cette raison, il est possible que vous souhaitiez limiter les résultats au pool en cours de désactivation. Par exemple, si vous désaffectez le pool avec le nom de domaine complet (FQDN) pool01.contoso.net, utilisez cette commande pour limiter les données renvoyées aux annuaires de conférences à partir du pool :
    
        Get-CsConferenceDirectory | Where-Object {$_.ServiceID -match "pool01.contoso.net"}
    
    Cette commande renvoie uniquement les répertoires de conférences dans lesquels la propriété ServiceID contient le nom de domaine complet pool01.contoso.net.

3.  Pour déplacer des répertoires de conférence, exécutez la commande suivante pour chaque annuaire de conférences de la liste :
    
        Move-CsConferenceDirectory -Identity <Numeric identity of conference directory> -TargetPool <FQDN of pool where ownership is to be transitioned>
    
    Par exemple, pour déplacer l’annuaire de conférence 3, utilisez cette commande en spécifiant un pool Lync Server 2013 en tant que TargetPool :
    
        Move-CsConferenceDirectory -Identity 3 -TargetPool "pool02.contoso.net"
    
    Si vous souhaitez déplacer tous les répertoires de conférence sur un pool, utilisez une commande similaire à celle qui suit :
    
        Get-CsConferenceDirectory | Where-Object {$_.ServiceID -match "pool01.contoso.net"} | Move-CsConferenceDirectory -TargetPool "pool02.contoso.net"

[https://go.microsoft.com/fwlink/p/?linkId=246227](https://go.microsoft.com/fwlink/p/?linkid=246227)Pour obtenir des instructions complètes et détaillées sur la désaffectation des pools 2010 de Lync, voir le document « désinstallation de Microsoft Lync Server 2010 et suppression des rôles de serveur » (qui peut être téléchargé à partir de).

Lorsque vous déplacez des répertoires de conférence, vous pouvez rencontrer l’erreur suivante :

    WARNING: Move operation failed for conference directory with ID "5". Cannot perform a rollback because data migration might have already started. Retry the operation.
    WARNING: Before using the -Force parameter, ensure that you have exported the conference directory data using DBImpExp.exe and imported the data on the target pool. Refer to the DBImpExp-Readme.htm file for more information.
    Move-CsConferenceDirectory : Unable to cast COM object of type 'System._ComObject' to interface type 'Microsoft.Rtc.Interop.User.IRtcConfDirManagement'. 
    This operation failed because the QueryInterface call on the COM component for the interface with SID '{4262B886-503F-4BEA-868C-04E8DF562CEB}' failed due to the following error: The specified module could not be found.

Cette erreur se produit généralement lorsque Lync Server Management Shell nécessite un ensemble mis à jour d’autorisations Active Directory pour effectuer une tâche. Pour résoudre le problème, fermez l’instance actuelle de Management Shell, puis ouvrez une nouvelle instance de l’interpréteur de commandes, puis réexécutez la commande afin de déplacer le répertoire de conférence.

</div>

</div>

<span> </span>

</div>

</div>

</div>

