---
title: 'Lync Server 2013 : Configuration de la fédération Lync'
description: 'Lync Server 2013 : configuration de la fédération Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Lync federation
ms:assetid: 374ddc43-26f9-499d-be68-a5158adfa49c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204800(v=OCS.15)
ms:contentKeyID: 48183822
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 382def41635f05525e5b047e97febffdb069da2a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395068"
---
# <a name="setting-up-lync-federation-in-lync-server-2013"></a>Configuration de la fédération Lync dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Rubrique dernière modification :** 2014-03-27_

Si vous avez déjà déployé vos serveurs ou serveurs Edge, l’ajout des fonctionnalités de scénarios fédérés se fait directement. Si vous n’avez pas encore installé de serveurs Edge, vous devez d’abord le faire. Pour plus d’informations, voir : Planification de l’accès des utilisateurs externes dans [Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) dans la documentation Planification et Déploiement de l’accès des utilisateurs externes dans [Lync Server 2013](lync-server-2013-deploying-external-user-access.md) dans la documentation De déploiement.

<div>


> [!NOTE]  
> Si vous envisagez de configurer une combinaison de fédération XMPP, de fédération Lync ou de connectivité de messagerie instantanée publique, vous pouvez les déployer simultanément ou une par une. Si vous configurez les options via le Générateur de topologie et l’shell de gestion de Lync Server, puis exécutez l’Assistant Déploiement sur le serveur Edge après avoir configuré les options pour un, deux ou les trois types de fédération, vous pouvez réduire le nombre d’étapes requises.



</div>

<div>

## <a name="setting-up-lync-federation-in-topology-builder-and-the-deployment-wizard"></a>Configuration de la fédération Lync dans le Générateur de topologie et l’Assistant Déploiement

1.  Sur un serveur frontal, ouvrez le Générateur de topologie. Développez les pools Edge, puis cliquez avec le bouton droit sur votre serveur Edge ou votre pool de serveurs Edge. Sélectionnez Modifier les propriétés.

2.  Dans Modifier les propriétés sous Général, sélectionnez Activer la fédération pour ce pool Edge (Port 5061). Cliquez sur OK.

3.  Cliquez sur Action, sélectionnez Topologie, puis Publier. Lorsque vous y est invité à publier la topologie, cliquez sur Suivant. Lorsque la publication est terminée, cliquez sur Terminer.

4.  Sur le serveur Edge, ouvrez l’Assistant Déploiement de Lync Server. Cliquez sur Installer ou mettre à jour Lync Server System, puis sur Installer ou supprimer des composants Lync Server. Cliquez sur Exécuter à nouveau.

5.  Pour configurer les composants de Lync Server, cliquez sur Suivant. L’écran de résumé affiche les actions au cours de leur exécution. Une fois le déploiement terminé, cliquez sur Afficher le journal pour afficher les fichiers journaux disponibles. Cliquez sur Terminer pour terminer le déploiement.
    
    <div>
    

    > [!IMPORTANT]  
    > Vous pouvez sélectionner cette option, mais un seul groupe Edge ou serveur Edge de votre organisation peut être publié en externe pour la fédération. Tout l’accès par les utilisateurs fédérés, y compris les utilisateurs de messagerie instantanée publique, passe par le même pool Edge ou le même serveur Edge. Par exemple, si votre déploiement inclut un pool Edge ou un serveur Edge unique déployé à New York et un serveur déployé à Londres et que vous activez la prise en charge de la fédération sur le pool Edge de New York ou le serveur Edge unique, le trafic de signal des utilisateurs fédérés passe par le pool Edge de New York ou le serveur Edge unique. Cela s’applique également aux communications avec les utilisateurs de Londres, même si un utilisateur interne de Londres qui appelle un utilisateur fédéré de Londres utilise le pool de serveurs ou le serveur Edge de Londres pour le trafic A/V.

    
    </div>

</div>

<div>

## <a name="configuring-federation-with-partners"></a>Configuration de la fédération avec des partenaires

