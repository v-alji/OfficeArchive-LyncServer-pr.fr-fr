---
title: 'Lync Server 2013 : déploiement de zones, de sites et de sous-réseaux réseau'
description: 'Lync Server 2013 : déploiement de zones, de sites et de sous-réseaux réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying network regions, sites, and subnets
ms:assetid: c4b75601-3538-4d07-8d23-1ad90459ae48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994067(v=OCS.15)
ms:contentKeyID: 51803978
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1c4c08cd9b78b1439000cdb4a7bbe3ffc2f99d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429845"
---
# <a name="deploying-network-regions-sites-and-subnets-in-lync-server-2013"></a><span data-ttu-id="e8228-103">Déploiement de zones, sites et sous-réseaux réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e8228-103">Deploying network regions, sites, and subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e8228-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e8228-104">

<span> </span></span></span>

<span data-ttu-id="e8228-105">_**Dernière modification de la rubrique :** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="e8228-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="e8228-106">Après le déploiement d’Enterprise Voice, vous devez configurer les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e8228-106">Once Enterprise Voice is deployed, you need to configure:</span></span>

  - <span data-ttu-id="e8228-107">Régions réseau</span><span class="sxs-lookup"><span data-stu-id="e8228-107">Network regions</span></span>

  - <span data-ttu-id="e8228-108">Sites réseau</span><span class="sxs-lookup"><span data-stu-id="e8228-108">Network sites</span></span>

  - <span data-ttu-id="e8228-109">Sous-réseaux réseau</span><span class="sxs-lookup"><span data-stu-id="e8228-109">Network subnets</span></span>

<div>

## <a name="define-network-regions"></a><span data-ttu-id="e8228-110">Définir des régions réseau</span><span class="sxs-lookup"><span data-stu-id="e8228-110">Define Network Regions</span></span>

<span data-ttu-id="e8228-111">Pour définir les zones du réseau, utilisez la commande Windows PowerShell de Lync Server, le nouveau-CsNetworkRegion ou le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e8228-111">Use the Lync Server Windows PowerShell command, New-CsNetworkRegion, or Lync Server Control Panel to define network regions.</span></span>

    New-CsNetworkRegion -NetworkRegionID <region ID> -CentralSite <site ID>

<span data-ttu-id="e8228-112">Pour plus d’informations, reportez-vous à [New-CsNetworkRegion](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion).</span><span class="sxs-lookup"><span data-stu-id="e8228-112">For more information, see [New-CsNetworkRegion](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion).</span></span>

<span data-ttu-id="e8228-113">Pour cet exemple, la commande Windows PowerShell suivante illustre la région du réseau, région 1 (Inde), définie dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="e8228-113">For this example, the following Windows PowerShell command illustrates the network region, region 1 (India), defined in this scenario.</span></span>

    New-CsNetworkRegion -NetworkRegionID "India" -CentralSite "India Central Site"

<div>


</div>

</div>

<div>

## <a name="define-network-sites"></a><span data-ttu-id="e8228-114">Définir des sites réseau</span><span class="sxs-lookup"><span data-stu-id="e8228-114">Define Network Sites</span></span>

<span data-ttu-id="e8228-115">Utilisez la commande Windows PowerShell de Lync Server, le nouveau-CsNetworkSite ou le panneau de configuration de Lync Server pour définir les sites réseau.</span><span class="sxs-lookup"><span data-stu-id="e8228-115">Use the Lync Server Windows PowerShell command, New-CsNetworkSite, or the Lync Server Control Panel to define network sites.</span></span>

    New-CsNetworkSite -NetworkSiteID <site ID> -NetworkRegionID <region ID>

<span data-ttu-id="e8228-116">Pour plus d’informations, reportez-vous à [New-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite).</span><span class="sxs-lookup"><span data-stu-id="e8228-116">For more information, see [New-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite).</span></span>

<span data-ttu-id="e8228-117">Pour cet exemple, le tableau suivant et la commande Windows PowerShell Lync Server illustrent les sites réseau définis dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="e8228-117">For this example, the following table and Lync Server Windows PowerShell command illustrate the network sites defined in this scenario.</span></span> <span data-ttu-id="e8228-118">Seuls les paramètres spécifiques au routage Location-Based sont inclus dans la table à des fins d’illustration.</span><span class="sxs-lookup"><span data-stu-id="e8228-118">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsNetworkSite -NetworkSiteID "Delhi" -NetworkRegionID "India"
    New-CsNetworkSite -NetworkSiteID "Hyderabad" -NetworkRegionID "India"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="e8228-119">Site 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="e8228-119">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="e8228-120">Site 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="e8228-120">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8228-121">ID de site</span><span class="sxs-lookup"><span data-stu-id="e8228-121">Site ID</span></span></p></td>
