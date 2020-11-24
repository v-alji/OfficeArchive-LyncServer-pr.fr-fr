---
title: 'Lync Server 2013 : Vérification de la connectivité pour les utilisateurs externes'
description: 'Lync Server 2013 : vérifier la connectivité pour les utilisateurs externes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify connectivity for external users
ms:assetid: 5c02bd6e-1c96-448a-a21d-58c9961c6640
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398402(v=OCS.15)
ms:contentKeyID: 48184249
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 50ef728157d01b93e7d0b8420442ce083a42b5b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395045"
---
# <a name="verify-connectivity-for-external-users-in-lync-server-2013"></a>Vérification de la connectivité pour les utilisateurs externes dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-19_

La validation de la connectivité des utilisateurs externes nécessite de garantir la connectivité des utilisateurs au serveur et au port du service Edge d’accès.

Pour confirmer votre configuration et la possibilité de vous connecter, d’envoyer et de recevoir les messages appropriés pour les scénarios requis par l’accès des utilisateurs externes est le site de l’analyseur de connectivité à distance ( <http://www.testocsconnectivity.com> ). Le site est géré et entretenu par le support technique de Microsoft. Pour accéder à l’analyseur de connectivité à distance, ouvrez le site Web dans un navigateur et suivez les instructions pour sélectionner le scénario.

<div>

## <a name="test-connectivity-of-external-users-and-external-access"></a>Tester la connectivité des utilisateurs externes et des accès externes

Les tests pour l’accès utilisateur externe doivent inclure chaque type d’utilisateur externe pris en charge par votre organisation, y compris tout ou partie des éléments suivants :

  - Utilisateurs d’au moins un domaine fédéré et test de la messagerie instantanée, de la présence, de A/V et du partage de bureau.

  - Utilisateurs de chaque fournisseur de services de messagerie instantanée publique pris en charge par votre organisation (et pour lesquels la mise en service est terminée).

  - Utilisateurs anonymes.

  - Les utilisateurs de votre organisation qui sont connectés à Lync à distance, mais qui ne l’utilisent pas.

Ces tests déterminent si votre serveur Edge est :

  - Écoute sur les ports requis à l’aide d’un client telnet depuis l’extérieur de votre réseau.
    
      - Exemple : Telnet sip.contoso.com 443
    
      - Effectuez le test précédent sur les ports que vous utilisez sur le serveur Edge ou le pool de serveurs Edge en fonction de votre déploiement.

  - Effectuer une résolution DNS externe précise.
    
      - Depuis l’extérieur de votre réseau, effectuez un test ping sur chacun des FQDN externes de votre pool Edge ou Edge. Même si le test échoue, vous verrez les adresses IP, que vous pouvez comparer à celles que vous avez affectées.

</div>

</div>

<span> </span>

</div>

</div>

</div>

