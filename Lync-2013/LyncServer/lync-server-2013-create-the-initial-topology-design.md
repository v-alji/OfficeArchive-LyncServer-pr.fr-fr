---
title: 'Lync Server 2013 : création de la conception de topologie initiale'
description: 'Lync Server 2013 : création de la conception de topologie initiale.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create the initial design
ms:assetid: f3131153-de14-41be-b1e6-7d4bb0191af1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615047(v=OCS.15)
ms:contentKeyID: 51541530
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c91bfe68a1de4a1f9862948edd708b8efa6a5c6d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431581"
---
# <a name="create-the-initial-topology-design-for-lync-server-2013"></a><span data-ttu-id="1653f-103">Créer la conception de topologie initiale pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1653f-103">Create the initial topology design for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1653f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1653f-104">

<span> </span></span></span>

<span data-ttu-id="1653f-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="1653f-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="1653f-106">Après l’installation de l’outil de planification Lync Server 2013, vous pouvez démarrer l’outil de planification et commencer à concevoir l’infrastructure Lync Server 2013 proposée.</span><span class="sxs-lookup"><span data-stu-id="1653f-106">After you have finished installing the Lync Server 2013, Planning Tool, you are ready to start the Planning Tool and begin designing the proposed Lync Server 2013 infrastructure.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1653f-107">L’outil de planification est un outil géré par l’Assistant contenant des guides détaillés pour informer votre processus de décision dans la conception de vos sites et de votre topologie.</span><span class="sxs-lookup"><span data-stu-id="1653f-107">The Planning Tool is a wizard-driven tool with detailed guides to inform your decision-making process in designing your sites and topology.</span></span> <span data-ttu-id="1653f-108">Ce sujet n’est pas une présentation exhaustive, mais simplement pour vous aider à commencer à utiliser l’outil de planification dans vos sessions de conception.</span><span class="sxs-lookup"><span data-stu-id="1653f-108">This topic is intended not as an exhaustive guide, but simply to help get you started using the Planning Tool in your design sessions.</span></span>



</div>

<div>

## <a name="to-get-started-using-the-planning-tool-and-create-the-initial-design"></a><span data-ttu-id="1653f-109">Pour commencer à utiliser l’outil de planification et créer la conception initiale</span><span class="sxs-lookup"><span data-stu-id="1653f-109">To get started using the Planning Tool and create the initial design</span></span>

1.  <span data-ttu-id="1653f-110">Démarrez l’outil de planification Lync Server 2013 : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur outil de **planification**.</span><span class="sxs-lookup"><span data-stu-id="1653f-110">Start the Lync Server 2013, Planning Tool: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Planning Tool**.</span></span>

