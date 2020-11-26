---
title: 'Lync Server 2013 : Prise en charge des clients et des serveurs pour le routage géodépendant'
description: 'Lync Server 2013 : prise en charge du routage Location-Based par le client et le serveur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Client and server support for Location-Based Routing
ms:assetid: 26c2ca3d-026d-4dd7-94fa-15ebb4406953
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994024(v=OCS.15)
ms:contentKeyID: 51803933
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20dca7444f58ee62dbc36edbb7d9e1c976a97807
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434899"
---
# <a name="client-and-server-support-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="d1a92-103">Prise en charge des clients et des serveurs pour le routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d1a92-103">Client and server support for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d1a92-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d1a92-104">

<span> </span></span></span>

<span data-ttu-id="d1a92-105">_**Dernière modification de la rubrique :** 2013-06-18_</span><span class="sxs-lookup"><span data-stu-id="d1a92-105">_**Topic Last Modified:** 2013-06-18_</span></span>

<span data-ttu-id="d1a92-106">Le routage Location-Based est appliqué par Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d1a92-106">Location-Based Routing is enforced by Lync Server.</span></span> <span data-ttu-id="d1a92-107">Lync Server peut identifier les sites réseau dans lesquels les utilisateurs se connectent au sein du réseau d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="d1a92-107">Lync Server can identify the network sites where users are connecting from within the corporate network.</span></span> <span data-ttu-id="d1a92-108">Comme les utilisateurs distants sont situés en dehors du réseau d’entreprise, leur emplacement est considéré comme inconnu.</span><span class="sxs-lookup"><span data-stu-id="d1a92-108">Since remote users are outside the corporate network, their location is considered to be unknown.</span></span>

<div>

## <a name="lync-server-support"></a><span data-ttu-id="d1a92-109">Prise en charge de Lync Server</span><span class="sxs-lookup"><span data-stu-id="d1a92-109">Lync Server Support</span></span>

<span data-ttu-id="d1a92-110">Location-Based le routage nécessite le déploiement de Lync Server 2013 CU1 sur tous les pools frontaux et les serveurs Standard Edition dans une topologie donnée.</span><span class="sxs-lookup"><span data-stu-id="d1a92-110">Location-Based Routing requires that Lync Server 2013 CU1 is deployed on all Front End pools and Standard Edition servers in a given topology.</span></span> <span data-ttu-id="d1a92-111">Si Lync Server 2013 CU1 n’est pas installé sur certains composants Lync de la topologie, Location-Based restrictions de routage ne peuvent pas être appliquées entièrement.</span><span class="sxs-lookup"><span data-stu-id="d1a92-111">If Lync Server 2013 CU1 is not installed on certain Lync components in the topology, Location-Based Routing restrictions cannot be fully enforced.</span></span>

<span data-ttu-id="d1a92-112">Le tableau suivant identifie la combinaison des rôles de serveur et des versions prises en charge pour le routage Location-Based.</span><span class="sxs-lookup"><span data-stu-id="d1a92-112">The following table identifies the combination of server roles and versions that is supported for Location-Based Routing.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d1a92-113">Version du pool</span><span class="sxs-lookup"><span data-stu-id="d1a92-113">Pool version</span></span></th>
<th><span data-ttu-id="d1a92-114">Version de serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="d1a92-114">Mediation Server version</span></span></th>
<th><span data-ttu-id="d1a92-115">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1a92-115">Supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1a92-116">Mise à jour cumulative de Lync Server 2013 février 2013</span><span class="sxs-lookup"><span data-stu-id="d1a92-116">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="d1a92-117">Mise à jour cumulative de Lync Server 2013 février 2013</span><span class="sxs-lookup"><span data-stu-id="d1a92-117">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="d1a92-118">Oui</span><span class="sxs-lookup"><span data-stu-id="d1a92-118">yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1a92-119">Mise à jour cumulative de Lync Server 2013 février 2013</span><span class="sxs-lookup"><span data-stu-id="d1a92-119">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="d1a92-120">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d1a92-120">Lync Server 2013</span></span></p></td>
<td><p><span data-ttu-id="d1a92-121">Non</span><span class="sxs-lookup"><span data-stu-id="d1a92-121">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1a92-122">Mise à jour cumulative de Lync Server 2013 février 2013</span><span class="sxs-lookup"><span data-stu-id="d1a92-122">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="d1a92-123">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="d1a92-123">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="d1a92-124">Non</span><span class="sxs-lookup"><span data-stu-id="d1a92-124">no</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1a92-125">Mise à jour cumulative de Lync Server 2013 février 2013</span><span class="sxs-lookup"><span data-stu-id="d1a92-125">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="d1a92-126">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="d1a92-126">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="d1a92-127">Non</span><span class="sxs-lookup"><span data-stu-id="d1a92-127">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1a92-128">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d1a92-128">Lync Server 2013</span></span></p></td>
<td><p><span data-ttu-id="d1a92-129">Quelconque</span><span class="sxs-lookup"><span data-stu-id="d1a92-129">any</span></span></p></td>
<td><p><span data-ttu-id="d1a92-130">Non</span><span class="sxs-lookup"><span data-stu-id="d1a92-130">no</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1a92-131">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="d1a92-131">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="d1a92-132">Quelconque</span><span class="sxs-lookup"><span data-stu-id="d1a92-132">any</span></span></p></td>
<td><p><span data-ttu-id="d1a92-133">Non</span><span class="sxs-lookup"><span data-stu-id="d1a92-133">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1a92-134">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="d1a92-134">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="d1a92-135">Quelconque</span><span class="sxs-lookup"><span data-stu-id="d1a92-135">any</span></span></p></td>
<td><p><span data-ttu-id="d1a92-136">Non</span><span class="sxs-lookup"><span data-stu-id="d1a92-136">no</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="lync-client-support"></a><span data-ttu-id="d1a92-137">Prise en charge du client Lync</span><span class="sxs-lookup"><span data-stu-id="d1a92-137">Lync Client Support</span></span>

