---
title: 'Lync Server 2013 : configuration requise pour l’application Lync du Windows Store'
description: 'Lync Server 2013 : configuration requise pour l’application Lync du Windows Store.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Windows Store app requirements
ms:assetid: 5f2e0a40-8450-4f61-b6f6-913fc1906020
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ823129(v=OCS.15)
ms:contentKeyID: 50120200
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 17e8705a55625bcf0ad099ead1000a82c994d867
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426166"
---
# <a name="lync-windows-store-app-requirements-for-lync-server-2013"></a>Configuration requise pour l’application Lync du Windows Store pour Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-12-03_

Les organisations disposant d’un déploiement local de Lync Server doivent respecter les exigences suivantes pour prendre en charge l’application Lync du Windows Store.

<div>


> [!NOTE]  
> Pour Lync Server 2010, exécutez la mise à jour cumulative pour Lync Server 2010:2012 février (disponible à l’adresse suivante : <A class=uri href="https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2670352"> https://go.microsoft.com/fwlink/?linkid=3052&amp kbid = 2670352</A>) ou version ultérieure sur tous les serveurs. Pour permettre aux utilisateurs de participer à des réunions, effectuez la mise à jour cumulative pour Lync Server 2010 : octobre 2012 (disponible à l’adresse suivante : <A class=uri href="https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2737915"> https://go.microsoft.com/fwlink/?linkid=3052&amp kbid = 2737915</A>) sur les serveurs.



</div>

  - Activez les services de découverte automatique, de Lync Web App et de ticket Web sur le serveur.

  - Activez l’authentification par certificat sur le serveur frontal ou le pool frontal. (Le processus d’inscription de l’utilisateur sur le serveur frontal ou le pool frontal est souvent désigné sous le nom d’bureau d’enregistrement.) Pour plus d’informations, consultez [créer des paramètres de configuration du Bureau d’enregistrement dans Lync Server 2013](lync-server-2013-create-registrar-configuration-settings.md).

  - Publiez les enregistrements de ressource d’alias DNS (CNAMe) pour le service de découverte automatique.

  - Il n’est plus nécessaire de veiller à ce que le point de distribution de la liste de révocation de certificats (CDP) pour les certificats émis à Lync Server pointe vers une ressource HTTP au lieu d’une ressource LDAP. Toutefois, assurez-vous que les ordinateurs client disposent des dernières mises à jour Windows.

  - Configurer les serveurs proxy HTTP dans l’entreprise pour autoriser le trafic HTTP lié au serveur Lync.  Ajoutez des exceptions pour les services de découverte automatique, Lync Web App et WebPart, si nécessaire.

  - Sur les clients, installez Windows 8,1 et la version la plus récente de l’application Lync du Windows Store pour résoudre un problème de connexion qui se produit généralement lors de l’utilisation de plusieurs domaines (par exemple, lorsque l’URI SIP est **usera@domainZ.com** mais que le serveur Edge est **SIP.domainX.com**).

Si votre organisation est inscrite au service Lync Online ou Microsoft 365 et que vous utilisez votre propre nom de domaine, vous devez effectuer quelques étapes supplémentaires pour configurer votre réseau pour la découverte automatique des serveurs Lync. La configuration requise pour la configuration réseau est la même pour l’application Lync du Windows Store et Lync sur les appareils mobiles.

<div>

## <a name="see-also"></a>Voir aussi


[Déploiement de l’application Lync du Windows Store dans Lync Server 2013](lync-server-2013-deploying-lync-windows-store-app.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>
