---
title: 'Lync Server 2013 : Modification ou configuration des URL simples'
description: 'Lync Server 2013 : modifiez ou configurez des URL simples.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Edit or configure simple URLs
ms:assetid: 0008aeea-4ae9-4e36-83cd-ef7ff7b6e128
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398063(v=OCS.15)
ms:contentKeyID: 48183216
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f9152a65083f71510f4cdb1189b3982afdd68b4c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393784"
---
# <a name="edit-or-configure-simple-urls-in-lync-server-2013"></a>Modification ou configuration des URL simples dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2014-02-04_

Cette procédure ne nécessite pas d’appartenance à un administrateur local ou à un groupe de domaines privilégiés. Vous devez vous connecter à un ordinateur en tant qu’utilisateur standard.

Lync Server 2013 utilise des URL simples pour diriger les appels internes et externes vers des services du serveur frontal ou du réalisateur, s’il a été déployé. Pour plus d’informations sur les URL simples, voir [planification d’URL simples dans Lync Server 2013](lync-server-2013-planning-for-simple-urls.md) dans la documentation de planification. Vous pouvez sélectionner le format de vos URL simples à partir de plusieurs options. Pour plus d’informations sur ces options, voir [configurations DNS requises pour les URL simples dans Lync Server 2013](lync-server-2013-dns-requirements-for-simple-urls.md) dans la documentation de planification.

Par défaut, les URL simples seront configurées sous la forme (par exemple, l’URL de connexion simple) : https://dialin .\<SIP Domain\>

<div>

## <a name="to-configure-simple-urls"></a>Pour configurer des URL simples

1.  Dans le générateur de topologie, cliquez avec le bouton droit sur le nœud du **serveur Lync** , puis cliquez sur **modifier les propriétés**.

2.  Dans le volet **URL simples**, sélectionnez **URL d’accès téléphonique :** (Dial-In) ou **URL de réunion :** (Meet) pour modifier l’URL, puis cliquez sur **Modifier l’URL**.

3.  Mettez à jour l’URL comme vous le souhaitez puis cliquez sur **OK** pour enregistrer l’URL modifiée. L’exemple présenté ici a modifié l’URL d’accès à la Conférence rendez-vous en https://pool01.contoso.net/dialin .

4.  Modifiez l’URL Meet en procédant de la même manière, si nécessaire.

</div>

<div>

## <a name="to-define-the-optional-admin-simple-url"></a>Pour définir l’URL simple Admin facultative

1.  Dans le générateur de topologie, cliquez avec le bouton droit sur le nœud du **serveur Lync** , puis cliquez sur **modifier les propriétés**.

2.  Dans la zone **URL d’accès administratif** , entrez l’URL de votre choix pour l’accès administratif au panneau de configuration de Lync Server 2013, puis cliquez sur **OK**.
    
    <div>
    

    > [!TIP]  
    > Nous vous recommandons d’utiliser l’URL la plus simple possible pour l’URL d’administration. L’option la plus simple est <STRONG> https://admin .</STRONG> &lt; Domain (domaine) &gt; .

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > Si vous changez une URL simple après son déploiement initial, vous devez savoir quels changements impactent vos enregistrements et certificats DNS pour les URL simples. Si le changement a un impact sur la base d’une URL simple, vous devez également modifier les enregistrements DNS et les certificats. Par exemple, https://lync.contoso.com/Meet https://meet.contoso.com si vous modifiez l’URL de base de lync.contoso.com à Meet.contoso.com, vous devez modifier les enregistrements DNS et les certificats pour faire référence à Meet.contoso.com. Si vous avez changé l’URL simple de https://lync.contoso.com/Meet à https://lync.contoso.com/Meetings , l’URL de base de Lync.contoso.com reste inchangée et aucune modification du DNS ou du certificat n’est nécessaire. Néanmoins, chaque fois que vous modifiez un nom d’URL simple, vous devez exécuter l’applet de passe <STRONG>Enable-CsComputer</STRONG> sur chaque réalisateur et serveur frontal pour enregistrer la modification.

    
    </div>

</div>

<div>

## <a name="see-also"></a>Voir aussi


[Planification des URL simples dans Lync Server 2013](lync-server-2013-planning-for-simple-urls.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

