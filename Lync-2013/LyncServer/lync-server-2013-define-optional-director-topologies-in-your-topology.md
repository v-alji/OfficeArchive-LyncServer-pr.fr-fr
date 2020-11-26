---
title: 'Lync Server 2013 : Définition des topologies facultatives de directeur dans votre topologie'
description: 'Lync Server 2013 : définir des topologies de réalisateur facultatives dans votre topologie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define optional Director topologies in your topology
ms:assetid: 8e9a659d-23b0-401d-b296-59c7df414d49
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398717(v=OCS.15)
ms:contentKeyID: 48184808
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5bc82108d4277969489739fc81db07ec6f96bb96
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431049"
---
# <a name="define-optional-director-topologies-in-your-topology-for-lync-server-2013"></a><span data-ttu-id="b26e6-103">Définition des topologies facultatives de directeur dans votre topologie pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b26e6-103">Define optional Director topologies in your topology for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b26e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b26e6-104">

<span> </span></span></span>

<span data-ttu-id="b26e6-105">_**Dernière modification de la rubrique :** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="b26e6-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="b26e6-106">Les directeurs Lync Server 2013 peuvent être des serveurs à instance unique qui peuvent être installés en tant que pool équilibré en charge de plusieurs directeurs pour une disponibilité et une capacité plus élevées.</span><span class="sxs-lookup"><span data-stu-id="b26e6-106">Lync Server 2013 Directors can be single-instance servers or they can be installed as a load-balanced pool of multiple Directors for higher availability and capacity.</span></span> <span data-ttu-id="b26e6-107">L’équilibrage de charge matérielle et l’équilibrage de charge DNS (Domain Name System) sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b26e6-107">Both hardware load balancing and Domain Name System (DNS) load balancing are supported.</span></span> <span data-ttu-id="b26e6-108">Cet article explique comment configurer l’équilibrage de charge DNS pour les pools de directeurs.</span><span class="sxs-lookup"><span data-stu-id="b26e6-108">This topic explains how to configure DNS load balancing for Director pools.</span></span>

<span data-ttu-id="b26e6-109">Pour réussir la publication, l’activation ou la désactivation d’une topologie lors de l’ajout ou de la suppression d’un rôle serveur, vous devez être connecté en tant qu’utilisateur membre des groupes **RTCUniversalServerAdmins** et **Admins du domaine** .</span><span class="sxs-lookup"><span data-stu-id="b26e6-109">To successfully publish, enable, or disable a topology when you add or remove a server role, you should be logged on as a user who is a member of the **RTCUniversalServerAdmins** and **Domain Admins** groups.</span></span> <span data-ttu-id="b26e6-110">Vous pouvez également déléguer les droits d’administrateur et les autorisations appropriés pour ajouter des rôles de serveur.</span><span class="sxs-lookup"><span data-stu-id="b26e6-110">You can also delegate the proper administrator rights and permissions for adding server roles.</span></span> <span data-ttu-id="b26e6-111">Pour plus d’informations, reportez-vous à la section [délégation des autorisations de configuration dans Lync server 2013](lync-server-2013-delegate-setup-permissions.md) dans la documentation de déploiement Standard Edition Server ou Enterprise Edition Server.</span><span class="sxs-lookup"><span data-stu-id="b26e6-111">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md) in the Standard Edition server or Enterprise Edition server Deployment documentation.</span></span> <span data-ttu-id="b26e6-112">Pour les autres modifications de configuration, seule l’appartenance au groupe **RTCUniversalServerAdmins** est requise.</span><span class="sxs-lookup"><span data-stu-id="b26e6-112">For other configuration changes, only membership in the **RTCUniversalServerAdmins** group is required.</span></span>

<span data-ttu-id="b26e6-113">Cette rubrique décrit les étapes permettant de définir et de publier la topologie pour les deux topologies de Director :</span><span class="sxs-lookup"><span data-stu-id="b26e6-113">This topic describes the steps to define and publish the topology for the two Director topologies:</span></span>

  - <span data-ttu-id="b26e6-114">Pour définir le directeur (instance unique)</span><span class="sxs-lookup"><span data-stu-id="b26e6-114">To define the Director (single instance)</span></span>

  - <span data-ttu-id="b26e6-115">Pour définir le directeur (pool de directeurs multiples)</span><span class="sxs-lookup"><span data-stu-id="b26e6-115">To define the Director (multiple Director pool)</span></span>

<div>

## <a name="to-define-the-director-single-instance"></a><span data-ttu-id="b26e6-116">Pour définir le directeur (instance unique)</span><span class="sxs-lookup"><span data-stu-id="b26e6-116">To define the Director (single instance)</span></span>

