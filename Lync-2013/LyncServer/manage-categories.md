---
title: Gestion des catégories
description: Gérer les catégories.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Manage categories
ms:assetid: 1b118d91-b4c4-4b2f-b842-b451417ec2c6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204719(v=OCS.15)
ms:contentKeyID: 48183543
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf335b96c455647ebeb665364944e15d2e463fbe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446961"
---
# <a name="manage-categories"></a>Manage categories

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-06_

Pour créer une nouvelle catégorie de serveur Chat permanent

    New-CsPersistentChatCategory -Name Foo -PersistentChatPoolFqdn client.contoso1b118d91-b4c4-4b2f-b842-b451417ec2c6.com [other parameters]

<div>


> [!IMPORTANT]  
> PersistentChatPoolFqdn est requis uniquement s’il existe plusieurs pools de serveurs de chat permanent.



</div>

Pour apporter des modifications à la catégorie de serveur Chat permanent existante

    Set-CsPersistentChatCategory -Identity testCat -AllowedMembers @{Add="sip:user1@contoso.com", "CN=container,DC=contoso,DC=com"}  -DeniedMembers @{Add="sip:user2@contoso.com"}
    Set-CsPersistentChatCategory -Identity testCat -Creators @{Add="sip:user1@contoso.com"}

Windows PowerShell : AllowedMembers, DeniedMembers et Creators peuvent être définis simultanément. Creators doit être le sous-ensemble de AllowedMembers moins DeniedMembers. Vous pouvez également définir les propriétés d’une catégorie en même temps que les membres et créateurs.

<div>

## <a name="create-get-set-or-remove-a-category"></a>Créer, obtenir, définir ou supprimer une catégorie

Pour créer une nouvelle catégorie

    New-CsPersistentChatCategory -Name <String> [-PersistentChatPoolFqdn <String>] [-Description <String>] [-EnableInvitations<Switch Parameter>] [-EnableFileUpload <Switch Parameter>] [-RemoveChatHistory <Switch Parameter>] [-MaxContentSize <Integer>]

Pour obtenir une catégorie

    Get-CsPersistentChatCategory -Identity <String>

ou

    Get-CsPersistentChatCategory -PersistentChatPoolFqdn <String>

Pour définir une catégorie

    Set-CsPersistentChatCategory -Instance <CategoryObject> [-WhatIf] [-Confirm] [<CommonParameters>]

ou

    Set-CsPersistentChatCategory [-Identity] <string> [-Name <string>] [-Description <string>] [-Invitations <bool>] [-FileUpload <bool>] [-ChatHistory <bool>] [-AllowedMembers <PSListModifier[string]>] [-DeniedMembers <PSListModifier[string]>] [-Creators <PSListModifier[string]>] [-WhatIf] [-Confirm]  [<CommonParameters>]

Pour supprimer une catégorie

    Remove-CsPersistentChatCategory -Instance <CategoryObject> [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

ou

    Remove-CsPersistentChatCategory -Identity <String> [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

</div>

</div>

<span> </span>

</div>

</div>

</div>

