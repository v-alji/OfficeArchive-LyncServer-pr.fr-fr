---
title: 'Lync Server 2013 : Création d’une topologie de serveurs Edge et directeurs'
description: 'Lync Server 2013 : création d’une topologie de périphérie et de directeur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Building an edge and Director topology
ms:assetid: 11e5759e-d69f-4c39-8994-f467c279c558
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398202(v=OCS.15)
ms:contentKeyID: 48183451
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bcb2d422136cf0a421c68ebc2adba50f03c5cc85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435935"
---
# <a name="building-an-edge-and-director-topology-in-lync-server-2013"></a><span data-ttu-id="f3b1f-103">Création d’une topologie de serveurs Edge et directeurs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3b1f-103">Building an edge and Director topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3b1f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3b1f-104">

<span> </span></span></span>

<span data-ttu-id="f3b1f-105">_**Dernière modification de la rubrique :** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="f3b1f-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="f3b1f-106">La création de la topologie implique les tâches de planification et de déploiement suivantes :</span><span class="sxs-lookup"><span data-stu-id="f3b1f-106">Building the topology involves the following planning and deployment tasks:</span></span>

  - <span data-ttu-id="f3b1f-107">**Planning**   Vous devez définir une topologie appropriée pour votre organisation et identifier les composants requis pour la déployer.</span><span class="sxs-lookup"><span data-stu-id="f3b1f-107">**Planning**   You need to define an appropriate topology for your organization and identify the components required to deploy it.</span></span> <span data-ttu-id="f3b1f-108">Voici les étapes standard du processus de planification.</span><span class="sxs-lookup"><span data-stu-id="f3b1f-108">These are standard steps in the planning process.</span></span> <span data-ttu-id="f3b1f-109">L’outil de planification de Microsoft Lync Server 2013, fourni avec Lync Server 2013, simplifie le démarrage du processus de planification, ainsi que la possibilité d’apporter facilement des modifications à la fin de vos exigences et plans.</span><span class="sxs-lookup"><span data-stu-id="f3b1f-109">The Microsoft Lync Server 2013, Planning Tool provided with Lync Server 2013 makes it easy to start the planning process, as well as including the ability to easily make changes as your requirements and plans are finalized.</span></span>

  - <span data-ttu-id="f3b1f-110">**Déploiement**   La topologie que vous définissez à l’aide du générateur de topologie est essentielle pour le déploiement de n’importe quel serveur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f3b1f-110">**Deployment**   The topology that you define using Topology Builder is essential to the deployment of any Lync Server 2013 server.</span></span> <span data-ttu-id="f3b1f-111">Si vous n’avez pas fini de définir et de publier votre topologie à l’aide du générateur de topologie dans le cadre de vos efforts de planification, vous devez la terminer et publier la topologie avant de déployer vos serveurs Edge.</span><span class="sxs-lookup"><span data-stu-id="f3b1f-111">If you do not finish defining and publishing your topology by using Topology Builder as part of your planning efforts, you must complete it and publish the topology before you deploy your Edge Servers.</span></span>

<span data-ttu-id="f3b1f-112">Vous ne pouvez pas déployer les composants du serveur Edge tant que vous n’avez pas déployé au moins un pool interne et vous devez installer le générateur de topologie pour déployer un pool interne.</span><span class="sxs-lookup"><span data-stu-id="f3b1f-112">You cannot deploy Edge Server components until you have deployed at least one internal pool, and you must install Topology Builder to deploy an internal pool.</span></span> <span data-ttu-id="f3b1f-113">Cette section ne couvre pas l’installation du générateur de topologie, car elle fait partie du processus d’installation du pool interne.</span><span class="sxs-lookup"><span data-stu-id="f3b1f-113">This section does not cover installation of Topology Builder because that is part of the installation process for the internal pool.</span></span>

<span data-ttu-id="f3b1f-114">Pour plus d’informations sur ces outils, voir [liste de vérification de déploiement pour l’accès des utilisateurs externes dans Lync Server 2013](lync-server-2013-deployment-checklist-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="f3b1f-114">For details about these tools, see [Deployment checklist for external user access in Lync Server 2013](lync-server-2013-deployment-checklist-for-external-user-access.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f3b1f-115">Si vous avez déjà utilisé le générateur de topologie pour définir une topologie complète, y compris la topologie de bord, vous pouvez ignorer la <A href="lync-server-2013-define-your-edge-topology.md">topologie de définition de votre topologie Edge dans Lync server 2013</A> et <A href="lync-server-2013-publish-your-topology.md">publier votre topologie dans les tâches 2013 serveur Lync</A> de cette section, mais vous devez effectuer l' <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">exportation de votre topologie Lync Server 2013 et la copier vers le média externe pour la tâche d’installation Edge</A> .</span><span class="sxs-lookup"><span data-stu-id="f3b1f-115">If you previously used Topology Builder to define a complete topology, including the edge topology, you do can skip the <A href="lync-server-2013-define-your-edge-topology.md">Define your edge topology in Lync Server 2013</A> and <A href="lync-server-2013-publish-your-topology.md">Publish your topology in Lync Server 2013</A> tasks in this section, but you do need to complete the <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">Export your Lync Server 2013 topology and copy it to external media for edge installation</A> task.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f3b1f-116">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f3b1f-116">In This Section</span></span>

  - [<span data-ttu-id="f3b1f-117">Définition de la topologie Edge dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3b1f-117">Define your edge topology in Lync Server 2013</span></span>](lync-server-2013-define-your-edge-topology.md)

  - [<span data-ttu-id="f3b1f-118">Définition des topologies facultatives de directeur dans votre topologie pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3b1f-118">Define optional Director topologies in your topology for Lync Server 2013</span></span>](lync-server-2013-define-optional-director-topologies-in-your-topology.md)

  - [<span data-ttu-id="f3b1f-119">Publication de la topologie dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3b1f-119">Publish your topology in Lync Server 2013</span></span>](lync-server-2013-publish-your-topology.md)

  - [<span data-ttu-id="f3b1f-120">Exportation de la topologie Lync Server 2013 et copie vers le support externe de l’installation Edge</span><span class="sxs-lookup"><span data-stu-id="f3b1f-120">Export your Lync Server 2013 topology and copy it to external media for edge installation</span></span>](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)

<span data-ttu-id="f3b1f-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3b1f-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

