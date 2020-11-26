---
title: 'Lync Server 2013 : Choix des modalités de déploiement de Microsoft Lync'
description: 'Lync Server 2013 : choix du déploiement de Microsoft Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deciding how to deploy Microsoft Lync
ms:assetid: 6ca677d3-745d-4935-8f05-19274a8bccf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204979(v=OCS.15)
ms:contentKeyID: 48184423
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a800b51dfddc6f2c99e42c8f117056ed4091b6a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431231"
---
# <a name="deciding-how-to-deploy-lync-server-2013"></a><span data-ttu-id="d77e0-103">Choix des modalités de déploiement de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d77e0-103">Deciding how to deploy Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d77e0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d77e0-104">

<span> </span></span></span>

<span data-ttu-id="d77e0-105">_**Dernière modification de la rubrique :** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="d77e0-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="d77e0-106">Lors de la planification de Lync, la première décision majeure consiste à déployer Microsoft Lync : comme Lync Server 2013 en local, ou Lync Online avec Microsoft 365 ou Office 365 dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="d77e0-106">When planning for Lync, the first major decision is how to deploy Microsoft Lync: as Lync Server 2013 on premises, or Lync Online with Microsoft 365 or Office 365 in the cloud.</span></span>

  - <span data-ttu-id="d77e0-107">**Lync Server 2013 local** : ce choix fournit l’ensemble des fonctionnalités Lync complètes et offre une souplesse de configuration, de personnalisation et d’utilisation de votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="d77e0-107">**Lync Server 2013 on-premises** : This choice provides the complete Lync feature set and provides ultimate flexibility in configuring, customizing, and operating your deployment.</span></span> <span data-ttu-id="d77e0-108">Tous les serveurs sont installés sur site et gérés par votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d77e0-108">All servers are installed onsite and maintained by your organization.</span></span> <span data-ttu-id="d77e0-109">Un déploiement local fournit une gamme complète de fonctionnalités de serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="d77e0-109">An on-premises deployment provides the full range of Lync Server features.</span></span>

  - <span data-ttu-id="d77e0-110">**Lync Online dans le Cloud** Lync Online est conçu pour les organisations qui souhaitent bénéficier de coûts et de compétences en matière de messagerie instantanée, de présence et de réunions dans le Cloud sans sacrifier les fonctionnalités de niveau professionnel de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d77e0-110">**Lync Online in the cloud** Lync Online is designed for organizations that want the cost and agility benefits of cloud-based instant messaging, presence, and meetings without sacrificing the business-class capabilities of Lync Server.</span></span> <span data-ttu-id="d77e0-111">Avec Lync Online, Microsoft déploie et met à jour l’infrastructure de serveur requise, ainsi que les mises à jour, les correctifs et les mises à niveau en continu.</span><span class="sxs-lookup"><span data-stu-id="d77e0-111">With Lync Online, Microsoft deploys and maintains the required server infrastructure, and handles ongoing maintenance, patches, and upgrades.</span></span> <span data-ttu-id="d77e0-112">Certaines fonctionnalités disponibles dans un déploiement local ne sont pas disponibles dans Lync Online.</span><span class="sxs-lookup"><span data-stu-id="d77e0-112">Some features available in an on-premises deployment are not available in Lync Online.</span></span>

<span data-ttu-id="d77e0-113">Le type de déploiement le plus approprié dépend des charges de travail que vous voulez déployer et du statut géographique et commercial de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d77e0-113">Which type of deployment would be best for you depends on the workloads you want to deploy, and your organization’s geographical and business status.</span></span>

<div>

## <a name="lync-server"></a><span data-ttu-id="d77e0-114">Lync Server</span><span class="sxs-lookup"><span data-stu-id="d77e0-114">Lync Server</span></span>

