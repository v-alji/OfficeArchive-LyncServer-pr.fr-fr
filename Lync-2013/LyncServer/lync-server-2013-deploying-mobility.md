---
title: 'Lync Server 2013 : Déploiement de la mobilité'
description: 'Lync Server 2013 : déploiement de la mobilité.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying mobility
ms:assetid: f41e6b25-d2cd-43fd-a17b-22cfda8bcd4f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690055(v=OCS.15)
ms:contentKeyID: 48185805
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cf927b950f8b94884fb91224a87e196fc815fca1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429873"
---
# <a name="deploying-mobility-in-lync-server-2013"></a><span data-ttu-id="eb5b2-103">Déploiement de la mobilité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb5b2-103">Deploying mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eb5b2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eb5b2-104">

<span> </span></span></span>

<span data-ttu-id="eb5b2-105">_**Dernière modification de la rubrique :** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="eb5b2-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="eb5b2-106">Lorsque vous déployez la fonctionnalité de mobilité de Lync Server 2013, les utilisateurs mobiles peuvent utiliser les appareils mobiles pris en charge pour les fonctionnalités Lync telles que la messagerie instantanée, la présence et les contacts.</span><span class="sxs-lookup"><span data-stu-id="eb5b2-106">When you deploy the Lync Server 2013 mobility feature, mobile users can use supported mobile devices for Lync functionality such as instant messaging (IM), presence, and contacts.</span></span>

<span data-ttu-id="eb5b2-107">Pour plus d’informations sur la configuration requise pour le déploiement de la fonctionnalité de mobilité, voir [planification de la mobilité dans Lync Server 2013](lync-server-2013-planning-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="eb5b2-107">For details about requirements for deploying the mobility feature, see [Planning for mobility in Lync Server 2013](lync-server-2013-planning-for-mobility.md).</span></span>

<span data-ttu-id="eb5b2-108">Cette section vous guide tout au long de la procédure de déploiement et de vérification des fonctionnalités de mobilité et de découverte automatique.</span><span class="sxs-lookup"><span data-stu-id="eb5b2-108">This section guides you through the steps for deploying and verifying the mobility and automatic discovery features.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="eb5b2-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="eb5b2-109">In This Section</span></span>

  - [<span data-ttu-id="eb5b2-110">Création d’enregistrements DNS pour le service de découverte automatique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb5b2-110">Creating DNS records for the Autodiscover Service in Lync Server 2013</span></span>](lync-server-2013-creating-dns-records-for-the-autodiscover-service.md)

  - [<span data-ttu-id="eb5b2-111">Modification des certificats pour la mobilité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb5b2-111">Modifying certificates for mobility in Lync Server 2013</span></span>](lync-server-2013-modifying-certificates-for-mobility.md)

  - [<span data-ttu-id="eb5b2-112">Configuration du proxy inverse pour la mobilité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb5b2-112">Configuring the reverse proxy for mobility in Lync Server 2013</span></span>](lync-server-2013-configuring-the-reverse-proxy-for-mobility.md)

  - [<span data-ttu-id="eb5b2-113">Configuration de la découverte automatique dans Lync Server 2013 pour la mobilité avec les déploiements hybrides</span><span class="sxs-lookup"><span data-stu-id="eb5b2-113">Configuring Autodiscover in Lync Server 2013 for mobility with hybrid deployments</span></span>](lync-server-2013-configuring-autodiscover-for-mobility-with-hybrid-deployments.md)

  - [<span data-ttu-id="eb5b2-114">Vérification du déploiement de mobilité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb5b2-114">Verifying your mobility deployment in Lync Server 2013</span></span>](lync-server-2013-verifying-your-mobility-deployment.md)

  - [<span data-ttu-id="eb5b2-115">Configuration des notifications push dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb5b2-115">Configuring for push notifications in Lync Server 2013</span></span>](lync-server-2013-configuring-for-push-notifications.md)

  - [<span data-ttu-id="eb5b2-116">Configuration de la stratégie de mobilité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb5b2-116">Configuring mobility policy in Lync Server 2013</span></span>](lync-server-2013-configuring-mobility-policy.md)

<span data-ttu-id="eb5b2-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eb5b2-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

