---
title: 'Lync Server 2013 : Table Registration'
description: 'Lync Server 2013 : table d’inscriptions.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Registration table
ms:assetid: 05ff9dd3-1aaa-4af0-bd69-8789fb8eaeb3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398114(v=OCS.15)
ms:contentKeyID: 48183298
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 806e1a4e944c9bc04ebdd167c41c80a57fde3f29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436565"
---
# <a name="registration-table-in-lync-server-2013"></a><span data-ttu-id="1276e-103">Table Registration dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1276e-103">Registration table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1276e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1276e-104">

<span> </span></span></span>

<span data-ttu-id="1276e-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="1276e-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="1276e-106">Chaque enregistrement représente un événement d’inscription utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1276e-106">Each record represents one user registration event.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-107">Colonne</span><span class="sxs-lookup"><span data-stu-id="1276e-107">Column</span></span></th>
<th><span data-ttu-id="1276e-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="1276e-108">Data Type</span></span></th>
<th><span data-ttu-id="1276e-109">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="1276e-109">Key/Index</span></span></th>
<th><span data-ttu-id="1276e-110">Détails</span><span class="sxs-lookup"><span data-stu-id="1276e-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1276e-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-112">DateHeure</span><span class="sxs-lookup"><span data-stu-id="1276e-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="1276e-113">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="1276e-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="1276e-114">Durée de la demande de session.</span><span class="sxs-lookup"><span data-stu-id="1276e-114">Time of session request.</span></span> <span data-ttu-id="1276e-115">Utilisé conjointement avec <strong>SessionIdSeq</strong> pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="1276e-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="1276e-116">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="1276e-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1276e-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-118">int</span><span class="sxs-lookup"><span data-stu-id="1276e-118">int</span></span></p></td>
<td><p><span data-ttu-id="1276e-119">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="1276e-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="1276e-120">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="1276e-120">ID number to identify the session.</span></span> <span data-ttu-id="1276e-121">Utilisé conjointement avec <strong>SessionIdTime</strong> pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="1276e-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="1276e-122">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="1276e-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1276e-123"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-123"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-124">int</span><span class="sxs-lookup"><span data-stu-id="1276e-124">int</span></span></p></td>
<td><p><span data-ttu-id="1276e-125">Externes</span><span class="sxs-lookup"><span data-stu-id="1276e-125">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1276e-126">IDENTIFIant de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1276e-126">The user ID.</span></span> <span data-ttu-id="1276e-127">Pour plus d’informations, consultez le <a href="lync-server-2013-users-table.md">tableau utilisateurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="1276e-127">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1276e-128"><strong>EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-128"><strong>EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-129">identificateur</span><span class="sxs-lookup"><span data-stu-id="1276e-129">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1276e-130">GUID permettant d’identifier un point de terminaison d’inscription.</span><span class="sxs-lookup"><span data-stu-id="1276e-130">A GUID to identify a registration endpoint.</span></span> <span data-ttu-id="1276e-131">En règle générale, l’événement Register sur le même ordinateur que le même utilisateur aura le même ID de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1276e-131">Usually the register event from the same computer of the same user will have the same endpoint ID.</span></span> <span data-ttu-id="1276e-132">Différents ordinateurs ont un ID de point de terminaison différent.</span><span class="sxs-lookup"><span data-stu-id="1276e-132">Different machines have a different endpoint ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1276e-133"><strong>EndpointEra</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-133"><strong>EndpointEra</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-134">Identificateur</span><span class="sxs-lookup"><span data-stu-id="1276e-134">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1276e-135">ID utilisé pour différencier les inscriptions qui impliquent le même utilisateur et le même point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1276e-135">ID used to differentiate registrations that involve the same user and the same endpoint.</span></span></p>
<p><span data-ttu-id="1276e-136">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1276e-136">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1276e-137"><strong>ClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-137"><strong>ClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-138">int</span><span class="sxs-lookup"><span data-stu-id="1276e-138">int</span></span></p></td>
<td><p><span data-ttu-id="1276e-139">Externes</span><span class="sxs-lookup"><span data-stu-id="1276e-139">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1276e-140">Version du client de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="1276e-140">Client version of current user.</span></span> <span data-ttu-id="1276e-141">Pour plus d’informations, voir la <a href="lync-server-2013-clientversions-table.md">table ClientVersions dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="1276e-141">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1276e-142"><strong>RegistrarId</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-142"><strong>RegistrarId</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-143">int</span><span class="sxs-lookup"><span data-stu-id="1276e-143">int</span></span></p></td>
<td><p><span data-ttu-id="1276e-144">Externes</span><span class="sxs-lookup"><span data-stu-id="1276e-144">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1276e-145">ID du serveur d’inscriptions utilisé pour l’inscription.</span><span class="sxs-lookup"><span data-stu-id="1276e-145">ID of the Registrar Server used for registration.</span></span> <span data-ttu-id="1276e-146">Pour plus d’informations, voir le <a href="lync-server-2013-servers-table.md">tableau des serveurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="1276e-146">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1276e-147"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-147"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-148">int</span><span class="sxs-lookup"><span data-stu-id="1276e-148">int</span></span></p></td>
<td><p><span data-ttu-id="1276e-149">Externes</span><span class="sxs-lookup"><span data-stu-id="1276e-149">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1276e-150">ID du pool dans lequel la session a été capturée.</span><span class="sxs-lookup"><span data-stu-id="1276e-150">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="1276e-151">Pour plus d’informations, voir la <a href="lync-server-2013-pools-table.md">table pools dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="1276e-151">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1276e-152"><strong>EdgeServerId</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-152"><strong>EdgeServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-153">int</span><span class="sxs-lookup"><span data-stu-id="1276e-153">int</span></span></p></td>
<td><p><span data-ttu-id="1276e-154">Externes</span><span class="sxs-lookup"><span data-stu-id="1276e-154">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1276e-155">Serveur Edge le passage à l’inscription.</span><span class="sxs-lookup"><span data-stu-id="1276e-155">Edge Server the registration is going through.</span></span> <span data-ttu-id="1276e-156">Pour plus d’informations, voir la <a href="lync-server-2013-edgeservers-table.md">table EdgeServers dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="1276e-156">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1276e-157"><strong>IsInternal</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-157"><strong>IsInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-158">Résolution</span><span class="sxs-lookup"><span data-stu-id="1276e-158">Bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1276e-159">Si l’utilisateur est connecté à partir d’une connexion interne ou non.</span><span class="sxs-lookup"><span data-stu-id="1276e-159">Whether the user is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1276e-160"><strong>IsUserServiceAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-160"><strong>IsUserServiceAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-161">bit</span><span class="sxs-lookup"><span data-stu-id="1276e-161">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1276e-162">Si le UserService est disponible ou non.</span><span class="sxs-lookup"><span data-stu-id="1276e-162">Whether the UserService is available or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1276e-163"><strong>IsPrimaryRegistrar</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-163"><strong>IsPrimaryRegistrar</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-164">bit</span><span class="sxs-lookup"><span data-stu-id="1276e-164">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1276e-165">S’il est inscrit au bureau d’enregistrement principal ou non.</span><span class="sxs-lookup"><span data-stu-id="1276e-165">Whether register to the primary Registrar or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1276e-166"><strong>IsPrimaryRegistrarCentral</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-166"><strong>IsPrimaryRegistrarCentral</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-167">bit</span><span class="sxs-lookup"><span data-stu-id="1276e-167">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1276e-168">Indique si l’utilisateur est inscrit auprès d’une unité de branchement survivant.</span><span class="sxs-lookup"><span data-stu-id="1276e-168">Indicates whether or not the user is registered with a survivable branch appliance.</span></span></p>
<p><span data-ttu-id="1276e-169">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1276e-169">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1276e-170"><strong>RegisterTime</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-170"><strong>RegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-171">DateHeure</span><span class="sxs-lookup"><span data-stu-id="1276e-171">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1276e-172">Durée de l’inscription.</span><span class="sxs-lookup"><span data-stu-id="1276e-172">Registration time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1276e-173"><strong>DeRegisterTime</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-173"><strong>DeRegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-174">DateHeure</span><span class="sxs-lookup"><span data-stu-id="1276e-174">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1276e-175">De-Registration temps.</span><span class="sxs-lookup"><span data-stu-id="1276e-175">De-Registration time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1276e-176"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-176"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-177">int</span><span class="sxs-lookup"><span data-stu-id="1276e-177">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1276e-178">Code de réponse de la demande Register.</span><span class="sxs-lookup"><span data-stu-id="1276e-178">Response code of the register request.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1276e-179"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-179"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-180">int</span><span class="sxs-lookup"><span data-stu-id="1276e-180">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1276e-181">ID de diagnostic de la demande d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1276e-181">Diagnostic ID of the register request.</span></span> <span data-ttu-id="1276e-182">Ce type d’informations indique ce type d’informations de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="1276e-182">This indicates that diagnostic information type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1276e-183"><strong>DeviceId</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-183"><strong>DeviceId</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-184">int</span><span class="sxs-lookup"><span data-stu-id="1276e-184">int</span></span></p></td>
<td><p><span data-ttu-id="1276e-185">Externes</span><span class="sxs-lookup"><span data-stu-id="1276e-185">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1276e-186">L’appareil à partir duquel la requête d’enregistrement provient.</span><span class="sxs-lookup"><span data-stu-id="1276e-186">The device that the register request is coming from.</span></span> <span data-ttu-id="1276e-187">Pour plus d’informations, voir le <a href="lync-server-2013-devices-table.md">tableau des appareils dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="1276e-187">See the <a href="lync-server-2013-devices-table.md">Devices table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1276e-188"><strong>DeRegisterTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-188"><strong>DeRegisterTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-189">tinyint</span><span class="sxs-lookup"><span data-stu-id="1276e-189">tinyint</span></span></p></td>
<td><p><span data-ttu-id="1276e-190">Externes</span><span class="sxs-lookup"><span data-stu-id="1276e-190">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1276e-191">La raison de l’annulation de l’inscription, par exemple « initié par l’utilisateur », « inscription expirée », « échec du client », etc.</span><span class="sxs-lookup"><span data-stu-id="1276e-191">The reason of de-register, such as ‘user initiated’, ‘registration expired’, ‘client fail’, and more.</span></span> <span data-ttu-id="1276e-192">Pour plus d’informations, voir la <a href="lync-server-2013-deregistertype-table.md">table DeRegisterType dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="1276e-192">See the <a href="lync-server-2013-deregistertype-table.md">DeRegisterType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1276e-193"><strong>IPAddress</strong></span><span class="sxs-lookup"><span data-stu-id="1276e-193"><strong>IPAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="1276e-194">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1276e-194">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1276e-195">Adresse IP du point de terminaison avec lequel l’utilisateur a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="1276e-195">IP address of the endpoint the user registered with.</span></span> <span data-ttu-id="1276e-196">Il peut s’agir d’une adresse IPv4 ou d’une adresse IPv6.</span><span class="sxs-lookup"><span data-stu-id="1276e-196">This can be an IPv4 address or an IPv6 address.</span></span></p>
<p><span data-ttu-id="1276e-197">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1276e-197">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1276e-198">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1276e-198">


</div>

<span> </span>

</div>

</div>

</span></span></div>

