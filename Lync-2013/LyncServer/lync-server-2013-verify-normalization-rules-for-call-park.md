---
title: 'Lync Server 2013 : vérifier les règles de normalisation du parc d’appels'
description: 'Lync Server 2013 : vérifier les règles de normalisation du parc d’appels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify normalization rules for Call Park
ms:assetid: deaa170f-041e-45cb-8eab-f02931ab541e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398981(v=OCS.15)
ms:contentKeyID: 48185646
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2ac4c15091141e3069e7b77533d0e4148459f570
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395033"
---
# <a name="verify-normalization-rules-for-call-park-in-lync-server-2013"></a>Vérifier les règles de normalisation du parc d’appels dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-09-11_

Le parking des orbites ne doit pas être normalisé. Vérifiez dans vos plans de numérotation que vos numéros orbites ne sont pas normalisés. Si vous devez créer une règle de normalisation supplémentaire pour empêcher la normalisation de vos orbites, suivez la procédure décrite dans la rubrique [créer un plan de numérotation dans Lync Server 2013](lync-server-2013-create-a-dial-plan.md) pour définir une nouvelle règle de normalisation, afin que le **modèle correspondant** identifie la plage d’orbite et le **modèle de traduction** est **$1**. Par exemple, si la plage de votre stationnement d’appels est 7000 – 7999, le **modèle à faire correspondre** est **^ (7 \\ d {3} ) $** et le **modèle de traduction** est **$1**.

<div>


> [!IMPORTANT]  
> Vérifiez que la règle de normalisation par défaut de vos plans de numérotation ne contient pas l’élément <STRONG>^(\d*)</STRONG>. Dans le cas contraire, votre règle de normalisation de parc d’appels ne sera jamais exécutée.



</div>

<div>

## <a name="see-also"></a>Voir aussi


[Créer un plan de numérotation dans Lync Server 2013](lync-server-2013-create-a-dial-plan.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

