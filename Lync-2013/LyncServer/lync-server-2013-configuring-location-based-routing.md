---
title: 'Lync Server 2013 : Configuration du routage géodépendant'
description: 'Lync Server 2013 : configuration du routage Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Location-Based Routing
ms:assetid: 63cdc474-e80f-43b1-a237-9d9ed673300a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994036(v=OCS.15)
ms:contentKeyID: 51803946
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 080c2a3a82a8714fc35ce882b0c6cb1630552f27
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433039"
---
# <a name="configuring-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="4527f-103">Configuration du routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4527f-103">Configuring Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4527f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4527f-104">

<span> </span></span></span>

<span data-ttu-id="4527f-105">_**Dernière modification de la rubrique :** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="4527f-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="4527f-106">Lync Server 2013 CU1, le routage Location-Based est une fonctionnalité de voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="4527f-106">Lync Server 2013 CU1, Location-Based Routing is a feature of Enterprise Voice.</span></span> <span data-ttu-id="4527f-107">Location-Based le routage est une fonctionnalité de gestion des appels qui contrôle le routage des appels par Lync Server 2013 CU1.</span><span class="sxs-lookup"><span data-stu-id="4527f-107">Location-Based Routing is a call management feature that controls how calls are routed by Lync Server 2013 CU1.</span></span> <span data-ttu-id="4527f-108">Il applique des restrictions sur la façon dont les appels peuvent être routés vers des destinations PBX ou PSTN en fonction de l’emplacement de l’appelant Lync.</span><span class="sxs-lookup"><span data-stu-id="4527f-108">It enforces restrictions on whether calls can be routed to PBX or PSTN destinations based on the Lync caller’s location.</span></span> <span data-ttu-id="4527f-109">Location-Based le routage applique des règles d’autorisation d’appel aux appels RTC en fonction de l’emplacement réseau de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="4527f-109">Location-Based Routing applies call authorization rules to PSTN calls based on the caller’s network location.</span></span> <span data-ttu-id="4527f-110">L’emplacement de l’appelant est déterminé en fonction du site réseau associé au sous-réseau sur lequel est connecté l’appelant.</span><span class="sxs-lookup"><span data-stu-id="4527f-110">The caller’s location is determined based on the network site associated with the network subnet the caller is connected on.</span></span> <span data-ttu-id="4527f-111">La configuration du routage Location-Based nécessite d’abord le déploiement de voix entreprise et la configuration des régions, sites et sous-réseaux réseau.</span><span class="sxs-lookup"><span data-stu-id="4527f-111">Configuring Location-Based Routing requires first deploying Enterprise Voice, then configuring network regions, sites and subnets.</span></span> <span data-ttu-id="4527f-112">Cela permet de configurer la base pour l’activation du routage Location-Based.</span><span class="sxs-lookup"><span data-stu-id="4527f-112">This sets up the foundation for enabling Location-Based Routing.</span></span>

<span data-ttu-id="4527f-113">Avant de déployer Location-Based le routage, vous devez d’abord déployer Enterprise Voice et configurer des régions, des sites et des sous-réseaux réseau associés sur les sites de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="4527f-113">Before deploying Location-Based Routing, you must first deploy Enterprise Voice, and configure network regions, sites, and associate network subnets to your network sites.</span></span> <span data-ttu-id="4527f-114">Lorsque vous avez terminé, vous pouvez configurer le routage de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="4527f-114">Once completed, you can configure Location-Based Routing.</span></span> <span data-ttu-id="4527f-115">Pour plus d’informations sur la façon de configurer des zones, des sites et des sous-réseaux, voir [déploiement de fonctionnalités avancées d’entreprise voix dans Lync Server 2013](lync-server-2013-deploying-advanced-enterprise-voice-features.md)</span><span class="sxs-lookup"><span data-stu-id="4527f-115">For steps on how to configure network regions, sites and subnets, see [Deploying advanced Enterprise Voice features in Lync Server 2013](lync-server-2013-deploying-advanced-enterprise-voice-features.md)</span></span>

<span data-ttu-id="4527f-116">Cette section vous guide dans la configuration du routage de Location-Based à l’aide de l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="4527f-116">This section guides you through the configuration of Location-Based Routing using the following example as illustration.</span></span>

