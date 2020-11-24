---
title: 'Lync Server 2013 : activation de la surveillance'
description: 'Lync Server 2013 : activation de la surveillance.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling monitoring
ms:assetid: 244df419-d0a8-4b1d-aedd-a92114172ab6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687994(v=OCS.15)
ms:contentKeyID: 49733584
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d8995042bdc9b121dc5253940104bb167567ddcc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394725"
---
# <a name="enabling-monitoring-in-lync-server-2013"></a><span data-ttu-id="f35f9-103">Activation de l’analyse dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f35f9-103">Enabling monitoring in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f35f9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f35f9-104">

<span> </span></span></span>

<span data-ttu-id="f35f9-105">_**Dernière modification de la rubrique :** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="f35f9-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="f35f9-106">Bien que les agents de collecte des données unifiées soient automatiquement installés et activés sur chaque serveur frontal, cela signifie que vous commencerez automatiquement à collecter des données d’analyse dès que vous avez terminé d’installer Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f35f9-106">Although the unified data collection agents are automatically installed and activated on each Front End server, that does not mean that you will automatically begin to collect monitoring data the moment you finish installing Microsoft Lync Server 2013.</span></span> <span data-ttu-id="f35f9-107">À la place, vous devez effectuer les deux actions suivantes : vous devez associer votre serveur frontal/les listes frontales à une base de données de surveillance, et vous devez activer l’enregistrement des détails des appels (CDR) et/ou la qualité de l’expertise (QoE) sur l’étendue globale et/ou l’étendue du site.</span><span class="sxs-lookup"><span data-stu-id="f35f9-107">Instead, you must do two things: you must associate your Front End servers/Front End pools with a monitoring database, and you must enable call detail recording (CDR) and/or Quality of Experience (QoE) monitoring at the global scope and/or the site scope.</span></span>

<span data-ttu-id="f35f9-108">Pour obtenir des instructions pas à pas sur l’utilisation d’un serveur frontal ou d’une base de données de surveillance, voir la rubrique [Association d’un magasin d’analyse avec un pool frontal dans Lync Server 2013](lync-server-2013-associating-a-monitoring-store-with-a-front-end-pool.md) dans le Guide de déploiement.</span><span class="sxs-lookup"><span data-stu-id="f35f9-108">For step-by-step instructions on associating Front End servers or Front End pools with a monitoring database, see the topic [Associating a monitoring store with a Front End pool in Lync Server 2013](lync-server-2013-associating-a-monitoring-store-with-a-front-end-pool.md) in the Deployment guide.</span></span> <span data-ttu-id="f35f9-109">Une fois ces associations créées et après la publication de votre nouvelle topologie de serveur Lync, vous ne pourrez toujours pas collecter de données d’analyse.</span><span class="sxs-lookup"><span data-stu-id="f35f9-109">After these associations have been made, and after your new Lync Server topology has been published, you will still not be able to collect monitoring data.</span></span> <span data-ttu-id="f35f9-110">C’est pourquoi, par défaut, la collection de données CDR et QoE est désactivée lors de l’installation de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f35f9-110">That's because, by default, both CDR and QoE data collection is disabled when you install Lync Server 2013.</span></span>

<span data-ttu-id="f35f9-111">Pour commencer la collecte de données, vous devez activer le contrôle CDR et/ou QoE.</span><span class="sxs-lookup"><span data-stu-id="f35f9-111">In order to begin data collection you will need to enable CDR and/or QoE monitoring.</span></span> <span data-ttu-id="f35f9-112">(Notez que vous n’avez pas besoin d’activer les contrôles CDR et QoE ; si vous le souhaitez, vous pouvez activer un seul type d’analyse tout en laissant l’autre type désactivé.) Pour activer le contrôle CDR dans l’étendue globale, exécutez la commande suivante à partir de Lync Server Management Shell :</span><span class="sxs-lookup"><span data-stu-id="f35f9-112">(Note that you do not have to enable both CDR and QoE monitoring; if you prefer, you can enable one type of monitoring while leaving the other type disabled.) To enable CDR monitoring at the global scope run the following command from within the Lync Server Management Shell:</span></span>

    Set-CsCdrConfiguration -Identity "global" -EnableCDR $True

<span data-ttu-id="f35f9-113">Vous pouvez également activer le contrôle de CDR à partir du panneau de configuration de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f35f9-113">Alternatively, you can enable CDR monitoring from within the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="f35f9-114">Dans le panneau de configuration de Lync Server, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="f35f9-114">From within the Lync Server Control Panel, complete the following procedure:</span></span>

