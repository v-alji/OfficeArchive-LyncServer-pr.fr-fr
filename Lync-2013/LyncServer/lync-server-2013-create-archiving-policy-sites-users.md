---
title: 'Lync Server 2013 : création d’une stratégie d’archivage pour activer ou désactiver l’archivage des communications internes ou externes pour des sites ou des utilisateurs spécifiques'
description: 'Lync Server 2013 : création d’une stratégie d’archivage pour activer ou désactiver l’archivage des communications internes ou externes pour des sites ou des utilisateurs spécifiques.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating an Archiving policy to enable or disable Archiving of internal or external communications for specific sites or users
ms:assetid: 5864793a-ba72-470c-bb5b-9fb41e968896
ms:mtpsurl: https://technet.microsoft.com/library/Gg398385(v=OCS.15)
ms:contentKeyID: 48184193
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a23f952229df9fe950f2666914263a7cf46595f4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431987"
---
# <a name="creating-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-specific-sites-or-users"></a>Création d’une stratégie d’archivage dans Lync Server 2013 pour activer ou désactiver l’archivage des communications internes ou externes pour des sites ou des utilisateurs spécifiques

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-23_

Dans Lync Server 2013, vous utilisez des stratégies pour activer et désactiver l’archivage des communications internes et des communications externes pour les utilisateurs hébergés sur Lync Server 2013. Cela inclut les stratégies d’archivage suivantes :

  - Stratégie globale créée par défaut lors du déploiement de Lync Server 2013.

  - Stratégies de niveau de site et de niveau utilisateur facultatives que vous pouvez créer et utiliser pour spécifier la façon dont l’archivage est implémenté pour des sites ou des utilisateurs spécifiques.

Vous définissez initialement des stratégies d’archivage lors du déploiement de l’archivage, mais vous pouvez modifier, ajouter et supprimer des stratégies après le déploiement. Dans Lync Server 2013 panneau de configuration, vous pouvez utiliser la page de **stratégie d’archivage** du groupe **archivage et surveillance** pour gérer les stratégies au niveau global, au niveau du site et au niveau de l’utilisateur. Si vous intégrez le stockage de votre serveur Lync au stockage 2013 Exchange, les stratégies d’utilisateur Exchange sont prioritaires sur les stratégies d’archivage de Lync Server 2013.

Pour plus d’informations sur l’implémentation de stratégies, y compris la hiérarchie des stratégies, voir fonctionnement [de l’archivage dans Lync Server 2013](lync-server-2013-how-archiving-works.md) dans la documentation de planification, la documentation de déploiement ou les opérations.

<div>


> [!NOTE]
> Pour contrôler l’implémentation de l’archivage, vous devez spécifier les options de configuration de l’archivage, par exemple pour archiver les messages instantanés ou les conférences, utiliser le mode Critical et les options de purge. Par défaut, aucune option n’est activée dans la configuration de l’archivage global ni dans toute configuration d’archivage de site ou de pool. Vous devez spécifier toutes les options appropriées dans les configurations d’archivage avant de procéder à l’archivage des communications internes ou externes dans les stratégies d’archivage. Pour plus d’informations, reportez-vous à <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">la section gestion des options de configuration de l’archivage dans Lync Server 2013 pour votre organisation, vos sites et vos pools</A> dans la documentation des opérations.<BR>Si vous avez activé l’intégration de Microsoft Exchange pour votre déploiement, les stratégies Exchange contrôlent la mise en place de l’archivage pour les utilisateurs hébergés sur Exchange 2013 et disposant de leurs boîtes aux lettres dans In-Place attente. Pour plus d’informations, reportez-vous à la rubrique <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">configuration de stratégies d’archivage dans Lync server 2013 lors de l’utilisation d’une intégration Exchange Server</A> dans la documentation de déploiement.



</div>

<div>

## <a name="to-create-an-archiving-policy-for-a-site-or-users"></a>Pour créer une stratégie d’archivage pour un site ou des utilisateurs

