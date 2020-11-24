---
title: Connexion d’une Survivable Branch Appliance
description: Connectez une unité de branchement survivant.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Connect a Survivable Branch Appliance
ms:assetid: fe3167e2-d1b1-4cd4-bf30-262e0e7d14e8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721948(v=OCS.15)
ms:contentKeyID: 49733886
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5bbf9e1a4189d3c80d6dec449adf68b82cd3691
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394092"
---
# <a name="connect-a-survivable-branch-appliance"></a><span data-ttu-id="43692-103">Connexion d’une Survivable Branch Appliance</span><span class="sxs-lookup"><span data-stu-id="43692-103">Connect a Survivable Branch Appliance</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="43692-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="43692-104">

<span> </span></span></span>

<span data-ttu-id="43692-105">_**Dernière modification de la rubrique :** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="43692-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="43692-106">Chaque appareil de branchement survivant (SBA) est associé à une réserve frontale qui sert de bureau d’enregistrement de sauvegarde pour le SBA.</span><span class="sxs-lookup"><span data-stu-id="43692-106">Every Survivable Branch Appliance (SBA) is associated with a Front End pool which serves as a backup registrar for the SBA.</span></span> <span data-ttu-id="43692-107">Lorsque le pool frontal a été déplacé vers Lync Server 2013, le SBA doit être désassocié du pool frontal 2010 de Lync Server lors de la mise à niveau du pool, une fois que le pool a été migré vers Lync Server 2013, il est possible de le réassocier à l’adresse du pool frontal mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="43692-107">When the Front End pool is migrated to Lync Server 2013, the SBA must be disassociated from the Lync Server 2010 Front End pool while the pool is upgraded, Once the pool has been migrated to Lync Server 2013, the SBA can be re-associated with the upgraded Front End pool.</span></span> <span data-ttu-id="43692-108">Cela implique la suppression de l’SBA de la topologie Lync Server 2010 héritée dans le générateur de topologie, puis l’ajout de l’SBA à la topologie de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="43692-108">This involves deleting the SBA from the legacy Lync Server 2010 topology in Topology Builder and then adding the SBA to the Lync Server 2013 topology.</span></span> <span data-ttu-id="43692-109">Les utilisateurs hébergés sur l’ancien serveur Lync Server 2010 SBA doivent d’abord être déplacés vers un autre pool frontal avant de supprimer l’SBA de la topologie.</span><span class="sxs-lookup"><span data-stu-id="43692-109">Users homed on the legacy Lync Server 2010 SBA must first be moved to another Front End pool before removing the SBA from the topology.</span></span> <span data-ttu-id="43692-110">Dès lors que l’SBA est ajouté à la topologie Lync Server 2013, les utilisateurs peuvent ensuite être repassés à l’adresse SBA.</span><span class="sxs-lookup"><span data-stu-id="43692-110">Once the SBA is added to the Lync Server 2013 topology, those users can then be moved back to the SBA.</span></span> <span data-ttu-id="43692-111">Ces étapes sont décrites ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="43692-111">These steps are summarized below:</span></span>

1.  <span data-ttu-id="43692-112">Déplacer les utilisateurs de succursales hébergés sur l’ancien réseau Lync Server 2010 vers un autre pool frontal.</span><span class="sxs-lookup"><span data-stu-id="43692-112">Move branch users homed on the legacy SBA Lync Server 2010 to another Front End pool.</span></span>

2.  <span data-ttu-id="43692-113">Supprimez SBA de la topologie de Lync Server 2010 héritée pour déconnecter le pool frontal existant en tant qu’Bureau d’enregistrement de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="43692-113">Remove SBA from the legacy Lync Server 2010 topology to disconnect the existing Front End pool as a backup registrar.</span></span>

3.  <span data-ttu-id="43692-114">Ajoutez SBA à la topologie Lync Server 2013 et configurez ce nouveau pool frontal comme bureau d’enregistrement de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="43692-114">Add SBA to the Lync Server 2013 topology and configure this new Front End pool as the backup registrar.</span></span>

4.  <span data-ttu-id="43692-115">Déplacez les utilisateurs de la succursale vers le nouveau Lync Server 2013 SBA.</span><span class="sxs-lookup"><span data-stu-id="43692-115">Move the branch users to the new Lync Server 2013 SBA.</span></span>

<span data-ttu-id="43692-116">**Ajouter le site de succursale Lync Server 2010 SBA à votre topologie**</span><span class="sxs-lookup"><span data-stu-id="43692-116">**Add Lync Server 2010 SBA Branch Site to Your Topology**</span></span>

1.  <span data-ttu-id="43692-117">Ouvrez le **Générateur de topologie**.</span><span class="sxs-lookup"><span data-stu-id="43692-117">Open **Topology Builder**.</span></span>

2.  <span data-ttu-id="43692-118">Dans le volet gauche, cliquez avec le bouton droit sur **sites de succursales**, puis cliquez sur **nouveau site de succursale**.</span><span class="sxs-lookup"><span data-stu-id="43692-118">In the left pane right-click **Branch sites**, and then click **New Branch Site**.</span></span>