<span data-ttu-id="d77e0-115">Le déploiement de Lync Server local est préférable pour les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="d77e0-115">An on-premises Lync Server deployment is best for the following scenarios:</span></span>

  - <span data-ttu-id="d77e0-116">**Fonctionnalités voix entreprise complètes**   Si vous envisagez de déployer une solution voix entreprise complète pour remplacer votre PBX ou utiliser des fonctionnalités d’appel avancées, un déploiement Lync Server local est requis.</span><span class="sxs-lookup"><span data-stu-id="d77e0-116">**Full Enterprise Voice Capabilities**   If you plan to deploy a full Enterprise Voice solution to replace your PBX or which uses advanced calling features, an on-premises Lync Server deployment is required.</span></span> <span data-ttu-id="d77e0-117">Locale prend en charge la connectivité directe avec les systèmes et les Trunks PBX, ainsi que les fonctionnalités de téléphone avancées telles que les Response Groups et le parc d’appels.</span><span class="sxs-lookup"><span data-stu-id="d77e0-117">On-premises supports direct connectivity with PBX systems and trunks, and advanced phone features such as response groups and call park.</span></span> <span data-ttu-id="d77e0-118">Pour le moment, Lync Online ne prend pas en charge ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="d77e0-118">Lync Online does not currently support these features.</span></span>

  - <span data-ttu-id="d77e0-119">**Contrôles de qualité multimédia**   Si vous souhaitez bénéficier de toutes les fonctionnalités d’assurance qualité multimédia, telles que les fonctionnalités de contrôle d’admission des appels (CAC) et de qualité de service (QoS), vous devez disposer d’un déploiement local.</span><span class="sxs-lookup"><span data-stu-id="d77e0-119">**Media Quality Controls**   If you want the full range of media quality assurance features, such as Call Admission Control (CAC) and Quality of Service (QoS) features, you will want an on-premises deployment .</span></span>

  - <span data-ttu-id="d77e0-120">**Conversation permanente**   Si vous devez déployer une conversation permanente pour votre organisation, vous devez choisir un déploiement local.</span><span class="sxs-lookup"><span data-stu-id="d77e0-120">**Persistent Chat**   If you need to deploy Persistent chat for your organization, you must choose an on-premises deployment.</span></span>

  - <span data-ttu-id="d77e0-121">**applications serveur tierces**   Seuls les déploiements locaux peuvent fonctionner avec des applications tierces approuvées qui utilisent l’API Microsoft Unified Communications Managed API (UCMA).</span><span class="sxs-lookup"><span data-stu-id="d77e0-121">**3rd-Party Server Applications**   Only on-premises deployments can work with trusted 3rd-party applications that use the Microsoft Unified Communications Managed API (UCMA).</span></span>

  - <span data-ttu-id="d77e0-122">La **prise en charge de l’assistance régionale est une entreprise multi-nationale/régionale** .   Si vous disposez de centres de donnees dans plusieurs pays ou régions et que vous avez besoin de déployer et de gérer des serveurs sur une base régionale, il est préférable d’utiliser un déploiement local, dans la mesure où il fournit ce type de fonctionnalité de gestion régionale.</span><span class="sxs-lookup"><span data-stu-id="d77e0-122">**Multi-National/Multi-Regional Companies Needing Regional Support**   If you have datacenters in multiple countries or regions and need servers to be deployed and managed on a regional basis, an on-premises deployment is best, as it provides this type of regional management capabilities.</span></span>

  - <span data-ttu-id="d77e0-123">**Contrôle total des stratégies, des rapports et des mises à niveau**   Le déploiement de Lync Server sur site vous permet d’accéder à l’ensemble des stratégies du serveur et du client, de la surveillance ainsi que d’autres rapports et de la synchronisation des mises à niveau.</span><span class="sxs-lookup"><span data-stu-id="d77e0-123">**Complete control over policies, reports, and upgrades**   With an on premises Lync Server deployment, you have access to the full set of server and client policies, Monitoring and other reports, and timing of upgrades.</span></span> <span data-ttu-id="d77e0-124">Lync Online fournit un sous-ensemble du paramètre de stratégie et des rapports, et fournit une fenêtre limitée, même importante, pour accepter les mises à niveau.</span><span class="sxs-lookup"><span data-stu-id="d77e0-124">Lync Online provides a subset of policy setting and reports, and provides a limited, though significant, window for accepting upgrades.</span></span>

</div>

<div>

## <a name="lync-online"></a><span data-ttu-id="d77e0-125">Lync Online</span><span class="sxs-lookup"><span data-stu-id="d77e0-125">Lync Online</span></span>

<span data-ttu-id="d77e0-126">Si aucun des facteurs de la liste précédente n’est essentiel pour vous, vous pouvez choisir Lync Online pour faciliter le déploiement et la gestion.</span><span class="sxs-lookup"><span data-stu-id="d77e0-126">If none of the factors in the preceding list are critical for you, you may want to choose Lync Online, for simpler deployment and manageability.</span></span> <span data-ttu-id="d77e0-127">Lync Online fournit un ensemble de fonctionnalités de messagerie instantanée, de présence et de conférence puissantes, ainsi que des appels audio et vidéo sur IP entre les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d77e0-127">Lync Online provides a robust IM, presence and conferencing feature set, and also enables voice and video calls over IP between users in your organization.</span></span>

<span data-ttu-id="d77e0-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d77e0-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
