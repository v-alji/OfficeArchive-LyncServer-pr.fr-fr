---
title: Configuration de la surveillance SCOM
description: Configurer l’analyse SCOM.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure SCOM monitoring
ms:assetid: 4003d225-2a33-448c-abd9-571750661140
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688033(v=OCS.15)
ms:contentKeyID: 49733624
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c93e10c705a1a1e08972d7534e00a33c472d23a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394108"
---
# <a name="configure-scom-monitoring"></a>Configuration de la surveillance SCOM

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-04_

Après avoir effectué une migration vers Microsoft Lync Server 2013, vous devez effectuer quelques tâches pour configurer Lync Server 2013 de manière à utiliser System Center Operations Manager.

  - Appliquez les mises à jour de Lync Server 2010 à un serveur élu pour gérer la logique de découverte centrale.

  - Mettez à jour la clé de Registre du serveur prototype de découverte central.

  - Configurer votre serveur de gestion Operations Manager principal de System Center pour remplacer le nœud de découverte central.

Vous trouverez ci-dessous des instructions pour chacune de ces tâches.

**Appliquez les mises à jour de Lync Server 2010 à un serveur élu pour gérer la logique de découverte centrale.**

1.  Électionnez un serveur sur lequel les fichiers de l’agent Operations Manager System Center Operations Manager sont installés et est configuré en tant que nœud de découverte candidat.

2.  Appliquez les mises à jour de Lync Server 2010 à ce serveur. Voir la rubrique [appliquer les mises à jour de Lync Server 2010](apply-lync-server-2010-updates.md).

**Mettez à jour la clé de Registre du serveur prototype de découverte central.**

1.  Sur le serveur choisi pour gérer la logique de découverte centralisée, ouvrez une fenêtre de commande Windows PowerShell.

2.  Dans la ligne de commande, tapez ce qui suit :
    
       ```PowerShell
        New-Item -Path "HKLM:\Software\Microsoft\Real-Time Communications\Health"
       ```
    
       ```PowerShell
        New-Item -Path "HKLM:\Software\Microsoft\Real-Time Communications\Health\CentralDiscoveryCandidate"
       ```
    
    <div class="">
    

    > [!NOTE]  
    > Dès lors que vous modifiez le registre, il est possible que la commande échoue si la clé de Registre existe déjà. Si vous êtes à l’abri de cela, vous pouvez ignorer l’erreur.

    
    </div>

**Configurez votre serveur de gestion du gestionnaire d’opérations principales pour remplacer le nœud du centre de découverte central.**

1.  Sur un ordinateur sur lequel est installé la console System Center Operations Manager, développez **objets du pack d’administration** , puis sélectionnez découvertes d' **objets**.

2.  Cliquez sur **modifier l’étendue...**

3.  Dans la page d' **objets du pack d’administration d’étendue** , sélectionnez **ls découverte candidate**.

4.  Remplacez la **valeur effective** de la fonction de découverte (LS) par le nom du serveur candidat élu dans la procédure précédente.

Enfin, pour finaliser vos modifications, redémarrez le service d’intégrité sur le serveur de gestion de racines System Center Operations Manager.

</div>

<span> </span>

</div>

</div>

</div>

