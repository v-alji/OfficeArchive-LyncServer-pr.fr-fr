---
title: >
  Lync Server 2013 : Processus de déploiement du routage géodépendant
description: "Lync Server 2013 : processus de déploiement d' Location-Based routage."
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for Location-Based Routing
ms:assetid: 9e923e72-83fc-4a4f-8937-28a55739ed3e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994055(v=OCS.15)
ms:contentKeyID: 51803966
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2c321d9b0eada6e9501b2ded69120feae36be171
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394905"
---
# <a name="deployment-process-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="4cdff-103">Processus de déploiement du routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4cdff-103">Deployment process for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4cdff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4cdff-104">

<span> </span></span></span>

<span data-ttu-id="4cdff-105">_**Dernière modification de la rubrique :** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="4cdff-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="4cdff-106">Cette rubrique fournit une vue d’ensemble du processus de configuration du routage Location-Based.</span><span class="sxs-lookup"><span data-stu-id="4cdff-106">This topic provides an overview of the process involved in configuring Location-Based Routing.</span></span> <span data-ttu-id="4cdff-107">Vous devez déployer Lync Server Enterprise Edition ou Standard Edition avec Enterprise Voice avant de configurer Location-Based routage.</span><span class="sxs-lookup"><span data-stu-id="4cdff-107">You must deploy Lync Server Enterprise Edition or Standard Edition with Enterprise Voice before you configure Location-Based Routing.</span></span> <span data-ttu-id="4cdff-108">Les composants requis par le routage Location-Based sont déjà installés et activés lors du déploiement d’Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="4cdff-108">The components required by Location-Based Routing are already installed and enabled when you deploy Enterprise Voice.</span></span>

