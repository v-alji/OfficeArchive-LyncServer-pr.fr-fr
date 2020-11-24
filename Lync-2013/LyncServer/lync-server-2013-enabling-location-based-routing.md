---
title: 'Lync Server 2013 : activation du routage Location-Based'
description: 'Lync Server 2013 : activation du routage Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling Location-Based Routing
ms:assetid: 029ede7e-0c4e-4ad2-af99-909ae674d6fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994014(v=OCS.15)
ms:contentKeyID: 51803920
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7844af5792468cd5645b6b42c857c63b943c2df1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394717"
---
# <a name="enabling-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="66206-103">Activation du routage Location-Based dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="66206-103">Enabling Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="66206-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="66206-104">

<span> </span></span></span>

<span data-ttu-id="66206-105">_**Dernière modification de la rubrique :** 2013-04-26_</span><span class="sxs-lookup"><span data-stu-id="66206-105">_**Topic Last Modified:** 2013-04-26_</span></span>

<span data-ttu-id="66206-106">Après le déploiement d’Enterprise Voice et des régions du réseau, des sites et des sous-réseaux sont définis, vous pouvez activer le routage Location-Based.</span><span class="sxs-lookup"><span data-stu-id="66206-106">Once Enterprise Voice is deployed and network regions, sites and subnets are defined, you can enable Location-Based Routing.</span></span> <span data-ttu-id="66206-107">Location-Based routage doit être activé pour les éléments vocaux d’entreprise suivants :</span><span class="sxs-lookup"><span data-stu-id="66206-107">Location-Based Routing must be enabled for the following Enterprise Voice elements:</span></span>

  - <span data-ttu-id="66206-108">Sites réseau</span><span class="sxs-lookup"><span data-stu-id="66206-108">Network sites</span></span>

  - <span data-ttu-id="66206-109">Configurations de Trunk</span><span class="sxs-lookup"><span data-stu-id="66206-109">Trunk configurations</span></span>

  - <span data-ttu-id="66206-110">Stratégies de voix</span><span class="sxs-lookup"><span data-stu-id="66206-110">Voice policies</span></span>

  - <span data-ttu-id="66206-111">Configuration de routage</span><span class="sxs-lookup"><span data-stu-id="66206-111">Routing configuration</span></span>

<div>

## <a name="enable-location-based-routing-to-network-sites"></a><span data-ttu-id="66206-112">Activer Location-Based le routage sur les sites réseau</span><span class="sxs-lookup"><span data-stu-id="66206-112">Enable Location-Based Routing to Network Sites</span></span>

<span data-ttu-id="66206-113">Après avoir déployé Enterprise Voice et configuré les sites réseau, vous pouvez configurer le routage Location-Based.</span><span class="sxs-lookup"><span data-stu-id="66206-113">After you have deployed Enterprise Voice, and configured network sites, you are ready to configure Location-Based Routing.</span></span> <span data-ttu-id="66206-114">Tout d’abord, vous devez créer une stratégie de routage vocal pour associer le site réseau aux utilisations RTC appropriées.</span><span class="sxs-lookup"><span data-stu-id="66206-114">First, you create a voice routing policy to associate the network site with the appropriate PSTN usages.</span></span> <span data-ttu-id="66206-115">Lorsque vous attribuez des utilisations RTC à une stratégie de routage vocale, n’utilisez que les utilisations RTC associées à des itinéraires vocaux qui utilisent une passerelle PSTN locale vers le site ou une passerelle RTC située dans une région où Location-Based restrictions de routage ne sont pas nécessaires. Utilisez la commande Windows PowerShell de Lync Server, le nouveau-CsVoiceRoutingPolicy ou le panneau de configuration de Lync Server pour créer des stratégies de routage de messagerie vocale.</span><span class="sxs-lookup"><span data-stu-id="66206-115">When assigning PSTN usages to a voice routing policy, make sure to only use PSTN usages that are associated to voice routes that use a PSTN gateway local to the site or a PSTN gateway that is located in a region where Location-Based Routing restrictions are not needed.Use the Lync Server Windows PowerShell command, New-CsVoiceRoutingPolicy, or Lync Server Control Panel to create voice routing policies.</span></span>

    New-CsVoiceRoutingPolicy -Identity <voice routing policy ID> -Name <voice routing policy name> -PstnUsages <usages>

