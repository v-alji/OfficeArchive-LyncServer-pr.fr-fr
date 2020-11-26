---
title: 'Lync Server 2013 : création ou modification de sites réseau'
description: 'Lync Server 2013 : création ou modification de sites réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating or modifying network sites
ms:assetid: 358aa08a-c5bc-45fc-8017-19e6202f88c5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520975(v=OCS.15)
ms:contentKeyID: 48183801
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 700f089cfe190a8f46b5eefc05e656e7c62a59a9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431385"
---
# <a name="creating-or-modifying-network-sites-in-lync-server-2013"></a><span data-ttu-id="9045c-103">Création ou modification de sites réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9045c-103">Creating or modifying network sites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9045c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9045c-104">

<span> </span></span></span>

<span data-ttu-id="9045c-105">_**Dernière modification de la rubrique :** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="9045c-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="9045c-106">Les sites réseau sont les bureaux ou les emplacements configurés dans chaque région d’un contrôle d’admission des appels (CAC) ou un déploiement 9-1-1 amélioré.</span><span class="sxs-lookup"><span data-stu-id="9045c-106">Network sites are the offices or locations configured within each region of a call admission control (CAC) or Enhanced 9-1-1 deployment.</span></span> <span data-ttu-id="9045c-107">Vous pouvez utiliser le panneau de configuration Microsoft Lync Server 2013 pour configurer les sites et les associer à des régions.</span><span class="sxs-lookup"><span data-stu-id="9045c-107">You can use the Microsoft Lync Server 2013 Control Panel to configure sites and associate them with regions.</span></span> <span data-ttu-id="9045c-108">Par exemple, une région réseau pour l’Amérique du Nord peut être associée à des sites réseaux tels que Chicago, Redmond et Vancouver.</span><span class="sxs-lookup"><span data-stu-id="9045c-108">For example, a network region for North America might be associated with networks sites such as Chicago, Redmond, and Vancouver.</span></span> <span data-ttu-id="9045c-109">Un site réseau CAC doit être créé pour chaque site au sein d’une organisation, même si ce site n’a pas de limitations de bande passante.</span><span class="sxs-lookup"><span data-stu-id="9045c-109">A CAC network site must be created for every site within an organization, even if that site has no bandwidth limitations.</span></span> <span data-ttu-id="9045c-110">Le panneau de configuration de Lync Server vous permet de créer, de modifier et de supprimer des sites réseau.</span><span class="sxs-lookup"><span data-stu-id="9045c-110">From the Lync Server Control Panel you can create, modify, and delete network sites.</span></span> <span data-ttu-id="9045c-111">Pour créer ou modifier un site réseau, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="9045c-111">Use the following procedures to create or modify a network site.</span></span> <span data-ttu-id="9045c-112">Pour plus d’informations sur la suppression d’un site réseau existant, reportez-vous à [la rubrique Suppression d’un site réseau existant dans Lync Server 2013](lync-server-2013-deleting-an-existing-network-site.md).</span><span class="sxs-lookup"><span data-stu-id="9045c-112">For details on deleting an existing network site, see [Deleting an existing network site in Lync Server 2013](lync-server-2013-deleting-an-existing-network-site.md).</span></span>

<div>

## <a name="to-create-a-network-site"></a><span data-ttu-id="9045c-113">Pour créer un site réseau</span><span class="sxs-lookup"><span data-stu-id="9045c-113">To create a network site</span></span>

1.  <span data-ttu-id="9045c-114">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="9045c-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="9045c-115">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9045c-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="9045c-116">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="9045c-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="9045c-117">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis cliquez sur **site**.</span><span class="sxs-lookup"><span data-stu-id="9045c-117">In the left navigation bar, click **Network Configuration** and then click **Site**.</span></span>

4.  <span data-ttu-id="9045c-118">Sur la page du **site** , cliquez sur **nouveau**.</span><span class="sxs-lookup"><span data-stu-id="9045c-118">On the **Site** page, click **New**.</span></span>

5.  <span data-ttu-id="9045c-119">Dans **nouveau site**, tapez un nom pour ce site dans le champ **nom** .</span><span class="sxs-lookup"><span data-stu-id="9045c-119">In **New Site**, type a name for this site in the **Name** field.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9045c-120">Les noms de site doivent être uniques dans le déploiement de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9045c-120">Site names must be unique within the Lync Server 2013 deployment.</span></span>

    
    </div>

6.  <span data-ttu-id="9045c-121">Dans la liste déroulante **région** , sélectionnez une région réseau à associer à ce site.</span><span class="sxs-lookup"><span data-stu-id="9045c-121">In the **Region** drop-down list, select a network region to associate with this site.</span></span>

