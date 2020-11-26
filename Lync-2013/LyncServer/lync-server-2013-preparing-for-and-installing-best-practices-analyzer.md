---
title: 'Lync Server 2013 : préparation et installation des meilleures pratiques Analyzer'
description: 'Lync Server 2013 : préparation de l’analyseur de meilleures pratiques et installation'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing for and installing Best Practices Analyzer
ms:assetid: 550613dd-dc08-482e-9980-a3fe187cd162
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg591347(v=OCS.15)
ms:contentKeyID: 48184149
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 005c5ac372a3564e74af549832830ebae899e9d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424141"
---
# <a name="preparing-for-and-installing-best-practices-analyzer-in-lync-server-2013"></a><span data-ttu-id="58d91-103">Préparation de l’analyseur de meilleures pratiques et de son installation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="58d91-103">Preparing for and installing Best Practices Analyzer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="58d91-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="58d91-104">

<span> </span></span></span>

<span data-ttu-id="58d91-105">_**Dernière modification de la rubrique :** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="58d91-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="58d91-106">Pour effectuer les tâches décrites dans cette rubrique, vous devez être connecté en tant que membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="58d91-106">You must be logged on as a member of the Administrators group to perform the tasks that are described in this topic.</span></span>

<div>

## <a name="system-requirements-for-best-practices-analyzer-installation"></a><span data-ttu-id="58d91-107">Configuration système requise pour l’installation de l’analyseur de meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="58d91-107">System Requirements for Best Practices Analyzer Installation</span></span>

<span data-ttu-id="58d91-108">Pour exécuter Lync Server 2013, le protocole recommandé Analyzer pour analyser votre environnement, l’ordinateur doit exécuter une édition 64 bits d’un des systèmes d’exploitation suivants :</span><span class="sxs-lookup"><span data-stu-id="58d91-108">To run Lync Server 2013, Best Practices Analyzer to scan your environment, the computer must be running a 64-bit edition of one of the following operating systems:</span></span>

  - <span data-ttu-id="58d91-109">Système d’exploitation standard de Windows Server 2008 R2 avec Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="58d91-109">Windows Server 2008 R2 with Service Pack 1 (SP1) Standard operating system</span></span>

  - <span data-ttu-id="58d91-110">Système d’exploitation Windows Server 2008 R2 avec SP1 entreprise</span><span class="sxs-lookup"><span data-stu-id="58d91-110">Windows Server 2008 R2 with SP1 Enterprise operating system</span></span>

  - <span data-ttu-id="58d91-111">Système d’exploitation Windows Server 2008 R2 avec SP1 Datacenter</span><span class="sxs-lookup"><span data-stu-id="58d91-111">Windows Server 2008 R2 with SP1 Datacenter operating system</span></span>

  - <span data-ttu-id="58d91-112">Système d’exploitation Windows Server 2012 Datacenter</span><span class="sxs-lookup"><span data-stu-id="58d91-112">Windows Server 2012 Datacenter operating system</span></span>

  - <span data-ttu-id="58d91-113">Système d’exploitation Windows Server 2012 standard</span><span class="sxs-lookup"><span data-stu-id="58d91-113">Windows Server 2012 Standard operating system</span></span>

  - <span data-ttu-id="58d91-114">Système d’exploitation Windows Server 2012 entreprise</span><span class="sxs-lookup"><span data-stu-id="58d91-114">Windows Server 2012 Enterprise operating system</span></span>

  - <span data-ttu-id="58d91-115">Système d’exploitation Windows Server 2012 R2 Datacenter</span><span class="sxs-lookup"><span data-stu-id="58d91-115">Windows Server 2012 R2 Datacenter operating system</span></span>

  - <span data-ttu-id="58d91-116">Système d’exploitation Windows Server 2012 R2 Standard</span><span class="sxs-lookup"><span data-stu-id="58d91-116">Windows Server 2012 R2 Standard operating system</span></span>

  - <span data-ttu-id="58d91-117">Système d’exploitation Windows Server 2012 R2 entreprise</span><span class="sxs-lookup"><span data-stu-id="58d91-117">Windows Server 2012 R2 Enterprise operating system</span></span>

  - <span data-ttu-id="58d91-118">Système d’exploitation Windows 8</span><span class="sxs-lookup"><span data-stu-id="58d91-118">Windows 8 operating system</span></span>

  - <span data-ttu-id="58d91-119">Système d’exploitation Windows 7</span><span class="sxs-lookup"><span data-stu-id="58d91-119">Windows 7 operating system</span></span>

