---
title: 'Lync Server 2013 : outil Diagnostics pour les préappel Lync'
description: 'Lync Server 2013 : outil de diagnostics de préappel Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync PreCall Diagnostics Tool
ms:assetid: 0ff291ec-cfb4-43eb-b5d6-a7a325681e3f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn451255(v=OCS.15)
ms:contentKeyID: 56708404
ms.date: 11/04/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 17c2c51551fe0991eb354a628b1d4660baa1532b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426338"
---
# <a name="lync-precall-diagnostics-tool-in-lync-server-2013"></a><span data-ttu-id="1dfb5-103">Outil de diagnostics d’préappel Lync dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1dfb5-103">Lync PreCall Diagnostics Tool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1dfb5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1dfb5-104">

<span> </span></span></span>

<span data-ttu-id="1dfb5-105">_**Dernière modification de la rubrique :** 2016-11-04_</span><span class="sxs-lookup"><span data-stu-id="1dfb5-105">_**Topic Last Modified:** 2016-11-04_</span></span>

<span data-ttu-id="1dfb5-106">L’outil de diagnostics d’avant-appel Lync (PCD) est une application basée sur le client qui vous permet de voir comment l’état actuel de votre réseau peut avoir un impact sur la qualité audio lors d’un appel voix entreprise à venir.</span><span class="sxs-lookup"><span data-stu-id="1dfb5-106">The Lync PreCall Diagnostics Tool (PCD) is a client-based application that allows you to see how the current state of your network might impact the audio quality in an upcoming Enterprise Voice call.</span></span>

<span data-ttu-id="1dfb5-107">PCD est particulièrement utile dans les situations dans lesquelles le dernier tronçon d’un réseau est susceptible d’être faible (par exemple, avec des ordinateurs portables sur un réseau WiFi public ou des particuliers).</span><span class="sxs-lookup"><span data-stu-id="1dfb5-107">PCD is most useful in situations where the last hop of a network is likely to be the weakest (for example, with laptops on a public WiFi network or home users).</span></span> <span data-ttu-id="1dfb5-108">PCD crée un petit flux de paquets qui traverse ce dernier tronçon du réseau.</span><span class="sxs-lookup"><span data-stu-id="1dfb5-108">PCD creates a small packet stream that traverses this final leg of the network.</span></span> <span data-ttu-id="1dfb5-109">L’outil analyse alors le flux de paquets pour évaluer la façon dont la gigue et la perte peuvent avoir un impact sur la qualité des appels, puis fournit un rapport.</span><span class="sxs-lookup"><span data-stu-id="1dfb5-109">The tool then analyzes the packet stream to estimate how the jitter and loss along this leg might impact call quality, and then provides a report.</span></span> <span data-ttu-id="1dfb5-110">Vous pouvez exécuter PCD en continu sur le client, même lorsque les appels sont en train d’être placés.</span><span class="sxs-lookup"><span data-stu-id="1dfb5-110">You can run PCD continuously on the client, even while calls are being placed.</span></span> <span data-ttu-id="1dfb5-111">Le flux de paquets n’a pas d’effet notable sur la bande passante.</span><span class="sxs-lookup"><span data-stu-id="1dfb5-111">The packet stream does not have a significant effect on bandwidth.</span></span>

<span data-ttu-id="1dfb5-112">**La dernière version du PCD, version 1,1, inclut les améliorations suivantes :**</span><span class="sxs-lookup"><span data-stu-id="1dfb5-112">**The latest release of the PCD, version 1.1, includes the following enhancements:**</span></span>

  - <span data-ttu-id="1dfb5-113">Prise en charge de mots de passe plus longs, qui peuvent désormais comporter jusqu’à 127 caractères</span><span class="sxs-lookup"><span data-stu-id="1dfb5-113">Support for longer passwords, which can now be up to 127 characters</span></span>

  - <span data-ttu-id="1dfb5-114">Diagnostics supplémentaires pour les problèmes de connexion d’authentification</span><span class="sxs-lookup"><span data-stu-id="1dfb5-114">Additional diagnostics for authentication sign-in issues</span></span>

  - <span data-ttu-id="1dfb5-115">Prise en charge améliorée des déploiements hybrides de Lync</span><span class="sxs-lookup"><span data-stu-id="1dfb5-115">Better support for Lync hybrid deployments</span></span>

  - <span data-ttu-id="1dfb5-116">Mises à jour du sélecteur d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="1dfb5-116">Updates to credential picker</span></span>

  - <span data-ttu-id="1dfb5-117">Améliorations de la stabilité</span><span class="sxs-lookup"><span data-stu-id="1dfb5-117">Stability improvements</span></span>

