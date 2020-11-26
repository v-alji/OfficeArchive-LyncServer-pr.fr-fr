---
title: 'Lync Server 2013 : Vérification de la conception de la topologie'
description: 'Lync Server 2013 : vérifier la conception topologique.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify the topology design
ms:assetid: c1b61814-239e-4101-aab0-de3db1d8793c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412951(v=OCS.15)
ms:contentKeyID: 48185311
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cb1e65343aacddbc11d3b909dfdff715503cab93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438910"
---
# <a name="verify-the-topology-design-in-lync-server-2013"></a>Vérification de la conception de la topologie dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-01-02_

Le générateur de topologie vérifie automatiquement la topologie. Toute erreur de topologie se caractérise par une erreur de validation, indiquée par l’icône d’erreur de validation située en regard du rôle de serveur. Il est important de vérifier également que la topologie représente correctement la topologie de votre déploiement.

<div>

## <a name="to-verify-the-topology-prior-to-publication"></a>Pour vérifier la topologie avant la publication

1.  Vérifiez que toutes les URL simples sont configurées correctement.

2.  Vérifiez que le serveur SQL Server est en ligne et que l’ordinateur sur lequel le Générateur de topologies est installé peut y accéder. Vérifiez également que les règles de pare-feu nécessaires sont disponibles.

3.  Vérifiez que le partage de fichiers est disponible et qu’il dispose des autorisations appropriées définies.

4.  Confirmez que les rôles serveur corrects qui répondent à la configuration requise pour le déploiement sont définis dans la topologie.

5.  Vérifiez que les serveurs existent dans les services de domaine Active Directory (AD FS). Ce problème se produit automatiquement si vous avez rejoint le domaine.

Lorsque vous avez vérifié la topologie et qu’aucune erreur de validation n’a été détectée, vous êtes prêt à publier la topologie. S’il existe des erreurs de validation, vous devez les corriger avant de pouvoir publier la topologie. Pour plus d’informations sur la publication de votre topologie, voir [publier la topologie dans Lync Server 2013](lync-server-2013-publish-the-topology.md).

</div>

</div>

<span> </span>

</div>

</div>

</div>

