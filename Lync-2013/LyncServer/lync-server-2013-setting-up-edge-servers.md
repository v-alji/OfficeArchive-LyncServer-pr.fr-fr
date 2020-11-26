---
title: 'Lync Server 2013 : Configuration des serveurs Edge'
description: 'Lync Server 2013 : configuration de serveurs Edge.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Edge Servers
ms:assetid: 09a22919-e36f-4122-8f0d-8d041198912d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398147(v=OCS.15)
ms:contentKeyID: 48183354
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e25c40e8d642d38b38afbab35225b2c7dda4d68
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423980"
---
# <a name="setting-up-edge-servers-in-lync-server-2013"></a><span data-ttu-id="37d8a-103">Configuration des serveurs Edge dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37d8a-103">Setting up Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="37d8a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="37d8a-104">

<span> </span></span></span>

<span data-ttu-id="37d8a-105">_**Dernière modification de la rubrique :** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="37d8a-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="37d8a-106">Les principales tâches nécessaires à la configuration des serveurs de frontière sont les mêmes pour l’installation d’un serveur de périphérie unique ou d’un pool d’équilibrage de charge de serveurs Edge, sauf qu’un ensemble de serveurs Edge équilibrés par la charge matérielle nécessite le déploiement des équilibreurs de charge et des étapes supplémentaires pour la réplication de l’installation sur plusieurs serveurs Edge.</span><span class="sxs-lookup"><span data-stu-id="37d8a-106">The primary tasks required to set up Edge Servers are the same for installing a single Edge Server or a load-balanced pool of Edge Servers, except that a pool of hardware load balanced Edge Servers requires deployment of the load balancers and additional steps for replicating the set up on multiple Edge Servers.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="37d8a-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="37d8a-107">In This Section</span></span>

  - [<span data-ttu-id="37d8a-108">Configuration des interfaces réseau pour les serveurs Edge dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37d8a-108">Set up network interfaces for Edge Servers in Lync Server 2013</span></span>](lync-server-2013-set-up-network-interfaces-for-edge-servers.md)

  - [<span data-ttu-id="37d8a-109">Installation du logiciel prérequis sur les serveurs Edge pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37d8a-109">Install prerequisite software on Edge Servers for Lync Server 2013</span></span>](lync-server-2013-install-prerequisite-software-on-edge-servers.md)

  - [<span data-ttu-id="37d8a-110">Exportation de la topologie Lync Server 2013 et copie vers le support externe de l’installation Edge</span><span class="sxs-lookup"><span data-stu-id="37d8a-110">Export your Lync Server 2013 topology and copy it to external media for edge installation</span></span>](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)

  - [<span data-ttu-id="37d8a-111">Installation des serveurs Edge pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37d8a-111">Install Edge Servers for Lync Server 2013</span></span>](lync-server-2013-install-edge-servers.md)

  - [<span data-ttu-id="37d8a-112">Configuration des certificats de serveur Edge pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37d8a-112">Set up Edge certificates for Lync Server 2013</span></span>](lync-server-2013-set-up-edge-certificates.md)

  - [<span data-ttu-id="37d8a-113">Démarrage des serveurs de périphérie dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37d8a-113">Start Edge Servers in Lync Server 2013</span></span>](lync-server-2013-start-edge-servers.md)

  - [<span data-ttu-id="37d8a-114">Configuration des serveurs proxy inverses pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37d8a-114">Setting up reverse proxy servers for Lync Server 2013</span></span>](lync-server-2013-setting-up-reverse-proxy-servers.md)

<span data-ttu-id="37d8a-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="37d8a-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