<span data-ttu-id="1dfb5-118">Nous vous remercions de votre avis.</span><span class="sxs-lookup"><span data-stu-id="1dfb5-118">We appreciate any feedback.</span></span> <span data-ttu-id="1dfb5-119">Vous pouvez envoyer toutes vos questions ou problèmes d’assistance à l’alias de [Commentaires PCD](mailto:pcdfb@microsoft.com) à l’adresse <pcdfb@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="1dfb5-119">Please send all support questions or issues to the [PCD Feedback](mailto:pcdfb@microsoft.com) alias at <pcdfb@microsoft.com>.</span></span>

<span data-ttu-id="1dfb5-120">Cette rubrique inclut les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="1dfb5-120">This topic includes the following sections:</span></span>

  - <span data-ttu-id="1dfb5-121">Versions de Lync PCD</span><span class="sxs-lookup"><span data-stu-id="1dfb5-121">Lync PCD Versions</span></span>

  - <span data-ttu-id="1dfb5-122">Configuration système requise pour Lync PCD</span><span class="sxs-lookup"><span data-stu-id="1dfb5-122">Lync PCD System Requirements</span></span>

  - <span data-ttu-id="1dfb5-123">Fonctionnalités de Lync PCD</span><span class="sxs-lookup"><span data-stu-id="1dfb5-123">Lync PCD Features</span></span>

  - <span data-ttu-id="1dfb5-124">Exécution de Lync PCD</span><span class="sxs-lookup"><span data-stu-id="1dfb5-124">Running Lync PCD</span></span>

  - <span data-ttu-id="1dfb5-125">Désinstallation de Lync PCD</span><span class="sxs-lookup"><span data-stu-id="1dfb5-125">Uninstalling Lync PCD</span></span>

<span id="Version"></span>

<div>

## <a name="lync-pcd-versions"></a><span data-ttu-id="1dfb5-126">Versions de Lync PCD</span><span class="sxs-lookup"><span data-stu-id="1dfb5-126">Lync PCD Versions</span></span>

