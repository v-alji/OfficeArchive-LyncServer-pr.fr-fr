---
title: 'Lync Server 2013 : création ou modification des itinéraires de la région réseau'
description: 'Lync Server 2013 : création ou modification des itinéraires de la région réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating or modifying network region routes
ms:assetid: 76993daa-76c2-4cec-8363-de8aebef0145
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521016(v=OCS.15)
ms:contentKeyID: 48184540
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 89106c905419778776ea16341f247027d49f1195
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431427"
---
# <a name="creating-or-modifying-network-region-routes-in-lync-server-2013"></a><span data-ttu-id="71df9-103">Création ou modification des itinéraires de région réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="71df9-103">Creating or modifying network region routes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="71df9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="71df9-104">

<span> </span></span></span>

<span data-ttu-id="71df9-105">_**Dernière modification de la rubrique :** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="71df9-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="71df9-106">Chaque région au sein d’une configuration de contrôle d’admission des appels (CAC) doit disposer d’un moyen d’accéder à toutes les autres régions.</span><span class="sxs-lookup"><span data-stu-id="71df9-106">Every region within a call admission control (CAC) configuration must have some way to access every other region.</span></span> <span data-ttu-id="71df9-107">Lorsque les liaisons de zone définissent des limitations de bande passante pour les connexions entre les régions et représentent également les liens physiques, un itinéraire détermine le chemin d’accès lié que la connexion traverse d’une région à l’autre.</span><span class="sxs-lookup"><span data-stu-id="71df9-107">While region links set bandwidth limitations on the connections between regions and also represent the physical links, a route determines which linked path the connection will traverse from one region to another.</span></span> <span data-ttu-id="71df9-108">Vous pouvez utiliser le panneau de configuration de Lync Server pour configurer les itinéraires de région réseau.</span><span class="sxs-lookup"><span data-stu-id="71df9-108">You can use Lync Server Control Panel to configure network region routes.</span></span> <span data-ttu-id="71df9-109">Dans le panneau de configuration de Lync Server, vous pouvez créer, modifier ou supprimer un itinéraire de la région du réseau.</span><span class="sxs-lookup"><span data-stu-id="71df9-109">From Lync Server Control Panel, you can create, modify, or delete a network region route.</span></span> <span data-ttu-id="71df9-110">Utilisez cette rubrique pour créer ou modifier un itinéraire de la région du réseau.</span><span class="sxs-lookup"><span data-stu-id="71df9-110">Use this topic to create or modify a network region route.</span></span> <span data-ttu-id="71df9-111">Pour plus d’informations sur la suppression d’un itinéraire de région réseau existant, voir [Suppression d’itinéraires de région réseau existants dans Lync Server 2013](lync-server-2013-deleting-existing-network-region-routes.md).</span><span class="sxs-lookup"><span data-stu-id="71df9-111">For details about deleting an existing network region routes, see [Deleting existing network region routes in Lync Server 2013](lync-server-2013-deleting-existing-network-region-routes.md).</span></span>

<div>

## <a name="to-create-a-network-region-route"></a><span data-ttu-id="71df9-112">Pour créer un itinéraire de la région du réseau</span><span class="sxs-lookup"><span data-stu-id="71df9-112">To create a network region route</span></span>

1.  <span data-ttu-id="71df9-113">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="71df9-113">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="71df9-114">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="71df9-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="71df9-115">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="71df9-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="71df9-116">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis sur **itinéraire des régions**.</span><span class="sxs-lookup"><span data-stu-id="71df9-116">In the left navigation bar, click **Network Configuration** and then click **Region Route**.</span></span>

4.  <span data-ttu-id="71df9-117">Sur la page itinéraire de la **région** , cliquez sur **nouveau**.</span><span class="sxs-lookup"><span data-stu-id="71df9-117">On the **Region Route** page, click **New**.</span></span>

