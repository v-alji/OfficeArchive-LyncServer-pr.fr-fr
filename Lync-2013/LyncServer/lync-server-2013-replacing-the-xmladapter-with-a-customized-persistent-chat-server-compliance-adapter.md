---
title: 'Lync Server 2013 : remplacement de XmlAdapter par un adaptateur de conformité personnalisé de serveur de conversation persistant'
description: 'Lync Server 2013 : remplacement de XmlAdapter par un adaptateur de conformité personnalisé de serveur de conversation persistant.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Replacing the XmlAdapter with a customized Persistent Chat Server Compliance adapter
ms:assetid: 2cb70db2-663f-40a6-abcf-89ea7d4a8b65
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ680106(v=OCS.15)
ms:contentKeyID: 49558152
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a90b4df7df42ffdc6c55e9b551b0eb53d07ab1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394512"
---
# <a name="replacing-the-xmladapter-with-a-customized-persistent-chat-server-compliance-adapter-in-lync-server-2013"></a>Remplacement de XmlAdapter par un adaptateur de conformité du serveur de chat permanent personnalisé dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-11-01_

Vous pouvez écrire un adaptateur personnalisé au lieu d’utiliser le XmlAdapter qui est installé avec le serveur de chat permanent. Pour ce faire, vous devez fournir un assembly .NET Framework contenant une classe publique qui implémente l’interface **IComplianceAdapter**. Dans le dossier d’installation serveur Chat permanent de chaque serveur dans votre pool de serveurs chat permanent, vous devez l’installer. Chacun des serveurs de conformité peut fournir des données de conformité à votre adaptateur, mais ils ne délivrent aucun duplicata des données de conformité à plusieurs instances de votre adaptateur.

<div>

## <a name="implementing-the-icomplianceadapter-interface"></a>Implémentation de l’interface IComplianceAdapter

L’interface est définie dans l’assembly Compliance.dll dans l’espace de noms `Microsoft.Rtc.Internal.Chat.Server.Compliance` . Elle définit deux méthodes que votre adaptateur personnalisé doit implémenter.

    void SetConfig(AdapterConfig config)

Le serveur de conformité des conversations permanent appelle cette méthode lors du premier chargement de la carte. Le `AdapterConfig` contient la configuration de compatibilité de conversation permanente pertinente pour la carte de conformité.

    void Translate(ConversationCollection conversations)

Le serveur de conformité des conversations permanent appelle cette méthode à intervalles réguliers tant qu’il existe de nouvelles données à traduire. Cet intervalle de temps est égal à la `RunInterval` valeur définie dans la configuration de la conformité aux conversations persistantes.

Le `ConversationCollection` contient les informations de conversation collectées à partir de la dernière fois que cette méthode a été appelée.

</div>

</div>

<span> </span>

</div>

</div>

</div>

