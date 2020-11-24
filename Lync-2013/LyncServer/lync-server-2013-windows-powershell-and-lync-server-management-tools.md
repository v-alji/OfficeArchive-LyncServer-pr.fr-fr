---
title: 'Lync Server 2013 : Outils de gestion de Windows PowerShell et Lync Server 2013'
description: 'Lync Server 2013 : outils de gestion de Windows PowerShell et de Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Windows PowerShell and Lync Server 2013 management tools
ms:assetid: 6a285f7c-0ef5-4cab-9976-d03be276e35d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481130(v=OCS.15)
ms:contentKeyID: 59893869
ms.date: 07/20/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11c8d63974ad05a041eb446182cbc7f9336044b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394461"
---
# <a name="windows-powershell-and-lync-server-2013-management-tools"></a><span data-ttu-id="8b2ad-103">Outils de gestion de Windows PowerShell et Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8b2ad-103">Windows PowerShell and Lync Server 2013 management tools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8b2ad-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8b2ad-104">

<span> </span></span></span>

<span data-ttu-id="8b2ad-105">_**Dernière modification de la rubrique :** 2016-07-20_</span><span class="sxs-lookup"><span data-stu-id="8b2ad-105">_**Topic Last Modified:** 2016-07-20_</span></span>

<span data-ttu-id="8b2ad-106">Dans Microsoft Lync Server 2013, les outils de gestion sont implémentés à l’aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-106">In Microsoft Lync Server 2013, management tools are implemented using Windows PowerShell.</span></span> <span data-ttu-id="8b2ad-107">Windows PowerShell inclut un environnement de ligne de commande, des commandes spécifiques au produit et un langage de script complet.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-107">Windows PowerShell includes a command-line environment, product-specific commands, and a full scripting language.</span></span> <span data-ttu-id="8b2ad-108">Les outils Lync Server 2013 implémentés à l’aide de Windows PowerShell incluent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8b2ad-108">Lync Server 2013 tools that are implemented using Windows PowerShell include the following:</span></span>

  - <span data-ttu-id="8b2ad-109">**Générateur de topologie**.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-109">**Topology Builder**.</span></span> <span data-ttu-id="8b2ad-110">Le générateur de topologie vous permet de créer, d’ajuster et de publier votre topologie planifiée et de valider votre topologie avant de commencer les installations serveur.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-110">You use Topology Builder to create, adjust, and publish your planned topology, and it validates your topology before you begin server installations.</span></span> <span data-ttu-id="8b2ad-111">Lorsque vous installez Lync Server 2013 sur des serveurs individuels, les serveurs lisent la topologie publiée dans le cadre du processus d’installation, et le programme d’installation déploie le serveur conformément aux instructions de la topologie.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-111">When you install Lync Server 2013 on individual servers, the servers read the published topology as part of the installation process, and the installation program deploys the server as directed in the topology.</span></span> <span data-ttu-id="8b2ad-112">After setup, configuration information is automatically replicated to all servers.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-112">After setup, configuration information is automatically replicated to all servers.</span></span> <span data-ttu-id="8b2ad-113">Components can be added to your deployment only by using Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-113">Components can be added to your deployment only by using Topology Builder.</span></span>

  - <span data-ttu-id="8b2ad-114">**Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-114">**Lync Server Management Shell**.</span></span> <span data-ttu-id="8b2ad-115">Vous pouvez utiliser Lync Server Management Shell pour une gestion complète de votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-115">You can use Lync Server Management Shell for full command-line management of your deployment.</span></span>

  - <span data-ttu-id="8b2ad-116">**Panneau de configuration de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-116">**Lync Server Control Panel**.</span></span> <span data-ttu-id="8b2ad-117">Vous pouvez utiliser l’interface utilisateur du panneau de configuration Microsoft Lync Server 2013 pour gérer les tâches les plus courantes dans votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-117">You can use the Microsoft Lync Server 2013 Control Panel user interface to manage the most common tasks in your deployment.</span></span>

