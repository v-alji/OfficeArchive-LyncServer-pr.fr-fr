---
title: 'Lync Server 2013 : affectation d’une stratégie de messagerie vocale hébergée par utilisateur'
description: 'Lync Server 2013 : attribuez une stratégie de messagerie vocale hébergée par utilisateur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a per-user hosted voice mail policy
ms:assetid: d44c71a0-4407-4ab4-b7e0-d671dde3425f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398919(v=OCS.15)
ms:contentKeyID: 48185456
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 071d504c452b4d3adb1b636cb5c4ff8835200107
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440520"
---
# <a name="assign-a-per-user-hosted-voice-mail-policy-in-lync-server-2013"></a>Affecter une stratégie de messagerie vocale hébergée par utilisateur dans Lync Server 2013

 


Le déploiement d’une ou plusieurs stratégies de messagerie vocale hébergées par utilisateur est facultatif. Si vous déployez des stratégies par utilisateur, vous devez les affecter explicitement aux utilisateurs, groupes ou objets de contact.

Pour plus d’informations sur l’attribution ou la suppression de l’attribution de stratégies de messagerie vocale hébergées par utilisateur, voir la documentation Lync Server Management Shell pour les applets de commande suivantes :

  - Grant-CsHostedVoicemailPolicy

  - Remove-CsHostedVoicemailPolicy

## <a name="to-assign-a-per-user-hosted-voice-mail-policy"></a>Pour attribuer une stratégie de messagerie vocale hébergée par utilisateur

1.  Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.

2.  Exécutez l’applet de cmdlet Grant-CsHostedVoicemailPolicy pour affecter la stratégie de messagerie vocale hébergée par utilisateur à des utilisateurs, des groupes et des objets de contact individuels. Par exemple, exécutez :
    
        Grant-CsHostedVoicemailPolicy -Identity "Ken Myer" -PolicyName ExRedmond
    
    Dans cet exemple, la stratégie de messagerie vocale hébergée exredmond est affectée à l’utilisateur Ken Myer.
    
    **Identité** indique le compte d’utilisateur à modifier. La valeur IDENTITY peut être spécifiée en utilisant l’un des formats suivants :
    
      - Adresse SIP de l’utilisateur
    
      - Nom d’utilisateur principal d’Active Directory de l’utilisateur
    
      - Le nom de connexion au domaine de l’utilisateur \\ (par exemple, Contoso \\ kenmyer);
    
      - Le Display-Name de services de domaine Active Directory de l’utilisateur (par exemple, Ken Myer). Si vous utilisez le Display-Name comme valeur d’identité, vous pouvez utiliser le \* caractère générique astérisque (). Par exemple, l’identité « \* Smith » renvoie tous les utilisateurs qui ont une Display-Name se terminant par la valeur de chaîne « Smith ».
    

    > [!NOTE]  
    > Le nom de compte SAM-nom Active Directory de l’utilisateur ne peut pas être utilisé en tant que valeur d’identité, car le nom de compte SAM n’est pas nécessairement unique dans la forêt.


