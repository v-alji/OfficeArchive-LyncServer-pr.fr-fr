---
title: Installation des systèmes d’exploitaition et des logiciels prérequis sur les serveurs
description: Installation de systèmes d’exploitation et logiciels prérequis sur des serveurs.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install operating systems and prerequisite software on servers
ms:assetid: 055991e0-5aeb-43fc-a7ba-d4b02316d73b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398103(v=OCS.15)
ms:contentKeyID: 48183288
ms.date: 07/24/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2bae9e57db9c2f1d3f3bde7ce9cc7071b73aa01d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427172"
---
# <a name="install-operating-systems-and-prerequisite-software-on-servers-for-lync-server-2013"></a>Installation des systèmes d’exploitaition et des logiciels prérequis sur les serveurs pour Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2014-07-24_

Après avoir configuré l’infrastructure matérielle et système, vous devez installer les systèmes d’exploitation Windows appropriés et les mises à jour, en plus de tous les autres logiciels requis sur chaque serveur que vous déployez. Cela comprend chaque rôle serveur Lync Server 2013 et les serveurs d’infrastructure supplémentaires qui exécutent SQL Server qui sont requis pour votre déploiement.

<div>


> [!NOTE]
> Cette section décrit l’installation de systèmes d’exploitation et logiciels prérequis pour les serveurs internes. Si vous déployez des serveurs Edge pour prendre en charge l’accès utilisateur externe, vous devez également installer les systèmes d’exploitation et les logiciels requis pour ces serveurs, y compris les serveurs de périphérie et les serveurs proxy inverse. Pour plus d’informations sur la façon de préparer des serveurs pour prendre en charge l’accès utilisateur externe, voir préparation de l' <A href="lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md">installation de serveurs dans le réseau de périmètre pour Lync Server 2013</A> dans la documentation de déploiement.



</div>

<div>

## <a name="install-windows-operating-systems-on-servers"></a>Installer des systèmes d’exploitation Windows sur des serveurs

Sur chaque serveur que vous déployez, installez le système d’exploitation Windows approprié en procédant comme suit :

  - **Serveurs exécutant Lync Server 2013**   Pour plus d’informations sur la configuration requise du système d’exploitation pour les serveurs exécutant Lync Server 2013, voir [prise en charge du système d’exploitation serveur et outils dans Lync server 2013](lync-server-2013-server-and-tools-operating-system-support.md) dans la documentation de prise en charge.

  - **Serveurs de base de données**   Pour plus d’informations sur la configuration système requise pour les serveurs de base de données, y compris la base de données principale, la base de données d’archivage et la base de données de surveillance, voir la documentation SQL Server. Pour SQL Server 2012, consultez la documentation SQL Server 2012 en ligne à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) .

<div>


> [!NOTE]
> Si vous installez Lync Server 2013 sur Windows Server &nbsp; 2008 &nbsp; R2 avec SP1, vous devez commencer par installer la mise à jour décrite dans l’article 2646886 de la base de connaissances Microsoft, « correctif : corruption du tas se produit lorsqu’un module appelle la méthode INSERTENTITYBODY dans IIS 7,5 », à <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=2646886"> https://go.microsoft.com/fwlink/p/?linkid=3052&amp ; kbid = 2646886</A>.<BR>Vous devez également modifier le registre comme décrit dans l’article de la base de connaissances, les <A href="https://go.microsoft.com/fwlink/p/?linkid=506893">ID d’événement 32402 et 61045 sont enregistrés dans les serveurs frontaux Lync Server 2013 installés dans Windows Server 2012 R2</A>.



</div>

</div>

<div>

## <a name="install-windows-update-on-servers"></a>Installer Windows Update sur les serveurs

Installez les mises à jour suivantes à partir de Windows Update sur chaque serveur :

  - **Windows Update pour les serveurs exécutant Lync Server 2013**   Pour plus d’informations sur les mises à jour de Windows Update requises pour les serveurs exécutant Lync Server 2013, voir [configuration logicielle requise supplémentaire pour Lync Server 2013](lync-server-2013-additional-software-requirements.md) dans la documentation de planification.

  - **Serveurs de base de données**   Pour plus d’informations sur les mises à jour de Windows Update requises pour les serveurs de base de données, y compris la base de données principale, la base de données d’archivage et la base de données de surveillance, voir la documentation SQL Server 2012. Pour SQL Server 2012, consultez la documentation SQL Server 2012 en ligne à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) .

</div>

<div>

## <a name="install-other-prerequisite-software-on-servers"></a>Installer d’autres logiciels prérequis sur des serveurs

Lync Server 2013 nécessite l’installation des logiciels supplémentaires suivants sur les serveurs :

  - **Logiciels requis pour les serveurs exécutant Lync Server 2013**   Les logiciels requis supplémentaires pour les serveurs exécutant Lync Server 2013 dépendent du rôle de serveur déployé. Pour en savoir plus sur la configuration logicielle requise pour chaque serveur, voir [configuration logicielle requise pour Lync server 2013](lync-server-2013-additional-software-requirements.md) dans la documentation de planification.

  - **Windows Identity Foundation**   Pour pouvoir prendre en charge les scénarios d’authentification de serveur à serveur, Lync Server 2013 nécessite l’installation de Windows Identity Foundation. Pour vérifier qu’il est déjà installé sur votre ordinateur, accédez au panneau de configuration, cliquez sur **programmes et fonctionnalités**, **consultez les mises à jour installées** et Regardez sous **Microsoft Windows**. Pour plus d’informations sur l’installation de Windows Identity Foundation, voir [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657) .

  - **Microsoft .NET Framework 4,5**   L’édition 64 bits de Microsoft .NET Framework 4,5 est requise pour Lync Server 2013.

  - **Logiciels requis pour les serveurs de base de données**   Pour plus d’informations sur la mise à jour Windows requise pour les serveurs de base de données, y compris la base de données principale, la base de données d’archivage et la base de données de surveillance, voir la documentation SQL Server 2012 à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) .
    
    <div>
    

    > [!NOTE]
    > Lync Server 2013 installe automatiquement Microsoft SQL Server 2012 Express sur chaque serveur Standard Edition et chaque serveur exécutant Lync Server 2013 sur lequel se trouve le magasin de configurations local.

    
    </div>

  - **Windows Media Format Runtime**   Tout serveur frontal et serveur Standard Edition sur lequel les conférences seront déployées doit avoir installé le runtime format Windows Media. Le runtime du format Windows Media est requis pour l’exécution des fichiers Windows Media audio (. WMA) que les applications de parc d’appels, d’annonce et de Response Group sont lues pour les annonces et la musique.
    
    <div>
    

    > [!NOTE]
    > Pour Windows Server 2012 et Windows Server 2012 R2, le runtime Windows Media Format Runtime s’installe avec Microsoft Media Foundation.

    
    </div>
    
    <div>
    

    > [!NOTE]
    > Pour Windows Server &nbsp; 2008 et Windows server &nbsp; 2008 &nbsp; R2, le runtime du format Windows Media est installé dans le cadre de l’expérience de bureau Windows. Nous vous recommandons d’installer la version de bureau de Windows avant d’installer Lync Server 2013. Si Lync Server 2013 ne trouve pas ce logiciel sur le serveur, il vous invite à l’installer, puis vous devez redémarrer le serveur pour terminer l’installation.

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

