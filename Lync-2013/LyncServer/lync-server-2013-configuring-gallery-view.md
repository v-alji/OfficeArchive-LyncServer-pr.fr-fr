---
title: 'Lync Server 2013 : configuration de l’affichage Galerie'
description: 'Lync Server 2013 : configuration de l’affichage Galerie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Gallery View
ms:assetid: 4a609178-47d8-4682-ac8d-29f882801924
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204871(v=OCS.15)
ms:contentKeyID: 48184069
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2aec2f1e3c7bff9a3736f40584a29880978b9daa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433093"
---
# <a name="configuring-gallery-view-in-lync-server-2013"></a>Configurer le mode Galerie dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-30_

Dans Lync Server 2013, vous configurez la conférence vidéo d’affichage de la galerie dans la stratégie de conférence. L’option vue Galerie est activée par défaut. Si vous ne voulez pas autoriser le mode Galerie, ou si vous voulez l’autoriser pour certains utilisateurs, vous devez désactiver la fonctionnalité dans la stratégie de conférence.

Lorsque la vidéo d’un participant à la Conférence n’est pas disponible, il est possible d’améliorer l’affichage de la Galerie de la Galerie des utilisateurs si vous déployez des photos haute résolution, une nouvelle fonctionnalité dans Lync Server 2013. Les photos haute résolution constituent une alternative aux photos de contact plus petites et limitées stockées dans les services de domaine Active Directory (AD FS). Les photos haute résolution sont stockées dans la boîte aux lettres Exchange 2013 d’un utilisateur et nécessitent donc l’intégration de Lync Server 2013 avec Exchange 2013. Pour plus d’informations, consultez l’article de blog NextHop intitulé « intégration d’Exchange 2013 et Lync Server 2013 » [https://go.microsoft.com/fwlink/p/?LinkId=260987](https://go.microsoft.com/fwlink/p/?linkid=260987) .

<div>


> [!NOTE]  
> Le contenu des blogs et leurs URL peuvent être modifiés sans préavis.



</div>

Vous pouvez afficher ou modifier les paramètres d’affichage de la galerie en utilisant le panneau de configuration de Lync Server 2013 ou en utilisant l’une des applets de commande suivantes :

  - **Get-CsConferencingPolicy**

  - **Set-CsConferencingPolicy**

  - **New-CsConferencingPolicy**

Configurer le mode Galerie avec les paramètres de stratégie de conférence suivants :

  - **AllowMultiview**   Ce paramètre indique si un utilisateur est autorisé à organiser des conférences vidéo d’affichage Galerie. Ce paramètre s’applique aux réunions planifiées et ponctuelles créées par l’utilisateur.
    
    Donnés
    
      - Ce paramètre est défini sur true pour l’utilisateur A qui est hébergé sur un pool Lync Server 2013. Réunions organisées par l’utilisateur permet aux utilisateurs de joindre et de recevoir plusieurs flux vidéo.
    
      - Ce paramètre est défini sur false pour l’utilisateur B, qui est hébergé sur un pool Lync Server 2013. Les réunions organisées par l’utilisateur B sont dotées d’un flux vidéo unique qui est semblable à l’interface de visioconférence fournie par Lync Server 2010.
    
    Ce paramètre détermine qui peut organiser des réunions qui autorisent plusieurs flux vidéo. Les participants à des réunions qui autorisent plusieurs flux vidéo peuvent, ou ne peuvent pas être autorisés à recevoir plusieurs flux vidéo, en fonction de leurs autorisations individuelles (voir la description du paramètre EnableMultiviewJoin).

  - **EnableMultiviewJoin**   Ce paramètre détermine si un participant à une réunion reçoit l’interface vidéo d’affichage de la galerie dans les réunions qui le permettent. Ce paramètre contrôle l’utilisation de l’utilisateur dans les réunions auxquelles il participe.
    
    Donnés
    
      - Ce paramètre est défini sur true pour l’utilisateur C. l’utilisateur c peut recevoir plusieurs flux vidéo lorsque vous participez à une réunion organisée ou démarrée par l’utilisateur A. l’utilisateur dispose d’un flux vidéo unique similaire à l’interface de visioconférence fournie 2010 par l’utilisateur B.
    
      - Ce paramètre est défini sur false pour l’utilisateur D. User d reçoit un flux vidéo unique qui est semblable à l’interface de visioconférence fournie par Lync Server 2010 lors de la participation à une réunion organisée par l’utilisateur A ou par l’utilisateur B.

Vous trouverez ci-dessous un exemple d’utilisation de Lync Server Management Shell pour activer la vidéoconférence d’affichage Galerie.

<div>

## <a name="to-modify-conferencing-policy-for-gallery-view-video-conferencing"></a>Pour modifier la stratégie de conférence pour les conférences vidéo sur l’affichage Galerie

1.  Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.

2.  Dans la ligne de commande, exécutez l’applet de commande suivante pour modifier la stratégie de conférence :
    
        Set-CsConferencingPolicy -Identity Pool01ConferencingPolicy -AllowMultiview $true -EnableMultiviewJoin $true 

</div>

</div>

<span> </span>

</div>

</div>

</div>