<span data-ttu-id="66206-116">Pour plus d’informations, consultez la rubrique [New-CsVoiceRoutingPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoiceRoutingPolicy).</span><span class="sxs-lookup"><span data-stu-id="66206-116">For more information, see [New-CsVoiceRoutingPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoiceRoutingPolicy).</span></span>

<span data-ttu-id="66206-117">Pour cet exemple, les commandes de tableau et Windows PowerShell suivantes montrent deux stratégies de routage de voix et leurs utilisations RTC associées définies dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="66206-117">For this example, the following table and Windows PowerShell commands illustrate two voice routing policies and their associated PSTN usages defined in this scenario.</span></span> <span data-ttu-id="66206-118">Seuls les paramètres spécifiques au routage Location-Based sont inclus dans la table à des fins d’illustration.</span><span class="sxs-lookup"><span data-stu-id="66206-118">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsVoiceRoutingPolicy -Identity "DelhiVoiceRoutingPolicy" -Name "Delhi voice routing policy" -PstnUsages @{add="Delhi usage", "PBX Del usage", "PBX Hyd usage"}
    New-CsVoiceRoutingPolicy -Identity "HyderabadVoiceRoutingPolicy" -Name " Hyderabad voice routing policy" -PstnUsages @{add="Hyderabad usage", "PBX Del usage", "PBX Hyd usage"}


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="66206-119">Politique de routage de la voix 1</span><span class="sxs-lookup"><span data-stu-id="66206-119">Voice routing policy 1</span></span></th>
<th><span data-ttu-id="66206-120">Politique de routage de la voix 2</span><span class="sxs-lookup"><span data-stu-id="66206-120">Voice routing policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66206-121">ID de la stratégie vocale</span><span class="sxs-lookup"><span data-stu-id="66206-121">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="66206-122">Politique de routage vocal de Delhi</span><span class="sxs-lookup"><span data-stu-id="66206-122">Delhi voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="66206-123">Politique de routage vocale Hyderabad</span><span class="sxs-lookup"><span data-stu-id="66206-123">Hyderabad voice routing policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66206-124">Usages RTC</span><span class="sxs-lookup"><span data-stu-id="66206-124">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="66206-125">Utilisation de Delhi, utilisation de PBX del, utilisation du PBX HYD</span><span class="sxs-lookup"><span data-stu-id="66206-125">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="66206-126">Utilisation de Hyderabad, utilisation de PBX HYD, utilisation de PBX del</span><span class="sxs-lookup"><span data-stu-id="66206-126">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
</tbody>
</table>

  

<span data-ttu-id="66206-127">Ensuite, configurez le routage de Location-Based pour les sites réseau concernés et associez-leur des stratégies de routage de votre voix.</span><span class="sxs-lookup"><span data-stu-id="66206-127">Next, configure Location-Based Routing for the applicable network sites and associate your voice routing policies to them.</span></span> <span data-ttu-id="66206-128">Utilisez la commande Windows PowerShell de Lync Server, New-CsNetworkSite, pour activer Location-Based le routage et associer des stratégies de routage de messagerie vocale à vos sites réseau qui doivent appliquer des restrictions de routage.</span><span class="sxs-lookup"><span data-stu-id="66206-128">Use the Lync Server Windows PowerShell command, New-CsNetworkSite, to enable Location-Based Routing and associate voice routing policies to your network sites that must enforce routing restrictions.</span></span>

    Set-CsNetworkSite -Identity <site ID> -EnableLocationBasedRouting <$true|$false> -VoiceRoutingPolicy <voice routing policy ID>

<span data-ttu-id="66206-129">Dans cet exemple, le tableau ci-dessous illustre le routage Location-Based de deux sites réseau différents, Delhi et Hyderabad, définis dans ce scénario à l’aide de Lync Server Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="66206-129">In this example, the following table illustrates Location-Based Routing for two different network sites, Delhi and Hyderabad, defined in this scenario using the Lync Server Windows PowerShell.</span></span> <span data-ttu-id="66206-130">Seuls les paramètres spécifiques au routage Location-Based sont inclus dans la table à des fins d’illustration.</span><span class="sxs-lookup"><span data-stu-id="66206-130">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    Set-CsNetworkSite -Identity "Delhi" -EnableLocationBasedRouting $true -VoiceRoutingPolicy "DelhiVoiceRoutingPolicy"
    Set-CsNetworkSite -Identity "Hyderabad" -EnableLocationBasedRouting $true -VoiceRoutingPolicy "HyderabadVoiceRoutingPolicy"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="66206-131">Site 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="66206-131">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="66206-132">Site 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="66206-132">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66206-133">Nom du site</span><span class="sxs-lookup"><span data-stu-id="66206-133">Site Name</span></span></p></td>