2.  <span data-ttu-id="1653f-111">Après le démarrage de l’outil de planification, la page **Bienvenue dans l’outil de planification de Microsoft Lync Server 2013** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1653f-111">After the Planning Tool has started, the **Welcome to the Planning Tool for Microsoft Lync Server 2013** page appears.</span></span> <span data-ttu-id="1653f-112">Choisissez l’une des options suivantes pour commencer votre conception :</span><span class="sxs-lookup"><span data-stu-id="1653f-112">Choose one of the following options to begin your design:</span></span>
    
      - <span data-ttu-id="1653f-113">**Option 1 : commencer**   Le fait de cliquer sur mise en **route** fournit une série spécifique de questions relatives aux entretiens et à la définition du critère.</span><span class="sxs-lookup"><span data-stu-id="1653f-113">**Option 1: Get Started**   Clicking **Get Started** provides a specific series of interview questions with relevant selections to define the criteria.</span></span> <span data-ttu-id="1653f-114">Lorsque vous en avez terminé avec la section **Mise en route** initiale, poursuivez avec **Concevoir des sites** pour définir l’architecture de votre site.</span><span class="sxs-lookup"><span data-stu-id="1653f-114">After you have finished the initial **Get Started** interview section, you proceed into **Design Sites** to define your site architecture.</span></span> <span data-ttu-id="1653f-115">Pour achever cette option, passez à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="1653f-115">To complete this option, proceed to step 3.</span></span>
    
      - <span data-ttu-id="1653f-116">**Option 2 : créer des sites**   Lorsque vous cliquez sur les **sites de création** sur la page d’accueil, les questions posées dans la section mise en **route sont** ignorées.</span><span class="sxs-lookup"><span data-stu-id="1653f-116">**Option 2: Design Sites**   Clicking **Design Sites** at the Welcome page bypasses the interview questions presented in the **Get Started** section.</span></span> <span data-ttu-id="1653f-117">Les informations collectées par les réponses fournies aux questions d’entretien dans la rubrique **Mise en route** sont définies comme valeurs par défaut avec cette option.</span><span class="sxs-lookup"><span data-stu-id="1653f-117">The information that would have been gathered by responding to the interview questions in **Get Started** section is set to default values with this option.</span></span> <span data-ttu-id="1653f-118">En cliquant sur **Concevoir des sites**, le concepteur expérimenté peut contourner l’entretien initial et modifier les valeurs par défaut selon ses besoins sur la page de démarrage **Sites centraux**.</span><span class="sxs-lookup"><span data-stu-id="1653f-118">By clicking **Design Sites**, the experienced designer can bypass the initial interview and change the default values, as needed, on the **Central Sites** start page.</span></span> <span data-ttu-id="1653f-119">Pour achever cette option, ignorez les étapes 3 à 5 et passez directement à l’étape 6.</span><span class="sxs-lookup"><span data-stu-id="1653f-119">To complete this option, skip over steps 3-5 and start at step 6.</span></span>
    
      - <span data-ttu-id="1653f-120">**Option 3 : afficher la topologie enregistrée**   Si vous avez déjà rempli et enregistré une topologie par le biais de l’utilisation précédente de l’outil de planification, vous pouvez ignorer la plupart de ces étapes et commencer par ouvrir et afficher la topologie.</span><span class="sxs-lookup"><span data-stu-id="1653f-120">**Option 3: Display Your Saved Topology**   If you have already completed and saved a topology through previous use of the Planning Tool, you can skip over most of these steps and start by opening and displaying the topology.</span></span> <span data-ttu-id="1653f-121">Vous pouvez également apporter des modifications et des mises à jour à la topologie, la ré-enregistrer, puis l’exporter dans Microsoft Excel ou Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="1653f-121">You can also make changes and updates to the topology, resave it, and then export it to Microsoft Excel or Microsoft Visio.</span></span> <span data-ttu-id="1653f-122">Pour achever cette option, ignorez les étapes 3 à 12 et passez directement à l’étape 13.</span><span class="sxs-lookup"><span data-stu-id="1653f-122">To complete this option, skip over steps 3-12 and start at step 13.</span></span>

3.  <span data-ttu-id="1653f-123">Cliquez sur mise en **route** pour commencer à concevoir votre topologie Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1653f-123">Click **Get Started** to begin designing your Lync Server 2013 topology.</span></span>

4.  <span data-ttu-id="1653f-p106">Répondez à chaque rubrique en sélectionnant les critères appropriés pour votre conception, puis cliquez sur **Suivant** pour passer à la page suivante de l’Assistant. Cliquez sur **Précédent** pour modifier les pages précédentes.</span><span class="sxs-lookup"><span data-stu-id="1653f-p106">Answer each section by selecting the appropriate criteria for your design, and then click **Next** to proceed to the next Wizard page. Click **Back** to make changes on previous pages.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="1653f-126">Chaque page contient une description des critères de sélection et des recommandations basées sur les pratiques préférées et la planification de la capacité.</span><span class="sxs-lookup"><span data-stu-id="1653f-126">Each page has a description of the selection criteria, and recommendations based on preferred practices and capacity planning.</span></span> <span data-ttu-id="1653f-127">Si vous avez besoin d’informations supplémentaires, cliquez sur <STRONG>en savoir plus</STRONG> pour lire des informations détaillées dans la documentation de planification de Lync Server 2013 sur le site Web Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="1653f-127">If you require additional details, click <STRONG>Learn more</STRONG> to read detailed information from the Lync Server 2013 Planning documentation on the Microsoft TechNet website.</span></span> <span data-ttu-id="1653f-128">Vous devez disposer d’une connexion à Internet pour accéder au site web Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="1653f-128">You must have Internet connectivity to access the Microsoft TechNet website.</span></span>

    
    </div>

