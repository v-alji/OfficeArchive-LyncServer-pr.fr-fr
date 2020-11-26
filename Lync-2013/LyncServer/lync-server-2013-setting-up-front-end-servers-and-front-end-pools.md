---
title: 'Lync Server 2013 : Configuration des serveurs et des pools frontaux'
description: 'Lync Server 2013 : configuration de serveurs frontaux et de listes frontales.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Front End Servers and Front End pools
ms:assetid: c88526f9-69e2-47dd-b3d7-056139d74fb2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398827(v=OCS.15)
ms:contentKeyID: 48185381
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d746bf342f6937c068e32caddd484b708a123910
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444727"
---
# <a name="setting-up-front-end-servers-and-front-end-pools-for-lync-server-2013"></a><span data-ttu-id="7cfc8-103">Configuration des serveurs et des pools frontaux pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7cfc8-103">Setting up Front End Servers and Front End pools for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7cfc8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7cfc8-104">

<span> </span></span></span>

<span data-ttu-id="7cfc8-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="7cfc8-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="7cfc8-106">Cette section vous guide tout au long de l’installation de Lync Server 2013 et de la configuration des rôles de serveur du serveur Standard Edition et du pool frontal, y compris des serveurs frontaux et des rôles serveur colocalisés avec les serveurs frontaux.</span><span class="sxs-lookup"><span data-stu-id="7cfc8-106">This section guides you through installing Lync Server 2013 and setting up the server roles for the Standard Edition server and the Front End pool, including the Front End Servers and any server roles that are collocated with the Front End Servers.</span></span> <span data-ttu-id="7cfc8-107">Pour installer et configurer les rôles de serveur, vous devez exécuter l’Assistant Déploiement de Lync Server sur chaque ordinateur sur lequel vous installez un rôle de serveur.</span><span class="sxs-lookup"><span data-stu-id="7cfc8-107">To install and set up server roles, you run the Lync Server Deployment Wizard on each computer on which you are installing a server role.</span></span> <span data-ttu-id="7cfc8-108">Faites appel à l’Assistant Déploiement pour exécuter les quatre étapes du déploiement que sont l’installation du magasin de configurations local, l’installation des serveurs frontaux, la configuration des certificats et le démarrage des services.</span><span class="sxs-lookup"><span data-stu-id="7cfc8-108">You use the Deployment Wizard to complete all four deployment steps, including installing the Local Configuration store, installing the Front End Servers, configuring certificates, and starting services.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7cfc8-109">Pour pouvoir configurer les rôles de serveurs, vous devez avoir correctement publié une topologie.</span><span class="sxs-lookup"><span data-stu-id="7cfc8-109">Before you can set up server roles, you must have successfully published a topology.</span></span> <span data-ttu-id="7cfc8-110">Pour plus d’informations sur la publication d’une topologie, voir <A href="lync-server-2013-finalizing-and-implementing-the-topology-design.md">Finalisation et implémentation de la conception topologique dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="7cfc8-110">For details about publishing a topology, see <A href="lync-server-2013-finalizing-and-implementing-the-topology-design.md">Finalizing and implementing the topology design in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7cfc8-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7cfc8-111">In This Section</span></span>

  - [<span data-ttu-id="7cfc8-112">Installation du magasin de configurations local dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7cfc8-112">Install the Local Configuration store in Lync Server 2013</span></span>](lync-server-2013-install-the-local-configuration-store.md)

  - [<span data-ttu-id="7cfc8-113">Installation des composants serveur pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7cfc8-113">Install server components for Lync Server 2013</span></span>](lync-server-2013-install-lync-server-server-components.md)

  - [<span data-ttu-id="7cfc8-114">Configuration des certificats pour les serveurs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7cfc8-114">Configure certificates for servers in Lync Server 2013</span></span>](lync-server-2013-configure-certificates-for-servers.md)

  - [<span data-ttu-id="7cfc8-115">Démarrer des services sur les serveurs pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7cfc8-115">Start services on servers for Lync Server 2013</span></span>](lync-server-2013-start-services-on-servers.md)

  - [<span data-ttu-id="7cfc8-116">Test du déploiement du pool dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7cfc8-116">Test the pool deployment in Lync Server 2013</span></span>](lync-server-2013-test-the-pool-deployment.md)

  - [<span data-ttu-id="7cfc8-117">Test du serveur Standard Edition dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7cfc8-117">Test the Standard Edition server in Lync Server 2013</span></span>](lync-server-2013-test-the-standard-edition-server.md)

<span data-ttu-id="7cfc8-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7cfc8-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

