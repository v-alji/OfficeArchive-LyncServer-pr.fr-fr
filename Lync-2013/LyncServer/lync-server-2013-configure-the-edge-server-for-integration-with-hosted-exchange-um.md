---
title: Configuration du serveur Edge pour l’intégration à la messagerie unifiée Exchange hébergée
description: Configurez le serveur Edge pour l’intégration avec la messagerie unie Hébergée Exchange.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the Edge Server for integration with hosted Exchange UM
ms:assetid: ede3f2f9-f412-418e-a705-8d8ec98176c5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399075(v=OCS.15)
ms:contentKeyID: 48185745
ms.date: 01/24/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d1a2eb55df172e6df0bacef0c468a235cb00c3f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433646"
---
# <a name="configure-the-edge-server-for-integration-with-hosted-exchange-um"></a>Configuration du serveur Edge pour l’intégration à la messagerie unifiée Exchange hébergée

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Rubrique dernière modification :** 23/01/2015_

Pour fournir à vos utilisateurs Lync Server 2013 des fonctionnalités de messagerie vocale sur une messagerie unifiée Exchange hébergée, vous devez effectuer les tâches de configuration suivantes sur edge Server :

  - Configurez le serveur Edge pour la fédération.

  - Répliquez les données du magasin de gestion centrale sur le serveur Edge et vérifiez la réplication.

  - Créez un fournisseur d’hébergement sur le serveur de périphérie.

Pour plus d’informations, consultez la documentation de Lync Server Management Shell concernant les cmdlets suivantes :

  - [Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))

  - [New-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))

<div>


> [!IMPORTANT]
> Avant d’effectuer ces étapes, vous devez créer un enregistrement SRV DNS pour le service Exchange d’hébergement. Pour plus d’informations, voir <A href="lync-server-2013-create-a-dns-srv-record-for-integration-with-hosted-exchange-um.md">Créer un enregistrement SRV DNS pour l’intégration</A>avec une um Exchange hébergée.



</div>

<div>

## <a name="to-configure-the-edge-server-for-federation"></a>Pour configurer le serveur de périphérique pour la fédération

1.  Démarrez l’shell de gestion de Lync Server : Cliquez sur **Démarrer,** sur Tous les **programmes,** sur **Microsoft Lync Server 2013,** puis sur **Lync Server Management Shell.**

2.  Exécutez l’applet de commande Set-CsAccessEdgeConfiguration pour configurer le serveur pour la fédération. Par exemple, exécutez :
    
        Set-CsAccessEdgeConfiguration -UseDnsSrvRouting -AllowFederatedUsers 1 -EnablePartnerDiscovery 0
    
    L’exemple qui précède définit les paramètres suivants :
    
      - **UseDnsSrvRouting** indique que les serveurs Edge doivent reposer sur les enregistrements DNS SRV lors de l’envoi et la réception des demandes de fédération.
    
      - **AllowFederatedUsers** indique si des utilisateurs internes sont autorisés à communiquer avec des utilisateurs de domaines fédérés. Cette propriété détermine également si des utilisateurs internes peuvent communiquer avec des utilisateurs de domaines fractionnés.
    
      - **EnablePartnerDiscovery** spécifie si Lync Server utilisera les enregistrements DNS pour tenter de découvrir les domaines partenaires qui ne sont pas répertoriés dans la liste des domaines autorisés d’Active Directory. Si c’est le cas, Lync Server 2013 ne fédérera que les domaines répertoriés dans la liste des domaines autorisés. Ce paramètre est requis si vous utilisez le routage de service DNS. Dans la plupart des déploiements, la valeur est définie sur False pour empêcher l’ouverture de la fédération à tous les partenaires.

</div>

<div>