5.  <span data-ttu-id="1653f-129">Sélectionnez les options appropriées pour votre conception.</span><span class="sxs-lookup"><span data-stu-id="1653f-129">Select the appropriate options for your design.</span></span> <span data-ttu-id="1653f-130">Une fois les critères initiaux définis, une page viendra confirmer que votre vue d’ensemble des fonctionnalités est complète.</span><span class="sxs-lookup"><span data-stu-id="1653f-130">After the initial criteria are defined, a page will confirm that your Features Overview is complete.</span></span>

6.  <span data-ttu-id="1653f-131">Cliquez sur **sites de création** pour définir votre site central.</span><span class="sxs-lookup"><span data-stu-id="1653f-131">Click **Design Sites** to define your central site.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1653f-132">Chaque topologie Lync Server 2013 dispose d’au moins un site central.</span><span class="sxs-lookup"><span data-stu-id="1653f-132">Each Lync Server 2013 topology will have at least one central site.</span></span> <span data-ttu-id="1653f-133">Votre conception est dotée d’un seul site central, d’un site central composé de plusieurs sites de succursales, d’un certain nombre de sites centraux ou d’un certain nombre de sites centraux avec des sites de succursales associés à chaque site central.</span><span class="sxs-lookup"><span data-stu-id="1653f-133">Your design may have a single central site, a central site with a number of branch sites, a number of central sites, or a number of central sites with branch sites associated with each central site.</span></span>

    
    </div>

7.  <span data-ttu-id="1653f-134">Dans **nom du site**, tapez le nom qui permettra d’identifier ce site central.</span><span class="sxs-lookup"><span data-stu-id="1653f-134">In **Site Name**, type the name that will identify this central site.</span></span>

8.  <span data-ttu-id="1653f-135">Dans la **page utilisateurs hébergés** sur le site, entrez le nombre d’utilisateurs simultanés locaux qui seront hébergés sur ce site central.</span><span class="sxs-lookup"><span data-stu-id="1653f-135">In **Site Homed Users**, type the expected number of on-premises concurrent users who will be homed in this central site.</span></span>

9.  <span data-ttu-id="1653f-136">Dans la **page utilisateurs** dans le Cloud, entrez le nombre prévu d’utilisateurs simultanés en ligne qui seront hébergés sur ce site central.</span><span class="sxs-lookup"><span data-stu-id="1653f-136">In **Cloud Homed Users**, type the expected number of online concurrent users who will be homed in this central site.</span></span>

10. <span data-ttu-id="1653f-137">Modifiez les sélections pour Collaboration en ligne, Utilisateurs, Voix, Options de déploiement supplémentaires ou Applications serveur, selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="1653f-137">Modify the selections for Online Collaboration, Users, Voice, Additional Deployment Options, or Server Applications, as needed.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="1653f-138">Ce n’est qu’à ce moment de la conception que vous pouvez activer ou désactiver les options de votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="1653f-138">At this point in the design, you can only select or clear options for your deployment.</span></span> <span data-ttu-id="1653f-139">Toutefois, vous pouvez configurer d’autres options dans une phase ultérieure de l’outil de planification.</span><span class="sxs-lookup"><span data-stu-id="1653f-139">However, you can configure more options in a later phase of the Planning Tool.</span></span> <span data-ttu-id="1653f-140">Certaines options sont également indisponibles et ne peuvent pas être désactivées.</span><span class="sxs-lookup"><span data-stu-id="1653f-140">There are also options that are unavailable and cannot be cleared.</span></span> <span data-ttu-id="1653f-141">En outre, vous pouvez être amené à désactiver une option pour en désactiver une autre.</span><span class="sxs-lookup"><span data-stu-id="1653f-141">In addition, you may have to clear one option in order to clear another.</span></span> <span data-ttu-id="1653f-142">Par exemple, si vous désactivez l’option <STRONG>Voix Entreprise</STRONG> sous Voix, les options <STRONG>Response Group</STRONG>, <STRONG>Annonce</STRONG> et <STRONG>Parcage d’appel</STRONG> sous Applications serveur (toutes étant des fonctionnalités de Voix Entreprise) sont également désactivées.</span><span class="sxs-lookup"><span data-stu-id="1653f-142">For example, if you clear the <STRONG>Enterprise Voice</STRONG> option under Voice, then the <STRONG>Response Group</STRONG>, <STRONG>Announcement</STRONG>, and <STRONG>Call Park</STRONG> options under Server Applications (all of which are features of Enterprise Voice) are also cleared.</span></span>

    
    </div>

