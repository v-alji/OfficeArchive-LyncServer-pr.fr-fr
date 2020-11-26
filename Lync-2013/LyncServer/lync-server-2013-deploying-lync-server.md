---
title: 'Lync Server 2013 : Déploiement de Lync Server'
description: 'Lync Server 2013 : déploiement de Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Lync Server 2013
ms:assetid: b76795a4-4e71-4c70-a5c0-d1197fa8028c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412892(v=OCS.15)
ms:contentKeyID: 48185197
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 569b1e8b07954f04ee7e4f73de51494ece27157e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429929"
---
# <a name="deploying-lync-server-2013"></a><span data-ttu-id="98ff0-103">Déploiement de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98ff0-103">Deploying Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98ff0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98ff0-104">

<span> </span></span></span>

<span data-ttu-id="98ff0-105">_**Dernière modification de la rubrique :** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="98ff0-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="98ff0-106">Votre processus de déploiement de Lync Server 2013 est déterminé par la topologie et les composants du serveur Lync que vous décidez d’installer, notamment si vous voulez déployer un pool frontal ou un serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="98ff0-106">Your deployment process for Lync Server 2013 is determined by the Lync Server topology and components you decide to install, including whether you want to deploy a Front End pool or a Standard Edition server.</span></span> <span data-ttu-id="98ff0-107">Les rubriques de cette section vous aident à déterminer quel environnement vous voulez déployer et vous guider lors du processus de déploiement.</span><span class="sxs-lookup"><span data-stu-id="98ff0-107">The topics in this section help you determine what environment you want to deploy and guide you through the deployment process.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="98ff0-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="98ff0-108">In This Section</span></span>

  - [<span data-ttu-id="98ff0-109">Vue d’ensemble du déploiement pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98ff0-109">Deployment overview for Lync Server 2013</span></span>](lync-server-2013-deployment-overview.md)

  - [<span data-ttu-id="98ff0-110">Configuration système requise pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98ff0-110">System requirements for Lync Server 2013</span></span>](lync-server-2013-system-requirements.md)

  - [<span data-ttu-id="98ff0-111">Préparation de l’infrastructure et des systèmes pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98ff0-111">Preparing the infrastructure and systems for Lync Server 2013</span></span>](lync-server-2013-preparing-the-infrastructure-and-systems.md)

  - [<span data-ttu-id="98ff0-112">Définition et configuration de la topologie dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98ff0-112">Defining and configuring the topology in Lync Server 2013</span></span>](lync-server-2013-defining-and-configuring-the-topology.md)

  - [<span data-ttu-id="98ff0-113">Finalisation et implémentation de la conception de topologie dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98ff0-113">Finalizing and implementing the topology design in Lync Server 2013</span></span>](lync-server-2013-finalizing-and-implementing-the-topology-design.md)

  - [<span data-ttu-id="98ff0-114">Configuration des serveurs et des pools frontaux pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98ff0-114">Setting up Front End Servers and Front End pools for Lync Server 2013</span></span>](lync-server-2013-setting-up-front-end-servers-and-front-end-pools.md)

  - [<span data-ttu-id="98ff0-115">Déploiement de Lync Server 2013 Standard Edition dans une instance existante de Lync Server 2013 Enterprise</span><span class="sxs-lookup"><span data-stu-id="98ff0-115">Deploying Lync Server 2013 Standard Edition into an existing Lync Server 2013 Enterprise</span></span>](lync-server-2013-deploying-lync-server-2013-standard-edition-into-an-existing-lync-server-2013-enterprise.md)

  - [<span data-ttu-id="98ff0-116">Ajout de rôles serveur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98ff0-116">Adding server roles in Lync Server 2013</span></span>](lync-server-2013-adding-server-roles.md)

  - [<span data-ttu-id="98ff0-117">Configuration de l’authentification Kerberos dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98ff0-117">Setting up Kerberos authentication in Lync Server 2013</span></span>](lync-server-2013-setting-up-kerberos-authentication.md)

<span data-ttu-id="98ff0-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98ff0-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

