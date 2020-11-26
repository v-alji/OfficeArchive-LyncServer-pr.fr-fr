---
title: 'Lync Server 2013 : configurer la contournement multimédia pour ignorer toujours le serveur de médiation'
description: 'Lync Server 2013 : configurer la contournement multimédia pour ignorer toujours le serveur de médiation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure media bypass to always bypass the Mediation Server
ms:assetid: 370c4f54-e520-4d77-96a3-84c5e84a9996
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425846(v=OCS.15)
ms:contentKeyID: 48183819
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b4981c7b12700d2f0bbf0bf05c8a51623bb8ba9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433912"
---
# <a name="configure-media-bypass-in-lync-server-2013-to-always-bypass-the-mediation-server"></a>Configure media bypass in Lync Server 2013 to always bypass the Mediation Server

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-25_

<div>


> [!NOTE]  
> Dans cette rubrique, nous partons du principe que vous avez déjà configuré le contournement multimédia pour n’importe quelle connexion de type trunk vers un homologue (une passerelle de réseau téléphonique commuté (PSTN), un PBX IP ou un contrôleur de bordure de session (SBC) sur un fournisseur de services de téléphonie Internet (ITSP) pour un site ou un service spécifique pour lequel vous souhaitez que les éléments multimédias<BR>Vous ne pouvez pas configurer le contenu multimédia pour ignorer toujours le serveur de médiation tout en activant également le contrôle d’admission des appels. Ces paramètres ne sont pas compatibles et sont donc mutuellement exclusifs dans l’interface utilisateur du panneau de configuration de Lync Server.



</div>

Outre l’activation de l’exclusion de médias pour les connexions de Trunk individuelles associées à un homologue au serveur de médiation, vous devez également configurer des paramètres globaux pour le contournement multimédia. Si vous suivez les étapes décrites dans cette rubrique pour configurer des paramètres globaux pour le contournement du média multimédia, il est supposé que vous disposez d’une bonne connectivité entre les points de terminaison Lync et les homologues pour lesquels vous avez configuré une contournement multimédia sur la connexion Trunk.

Si vous n’avez pas de bonne connectivité entre les points de terminaison Lync Server et tous les homologues sur le serveur de médiation pour lesquels le raccordement multimédia a été activé, vous devez configurer des paramètres globaux de contournement du média pour utiliser les informations sur les sites et les régions lors de l’utilisation d’une dérivation de média. Cela permet d’augmenter le contrôle lors du contournement du serveur de médiation par le média. Pour cela, suivez les étapes décrites dans [configurer les paramètres globaux de contournement de médias dans Lync server 2013 pour utiliser les informations de site et de région](lync-server-2013-configure-media-bypass-global-settings-to-use-site-and-region-information.md) , puis [associez un sous-réseau à un site réseau dans Lync Server 2013 à la](lync-server-2013-associate-a-subnet-with-a-network-site.md) place.

<div>

## <a name="to-enable-media-bypass-globally-to-always-bypass-the-mediation-server"></a>Pour activer la déviation du trafic multimédia au niveau global pour qu’il contourne toujours le serveur de médiation

1.  Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server. Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

2.  Dans la barre de navigation de gauche, cliquez sur **Configuration réseau**.

3.  Double-cliquez sur la configuration **Globale** dans la liste.

4.  Dans la page **Modifier la configuration globale**, activez la case à cocher **Activer la déviation du trafic multimédia**.

5.  Cliquez sur **Toujours ignorer**.

6.  Cliquez sur **Valider**.

</div>

<div>

## <a name="see-also"></a>Voir aussi


[Configuration de la déviation du trafic multimédia dans Lync Server 2013](lync-server-2013-configure-media-bypass.md)  
[Options de contournement global de médias dans Lync Server 2013](lync-server-2013-global-media-bypass-options.md)  
[Déviation du trafic multimédia et serveur de médiation dans Lync Server 2013](lync-server-2013-media-bypass-and-mediation-server.md)  


[Planification de la déviation du trafic multimédia dans Lync Server 2013](lync-server-2013-planning-for-media-bypass.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