1.  <span data-ttu-id="b26e6-117">Démarrer le générateur de topologie : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Générateur de topologie de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-117">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="b26e6-118">Dans la page Bienvenue, cliquez sur **Télécharger la topologie à partir du déploiement existant**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-118">On the welcome page, click **Download Topology from Existing Deployment**.</span></span>

3.  <span data-ttu-id="b26e6-119">Dans la boîte de dialogue **enregistrer la topologie en tant que** , entrez le nom et l’emplacement de la copie locale de la topologie existante, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-119">In the **Save Topology As** dialog box, type the name and location of the local copy of the existing topology, and then click **Save**.</span></span>

4.  <span data-ttu-id="b26e6-120">Développez le site dans lequel vous envisagez d’ajouter le directeur, cliquez avec le bouton droit sur **pools de réalisateurs**, puis cliquez sur **nouvelle liste de répertoires**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-120">Expand the site in which you plan to add the Director, right-click **Director pools**, and then click **New Director Pool**.</span></span>

5.  <span data-ttu-id="b26e6-121">Dans la boîte de dialogue **définir le nom de domaine complet du pool de répertoires** , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b26e6-121">In the **Define the Director pool FQDN** dialog box, do the following:</span></span>
    
      - <span data-ttu-id="b26e6-122">Dans **nom de domaine complet (FQDN**) du pool, tapez le nom de domaine complet (FQDN) du pool</span><span class="sxs-lookup"><span data-stu-id="b26e6-122">In **Pool FQDN**, type the FQDN for the Director pool.</span></span>
    
      - <span data-ttu-id="b26e6-123">Cliquez sur **pool d’ordinateurs unique**, puis sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-123">Click **Single computer pool**, and then click **Next**.</span></span>

6.  <span data-ttu-id="b26e6-124">Dans la boîte de dialogue **définir le partage de fichiers** , effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b26e6-124">In the **Define the file share** dialog box, do one of the following:</span></span>
    
    1.  <span data-ttu-id="b26e6-125">Pour utiliser un partage de fichier existant, cliquez sur **utiliser un partage de fichiers déjà défini**, sélectionnez un partage de fichiers dans la liste, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-125">To use an existing file share, click **Use a previously defined file share**, select a file share from the list, and then click **Next**.</span></span>
    
    2.  <span data-ttu-id="b26e6-126">Pour créer un nouveau partage de fichiers, cliquez sur **définir un nouveau partage de fichier**, tapez le nom de domaine complet (FQDN) de l’emplacement du partage de fichiers dans **nom de domaine complet du serveur de fichiers**, tapez le nom du partage dans partage de **fichiers**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-126">To create a new file share, click **Define a new file share**, type the FQDN for the location of the file share in **File Server FQDN**, type the name of the share in **File Share**, and then click **Next**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b26e6-127">Le partage de fichiers que vous spécifiez ou créez dans cette étape doit exister ou être créé avant la publication de la topologie.</span><span class="sxs-lookup"><span data-stu-id="b26e6-127">The file share that you specify or create in this step must exist or be created prior to publishing the topology.</span></span><BR><span data-ttu-id="b26e6-128">Le partage de fichiers attribué à un directeur n’est pas utilisé pour vous permettre d’affecter le partage de fichiers de n’importe quel pool au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="b26e6-128">The file share assigned to a Director is not actually used, so you can assign the file share of any pool in the organization.</span></span>

    
    </div>

