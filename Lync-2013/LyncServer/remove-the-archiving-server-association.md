---
title: Supprimer l’association au serveur d’archivage
description: Supprimez l’Association du serveur d’archivage.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove the Archiving server association
ms:assetid: dabac157-71ee-4afe-b0b6-4a083d165ffb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721903(v=OCS.15)
ms:contentKeyID: 49733837
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f6c34e49b0217a8318a83752b3878a7625e5d58
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395249"
---
# <a name="remove-the-archiving-server-association"></a>Supprimer l’association au serveur d’archivage

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-04_

Pour supprimer un serveur d’archivage, vous devez modifier ou effacer la dépendance sur le pool frontal associé, le serveur frontal, l’unité de branchement Survivable et le serveur de succursales survivant. Vous pouvez modifier les propriétés du pool frontal, du serveur frontal, de l’unité de branchement Survivable et du serveur de succursales survivant pour supprimer la dépendance. Une fois que vous avez effacé les dépendances et que vous avez supprimé le serveur dans le générateur de topologie, vous êtes informé que l’objet du magasin de base de données associé dans le générateur de topologie sera également supprimé.

<div>

## <a name="to-remove-the-archiving-server-association"></a>Pour supprimer l’Association du serveur d’archivage

1.  Ouvrez le serveur frontal Lync Server 2013, ouvrez le générateur de topologie.

2.  Accédez au nœud Lync Server 2010.

3.  Dans le générateur de topologie, développez **Pools front end Edition**, **serveurs front end Standard Edition** ou **sites de succursales** en fonction de l’emplacement de définition du serveur d’archivage.

4.  Si vous avez un serveur de succursales Survivable associé, développez **sites de succursales**, développez le nom du site de la succursale, puis développez **appareils de branchement survivables**.
    
    <div>
    

    > [!NOTE]  
    > Les <STRONG>appareils de branchement survivables</STRONG> dans l’interface utilisateur s’appliquent à la fois au serveur de succursales survivant et au dispositif de branchement survivant.

    
    </div>

5.  Cliquez avec le bouton droit sur le pool, le serveur ou l’appareil associé au serveur d’archivage, puis cliquez sur **modifier les propriétés**.

6.  Dans la boîte de **dialogue Modifier les propriétés**, sous **général**, sous **associations**, décochez la case associer un **serveur d’archivage** , puis cliquez sur **OK**.

7.  Répétez l’étape précédente pour tout autre serveur ou appareil associé au serveur d’archivage que vous voulez supprimer.

8.  Cliquez avec le bouton droit sur le serveur d’archivage, puis cliquez sur **supprimer**.

9.  Sur **Supprimer les magasins dépendants**, cliquez sur **OK**.

10. Publiez la topologie, vérifiez l’état de la réplication, puis exécutez l’Assistant Déploiement de Lync Server selon vos besoins.

</div>

</div>

<span> </span>

</div>

</div>

</div>

