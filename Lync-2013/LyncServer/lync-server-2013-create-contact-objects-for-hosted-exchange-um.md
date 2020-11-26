---
title: 'Lync Server 2013 : Création des objets de contact pour la messagerie unifiée Exchange hébergée'
description: 'Lync Server 2013 : création d’objets de contact pour le message unifié Exchange hébergé.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create contact objects for hosted Exchange UM
ms:assetid: a39be52f-488a-4523-ad5f-ce1f0d681959
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412765(v=OCS.15)
ms:contentKeyID: 48185045
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c9760e2a39b5182f9b5194e364e059bddc6a63d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431973"
---
# <a name="create-contact-objects-for-hosted-exchange-um-in-lync-server-2013"></a>Création des objets de contact pour la messagerie unifiée Exchange hébergée dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-09-24_

La procédure suivante vous explique comment créer des objets de contact de standard automatique (AA) ou d’accès d’abonné (SA) pour la messagerie unifiée Exchange hébergée.

Pour plus d’informations, reportez-vous à la rubrique [gestion des objets de contact Exchange hébergés dans Lync Server 2013](lync-server-2013-hosted-exchange-contact-object-management.md) dans la documentation de planification.

Pour plus d’informations sur la configuration des objets de contact, consultez la documentation Lync Server Management Shell pour les applets de commande suivantes :

  - [New-CsExUmContact](https://docs.microsoft.com/powershell/module/skype/New-CsExUmContact)

  - [Set-CsExUmContact](https://docs.microsoft.com/powershell/module/skype/Set-CsExUmContact)

<div class=" ">


> [!IMPORTANT]  
> Pour que les objets de contact Lync Server 2013 puissent être activés pour la messagerie unifiée Exchange hébergée, une stratégie de messagerie vocale hébergée qui s’applique à ces derniers doit être déployée. Pour plus d’informations, reportez-vous <A href="lync-server-2013-hosted-voice-mail-policies.md">à stratégies de messagerie vocale hébergées dans Lync Server 2013</A>.



</div>

<div>

## <a name="to-create-aa-or-sa-contact-objects-for-hosted-exchange-um"></a>Pour créer des objets de contact AA ou SA pour le UM Exchange hébergé

1.  Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.

2.  Exécutez l’applet de demande New-CsExUmContact pour créer des objets de contact requis pour votre déploiement. Par exemple, exécutez la commande suivante pour créer un objet de contact AA et son :
    
       ```powershell
        New-CsExUmContact -SipAddress "sip:exumaa1@fabrikam.com" -RegistrarPool "RedmondPool.litwareinc.com" -OU "HostedExUM Integration" -DisplayNumber "+14255550101" -AutoAttendant $True
       ```
    
       ```powershell
        New-CsExUmContact -SipAddress "sip:exumsa1@fabrikam.com" -RegistrarPool "RedmondPool.litwareinc.com" -OU "HostedExUM Integration" -DisplayNumber "+14255550101"
       ```
    
    Ces exemples définissent les paramètres suivants :
    
      - **SipAddress** spécifie l’adresse SIP de l’objet contact. Il doit s’agir d’une adresse qui n’a pas encore été utilisée pour configurer un objet utilisateur ou contact dans les services de domaine Active Directory (AD FS). Cette valeur doit être au format "SIP : \<*SIP address*\> " comme le montre l’exemple précédent.
    
      - **RegistrarPool** spécifie le nom de domaine complet (FQDN) du pool sur lequel le service de bureau d’enregistrement est en cours d’exécution.
        
        <div class=" ">
        

        > [!NOTE]  
        > Les objets de contact de MU Exchange ne peuvent pas être déplacés vers des pools qui font partie des déploiements Lync Server 2013 antérieurs à Lync Server 2013.

        
        </div>
    
      - **UO** spécifie l’unité d’organisation Active Directory dans laquelle se trouve l’objet contact.
    
      - **DisplayNumber** spécifie le numéro de téléphone de l’objet contact. Le numéro de téléphone de chaque objet contact doit être unique.
    
      - Le **standard automatique indique si** l’objet contact est un standard automatique. Le standard automatique propose un ensemble d’invites vocales permettant aux appelants de naviguer dans le système téléphonique et de joindre la partie qu’ils souhaitent contacter. La valeur **false** (valeur par défaut) pour ce paramètre indique un objet contact d’accès abonné.

</div>

</div>

<span> </span>

</div>

</div>

</div>