11. <span data-ttu-id="1653f-143">Après avoir défini le nom du site et le nombre d’utilisateurs, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="1653f-143">After defining a site name and number of users, click **Next**.</span></span>

12. <span data-ttu-id="1653f-144">Les pages suivantes vous demandent des informations relatives aux domaines SIP, aux paramètres de conférence, aux paramètres vocaux et à l’infrastructure, à la messagerie unifiée, aux options de colocalisation et aux sites de succursales d’Exchange.</span><span class="sxs-lookup"><span data-stu-id="1653f-144">The following pages ask for information about SIP domains, conference settings, voice settings and infrastructure, Exchange UM, external user access, Persistent Chat settings, client settings, collocation options, and branch sites.</span></span> <span data-ttu-id="1653f-145">Répondez à toutes ces questions selon le cas.</span><span class="sxs-lookup"><span data-stu-id="1653f-145">Answer these questions as appropriate.</span></span>

13. <span data-ttu-id="1653f-146">La question finale vous demande si vous souhaitez créer un autre site central.</span><span class="sxs-lookup"><span data-stu-id="1653f-146">The final question asks if you want to create another central site.</span></span> <span data-ttu-id="1653f-147">Si vous sélectionnez **Oui**, l’outil de planification revient à la page sites centraux.</span><span class="sxs-lookup"><span data-stu-id="1653f-147">If you select **Yes**, then the Planning Tool returns to the Central Sites page.</span></span> <span data-ttu-id="1653f-148">Si vous sélectionnez **Non**, cliquez sur **Suivant**, puis sur **Dessiner** pour afficher la vue Topologie globale de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="1653f-148">If you select **No**, click **Next**, and then click **Draw** to display the high-level Global Topology view.</span></span>

14. <span data-ttu-id="1653f-149">Pour afficher la topologie existante, cliquez sur **Afficher**.</span><span class="sxs-lookup"><span data-stu-id="1653f-149">To view an existing topology, click **Display**.</span></span>

15. <span data-ttu-id="1653f-150">Cliquez sur le fichier .xml qui représente la topologie précédemment enregistrée, puis cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="1653f-150">Click the .xml file that represents the previously saved topology, and then click **Open**.</span></span>

16. <span data-ttu-id="1653f-151">L’outil de planification affiche la page de topologie globale.</span><span class="sxs-lookup"><span data-stu-id="1653f-151">The Planning Tool displays the Global Topology page.</span></span> <span data-ttu-id="1653f-152">Vous pouvez désormais commencer à modifier, à mettre à jour ou à modifier la topologie en utilisant les outils disponibles dans l’outil de planification.</span><span class="sxs-lookup"><span data-stu-id="1653f-152">You can now begin editing, updating, or changing the topology by using the tools available in the Planning Tool.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1653f-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1653f-153">See Also</span></span>


[<span data-ttu-id="1653f-154">Modification de la conception dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1653f-154">Editing the design in Lync Server 2013</span></span>](lync-server-2013-editing-the-design.md)  
  

<span data-ttu-id="1653f-155"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1653f-155"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