5.  <span data-ttu-id="71df9-118">Dans la **zone nouvel itinéraire** de la région, tapez une valeur dans le champ **nom** .</span><span class="sxs-lookup"><span data-stu-id="71df9-118">In **New Region Route**, type a value in the **Name** field.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="71df9-119">Cette valeur doit être unique dans le cadre de votre déploiement de Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="71df9-119">This value must be unique within your Microsoft Lync Server 2013 deployment.</span></span>

    
    </div>

6.  <span data-ttu-id="71df9-120">Dans la liste déroulante **région de réseau \# 1** , sélectionnez l’une des deux régions auxquelles vous voulez être connectée par cet itinéraire.</span><span class="sxs-lookup"><span data-stu-id="71df9-120">From the **Network region \#1** drop-down list, select one of the two regions to be connected by this route.</span></span>

7.  <span data-ttu-id="71df9-121">Dans la liste déroulante de la **région réseau \# 2** , sélectionnez une autre région pour ce routage.</span><span class="sxs-lookup"><span data-stu-id="71df9-121">From the **Network region \#2** drop-down list, select the other region for this route.</span></span> <span data-ttu-id="71df9-122">Cette région doit être différente de la région sélectionnée pour la région réseau \# 1.</span><span class="sxs-lookup"><span data-stu-id="71df9-122">This region must be different from the region selected for Network region \#1.</span></span>

8.  <span data-ttu-id="71df9-123">Utilisez la zone de liste **liaisons de région réseau** pour ajouter des liens de région à l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="71df9-123">Use the **Network region links** list box to add region links to the route.</span></span> <span data-ttu-id="71df9-124">Cliquez sur le bouton **Ajouter** pour afficher la page de liaison de la **zone** .</span><span class="sxs-lookup"><span data-stu-id="71df9-124">Click the **Add** button to display the **Region Link** page.</span></span> <span data-ttu-id="71df9-125">Cliquez sur le lien d’une région pour l’ajouter à ce routage, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="71df9-125">Click a region link to add to this route, and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="71df9-126">Continuez à cliquer sur le bouton <STRONG>Ajouter</STRONG> pour ajouter d’autres liens, ou sélectionnez un lien et cliquez sur <STRONG>supprimer</STRONG> pour supprimer un lien.</span><span class="sxs-lookup"><span data-stu-id="71df9-126">Continue to click the <STRONG>Add</STRONG> button to add more links, or select a link and click <STRONG>Remove</STRONG> to remove a link.</span></span>

    
    </div>

9.  <span data-ttu-id="71df9-127">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="71df9-127">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-a-network-region-route"></a><span data-ttu-id="71df9-128">Pour modifier un itinéraire de la région du réseau</span><span class="sxs-lookup"><span data-stu-id="71df9-128">To modify a network region route</span></span>

1.  <span data-ttu-id="71df9-129">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="71df9-129">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="71df9-130">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="71df9-130">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="71df9-131">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="71df9-131">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="71df9-132">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis sur **itinéraire des régions**.</span><span class="sxs-lookup"><span data-stu-id="71df9-132">In the left navigation bar, click **Network Configuration** and then click **Region Route**.</span></span>

4.  <span data-ttu-id="71df9-133">Sur la page itinéraire de la **région** , cliquez sur le secteur que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="71df9-133">On the **Region Route** page, click the region route that you want to modify.</span></span>

5.  <span data-ttu-id="71df9-134">Dans le menu **Edition**, cliquez sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="71df9-134">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="71df9-135">Dans la **zone modifier le routage** des régions, vous pouvez modifier les régions jointes par cet itinéraire et les liaisons de région associées à l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="71df9-135">In **Edit Region Route**, you can modify the regions joined by this route and the region links associated with the route.</span></span>

7.  <span data-ttu-id="71df9-136">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="71df9-136">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="71df9-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71df9-137">See Also</span></span>


[<span data-ttu-id="71df9-138">Supprimer des itinéraires de région réseau existants dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="71df9-138">Deleting existing network region routes in Lync Server 2013</span></span>](lync-server-2013-deleting-existing-network-region-routes.md)  
  

<span data-ttu-id="71df9-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="71df9-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

