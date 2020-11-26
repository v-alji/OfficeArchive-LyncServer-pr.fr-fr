---
title: 'Lync Server 2013 : suppression des régions réseau existantes'
description: 'Lync Server 2013 : suppression des régions réseau existantes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting existing network regions
ms:assetid: c7293a2f-2b49-4c4a-903f-f7edcea2bc5f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721882(v=OCS.15)
ms:contentKeyID: 49733815
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b148f0bd92ad398ab7057a5a291bf3245df3e47e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430321"
---
# <a name="deleting-existing-network-regions-in-lync-server-2013"></a><span data-ttu-id="6ad2b-103">Supprimer des zones réseau existantes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ad2b-103">Deleting existing network regions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6ad2b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6ad2b-104">

<span> </span></span></span>

<span data-ttu-id="6ad2b-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="6ad2b-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="6ad2b-106">Une région réseau interconnecte diverses parties d’un réseau à plusieurs zones géographiques.</span><span class="sxs-lookup"><span data-stu-id="6ad2b-106">A network region interconnects various parts of a network across multiple geographic areas.</span></span> <span data-ttu-id="6ad2b-107">Chaque région du réseau doit être associée à un site central.</span><span class="sxs-lookup"><span data-stu-id="6ad2b-107">Every network region must be associated with a central site.</span></span> <span data-ttu-id="6ad2b-108">Le site central est le site du centre de données sur lequel le service de stratégie de bande passante de contrôle d’admission des appels (CAC) est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6ad2b-108">The central site is the data center site on which the call admission control (CAC) bandwidth policy service is running.</span></span> <span data-ttu-id="6ad2b-109">Vous pouvez utiliser le panneau de configuration de Lync Server pour configurer des régions réseau.</span><span class="sxs-lookup"><span data-stu-id="6ad2b-109">You can use Lync Server Control Panel to configure network regions.</span></span> <span data-ttu-id="6ad2b-110">Les régions réseau incluent des paramètres qui déterminent si d’autres chemins d’accès via Internet sont autorisés pour les connexions audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="6ad2b-110">Network regions include settings that determine whether alternate paths through the Internet are allowed for audio and video connections.</span></span> <span data-ttu-id="6ad2b-111">Dans le panneau de configuration de Lync Server, vous pouvez créer, modifier ou supprimer une région réseau.</span><span class="sxs-lookup"><span data-stu-id="6ad2b-111">From the Lync Server Control Panel, you can create, modify, or delete a network region.</span></span> <span data-ttu-id="6ad2b-112">Utilisez cette rubrique pour supprimer des régions réseau existantes.</span><span class="sxs-lookup"><span data-stu-id="6ad2b-112">Use this topic to delete existing network regions.</span></span> <span data-ttu-id="6ad2b-113">Pour plus d’informations sur la création ou la modification de régions réseau existantes, voir [création ou modification des régions réseau dans Lync Server 2013](lync-server-2013-creating-or-modifying-network-regions.md).</span><span class="sxs-lookup"><span data-stu-id="6ad2b-113">For details about creating or modifying existing network regions, see [Creating or modifying network regions in Lync Server 2013](lync-server-2013-creating-or-modifying-network-regions.md).</span></span>

<div>

## <a name="to-delete-a-network-region"></a><span data-ttu-id="6ad2b-114">Pour supprimer une zone réseau</span><span class="sxs-lookup"><span data-stu-id="6ad2b-114">To delete a network region</span></span>

1.  <span data-ttu-id="6ad2b-115">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="6ad2b-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="6ad2b-116">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6ad2b-116">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="6ad2b-117">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6ad2b-117">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="6ad2b-118">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis cliquez sur **région**.</span><span class="sxs-lookup"><span data-stu-id="6ad2b-118">In the left navigation bar, click **Network Configuration** and then click **Region**.</span></span>

4.  <span data-ttu-id="6ad2b-119">Dans la page **zone** , cliquez sur la zone que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="6ad2b-119">On the **Region** page, click the region you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="6ad2b-120">Vous pouvez supprimer plusieurs régions à la fois.</span><span class="sxs-lookup"><span data-stu-id="6ad2b-120">You can delete more than one region at a time.</span></span> <span data-ttu-id="6ad2b-121">Pour cela, appuyez sur CTRL et sélectionnez plusieurs régions tout en maintenant la touche CTRL enfoncée.</span><span class="sxs-lookup"><span data-stu-id="6ad2b-121">To do this, press CTRL and select multiple regions while holding down the CTRL key.</span></span> <span data-ttu-id="6ad2b-122">Vous pouvez sélectionner toutes les <STRONG>régions dans le</STRONG> menu <STRONG>Edition</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="6ad2b-122">Or, to select all regions, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="6ad2b-123">Dans le menu **modifier** , cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="6ad2b-123">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="6ad2b-124">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ad2b-124">Click **OK**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="6ad2b-125">Une région réseau ne peut pas être supprimée si elle est associée à un site réseau.</span><span class="sxs-lookup"><span data-stu-id="6ad2b-125">A network region cannot be removed if it is associated with a network site.</span></span> <span data-ttu-id="6ad2b-126">Si vous tentez de supprimer une région associée à un site, vous recevez un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="6ad2b-126">If you attempt to remove a region associated with a site you will receive an error message.</span></span> <span data-ttu-id="6ad2b-127">Pour déterminer si une région est associée à des sites, sélectionnez la région, puis cliquez sur <STRONG>afficher les détails</STRONG> dans le menu <STRONG>modifier</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="6ad2b-127">To see if a region is associated with any sites, select the region and then click <STRONG>Show details</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6ad2b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ad2b-128">See Also</span></span>


[<span data-ttu-id="6ad2b-129">Création ou modification des régions réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ad2b-129">Creating or modifying network regions in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-regions.md)  
  

<span data-ttu-id="6ad2b-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6ad2b-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

