---
title: 'Lync Server 2013 : configuration d’Enterprise Voice'
description: 'Lync Server 2013 : configuration d’Enterprise Voice.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Enterprise Voice
ms:assetid: 7df179fa-d3a2-4b23-a433-b750aedf980b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994041(v=OCS.15)
ms:contentKeyID: 51803952
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 49a231b92bf7b04aa3466927a79258f0cbad4e3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433121"
---
# <a name="configuring-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="314e0-103">Configuration d’Enterprise Voice dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="314e0-103">Configuring Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="314e0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="314e0-104">

<span> </span></span></span>

<span data-ttu-id="314e0-105">_**Dernière modification de la rubrique :** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="314e0-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="314e0-106">Pour déployer Enterprise Voice, vous devez configurer les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="314e0-106">To deploy Enterprise Voice, you’ll need to configure the following:</span></span>

  - <span data-ttu-id="314e0-107">Créer un Trunk</span><span class="sxs-lookup"><span data-stu-id="314e0-107">Create a Trunk</span></span>

  - <span data-ttu-id="314e0-108">Définir une politique vocale</span><span class="sxs-lookup"><span data-stu-id="314e0-108">Define a Voice Policy</span></span>

  - <span data-ttu-id="314e0-109">Définir une gamme vocale</span><span class="sxs-lookup"><span data-stu-id="314e0-109">Define a Voice Route</span></span>

  - <span data-ttu-id="314e0-110">Enable Users for Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="314e0-110">Enable Users for Enterprise Voice</span></span>

<div>

## <a name="create-a-trunk"></a><span data-ttu-id="314e0-111">Créer un Trunk</span><span class="sxs-lookup"><span data-stu-id="314e0-111">Create a Trunk</span></span>