### <a name="location-based-routing-deployment-process"></a><span data-ttu-id="4cdff-109">Processus de déploiement de routage de Location-Based</span><span class="sxs-lookup"><span data-stu-id="4cdff-109">Location-Based Routing Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4cdff-110">Phase</span><span class="sxs-lookup"><span data-stu-id="4cdff-110">Phase</span></span></th>
<th><span data-ttu-id="4cdff-111">Étapes</span><span class="sxs-lookup"><span data-stu-id="4cdff-111">Steps</span></span></th>
<th><span data-ttu-id="4cdff-112">Groupes et rôles requis</span><span class="sxs-lookup"><span data-stu-id="4cdff-112">Required groups and roles</span></span></th>
<th><span data-ttu-id="4cdff-113">Documentation de déploiement</span><span class="sxs-lookup"><span data-stu-id="4cdff-113">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cdff-114">Déploiement de Voix Entreprise</span><span class="sxs-lookup"><span data-stu-id="4cdff-114">Deploy Enterprise Voice</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="4cdff-115">Configurer des Trunks</span><span class="sxs-lookup"><span data-stu-id="4cdff-115">Configure Trunks</span></span></p></li>
<li><p><span data-ttu-id="4cdff-116">Créer des stratégies vocales</span><span class="sxs-lookup"><span data-stu-id="4cdff-116">Create Voice Policies</span></span></p></li>
<li><p><span data-ttu-id="4cdff-117">Définir des itinéraires vocaux</span><span class="sxs-lookup"><span data-stu-id="4cdff-117">Define Voice Routes</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="4cdff-118">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="4cdff-118">CSVoiceAdmins</span></span><br />
<span data-ttu-id="4cdff-119">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="4cdff-119">CsAdministrator</span></span><br />
<span data-ttu-id="4cdff-120">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="4cdff-120">CsServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="4cdff-121">Déploiement d’Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="4cdff-121">Deploying Enterprise Voice</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cdff-122">Vérifier votre déploiement voix entreprise</span><span class="sxs-lookup"><span data-stu-id="4cdff-122">Verify your Enterprise Voice deployment</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4cdff-123">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="4cdff-123">CSVoiceAdmins</span></span><br />
<span data-ttu-id="4cdff-124">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="4cdff-124">CsAdministrator</span></span><br />
<span data-ttu-id="4cdff-125">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="4cdff-125">CsServerAdministrator</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cdff-126">Configurer des zones, des sites et des sous-réseaux réseau</span><span class="sxs-lookup"><span data-stu-id="4cdff-126">Configure network regions, sites, and subnets</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="4cdff-127">Créer des régions réseau</span><span class="sxs-lookup"><span data-stu-id="4cdff-127">Create network regions</span></span></p></li>
<li><p><span data-ttu-id="4cdff-128">Créer des sites réseau</span><span class="sxs-lookup"><span data-stu-id="4cdff-128">Create network sites</span></span></p></li>
<li><p><span data-ttu-id="4cdff-129">Associe des sous-réseaux aux sites réseau</span><span class="sxs-lookup"><span data-stu-id="4cdff-129">Associates subnets with network sites</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="4cdff-130">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="4cdff-130">CSVoiceAdmins</span></span><br />
<span data-ttu-id="4cdff-131">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="4cdff-131">CsAdministrator</span></span><br />
<span data-ttu-id="4cdff-132">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="4cdff-132">CsServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="4cdff-133">À propos des zones, des sites et des sous-réseaux réseau</span><span class="sxs-lookup"><span data-stu-id="4cdff-133">About Network Regions, Sites, and Subnets</span></span><br />
<span data-ttu-id="4cdff-134">Créer ou modifier une région de réseau</span><span class="sxs-lookup"><span data-stu-id="4cdff-134">Create or Modify a Network Region</span></span><br />
<span data-ttu-id="4cdff-135">Créer ou modifier un site réseau</span><span class="sxs-lookup"><span data-stu-id="4cdff-135">Create or Modify a Network Site</span></span><br />
<span data-ttu-id="4cdff-136">Associer un sous-réseau à un site réseau</span><span class="sxs-lookup"><span data-stu-id="4cdff-136">Associate a Subnet with a Network Site</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cdff-137">Configurer le routage de Location-Based</span><span class="sxs-lookup"><span data-stu-id="4cdff-137">Configure Location-Based Routing</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="4cdff-138">Créer des stratégies de routage de la voix</span><span class="sxs-lookup"><span data-stu-id="4cdff-138">Create voice routing policies</span></span></p></li>
<li><p><span data-ttu-id="4cdff-139">Définir une configuration de Trunk séparée par Trunk</span><span class="sxs-lookup"><span data-stu-id="4cdff-139">Define separate trunk configuration per trunk</span></span></p></li>
<li><p><span data-ttu-id="4cdff-140">Modifier les stratégies vocales</span><span class="sxs-lookup"><span data-stu-id="4cdff-140">Modify voice policies</span></span></p></li>
<li><p><span data-ttu-id="4cdff-141">Activer Location-Based configuration de routage</span><span class="sxs-lookup"><span data-stu-id="4cdff-141">Enable Location-Based Routing configuration</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="4cdff-142">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="4cdff-142">CSVoiceAdmins</span></span><br />
<span data-ttu-id="4cdff-143">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="4cdff-143">CsAdministrator</span></span><br />
<span data-ttu-id="4cdff-144">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="4cdff-144">CsServerAdministrator</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>

## <a name="sample-deployment"></a><span data-ttu-id="4cdff-145">Exemple de déploiement</span><span class="sxs-lookup"><span data-stu-id="4cdff-145">Sample Deployment</span></span>

<span data-ttu-id="4cdff-146">Le déploiement suivant est utilisé pour illustrer davantage les mécanismes activés par Location-Based routage.</span><span class="sxs-lookup"><span data-stu-id="4cdff-146">The following deployment is used to illustrate further the mechanisms enabled by Location-Based Routing.</span></span>

<span data-ttu-id="4cdff-147">![e1bd2230-44DA-4784-b359-24572b6ce02d](images/JJ994055.e1bd2230-44da-4784-b359-24572b6ce02d(OCS.15).png "e1bd2230-44DA-4784-b359-24572b6ce02d")</span><span class="sxs-lookup"><span data-stu-id="4cdff-147">![e1bd2230-44da-4784-b359-24572b6ce02d](images/JJ994055.e1bd2230-44da-4784-b359-24572b6ce02d(OCS.15).png "e1bd2230-44da-4784-b359-24572b6ce02d")</span></span>

