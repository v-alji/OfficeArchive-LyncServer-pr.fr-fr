---
title: 'Lync Server 2013 : création ou modification de sous-réseaux réseau'
description: 'Lync Server 2013 : création ou modification de sous-réseaux réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify network subnets
ms:assetid: 1ba8c4e3-fbc7-4758-88ac-d651fef17bed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520957(v=OCS.15)
ms:contentKeyID: 48183548
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37695707bf39b10c351a4990b132c9799406f9c4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431651"
---
# <a name="create-or-modify-network-subnets-in-lync-server-2013"></a><span data-ttu-id="ff93c-103">Créer ou modifier des sous-réseaux réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ff93c-103">Create or modify network subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ff93c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ff93c-104">

<span> </span></span></span>

<span data-ttu-id="ff93c-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="ff93c-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="ff93c-106">Un sous-réseau doit être associé à un site réseau pour vous permettre de déterminer l’emplacement géographique de l’hôte appartenant à ce sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="ff93c-106">A network subnet must be associated with a network site for the purposes of determining the geographic location of the host belonging to this subnet.</span></span> <span data-ttu-id="ff93c-107">Le panneau de configuration de Lync Server vous permet de configurer les sous-réseaux.</span><span class="sxs-lookup"><span data-stu-id="ff93c-107">You can use Lync Server Control Panel to configure subnets.</span></span> <span data-ttu-id="ff93c-108">Dans le panneau de configuration de Lync Server, vous pouvez créer, modifier ou supprimer un sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="ff93c-108">From the Lync Server Control Panel, you can create, modify, or delete a network subnet.</span></span> <span data-ttu-id="ff93c-109">Pour plus d’informations sur la suppression de sous-réseaux réseau, voir [Suppression de sous-réseaux réseau dans Lync Server 2013](lync-server-2013-deleting-network-subnets.md).</span><span class="sxs-lookup"><span data-stu-id="ff93c-109">For details about deleting network subnets, see [Deleting network subnets in Lync Server 2013](lync-server-2013-deleting-network-subnets.md).</span></span>