<td><p><span data-ttu-id="e8228-122">Site 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="e8228-122">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="e8228-123">Site 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="e8228-123">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8228-124">ID de région</span><span class="sxs-lookup"><span data-stu-id="e8228-124">Region ID</span></span></p></td>
<td><p><span data-ttu-id="e8228-125">Région 1 (Inde)</span><span class="sxs-lookup"><span data-stu-id="e8228-125">Region 1 (India)</span></span></p></td>
<td><p><span data-ttu-id="e8228-126">Région 1 (Inde)</span><span class="sxs-lookup"><span data-stu-id="e8228-126">Region 1 (India)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="define-network-subnets"></a><span data-ttu-id="e8228-127">Définir des sous-réseaux réseau</span><span class="sxs-lookup"><span data-stu-id="e8228-127">Define Network Subnets</span></span>

<span data-ttu-id="e8228-128">Utilisez la commande Windows PowerShell de Lync Server, le nouveau-CsNetworkSubnet ou le panneau de configuration de Lync Server pour définir des sous-réseaux réseau et les affecter à des sites réseau.</span><span class="sxs-lookup"><span data-stu-id="e8228-128">Use the Lync Server Windows PowerShell command, New-CsNetworkSubnet, or the Lync Server Control Panel to define network subnets and assign them to network sites.</span></span>

    New-CsNetworkSubnet -SubnetID <Subnet IP address> -MaskBits <Subnet bitmask> -NetworkSiteID <site ID>

<span data-ttu-id="e8228-129">Pour plus d’informations, reportez-vous à [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span><span class="sxs-lookup"><span data-stu-id="e8228-129">For more information, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<span data-ttu-id="e8228-130">Pour cet exemple, les commandes de tableau et Windows PowerShell suivantes montrent l’affectation de sous-réseaux réseau aux sites réseau, Delhi et Hyderabad définis dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="e8228-130">For this example, the following table and Windows PowerShell commands illustrate the assignment of network subnets to the network sites, Delhi and Hyderabad, defined in this scenario.</span></span> <span data-ttu-id="e8228-131">Seuls les paramètres spécifiques au routage Location-Based sont inclus dans la table à des fins d’illustration.</span><span class="sxs-lookup"><span data-stu-id="e8228-131">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsNetworkSubnet -SubnetID "192.168.0.0" -MaskBits "24" -NetworkSiteID "Delhi"
    New-CsNetworkSubnet -SubnetID "192.168.1.0" -MaskBits "24" -NetworkSiteID "Hyderabad"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="e8228-132">Site 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="e8228-132">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="e8228-133">Site 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="e8228-133">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8228-134">ID de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="e8228-134">Subnet ID</span></span></p></td>
<td><p><span data-ttu-id="e8228-135">192.168.0.0</span><span class="sxs-lookup"><span data-stu-id="e8228-135">192.168.0.0</span></span></p></td>
<td><p><span data-ttu-id="e8228-136">192.168.1.0</span><span class="sxs-lookup"><span data-stu-id="e8228-136">192.168.1.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8228-137">Réseau</span><span class="sxs-lookup"><span data-stu-id="e8228-137">Mask</span></span></p></td>
<td><p><span data-ttu-id="e8228-138">24</span><span class="sxs-lookup"><span data-stu-id="e8228-138">24</span></span></p></td>
<td><p><span data-ttu-id="e8228-139">24</span><span class="sxs-lookup"><span data-stu-id="e8228-139">24</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8228-140">ID de site</span><span class="sxs-lookup"><span data-stu-id="e8228-140">Site ID</span></span></p></td>
<td><p><span data-ttu-id="e8228-141">Site 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="e8228-141">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="e8228-142">Site 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="e8228-142">Site 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e8228-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8228-143">See Also</span></span>


[<span data-ttu-id="e8228-144">Configuration du routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e8228-144">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="e8228-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e8228-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

