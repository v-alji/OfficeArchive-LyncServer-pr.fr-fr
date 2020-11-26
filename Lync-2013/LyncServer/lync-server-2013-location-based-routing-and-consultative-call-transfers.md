---
title: 'Lync Server 2013 : Location-Based de routage et de consultation des appels'
description: 'Lync Server 2013 : Location-Based de routage et de consultation des appels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location-Based Routing and consultative call transfers
ms:assetid: b12460c2-36c8-481f-b867-fe10dc1c0bdf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362836(v=OCS.15)
ms:contentKeyID: 56335089
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d07cf6a33ff4d6ad57f8913a798fac3bc393a00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426551"
---
# <a name="location-based-routing-and-consultative-call-transfers-in-lync-server-2013"></a><span data-ttu-id="0fd46-103">Acheminement des appels d' Location-Based de routage et de consultation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0fd46-103">Location-Based Routing and consultative call transfers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0fd46-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0fd46-104">

<span> </span></span></span>

<span data-ttu-id="0fd46-105">_**Dernière modification de la rubrique :** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="0fd46-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="0fd46-106">En plus d’appliquer des Location-Based le routage aux réunions Lync, l’application de conférence de routage Location-Based applique les restrictions de routage Location-Basedes sur le transfert d’appel consultatif vers les points de terminaison RTC.</span><span class="sxs-lookup"><span data-stu-id="0fd46-106">In addition to enforcing Location-Based Routing to Lync meetings, the Location-Based Routing Conferencing application enforces Location-Based Routing restrictions on consultative call transfers that egress to PSTN endpoints.</span></span> <span data-ttu-id="0fd46-107">Un transfert d’appel consultatif est un appel établi entre deux parties dans lequel une des parties transfère l’appel vers un nouvel utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0fd46-107">A consultative call transfer is a call established between two parties where one of the parties transfers the call to a new user.</span></span> <span data-ttu-id="0fd46-108">Par exemple, un point de terminaison PSTN appelle l’utilisateur A (appelé Lync).</span><span class="sxs-lookup"><span data-stu-id="0fd46-108">For example, a PSTN endpoint calls user A (Lync callee).</span></span> <span data-ttu-id="0fd46-109">Un utilisateur A détermine que l’utilisateur RTC doit être renvoyé à l’utilisateur B (utilisateur Lync).</span><span class="sxs-lookup"><span data-stu-id="0fd46-109">User A determines the PSTN user should be forwarded to user B (Lync user).</span></span> <span data-ttu-id="0fd46-110">L’utilisateur A passe l’appel avec l’utilisateur PSTN en attente, et appelle l’utilisateur B. L’utilisateur B accepte de parler à l’utilisateur PSTN.</span><span class="sxs-lookup"><span data-stu-id="0fd46-110">User A places the call with the PSTN user on hold, and calls user B. User B agrees to talk to the PSTN user.</span></span> <span data-ttu-id="0fd46-111">L’utilisateur A transfère l’appel en attente à l’utilisateur B.</span><span class="sxs-lookup"><span data-stu-id="0fd46-111">User A transfers the call on-hold to user B.</span></span>

<span data-ttu-id="0fd46-112">**Flux des transferts d’appel consultatifs**</span><span class="sxs-lookup"><span data-stu-id="0fd46-112">**Consultative call transfer call flow**</span></span>

<span data-ttu-id="0fd46-113">![Diagramme Routage géodépendant pour les conférences](images/Dn362836.e4d43d6f-23d2-49c9-b12b-15248a743f92(OCS.15).jpg "Diagramme Routage géodépendant pour les conférences")</span><span class="sxs-lookup"><span data-stu-id="0fd46-113">![Location-based routing for conferencing diagram](images/Dn362836.e4d43d6f-23d2-49c9-b12b-15248a743f92(OCS.15).jpg "Location-based routing for conferencing diagram")</span></span>

