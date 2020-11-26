---
title: 'Lync Server 2013 : Création ou modification des fournisseurs fédérés SIP hébergés'
description: 'Lync Server 2013 : créez ou modifiez des fournisseurs fédérés SIP hébergés.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or edit hosted SIP federated providers
ms:assetid: 0dd6dcb6-a88d-46b8-9c96-b35967309bcd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552445(v=OCS.15)
ms:contentKeyID: 48679556
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aaaa1b29b9a85332b85dfb7a1f258503fa4e9c77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431903"
---
# <a name="create-or-edit-hosted-sip-federated-providers-lync-server-2013"></a>Création ou modification des fournisseurs fédérés SIP hébergés dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-19_

La connectivité de messagerie instantanée du fournisseur hébergé permet aux utilisateurs de votre organisation d’utiliser la messagerie instantanée pour communiquer avec les utilisateurs de services de messagerie instantanée proposés par des fournisseurs hébergés, notamment Microsoft 365 et Lync Online.

Chaque fournisseur hébergé est configuré à l’aide du nom de domaine complet du serveur Edge du fournisseur, et le niveau de vérification par défaut **permet aux utilisateurs de communiquer uniquement avec des personnes de leur liste de contacts qui utilisent ce fournisseur**.

Pour créer ou modifier des fournisseurs hébergés, procédez comme suit :

<div>

## <a name="to-create-or-edit-hosted-providers"></a>Pour créer ou modifier des fournisseurs hébergés

1.  À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.

2.  Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server. Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Dans la barre de navigation de gauche, cliquez sur **Fédération et accès externe**, puis sur **fournisseurs fédérés SIP**.

4.  Si vous avez besoin de créer un nouveau fournisseur hébergé, cliquez sur **nouveau** , puis cliquez sur **fournisseur hébergé**.

5.  Si vous avez besoin de modifier une entrée de la liste des fournisseurs hébergés, sélectionnez un fournisseur hébergé, cliquez sur **modifier**, puis sur **afficher les détails**.

6.  Dans la page **modifier le fournisseur fédéré SIP** , vous pouvez taper ou modifier les paramètres suivants :
    
      - **Activer les communications avec ce fournisseur**   Ce paramètre permet de communiquer avec les utilisateurs de ce fournisseur.
    
      - **Nom du fournisseur :**   Une propriété requise, tapez le nom du fournisseur tel qu’il sera reflété dans la liste des fournisseurs fédérés SIP.
    
      - **Service Edge d’accès (FQDN) :**   Une propriété requise, tapez le nom de domaine complet du service Edge d’accès du fournisseur hébergé que vous configurez. Ces informations doivent être fournies par le fournisseur hébergé et ne doivent être changées que si le fournisseur hébergé apporte une modification au FQDN du service Edge d’accès au fournisseur hébergé.
    
      - **Niveau de vérification par défaut :**   Le paramètre par défaut, **permettre aux utilisateurs de communiquer avec des personnes de leur liste de contacts qui utilisent ce fournisseur** , limite la communication aux contacts que vous avez acceptés et qui figurent dans votre liste de contacts.
        
        Sélectionner **permettre aux utilisateurs de communiquer avec tout le monde à l’aide de ce fournisseur** supprime la restriction que vous devez avoir reçu et accepté une invitation de contact. Ce paramètre ne limite pas qui peut vous contacter à partir du réseau du fournisseur hébergé.

7.  Lorsque vous avez configuré les paramètres, cliquez sur **valider** pour enregistrer ou cliquez sur **Annuler** pour ignorer vos modifications.

</div>

<div>

## <a name="see-also"></a>Voir aussi


[Configuration des stratégies de contrôle d’accès des utilisateurs publics dans Lync Server 2013](lync-server-2013-configure-policies-to-control-public-user-access.md)  
[Activation ou désactivation de la fédération et de la connectivité PIC dans Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

