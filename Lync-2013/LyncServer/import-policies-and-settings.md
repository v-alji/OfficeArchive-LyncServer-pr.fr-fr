---
title: Importer des stratégies et des paramètres
description: Importer des stratégies et des paramètres.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Import policies and settings
ms:assetid: b25decee-2ee5-4836-b370-454411d39252
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205178(v=OCS.15)
ms:contentKeyID: 48185147
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e014b7e8f0498742104118eec9eb313394ae6a94
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439603"
---
# <a name="import-policies-and-settings"></a>Importer des stratégies et des paramètres

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-09-28_

Après avoir fusionné vos informations topologiques Office Communications Server 2007 R2 avec votre pool de pilotes de Lync Server 2013, vous devez exécuter une cmdlet Lync Server 2013 Management Shell pour migrer vos stratégies et paramètres de configuration d’Office Communications Server 2007 R2 vers votre pool de pilotes Lync Server 2013.

L’applet **de connexion Import-CsLegacyConfiguration** importe les stratégies, les itinéraires vocaux, les plans de numérotation, les URL et les numéros d’accès rendez-vous sur Lync Server 2013.

<div>

## <a name="to-migrate-policies-and-settings"></a>Pour migrer des stratégies et des paramètres

1.  Sur le serveur frontal Lync Server 2013, démarrez Lync Server Management Shell.

2.  Dans la ligne de commande, tapez ce qui suit :
    
        Import-CsLegacyConfiguration
    
    Une fois les stratégies importées, utilisez la procédure suivante pour afficher les stratégies importées dans le panneau de configuration de Lync Server.

</div>

<div>

## <a name="to-view-imported-policies"></a>Pour afficher les stratégies importées

1.  Ouvrez le panneau de configuration de Lync Server 2013.

2.  Cliquez sur **routage** et afficher les stratégies importées.

3.  Cliquez sur **Conférence** et affichez les stratégies importées.

4.  Cliquez sur **Fédération et accès externe** , puis affichez les stratégies importées.

5.  Cliquez sur **surveillance et archivage** et afficher les stratégies importées.

</div>

</div>

<span> </span>

</div>

</div>

</div>

