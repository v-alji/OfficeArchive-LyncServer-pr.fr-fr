---
title: 'Lync Server 2013 : Table VoipDetails'
description: 'Tableau Lync Server 2013 : VoipDetails'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VoipDetails table
ms:assetid: 74ffbb71-569b-4018-be1f-4db2bbafcf36
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398566(v=OCS.15)
ms:contentKeyID: 48184522
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f23d991c1d577a15717de2572d744e1b65ba6bab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393785"
---
# <a name="voipdetails-table-in-lync-server-2013"></a><span data-ttu-id="0ae1f-103">Table VoipDetails dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ae1f-103">VoipDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0ae1f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0ae1f-104">

<span> </span></span></span>

<span data-ttu-id="0ae1f-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="0ae1f-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="0ae1f-106">Chaque enregistrement 1 2 représente un appel vers un tiers, dont au moins un utilisateur est une VoIP.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-106">Each record represents one two-party call in which at least one user is a VoIP user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ae1f-107">Colonne</span><span class="sxs-lookup"><span data-stu-id="0ae1f-107">Column</span></span></th>
<th><span data-ttu-id="0ae1f-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="0ae1f-108">Data Type</span></span></th>
<th><span data-ttu-id="0ae1f-109">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="0ae1f-109">Key/Index</span></span></th>
<th><span data-ttu-id="0ae1f-110">Détails</span><span class="sxs-lookup"><span data-stu-id="0ae1f-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ae1f-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="0ae1f-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae1f-112">DateHeure</span><span class="sxs-lookup"><span data-stu-id="0ae1f-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-113">Principal</span><span class="sxs-lookup"><span data-stu-id="0ae1f-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-114">Durée de la demande de session.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-114">Time of session request.</span></span> <span data-ttu-id="0ae1f-115">Utilisé conjointement avec <strong>SessionIdSeq</strong> pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="0ae1f-116">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ae1f-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae1f-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="0ae1f-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae1f-118">int</span><span class="sxs-lookup"><span data-stu-id="0ae1f-118">int</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-119">Principal</span><span class="sxs-lookup"><span data-stu-id="0ae1f-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-120">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-120">ID number to identify the session.</span></span> <span data-ttu-id="0ae1f-121">Utilisé conjointement avec <strong>SessionIdTime</strong> pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="0ae1f-122">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ae1f-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae1f-123"><strong>FromNumberId</strong></span><span class="sxs-lookup"><span data-stu-id="0ae1f-123"><strong>FromNumberId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae1f-124">int</span><span class="sxs-lookup"><span data-stu-id="0ae1f-124">int</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-125">Externes</span><span class="sxs-lookup"><span data-stu-id="0ae1f-125">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-126"><strong>PhoneId</strong> de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-126"><strong>PhoneId</strong> of the caller.</span></span> <span data-ttu-id="0ae1f-127">Pour plus d’informations, voir la <a href="lync-server-2013-phones-table.md">table téléphones dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ae1f-127">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="0ae1f-128">Si ce n’est pas nul et que <strong>FromGatewayId</strong> n’est pas null, l’appelant était un utilisateur PSTN.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-128">If not NULL and <strong>FromGatewayId</strong> is not NULL, then the caller was a PSTN user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae1f-129"><strong>ConnectedNumberId</strong></span><span class="sxs-lookup"><span data-stu-id="0ae1f-129"><strong>ConnectedNumberId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae1f-130">int</span><span class="sxs-lookup"><span data-stu-id="0ae1f-130">int</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-131">Externes</span><span class="sxs-lookup"><span data-stu-id="0ae1f-131">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-132"><strong>PhoneId</strong> du destinataire de l’appel.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-132"><strong>PhoneId</strong> of the call receiver.</span></span> <span data-ttu-id="0ae1f-133">Pour plus d’informations, voir la <a href="lync-server-2013-phones-table.md">table téléphones dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ae1f-133">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="0ae1f-134">Si ce n’est pas nul et que <strong>ToGatewayId</strong> n’est pas null, le destinataire de l’appel était un utilisateur RTC.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-134">If not NULL and <strong>ToGatewayId</strong> is not NULL, then the call receiver was a PSTN user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae1f-135"><strong>FromMediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="0ae1f-135"><strong>FromMediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae1f-136">int</span><span class="sxs-lookup"><span data-stu-id="0ae1f-136">int</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-137">Externes</span><span class="sxs-lookup"><span data-stu-id="0ae1f-137">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-138">Serveur de médiation depuis lequel l’appel provient.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-138">The Mediation Server the call is coming from.</span></span> <span data-ttu-id="0ae1f-139">Pour plus d’informations, voir la <a href="lync-server-2013-mediationservers-table.md">table MediationServers dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ae1f-139">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae1f-140"><strong>ToMediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="0ae1f-140"><strong>ToMediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae1f-141">int</span><span class="sxs-lookup"><span data-stu-id="0ae1f-141">int</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-142">Externes</span><span class="sxs-lookup"><span data-stu-id="0ae1f-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-143">Le serveur de médiation appelé va.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-143">The Mediation Server called is going to.</span></span> <span data-ttu-id="0ae1f-144">Pour plus d’informations, voir la <a href="lync-server-2013-mediationservers-table.md">table MediationServers dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ae1f-144">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae1f-145"><strong>FromGatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="0ae1f-145"><strong>FromGatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae1f-146">int</span><span class="sxs-lookup"><span data-stu-id="0ae1f-146">int</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-147">Externes</span><span class="sxs-lookup"><span data-stu-id="0ae1f-147">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-148">Passerelle provenant de l’appel.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-148">Gateway the call is coming from.</span></span> <span data-ttu-id="0ae1f-149">Pour plus d’informations, voir le <a href="lync-server-2013-gateways-table.md">tableau passerelles dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ae1f-149">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae1f-150"><strong>ToGatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="0ae1f-150"><strong>ToGatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae1f-151">int</span><span class="sxs-lookup"><span data-stu-id="0ae1f-151">int</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-152">Externes</span><span class="sxs-lookup"><span data-stu-id="0ae1f-152">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-153">Passerelle de destination de l’appel.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-153">Gateway the call is going to.</span></span> <span data-ttu-id="0ae1f-154">Pour plus d’informations, voir le <a href="lync-server-2013-gateways-table.md">tableau passerelles dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ae1f-154">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ae1f-155"><strong>DisconnectedbyURIId</strong></span><span class="sxs-lookup"><span data-stu-id="0ae1f-155"><strong>DisconnectedbyURIId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae1f-156">int</span><span class="sxs-lookup"><span data-stu-id="0ae1f-156">int</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-157">Externes</span><span class="sxs-lookup"><span data-stu-id="0ae1f-157">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-158">URI de l’utilisateur qui a déconnecté l’appel, s’il possède un URI.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-158">URI of the user who disconnected the call, if the user has a URI.</span></span> <span data-ttu-id="0ae1f-159">Pour plus d’informations, consultez le <a href="lync-server-2013-users-table.md">tableau utilisateurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ae1f-159">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ae1f-160"><strong>DisconnectedbyPhoneId</strong></span><span class="sxs-lookup"><span data-stu-id="0ae1f-160"><strong>DisconnectedbyPhoneId</strong></span></span></p></td>
<td><p><span data-ttu-id="0ae1f-161">int</span><span class="sxs-lookup"><span data-stu-id="0ae1f-161">int</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-162">Externes</span><span class="sxs-lookup"><span data-stu-id="0ae1f-162">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0ae1f-163">ID du téléphone sur lequel l’appel a été déconnecté d’un téléphone.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-163">ID of the phone that disconnected the call was disconnected from a phone.</span></span> <span data-ttu-id="0ae1f-164">Pour plus d’informations, voir la <a href="lync-server-2013-phones-table.md">table téléphones dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0ae1f-164">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0ae1f-165">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0ae1f-165">


</div>

<span> </span>

</div>

</div>

</span></span></div>