7.  <span data-ttu-id="9045c-122">Facultatif Si vous voulez appliquer des limitations de bande passante pour les appels audio ou vidéo vers ce site, sélectionnez le profil de la stratégie de bande passante avec les paramètres appropriés dans la liste déroulante **stratégie de bande passante** .</span><span class="sxs-lookup"><span data-stu-id="9045c-122">(Optional) If you want to place bandwidth limitations on audio or video calls to this site, select the bandwidth policy profile with the appropriate settings from the **Bandwidth policy** drop-down list.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9045c-123">Vous pouvez afficher les détails des profils de stratégie de bande passante disponibles ou créer un nouveau profil de stratégie de bande passante dans la page profil de la <STRONG>stratégie</STRONG> du groupe de <STRONG>configuration du réseau</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="9045c-123">You can view the details of the available bandwidth policy profiles, or create a new bandwidth policy profile, on the <STRONG>Policy Profile</STRONG> page of the <STRONG>Network Configuration</STRONG> group.</span></span> <span data-ttu-id="9045c-124">Pour plus d’informations, reportez-vous à <A href="lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md">créer ou modifier des profils de stratégie de bande passante dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="9045c-124">For details, see <A href="lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md">Creating or modifying bandwidth policy profiles in Lync Server 2013</A>.</span></span>

    
    </div>

8.  <span data-ttu-id="9045c-125">Facultatif Si vous voulez fournir des paramètres d’emplacement pour ce site, sélectionnez une stratégie d’emplacement dans la liste déroulante **stratégie d’emplacement** .</span><span class="sxs-lookup"><span data-stu-id="9045c-125">(Optional) If you want to provide location settings for this site, select a location policy from the **Location policy** drop-down list.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9045c-126">La stratégie d’emplacement attribue des paramètres de 9-1-1 et d’emplacement client spécifiques au site.</span><span class="sxs-lookup"><span data-stu-id="9045c-126">The location policy assigns specific Enhanced 9-1-1 (E9-1-1) and client location settings to the site.</span></span> <span data-ttu-id="9045c-127">Vous pouvez afficher les détails des stratégies d’emplacement disponibles ou créer une nouvelle stratégie d’emplacement à partir de la page <STRONG>stratégie d’emplacement</STRONG> du groupe de <STRONG>Configuration réseau</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="9045c-127">You can view the details of the available location policies, or create a new location policy, from the <STRONG>Location Policy</STRONG> page of the <STRONG>Network Configuration</STRONG> group.</span></span> <span data-ttu-id="9045c-128">Pour plus d’informations, reportez-vous à la rubrique <A href="lync-server-2013-viewing-location-policy-information.md">affichage des informations de stratégie d’emplacement dans Lync Server 2013</A></span><span class="sxs-lookup"><span data-stu-id="9045c-128">For details, see <A href="lync-server-2013-viewing-location-policy-information.md">Viewing location policy information in Lync Server 2013</A>.</span></span>

    
    </div>

9.  <span data-ttu-id="9045c-129">Facultatif Tapez une valeur dans le champ **Description** pour fournir des informations supplémentaires sur ce site qui ne peut pas être exprimé uniquement par le nom.</span><span class="sxs-lookup"><span data-stu-id="9045c-129">(Optional) Type a value in the **Description** field to provide more information about this site that cannot be expressed by the name alone.</span></span>

10. <span data-ttu-id="9045c-130">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="9045c-130">Click **Commit**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9045c-131">Vous n’utilisez pas la table de <STRONG>sous-réseaux associés</STRONG> lorsque vous créez un site réseau.</span><span class="sxs-lookup"><span data-stu-id="9045c-131">You do not use the <STRONG>Associated Subnets</STRONG> table when you create a new network site.</span></span> <span data-ttu-id="9045c-132">Vous associez un sous-réseau à un site lors de la création ou de la modification du sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="9045c-132">You associate a subnet with a site when you create or modify the subnet.</span></span> <span data-ttu-id="9045c-133">Pour plus d’informations, reportez-vous à <A href="lync-server-2013-create-or-modify-network-subnets.md">créer ou modifier des sous-réseaux réseau dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="9045c-133">For details, see <A href="lync-server-2013-create-or-modify-network-subnets.md">Create or modify network subnets in Lync Server 2013</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="to-modify-a-network-site"></a><span data-ttu-id="9045c-134">Pour modifier un site réseau</span><span class="sxs-lookup"><span data-stu-id="9045c-134">To modify a network site</span></span>

1.  <span data-ttu-id="9045c-135">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="9045c-135">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="9045c-136">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9045c-136">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="9045c-137">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="9045c-137">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="9045c-138">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis cliquez sur **site**.</span><span class="sxs-lookup"><span data-stu-id="9045c-138">In the left navigation bar, click **Network Configuration** and then click **Site**.</span></span>