3.  <span data-ttu-id="43692-119">Dans la boîte de dialogue **définir un nouveau site de succursale** , cliquez sur **nom**, puis tapez le nom du site de la succursale.</span><span class="sxs-lookup"><span data-stu-id="43692-119">In the **Define New Branch Site** dialog box, click **Name**, and then type the name of the branch site.</span></span>

4.  <span data-ttu-id="43692-120">Facultatif Cliquez sur **Description**, puis tapez une description significative pour le site de la succursale.</span><span class="sxs-lookup"><span data-stu-id="43692-120">(Optional) Click **Description**, and then type a meaningful description for the branch site.</span></span>

5.  <span data-ttu-id="43692-121">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="43692-121">Click **Next**.</span></span>

6.  <span data-ttu-id="43692-122">Facultatif Dans la boîte de dialogue **définir un nouveau site de succursale** suivante, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="43692-122">(Optional) In the next **Define New Branch Site** dialog box, do any of the following:</span></span>
    
    1.  <span data-ttu-id="43692-123">Cliquez sur **City**, puis tapez le nom de la ville dans laquelle se trouve le site de la succursale.</span><span class="sxs-lookup"><span data-stu-id="43692-123">Click **City**, and then type the name of the city in which the branch site is located.</span></span>
    
    2.  <span data-ttu-id="43692-124">Cliquez sur **état/région**, puis tapez le nom de l’État ou de la région où se trouve le site de la succursale.</span><span class="sxs-lookup"><span data-stu-id="43692-124">Click **State/Region**, and then type the name of the state or region in which the branch site is located.</span></span>
    
    3.  <span data-ttu-id="43692-125">Cliquez sur **indicatif du pays**, puis tapez le code d’appel à deux chiffres correspondant au pays/la région où se trouve le site de la succursale.</span><span class="sxs-lookup"><span data-stu-id="43692-125">Click **Country Code**, and then type the two-digit calling code for the country/region in which the branch site is located.</span></span>

7.  <span data-ttu-id="43692-126">Cliquez sur **suivant**, puis effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="43692-126">Click **Next**, and then do one of the following:</span></span>
    
    1.  <span data-ttu-id="43692-127">Si vous utilisez une application de succursale ou un serveur Lync 2010 sur ce site, veillez à désactiver l’option **ouvrir le nouvel Assistant survie lorsque cet Assistant se ferme** .</span><span class="sxs-lookup"><span data-stu-id="43692-127">If you are using a Lync 2010 Survivable Branch Appliance or Server at this site, be sure to uncheck the **Open the New Survivable Wizard when this wizard closes** option.</span></span> <span data-ttu-id="43692-128">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="43692-128">Click **Finish**.</span></span>

8.  <span data-ttu-id="43692-129">Pour associer l’ancien serveur Lync Server 2010 SBA au pool frontal 2013 Server, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="43692-129">To associate the legacy Lync Server 2010 SBA to the Lync Server 2013 Front End pool:</span></span>
    
    1.  <span data-ttu-id="43692-130">Développez le site de succursale qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="43692-130">Expand the branch site that has been created.</span></span>
    
    2.  <span data-ttu-id="43692-131">Cliquez avec le bouton droit sur **Lync Server 2010** , puis cliquez sur **nouveau**.</span><span class="sxs-lookup"><span data-stu-id="43692-131">Right click on **Lync Server 2010** and then click **New**.</span></span>
    
    3.  <span data-ttu-id="43692-132">Cliquez sur l' **application branchement Survivable...**</span><span class="sxs-lookup"><span data-stu-id="43692-132">Click **Survivable Branch Appliance…**</span></span>

9.  <span data-ttu-id="43692-133">Suivez les instructions de l’Assistant qui s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="43692-133">Follow the directions in the wizard that opens.</span></span> <span data-ttu-id="43692-134">Pour plus d’informations sur les éléments de l’Assistant, voir [définir une unité ou un serveur de succursales survivant dans Lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md).</span><span class="sxs-lookup"><span data-stu-id="43692-134">For information about wizard items, see [Define a Survivable Branch Appliance or Server in Lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="43692-135">Une unité de branchement de Lync Server 2010 Survivable ne peut être associée qu’à un magasin de contrôle d' 2010 serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="43692-135">A Lync Server 2010 Survivable Branch Appliance can only be associated with a Lync Server 2010 Monitoring Store.</span></span>

    
    </div>

10. <span data-ttu-id="43692-136">Si vous n’utilisez pas d’appareil ou serveur de succursales survivant sur ce site, désactivez la case à cocher **ouvrir le nouvel Assistant survie lorsque cet Assistant se ferme** , puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="43692-136">If you are not using a Survivable Branch Appliance or Server at this site, clear the **Open the New Survivable Wizard when this wizard closes** check box, and then click **Finish**.</span></span>

11. <span data-ttu-id="43692-137">Répétez les étapes précédentes pour chaque site de succursale que vous voulez ajouter à la topologie.</span><span class="sxs-lookup"><span data-stu-id="43692-137">Repeat the previous steps for each branch site you want to add to the topology.</span></span>

<span data-ttu-id="43692-138"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="43692-138"></div>

<span> </span>

</div>

</div>

</span></span></div>