7.  <span data-ttu-id="b26e6-129">Dans la boîte de dialogue **spécifier l’URL du service Web** , dans **URL de base externe**, spécifiez le nom de domaine complet (FQDN) pour les directeurs, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-129">In the **Specify the Web Services URL** dialog box, in **External Base URL**, specify the FQDN for the Directors, and then click **Finish**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b26e6-130">Le nom doit pouvoir être résolu à partir des serveurs DNS Internet et pointe vers l’adresse IP publique du proxy inverse, qui écoute les demandes HTTP/HTTPs à cette URL et les transmet au répertoire virtuel des services Web externes de ce réalisateur.</span><span class="sxs-lookup"><span data-stu-id="b26e6-130">The name must be resolvable from Internet DNS servers and point to the public IP address of the reverse proxy, which listens for HTTP/HTTPS requests to that URL and proxies them to the external Web Services virtual directory on that Director.</span></span>

    
    </div>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="b26e6-131">Si vous avez plusieurs pools front-end ou serveur frontal, le nom de domaine complet des services Web externes doit être unique.</span><span class="sxs-lookup"><span data-stu-id="b26e6-131">If you have more than one Front End pool or Front End Server the external Web services FQDN must be unique.</span></span> <span data-ttu-id="b26e6-132">Par exemple, si vous définissez le nom de domaine complet des services Web externes d’un serveur frontal en tant que <STRONG>pool01.contoso.com</STRONG>, vous ne pouvez pas utiliser <STRONG>pool01.contoso.com</STRONG> pour un autre pool frontal ou serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="b26e6-132">For example, if you define the external Web services FQDN of a Front End Server as <STRONG>pool01.contoso.com</STRONG>, you cannot use <STRONG>pool01.contoso.com</STRONG> for another Front End pool or Front End Server.</span></span> <span data-ttu-id="b26e6-133">Si vous déployez également des directeurs, le nom de domaine complet des services Web externes défini pour n’importe quel directeur ou pool de réalisateur doit être unique à partir d’un autre directeur ou pool de directeurs, ainsi que sur n’importe quel pool frontal ou serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="b26e6-133">If you are also deploying Directors, the external Web services FQDN defined for any Director or Director pool must be unique from any other Director or Director pool as well as any Front End pool or Front End Server.</span></span> <span data-ttu-id="b26e6-134">Si vous décidez de remplacer les services Web internes par un nom de domaine complet autonome, chaque nom de domaine complet doit être unique à partir de n’importe quel autre pool frontal, directeur ou pool de réalisateur.</span><span class="sxs-lookup"><span data-stu-id="b26e6-134">If decide to override the Internal web services with a self-defined FQDN, each FQDN must be unique from any other Front End pool, Director or a Director pool.</span></span>

    
    </div>

8.  <span data-ttu-id="b26e6-135">Publiez la topologie.</span><span class="sxs-lookup"><span data-stu-id="b26e6-135">Publish the topology.</span></span>

</div>

<div>

## <a name="to-define-the-director-multiple-director-pool"></a><span data-ttu-id="b26e6-136">Pour définir le directeur (pool de directeurs multiples)</span><span class="sxs-lookup"><span data-stu-id="b26e6-136">To define the Director (multiple Director pool)</span></span>

1.  <span data-ttu-id="b26e6-137">Démarrer le générateur de topologie : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Générateur de topologie de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-137">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="b26e6-138">Dans la page Bienvenue, cliquez sur **Télécharger la topologie à partir du déploiement existant**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-138">On the welcome page, click **Download Topology from Existing Deployment**.</span></span>

3.  <span data-ttu-id="b26e6-139">Dans la boîte de dialogue **enregistrer la topologie en tant que** , entrez le nom et l’emplacement de la copie locale de la topologie existante, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-139">In the **Save Topology As** dialog box, type the name and location of the local copy of the existing topology, and then click **Save**.</span></span>

4.  <span data-ttu-id="b26e6-140">Développez le site dans lequel vous envisagez d’ajouter le directeur, cliquez avec le bouton droit sur **pools de réalisateurs**, puis cliquez sur **nouvelle liste de répertoires**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-140">Expand the site in which you plan to add the Director, right-click **Director pools**, and then click **New Director Pool**.</span></span>

5.  <span data-ttu-id="b26e6-141">Dans la boîte de dialogue **définir le nom de domaine complet du pool de répertoires** , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b26e6-141">In the **Define the Director pool FQDN** dialog box, do the following:</span></span>
    
      - <span data-ttu-id="b26e6-142">Dans **nom de domaine complet (FQDN**) du pool, tapez le nom de domaine complet (FQDN) du pool</span><span class="sxs-lookup"><span data-stu-id="b26e6-142">In **Pool FQDN**, type the FQDN for the Director pool.</span></span>
    
      - <span data-ttu-id="b26e6-143">Cliquez sur **plusieurs pools d’ordinateurs**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-143">Click **Multiple computer pool**, and then click **Next**.</span></span>

6.  <span data-ttu-id="b26e6-144">Dans la boîte de dialogue **définir les ordinateurs dans cette liste** , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b26e6-144">In the **Define the computers in this pool** dialog box, do the following:</span></span>
    
      - <span data-ttu-id="b26e6-145">Spécifiez le nom de domaine complet du premier membre de la liste, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-145">Specify the computer FQDN of the first pool member, and then click **Add**.</span></span>
    
      - <span data-ttu-id="b26e6-146">Répétez l’étape précédente pour chaque ordinateur que vous voulez ajouter.</span><span class="sxs-lookup"><span data-stu-id="b26e6-146">Repeat the previous step for each computer that you want to add.</span></span> <span data-ttu-id="b26e6-147">Lorsque vous avez terminé, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-147">When you are finished, click **Next**.</span></span>

