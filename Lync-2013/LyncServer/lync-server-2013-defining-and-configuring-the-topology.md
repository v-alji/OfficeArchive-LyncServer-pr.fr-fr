---
title: 'Lync Server 2013 : Définition et configuration de la topologie'
description: 'Lync Server 2013 : définition et configuration de la topologie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining and configuring the topology
ms:assetid: 51d1601e-4f83-48d4-ad08-3b4d5e2003aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398339(v=OCS.15)
ms:contentKeyID: 48184146
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec444a1ddf434c5a80fdc2d56bdba27573da14ab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431000"
---
# <a name="defining-and-configuring-the-topology-in-lync-server-2013"></a><span data-ttu-id="64870-103">Définition et configuration de la topologie dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64870-103">Defining and configuring the topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="64870-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="64870-104">

<span> </span></span></span>

<span data-ttu-id="64870-105">_**Dernière modification de la rubrique :** 2012-09-14_</span><span class="sxs-lookup"><span data-stu-id="64870-105">_**Topic Last Modified:** 2012-09-14_</span></span>

<span data-ttu-id="64870-106">Vous définissez et configurez votre topologie à l’aide du générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="64870-106">You define and configure your topology by using Topology Builder.</span></span> <span data-ttu-id="64870-107">Le générateur de topologie ne doit pas nécessairement être membre du groupe Administrateurs local ou d’un groupe de domaine privilégié (par exemple, administrateurs de domaine).</span><span class="sxs-lookup"><span data-stu-id="64870-107">Topology Builder does not require you to be a member of the local Administrators group or a privileged domain group (such as Domain Admins).</span></span> <span data-ttu-id="64870-108">Vous pouvez définir votre topologie en tant qu’utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="64870-108">You can define your topology as a standard user.</span></span> <span data-ttu-id="64870-109">Lorsque vous démarrez le générateur de topologie lors de la première utilisation et des sessions d’édition ultérieures, vous êtes invité à indiquer l’emplacement où vous voulez que le générateur de topologie charge le document de configuration actuel.</span><span class="sxs-lookup"><span data-stu-id="64870-109">When you start Topology Builder on first use and subsequent edit sessions, you are prompted for the location where you want Topology Builder to load the current configuration document.</span></span> <span data-ttu-id="64870-110">Les choix possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="64870-110">The choices are the following:</span></span>

  - <span data-ttu-id="64870-111">Téléchargement de la topologie à partir d’un déploiement existant</span><span class="sxs-lookup"><span data-stu-id="64870-111">Download topology from existing deployment</span></span>

  - <span data-ttu-id="64870-112">Ouvrir la topologie à partir d’un fichier local</span><span class="sxs-lookup"><span data-stu-id="64870-112">Open topology from a local file</span></span>

  - <span data-ttu-id="64870-113">Nouvelle topologie</span><span class="sxs-lookup"><span data-stu-id="64870-113">New topology</span></span>

<span data-ttu-id="64870-114">Si vous avez déjà défini une topologie et que vous avez établi la Banque centrale de gestion, vous devez choisir de télécharger une topologie à partir d’un déploiement existant.</span><span class="sxs-lookup"><span data-stu-id="64870-114">If you have already defined a topology and have established the Central Management store, you should choose to download a topology from an existing deployment.</span></span> <span data-ttu-id="64870-115">Le générateur de topologie lira la base de données et récupérera la définition actuelle.</span><span class="sxs-lookup"><span data-stu-id="64870-115">Topology Builder will read the database and retrieve the current definition.</span></span> <span data-ttu-id="64870-116">Si vous avez déjà un magasin central de gestion, vous devez toujours choisir cette option.</span><span class="sxs-lookup"><span data-stu-id="64870-116">If you have an existing Central Management store, you should always choose this option.</span></span>