4.  <span data-ttu-id="9045c-139">Sur la page du **site** , cliquez sur le site que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="9045c-139">On the **Site** page, click the site that you want to modify.</span></span>

5.  <span data-ttu-id="9045c-140">Dans le menu **Edition**, cliquez sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="9045c-140">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="9045c-141">Dans la page **modifier le site** , vous pouvez modifier la description, la région, le profil de la stratégie de bande passante et la stratégie d’emplacement associées au site.</span><span class="sxs-lookup"><span data-stu-id="9045c-141">On the **Edit Site** page, you can modify the description, region, bandwidth policy profile, and location policy associated with the site.</span></span> <span data-ttu-id="9045c-142">Pour plus d’informations, consultez la section « pour créer un site réseau » plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="9045c-142">For details, see "To create a network site" section earlier in this topic.</span></span>

7.  <span data-ttu-id="9045c-143">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="9045c-143">Click **Commit**.</span></span>

<span data-ttu-id="9045c-144">Vous ne pouvez pas modifier le tableau sous- **réseaux associés** sur cette page.</span><span class="sxs-lookup"><span data-stu-id="9045c-144">You cannot modify the **Associated Subnets** table on this page.</span></span> <span data-ttu-id="9045c-145">La liste des sous-réseaux associés est fournie à des fins de référence afin de savoir quels sous-réseaux seront affectés lorsque vous modifiez les paramètres du site.</span><span class="sxs-lookup"><span data-stu-id="9045c-145">The list of associated subnets is provided for reference so that you are aware of what subnets will be affected when you modify the site settings.</span></span>

</div>

<div>

## <a name="to-delete-a-network-site"></a><span data-ttu-id="9045c-146">Pour supprimer un site réseau</span><span class="sxs-lookup"><span data-stu-id="9045c-146">To delete a network site</span></span>

1.  <span data-ttu-id="9045c-147">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="9045c-147">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="9045c-148">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9045c-148">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="9045c-149">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="9045c-149">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="9045c-150">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis cliquez sur **site**.</span><span class="sxs-lookup"><span data-stu-id="9045c-150">In the left navigation bar, click **Network Configuration** and then click **Site**.</span></span>

4.  <span data-ttu-id="9045c-151">Sur la page du **site** , cliquez sur le site que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="9045c-151">On the **Site** page, click the site that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9045c-152">Vous pouvez supprimer plusieurs sites à la fois.</span><span class="sxs-lookup"><span data-stu-id="9045c-152">You can delete more than one site at a time.</span></span> <span data-ttu-id="9045c-153">Pour cela, appuyez sur CTRL et sélectionnez plusieurs sites tout en maintenant la touche CTRL enfoncée.</span><span class="sxs-lookup"><span data-stu-id="9045c-153">To do this, press CTRL and select multiple sites while holding down the CTRL key.</span></span> <span data-ttu-id="9045c-154">Pour sélectionner tous les sites, dans le menu <STRONG>Edition</STRONG> , cliquez sur <STRONG>Sélectionner tout</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="9045c-154">Or, to select all sites, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="9045c-155">Dans le menu **modifier** , cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="9045c-155">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="9045c-156">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="9045c-156">Click **OK**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="9045c-157">Vous ne pouvez pas supprimer un site réseau s’il est associé à un sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="9045c-157">You cannot remove a network site if it is associated with a network subnet.</span></span> <span data-ttu-id="9045c-158">Si vous tentez de supprimer un site associé à un sous-réseau, vous recevez un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9045c-158">If you attempt to remove a site associated with a subnet you will receive an error message.</span></span> <span data-ttu-id="9045c-159">Pour savoir si un site est associé à des sous-réseaux, cliquez sur le site, puis cliquez sur <STRONG>afficher les détails</STRONG> dans le menu <STRONG>modifier</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="9045c-159">To see if a site is associated with any subnets, click the site and then click <STRONG>Show details</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9045c-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9045c-160">See Also</span></span>


[<span data-ttu-id="9045c-161">Suppression d’un site réseau existant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9045c-161">Deleting an existing network site in Lync Server 2013</span></span>](lync-server-2013-deleting-an-existing-network-site.md)  


[<span data-ttu-id="9045c-162">New-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="9045c-162">New-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite)  
[<span data-ttu-id="9045c-163">Set-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="9045c-163">Set-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkSite)  
[<span data-ttu-id="9045c-164">Remove-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="9045c-164">Remove-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkSite)  
[<span data-ttu-id="9045c-165">Get-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="9045c-165">Get-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSite)  
  

<span data-ttu-id="9045c-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9045c-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

