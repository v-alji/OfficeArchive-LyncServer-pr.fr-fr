---
title: 'Lync Server 2013 : composants utilisés par le prélèvement d’appels de groupe'
description: 'Lync Server 2013 : composants utilisés par le prélèvement d’appels de groupe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Group Call Pickup
ms:assetid: 45db2f23-d486-4b20-a8cf-7b48a1f9fd3a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945625(v=OCS.15)
ms:contentKeyID: 51541470
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 517f75dcbac8bfed0e749c061a9696b7667e10ed
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394209"
---
# <a name="components-used-by-group-call-pickup-in-lync-server-2013"></a>Composants utilisés par le prélèvement d’appels de groupe dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-01-30_

La prise d’appel de groupe est déployée automatiquement lors du déploiement de l’application voix entreprise et de l’application de parc d’appels. Vous pouvez activer le prélèvement d’appels de groupe en configurant la table orbite du parc d’appels avec des plages de numéros distinctes désignés comme numéros de groupe de capture d’appel, puis en attribuant aux utilisateurs la possibilité d’appeler les groupes de capture et en permettant aux utilisateurs de procéder à un appel de groupe. Les composants Lync Server suivants prennent en charge la cueillette des appels de groupe :

  - **Service d’application**   Le service d’application fournit une plateforme de déploiement, d’hébergement et de gestion d’applications de communications unifiées, telles que l’application de parc d’appels. Le service d’application est automatiquement installé sur chaque serveur frontal d’une grappe frontale et sur tous les serveurs Standard Edition Server.

  - **Application de parc d’appels**   L’application de parc d’appels est l’une des applications de communications unifiées hébergées par le service d’application. Le prélèvement d’appels de groupe est basé sur l’application de parc d’appels.

  - **Lync Server Management Shell**   Vous utilisez Lync Server Management Shell pour gérer les groupes de capture d’appels de groupe.

  - **Outil du kit de ressources SEFAUtil**   Vous pouvez utiliser l’utilitaire d’activation de fonctionnalité d’extension secondaire (SEFAUtil) pour attribuer des utilisateurs à un groupe de capture d’appel et activer ou désactiver le prélèvement d’appels pour les utilisateurs.

</div>

<span> </span>

</div>

</div>

</div>