<span data-ttu-id="d1a92-138">Le tableau suivant identifie les clients pris en charge par Location-Based routage.</span><span class="sxs-lookup"><span data-stu-id="d1a92-138">The following table identifies the clients that Location-Based Routing supports.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d1a92-139">Type de client</span><span class="sxs-lookup"><span data-stu-id="d1a92-139">Client type</span></span></th>
<th><span data-ttu-id="d1a92-140">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1a92-140">Supported</span></span></th>
<th><span data-ttu-id="d1a92-141">Détails</span><span class="sxs-lookup"><span data-stu-id="d1a92-141">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1a92-142">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="d1a92-142">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="d1a92-143">Oui</span><span class="sxs-lookup"><span data-stu-id="d1a92-143">yes</span></span></p></td>
<td><p><span data-ttu-id="d1a92-144">Y compris la mise à jour cumulative de Lync 2013 février 2013</span><span class="sxs-lookup"><span data-stu-id="d1a92-144">Including Lync 2013 February 2013 Cumulative Update</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1a92-145">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="d1a92-145">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="d1a92-146">Oui</span><span class="sxs-lookup"><span data-stu-id="d1a92-146">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1a92-147">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="d1a92-147">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="d1a92-148">Non</span><span class="sxs-lookup"><span data-stu-id="d1a92-148">no</span></span></p></td>
<td> </td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1a92-149">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="d1a92-149">Lync Phone Edition</span></span></p></td>
<td><p><span data-ttu-id="d1a92-150">Oui</span><span class="sxs-lookup"><span data-stu-id="d1a92-150">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1a92-151">Lync Attendant</span><span class="sxs-lookup"><span data-stu-id="d1a92-151">Lync Attendant</span></span></p></td>
<td><p><span data-ttu-id="d1a92-152">Oui</span><span class="sxs-lookup"><span data-stu-id="d1a92-152">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1a92-153">Lync pour Windows 8</span><span class="sxs-lookup"><span data-stu-id="d1a92-153">Lync for Windows 8</span></span></p></td>
<td><p><span data-ttu-id="d1a92-154">Non</span><span class="sxs-lookup"><span data-stu-id="d1a92-154">no</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1a92-155">2013 mobile Lync</span><span class="sxs-lookup"><span data-stu-id="d1a92-155">Lync Mobile 2013</span></span></p></td>
<td><p><span data-ttu-id="d1a92-156">Non</span><span class="sxs-lookup"><span data-stu-id="d1a92-156">no</span></span></p></td>
<td><p><span data-ttu-id="d1a92-157">VoIP doit être désactivée pour les clients 2013 mobiles Lync, s’il est utilisé par les utilisateurs dotés du routage Location-Based activé.</span><span class="sxs-lookup"><span data-stu-id="d1a92-157">VoIP must be disabled for Lync Mobile 2013 clients if used by users with Location-Based Routing enabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1a92-158">2010 mobile Lync</span><span class="sxs-lookup"><span data-stu-id="d1a92-158">Lync Mobile 2010</span></span></p></td>
<td><p><span data-ttu-id="d1a92-159">Oui</span><span class="sxs-lookup"><span data-stu-id="d1a92-159">yes</span></span></p></td>
<td> </td>
</tr>
</tbody>
</table>

  

<div>


> [!NOTE]  
> <span data-ttu-id="d1a92-160">Pour désactiver la voix sur IP (VoIP) pour les clients 2013 Lync mobile, attribuez une stratégie de mobilité avec le paramètre, audio/vidéo IP désactivé pour tous les utilisateurs activés pour le routage en fonction de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="d1a92-160">To disable VoIP for Lync Mobile 2013 clients, assign a mobility policy with the setting, IP Audio/Video, disabled for all users enabled for Location Based Routing.</span></span> <span data-ttu-id="d1a92-161">Pour plus d’informations sur la stratégie de mobilité, reportez-vous à <A href="https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy">New-CsMobilityPolicy</A>.</span><span class="sxs-lookup"><span data-stu-id="d1a92-161">For more details about mobility policy, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy">New-CsMobilityPolicy</A>.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d1a92-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1a92-162">See Also</span></span>


[<span data-ttu-id="d1a92-163">Planification du routage géodépendant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d1a92-163">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="d1a92-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d1a92-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

