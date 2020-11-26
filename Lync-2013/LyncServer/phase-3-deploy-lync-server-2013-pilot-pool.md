---
title: 'Étape 3 : déployer le pool de pilotes de Lync Server 2013'
description: 'Étape 3 : déployer le pool de pilotes de Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Phase 3: Deploy Lync Server 2013 pilot pool'
ms:assetid: f12b1517-fb56-4ded-8323-57aa9fc9ea48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205367(v=OCS.15)
ms:contentKeyID: 48185778
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f72f0cdd2e7d3b9e29891a4adc0ab0551539f465
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438455"
---
# <a name="phase-3-deploy-lync-server-2013-pilot-pool"></a><span data-ttu-id="c9cdd-103">Étape 3 : déployer le pool de pilotes de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c9cdd-103">Phase 3: Deploy Lync Server 2013 pilot pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c9cdd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c9cdd-104">

<span> </span></span></span>

<span data-ttu-id="c9cdd-105">_**Dernière modification de la rubrique :** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="c9cdd-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="c9cdd-106">Cette section présente les étapes nécessaires au déploiement d’un pool de pilotes de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c9cdd-106">This section covers the steps required to deploy a pilot pool of Lync Server 2013.</span></span> <span data-ttu-id="c9cdd-107">Le déploiement de Lync Server 2013 nécessite l’utilisation du générateur de topologie pour définir votre topologie et les composants que vous voulez déployer, en préservant votre environnement pour le déploiement des composants Lync Server 2013, en publiant votre conception topologique sur le premier serveur frontal, puis en installant et en configurant le logiciel Lync Server 2013 pour les composants de votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="c9cdd-107">The deployment of Lync Server 2013 requires using Topology Builder to define your topology and the components you want to deploy, preparing your environment for deployment of the Lync Server 2013 components, publishing your topology design on the first Front End Server, and then installing and configuring Lync Server 2013 software for the components for your deployment.</span></span> <span data-ttu-id="c9cdd-108">Lorsque vous avez terminé, votre déploiement de la liste de ressources pilotes 2010 de Lync 2013 Server</span><span class="sxs-lookup"><span data-stu-id="c9cdd-108">When completed, your Lync Server 2013 pilot pool deployment will coexist with an existing Lync Server 2010 pool.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c9cdd-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="c9cdd-109">In This Section</span></span>

  - [<span data-ttu-id="c9cdd-110">Préparation d’Active Directory pour Lync Server</span><span class="sxs-lookup"><span data-stu-id="c9cdd-110">Prepare Active Directory for Lync Server</span></span>](prepare-active-directory-for-lync-server.md)

  - [<span data-ttu-id="c9cdd-111">Téléchargement de la topologie à partir d’un déploiement existant</span><span class="sxs-lookup"><span data-stu-id="c9cdd-111">Download topology from existing deployment</span></span>](download-topology-from-existing-deployment.md)

  - [<span data-ttu-id="c9cdd-112">Déploiement du pool de pilotes Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c9cdd-112">Deploy Lync Server 2013 pilot pool</span></span>](deploy-lync-server-2013-pilot-pool.md)

  - [<span data-ttu-id="c9cdd-113">Vérification de la coexistence du pool pilote avec le pool hérité</span><span class="sxs-lookup"><span data-stu-id="c9cdd-113">Verify pilot pool coexistence with legacy pool</span></span>](verify-pilot-pool-coexistence-with-legacy-pool.md)

  - [<span data-ttu-id="c9cdd-114">Connexion du pool pilote aux serveurs Edge hérités</span><span class="sxs-lookup"><span data-stu-id="c9cdd-114">Connect pilot pool to legacy Edge Servers</span></span>](connect-pilot-pool-to-legacy-edge-servers.md)

  - [<span data-ttu-id="c9cdd-115">Configuration des certificats et des stratégies d’accès de passerelle XMPP</span><span class="sxs-lookup"><span data-stu-id="c9cdd-115">Configure XMPP gateway access policies and certificates</span></span>](configure-xmpp-gateway-access-policies-and-certificates.md)

<span data-ttu-id="c9cdd-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c9cdd-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

