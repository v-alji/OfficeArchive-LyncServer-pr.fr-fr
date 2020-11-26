---
title: 'Lync Server 2013 : affichage des informations de stratégie d’emplacement'
description: 'Lync Server 2013 : affichage des informations de stratégie d’emplacement.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing location policy information
ms:assetid: 14e41bcb-ea0a-49c2-99b3-1f61fc34416d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520954(v=OCS.15)
ms:contentKeyID: 48183489
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2fecc5de5fb71014a1641038e9e09afba0e90cdb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443957"
---
# <a name="viewing-location-policy-information-in-lync-server-2013"></a>Affichage des informations de stratégie d’emplacement dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-11-01_

Dans Lync Server 2013, vous pouvez utiliser la stratégie d’emplacement pour appliquer les paramètres relatifs à la fonctionnalité améliorée 9-1-1 (E9-1-1) et aux paramètres d’emplacement des utilisateurs ou des contacts. La stratégie d’emplacement détermine si un utilisateur est activé pour E9-1-1 et, si oui, le comportement d’un appel d’urgence. Par exemple, vous pouvez utiliser la stratégie d’emplacement pour définir le numéro constituant un appel d’urgence (par exemple, 911 aux États-Unis), si la sécurité d’entreprise doit être automatiquement notifiée et la manière dont l’appel doit être routé.

Vous pouvez configurer des stratégies d’emplacement à partir du groupe de **Configuration réseau** dans Lync Server 2013 Control Panel. Le panneau de configuration de Lync Server vous permet d’afficher, de créer, de modifier ou de supprimer des stratégies d’emplacement. Pour afficher des informations sur les stratégies d’emplacement, procédez comme suit. Pour plus d’informations sur la création ou la modification de stratégies d’emplacement, voir [création ou modification d’une stratégie d’emplacement dans Lync Server 2013](lync-server-2013-creating-or-modifying-a-location-policy.md).

<div>

## <a name="to-view-information-about-a-location-policy"></a>Pour afficher des informations sur une stratégie d’emplacement

1.  À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.

2.  Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server. Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis sur **stratégie d’emplacement**.

4.  Dans la page de **stratégie d’emplacement** , sélectionnez la stratégie d’emplacement que vous voulez modifier.

5.  Dans le menu **Edition**, cliquez sur **Afficher les détails**.
    
    <div>
    

    > [!NOTE]  
    > Vous pouvez uniquement afficher des informations sur une stratégie d’emplacement à la fois.

    
    </div>

Une stratégie unique, appelée global, existe par défaut et ne peut pas être supprimée ou renommée. Toutefois, vous pouvez modifier la stratégie globale. Ce paramètre s’applique à tous les utilisateurs et contacts, sauf si vous créez des stratégies de site ou des stratégies par utilisateur. Les stratégies par utilisateur doivent être appliquées à des utilisateurs spécifiques.

</div>

<div>

## <a name="see-also"></a>Voir aussi


[Création ou modification d’une stratégie d’emplacement dans Lync Server 2013](lync-server-2013-creating-or-modifying-a-location-policy.md)  
[Créer des stratégies d’emplacement dans Lync Server 2013](lync-server-2013-create-location-policies.md)  
[Création ou modification d’un site réseau dans Lync Server 2013](lync-server-2013-create-or-modify-a-network-site.md)  


[Nouveau-CsLocationPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsLocationPolicy)  
[Set-CsLocationPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsLocationPolicy)  
[Remove-CsLocationPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsLocationPolicy)  
[Get-CsLocationPolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsLocationPolicy)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