1.  <span data-ttu-id="f35f9-115">Cliquez sur **surveillance**.</span><span class="sxs-lookup"><span data-stu-id="f35f9-115">Click **Monitoring**.</span></span>

2.  <span data-ttu-id="f35f9-116">Dans l’onglet **enregistrement des détails des appels** , double-cliquez sur le paramètre **Global** .</span><span class="sxs-lookup"><span data-stu-id="f35f9-116">On the **Call Detail Recording** tab, double-click the **Global** setting.</span></span>

3.  <span data-ttu-id="f35f9-117">Dans le volet **modifier les paramètres d’enregistrement des détails des appels (CdR)** , sélectionnez **activer l’analyse de CDR** , puis cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="f35f9-117">In the **Edit Call Detail Recording (CDR) Setting** pane, select **Enable monitoring of CDRs** and then click **Commit**.</span></span>

<span data-ttu-id="f35f9-118">Pour activer le contrôle QoE au niveau de l’étendue globale, exécutez la commande suivante à partir de Lync Server Management Shell :</span><span class="sxs-lookup"><span data-stu-id="f35f9-118">To enable QoE monitoring at the global scope, run this command from within the Lync Server Management Shell:</span></span>

    Set-CsQoEConfiguration -Identity "global" -EnableQoE $True

<span data-ttu-id="f35f9-119">Si vous le souhaitez, vous pouvez également activer le contrôle QoE dans le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f35f9-119">If you prefer, you can also enable QoE monitoring from within the Lync Server Control Panel.</span></span> <span data-ttu-id="f35f9-120">Dans le panneau de configuration, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="f35f9-120">From within the Control Panel, complete the following procedure:</span></span>

1.  <span data-ttu-id="f35f9-121">Cliquez sur **surveillance**.</span><span class="sxs-lookup"><span data-stu-id="f35f9-121">Click **Monitoring**.</span></span>

2.  <span data-ttu-id="f35f9-122">Sous l’onglet **données de qualité de l’environnement** , double-cliquez sur le paramètre **Global** .</span><span class="sxs-lookup"><span data-stu-id="f35f9-122">On the **Quality of Experience Data** tab, double-click the **Global** setting.</span></span>

3.  <span data-ttu-id="f35f9-123">Dans le volet des **paramètres de modification de la qualité de l’utilisation** , sélectionnez **activer l’analyse des données QoE** , puis cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="f35f9-123">In the **Edit Quality of Experience (QoE) Setting** pane, select **Enable monitoring of QoE data** and then click **Commit**.</span></span>

<span data-ttu-id="f35f9-124">Comme indiqué précédemment, les exemples précédents permettent de surveiller au niveau de l’étendue globale ; en d’autres, ils autorisent le contrôle CDR et QoE au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f35f9-124">As noted, the preceding examples enable monitoring at the global scope; that is, they enable CDR and QoE monitoring throughout your organization.</span></span> <span data-ttu-id="f35f9-125">Vous pouvez également créer des paramètres de configuration de CDR et QoE séparés sur l’étendue du site, puis activer ou désactiver de manière sélective le contrôle de chaque site.</span><span class="sxs-lookup"><span data-stu-id="f35f9-125">Alternatively, you can create separate CDR and QoE configuration settings at the site scope, and then selectively enable or disable monitoring for each site.</span></span> <span data-ttu-id="f35f9-126">Par exemple, vous pouvez activer le contrôle de CDR pour votre site de Redmond, mais désactiver le contrôle CDR pour votre site de Dublin.</span><span class="sxs-lookup"><span data-stu-id="f35f9-126">For example, you could enable CDR monitoring for your Redmond site, yet disable CDR monitoring for your Dublin site.</span></span> <span data-ttu-id="f35f9-127">Pour plus d’informations sur la gestion de vos paramètres de configuration de la surveillance, voir le Guide de déploiement [Configuration des paramètres d’enregistrement des détails des appels et de la qualité de l’utilisation dans Lync Server 2013](lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md).</span><span class="sxs-lookup"><span data-stu-id="f35f9-127">For more information on managing your monitoring configuration settings, see the Deployment guide topic [Configuring call detail recording and Quality of Experience settings in Lync Server 2013](lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md).</span></span>

<span data-ttu-id="f35f9-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f35f9-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

