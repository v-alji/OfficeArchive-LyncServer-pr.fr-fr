---
title: Cmdlets dans Skype entreprise Online utilisant une identité d’utilisateur et une étendue de balises
description: Cmdlets dans Skype entreprise Online qui utilisent une identité d’utilisateur et l’étendue des balises.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that use a user identity and the tag scope
ms:assetid: 344a21b0-5301-4e77-853a-970bb1c11e1d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362781(v=OCS.15)
ms:contentKeyID: 56558838
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3e2ddbcc9c90096cea5fad4cb680f4ea1797ce48
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394240"
---
# <a name="cmdlets-in-skype-for-business-online-that-use-a-user-identity-and-the-tag-scope"></a>Cmdlets dans Skype entreprise Online utilisant une identité d’utilisateur et une étendue de balises

 


Les applets de demande d' **autorisation-CS** (utilisées pour attribuer des stratégies aux utilisateurs) nécessitent deux identificateurs : une identité d’utilisateur (le paramètre Identity) et l’identité d’une stratégie par utilisateur (paramètre PolicyName). Par exemple, pour affecter la stratégie vocale, RedmondVoicePolicy, à l’utilisateur Ken Myer, utilisez la commande suivante :

    Grant-CsVoicePolicy -Identity "Ken Myer" -PolicyName "RedmondVoicePolicy"

Il existe deux éléments à garder à l’esprit lors de l’attribution de stratégies aux utilisateurs. Tout d’abord, seules les stratégies par utilisateur peuvent être affectées. Vous ne pouvez pas attribuer de stratégie globale à un utilisateur. Par exemple, la commande suivante échoue :

    Grant-CsVoicePolicy -Identity "Ken Myer" -PolicyName "global"

Cette commande échoue, car il n’est pas nécessaire d’affecter la stratégie globale. Si vous souhaitez gérer un utilisateur à l’aide de la stratégie globale, veillez à ne pas affecter cet utilisateur à une stratégie par utilisateur. Si aucune stratégie par utilisateur n’a été attribuée à un utilisateur, l’utilisateur est automatiquement géré à l’aide de la stratégie globale.


> [!NOTE]  
> Que se passe-t-il si une stratégie par utilisateur a déjà été affectée à l’utilisateur et que vous souhaitez annuler l’affectation de cette stratégie et l’utilisateur est-il géré à la place par la politique globale ? Dans ce cas, vous devez commencer par utiliser la syntaxe suivante, qui annule l’affectation d’une stratégie par utilisateur en attribuant une stratégie null à l’utilisateur :<BR>Grant-CsVoicePolicy-identité « Ken Myer »-PolicyName $Null



Deuxièmement, gardez à l’esprit que les stratégies par utilisateur sont créées à l’étendue de la balise. Toutefois, vous pouvez omettre le **préfixe** d’indicateur lorsque vous spécifiez le nom d’une stratégie. Ces deux commandes sont identiques :

    Grant-CsVoicePolicy -Identity "Ken Myer" -PolicyName "tag:RedmondVoicePolicy"
    Grant-CsVoicePolicy -Identity "Ken Myer" -PolicyName "RedmondVoicePolicy"

Si vous souhaitez renvoyer les identités pour toutes les stratégies par utilisateur (ou, au moins, toutes les stratégies par utilisateur de type spécifié, par exemple les stratégies vocales), utilisez une commande similaire à celle-ci :

    Get-CsVoicePolicy -Filter "tag:*"

Les applets de commande suivantes utilisent à la fois une identité d’utilisateur et l’étendue de la balise :

  - [Grant-CsClientPolicy](https://technet.microsoft.com/library/gg412942\(v=ocs.15\))

  - [Grant-CsConferencingPolicy](https://technet.microsoft.com/library/gg425937\(v=ocs.15\))

  - [Grant-CsDialPlan](https://technet.microsoft.com/library/gg398547\(v=ocs.15\))

  - [Grant-CsExternalAccessPolicy](https://technet.microsoft.com/library/gg425942\(v=ocs.15\))

  - [Grant-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/gg412829\(v=ocs.15\))

  - [Grant-CsVoicePolicy](https://technet.microsoft.com/library/gg398828\(v=ocs.15\))

## <a name="see-also"></a>Voir aussi


[Identités, étendues et clients dans Skype entreprise Online](identities-scopes-and-tenants-in-skype-for-business-online.md)  
[Applets de commande de Lync Online](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))