<span data-ttu-id="0fd46-114">Lorsqu’un utilisateur a activé le routage de Location-Based initie un transfert d’appel d’un point de terminaison PSTN (comme le montre l’illustration précédente), il génère deux appels actifs, un appel entre l’utilisateur RTC et l’utilisateur Lync A, et les autres utilisateurs de Lync A et Lync B. le comportement suivant est appliqué par l’application de conférence de routage Location-Based :</span><span class="sxs-lookup"><span data-stu-id="0fd46-114">When a user enabled for Location-Based Routing initiates a consultative call transfer of a PSTN endpoint (as shown in the preceding figure), this creates two active calls, one call between the PSTN user and Lync user A, and the other between Lync user A and Lync user B. the following behavior is enforced by the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="0fd46-115">Si le routage SIP Trunk est autorisé à rediriger l’appel RTC vers le site du réseau sur lequel l’utilisateur de Lync B (c.-à-d. destination du transfert) se trouve, le transfert d’appel sera autorisé. dans le cas contraire, le transfert d’appel consultatif sera bloqué.</span><span class="sxs-lookup"><span data-stu-id="0fd46-115">If the SIP trunk routing the PSTN call is authorized to re-route the PSTN call to the network site where Lync user B (i.e. transfer target) is located,, then the call transfer will be allowed; otherwise, the consultative call transfer will be blocked.</span></span> <span data-ttu-id="0fd46-116">Cette autorisation est effectuée en fonction de l’emplacement de la partie transférée sur le même site réseau que le Trunk SIP qui achemine l’appel actif vers le point de terminaison RTC.</span><span class="sxs-lookup"><span data-stu-id="0fd46-116">This authorization is performed based on the transferred party’s location being in the same network site as the SIP trunk that is routing the active call to the PSTN endpoint.</span></span>

  - <span data-ttu-id="0fd46-117">Si le routage SIP de l’appel RTC n’est pas autorisé à acheminer les appels vers le site du réseau sur lequel la partie transférée (utilisateur Lync B) est située ou si la partie transférée est située sur un site réseau inconnu, le transfert d’appel vers le point de terminaison RTC (c.-à-d. destination du transfert d’appel) sera bloqué.</span><span class="sxs-lookup"><span data-stu-id="0fd46-117">If the SIP trunk routing the inbound PSTN call is not authorized to route calls to the network site where the transferred party (Lync user B) is located or the transferred party is located in an unknown network site, then the consultative call transfer to the PSTN endpoint (i.e. call transfer target) will be blocked.</span></span>