<div>

## <a name="incoming-pstn-calls"></a><span data-ttu-id="4cdff-148">Appels RTC entrants</span><span class="sxs-lookup"><span data-stu-id="4cdff-148">Incoming PSTN calls</span></span>

<span data-ttu-id="4cdff-149">Un administrateur peut activer le Trunk défini pour acheminer les appels vers « passerelle site 1 » pour le routage de Location-Based et associer la « passerelle site 1 » au site 1.</span><span class="sxs-lookup"><span data-stu-id="4cdff-149">An administrator can enable the trunk defined to route calls to “Site 1 Gateway” for Location-Based Routing and associate the “Site 1 Gateway” to site 1.</span></span> <span data-ttu-id="4cdff-150">Lorsque l’option est activée, les appels routés par le biais de la passerelle « site 1 » ne seront routés qu’aux utilisateurs situés dans le site 1.</span><span class="sxs-lookup"><span data-stu-id="4cdff-150">Once enabled, calls that are routed through “Site 1 Gateway“ will only be routed to users that are located in site 1.</span></span> <span data-ttu-id="4cdff-151">Tous les appels routés via le Trunk « site 1 passerelle » destinés aux utilisateurs d’un site différent, comme le site 2, seront bloqués pour empêcher les détournements d’appels RTC.</span><span class="sxs-lookup"><span data-stu-id="4cdff-151">All calls routed through the “Site 1 Gateway” trunk destined to users in a different site, such as site 2 will be blocked to prevent PSTN toll bypass.</span></span>

<span data-ttu-id="4cdff-152">Tous les appels RTC entrants par le biais de la « passerelle du site 1 » ne seront autorisés à effectuer le routage qu’aux points de terminaison situés dans le site 1.</span><span class="sxs-lookup"><span data-stu-id="4cdff-152">All incoming PSTN calls through “Site 1 Gateway” will only be allowed to route to endpoints located in site 1.</span></span> <span data-ttu-id="4cdff-153">Par exemple, lorsque « Lync User 1 » voyage sur le site 2, tous les appels RTC entrants par le biais de « passerelle site 1 » ne seront pas routés aux points de terminaison « Lync User 1 » situés dans le site 2.</span><span class="sxs-lookup"><span data-stu-id="4cdff-153">For example, when “Lync user 1” travels to site 2, all incoming PSTN calls through “Site 1 Gateway” will not be routed to “Lync user 1” endpoints located in site 2.</span></span> <span data-ttu-id="4cdff-154">La même règle de routage s’applique si « Lync User 1 » voyage sur un site réseau inconnu où l’emplacement de l’utilisateur ne peut pas être déterminé.</span><span class="sxs-lookup"><span data-stu-id="4cdff-154">The same routing rule applies if “Lync user 1” travels to an unknown network site where the user’s location can’t be determined.</span></span>

<span data-ttu-id="4cdff-155">Le tableau suivant décrit l’environnement utilisateur de « Lync User 1 » dans ce contexte.</span><span class="sxs-lookup"><span data-stu-id="4cdff-155">The following table outlines the user experience of “Lync user 1” in this context.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="4cdff-156">Points de terminaison Lync User 1 situés dans le site réseau 1</span><span class="sxs-lookup"><span data-stu-id="4cdff-156">Lync user 1 endpoints located in network site 1</span></span></th>
<th><span data-ttu-id="4cdff-157">Points de terminaison Lync User 1 situés dans le site réseau 2</span><span class="sxs-lookup"><span data-stu-id="4cdff-157">Lync user 1 endpoints located in network site 2</span></span></th>
<th><span data-ttu-id="4cdff-158">Points de terminaison Lync User 1 situés dans un site réseau inconnu</span><span class="sxs-lookup"><span data-stu-id="4cdff-158">Lync user 1 endpoints located in unknown network site</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cdff-159">Appels RTC entrants vers l’utilisateur Lync 1</span><span class="sxs-lookup"><span data-stu-id="4cdff-159">Inbound PSTN calls to Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="4cdff-160">Les appels sont routés vers les points de terminaison dans cet emplacement</span><span class="sxs-lookup"><span data-stu-id="4cdff-160">Calls are routed to endpoints in this location</span></span></p></td>
<td><p><span data-ttu-id="4cdff-161">Les appels ne sont pas routés aux points de terminaison dans cet emplacement</span><span class="sxs-lookup"><span data-stu-id="4cdff-161">Calls are not routed to endpoints in this location</span></span></p></td>
<td><p><span data-ttu-id="4cdff-162">Les appels ne sont pas routés aux points de terminaison dans cet emplacement</span><span class="sxs-lookup"><span data-stu-id="4cdff-162">Calls are not routed to endpoints in this location</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="outgoing-pstn-calls"></a><span data-ttu-id="4cdff-163">Appels RTC sortants</span><span class="sxs-lookup"><span data-stu-id="4cdff-163">Outgoing PSTN calls</span></span>

