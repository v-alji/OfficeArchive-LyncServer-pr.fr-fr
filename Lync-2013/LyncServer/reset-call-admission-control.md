---
title: Réinitialisation du contrôle d’admission des appels
description: Réinitialiser le contrôle d’admission des appels.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Reset call admission control
ms:assetid: 5873f56c-f3d6-4d73-beea-c9f37d5077f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688064(v=OCS.15)
ms:contentKeyID: 49733658
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c4539cda453de6249be3a9b9b61521ecf478cb70
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443621"
---
# <a name="reset-call-admission-control"></a>Réinitialisation du contrôle d’admission des appels

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-11_

Si un pool frontal de Lync Server 2010 est en cours d’hébergement par le biais du contrôle d’admission des appels (CAC), vous devez déplacer l’hébergement CAC vers un pool Lync Server 2013 avant de pouvoir supprimer le pool frontal de Lync Server 2010.

<div>

## <a name="to-reset-cac"></a>Pour réinitialiser le CAC

1.  Ouvrez le générateur de topologie.

2.  Cliquez avec le bouton droit sur le nœud site, puis cliquez sur **modifier les propriétés**.

3.  Sous **paramètre de contrôle d’admission des appels**, assurez-vous que l’option **activer le contrôle d’admission des appels** est activée.

4.  Sous **pool frontal pour exécuter le contrôle d’admission des appels (CAC)**, sélectionnez le pool Lync Server 2013 à hôte CAC, puis cliquez sur **OK**.

5.  Publiez la topologie.

</div>

</div>

<span> </span>

</div>

</div>

</div>