<span data-ttu-id="4527f-117">![Exemple de routage en fonction de l’emplacement voix entreprise](images/JJ994036.b6ef5afc-36ac-406f-8ec2-a87532b20612(OCS.15).png "Exemple de routage en fonction de l’emplacement voix entreprise")</span><span class="sxs-lookup"><span data-stu-id="4527f-117">![Enterprise Voice location-based routing example](images/JJ994036.b6ef5afc-36ac-406f-8ec2-a87532b20612(OCS.15).png "Enterprise Voice location-based routing example")</span></span>

  
<span data-ttu-id="4527f-118">Le tableau suivant représente les utilisateurs définis dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="4527f-118">The following table represents the users defined in this example.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4527f-119">Type de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="4527f-119">Endpoint type</span></span></th>
<th><span data-ttu-id="4527f-120">Lieu</span><span class="sxs-lookup"><span data-stu-id="4527f-120">Location</span></span></th>
<th><span data-ttu-id="4527f-121">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4527f-121">Users</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4527f-122">Lync</span><span class="sxs-lookup"><span data-stu-id="4527f-122">Lync</span></span></p></td>
<td><p><span data-ttu-id="4527f-123">Delhi entreprise entreprise</span><span class="sxs-lookup"><span data-stu-id="4527f-123">Delhi corporate office</span></span></p></td>
<td><p><span data-ttu-id="4527f-124">DEL-LYNC-1, DEL-LYNC-2, DEL-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="4527f-124">DEL-LYNC-1,DEL-LYNC-2,DEL-LYNC-3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4527f-125">Lync</span><span class="sxs-lookup"><span data-stu-id="4527f-125">Lync</span></span></p></td>
<td><p><span data-ttu-id="4527f-126">Bureau d’entreprise Hyderabad</span><span class="sxs-lookup"><span data-stu-id="4527f-126">Hyderabad corporate office</span></span></p></td>
<td><p><span data-ttu-id="4527f-127">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="4527f-127">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4527f-128">Lync</span><span class="sxs-lookup"><span data-stu-id="4527f-128">Lync</span></span></p></td>
<td><p><span data-ttu-id="4527f-129">Inconnu (c.-à-d. hôtel)</span><span class="sxs-lookup"><span data-stu-id="4527f-129">Unknown (i.e. hotel)</span></span></p></td>
<td><p><span data-ttu-id="4527f-130">UNK-LYNC-1</span><span class="sxs-lookup"><span data-stu-id="4527f-130">UNK-LYNC-1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4527f-131">Private</span><span class="sxs-lookup"><span data-stu-id="4527f-131">PBX</span></span></p></td>
<td><p><span data-ttu-id="4527f-132">Delhi entreprise entreprise</span><span class="sxs-lookup"><span data-stu-id="4527f-132">Delhi corporate office</span></span></p></td>
<td><p><span data-ttu-id="4527f-133">DEL-PBX-1, DEL-PBX-2</span><span class="sxs-lookup"><span data-stu-id="4527f-133">DEL-PBX-1, DEL-PBX-2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4527f-134">Private</span><span class="sxs-lookup"><span data-stu-id="4527f-134">PBX</span></span></p></td>
<td><p><span data-ttu-id="4527f-135">Bureau d’entreprise Hyderabad</span><span class="sxs-lookup"><span data-stu-id="4527f-135">Hyderabad corporate office</span></span></p></td>
<td><p><span data-ttu-id="4527f-136">HYD-PBX-1, HYD-PBX-2</span><span class="sxs-lookup"><span data-stu-id="4527f-136">HYD-PBX-1, HYD-PBX-2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4527f-137">PSTN</span><span class="sxs-lookup"><span data-stu-id="4527f-137">PSTN</span></span></p></td>
<td><p><span data-ttu-id="4527f-138">Encore</span><span class="sxs-lookup"><span data-stu-id="4527f-138">Unknown</span></span></p></td>
<td><p><span data-ttu-id="4527f-139">RTC-1, RTC-2, RTC-3</span><span class="sxs-lookup"><span data-stu-id="4527f-139">PSTN-1, PSTN-2, PSTN-3</span></span></p></td>
</tr>
</tbody>
</table>

  