1.  À partir d’un compte d’utilisateur auquel est affecté un des rôles CsArchivingAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.

2.  Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server. Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Dans la barre de navigation gauche, cliquez sur **surveillance et archivage**, puis cliquez sur **stratégie d’archivage**.

4.  Cliquez sur **Nouveau**, puis effectuez l’une des opérations suivantes :
    
      - Pour créer une stratégie d’archivage au niveau du site, cliquez sur **stratégie de site** , puis dans **Sélectionner un site**, cliquez sur le site auquel vous voulez appliquer la stratégie.
    
      - Pour créer une stratégie d’archivage au niveau de l’utilisateur, cliquez sur **Stratégie de l’utilisateur**.

5.  Dans **Nouvelle stratégie d’archivage**, procédez comme suit :
    
      - Dans **Nom**, spécifiez un nom pour la nouvelle stratégie (par exemple, externalContoso).
    
      - Dans **Description**, entrez des informations décrivant la stratégie (par exemple, stratégie d’archivage des utilisateurs externes pour Contoso).
    
      - Pour contrôler l’archivage des communications avec les utilisateurs internes, activez ou désactivez la case à cocher **Archiver les communications internes**.
    
      - Pour contrôler l’archivage des communications avec les utilisateurs externes, activez ou désactivez la case à cocher **Archiver les communications externes**.

6.  Cliquez sur **Valider**.
    
    <div>
    

    > [!IMPORTANT]
    > Les paramètres d’une stratégie utilisateur ne s’appliquent qu’aux utilisateurs et groupes d’utilisateurs spécifiques pour lesquels la stratégie a été définie. Pour plus d’informations, reportez-vous <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">à appliquer une stratégie d’archivage aux utilisateurs de Lync Server 2013</A>

    
    </div>

</div>

<div>

## <a name="creating-an-archiving-policy-by-using-windows-powershell-cmdlets"></a>Création d’une stratégie d’archivage à l’aide d’applets de cmdlet Windows PowerShell

Les stratégies d’archivage peuvent être créées à l’aide de Windows PowerShell et de l’applet de passe **Remove-CsArchivingPolicy** . Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell. Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-create-a-new-archiving-policy-at-the-site-scope"></a>Pour créer une nouvelle stratégie d’archivage à l’étendue du site

  - Cette commande crée une stratégie d’archivage pour le site Redmond :
    
        New-CsArchivingPolicy -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-per-user-scope"></a>Pour créer une nouvelle stratégie d’archivage à l’étendue de chaque utilisateur

  - Pour créer une nouvelle stratégie d’archivage à l’étendue par utilisateur, spécifiez simplement une identité unique lors de la création de la stratégie :
    
        New-CsArchivingPolicy -Identity "RedmondArchivingPolicy"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-internal-communication-sessions"></a>Pour créer une nouvelle stratégie d’archivage qui permet d’archiver des sessions de communication interne

  - Dans la mesure où aucun paramètre (à l’exception du paramètre obligatoire Identity) n’a été spécifié dans les commandes précédentes, les nouvelles stratégies utilisent les valeurs par défaut pour toutes leurs propriétés. Pour créer des stratégies qui utilisent des valeurs de propriétés distinctes, il vous suffit d’inclure le paramètre et la valeur de paramètre appropriés. Par exemple, pour créer une stratégie d’archivage qui permet l’archivage des sessions de messagerie instantanée internes, utilisez une commande comme celle-ci :
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-both-internal-and-external-communication-sessions"></a>Pour créer une nouvelle stratégie d’archivage qui permet d’archiver des sessions de communication interne et externe

  - Vous pouvez modifier plusieurs valeurs de propriétés en incluant plusieurs paramètres. Par exemple, cette commande configure la nouvelle stratégie d’archivage des sessions de messagerie instantanée internes et externes :
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True -ArchiveExternal $True

</div>

Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de [nouvelle-CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) .

</div>

<div>

## <a name="see-also"></a>Voir aussi


[Gestion de l’archivage des communications internes et externes dans Lync Server 2013](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