## <a name="to-replicate-data-to-the-edge-server-and-verify-the-replication"></a>Pour répliquer des données sur le serveur de périphérie et vérifier que la réplication s’est correctement effectuée

  - Vérifiez que la réplication du serveur de périphérie est complète. Pour la procédure, voir Vérifier la connectivité entre les serveurs internes et les serveurs Edge dans [Lync Server 2013.](lync-server-2013-verify-connectivity-between-internal-servers-and-edge-servers.md)

</div>

<div>

## <a name="to-create-a-hosting-provider-on-the-edge-server"></a>Pour créer un fournisseur d’hébergement sur le serveur de périphérie

1.  Démarrez l’shell de gestion de Lync Server : Cliquez sur **Démarrer,** sur Tous les **programmes,** sur **Microsoft Lync Server 2013,** puis sur **Lync Server Management Shell.**

2.  Exécutez l’applet de commande **New-CsHostingProvider** pour configurer le fournisseur d’hébergement. Par exemple, exécutez :
    
        New-CsHostingProvider -Identity Fabrikam.com -Enabled $True -EnabledSharedAddressSpace $True -HostsOCSUsers $False -ProxyFQDN "proxyserver.fabrikam.com" -IsLocal $False -VerificationLevel UseSourceVerification
    
    L’exemple qui précède définit les paramètres suivants :
    
      - **Identity** spécifie un identificateur de valeur de chaîne unique pour le fournisseur d’hébergement que vous créez, par exemple, **Fabrikam.com**. Notez que la commande échouera si un fournisseur existant a déjà été configuré avec ce paramètre Identity.
    
      - **Enabled** indique si la connexion réseau entre votre domaine et le fournisseur d’hébergement est activée. Les messages ne peuvent pas être échangés entre les deux entreprises tant que cette valeur n’est pas définie sur **True**.
    
      - **EnabledSharedAddressSpace** indique si le fournisseur d’hébergement sera utilisé dans un scénario d’espace d’adresse SIP partagé (domaine fractionné).
        
        <div>
        

        > [!NOTE]
        > Avant de définir True, essayez de <CODE>EnableSharedAddressSpace</CODE> résoudre l’enregistrement SRV de fédération en interne. Si cet enregistrement ne peut pas être résolu en interne, vous devez créer les enregistrements, _sipfederationtls._tcp. &lt; domaine &gt; et _sip._tls. &lt; dans &gt; le DNS interne. Ces enregistrements doivent pointer vers l’adresse IP externe de l’interface d’accès du serveur Edge.

        
        </div>
    
      - **HostsOCSUsers** indique si le fournisseur d’hébergement est utilisé pour héberger des comptes Lync Server 2013. Si la valeur est **False**, le fournisseur héberge d’autres types de comptes, comme des comptes Microsoft Exchange.
    
      - **ProxyFQDN** spécifie le nom de domaine complet du serveur proxy utilisé par le fournisseur d’hébergement, dans cet exemple, **proxyserver.fabrikam.com**. Cette valeur ne peut pas être modifiée. Si le fournisseur d’hébergement change de serveur proxy, vous devrez supprimer puis recréer l’entrée pour ce fournisseur.
    
      - **IsLocal indique** si le serveur proxy utilisé par le fournisseur d’hébergement est contenu dans votre topologie Lync Server 2013.
    
      - **VerificationLevel** indique le niveau de vérification autorisé pour les messages à destination et en provenance du fournisseur hébergé. Spécifiez **UseSourceVerification**, qui repose sur le niveau de vérification inclus dans les messages en provenance du fournisseur hébergé. Si ce niveau n’est pas spécifié, le message sera rejeté comme message non vérifiable.

</div>

<div>

## <a name="see-also"></a>Voir aussi


[Exportation de la topologie Lync Server 2013 et copie vers le support externe de l’installation Edge](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)  


[Vérification de la connectivité entre les serveurs internes et les serveurs Edge dans Lync Server 2013](lync-server-2013-verify-connectivity-between-internal-servers-and-edge-servers.md)  


[New-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

