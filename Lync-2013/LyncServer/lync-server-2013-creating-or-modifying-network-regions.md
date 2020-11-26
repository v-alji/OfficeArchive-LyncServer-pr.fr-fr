---
title: 'Lync Server 2013 : création ou modification de régions réseau'
description: 'Lync Server 2013 : création ou modification de régions réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating or modifying network regions
ms:assetid: bd08bb66-5976-4ece-b45c-7de19569f814
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182579(v=OCS.15)
ms:contentKeyID: 48185266
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b02a041272f0df27d2133ca26096caeb01816c7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431413"
---
# <a name="creating-or-modifying-network-regions-in-lync-server-2013"></a><span data-ttu-id="f8f32-103">Création ou modification des régions réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f8f32-103">Creating or modifying network regions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f8f32-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f8f32-104">

<span> </span></span></span>

<span data-ttu-id="f8f32-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="f8f32-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="f8f32-106">Une région réseau interconnecte diverses parties d’un réseau à plusieurs zones géographiques.</span><span class="sxs-lookup"><span data-stu-id="f8f32-106">A network region interconnects various parts of a network across multiple geographic areas.</span></span> <span data-ttu-id="f8f32-107">Chaque région du réseau doit être associée à un site central.</span><span class="sxs-lookup"><span data-stu-id="f8f32-107">Every network region must be associated with a central site.</span></span> <span data-ttu-id="f8f32-108">Le site central est le site du centre de données sur lequel le service de stratégie de bande passante de contrôle d’admission des appels (CAC) est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f8f32-108">The central site is the data center site on which the call admission control (CAC) bandwidth policy service is running.</span></span> <span data-ttu-id="f8f32-109">Vous pouvez utiliser le panneau de configuration de Lync Server pour configurer des régions réseau.</span><span class="sxs-lookup"><span data-stu-id="f8f32-109">You can use Lync Server Control Panel to configure network regions.</span></span> <span data-ttu-id="f8f32-110">Les régions réseau incluent des paramètres qui déterminent si d’autres chemins d’accès via Internet sont autorisés pour les connexions audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="f8f32-110">Network regions include settings that determine whether alternate paths through the Internet are allowed for audio and video connections.</span></span> <span data-ttu-id="f8f32-111">Dans le panneau de configuration de Lync Server, vous pouvez créer, modifier ou supprimer une région réseau.</span><span class="sxs-lookup"><span data-stu-id="f8f32-111">From the Lync Server Control Panel, you can create, modify, or delete a network region.</span></span> <span data-ttu-id="f8f32-112">Utilisez cette rubrique pour créer et modifier des régions réseau.</span><span class="sxs-lookup"><span data-stu-id="f8f32-112">Use this topic to create and modify network regions.</span></span> <span data-ttu-id="f8f32-113">Pour plus d’informations sur la suppression de régions réseau existantes, voir [Suppression de régions réseau existantes dans Lync Server 2013](lync-server-2013-deleting-existing-network-regions.md).</span><span class="sxs-lookup"><span data-stu-id="f8f32-113">For details about deleting existing network regions, see [Deleting existing network regions in Lync Server 2013](lync-server-2013-deleting-existing-network-regions.md).</span></span>

<div>

## <a name="to-create-a-network-region"></a><span data-ttu-id="f8f32-114">Pour créer une zone réseau</span><span class="sxs-lookup"><span data-stu-id="f8f32-114">To create a network region</span></span>

1.  <span data-ttu-id="f8f32-115">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="f8f32-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="f8f32-116">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f8f32-116">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f8f32-117">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="f8f32-117">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f8f32-118">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis cliquez sur **région**.</span><span class="sxs-lookup"><span data-stu-id="f8f32-118">In the left navigation bar, click **Network Configuration** and then click **Region**.</span></span>

4.  <span data-ttu-id="f8f32-119">Dans la page **région** , cliquez sur **nouveau**.</span><span class="sxs-lookup"><span data-stu-id="f8f32-119">On the **Region** page, click **New**.</span></span>

5.  <span data-ttu-id="f8f32-120">Dans la page **nouvelle région** , tapez une valeur dans le champ **nom** .</span><span class="sxs-lookup"><span data-stu-id="f8f32-120">In the **New Region** page, type a value in the **Name** field.</span></span> <span data-ttu-id="f8f32-121">Cette valeur doit être unique dans le cadre de votre déploiement de Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f8f32-121">This value must be unique within your Microsoft Lync Server 2013 deployment.</span></span>

6.  <span data-ttu-id="f8f32-122">Dans la liste déroulante **site central** , sélectionnez le site central pour cette région réseau.</span><span class="sxs-lookup"><span data-stu-id="f8f32-122">From the **Central site** drop-down list, select the central site for this network region.</span></span>

7.  <span data-ttu-id="f8f32-123">La case à cocher **activer le chemin audio alternatif** est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="f8f32-123">The **Enable audio alternate path** check box is checked by default.</span></span> <span data-ttu-id="f8f32-124">Ce champ détermine si les appels audio seront routés par le biais d’un autre chemin si la bande passante suffisante n’existe pas dans le chemin principal.</span><span class="sxs-lookup"><span data-stu-id="f8f32-124">This field determines whether audio calls will be routed through an alternate path if adequate bandwidth does not exist in the primary path.</span></span> <span data-ttu-id="f8f32-125">Désactivez cette case à cocher uniquement si vous avez besoin de désactiver le déchargement sur Internet.</span><span class="sxs-lookup"><span data-stu-id="f8f32-125">Clear this check box only if you need to turn off the offload to the Internet.</span></span> <span data-ttu-id="f8f32-126">Si l’un de vos appels sera appelé appels Internet, cette case doit être cochée, quels que soient les paramètres de bande passante.</span><span class="sxs-lookup"><span data-stu-id="f8f32-126">If any of your calls will be Internet calls, this check box must be checked, regardless of bandwidth settings.</span></span>