<td><p><span data-ttu-id="66206-134">Site 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="66206-134">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="66206-135">Site 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="66206-135">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66206-136">EnableLocationBasedRouting</span><span class="sxs-lookup"><span data-stu-id="66206-136">EnableLocationBasedRouting</span></span></p></td>
<td><p><span data-ttu-id="66206-137">Vrai</span><span class="sxs-lookup"><span data-stu-id="66206-137">True</span></span></p></td>
<td><p><span data-ttu-id="66206-138">Vrai</span><span class="sxs-lookup"><span data-stu-id="66206-138">True</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66206-139">Politique de routage de la voix</span><span class="sxs-lookup"><span data-stu-id="66206-139">Voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="66206-140">Politique de routage vocal de Delhi</span><span class="sxs-lookup"><span data-stu-id="66206-140">Delhi voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="66206-141">Politique de routage vocale Hyderabad</span><span class="sxs-lookup"><span data-stu-id="66206-141">Hyderabad voice routing policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66206-142">Sous-réseaux</span><span class="sxs-lookup"><span data-stu-id="66206-142">Subnets</span></span></p></td>
<td><p><span data-ttu-id="66206-143">Sous-réseau 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="66206-143">Subnet 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="66206-144">Sous-réseau 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="66206-144">Subnet 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-to-trunks"></a><span data-ttu-id="66206-145">Activer Location-Based le routage vers les lignes</span><span class="sxs-lookup"><span data-stu-id="66206-145">Enable Location-Based Routing to Trunks</span></span>

<span data-ttu-id="66206-146">Pour que la configuration de Trunk puisse être activée pour le routage Location-Based, vous devez créer une configuration de Trunk pour chaque Trunk ou chaque site réseau.</span><span class="sxs-lookup"><span data-stu-id="66206-146">Before a trunk configuration can be enabled for Location-Based Routing, you need to create a trunk configuration for each trunk or each network site.</span></span> <span data-ttu-id="66206-147">Pour créer une configuration de Trunk, utilisez la commande Windows PowerShell de Lync Server, New-CsTrunkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="66206-147">Use the Lync Server Windows PowerShell command, New-CsTrunkConfiguration, to create a trunk configuration.</span></span> <span data-ttu-id="66206-148">Si plusieurs lignes sont associées à un système (c’est-à-dire, à la passerelle ou au PBX), chaque configuration de Trunk doit être modifiée pour permettre Location-Based restrictions de routage.</span><span class="sxs-lookup"><span data-stu-id="66206-148">If multiple trunks are associated with a given system (i.e. Gateway or PBX), each trunk configuration must be modified to enable Location-Based Routing restrictions.</span></span>

    New-CsTrunkConfiguration -Identity < trunk configuration ID>