<span data-ttu-id="58d91-120">L’ordinateur doit également exécuter les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="58d91-120">The computer must also be running the following:</span></span>

  - <span data-ttu-id="58d91-121">Microsoft .NET Framework 4,5.</span><span class="sxs-lookup"><span data-stu-id="58d91-121">Microsoft .NET Framework 4.5.</span></span> <span data-ttu-id="58d91-122">Pour Lync Server 2013, vous devez installer manuellement l’édition 64 bits de Microsoft .NET Framework 4,5 sur le serveur avant de procéder à l’installation de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="58d91-122">For Lync Server 2013, you must manually install the 64-bit edition of Microsoft .NET Framework 4.5 on the server prior to installing Lync Server 2013.</span></span>

  - <span data-ttu-id="58d91-123">Lync Server 2013, composants principaux.</span><span class="sxs-lookup"><span data-stu-id="58d91-123">Lync Server 2013, Core Components.</span></span>

  - <span data-ttu-id="58d91-124">Package de compatibilité descendante WMI.</span><span class="sxs-lookup"><span data-stu-id="58d91-124">WMI Backward Compatibility Package.</span></span> <span data-ttu-id="58d91-125">Pour plus d’informations, voir [installer le package de compatibilité descendante WMI](install-wmi-backward-compatibility-package.md) dans la documentation relative à la migration.</span><span class="sxs-lookup"><span data-stu-id="58d91-125">For details, see [Install WMI Backward Compatibility package](install-wmi-backward-compatibility-package.md) in the Migration documentation.</span></span>

  - <span data-ttu-id="58d91-126">Windows PowerShell 3,0.</span><span class="sxs-lookup"><span data-stu-id="58d91-126">Windows PowerShell 3.0.</span></span> <span data-ttu-id="58d91-127">Pour plus d’informations, consultez [installation de Windows PowerShell 3,0 pour Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md) dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="58d91-127">For details, see [Installing Windows PowerShell 3.0 for Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md) in the Deployment documentation.</span></span>

<span data-ttu-id="58d91-128">Vous pouvez installer le vérificateur de meilleures pratiques sur les ordinateurs dotés d’un système d’exploitation pris en charge qui n’exécute pas Lync Server 2013, les composants principaux ou le package de compatibilité descendante WMI, mais vous pouvez utiliser l’analyseur de recommandations</span><span class="sxs-lookup"><span data-stu-id="58d91-128">You can install Best Practices Analyzer on computers with a supported operating system that are not running Lync Server 2013, Core Components or WMI Backward Compatibility Package, but you can use Best Practices Analyzer on those computers only to view reports, not to run scans.</span></span>

</div>

<div>

## <a name="choosing-a-computer-for-installation"></a><span data-ttu-id="58d91-129">Choix d’un ordinateur pour l’installation</span><span class="sxs-lookup"><span data-stu-id="58d91-129">Choosing a Computer for Installation</span></span>

<span data-ttu-id="58d91-130">Nous vous recommandons d’installer Lync Server 2013, le protocole recommandé Analyzer sur un ordinateur dédié à la gestion de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="58d91-130">We recommend that you install Lync Server 2013, Best Practices Analyzer on a computer that is dedicated to Lync Server 2013 management.</span></span> <span data-ttu-id="58d91-131">Vous pouvez installer l’outil sur un serveur exécutant Lync Server 2013 ou un ordinateur d’administration exécutant les outils d’administration de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="58d91-131">You can install the tool on a server running Lync Server 2013 or an administrative computer running Lync Server 2013 administrative tools.</span></span> <span data-ttu-id="58d91-132">Si vous installez l’outil sur un serveur exécutant Lync Server, nous vous conseillons d’utiliser l’outil pour analyser uniquement ce serveur.</span><span class="sxs-lookup"><span data-stu-id="58d91-132">If you install the tool on a server that is running Lync Server, we recommend that you use the tool to scan only that server.</span></span>

</div>

<div>

## <a name="installing-best-practices-analyzer"></a><span data-ttu-id="58d91-133">Installation de l’analyseur de meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="58d91-133">Installing Best Practices Analyzer</span></span>

<span data-ttu-id="58d91-134">Vous pouvez télécharger le recommandations Analyzer pour Lync Server 2013 à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=266539](https://go.microsoft.com/fwlink/p/?linkid=266539) .</span><span class="sxs-lookup"><span data-stu-id="58d91-134">You can download the Best Practices Analyzer for Lync Server 2013 at [https://go.microsoft.com/fwlink/p/?linkId=266539](https://go.microsoft.com/fwlink/p/?linkid=266539).</span></span>

<span data-ttu-id="58d91-135">Pour installer le vérificateur de meilleures pratiques, démarrez le fichier Microsoft installer RtcBPA.msi sur l’ordinateur sur lequel vous souhaitez installer l’outil, puis suivez les instructions à l’écran.</span><span class="sxs-lookup"><span data-stu-id="58d91-135">To install Best Practices Analyzer, start the Microsoft Installer file RtcBPA.msi on the computer where you want to install the tool, and then follow the instructions on the screen.</span></span> <span data-ttu-id="58d91-136">L’emplacement par défaut pour l’installation des fichiers programme est \<system drive\> \\ Program Files \\ Lync Server 2013 \\ BPA.</span><span class="sxs-lookup"><span data-stu-id="58d91-136">The default location for installing the program files is \<system drive\>\\Program Files\\Lync Server 2013\\BPA.</span></span>

<span data-ttu-id="58d91-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="58d91-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