<span data-ttu-id="4cdff-164">Les itinéraires vocaux sont référencés dans les stratégies vocales attribuées directement aux utilisateurs et les stratégies de routage vocal affectées aux sites réseau.</span><span class="sxs-lookup"><span data-stu-id="4cdff-164">Voice routes are referenced in both Voice Policies assigned directly to users, and Voice Routing Policies assigned to network sites.</span></span> <span data-ttu-id="4cdff-165">Les deux stratégies contiennent des références à des itinéraires qui peuvent être utilisées pour acheminer un appel différemment.</span><span class="sxs-lookup"><span data-stu-id="4cdff-165">Both policies contain references to routes, which can be used to route a call differently.</span></span> <span data-ttu-id="4cdff-166">Par exemple, un administrateur peut définir une stratégie de routage vocale pour tous les utilisateurs situés dans le site réseau 1 pour acheminer tous les appels sortants par le biais de la « passerelle site 1 », tandis que la stratégie vocale de certains utilisateurs définit un itinéraire pour tous les appels sortants par le biais de la « passerelle site 2 ».</span><span class="sxs-lookup"><span data-stu-id="4cdff-166">For example, an administrator can define a Voice Routing Policy for all users located in network site 1 to route all outbound calls through the “Site 1 Gateway” while the Voice Policy of some users define a route for all outbound calls through the “Site 2 Gateway”.</span></span> <span data-ttu-id="4cdff-167">Même si ces utilisateurs se trouvent dans le site réseau 1, les appels sortants sont routés par le biais de la « passerelle du site 1 ».</span><span class="sxs-lookup"><span data-stu-id="4cdff-167">While these users are located in network site 1, their outbound calls will be routed through the “Site 1 Gateway”.</span></span>

<span data-ttu-id="4cdff-168">Lorsqu’un utilisateur se trouve sur un site réseau configuré pour le routage Location-Based, l’itinéraire de la stratégie de routage de la voix du site réseau remplace l’itinéraire de la stratégie vocale de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4cdff-168">When a user is located in a network site configured for Location-Based Routing, the network site’s Voice Routing Policy route overrides the user’s Voice Policy route.</span></span> <span data-ttu-id="4cdff-169">Cette règle est particulièrement utile pour les utilisateurs qui se déplacent temporairement sur un autre site.</span><span class="sxs-lookup"><span data-stu-id="4cdff-169">This rule is particularly useful for users that temporarily move to a different site.</span></span> <span data-ttu-id="4cdff-170">Dans ce cas particulier, un utilisateur utilisera toujours une passerelle locale vers son emplacement. Si "Lync User 3" est situé sur "site 2", tous les appels sortants seront routés par le biais de la « passerelle site 2 », mais s’il est acheminé vers le site 1, tous les appels sortants placés alors qu’il se trouve sur le site 1 seront routés par le biais de « passerelle site 1 ».</span><span class="sxs-lookup"><span data-stu-id="4cdff-170">In this particular case a user will always use a gateway that is local to his location; if “Lync user 3” is located at “Site 2”, all his outbound calls will be routed via “Site 2 Gateway”, but if he travels to site 1, all his outbound calls placed while he’s at site 1 will be routed through “Site 1 Gateway”.</span></span>

