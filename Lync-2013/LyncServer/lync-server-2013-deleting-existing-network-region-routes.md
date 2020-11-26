---
title: 'Lync Server 2013 : suppression des itinéraires de région réseau existants'
description: 'Lync Server 2013 : suppression des itinéraires de région réseau existants.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting existing network region routes
ms:assetid: 6256ff80-5f1e-48b4-928b-24aeb3c1a0e7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688074(v=OCS.15)
ms:contentKeyID: 49733669
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c2501dc3f4ed88a56e9f591e3af11a673046280a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430335"
---
# <a name="deleting-existing-network-region-routes-in-lync-server-2013"></a><span data-ttu-id="4bd64-103">Supprimer des itinéraires de région réseau existants dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4bd64-103">Deleting existing network region routes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4bd64-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4bd64-104">

<span> </span></span></span>

<span data-ttu-id="4bd64-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="4bd64-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="4bd64-106">Chaque région au sein d’une configuration de contrôle d’admission des appels (CAC) doit disposer d’un moyen d’accéder à toutes les autres régions.</span><span class="sxs-lookup"><span data-stu-id="4bd64-106">Every region within a call admission control (CAC) configuration must have some way to access every other region.</span></span> <span data-ttu-id="4bd64-107">Lorsque les liaisons de zone définissent des limitations de bande passante pour les connexions entre les régions et représentent également les liens physiques, un itinéraire détermine le chemin d’accès lié que la connexion traverse d’une région à l’autre.</span><span class="sxs-lookup"><span data-stu-id="4bd64-107">While region links set bandwidth limitations on the connections between regions and also represent the physical links, a route determines which linked path the connection will traverse from one region to another.</span></span> <span data-ttu-id="4bd64-108">Vous pouvez utiliser le panneau de configuration de Lync Server pour configurer les itinéraires de région réseau.</span><span class="sxs-lookup"><span data-stu-id="4bd64-108">You can use Lync Server Control Panel to configure network region routes.</span></span> <span data-ttu-id="4bd64-109">Dans le panneau de configuration de Lync Server, vous pouvez créer, modifier ou supprimer un itinéraire de la région du réseau.</span><span class="sxs-lookup"><span data-stu-id="4bd64-109">From Lync Server Control Panel, you can create, modify, or delete a network region route.</span></span> <span data-ttu-id="4bd64-110">Utilisez cette rubrique pour supprimer des itinéraires de la région de réseau existants.</span><span class="sxs-lookup"><span data-stu-id="4bd64-110">Use this topic to delete existing network region routes.</span></span> <span data-ttu-id="4bd64-111">Pour plus d’informations sur la création et la modification des itinéraires de région réseau, voir [création ou modification des itinéraires de région réseau dans Lync Server 2013](lync-server-2013-creating-or-modifying-network-region-routes.md).</span><span class="sxs-lookup"><span data-stu-id="4bd64-111">For details about creating or modifying network region routes, see [Creating or modifying network region routes in Lync Server 2013](lync-server-2013-creating-or-modifying-network-region-routes.md).</span></span>

<div>

## <a name="to-delete-a-network-region-route"></a><span data-ttu-id="4bd64-112">Pour supprimer un itinéraire de la région du réseau</span><span class="sxs-lookup"><span data-stu-id="4bd64-112">To delete a network region route</span></span>

1.  <span data-ttu-id="4bd64-113">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="4bd64-113">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="4bd64-114">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="4bd64-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="4bd64-115">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="4bd64-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="4bd64-116">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis sur **itinéraire des régions**.</span><span class="sxs-lookup"><span data-stu-id="4bd64-116">In the left navigation bar, click **Network Configuration** and then click **Region Route**.</span></span>

4.  <span data-ttu-id="4bd64-117">Sur la page itinéraire de la **région** , cliquez sur le secteur que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="4bd64-117">On the **Region Route** page, click the region route that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4bd64-118">Vous pouvez supprimer plusieurs itinéraires par région à la fois.</span><span class="sxs-lookup"><span data-stu-id="4bd64-118">You can delete more than one region route at a time.</span></span> <span data-ttu-id="4bd64-119">Pour cela, appuyez sur CTRL et sélectionnez plusieurs itinéraires de région tout en maintenant la touche CTRL enfoncée.</span><span class="sxs-lookup"><span data-stu-id="4bd64-119">To do this, press CTRL and select multiple region routes while holding down the CTRL key.</span></span> <span data-ttu-id="4bd64-120">Pour sélectionner tous les itinéraires de région, cliquez sur <STRONG>Sélectionner tout</STRONG> dans le menu <STRONG>édition</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="4bd64-120">Or, to select all region routes, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="4bd64-121">Dans le menu **modifier** , cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="4bd64-121">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="4bd64-122">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="4bd64-122">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4bd64-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bd64-123">See Also</span></span>


[<span data-ttu-id="4bd64-124">Création ou modification des itinéraires de région réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4bd64-124">Creating or modifying network region routes in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-region-routes.md)  


<span data-ttu-id="4bd64-125">[Configurer un itinéraire de région réseau](https://technet.microsoft.com/library/gg133706\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="4bd64-125">[Configure a Network Region Route](https://technet.microsoft.com/library/gg133706\(v=ocs.15\))</span></span>  


[<span data-ttu-id="4bd64-126">New-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="4bd64-126">New-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkInterRegionRoute)  
[<span data-ttu-id="4bd64-127">Set-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="4bd64-127">Set-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkInterRegionRoute)  
[<span data-ttu-id="4bd64-128">Remove-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="4bd64-128">Remove-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkInterRegionRoute)  
[<span data-ttu-id="4bd64-129">Get-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="4bd64-129">Get-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterRegionRoute)  
  

<span data-ttu-id="4bd64-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4bd64-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