<span data-ttu-id="0fd46-118">Le tableau suivant décrit la façon dont Location-Based restrictions de routage sont appliquées par l’application de conférence de routage Location-Based pour les transferts d’appel.</span><span class="sxs-lookup"><span data-stu-id="0fd46-118">The following table describes how Location-Based Routing restrictions are applied by the Location-Based Routing Conferencing application for consultative call transfers.</span></span> <span data-ttu-id="0fd46-119">Si les points de terminaison PBX ne sont pas directement associés à un site réseau, la jonction SIP à laquelle le PBX est connecté peut être affectée à un site réseau.</span><span class="sxs-lookup"><span data-stu-id="0fd46-119">Although PBX endpoints are not directly associated with a network site, the SIP trunk the PBX is connected to can be assigned a network site.</span></span> <span data-ttu-id="0fd46-120">Par conséquent, le point de terminaison PBX peut être indirectement associé à un site réseau.</span><span class="sxs-lookup"><span data-stu-id="0fd46-120">Therefore, the PBX endpoint can be indirectly associated with a network site.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0fd46-121">Site réseau de la partie dont l’appel est transféré</span><span class="sxs-lookup"><span data-stu-id="0fd46-121">Network site of call transferred party</span></span></p></td>
<td><p><span data-ttu-id="0fd46-122">Site réseau de la cible de transfert d’appel</span><span class="sxs-lookup"><span data-stu-id="0fd46-122">Network site of call transfer target</span></span></p></td>
<td><p><span data-ttu-id="0fd46-123">Comportement</span><span class="sxs-lookup"><span data-stu-id="0fd46-123">Behavior</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fd46-124">Point de terminaison PSTN</span><span class="sxs-lookup"><span data-stu-id="0fd46-124">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="0fd46-125">Utilisateur Lync sur le même site réseau (par exemple, site 1)</span><span class="sxs-lookup"><span data-stu-id="0fd46-125">Lync user in the same network site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="0fd46-126">Le transfert consultatif est autorisé</span><span class="sxs-lookup"><span data-stu-id="0fd46-126">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fd46-127">Point de terminaison PSTN</span><span class="sxs-lookup"><span data-stu-id="0fd46-127">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="0fd46-128">Utilisateur Lync dans différents sites réseau (par exemple, site 2)</span><span class="sxs-lookup"><span data-stu-id="0fd46-128">Lync user in different network sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="0fd46-129">Le transfert consultatif n’est pas autorisé</span><span class="sxs-lookup"><span data-stu-id="0fd46-129">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fd46-130">Point de terminaison PSTN</span><span class="sxs-lookup"><span data-stu-id="0fd46-130">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="0fd46-131">Utilisateur Lync dans un site réseau inconnu</span><span class="sxs-lookup"><span data-stu-id="0fd46-131">Lync user in an unknown network site</span></span></p></td>
<td><p><span data-ttu-id="0fd46-132">Le transfert consultatif n’est pas autorisé</span><span class="sxs-lookup"><span data-stu-id="0fd46-132">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fd46-133">Point de terminaison PSTN</span><span class="sxs-lookup"><span data-stu-id="0fd46-133">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="0fd46-134">Utilisateur fédéré de Lync</span><span class="sxs-lookup"><span data-stu-id="0fd46-134">Federated Lync user</span></span></p></td>
<td><p><span data-ttu-id="0fd46-135">Le transfert consultatif n’est pas autorisé</span><span class="sxs-lookup"><span data-stu-id="0fd46-135">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fd46-136">Point de terminaison PSTN</span><span class="sxs-lookup"><span data-stu-id="0fd46-136">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="0fd46-137">Point de terminaison PBX dans le même site (site 1)</span><span class="sxs-lookup"><span data-stu-id="0fd46-137">PBX endpoint in the same site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="0fd46-138">Le transfert consultatif est autorisé</span><span class="sxs-lookup"><span data-stu-id="0fd46-138">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fd46-139">Point de terminaison PSTN</span><span class="sxs-lookup"><span data-stu-id="0fd46-139">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="0fd46-140">Point de terminaison PBX dans un autre site (site 2)</span><span class="sxs-lookup"><span data-stu-id="0fd46-140">PBX endpoint in a different sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="0fd46-141">Le transfert consultatif n’est pas autorisé</span><span class="sxs-lookup"><span data-stu-id="0fd46-141">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fd46-142">Point de terminaison PBX dans le même site (site 1)</span><span class="sxs-lookup"><span data-stu-id="0fd46-142">PBX endpoint in the same site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="0fd46-143">Point de terminaison PSTN</span><span class="sxs-lookup"><span data-stu-id="0fd46-143">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="0fd46-144">Le transfert consultatif est autorisé</span><span class="sxs-lookup"><span data-stu-id="0fd46-144">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fd46-145">Point de terminaison PBX dans un autre site (site 2)</span><span class="sxs-lookup"><span data-stu-id="0fd46-145">PBX endpoint in a different site (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="0fd46-146">Point de terminaison PSTN</span><span class="sxs-lookup"><span data-stu-id="0fd46-146">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="0fd46-147">Le transfert consultatif n’est pas autorisé</span><span class="sxs-lookup"><span data-stu-id="0fd46-147">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fd46-148">Point de terminaison PBX dans un site quelconque</span><span class="sxs-lookup"><span data-stu-id="0fd46-148">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="0fd46-149">Utilisateur Lync sur le même site réseau (par exemple, site 1)</span><span class="sxs-lookup"><span data-stu-id="0fd46-149">Lync user in the same network site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="0fd46-150">Le transfert consultatif est autorisé</span><span class="sxs-lookup"><span data-stu-id="0fd46-150">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fd46-151">Point de terminaison PBX dans un site quelconque</span><span class="sxs-lookup"><span data-stu-id="0fd46-151">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="0fd46-152">Utilisateur Lync dans différents sites réseau (par exemple, site 2)</span><span class="sxs-lookup"><span data-stu-id="0fd46-152">Lync user in different network sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="0fd46-153">Le transfert consultatif est autorisé</span><span class="sxs-lookup"><span data-stu-id="0fd46-153">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fd46-154">Point de terminaison PBX dans un site quelconque</span><span class="sxs-lookup"><span data-stu-id="0fd46-154">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="0fd46-155">Utilisateur Lync dans un site réseau inconnu</span><span class="sxs-lookup"><span data-stu-id="0fd46-155">Lync user in an unknown network site</span></span></p></td>
<td><p><span data-ttu-id="0fd46-156">Le transfert consultatif est autorisé</span><span class="sxs-lookup"><span data-stu-id="0fd46-156">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fd46-157">Point de terminaison PBX dans un site quelconque</span><span class="sxs-lookup"><span data-stu-id="0fd46-157">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="0fd46-158">Utilisateur fédéré de Lync</span><span class="sxs-lookup"><span data-stu-id="0fd46-158">Federated Lync user</span></span></p></td>
<td><p><span data-ttu-id="0fd46-159">Le transfert consultatif est autorisé</span><span class="sxs-lookup"><span data-stu-id="0fd46-159">Consultative transfer will be allowed</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0fd46-160">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0fd46-160">


</div>

<span> </span>

</div>

</div>

</span></span></div>

