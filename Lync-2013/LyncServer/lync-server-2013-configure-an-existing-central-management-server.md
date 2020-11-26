---
title: 'Lync Server 2013 : Configuration d’un serveur de gestion centralisée existant'
description: 'Lync Server 2013 : configurez un serveur de gestion central existant.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure an existing Central Management Server
ms:assetid: d715b24a-1256-4a7c-a5ef-1cee41d6b733
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205315(v=OCS.15)
ms:contentKeyID: 48185584
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef93281be2537ca5e4a5892a8617500ce54f3c45
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434122"
---
# <a name="configure-an-existing-central-management-server-in-lync-server-2013"></a>Configuration d’un serveur de gestion centralisée existant dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-21_

Si vous réutilisez un serveur de gestion central à partir d’un déploiement 2013 de Lync Server, vous devez exécuter la procédure décrite ci-dessous pour vous assurer que le panneau de configuration de Lync Server et Windows PowerShell fonctionnent correctement.

<div>

## <a name="to-configure-an-existing-central-management-server"></a>Pour configurer un serveur de gestion central existant

1.  Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.

2.  Utilisez l’applet de commande **Update-CsAdminRole** pour mettre à jour les rôles de contrôle d’accès basé sur les rôles stockés dans le serveur de gestion central.
    
    <div>
    

    > [!NOTE]  
    > Aucune sortie n’est attendue, sauf s’il y a une erreur.

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