<span data-ttu-id="66206-149">Pour plus d’informations, reportez-vous à [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span><span class="sxs-lookup"><span data-stu-id="66206-149">For more information, see [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span></span>

<span data-ttu-id="66206-150">Pour cet exemple, les commandes Windows PowerShell suivantes montrent comment créer une configuration de Trunk pour chaque Trunk dans le déploiement défini dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="66206-150">For this example, the following Windows PowerShell commands illustrate creating one trunk configuration for each trunk in the deployment defined in this scenario.</span></span>

    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 1 DEL-GW>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 2 HYD-GW>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 3 DEL-PBX>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 4 HYD-PBX>"

<span data-ttu-id="66206-151">Une fois qu’une configuration de Trunk est configurée par Trunk, vous pouvez utiliser la commande Windows PowerShell de Lync Server, Set-CsTrunkConfiguration, pour activer Location-Based le routage sur vos lignes de Trunk qui doivent appliquer des restrictions de routage.</span><span class="sxs-lookup"><span data-stu-id="66206-151">Once a trunk configuration is configured per trunk, you can use the Lync Server Windows PowerShell command, Set-CsTrunkConfiguration, to enable Location-Based Routing to your trunks that must enforce routing restrictions.</span></span> <span data-ttu-id="66206-152">Activez Location-Based le routage vers des lignes pour acheminer les appels vers les passerelles RTC qui routent les appels vers le RTC et associez le site réseau où se trouve la passerelle.</span><span class="sxs-lookup"><span data-stu-id="66206-152">Enable Location-Based Routing to trunks that route calls to PSTN gateways that route calls to the PSTN, and associate the network site where the gateway is located.</span></span>

    Set-CsTrunkConfiguration -Identity <trunk configuration ID> -EnableLocationRestriction $true -NetworkSiteID <site ID>

<span data-ttu-id="66206-153">Pour plus d’informations, reportez-vous à [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span><span class="sxs-lookup"><span data-stu-id="66206-153">For more information, see [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span></span>

<span data-ttu-id="66206-154">Dans cet exemple, Location-Based routage est activé pour chaque Trunk associé aux passerelles RTC dans Delhi et Hyderabad :</span><span class="sxs-lookup"><span data-stu-id="66206-154">In this example, Location-Based Routing is enabled for each trunk that is associated to PSTN gateways in Delhi and Hyderabad:</span></span>

    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 1 DEL-GW -EnableLocationRestriction $true -NetworkSiteID "Delhi"
    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 2 HYD-GW -EnableLocationRestriction $true -NetworkSiteID "Hyderabad"

  

<span data-ttu-id="66206-155">N’activez pas le routage Location-Based pour les lignes qui ne routent pas les appels vers le RTC ; Toutefois, vous devez toujours associer le Trunk au site réseau où se trouve le système en tant que Location-Based les restrictions de routage doivent être appliquées pour les appels RTC atteignant des points de terminaison connectés par le biais de ce Trunk.</span><span class="sxs-lookup"><span data-stu-id="66206-155">Do not enable Location-Based Routing for trunks that do not route calls to the PSTN; however, you must still associate the trunk to the network site where the system is located as Location-Based Routing restrictions need to be enforced for PSTN calls reaching endpoints connected via this trunk.</span></span> <span data-ttu-id="66206-156">Pour cet exemple, Location-Based routage n’est pas activé pour chaque Trunk associé aux systèmes PBX dans Delhi et Hyderabad :</span><span class="sxs-lookup"><span data-stu-id="66206-156">For this example, Location-Based Routing is not enabled for each trunk that is associated to PBX systems in Delhi and Hyderabad:</span></span>

    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 3 DEL-PBX -EnableLocationRestriction $false -NetworkSiteID "Delhi"
    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 4 HYD-PBX -EnableLocationRestriction $false -NetworkSiteID "Hyderabad"

  
<span data-ttu-id="66206-157">Les points de terminaison qui sont connectés à des systèmes qui ne routent pas les appels vers le RTC (par exemple, un PBX) présentent des restrictions similaires aux points de terminaison Lync des utilisateurs pour le routage Location-Based.</span><span class="sxs-lookup"><span data-stu-id="66206-157">Endpoints that are connected to systems that do not route calls to the PSTN (i.e. a PBX) will have similar restrictions as Lync endpoints of users enabled for Location-Based Routing.</span></span> <span data-ttu-id="66206-158">Cela signifie que ces utilisateurs seront en mesure de passer et de recevoir des appels vers et à partir de l’utilisateur Lync indépendamment de l’emplacement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="66206-158">This means that these users will be able to place and receive calls to and from Lync user regardless of the user’s location.</span></span> <span data-ttu-id="66206-159">Ils seront également en mesure de passer des appels de réception vers et à partir d’autres systèmes qui ne routent pas les appels vers le réseau PSTN (par exemple, un point de terminaison connecté à un autre système PBX), quel que soit le site du réseau auquel le système est associé.</span><span class="sxs-lookup"><span data-stu-id="66206-159">They will also be able to place an receive calls to and from other systems that do not route calls to the PSTN network (i.e. an endpoint connected to a different PBX) regardless of the network site to which the system is associated.</span></span> <span data-ttu-id="66206-160">Tous les appels entrants, les appels sortants, les transferts d’appel et le transfert d’appel impliquant des points de terminaison RTC sont soumis aux Location-Based de routage.</span><span class="sxs-lookup"><span data-stu-id="66206-160">All inbound calls, outbound calls, call transfers and call forwarding involving PSTN endpoints will be subject to Location-Based Routing enforcements.</span></span> <span data-ttu-id="66206-161">Ces appels doivent uniquement utiliser des passerelles RTC définies comme locales pour ces systèmes.</span><span class="sxs-lookup"><span data-stu-id="66206-161">Such calls must use only PSTN gateways that are defined as local to such systems.</span></span>

<span data-ttu-id="66206-162">Le tableau suivant illustre la configuration de Trunk de quatre Trunks dans deux sites réseau différents : deux connectés à des passerelles RTC et deux connectés à des systèmes PBX.</span><span class="sxs-lookup"><span data-stu-id="66206-162">The following table illustrates the trunk configuration of four trunks in two different network sites: two connected to PSTN gateways and two connected to PBX systems.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66206-163">Nom</span><span class="sxs-lookup"><span data-stu-id="66206-163">Name</span></span></th>
<th><span data-ttu-id="66206-164">EnableLocationRestriction</span><span class="sxs-lookup"><span data-stu-id="66206-164">EnableLocationRestriction</span></span></th>
<th><span data-ttu-id="66206-165">NetworkSiteID</span><span class="sxs-lookup"><span data-stu-id="66206-165">NetworkSiteID</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66206-166">PstnGateway : Trunk 1 DEL-GW</span><span class="sxs-lookup"><span data-stu-id="66206-166">PstnGateway:Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="66206-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="66206-167">True</span></span></p></td>
<td><p><span data-ttu-id="66206-168">Site 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="66206-168">Site 1 (Delhi)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66206-169">PstnGateway : Trunk 2 HYD-GW</span><span class="sxs-lookup"><span data-stu-id="66206-169">PstnGateway:Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="66206-170">Vrai</span><span class="sxs-lookup"><span data-stu-id="66206-170">True</span></span></p></td>
<td><p><span data-ttu-id="66206-171">Site 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="66206-171">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66206-172">PstnGateway : Trunk 3 DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="66206-172">PstnGateway:Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="66206-173">False</span><span class="sxs-lookup"><span data-stu-id="66206-173">False</span></span></p></td>
<td><p><span data-ttu-id="66206-174">Site 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="66206-174">Site 1 (Delhi)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66206-175">PstnGateway : Trunk 4 HYD-PBX</span><span class="sxs-lookup"><span data-stu-id="66206-175">PstnGateway:Trunk 4 HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="66206-176">False</span><span class="sxs-lookup"><span data-stu-id="66206-176">False</span></span></p></td>
<td><p><span data-ttu-id="66206-177">Site 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="66206-177">Site 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-to-voice-policies"></a><span data-ttu-id="66206-178">Activer Location-Based le routage sur les stratégies vocales</span><span class="sxs-lookup"><span data-stu-id="66206-178">Enable Location-Based Routing to Voice Policies</span></span>

<span data-ttu-id="66206-179">Pour garantir le routage Location-Based vers des utilisateurs spécifiques, configurez la politique vocale de ces utilisateurs de sorte qu’ils n’empêchent pas les appels vocaux RTC.</span><span class="sxs-lookup"><span data-stu-id="66206-179">To enforce Location-Based Routing to specific users, configure those users’ voice policy to prevent PSTN toll bypass.</span></span> <span data-ttu-id="66206-180">Pour activer Location-Based le routage par le biais de l’utilisation d’une stratégie existante, utilisez la commande Lync Server Windows PowerShell, New-CsVoicePolicy, pour créer une nouvelle stratégie vocale ou Set-CsVoicePolicy</span><span class="sxs-lookup"><span data-stu-id="66206-180">Use the Lync Server Windows PowerShell command, New-CsVoicePolicy, to create a new voice policy or Set-CsVoicePolicy, if using an existing policy, to enable Location-Based Routing by preventing PSTN toll bypass.</span></span>

    Set-CsVoicePolicy -Identity <voice policy ID> -PreventPSTNTollBypass <$true|$false>

<span data-ttu-id="66206-181">Pour plus d’informations, reportez-vous à [New-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoicePolicy).</span><span class="sxs-lookup"><span data-stu-id="66206-181">For more information, see [New-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoicePolicy).</span></span>

<span data-ttu-id="66206-182">Pour cet exemple, les commandes de tableau et de Windows PowerShell suivantes illustrent l’activation de la fonctionnalité de prévention des appels payants RTC aux politiques vocales Delhi et Hyderabad définies dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="66206-182">For this example, the following table and Windows PowerShell commands illustrate enabling the prevention of PSTN toll bypass to the Delhi and Hyderabad voice policies defined in this scenario.</span></span> <span data-ttu-id="66206-183">Seuls les paramètres spécifiques au routage Location-Based sont inclus dans la table à des fins d’illustration.</span><span class="sxs-lookup"><span data-stu-id="66206-183">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    Set-CsVoicePolicy -Identity "Delhi voice policy" -PreventPSTNTollBypass $true
    Set-CsVoicePolicy -Identity "Hyderabad voice policy" -PreventPSTNTollBypass $true


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="66206-184">Politique vocale 1</span><span class="sxs-lookup"><span data-stu-id="66206-184">Voice policy 1</span></span></th>
<th><span data-ttu-id="66206-185">Politique vocale 2</span><span class="sxs-lookup"><span data-stu-id="66206-185">Voice policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66206-186">ID de la stratégie vocale</span><span class="sxs-lookup"><span data-stu-id="66206-186">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="66206-187">Politique vocale de Delhi</span><span class="sxs-lookup"><span data-stu-id="66206-187">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="66206-188">Politique vocale Hyderabad</span><span class="sxs-lookup"><span data-stu-id="66206-188">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66206-189">Usages RTC</span><span class="sxs-lookup"><span data-stu-id="66206-189">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="66206-190">Utilisation de Delhi, utilisation de PBX del, utilisation du PBX HYD</span><span class="sxs-lookup"><span data-stu-id="66206-190">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="66206-191">Utilisation de Hyderabad, utilisation de PBX HYD, utilisation de PBX del</span><span class="sxs-lookup"><span data-stu-id="66206-191">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66206-192">PreventPSTNTollBypass</span><span class="sxs-lookup"><span data-stu-id="66206-192">PreventPSTNTollBypass</span></span></p></td>
<td><p><span data-ttu-id="66206-193">Vrai</span><span class="sxs-lookup"><span data-stu-id="66206-193">True</span></span></p></td>
<td><p><span data-ttu-id="66206-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="66206-194">True</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-in-the-routing-configuration"></a><span data-ttu-id="66206-195">Activer le routage Location-Based dans la configuration de routage</span><span class="sxs-lookup"><span data-stu-id="66206-195">Enable Location-Based Routing in the routing configuration</span></span>

<span data-ttu-id="66206-196">Enfin, activez globalement le routage Location-Based vers votre configuration de routage.</span><span class="sxs-lookup"><span data-stu-id="66206-196">Finally, globally enable Location-Based Routing to your routing configuration.</span></span> <span data-ttu-id="66206-197">Pour activer Location-Based le routage, utilisez la commande Windows PowerShell de Lync Server, New-CsRoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="66206-197">Use the Lync Server Windows PowerShell command, New-CsRoutingConfiguration, to enable Location-Based Routing.</span></span>

    Set-CsRoutingConfiguration -EnableLocationBasedRouting $true

<span data-ttu-id="66206-198">Pour plus d’informations, consultez la rubrique [Set-CsRoutingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsRoutingConfiguration).</span><span class="sxs-lookup"><span data-stu-id="66206-198">For more information, see [Set-CsRoutingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsRoutingConfiguration).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="66206-199">Si Location-Based routage doit être activé via une configuration globale, l’ensemble de règles à appliquer sera appliqué uniquement aux sites, utilisateurs et Trunks pour lesquels il a été configuré comme spécifié dans cette documentation.</span><span class="sxs-lookup"><span data-stu-id="66206-199">while Location-Based Routing must be enabled via a global configuration, the set of rules to be applied will only be enforced for the sites, users and trunks for which it has been configured as specified in this documentation.</span></span>



</div>

<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="66206-200">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66206-200">See Also</span></span>


[<span data-ttu-id="66206-201">Configuration du routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="66206-201">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="66206-202"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="66206-202"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

