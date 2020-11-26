---
title: 'Lync Server 2013 : installation d’un certificat sur un nœud FileSystemWatcher situé en dehors du réseau de périmètre'
description: 'Lync Server 2013 : installation d’un certificat sur un nœud d’observateur situé en dehors du réseau de périmètre.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing a certificate on a watcher node located outside the perimeter network
ms:assetid: 825c9c02-1951-4d7a-a25e-a313a85333f8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688113(v=OCS.15)
ms:contentKeyID: 49733711
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 66f40886e9784b5bd4182a60b955745b5daf2034
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427067"
---
# <a name="installing-a-certificate-on-a-watcher-node-located-outside-the-perimeter-network-of-lync-server-2013"></a><span data-ttu-id="d3a16-103">Installation d’un certificat sur un nœud d’observation situé hors du réseau de périmètre de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3a16-103">Installing a certificate on a watcher node located outside the perimeter network of Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d3a16-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d3a16-104">

<span> </span></span></span>

<span data-ttu-id="d3a16-105">_**Dernière modification de la rubrique :** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="d3a16-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="d3a16-106">Les agents du gestionnaire d’opérations de System Center qui s’exécutent dans un réseau de périmètre (par exemple, un serveur Edge de Lync Server), en dehors de l’entreprise (par exemple, un nœud d’observateur de transactions synthétiques externes) ou sur une limite d’approbation de services de domaine Active Directory, peuvent nécessiter la configuration d’un serveur de passerelle System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="d3a16-106">System Center Operations Manager agents running in a perimeter network (such as a Lync Server Edge Server), outside of the enterprise (such as an external synthetic transaction watcher node), or across an Active Directory Domain Services trust boundary, might require the configuration of a System Center Operations Manager Gateway Server.</span></span> <span data-ttu-id="d3a16-107">Ce rôle de serveur permet aux agents qui n’ont pas de relation d’approbation avec le serveur de gestion racine de déclencher des alertes.</span><span class="sxs-lookup"><span data-stu-id="d3a16-107">This server role allows agents that do not have a trust relationship with the Root Management Server to raise alerts.</span></span> <span data-ttu-id="d3a16-108">Pour plus d’informations, voir la section « gestion des serveurs de passerelles dans Operations Manager 2007 » dans la bibliothèque TechNet de System Center Operations Manager à l’adresse [https://go.microsoft.com/fwlink/p/?LinkId=268703](https://go.microsoft.com/fwlink/p/?linkid=268703) .</span><span class="sxs-lookup"><span data-stu-id="d3a16-108">For details, see "Managing Gateway Servers in Operations Manager 2007" in the System Center Operations Manager TechNet Library at [https://go.microsoft.com/fwlink/p/?LinkId=268703](https://go.microsoft.com/fwlink/p/?linkid=268703).</span></span>

<span data-ttu-id="d3a16-109">Si vous déployez un agent à l’un de ces emplacements, vous devrez également demander et configurer un certificat qui permet au nœud d’observation d’envoyer des alertes à System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="d3a16-109">If you deploy an agent in one of these locations, you will also need to request and configure a certificate that enables the watcher node to send alerts to System Center Operations Manager.</span></span> <span data-ttu-id="d3a16-110">Pour simplifier ce processus, l’équipe Operations Manager a créé un ensemble d’utilitaires qui vous permettent de demander et d’installer le type correct de certificat sur l’ordinateur de nœud d’observation.</span><span class="sxs-lookup"><span data-stu-id="d3a16-110">To simplify this process, the Operations Manager team has created a set of utilities that enable you to request and install the correct type of certificate on the watcher node computer.</span></span> <span data-ttu-id="d3a16-111">Pour plus d’informations, reportez-vous à l’article « obtention de certificats pour les agents non-domaines » en plus facilement avec l’Assistant Création de certificats [https://go.microsoft.com/fwlink/p/?LinkId=267421](https://go.microsoft.com/fwlink/p/?linkid=267421) .</span><span class="sxs-lookup"><span data-stu-id="d3a16-111">For details, and to download these utilities, see the "Obtaining Certificates for Non-Domain Joined Agents Made Easy With Certificate Generation Wizard" blog article at [https://go.microsoft.com/fwlink/p/?LinkId=267421](https://go.microsoft.com/fwlink/p/?linkid=267421).</span></span>

<span data-ttu-id="d3a16-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d3a16-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