<span data-ttu-id="64870-117">Si vous n’avez pas établi de magasin de gestion central et voulez modifier une configuration déjà enregistrée, vous devez choisir d’ouvrir la topologie à partir d’un fichier local.</span><span class="sxs-lookup"><span data-stu-id="64870-117">If you have not established a Central Management store and want to edit a previously saved configuration, you should choose to open the topology from a local file.</span></span> <span data-ttu-id="64870-118">Le fichier que vous allez ouvrir sera le fichier de configuration enregistré dans une session précédente.</span><span class="sxs-lookup"><span data-stu-id="64870-118">The file that you will open would be the configuration file that was saved in a previous session.</span></span> <span data-ttu-id="64870-119">Vous pouvez utiliser cette option pour modifier la topologie précédemment enregistrée.</span><span class="sxs-lookup"><span data-stu-id="64870-119">You can use this option to edit the previously saved topology.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="64870-120">Si vous disposez déjà d’une topologie publiée, vous ne devez pas charger de fichier de configuration local.</span><span class="sxs-lookup"><span data-stu-id="64870-120">If you already have a published topology, you should not load a local configuration file.</span></span> <span data-ttu-id="64870-121">Vous devez choisir de télécharger la topologie à partir d’un déploiement existant.</span><span class="sxs-lookup"><span data-stu-id="64870-121">You should choose to download the topology from an existing deployment.</span></span>



</div>

<span data-ttu-id="64870-122">Choisissez de créer une nouvelle topologie si vous voulez créer une nouvelle configuration de générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="64870-122">Choose to create a new topology, if you want to create a new Topology Builder configuration.</span></span> <span data-ttu-id="64870-123">Une conception déjà enregistrée n’est pas remplacée, sauf si vous choisissez de l’enregistrer dans le même fichier que celui que vous avez créé lors d’une session de conception antérieure.</span><span class="sxs-lookup"><span data-stu-id="64870-123">A previously saved design is not overwritten unless you choose to save it as the same file that you created in an earlier design session.</span></span>

<span data-ttu-id="64870-124">Dans chacune de ces options, vous êtes invité à fournir un emplacement pour le stockage du fichier de configuration du générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="64870-124">In each of these options, you will be prompted for a location to store the Topology Builder configuration file.</span></span> <span data-ttu-id="64870-125">L’emplacement du fichier peut correspondre à un emplacement local, à un emplacement partagé sur un partage de fichiers établi ou un média amovible.</span><span class="sxs-lookup"><span data-stu-id="64870-125">The location for the file could be a local location, a shared location on an established file share, or removable media.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="64870-126">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="64870-126">In This Section</span></span>

  - [<span data-ttu-id="64870-127">Définition et configuration d’une topologie dans le générateur de topologie pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64870-127">Define and configure a topology in Topology Builder for Lync Server 2013</span></span>](lync-server-2013-define-and-configure-a-topology-in-topology-builder.md)

  - [<span data-ttu-id="64870-128">Définition et configuration d’un pool frontal ou d’un serveur Standard Edition dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64870-128">Define and configure a Front End pool or Standard Edition server in Lync Server 2013</span></span>](lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md)

  - [<span data-ttu-id="64870-129">Déploiement de pools frontaux couplés pour la récupération d’urgence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64870-129">Deploying paired Front End pools for disaster recovery in Lync Server 2013</span></span>](lync-server-2013-deploying-paired-front-end-pools-for-disaster-recovery.md)

  - [<span data-ttu-id="64870-130">Déploiement de la mise en miroir SQL pour la haute disponibilité des serveurs principaux dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64870-130">Deploying SQL mirroring for Back End Server high availability in Lync Server 2013</span></span>](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md)

  - [<span data-ttu-id="64870-131">Modification ou configuration des URL simples dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64870-131">Edit or configure simple URLs in Lync Server 2013</span></span>](lync-server-2013-edit-or-configure-simple-urls.md)

  - [<span data-ttu-id="64870-132">Sélection du serveur de gestion centralisée dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64870-132">Select the Central Management Server in Lync Server 2013</span></span>](lync-server-2013-select-the-central-management-server.md)

<span data-ttu-id="64870-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="64870-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

