---
title: 'Lync Server 2013 : Planification des déploiements hybrides'
description: 'Lync Server 2013 : Planification des déploiements hybrides.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for hybrid deployments
ms:assetid: f8b3d240-bc2e-42c9-acf8-d532d641a14c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205403(v=OCS.15)
ms:contentKeyID: 48185910
ms.date: 05/25/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 919f6058059fc9bfcb6bcb4f4c38140e53be6274
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424547"
---
# <a name="planning-for-lync-server-2013-hybrid-deployments"></a>Planification des déploiements hybrides Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Rubrique dernière modification :** 2016-05-25_

Vous devez tenir compte des exigences suivantes pour les utilisateurs et votre infrastructure réseau lors de la planification d’un déploiement hybride.

<div>

## <a name="infrastructure-requirements"></a>Conditions requises pour l’infrastructure

Pour implémenter et déployer un déploiement hybride, vous devez configurer les configurations suivantes dans votre environnement.

  - Organisation Microsoft 365 ou Office 365 avec Skype Entreprise Online activé. Notez que vous ne pouvez utiliser qu’un seul client pour une configuration hybride avec votre déploiement local.

  - Un seul déploiement local (infrastructure) de Skype Entreprise Server ou de Lync Server déployé dans une topologie prise en charge. Consultez la topologie requise.
    
    Pour plus d’informations sur la configuration de votre déploiement Lync Server 2013 ou Lync Server 2010 pour un déploiement hybride, voir Configuration des [déploiements hybrides de Lync Server 2013.](lync-server-2013-configuring-hybrid-deployments.md)

  - Outils d’administration Skype Entreprise Server 2015. Si vous utilisez Lync Server 2013 ou Lync Server 2010, vous pouvez utiliser les outils d’administration de Lync Server 2013.

  - Pour prendre en charge l’authentification unique avec Microsoft 365 ou Office 365, afin que les utilisateurs peuvent utiliser les mêmes informations d’identification pour se connecter à Office et pour se connecter en local, vous pouvez utiliser les fonctionnalités de synchronisation des mots de passe d’Azure Active Directory (AAD) Connect. Vous pouvez également utiliser les services AD FS (Active Directory Federation Services) pour l' sign-on unique avec Microsoft 365 ou Office 365.
    
    Pour plus d’informations, voir Intégration de vos [identités locales avec Azure Active Directory.](https://go.microsoft.com/fwlink/p/?linkid=619754)

  - Une solution de synchronisation d’annuaires unique pour assurer la synchronisation de vos objets Active Directory locaux et en ligne. Pour plus d’informations sur la synchronisation d’annuaires, voir [Outils d’intégration d’annuaire.](https://go.microsoft.com/fwlink/p/?linkid=530320)

</div>

<div>

## <a name="lync-client-support"></a>Lync Client Support

Il existe des différences entre les fonctionnalités pris en charge dans les clients Lync, ainsi que dans les fonctionnalités disponibles dans les environnements locaux et en ligne. Avant de choisir l’emplacement où vous souhaitez home les utilisateurs dans votre organisation, vous pouvez consulter le support client pour les différentes configurations de Lync Server. Les clients suivants sont pris en charge avec Skype Entreprise Online dans un déploiement hybride Lync :

  - Lync 2010

  - Lync 2013

  - application Lync du Windows Store

  - Lync Web App

  - Lync Mobile

  - Lync pour Mac 2011

  - Lync Room System

  - Lync Basic 2013

Pour plus d’informations sur le support client, voir les rubriques suivantes :

  - [Clients pour Lync Online](https://go.microsoft.com/fwlink/?linkid=281902)

  - [Tableau de comparaison des clients pour Lync Server 2013](lync-server-2013-desktop-client-comparison-tables.md)

  - [Tableau de comparaison des clients mobiles pour Lync Server 2013](lync-server-2013-mobile-client-comparison-tables.md)

</div>

<span id="BKMK_Topology"></span>

<div>

## <a name="topology-requirements"></a>Conditions requises pour la topologie

Pour configurer votre déploiement pour un déploiement hybride avec Skype Entreprise Online, l’une des topologies suivantes doit être prise en charge :

  - Déploiement de Skype Entreprise Server 2015 avec tous les serveurs exécutant Skype Entreprise Server 2015.

  - Déploiement de Lync Server 2013 avec tous les serveurs exécutant Lync Server 2013.

  - Un déploiement Lync Server 2010 avec tous les serveurs exécutant Lync Server 2010 avec les dernières mises à jour cumulatives.
    
      - Le serveur Edge de fédération et le serveur du saut suivant à partir du serveur Edge de fédération doivent exécutent Lync Server 2010 avec les dernières mises à jour cumulatives.
    
      - Les outils d’administration de Skype Entreprise Server 2015 ou Lync Server 2013 doivent être installés sur au moins un serveur ou une station de travail de gestion.

  - Déploiement mixte de Lync Server 2013 et de Skype Entreprise Server 2015 avec les rôles de serveur suivants sur au moins un site exécutant Skype Entreprise Server 2015 :
    
      - Au moins un pool d'entreprise ou serveur Standard Edition 
    
      - Pool directeur associé à la fédération SIP, le cas échéant
    
      - Pool Edge associé à la fédération SIP

  - Déploiement mixte de Lync Server 2010 et de Skype Entreprise Server 2015 avec les rôles de serveurs suivants sur au moins un site exécutant Skype Entreprise Server 2015 :
    
      - Au moins un pool d'entreprise ou serveur Standard Edition 
    
      - Pool directeur associé à la fédération SIP, le cas échéant
    
      - Pool Edge associé à la fédération SIP pour le site

  - Déploiement de Lync Server 2010 et Lync Server 2013 mixte avec les rôles de serveur suivants sur au moins un site exécutant Lync Server 2013 :
    
      - Au moins un pool d'entreprise ou serveur Standard Edition dans le site
    
      - Pool directeur associé à la fédération SIP, si elle existe dans le site
    
      - Pool Edge associé à la fédération SIP pour le site

<div>


> [!IMPORTANT]  
> La gestion des utilisateurs, y compris les déplacements entre les utilisateurs locaux et UNRESOLVED_TOKEN_VAL (skypeforbusiness) Online, doit être effectuée à l’aide de la dernière version installée des outils d’administration. Les outils d’administration doivent être installés sur un serveur distinct connecté au déploiement local existant et à Internet. L’let <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Move-CsUser</A> pour déplacer les utilisateurs de votre déploiement local vers UNRESOLVED_TOKEN_VAL(skype16_online) doit être exécuté à partir des outils d’administration connectés à votre déploiement local.



</div>

Pour plus d’informations sur les topologies pris en charge, voir Topologies pris en charge dans [Lync Server 2013](lync-server-2013-supported-topologies.md)et topologies de référence [Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=398709)pour les déploiements hybrides d’entreprise.

Pour obtenir des informations de dépannage sur les déploiements hybrides et la connexion de PowerShell à Lync Online, voir [Lync Online : Lync PowerShell](https://go.microsoft.com/fwlink/p/?linkid=306718)et résolution des problèmes hybrides.

</div>

<div>

## <a name="requirements-for-federation-allowedblocked-lists"></a>Conditions requises pour les listes de fédération autorisées/bloquées

La liste des domaines autorisés comprend les domaines pour lesquels un nom de domaine complet Edge partenaire est configuré (parfois appelé *serveur partenaire autorisé* ou *partenaire de fédération direct*). Vous devez connaitre la différence entre la fédération ouverte et la fédération fermée, appelée *découverte de partenaire* et *liste de domaines partenaires autorisés*, dans les déploiements locaux.

La configuration ci-dessous est requise pour configurer un déploiement hybride :

  - La correspondance de domaine doit être identique pour votre déploiement local et votre organisation Microsoft 365 ou Office 365. Si la découverte de partenaire est activée sur le déploiement local, la fédération ouverte doit être configurée pour votre client en ligne. Si la découverte de partenaire n'est pas activée, alors la fédération fermée doit être configurée pour votre client en ligne.

  - La liste des domaines bloqués dans le déploiement local doit correspondre exactement à la liste des domaines bloqués pour votre client en ligne.

  - La liste des domaines autorisés dans le déploiement local doit correspondre exactement à la liste des domaines autorisés pour votre client en ligne.

  - La fédération doit être activée pour les communications externes pour le client en ligne, qui est configuré à l’aide du Panneau de configuration de Lync Online.

</div>

<div>

## <a name="dns-settings"></a>Paramètres DNS

Lors de la création d’enregistrements DNS pour les déploiements hybrides, tous les enregistrements DNS externes de Lync doivent pointer vers l’infrastructure locale. Pour plus d’informations sur les enregistrements DNS requis, reportez-vous aux conditions [DNS requises pour Lync Server 2013.](lync-server-2013-domain-name-system-dns-requirements.md)

En outre, vous devez vous assurer que la résolution DNS décrite dans le tableau ci-dessous fonctionne dans votre déploiement local :


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Enregistrement DNS</p></td>
<td><p>Résolvable par</p></td>
<td><p>Enregistrement DNS requis</p></td>
</tr>
<tr class="even">
<td><p>Enregistrement SRV DNS pour _sipfederationtls._tcp. &lt; sipdomain.com pour tous les domaines SIP pris en charge résolvant vers des adresses IP externes &gt; Access Edge</p></td>
<td><p>Serveur(s) Edge</p></td>
<td><p>Permettre la communication fédérée dans une configuration hybride. Le serveur Edge doit savoir où acheminer le trafic fédéré pour le domaine SIP qui est à la fois en local et en ligne.</p></td>
</tr>
<tr class="odd">
<td><p>Enregistrement(s) DNS A pour le FQDN du service de conférence web Edge, par exemple webcon.contoso.com se résolvant en adresse(s) IP externe(s) Edge de conférence web</p></td>
<td><p>Ordinateurs des utilisateurs connectés au réseau d'entreprise interne</p></td>
<td><p>Permettre aux utilisateurs de présenter ou d'afficher le contenu de réunions hébergées localement. Ce contenu peut inclure des fichiers PowerPoint, des tableaux blancs, des sondages et des notes partagées. </p></td>
</tr>
</tbody>
</table>


En fonction de la configuration DNS de votre organisation, vous devrez peut-être ajouter ces enregistrements dans la zone DNS hébergée en interne pour le(s) domaine(s) SIP correspondant(s) afin de fournir à ces enregistrements une résolution DNS interne.

</div>

<div>

## <a name="firewall-considerations"></a>Éléments à prendre en compte pour le pare-feu

Les ordinateurs du réseau doivent être en mesure d'effectuer des recherches DNS Internet. Si ces ordinateurs peuvent accéder à des sites Internet standard, votre réseau est correctement configuré.

Selon l’emplacement de votre centre de données Microsoft Online Services, vous devez également configurer vos appareils de pare-feu réseau pour accepter les connexions en fonction de noms de domaine génériques (par exemple, tout le trafic en provenance de \* .outlook.com). Si les pare-feu de votre organisation ne prennent pas en charge les configurations de nom génériques, vous devrez déterminer manuellement les plages d'adresses IP que vous voulez autoriser et les ports.

Consultez la rubrique d’aide sur les URL et [plages d’adresses IP Office 365.](https://go.microsoft.com/fwlink/p/?linkid=252942)

</div>

<span id="b"></span>

<div>

## <a name="port-and-protocol-requirements"></a>Exigences en matière de port et de protocole

Outre la configuration requise pour les ports pour les communications internes à Lync Server 2013, vous devez également configurer les ports suivants.


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Protocole /Port</th>
<th>Applications</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>TCP 443</p></td>
<td><p>Ouvrir entrant</p>
<ul>
<li><p>Services AD FS (rôle serveur de fédération)</p>
<p>Pour plus d’informations, voir <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">Comprendre les services de rôle d’AD FS.</a></p></li>
<li><p>Services AD FS (rôle serveur proxy)</p></li>
<li><p>Microsoft Online Services’entreprise</p></li>
<li><p>Mon portail d’entreprise</p></li>
<li><p>Outlook Web App</p></li>
<li><p>Client Lync (communication avec Lync Online à partir d’un serveur Lync local)</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>TCP 80 et 443</p></td>
<td><p>Ouvrir entrant</p>
<ul>
<li><p>Microsoft Online Services - Outil de synchronisation d'annuaires</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>TCP 5061</p></td>
<td><p>Ouvrir entrant/sortant sur le serveur Edge</p></td>
</tr>
<tr class="even">
<td><p>PSOM/TLS 443</p></td>
<td><p>Ouvrir entrant/sortant pour les sessions de partage de données</p></td>
</tr>
<tr class="odd">
<td><p>STUN/TCP 443</p></td>
<td><p>Ouvrir entrant/sortant pour les sessions de partage audio, vidéo et d’application</p></td>
</tr>
<tr class="even">
<td><p>STUN/UDP 3478</p></td>
<td><p>Ouvrir entrant/sortant pour les sessions audio et vidéo</p></td>
</tr>
<tr class="odd">
<td><p>RTP/TCP 50000-59999</p></td>
<td><p>Ouvrir sortant pour les sessions audio et vidéo</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-accounts-and-data"></a>Comptes et données d’utilisateurs

Dans un déploiement hybride Lync Server 2013, tout utilisateur que vous souhaitez home dans Lync Online doit d’abord être créé dans le déploiement local afin que le compte d’utilisateur soit créé dans les services de domaine Active Directory. Vous pouvez ensuite déplacer l’utilisateur vers Skype Entreprise Online afin de déplacer sa liste de contacts.

Lorsque vous synchronisez les comptes d’utilisateurs entre vos déploiements Lync local et Lync Online avec AD FS et Dirsync, vous devez synchroniser les comptes AD de tous les utilisateurs Lync de votre organisation entre vos déploiements Lync locaux et en ligne, même si les utilisateurs ne sont pas déplacés vers Lync Online. Si vous ne synchronisez pas tous les utilisateurs, la communication entre les utilisateurs locaux et en ligne dans votre organisation risque de ne pas fonctionner comme vous le souhaitez.

<div>


> [!IMPORTANT]  
> Si l’utilisateur est créé à l’aide du portail en ligne du Centre d’administration Microsoft 365, le compte d’utilisateur n’est pas synchronisé avec Active Directory local et l’utilisateur n’existera pas dans l’Active Directory local. Si vous avez déjà créé des utilisateurs dans Lync Online et que vous souhaitez configurer un hybride avec un serveur Lync local, consultez Déplacer des utilisateurs de Lync Online vers Lync local dans <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Lync Server 2013.</A>



</div>

Lors de la planification d'un déploiement hybride, prenez en compte les aspects suivants liés aux utilisateurs.

  - **Contacts de l’utilisateur**   La limite de contacts pour les utilisateurs de Lync Online est de 250. Au-delà de ce chiffre, les contacts seront supprimés de la liste des contacts de l'utilisateur.

  - **Messagerie instantanée et présence**   Les listes de contacts, groupes et listes de contrôle d'accès des utilisateurs sont migrés avec le compte de l'utilisateur.

  - **Données de conférence, contenu de réunion et réunions programmées**   Ce contenu n’est pas migré avec le compte d’utilisateur. Les utilisateurs doivent replanifier les réunions une fois leur compte migré sur Lync Online.

</div>

<div>

## <a name="user-policies-and-features"></a>Fonctionnalités et stratégies utilisateur

  - Dans un environnement hybride Lync Server 2013, les utilisateurs peuvent utiliser la messagerie instantanée, la voix et les réunions en local ou en ligne, mais pas les deux simultanément.

  - **Client Lync**    Certains utilisateurs peuvent avoir besoin d’une nouvelle version du client lorsqu’ils sont déplacés vers Lync Online. Pour Office Communications Server 2007 R2, les utilisateurs doivent être déplacés vers un pool Lync Server 2013 avant la migration vers Lync Online.
    
    Pour plus d’informations sur le support client, voir [Clients pour Lync Online](https://go.microsoft.com/fwlink/p/?linkid=281902) et les clients Lync pris en charge et les [configurations de ports réseau.](https://go.microsoft.com/fwlink/p/?linkid=281901)

  - **Configuration et stratégies sur site (non-utilisateur)**   Les stratégies en ligne et sur site nécessitent une configuration distincte. Vous ne pouvez pas définir des stratégies globales qui s'appliquent au deux.

</div>

</div>

<span> </span>

</div>

</div>

</div>