<span data-ttu-id="4527f-140">Le tableau suivant représente les systèmes illustrés dans cet exemple d’environnement.</span><span class="sxs-lookup"><span data-stu-id="4527f-140">The following table represents the systems illustrated in this example environment.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4527f-141">SYSTEME</span><span class="sxs-lookup"><span data-stu-id="4527f-141">System</span></span></th>
<th><span data-ttu-id="4527f-142">Lieu</span><span class="sxs-lookup"><span data-stu-id="4527f-142">Location</span></span></th>
<th><span data-ttu-id="4527f-143">Nom</span><span class="sxs-lookup"><span data-stu-id="4527f-143">Name</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4527f-144">Lync Server 2013 CU1 pool</span><span class="sxs-lookup"><span data-stu-id="4527f-144">Lync Server 2013 CU1 pool</span></span></p></td>
<td><p><span data-ttu-id="4527f-145">indifférente</span><span class="sxs-lookup"><span data-stu-id="4527f-145">any</span></span></p></td>
<td><p><span data-ttu-id="4527f-146">LS-PL1</span><span class="sxs-lookup"><span data-stu-id="4527f-146">LS-PL1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4527f-147">Lync Server 2013 CU1, médiation Server</span><span class="sxs-lookup"><span data-stu-id="4527f-147">Lync Server 2013 CU1, Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="4527f-148">indifférente</span><span class="sxs-lookup"><span data-stu-id="4527f-148">any</span></span></p></td>
<td><p><span data-ttu-id="4527f-149">MS-PL1</span><span class="sxs-lookup"><span data-stu-id="4527f-149">MS-PL1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4527f-150">Passerelle RTC 1</span><span class="sxs-lookup"><span data-stu-id="4527f-150">PSTN gateway 1</span></span></p></td>
<td><p><span data-ttu-id="4527f-151">Delhi</span><span class="sxs-lookup"><span data-stu-id="4527f-151">Delhi</span></span></p></td>
<td><p><span data-ttu-id="4527f-152">DEL-GW</span><span class="sxs-lookup"><span data-stu-id="4527f-152">DEL-GW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4527f-153">Passerelle RTC 2</span><span class="sxs-lookup"><span data-stu-id="4527f-153">PSTN gateway 2</span></span></p></td>
<td><p><span data-ttu-id="4527f-154">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="4527f-154">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="4527f-155">HYD-GW</span><span class="sxs-lookup"><span data-stu-id="4527f-155">HYD-GW</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4527f-156">PBX 1</span><span class="sxs-lookup"><span data-stu-id="4527f-156">PBX 1</span></span></p></td>
<td><p><span data-ttu-id="4527f-157">Delhi</span><span class="sxs-lookup"><span data-stu-id="4527f-157">Delhi</span></span></p></td>
<td><p><span data-ttu-id="4527f-158">DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="4527f-158">DEL-PBX</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4527f-159">PBX 2</span><span class="sxs-lookup"><span data-stu-id="4527f-159">PBX 2</span></span></p></td>
<td><p><span data-ttu-id="4527f-160">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="4527f-160">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="4527f-161">PBX ROUGE</span><span class="sxs-lookup"><span data-stu-id="4527f-161">RED-PBX</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="in-this-section"></a><span data-ttu-id="4527f-162">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="4527f-162">In This Section</span></span>

  - [<span data-ttu-id="4527f-163">Configuration d’Enterprise Voice dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4527f-163">Configuring Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-configuring-enterprise-voice.md)

  - [<span data-ttu-id="4527f-164">Déploiement de zones, sites et sous-réseaux réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4527f-164">Deploying network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-deploying-network-regions-sites-and-subnets.md)

  - [<span data-ttu-id="4527f-165">Activation du routage Location-Based dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4527f-165">Enabling Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-enabling-location-based-routing.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4527f-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4527f-166">See Also</span></span>


[<span data-ttu-id="4527f-167">Déploiement de fonctionnalités avancées d’entreprise voix dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4527f-167">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)  
  

<span data-ttu-id="4527f-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4527f-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