<span data-ttu-id="1dfb5-127">Cette rubrique décrit les versions suivantes de l’outil disponibles en téléchargement gratuit :</span><span class="sxs-lookup"><span data-stu-id="1dfb5-127">This topic describes the following versions of the tool, available for free download:</span></span>

  - <span data-ttu-id="1dfb5-128">Application de bureau Windows ( [https://go.microsoft.com/fwlink/?LinkId=327914](https://go.microsoft.com/fwlink/p/?linkid=327914) )</span><span class="sxs-lookup"><span data-stu-id="1dfb5-128">Windows Desktop App ([https://go.microsoft.com/fwlink/?LinkId=327914](https://go.microsoft.com/fwlink/p/?linkid=327914))</span></span>

</div>

<span id="Requirements"></span>

<div>

## <a name="lync-pcd-system-requirements"></a><span data-ttu-id="1dfb5-129">Configuration système requise pour Lync PCD</span><span class="sxs-lookup"><span data-stu-id="1dfb5-129">Lync PCD System Requirements</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1dfb5-130">PCD nécessite l’installation et la configuration de l’API Web de communications unifiées (UCWA) pour la prise en charge des clients mobiles dans le déploiement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1dfb5-130">PCD requires that Unified Communications Web API (UCWA) be installed and configured to support mobile clients in the Lync Server deployment.</span></span> <span data-ttu-id="1dfb5-131">UCWA est installé avec Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1dfb5-131">UCWA is installed with Lync Server.</span></span>



</div>

<div>

## <a name="windows-desktop-app-requirements"></a><span data-ttu-id="1dfb5-132">Configuration requise pour l’application de bureau Windows</span><span class="sxs-lookup"><span data-stu-id="1dfb5-132">Windows Desktop App Requirements</span></span>

  - <span data-ttu-id="1dfb5-133">Toute édition du système d’exploitation Windows 7 ou Windows 8</span><span class="sxs-lookup"><span data-stu-id="1dfb5-133">Any edition of the Windows 7 or Windows 8 operating system</span></span>

  - <span data-ttu-id="1dfb5-134">Microsoft .NET Framework 4,5 disponible sur le [https://go.microsoft.com/fwlink/?LinkId=327790](https://go.microsoft.com/fwlink/p/?linkid=327790)</span><span class="sxs-lookup"><span data-stu-id="1dfb5-134">Microsoft .NET Framework 4.5 available at [https://go.microsoft.com/fwlink/?LinkId=327790](https://go.microsoft.com/fwlink/p/?linkid=327790)</span></span>

</div>

</div>

<span id="features"></span>

<div>

## <a name="lync-pcd-features"></a><span data-ttu-id="1dfb5-135">Fonctionnalités de Lync PCD</span><span class="sxs-lookup"><span data-stu-id="1dfb5-135">Lync PCD Features</span></span>

<span data-ttu-id="1dfb5-136">Lync PCD inclut les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="1dfb5-136">Lync PCD includes the following features:</span></span>

  - <span data-ttu-id="1dfb5-137">Exécution par défaut à la demande (burst de 2 minutes)</span><span class="sxs-lookup"><span data-stu-id="1dfb5-137">Run in default On Demand (2 minute bursts)</span></span>

  - <span data-ttu-id="1dfb5-138">Exécution dans le mode toujours activé (jusqu’à 24 heures dans l’affichage aligné)</span><span class="sxs-lookup"><span data-stu-id="1dfb5-138">Run in Always On (up to 24 hours in snapped view) mode</span></span>

  - <span data-ttu-id="1dfb5-139">Affichage historique de vos séries de tests</span><span class="sxs-lookup"><span data-stu-id="1dfb5-139">Historical view of your test runs</span></span>

  - <span data-ttu-id="1dfb5-140">Diagnostiquer les échecs de connexion (Lync PCD pour Windows 8 uniquement)</span><span class="sxs-lookup"><span data-stu-id="1dfb5-140">Diagnose sign-in failures (Lync PCD for Windows 8 only)</span></span>

<span data-ttu-id="1dfb5-141">![Capture d’écran de la capture d’écran de l’application Lync](images/Dn451255.7e0eb891-1481-47ae-8d63-164468f69c96(OCS.15).png "Capture d’écran de la capture d’écran de l’application Lync")</span><span class="sxs-lookup"><span data-stu-id="1dfb5-141">![Lync PCD features Sign in progress screen shot](images/Dn451255.7e0eb891-1481-47ae-8d63-164468f69c96(OCS.15).png "Lync PCD features Sign in progress screen shot")</span></span>

  - <span data-ttu-id="1dfb5-142">Affichage graphique des métriques du réseau (MOS du réseau, perte de paquets et gigue d’interentrée) en plein écran et en affichage aligné.</span><span class="sxs-lookup"><span data-stu-id="1dfb5-142">Graphical view of network metrics – Network MOS, Packet Loss and Interarrival Jitter in full screen and snapped view.</span></span>

<span data-ttu-id="1dfb5-143">**Mode plein écran**</span><span class="sxs-lookup"><span data-stu-id="1dfb5-143">**Full screen view**</span></span>

<span data-ttu-id="1dfb5-144">![Graphes de résultats de test de l’outil de diagnostic avant appel](images/Dn451255.5d01fd94-9e59-4823-96c7-7a1c83dd7d31(OCS.15).png "Graphes de résultats de test de l’outil de diagnostic avant appel")</span><span class="sxs-lookup"><span data-stu-id="1dfb5-144">![PreCall Diagnostic Tool test result graphs](images/Dn451255.5d01fd94-9e59-4823-96c7-7a1c83dd7d31(OCS.15).png "PreCall Diagnostic Tool test result graphs")</span></span>

<span data-ttu-id="1dfb5-145">**Affichage aligné**</span><span class="sxs-lookup"><span data-stu-id="1dfb5-145">**Snapped view**</span></span>

<span data-ttu-id="1dfb5-146">![Résultats du test d’utilisation de l’outil de diagnostic avant appel](images/Dn451255.30501ba7-22d1-4db1-9297-56cf7dc6721c(OCS.15).png "Résultats du test d’utilisation de l’outil de diagnostic avant appel")</span><span class="sxs-lookup"><span data-stu-id="1dfb5-146">![PreCall Diagnostic Tool Utilization test results](images/Dn451255.30501ba7-22d1-4db1-9297-56cf7dc6721c(OCS.15).png "PreCall Diagnostic Tool Utilization test results")</span></span>

</div>

<span id="running"></span>

<div>

## <a name="running-lync-pcd"></a><span data-ttu-id="1dfb5-147">Exécution de Lync PCD</span><span class="sxs-lookup"><span data-stu-id="1dfb5-147">Running Lync PCD</span></span>

<div>

## <a name="running-windows-desktop-app"></a><span data-ttu-id="1dfb5-148">Exécution d’une application de bureau Windows</span><span class="sxs-lookup"><span data-stu-id="1dfb5-148">Running Windows Desktop App</span></span>

1.  <span data-ttu-id="1dfb5-149">Pour démarrer le PCD sur un système Windows 7, sélectionnez **Diagnostics préappel** dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="1dfb5-149">To start the PCD on a Windows 7 system, select **PreCall Diagnostics** from the **Start** menu.</span></span>
    
    <span data-ttu-id="1dfb5-150">Pour démarrer le PCD sur un système Windows 8, sélectionnez l’icône sur votre écran d’accueil, ou recherchez « Diagnostics de préappel ».</span><span class="sxs-lookup"><span data-stu-id="1dfb5-150">To start the PCD on a Windows 8 system, select the icon on your Start screen, or search for “PreCall Diagnostics.”</span></span>
    
    <span data-ttu-id="1dfb5-151">![Icône de l’outil PreCall Diagnostic](images/Dn451255.c9800fde-54f6-4efe-bb35-1a38064ec380(OCS.15).png "Icône de l’outil PreCall Diagnostic")</span><span class="sxs-lookup"><span data-stu-id="1dfb5-151">![PreCall Diagnostic tool icon](images/Dn451255.c9800fde-54f6-4efe-bb35-1a38064ec380(OCS.15).png "PreCall Diagnostic tool icon")</span></span>

2.  <span data-ttu-id="1dfb5-152">Lorsque l’outil démarre, sélectionnez la méthode de votre choix pour fournir des informations d’identification, puis sélectionnez le mode de fonctionnement réseau dans la boîte de dialogue Options de l' **outil Diagnostics** de l’appel, puis cliquez sur **OK**:</span><span class="sxs-lookup"><span data-stu-id="1dfb5-152">When the tool starts, select your preferred method of providing credentials and select the network operating mode in the **PreCall Diagnostics Tool Options** dialog box, then select **OK**:</span></span>

3.  <span data-ttu-id="1dfb5-153">Cliquez sur le bouton **Démarrer le test** pour démarrer l’exécution des Diagnostics.</span><span class="sxs-lookup"><span data-stu-id="1dfb5-153">Select the **Start Test** button to start running diagnostics.</span></span>
    
    <span data-ttu-id="1dfb5-154">Si vous avez sélectionné l’option **utiliser les informations d’identification réseau** , le test commence immédiatement.</span><span class="sxs-lookup"><span data-stu-id="1dfb5-154">If you selected the **Use network credentials** option, the test begins immediately.</span></span>
    
    <span data-ttu-id="1dfb5-155">Si vous avez sélectionné l’option **me permettre d’entrer mes informations d’identification** , la boîte de dialogue de **sécurité Windows** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="1dfb5-155">If you selected the **Let me enter my credentials** option, the **Windows Security** dialog box opens.</span></span> <span data-ttu-id="1dfb5-156">Après avoir entré vos informations d’identification, le test démarre.</span><span class="sxs-lookup"><span data-stu-id="1dfb5-156">After you enter your credentials, the test starts.</span></span>

</div>

</div>

<span id="uninstall"></span>

<div>

## <a name="uninstalling-lync-pcd"></a><span data-ttu-id="1dfb5-157">Désinstallation de Lync PCD</span><span class="sxs-lookup"><span data-stu-id="1dfb5-157">Uninstalling Lync PCD</span></span>

<span data-ttu-id="1dfb5-158">Pour supprimer Lync PCD, suivez la procédure pour votre système d’exploitation :</span><span class="sxs-lookup"><span data-stu-id="1dfb5-158">To remove Lync PCD, follow the procedure for your operating system:</span></span>

  - <span data-ttu-id="1dfb5-159">Sur un système Windows 7, ouvrez le **panneau de configuration**, sélectionnez **programmes et fonctionnalités**, puis double-cliquez sur **Diagnostics de l’appel Lync 2013**.</span><span class="sxs-lookup"><span data-stu-id="1dfb5-159">On a Windows 7 system, open the **Control Panel**, select **Programs and Features**, and double-click **Lync 2013 PreCall Diagnostics**.</span></span>

  - <span data-ttu-id="1dfb5-160">Sur un système Windows 8, cliquez avec le bouton droit sur la vignette PCD, puis cliquez sur **désinstaller** dans la barre de l’application en bas de l’écran d’accueil.</span><span class="sxs-lookup"><span data-stu-id="1dfb5-160">On a Windows 8 system, right-click on the PCD tile and click **Uninstall** from the app bar at the bottom of the start screen.</span></span>

<span data-ttu-id="1dfb5-161"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1dfb5-161"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