<span data-ttu-id="314e0-112">Vous devez définir des Trunks dans votre déploiement voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="314e0-112">You must define trunks in your Enterprise Voice deployment.</span></span> <span data-ttu-id="314e0-113">Pour le routage Location-Based, vous devez créer une configuration de Trunk par Trunk.</span><span class="sxs-lookup"><span data-stu-id="314e0-113">For Location-Based Routing, you must create a trunk configuration per trunk.</span></span> <span data-ttu-id="314e0-114">Utilisez le générateur de topologie de serveur Lync pour définir vos Trunks, puis utilisez la commande Windows PowerShell de Lync Server, le nouveau-CsTrunkConfiguration ou le panneau de configuration de Lync Server pour définir les configurations de Trunk correspondantes.</span><span class="sxs-lookup"><span data-stu-id="314e0-114">Use the Lync Server Topology Builder to define your trunks, and use the Lync Server Windows PowerShell command, New-CsTrunkConfiguration, or the Lync Server Control Panel to define the corresponding trunk configurations.</span></span> <span data-ttu-id="314e0-115">Pour plus d’informations sur l’activation du routage de Location-Based sur les configurations de Trunk, reportez-vous à la rubrique activer Location-Based le routage sur les Trunks, dans la rubrique [activation du routage des Location-Based dans Lync Server 2013](lync-server-2013-enabling-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="314e0-115">More information on how to enable Location-Based Routing on trunk configurations can be found in the section, Enable Location-Based Routing to Trunks, in the topic, [Enabling Location-Based Routing in Lync Server 2013](lync-server-2013-enabling-location-based-routing.md).</span></span> <span data-ttu-id="314e0-116">Pour cet exemple, le tableau ci-dessous illustre les Trunks utilisés dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="314e0-116">For this example, the following table illustrates the trunks used in this scenario.</span></span>

<span data-ttu-id="314e0-117">Pour plus d’informations, reportez-vous à la section [définir des lignes supplémentaires dans le générateur de topologie de Lync Server 2013](lync-server-2013-define-additional-trunks-in-topology-builder.md).</span><span class="sxs-lookup"><span data-stu-id="314e0-117">For more information, see [Define additional trunks in Topology Builder in Lync Server 2013](lync-server-2013-define-additional-trunks-in-topology-builder.md).</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="314e0-118">Nom du Trunk</span><span class="sxs-lookup"><span data-stu-id="314e0-118">Trunk name</span></span></th>
<th><span data-ttu-id="314e0-119">Type de système</span><span class="sxs-lookup"><span data-stu-id="314e0-119">System type</span></span></th>
<th><span data-ttu-id="314e0-120">Nom</span><span class="sxs-lookup"><span data-stu-id="314e0-120">Name</span></span></th>
<th><span data-ttu-id="314e0-121">Lieu</span><span class="sxs-lookup"><span data-stu-id="314e0-121">Location</span></span></th>
<th><span data-ttu-id="314e0-122">serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="314e0-122">Mediation Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="314e0-123">Trunk 1 DEL-GW</span><span class="sxs-lookup"><span data-stu-id="314e0-123">Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="314e0-124">Passerelle RTC</span><span class="sxs-lookup"><span data-stu-id="314e0-124">PSTN gateway</span></span></p></td>
<td><p><span data-ttu-id="314e0-125">DEL-GW</span><span class="sxs-lookup"><span data-stu-id="314e0-125">DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="314e0-126">Delhi</span><span class="sxs-lookup"><span data-stu-id="314e0-126">Delhi</span></span></p></td>
<td><p><span data-ttu-id="314e0-127">MS1</span><span class="sxs-lookup"><span data-stu-id="314e0-127">MS1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="314e0-128">Trunk 2 HYD-GW</span><span class="sxs-lookup"><span data-stu-id="314e0-128">Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="314e0-129">Passerelle RTC</span><span class="sxs-lookup"><span data-stu-id="314e0-129">PSTN gateway</span></span></p></td>
<td><p><span data-ttu-id="314e0-130">HYD-GW</span><span class="sxs-lookup"><span data-stu-id="314e0-130">HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="314e0-131">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="314e0-131">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="314e0-132">MS1</span><span class="sxs-lookup"><span data-stu-id="314e0-132">MS1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="314e0-133">Trunk 3 DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="314e0-133">Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="314e0-134">Private</span><span class="sxs-lookup"><span data-stu-id="314e0-134">PBX</span></span></p></td>
<td><p><span data-ttu-id="314e0-135">DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="314e0-135">DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="314e0-136">Delhi</span><span class="sxs-lookup"><span data-stu-id="314e0-136">Delhi</span></span></p></td>
<td><p><span data-ttu-id="314e0-137">MS1</span><span class="sxs-lookup"><span data-stu-id="314e0-137">MS1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="314e0-138">Trunk 4 HYD-PBX</span><span class="sxs-lookup"><span data-stu-id="314e0-138">Trunk 4 HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="314e0-139">Private</span><span class="sxs-lookup"><span data-stu-id="314e0-139">PBX</span></span></p></td>
<td><p><span data-ttu-id="314e0-140">HYD-PBX</span><span class="sxs-lookup"><span data-stu-id="314e0-140">HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="314e0-141">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="314e0-141">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="314e0-142">MS1</span><span class="sxs-lookup"><span data-stu-id="314e0-142">MS1</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="defines-voice-policies"></a><span data-ttu-id="314e0-143">Définit les stratégies vocales</span><span class="sxs-lookup"><span data-stu-id="314e0-143">Defines Voice Policies</span></span>

<span data-ttu-id="314e0-144">Vous devez définir des politiques vocales pour le déploiement de votre voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="314e0-144">You must define voice policies for your Enterprise Voice deployment.</span></span> <span data-ttu-id="314e0-145">Définissez une stratégie vocale pour appliquer des restrictions de routage de Location-Based à un sous-ensemble d’utilisateurs, si seul un sous-ensemble d’eux est requis pour utiliser Location-Based routage.</span><span class="sxs-lookup"><span data-stu-id="314e0-145">Define a Voice Policy to enforce Location-Based Routing restrictions to a subset of users if only a subset of them is required to use Location-Based Routing.</span></span> <span data-ttu-id="314e0-146">Pour cet exemple, le tableau ci-dessous illustre les stratégies vocales utilisées dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="314e0-146">For this example, the following table illustrates the voice policies used in this scenario.</span></span> <span data-ttu-id="314e0-147">Seuls les paramètres spécifiques au routage Location-Based sont inclus dans la table à des fins d’illustration.</span><span class="sxs-lookup"><span data-stu-id="314e0-147">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="314e0-148">Pour plus d’informations, reportez-vous [à configuration des stratégies de voix et des enregistrements d’utilisation RTC pour autoriser les fonctionnalités et privilèges d’utilisation dans Lync Server 2013](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md).</span><span class="sxs-lookup"><span data-stu-id="314e0-148">For more information, see [Configuring voice policies and PSTN usage records to authorize calling features and privileges in Lync Server 2013](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="314e0-149">Politique vocale 1</span><span class="sxs-lookup"><span data-stu-id="314e0-149">Voice policy 1</span></span></th>
<th><span data-ttu-id="314e0-150">Politique vocale 2</span><span class="sxs-lookup"><span data-stu-id="314e0-150">Voice policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="314e0-151">ID de la stratégie vocale</span><span class="sxs-lookup"><span data-stu-id="314e0-151">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="314e0-152">Politique vocale de Delhi</span><span class="sxs-lookup"><span data-stu-id="314e0-152">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="314e0-153">Politique vocale Hyderabad</span><span class="sxs-lookup"><span data-stu-id="314e0-153">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="314e0-154">Usages RTC</span><span class="sxs-lookup"><span data-stu-id="314e0-154">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="314e0-155">Utilisation de Delhi, utilisation de PBX del, utilisation du PBX HYD</span><span class="sxs-lookup"><span data-stu-id="314e0-155">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="314e0-156">Utilisation de Hyderabad, utilisation de PBX HYD, utilisation de PBX del</span><span class="sxs-lookup"><span data-stu-id="314e0-156">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="314e0-157">PreventPSTNTollBypass</span><span class="sxs-lookup"><span data-stu-id="314e0-157">PreventPSTNTollBypass</span></span></p></td>
<td><p><span data-ttu-id="314e0-158">False</span><span class="sxs-lookup"><span data-stu-id="314e0-158">False</span></span></p></td>
<td><p><span data-ttu-id="314e0-159">False</span><span class="sxs-lookup"><span data-stu-id="314e0-159">False</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="define-voice-routes"></a><span data-ttu-id="314e0-160">Définir des itinéraires vocaux</span><span class="sxs-lookup"><span data-stu-id="314e0-160">Define Voice Routes</span></span>

<span data-ttu-id="314e0-161">Vous devez définir des itinéraires vocaux pour votre déploiement voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="314e0-161">You must define voice routes for your Enterprise Voice deployment.</span></span> <span data-ttu-id="314e0-162">Pour cet exemple, le tableau ci-dessous illustre les itinéraires vocaux utilisés dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="314e0-162">For this example, the following table illustrates the voice routes used in this scenario.</span></span> <span data-ttu-id="314e0-163">Seuls les paramètres spécifiques au routage Location-Based sont inclus dans la table à des fins d’illustration.</span><span class="sxs-lookup"><span data-stu-id="314e0-163">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="314e0-164">Pour plus d’informations, reportez-vous à la rubrique [Configuration des itinéraires vocaux pour les appels sortants dans Lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).</span><span class="sxs-lookup"><span data-stu-id="314e0-164">For more information, see [Configuring voice routes for outbound calls in Lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="314e0-165">Route vocale 1</span><span class="sxs-lookup"><span data-stu-id="314e0-165">Voice route 1</span></span></th>
<th><span data-ttu-id="314e0-166">Route vocale 2</span><span class="sxs-lookup"><span data-stu-id="314e0-166">Voice route 2</span></span></th>
<th><span data-ttu-id="314e0-167">Route vocale 3</span><span class="sxs-lookup"><span data-stu-id="314e0-167">Voice route 3</span></span></th>
<th><span data-ttu-id="314e0-168">Route vocale 4</span><span class="sxs-lookup"><span data-stu-id="314e0-168">Voice route 4</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="314e0-169">Nom</span><span class="sxs-lookup"><span data-stu-id="314e0-169">Name</span></span></p></td>
<td><p><span data-ttu-id="314e0-170">Delhi route</span><span class="sxs-lookup"><span data-stu-id="314e0-170">Delhi route</span></span></p></td>
<td><p><span data-ttu-id="314e0-171">Route Hyderabad</span><span class="sxs-lookup"><span data-stu-id="314e0-171">Hyderabad route</span></span></p></td>
<td><p><span data-ttu-id="314e0-172">Route PBX del</span><span class="sxs-lookup"><span data-stu-id="314e0-172">PBX Del route</span></span></p></td>
<td><p><span data-ttu-id="314e0-173">Route HYD PBX</span><span class="sxs-lookup"><span data-stu-id="314e0-173">PBX Hyd route</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="314e0-174">Usages RTC</span><span class="sxs-lookup"><span data-stu-id="314e0-174">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="314e0-175">L’utilisation de Delhi</span><span class="sxs-lookup"><span data-stu-id="314e0-175">Delhi usage</span></span></p></td>
<td><p><span data-ttu-id="314e0-176">Utilisation de Hyderabad</span><span class="sxs-lookup"><span data-stu-id="314e0-176">Hyderabad usage</span></span></p></td>
<td><p><span data-ttu-id="314e0-177">Utilisation de PBX del</span><span class="sxs-lookup"><span data-stu-id="314e0-177">PBX Del usage</span></span></p></td>
<td><p><span data-ttu-id="314e0-178">Utilisation de HYD PBX</span><span class="sxs-lookup"><span data-stu-id="314e0-178">PBX Hyd usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="314e0-179">Jonction</span><span class="sxs-lookup"><span data-stu-id="314e0-179">Trunk</span></span></p></td>
<td><p><span data-ttu-id="314e0-180">Trunk 1 DEL-GW</span><span class="sxs-lookup"><span data-stu-id="314e0-180">Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="314e0-181">Trunk 2 HYD-GW</span><span class="sxs-lookup"><span data-stu-id="314e0-181">Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="314e0-182">Trunk 3 DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="314e0-182">Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="314e0-183">Trunk 4 HYD-PBX</span><span class="sxs-lookup"><span data-stu-id="314e0-183">Trunk 4 HYD-PBX</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-users-for-enterprise-voice"></a><span data-ttu-id="314e0-184">Enable Users for Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="314e0-184">Enable Users for Enterprise Voice</span></span>

<span data-ttu-id="314e0-185">Activez les utilisateurs pour voix entreprise et attribuez-leur une stratégie vocale déjà définie.</span><span class="sxs-lookup"><span data-stu-id="314e0-185">Enable users for Enterprise Voice and assign them a voice policy you’ve previously defined.</span></span> <span data-ttu-id="314e0-186">Pour cet exemple, le tableau ci-dessous illustre l’affectation utilisée dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="314e0-186">For this example, the following table illustrates the assignment used in this scenario.</span></span> <span data-ttu-id="314e0-187">Seuls les paramètres spécifiques au routage Location-Based sont inclus dans la table à des fins d’illustration.</span><span class="sxs-lookup"><span data-stu-id="314e0-187">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="314e0-188">Pour plus d’informations, reportez-vous à [activer l’application voix entreprise dans Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span><span class="sxs-lookup"><span data-stu-id="314e0-188">For more information, see [Enable users for Enterprise Voice in Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="314e0-189">Utilisateurs situés à Delhi</span><span class="sxs-lookup"><span data-stu-id="314e0-189">Users located in Delhi</span></span></th>
<th><span data-ttu-id="314e0-190">Utilisateurs situés dans Hyderabad</span><span class="sxs-lookup"><span data-stu-id="314e0-190">Users located in Hyderabad</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="314e0-191">Politique vocale associée</span><span class="sxs-lookup"><span data-stu-id="314e0-191">Associated voice policy</span></span></p></td>
<td><p><span data-ttu-id="314e0-192">Politique vocale de Delhi</span><span class="sxs-lookup"><span data-stu-id="314e0-192">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="314e0-193">Politique vocale Hyderabad</span><span class="sxs-lookup"><span data-stu-id="314e0-193">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="314e0-194">Exemples d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="314e0-194">Sample users</span></span></p></td>
<td><p><span data-ttu-id="314e0-195">DEL-LYNC-1, DEL-LYNC-2, DEL-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="314e0-195">DEL-LYNC-1,DEL-LYNC-2,DEL-LYNC-3</span></span></p></td>
<td><p><span data-ttu-id="314e0-196">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="314e0-196">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="314e0-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="314e0-197">See Also</span></span>


[<span data-ttu-id="314e0-198">Configuration du routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="314e0-198">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="314e0-199"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="314e0-199"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