8.  <span data-ttu-id="f8f32-127">La case à cocher **activer le chemin vidéo alternatif** est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="f8f32-127">The **Enable video alternate path** check box is checked by default.</span></span> <span data-ttu-id="f8f32-128">Ce champ détermine si les appels vidéo sont routés par le biais d’une autre trajectoire si la bande passante suffisante n’existe pas dans le chemin principal.</span><span class="sxs-lookup"><span data-stu-id="f8f32-128">This field determines whether video calls will be routed through an alternate path if adequate bandwidth does not exist in the primary path.</span></span> <span data-ttu-id="f8f32-129">Désactivez cette case à cocher uniquement si vous avez besoin de désactiver le déchargement sur Internet.</span><span class="sxs-lookup"><span data-stu-id="f8f32-129">Clear this check box only if you need to turn off the offload to the Internet.</span></span> <span data-ttu-id="f8f32-130">Si l’un de vos appels sera appelé appels Internet, cette case doit être cochée, quels que soient les paramètres de bande passante.</span><span class="sxs-lookup"><span data-stu-id="f8f32-130">If any of your calls will be Internet calls, this check box must be checked, regardless of bandwidth settings.</span></span>

9.  <span data-ttu-id="f8f32-131">Facultatif Tapez une valeur dans le champ **Description** pour fournir plus d’informations sur cette région qui ne peut pas être exprimée à l’aide du nom seul.</span><span class="sxs-lookup"><span data-stu-id="f8f32-131">(Optional) Type a value in the **Description** field to provide more information about this region that cannot be expressed by the name alone.</span></span>

10. <span data-ttu-id="f8f32-132">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="f8f32-132">Click **Commit**.</span></span>

<span data-ttu-id="f8f32-133">La table **site associée** n’est pas utilisée pour créer une région réseau.</span><span class="sxs-lookup"><span data-stu-id="f8f32-133">The **Associated sites** table is not used for creating a network region.</span></span> <span data-ttu-id="f8f32-134">Vous associez un site à une région lorsque vous créez ou modifiez le site.</span><span class="sxs-lookup"><span data-stu-id="f8f32-134">You associate a site with a region when you create or modify the site.</span></span> <span data-ttu-id="f8f32-135">Pour plus d’informations, consultez [création ou modification de sites réseau dans Lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md).</span><span class="sxs-lookup"><span data-stu-id="f8f32-135">For details, see [Creating or modifying network sites in Lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md).</span></span>

</div>

<div>

## <a name="to-modify-a-network-region"></a><span data-ttu-id="f8f32-136">Pour modifier une zone réseau</span><span class="sxs-lookup"><span data-stu-id="f8f32-136">To modify a network region</span></span>

1.  <span data-ttu-id="f8f32-137">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="f8f32-137">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="f8f32-138">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f8f32-138">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f8f32-139">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="f8f32-139">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f8f32-140">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis cliquez sur **région**.</span><span class="sxs-lookup"><span data-stu-id="f8f32-140">In the left navigation bar, click **Network Configuration** and then click **Region**.</span></span>

4.  <span data-ttu-id="f8f32-141">Dans la page **zone** , cliquez sur la zone que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="f8f32-141">On the **Region** page, click the region that you want to modify.</span></span>

5.  <span data-ttu-id="f8f32-142">Dans le menu **Edition**, cliquez sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="f8f32-142">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="f8f32-143">Dans la page **modifier la région** , vous pouvez modifier les paramètres d’activation et de désactivation des chemins audio et vidéo, et modifier la description (pour plus de détails, reportez-vous à la section « créer une région réseau » plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="f8f32-143">On the **Edit Region** page, you can modify the settings for enabling and disabling audio and video alternate paths, and change the description (for details, see the "To create a network region" section earlier in this topic.</span></span>

7.  <span data-ttu-id="f8f32-144">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="f8f32-144">Click **Commit**.</span></span>

<span data-ttu-id="f8f32-145">Vous ne pouvez pas modifier les **sites associés** sur cette page.</span><span class="sxs-lookup"><span data-stu-id="f8f32-145">You cannot modify the **Associated sites** on this page.</span></span> <span data-ttu-id="f8f32-146">La liste des sites associés est fournie à des fins de référence, afin que vous soyez attentif aux sites qui seront affectés lors de la modification des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="f8f32-146">The list of associated sites is provided for reference so you are aware of which sites will be affected when you modify the region settings.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f8f32-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8f32-147">See Also</span></span>


[<span data-ttu-id="f8f32-148">Supprimer des zones réseau existantes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f8f32-148">Deleting existing network regions in Lync Server 2013</span></span>](lync-server-2013-deleting-existing-network-regions.md)  
[<span data-ttu-id="f8f32-149">Configurer des régions réseau pour CAC dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f8f32-149">Configure network regions for CAC in Lync Server 2013</span></span>](lync-server-2013-configure-network-regions-for-cac.md)  


[<span data-ttu-id="f8f32-150">New-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="f8f32-150">New-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion)  
[<span data-ttu-id="f8f32-151">Set-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="f8f32-151">Set-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkRegion)  
[<span data-ttu-id="f8f32-152">Remove-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="f8f32-152">Remove-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkRegion)  
[<span data-ttu-id="f8f32-153">Get-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="f8f32-153">Get-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink)  
  

<span data-ttu-id="f8f32-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f8f32-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