<span data-ttu-id="8b2ad-118">Ces outils utilisent des cmdlets Windows PowerShell pour la gestion de votre déploiement, y compris des applets de applet 550 spécifiques au produit.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-118">These tools use Windows PowerShell cmdlets for management of your deployment, including close to 550 product-specific cmdlets.</span></span> <span data-ttu-id="8b2ad-119">Les applets de vérification intégrés à Lync Server 2013 servent essentiellement à gérer l’authentification, ainsi que les droits et les autorisations des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-119">The security cmdlets included in Lync Server 2013 are primarily used to manage authentication, and user rights and permissions.</span></span> <span data-ttu-id="8b2ad-120">Une vaste gamme d’applets de commande est disponible pour gérer l’authentification, dont des applets de commande pour l’authentification de certificats et de codes confidentiels (PIN).</span><span class="sxs-lookup"><span data-stu-id="8b2ad-120">A wide variety of cmdlets are available for managing authentication, including cmdlets for certificate and personal identification number (PIN) authentication.</span></span> <span data-ttu-id="8b2ad-121">De plus, un certain nombre d’applets de commande vous permettent d’utiliser la nouvelle fonctionnalité de contrôle d’accès Role-Based (RBAC) pour déléguer le contrôle d’administration de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-121">In addition, a number of cmdlets enable you to use the new Role-Based Access Control (RBAC) feature to delegate administrative control of Lync Server 2013.</span></span> <span data-ttu-id="8b2ad-122">Pour plus d’informations sur les applets de connexion Lync Server, voir [Lync server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md).</span><span class="sxs-lookup"><span data-stu-id="8b2ad-122">For details about the Lync Server cmdlets, see [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md).</span></span>

<span data-ttu-id="8b2ad-123">Les fonctionnalités de sécurité de script pour Windows PowerShell sont spécifiquement conçues pour éviter certains problèmes de sécurité liés au script des technologies plus anciennes, y compris Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="8b2ad-123">The script security features for Windows PowerShell are specifically designed to help prevent some of the scripting-related security problems of older technologies, including Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="8b2ad-124">Les fonctionnalités de sécurité de Windows PowerShell sont conçues pour créer un environnement dans lequel les utilisateurs ne peuvent pas facilement exécuter de scripts ou sans le savoir.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-124">The Windows PowerShell security features are intended to create an environment in which users cannot easily or unknowingly run scripts.</span></span> <span data-ttu-id="8b2ad-125">Par défaut, les fonctionnalités de sécurité de Windows PowerShell sont activées.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-125">By default, Windows PowerShell security features are enabled.</span></span> <span data-ttu-id="8b2ad-126">Vous pouvez modifier l’état de ces fonctionnalités pour les adapter à vos besoins de script et à divers objectifs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-126">You can modify the state of those features to accommodate your scripting needs and a variety of security goals.</span></span> <span data-ttu-id="8b2ad-127">Cela ne veut pas dire que le shell empêche les utilisateurs d’exécuter des scripts.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-127">This is not to say that the shell makes it impossible for users to run scripts.</span></span> <span data-ttu-id="8b2ad-128">Mais plutôt, il est plus difficile, par défaut, pour les utilisateurs d’exécuter des scripts sans en avoir conscience.</span><span class="sxs-lookup"><span data-stu-id="8b2ad-128">Rather, the shell makes it difficult—by default—for users to run scripts without realizing they are doing so.</span></span> <span data-ttu-id="8b2ad-129">Pour plus d’informations, consultez sécurité du script Windows PowerShell à l’adresse [https://go.microsoft.com/fwlink/p/?LinkId=213145](https://go.microsoft.com/fwlink/p/?linkid=213145) .</span><span class="sxs-lookup"><span data-stu-id="8b2ad-129">For details, see Windows PowerShell Script Security at [https://go.microsoft.com/fwlink/p/?LinkId=213145](https://go.microsoft.com/fwlink/p/?linkid=213145).</span></span>

<span data-ttu-id="8b2ad-130"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8b2ad-130"></div>

<span> </span>

</div>

</div>

</span></span></div>