<span data-ttu-id="ff93c-110">Dans la plupart des déploiements de Microsoft Lync Server 2013 sur lequel est implémenté le contrôle d’admission des appels, il existe généralement un grand nombre de sous-réseaux.</span><span class="sxs-lookup"><span data-stu-id="ff93c-110">In most deployments of Microsoft Lync Server 2013 where call admission control (CAC) is implemented, there will typically be a large number of subnets.</span></span> <span data-ttu-id="ff93c-111">Pour cette raison, il est souvent préférable de configurer les sous-réseaux à partir de Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="ff93c-111">Because of this, it is often best to configure subnets from the Lync Server Management Shell.</span></span> <span data-ttu-id="ff93c-112">À partir de là, vous pouvez appeler **New-CsNetworkSubnet** conjointement avec l’applet de cmdlet Windows PowerShell **Import-CSV**.</span><span class="sxs-lookup"><span data-stu-id="ff93c-112">From there you can call **New-CsNetworkSubnet** in conjunction with the Windows PowerShell cmdlet **Import-CSV**.</span></span> <span data-ttu-id="ff93c-113">L’utilisation conjointe de ces applets de passe vous permet de lire les paramètres de sous-réseau à partir d’un fichier de valeurs séparées par des virgules (. csv) et de créer plusieurs sous-réseaux en même temps.</span><span class="sxs-lookup"><span data-stu-id="ff93c-113">By using these cmdlets together, you can read in subnet settings from a comma-separated values (.csv) file and create multiple subnets at the same time.</span></span> <span data-ttu-id="ff93c-114">Pour obtenir des exemples sur la façon de créer des sous-réseaux à partir d’un fichier. csv, voir [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span><span class="sxs-lookup"><span data-stu-id="ff93c-114">For examples of how to create subnets from a .csv file, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<div>

## <a name="to-create-a-network-subnet"></a><span data-ttu-id="ff93c-115">Pour créer un sous-réseau du réseau</span><span class="sxs-lookup"><span data-stu-id="ff93c-115">To create a network subnet</span></span>

1.  <span data-ttu-id="ff93c-116">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="ff93c-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ff93c-117">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ff93c-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ff93c-118">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ff93c-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ff93c-119">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis sur **sous-réseau**.</span><span class="sxs-lookup"><span data-stu-id="ff93c-119">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="ff93c-120">Sur la page **sous-réseau** , cliquez sur **nouveau**.</span><span class="sxs-lookup"><span data-stu-id="ff93c-120">On the **Subnet** page, click **New**.</span></span>

5.  <span data-ttu-id="ff93c-121">Dans **nouveau sous-réseau**, entrez une valeur dans le champ **ID de sous-réseau** .</span><span class="sxs-lookup"><span data-stu-id="ff93c-121">In **New Subnet**, enter a value in the **Subnet ID** field.</span></span> <span data-ttu-id="ff93c-122">Il doit s’agir d’une adresse IP (par exemple, 174.11.12.0) et doit être la première adresse de la plage d’adresses IP définie par le sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="ff93c-122">This must be an IP address (for example, 174.11.12.0), and it must be the first address in the IP address range defined by the subnet.</span></span>

6.  <span data-ttu-id="ff93c-123">Dans le champ **masque** , entrez une valeur numérique comprise entre 1 et 32.</span><span class="sxs-lookup"><span data-stu-id="ff93c-123">In the **Mask** field, enter a numeric value from 1 through 32.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ff93c-124">Cette valeur correspond au masque de passe à appliquer au sous-réseau qui est créé.</span><span class="sxs-lookup"><span data-stu-id="ff93c-124">This value is the bitmask that is to be applied to the subnet being created.</span></span>

    
    </div>

7.  <span data-ttu-id="ff93c-125">Dans **ID du site réseau**, sélectionnez le site auquel appartient ce sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="ff93c-125">In **Network site ID**, select the site to which this subnet belongs.</span></span>

8.  <span data-ttu-id="ff93c-126">Facultatif Tapez une valeur dans le champ **Description** pour fournir davantage d’informations sur ce sous-réseau qui ne peut pas être exprimé par le nom seul.</span><span class="sxs-lookup"><span data-stu-id="ff93c-126">(Optional) Type a value in the **Description** field to provide more information about this subnet that cannot be expressed by the name alone.</span></span>

9.  <span data-ttu-id="ff93c-127">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="ff93c-127">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-a-network-subnet"></a><span data-ttu-id="ff93c-128">Pour modifier un sous-réseau</span><span class="sxs-lookup"><span data-stu-id="ff93c-128">To modify a network subnet</span></span>

1.  <span data-ttu-id="ff93c-129">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="ff93c-129">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ff93c-130">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ff93c-130">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ff93c-131">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ff93c-131">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ff93c-132">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis sur **sous-réseau**.</span><span class="sxs-lookup"><span data-stu-id="ff93c-132">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="ff93c-133">Dans la page de **sous-réseau** , cliquez sur le sous-réseau que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="ff93c-133">On the **Subnet** page, click the subnet that you want to modify.</span></span>

5.  <span data-ttu-id="ff93c-134">Dans le menu **Edition**, cliquez sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="ff93c-134">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="ff93c-135">Dans la page **modifier le sous-réseau** , vous pouvez modifier le masque de la page, le site réseau associé ou la description.</span><span class="sxs-lookup"><span data-stu-id="ff93c-135">On the **Edit Subnet** page, you can modify the bitmask, associated network site, or description.</span></span> <span data-ttu-id="ff93c-136">Si vous modifiez le masque de réinitialisation, n’oubliez pas que l’ID de sous-réseau doit toujours être la première adresse de la plage d’adresses IP définie par le sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="ff93c-136">If you modify the bitmask, keep in mind that the Subnet ID must still be the first address in the IP address range defined by the subnet.</span></span>

7.  <span data-ttu-id="ff93c-137">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="ff93c-137">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ff93c-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff93c-138">See Also</span></span>


[<span data-ttu-id="ff93c-139">Supprimer des sous-réseaux réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ff93c-139">Deleting network subnets in Lync Server 2013</span></span>](lync-server-2013-deleting-network-subnets.md)  


[<span data-ttu-id="ff93c-140">À propos des régions réseau, des sites réseau et des sous-réseaux dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ff93c-140">About network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-about-network-regions-sites-and-subnets.md)  


[<span data-ttu-id="ff93c-141">New-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="ff93c-141">New-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet)  
[<span data-ttu-id="ff93c-142">Set-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="ff93c-142">Set-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkSubnet)  
[<span data-ttu-id="ff93c-143">Remove-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="ff93c-143">Remove-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkSubnet)  
[<span data-ttu-id="ff93c-144">Get-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="ff93c-144">Get-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSubnet)  
  

<span data-ttu-id="ff93c-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ff93c-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