<span data-ttu-id="4cdff-171">Le tableau suivant illustre l’utilisation de l’utilisateur Lync 1 lors du placement d’un appel sortant sur les sites réseau suivants.</span><span class="sxs-lookup"><span data-stu-id="4cdff-171">The following table illustrates the user experience of Lync user 1 placing an outbound call from the following network sites.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="4cdff-172">Site réseau 1</span><span class="sxs-lookup"><span data-stu-id="4cdff-172">Network site 1</span></span></th>
<th><span data-ttu-id="4cdff-173">Site réseau 2</span><span class="sxs-lookup"><span data-stu-id="4cdff-173">Network site 2</span></span></th>
<th><span data-ttu-id="4cdff-174">Site réseau inconnu ou non activé pour le routage Location-Based</span><span class="sxs-lookup"><span data-stu-id="4cdff-174">Unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cdff-175">Autorisation des appels sortants</span><span class="sxs-lookup"><span data-stu-id="4cdff-175">Authorization of outbound calls</span></span></p></td>
<td><p><span data-ttu-id="4cdff-176">Politique vocale utilisateur Lync 1</span><span class="sxs-lookup"><span data-stu-id="4cdff-176">Lync user 1 voice policy</span></span></p></td>
<td><p><span data-ttu-id="4cdff-177">Politique vocale utilisateur Lync 1</span><span class="sxs-lookup"><span data-stu-id="4cdff-177">Lync user 1 voice policy</span></span></p></td>
<td><p><span data-ttu-id="4cdff-178">Politique vocale utilisateur Lync 1</span><span class="sxs-lookup"><span data-stu-id="4cdff-178">Lync user 1 voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cdff-179">Routage des appels sortants</span><span class="sxs-lookup"><span data-stu-id="4cdff-179">Routing of outbound calls</span></span></p></td>
<td><p><span data-ttu-id="4cdff-180">Site 1 politique de routage de la voix</span><span class="sxs-lookup"><span data-stu-id="4cdff-180">Site 1 voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="4cdff-181">Politique de routage téléphonique de site 2</span><span class="sxs-lookup"><span data-stu-id="4cdff-181">Site 2 voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="4cdff-182">Politique vocale de l’utilisateur et uniquement aux systèmes non activés pour le routage Location-Based</span><span class="sxs-lookup"><span data-stu-id="4cdff-182">User’s voice policy and only to systems not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="call-transfers-and-forwards"></a><span data-ttu-id="4cdff-183">Transférer et transférer des appels</span><span class="sxs-lookup"><span data-stu-id="4cdff-183">Call transfers and forwards</span></span>

<span data-ttu-id="4cdff-184">Lorsque les appels sont transférés ou transférés, le routage des appels est affecté par Location-Based routage.</span><span class="sxs-lookup"><span data-stu-id="4cdff-184">When calls are transferred or forwarded, the routing of calls is affected by Location-Based Routing.</span></span>

