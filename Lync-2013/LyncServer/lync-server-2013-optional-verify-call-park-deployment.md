---
title: 'Lync Server 2013 : (facultatif) vérifier le déploiement du parc d’appels'
description: 'Lync Server 2013 : (facultatif) Vérifiez le déploiement du parc d’appels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Verify Call Park deployment
ms:assetid: fcfe0962-1a9c-4cbd-847c-fed40e3b1480
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413076(v=OCS.15)
ms:contentKeyID: 48185952
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 772392a3a791ed57c3220d80e9bd510d8803debb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424862"
---
# <a name="optional-verify-call-park-deployment-in-lync-server-2013"></a>Facultatif Vérifier le déploiement du parc d’appels dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-09-11_

Après l’installation et la configuration du parc d’appels, vous devez vérifier la configuration pour vous assurer que le parking et la récupération des appels fonctionnent comme prévu. Vérifiez au minimum les éléments suivants :

  - Appeler un utilisateur dont le parc d’appels est activé et demander à l’utilisateur d’appeler l’appel.
    
    <div>
    

    > [!NOTE]  
    > Si vous avez activé le parc d’appels dans la politique vocale juste avant d’effectuer ce test, l’utilisateur qui travaille en stationnement doit se déconnecter de Lync Server, puis se reconnecter pour pouvoir voir l’option de transfert d’appel dans la liste transférer l’appel.

    
    </div>

  - Composez le numéro orbite pour récupérer l’appel.

  - Parquez un autre appel, laissez expirer le délai d’attente de l’appel parqué et ne décrochez pas lors du rappel. Vérifiez que l’appel dont le délai d’attente a expiré est routé correctement vers la destination secondaire spécifiée pour **OnTimeoutURI**.

</div>

<span> </span>

</div>

</div>

</div>