7.  <span data-ttu-id="b26e6-148">Dans la boîte de dialogue **définir le partage de fichiers** , effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b26e6-148">In the **Define the file share** dialog box, do one of the following:</span></span>
    
      - <span data-ttu-id="b26e6-149">Pour utiliser un partage de fichier existant, cliquez sur **utiliser un partage de fichiers déjà défini**, sélectionnez un partage de fichiers dans la liste, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-149">To use an existing file share, click **Use a previously defined file share**, select a file share from the list, and then click **Next**.</span></span>
    
      - <span data-ttu-id="b26e6-150">Pour créer un nouveau partage de fichiers, cliquez sur **définir un nouveau partage de fichier**, tapez le nom de domaine complet (FQDN) de l’emplacement du partage de fichiers dans **nom de domaine complet du serveur de fichiers**, tapez le nom du partage dans partage de **fichiers**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-150">To create a new file share, click **Define a new file share**, type the FQDN for the location of the file share in **File Server FQDN**, type the name of the share in **File Share**, and then click **Next**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b26e6-151">Le partage de fichiers que vous spécifiez ou créez dans cette étape doit exister ou être créé avant la publication de la topologie.</span><span class="sxs-lookup"><span data-stu-id="b26e6-151">The file share that you specify or create in this step must exist or be created prior to publishing the topology.</span></span><BR><span data-ttu-id="b26e6-152">Le partage de fichiers attribué à un directeur n’est pas utilisé pour vous permettre d’affecter le partage de fichiers de n’importe quel pool au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="b26e6-152">The file share assigned to a Director is not actually used, so you can assign the file share of any pool in the organization.</span></span>

    
    </div>

8.  <span data-ttu-id="b26e6-153">Dans la boîte de dialogue **spécifier l’URL du service Web** , dans **URL de base externe**, spécifiez le nom de domaine complet (FQDN) pour les directeurs, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="b26e6-153">In the **Specify the Web Services URL** dialog box, in **External Base URL**, specify the FQDN for the Directors, and then click **Finish**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b26e6-154">Ce nom ne doit pas être résolu à partir des serveurs DNS Internet et pointe vers l’adresse IP publique du proxy inverse, qui écoute les requêtes HTTP/HTTPs envoyées à cette URL et les transmet au répertoire virtuel des services Web externes dans ce pool de répertoires.</span><span class="sxs-lookup"><span data-stu-id="b26e6-154">The name must be resolvable from Internet DNS servers and point to the public IP address of the reverse proxy, which listens for HTTP/HTTPS requests sent to that URL and proxies them to the external Web Services virtual directory on that Director pool.</span></span>

    
    </div>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="b26e6-155">Si vous avez plusieurs pools front-end ou serveur frontal, le nom de domaine complet des services Web externes doit être unique.</span><span class="sxs-lookup"><span data-stu-id="b26e6-155">If you have more than one Front End pool or Front End Server the external Web services FQDN must be unique.</span></span> <span data-ttu-id="b26e6-156">Par exemple, si vous définissez le nom de domaine complet des services Web externes d’un serveur frontal en tant que <STRONG>pool01.contoso.com</STRONG>, vous ne pouvez pas utiliser <STRONG>pool01.contoso.com</STRONG> pour un autre pool frontal ou serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="b26e6-156">For example, if you define the external Web services FQDN of a Front End Server as <STRONG>pool01.contoso.com</STRONG>, you cannot use <STRONG>pool01.contoso.com</STRONG> for another Front End pool or Front End Server.</span></span> <span data-ttu-id="b26e6-157">Si vous déployez également des directeurs, le nom de domaine complet des services Web externes défini pour n’importe quel directeur ou pool de réalisateur doit être unique à partir d’un autre directeur ou pool de directeurs, ainsi que sur n’importe quel pool frontal ou serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="b26e6-157">If you are also deploying Directors, the external Web services FQDN defined for any Director or Director pool must be unique from any other Director or Director pool as well as any Front End pool or Front End Server.</span></span> <span data-ttu-id="b26e6-158">Si vous décidez de remplacer les services Web internes par un nom de domaine complet autonome, chaque nom de domaine complet doit être unique à partir de n’importe quel autre pool frontal, directeur ou pool de réalisateur.</span><span class="sxs-lookup"><span data-stu-id="b26e6-158">If decide to override the Internal web services with a self-defined FQDN, each FQDN must be unique from any other Front End pool, Director or a Director pool.</span></span>

    
    </div>

9.  <span data-ttu-id="b26e6-159">Publiez la topologie.</span><span class="sxs-lookup"><span data-stu-id="b26e6-159">Publish the topology.</span></span>

<span data-ttu-id="b26e6-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b26e6-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