<span data-ttu-id="4cdff-185">Le tableau suivant décrit l’utilisateur Lync 1 qui transfère ou transfère un appel PSTN vers un autre utilisateur Lync.</span><span class="sxs-lookup"><span data-stu-id="4cdff-185">The following table depicts Lync user 1 transferring or forwarding a PSTN call to another Lync user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4cdff-186">Utilisateur déclenchant ou transférant un appel</span><span class="sxs-lookup"><span data-stu-id="4cdff-186">User initiating call transfer or forward</span></span></th>
<th><span data-ttu-id="4cdff-187">Utilisateur Lync 2</span><span class="sxs-lookup"><span data-stu-id="4cdff-187">Lync user 2</span></span></th>
<th><span data-ttu-id="4cdff-188">Utilisateur Lync 4</span><span class="sxs-lookup"><span data-stu-id="4cdff-188">Lync user 4</span></span></th>
<th><span data-ttu-id="4cdff-189">Utilisateur Lync dans le site réseau non activé pour le routage de Location-Based</span><span class="sxs-lookup"><span data-stu-id="4cdff-189">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cdff-190">Utilisateur Lync 1</span><span class="sxs-lookup"><span data-stu-id="4cdff-190">Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="4cdff-191">Le transfert ou renvoi de l’appel est autorisé</span><span class="sxs-lookup"><span data-stu-id="4cdff-191">Call forward or transfer is allowed</span></span></p></td>
<td><p><span data-ttu-id="4cdff-192">Le transfert ou renvoi de l’appel n’est pas autorisé</span><span class="sxs-lookup"><span data-stu-id="4cdff-192">Call forward or transfer is not allowed</span></span></p></td>
<td><p><span data-ttu-id="4cdff-193">Le transfert ou renvoi de l’appel n’est pas autorisé</span><span class="sxs-lookup"><span data-stu-id="4cdff-193">Call forward or transfer is not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="4cdff-194">Le tableau suivant illustre la façon dont Location-Based le routage affecte le mode de routage de l’appel en fonction de l’emplacement de transfert de l’utilisateur Lync (utilisateur Lync 2, utilisateur Lync 4, etc.) vers un point de terminaison RTC.</span><span class="sxs-lookup"><span data-stu-id="4cdff-194">The following table illustrates how Location-Based Routing affects how the call is routed based on the location of the Lync user being transferred (Lync user 2, Lync user 4, etc) to a PSTN endpoint</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4cdff-195">Point de terminaison pour lequel l’appel est transféré ou renvoyé vers</span><span class="sxs-lookup"><span data-stu-id="4cdff-195">Endpoint where call is transferred or forwarded to</span></span></th>
<th><span data-ttu-id="4cdff-196">Utilisateur Lync 2</span><span class="sxs-lookup"><span data-stu-id="4cdff-196">Lync user 2</span></span></th>
<th><span data-ttu-id="4cdff-197">Utilisateur Lync 4</span><span class="sxs-lookup"><span data-stu-id="4cdff-197">Lync user 4</span></span></th>
<th><span data-ttu-id="4cdff-198">Utilisateur Lync dans le site réseau non activé pour le routage de Location-Based</span><span class="sxs-lookup"><span data-stu-id="4cdff-198">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cdff-199">Point de terminaison PSTN</span><span class="sxs-lookup"><span data-stu-id="4cdff-199">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="4cdff-200">Le transfert d’appel est acheminé par le biais du site 1 politique de routage de la voix et sortie via la passerelle site 1</span><span class="sxs-lookup"><span data-stu-id="4cdff-200">Call forward or transfer is routed through site 1 voice routing policy and egress via Site 1 Gateway</span></span></p></td>
<td><p><span data-ttu-id="4cdff-201">Le transfert d’appel ou le transfert est acheminé via la stratégie de routage de la voix site 2 et la sortie via la passerelle site 2</span><span class="sxs-lookup"><span data-stu-id="4cdff-201">Call forward or transfer is routed through site 2 voice routing policy and egress via Site 2 Gateway</span></span></p></td>
<td><p><span data-ttu-id="4cdff-202">Le transfert d’appel est routé par le biais de la stratégie vocale et de la sortie de l’utilisateur Lync via une passerelle non activée pour le routage sur site (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="4cdff-202">Call forward or transfer is routed through the Lync user voice policy and egress via a gateway not enabled for location-based routing (if available)</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="simultaneous-ringing"></a><span data-ttu-id="4cdff-203">Sonnerie simultanée</span><span class="sxs-lookup"><span data-stu-id="4cdff-203">Simultaneous ringing</span></span>

<span data-ttu-id="4cdff-204">Lorsque le routage par emplacement est configuré dans l’exemple de topologie, les interactions suivantes sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="4cdff-204">Once location-based routing is configured in the sample topology, the following interactions are enforced.</span></span>

<span data-ttu-id="4cdff-205">Le tableau suivant indique si Location-Based de routage autorise une sonnerie simultanée pour différents utilisateurs de Lync (par exemple, utilisateur Lync 2, utilisateur Lync 4, etc.).</span><span class="sxs-lookup"><span data-stu-id="4cdff-205">The following table illustrates whether Location-Based Routing allows simultaneous ringing for different Lync users (i.e. Lync user 2, Lync user 4, etc).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4cdff-206">Destination de l’appel RTC entrant</span><span class="sxs-lookup"><span data-stu-id="4cdff-206">Incoming PSTN call target</span></span></th>
<th><span data-ttu-id="4cdff-207">Utilisateur Lync 2</span><span class="sxs-lookup"><span data-stu-id="4cdff-207">Lync user 2</span></span></th>
<th><span data-ttu-id="4cdff-208">Utilisateur Lync 4</span><span class="sxs-lookup"><span data-stu-id="4cdff-208">Lync user 4</span></span></th>
<th><span data-ttu-id="4cdff-209">Utilisateur Lync dans le site réseau non activé pour le routage de Location-Based</span><span class="sxs-lookup"><span data-stu-id="4cdff-209">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cdff-210">Utilisateur Lync 1</span><span class="sxs-lookup"><span data-stu-id="4cdff-210">Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="4cdff-211">Sonnerie simultanée autorisée</span><span class="sxs-lookup"><span data-stu-id="4cdff-211">Simultaneous ring is allowed</span></span></p></td>
<td><p><span data-ttu-id="4cdff-212">Sonnerie simultanée interdite</span><span class="sxs-lookup"><span data-stu-id="4cdff-212">Simultaneous ring is not allowed</span></span></p></td>
<td><p><span data-ttu-id="4cdff-213">Sonnerie simultanée interdite</span><span class="sxs-lookup"><span data-stu-id="4cdff-213">Simultaneous ring is not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="4cdff-214">Le tableau suivant indique si Location-Based de routage autorise la sonnerie simultanée d’un point de terminaison RTC provenant de différents utilisateurs de Lync (c’est-à-dire, utilisateur Lync 2, utilisateur Lync 4, etc.).</span><span class="sxs-lookup"><span data-stu-id="4cdff-214">The following table illustrates whether Location-Based Routing allows simultaneous ringing to a PSTN endpoint from different Lync users (i.e. Lync user 2, Lync user 4, etc).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4cdff-215">Cible de la sonnerie simultanée</span><span class="sxs-lookup"><span data-stu-id="4cdff-215">Simultaneous ring target</span></span></th>
<th><span data-ttu-id="4cdff-216">Utilisateur Lync 2</span><span class="sxs-lookup"><span data-stu-id="4cdff-216">Lync user 2</span></span></th>
<th><span data-ttu-id="4cdff-217">Utilisateur Lync 4</span><span class="sxs-lookup"><span data-stu-id="4cdff-217">Lync user 4</span></span></th>
<th><span data-ttu-id="4cdff-218">Utilisateur Lync dans le site réseau non activé pour le routage de Location-Based</span><span class="sxs-lookup"><span data-stu-id="4cdff-218">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cdff-219">Utilisateur Lync 1 téléphone mobile (point de terminaison PSTN)</span><span class="sxs-lookup"><span data-stu-id="4cdff-219">Lync user 1 mobile phone (PSTN endpoint)</span></span></p></td>
<td><p><span data-ttu-id="4cdff-220">Appels routés par le biais de la stratégie de routage vocale du site réseau 1 et de la sortie via le site 1 passerelle</span><span class="sxs-lookup"><span data-stu-id="4cdff-220">Call routed through network site 1’s voice routing policy and egress via site 1 gateway</span></span></p></td>
<td><p><span data-ttu-id="4cdff-221">Appels routés par le biais de la stratégie de routage de la voix du site Network 2 et de la sortie via la passerelle site 2</span><span class="sxs-lookup"><span data-stu-id="4cdff-221">Call routed through network site 2’s voice routing policy and egress via site 2 gateway</span></span></p></td>
<td><p><span data-ttu-id="4cdff-222">Appels routés par le biais de la stratégie vocale de l’appelant et sortie via une passerelle RTC non activée pour le routage Location-Based</span><span class="sxs-lookup"><span data-stu-id="4cdff-222">Call routed through the caller voice policy and will egress via a PSTN gateway not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4cdff-223">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cdff-223">See Also</span></span>


[<span data-ttu-id="4cdff-224">Planification du routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4cdff-224">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="4cdff-225"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4cdff-225"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