1.  Pour configurer une fédération réussie avec un autre Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2 ou Office Communicator 2007, sélectionnez le type de fédération dans le tableau suivant et définissez les enregistrements SRV DNS, hôte DNS (A ou AAAA pour IPv6) et configurez les stratégies applicables au type de fédération :
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Type de fédération</th>
    <th>Enregistrements DNS</th>
    <th>Définition de stratégie</th>
    <th>Remarques</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Domaine partenaire découvert</p></td>
    <td><p>Configurez l’enregistrement SRV du format _sipfederationtls._tcp. &lt; nom de domaine externe Où la valeur de port de l’enregistrement SRV est &gt; TCP 5061 et où l’hôte offrant ce <strong>service</strong> est défini comme sip. &lt;nom de domaine &gt; externe (FQDN) de votre service Edge Access. Pour plus d’informations sur la création de l’enregistrement SRV, voir Configurer le DNS pour la prise en charge de Edge dans <a href="lync-server-2013-configure-dns-for-edge-support.md">Lync Server 2013</a></p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Activation ou désactivation de la fédération et de la connectivité PIC dans Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Activation ou désactivation de la découverte de partenaires de fédération dans Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Les versions précédentes ont fait référence à ce type de fédération <strong>appelée Open Enhanced Federation.</strong> La création de l’enregistrement SRV est requise pour ce type de fédération et permet à d’autres partenaires de découvrir votre fédération.</p></td>
    </tr>
    <tr class="even">
    <td><p>Domaine partenaire autorisé</p></td>
    <td><p>Configurez l’enregistrement SRV du format _sipfederationtls._tcp. &lt; nom de domaine externe Où la valeur de port de l’enregistrement SRV est &gt; TCP 5061 et où l’hôte offrant ce <strong>service</strong> est défini comme sip. &lt;nom de domaine &gt; externe (FQDN) de votre service Edge Access. Pour plus d’informations sur la création de l’enregistrement SRV, voir Configurer le DNS pour la prise en charge de Edge dans <a href="lync-server-2013-configure-dns-for-edge-support.md">Lync Server 2013</a></p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Activation ou désactivation de la fédération et de la connectivité PIC dans Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Les versions précédentes ont fait référence à ce type de fédération appelée <strong>fédération améliorée.</strong> La création de l’enregistrement SRV est facultative pour ce type de fédération et permet à d’autres partenaires de découvrir votre fédération. Bien entendu, il s’agit alors <strong>d’une fédération</strong>open enhanced ou du domaine partenaire <strong>découvert.</strong></p></td>
    </tr>
    <tr class="odd">
    <td><p>Serveur partenaire autorisé</p></td>
    <td><p>Configurer le nom de domaine SIP et le nom de domaine complet du partenaire Edge Server en tant que partenaire de fédération dans Stratégies</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Activation ou désactivation de la fédération et de la connectivité PIC dans Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Configuration de la prise en charge des domaines externes autorisés dans Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Configuration de la prise en charge pour les domaines externes bloqués dans Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Ce type de fédération est la définition d’une relation un à un et ne permet pas de découvrir d’autres partenaires de fédération. Chaque partenaire de fédération est configuré de manière explicite. Dans les versions précédentes, il s’agissait de fédération <strong>directe</strong></p></td>
    </tr>
    <tr class="even">
    <td><p>Fournisseur d’hébergement et fournisseur de messagerie instantanée publique</p></td>
    <td><p>Aucune exigences DNS spécifique n’est définie pour ce type de fédération</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Activation ou désactivation de la fédération et de la connectivité PIC dans Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Création ou modification des fournisseurs fédérés SIP publics dans Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Création ou modification des fournisseurs fédérés SIP hébergés dans Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Ce type de fédération définit les services et fournisseurs d’hébergement que vous voulez configurer pour vos utilisateurs. Les utilisations classiques incluent la configuration de fournisseurs de messagerie instantanée publique tels Windows Live Messenger, Yahoo! et AOL, ainsi que des fournisseurs d’hébergement tels que Lync Online et Microsoft 365</p>
    <div>

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P>À compter du 1er septembre 2012, la licence d’abonnement utilisateur Microsoft Lync Public IM Connectivity (« PIC USL ») n’est plus disponible à l’achat pour les nouveaux contrats ou le renouvellement. Les clients titulaires d’une licence active pourront continuer à se fédérer avec Yahoo! Messenger jusqu’à la date d’arrêt du service. Date de fin de vie en juin 2014 pour AOL et Yahoo! a été annoncé. Pour plus d’informations, consultez la prise en charge de la connectivité de messagerie instantanée publique dans <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Lync Server 2013.</A></P>
    > <LI>
    > <P>L’outil PIC USL est une licence d’abonnement par utilisateur et par mois requise pour que Lync Server ou Office Communications Server se fédérer avec Yahoo! Messenger. La capacité de Microsoft à fournir ce service a été prise en charge par Yahoo!, le contrat sous-jacent pour lequel il est en cours de liquidation.</P>
    > <LI>
    > <P>Plus que jamais, Lync est un outil puissant permettant de communiquer entre les organisations et les individus dans le monde entier. La fédération avec d Windows Live Messenger ne nécessite aucune licence utilisateur/appareil supplémentaire au-delà de la licence d’accès client standard de Lync. La fédération Skype sera ajoutée à cette liste, ce qui permettra aux utilisateurs de Lync d’atteindre des centaines de millions de personnes avec la messagerie instantanée et la voix.</P></LI></UL>


    </div></td>
    </tr>
    </tbody>
    </table>


2.  Définir et configurer les enregistrements SRV DNS requis (A ou AAAA pour IPv6) et DNS

3.  Définissez et configurez les stratégies à l’aide du Panneau de configuration de Lync Server ou à l’aide de Lync Server Management Shell et des cmdlets appropriées. Pour plus d’informations sur les cmdlets Lync Server Management Shell, voir les cmdlets de fédération et d’accès externe dans [Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)
    
    <div>
    

    > [!NOTE]  
    > Lync Room System (LRS) n’affiche pas le bouton Rejoindre pour les réunions envoyées par les organisateurs dans des partenaires Lync fédérés. Pour qu’un lien d’accès à une réunion s’affiche sur LRS, l’organisation d’envoi doit activer le TNEF à l’aide de l’cmdlet suivante :<BR><BR><CODE>New-RemoteDomain -DomainName Contoso.com -Name Contoso</CODE><BR><CODE>Set-RemoteDomain -Identity Contoso -TNEFEnabled $true</CODE><BR>Notez que ce n’est pas spécifique au LRS. Outlook et Lync n’afficheront pas non plus de liens de participer dans ce cas, car les propriétés MAPI ne sont pas transportées, mais dans le cas Outlook, l’utilisateur peut ouvrir l’invitation à la réunion et cliquer sur l’URL de la réunion. Lorsque TNEFEnabled est définie sur true Exchange 2013 ne déconnecte pas les propriétés MAPI, y compris OnlineMeetingExternalLink, et le bouton Rejoindre s’affiche dans le rappel.

    
    </div>

</div>

<div>

## <a name="see-also"></a>Voir aussi


[Planification de la fédération SIP, XMPP et de la messagerie instantanée publique dans Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)  
[Gestion de la fédération et de l’accès externe à Lync Server 2013](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

