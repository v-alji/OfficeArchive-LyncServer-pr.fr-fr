---
title: 'Lync Server 2013 : Interopérabilité des clients dans Lync 2013'
description: 'Lync Server 2013 : interopérabilité client dans Lync 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Client interoperability in Lync 2013
ms:assetid: 0f126571-91a2-45d5-855c-1e4ddb45fc04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204672(v=OCS.15)
ms:contentKeyID: 48183417
ms.date: 03/04/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea6e90d9479f03dd6d946787e70a2b3cc078699
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434920"
---
# <a name="client-interoperability-in-lync-2013"></a><span data-ttu-id="37027-103">Interopérabilité des clients dans Lync 2013</span><span class="sxs-lookup"><span data-stu-id="37027-103">Client interoperability in Lync 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="37027-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="37027-104">

<span> </span></span></span>

<span data-ttu-id="37027-105">_**Dernière modification de la rubrique :** 2016-03-04_</span><span class="sxs-lookup"><span data-stu-id="37027-105">_**Topic Last Modified:** 2016-03-04_</span></span>

<span data-ttu-id="37027-106">Cette rubrique explique la possibilité pour les clients Microsoft Lync Server 2013 de cohabiter et d’interagir avec les clients provenant de versions antérieures de Lync Server et d’Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="37027-106">This topic discusses the ability of Microsoft Lync Server 2013 clients to coexist and interact with clients from earlier versions of Lync Server and Office Communications Server.</span></span>

<div>

## <a name="server-and-client-compatibility"></a><span data-ttu-id="37027-107">Compatibilité entre le serveur et le client</span><span class="sxs-lookup"><span data-stu-id="37027-107">Server and Client Compatibility</span></span>

<span data-ttu-id="37027-108">Le tableau ci-dessous indique les combinaisons prises en charge par les versions de client et serveur.</span><span class="sxs-lookup"><span data-stu-id="37027-108">The following table shows the supported combinations of client versions and server versions.</span></span> <span data-ttu-id="37027-109">Ce tableau indique si la connexion est prise en charge lorsque le client tente de se connecter au serveur indiqué.</span><span class="sxs-lookup"><span data-stu-id="37027-109">This table indicates whether sign-in is supported when the client attempts to connect to the server indicated.</span></span> <span data-ttu-id="37027-110">Lync Server 2013 prend en charge la version précédente du client.</span><span class="sxs-lookup"><span data-stu-id="37027-110">Lync Server 2013 supports the previous client version.</span></span> <span data-ttu-id="37027-111">Par ailleurs, contrairement aux versions précédentes, Lync Server 2010 prend en charge les nouveaux clients Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="37027-111">Also, unlike previous releases, Lync Server 2010 supports the new Lync 2013 clients.</span></span> <span data-ttu-id="37027-112">Cela permet aux organisations qui effectuent la mise à niveau de Lync Server 2010 de déployer de nouveaux clients indépendamment des mises à niveau de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="37027-112">This allows organizations who are upgrading from Lync Server 2010 to roll out new clients independent of Lync Server upgrades.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37027-113">Client</span><span class="sxs-lookup"><span data-stu-id="37027-113">Client</span></span></th>
<th><span data-ttu-id="37027-114">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37027-114">Lync Server 2013</span></span></th>
<th><span data-ttu-id="37027-115">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="37027-115">Lync Server 2010</span></span></th>
<th><span data-ttu-id="37027-116">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="37027-116">Office Communications Server 2007 R2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37027-117">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="37027-117">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="37027-118">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-118">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-119">Supported5</span><span class="sxs-lookup"><span data-stu-id="37027-119">Supported5</span></span></p></td>
<td><p><span data-ttu-id="37027-120">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-120">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37027-121">Lync 2013 de base</span><span class="sxs-lookup"><span data-stu-id="37027-121">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="37027-122">Pris en charge </span><span class="sxs-lookup"><span data-stu-id="37027-122">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-123">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-123">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-124">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-124">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37027-125">Lync Web App 2013</span><span class="sxs-lookup"><span data-stu-id="37027-125">Lync Web App 2013</span></span></p></td>
<td><p><span data-ttu-id="37027-126">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-126">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-127">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-127">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-128">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-128">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37027-129">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="37027-129">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="37027-130">Pris en charge </span><span class="sxs-lookup"><span data-stu-id="37027-130">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-131">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-131">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-132">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-132">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37027-133">Lync 2010 attendant</span><span class="sxs-lookup"><span data-stu-id="37027-133">Lync 2010 Attendant</span></span></p></td>
<td><p><span data-ttu-id="37027-134">Pris en charge </span><span class="sxs-lookup"><span data-stu-id="37027-134">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-135">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-135">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-136">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-136">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37027-137">Conversation de groupe Lync 2010</span><span class="sxs-lookup"><span data-stu-id="37027-137">Lync 2010 Group Chat</span></span></p></td>
<td><p><span data-ttu-id="37027-138">Supported1</span><span class="sxs-lookup"><span data-stu-id="37027-138">Supported1</span></span></p></td>
<td><p><span data-ttu-id="37027-139">Supported2</span><span class="sxs-lookup"><span data-stu-id="37027-139">Supported2</span></span></p></td>
<td><p><span data-ttu-id="37027-140">Non applicable</span><span class="sxs-lookup"><span data-stu-id="37027-140">Not Applicable</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37027-141">Lync Web App 2010</span><span class="sxs-lookup"><span data-stu-id="37027-141">Lync Web App 2010</span></span></p></td>
<td><p><span data-ttu-id="37027-142">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-142">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-143">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-143">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-144">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-144">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37027-145">Lync 2010 participant</span><span class="sxs-lookup"><span data-stu-id="37027-145">Lync 2010 Attendee</span></span></p></td>
<td><p><span data-ttu-id="37027-146">Non Supported3</span><span class="sxs-lookup"><span data-stu-id="37027-146">Not Supported3</span></span></p></td>
<td><p><span data-ttu-id="37027-147">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-147">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-148">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-148">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37027-149">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="37027-149">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="37027-150">Interoperable4</span><span class="sxs-lookup"><span data-stu-id="37027-150">Interoperable4</span></span></p></td>
<td><p><span data-ttu-id="37027-151">Pris en charge </span><span class="sxs-lookup"><span data-stu-id="37027-151">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-152">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-152">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37027-153">Microsoft Office Communications Server 2007 R2 attendant</span><span class="sxs-lookup"><span data-stu-id="37027-153">Microsoft Office Communications Server 2007 R2 Attendant</span></span></p></td>
<td><p><span data-ttu-id="37027-154">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-154">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-155">Pris en charge </span><span class="sxs-lookup"><span data-stu-id="37027-155">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-156">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-156">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37027-157">Office Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="37027-157">Office Communicator 2007</span></span></p></td>
<td><p><span data-ttu-id="37027-158">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-158">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-159">Pris en charge </span><span class="sxs-lookup"><span data-stu-id="37027-159">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-160">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-160">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37027-161">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="37027-161">Office Live Meeting 2007</span></span></p></td>
<td><p><span data-ttu-id="37027-162">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-162">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-163">Pris en charge </span><span class="sxs-lookup"><span data-stu-id="37027-163">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-164">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-164">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37027-165">application Lync du Windows Store</span><span class="sxs-lookup"><span data-stu-id="37027-165">Lync Windows Store app</span></span></p></td>
<td><p><span data-ttu-id="37027-166">Pris en charge </span><span class="sxs-lookup"><span data-stu-id="37027-166">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-167">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-167">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-168">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-168">Not Supported</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="37027-169">1Pour plus d’informations, reportez-vous à la section [migration de Lync server 2010, discussion de groupe ou Office Communications Server 2007 R2 en conversation de groupe vers Lync server 2013, serveur de conversation persistant](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="37027-169">1For details, see [Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md).</span></span>

<span data-ttu-id="37027-170">2In Microsoft Lync Server 2010, les fonctionnalités de discussion de groupe étaient disponibles avec le serveur de discussion de groupe, une application de confiance tierce pour Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="37027-170">2In Microsoft Lync Server 2010, group chat functionality was available with Group Chat Server, a third-party trusted application for Lync Server 2010.</span></span> <span data-ttu-id="37027-171">Les clients 2013 Lync ne sont pas compatibles avec Lync Server 2010 et la discussion de groupe.</span><span class="sxs-lookup"><span data-stu-id="37027-171">Lync 2013 clients are not compatible with Lync Server 2010, Group Chat.</span></span>

<span data-ttu-id="37027-172">3Lync Web App 2013 offre désormais une prise en compte complète de la réunion, y compris le son et la vidéo de l’ordinateur, et est considérée comme un élément de remplacement de Lync 2010 Attendee.</span><span class="sxs-lookup"><span data-stu-id="37027-172">3Lync Web App 2013 now provides a full in-meeting experience, including computer audio and video, and is considered the replacement for Lync 2010 Attendee.</span></span> <span data-ttu-id="37027-173">Lync 2010 Attendee se connecte à Lync Server 2013 uniquement si vous utilisez un navigateur non pris en charge (Internet Explorer 6 ou Internet Explorer 7) et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="37027-173">Lync 2010 Attendee will connect to Lync Server 2013 only when you are using an unsupported browser (Internet Explorer 6 or Internet Explorer 7) and Windows XP.</span></span>

<span data-ttu-id="37027-174">4Synthèse les fonctionnalités de présence et de messagerie instantanée d’Office Communicator 2007 R2 sont compatibles avec Lync Server 2013, mais pas les fonctionnalités de conférence.</span><span class="sxs-lookup"><span data-stu-id="37027-174">4The presence and IM features in Office Communicator 2007 R2 are compatible with Lync Server 2013, but conferencing features are not.</span></span> <span data-ttu-id="37027-175">Lors de la migration à partir d’Office Communications Server 2007 R2, Office Communicator 2007 R2 est approprié pour l’interopérabilité de la présence et de la messagerie instantanée, mais les utilisateurs doivent utiliser Lync Web App 2013 pour participer aux réunions Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="37027-175">During migration from Office Communications Server 2007 R2, Office Communicator 2007 R2 is suitable for presence and IM interoperability, but users should use Lync Web App 2013 to join Lync Server 2013 meetings.</span></span>

<span data-ttu-id="37027-176">5 pour plus d’limitations, voir la section « assistance technique pour les clients Lync 2013 dans les réunions Lync Server 2010 » plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="37027-176">5 For limitations, see "Conferencing Feature Support for Lync 2013 Clients in Lync Server 2010 Meetings" later in this topic.</span></span>

</div>

<div>

## <a name="interoperability-among-clients"></a><span data-ttu-id="37027-177">Interopérabilité entre les clients</span><span class="sxs-lookup"><span data-stu-id="37027-177">Interoperability among Clients</span></span>

<span data-ttu-id="37027-178">Avec la version 2013 du serveur Lync, les différentes versions du client peuvent interagir en toute transparence dans les scénarios d’égal à égal et de conférence.</span><span class="sxs-lookup"><span data-stu-id="37027-178">With the Lync Server 2013 release, various client versions can interact seamlessly in both peer-to-peer and conferencing scenarios.</span></span> <span data-ttu-id="37027-179">Cette section traite de la disponibilité des fonctionnalités lorsque les utilisateurs interagissent avec d’autres utilisateurs qui utilisent des versions différentes de clients et de serveurs.</span><span class="sxs-lookup"><span data-stu-id="37027-179">This section discusses feature availability when users interact with other users who are using different versions of clients and servers.</span></span>

<div>

## <a name="peer-to-peer-feature-support"></a><span data-ttu-id="37027-180">Prise en charge des fonctionnalités d’égal à égal</span><span class="sxs-lookup"><span data-stu-id="37027-180">Peer-to-Peer Feature Support</span></span>

<span data-ttu-id="37027-181">Les fonctionnalités d’égal à égal sont prises en charge pour les utilisateurs hébergés sur des versions différentes du serveur et utilisant des versions de clients différentes.</span><span class="sxs-lookup"><span data-stu-id="37027-181">Peer-to-peer features are supported for users who are homed on different versions of the server and who are using different client versions.</span></span> <span data-ttu-id="37027-182">L’utilisation des fonctionnalités finales et des fonctionnalités disponibles est cohérente avec les fonctionnalités du client de l’utilisateur et celle du serveur auquel il est connecté.</span><span class="sxs-lookup"><span data-stu-id="37027-182">The end-user experience and available features are consistent with the capabilities of the user’s client and the version of the server the user is signed in to.</span></span> <span data-ttu-id="37027-183">En d’autres termes :</span><span class="sxs-lookup"><span data-stu-id="37027-183">In other words:</span></span>

  - <span data-ttu-id="37027-184">Si un utilisateur est connecté à Lync Server 2013 avec un client plus ancien, il aura la même connaissance qu’il est utilisé.</span><span class="sxs-lookup"><span data-stu-id="37027-184">If a user is signed in to Lync Server 2013 with an older client, the user will have the same experience he or she is used to.</span></span> <span data-ttu-id="37027-185">Aucune des nouvelles fonctionnalités introduites dans Lync Server 2013 ne sera disponible tant que le client de l’utilisateur n’a pas été mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="37027-185">None of the new features introduced in Lync Server 2013 will be available until the user’s client is upgraded.</span></span> <span data-ttu-id="37027-186">Il s’agit notamment de l’affichage Galerie de vidéos, de la vidéo HD, de la mise à jour du partage PowerPoint et de l’option désactiver l’audio et la vidéo des participants lors de la réunion.</span><span class="sxs-lookup"><span data-stu-id="37027-186">Examples include video gallery view, HD video, updated PowerPoint sharing, and the option to mute all attendee audio and video upon meeting entry.</span></span> <span data-ttu-id="37027-187">Les nouvelles fonctionnalités sont présentées dans les [nouvelles fonctionnalités de conférence de Lync server 2013](lync-server-2013-new-conferencing-features.md) et [les nouveautés pour les clients de Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span><span class="sxs-lookup"><span data-stu-id="37027-187">The new features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

  - <span data-ttu-id="37027-188">Si un utilisateur est connecté à Lync Server 2010 avec un client 2013 Lync, toutes les nouvelles fonctionnalités non prises en charge par Lync Server 2010 ne seront pas disponibles tant que l’utilisateur n’aura pas été déplacé vers Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="37027-188">If a user is signed in to Lync Server 2010 with a Lync 2013 client, any new features not supported by Lync Server 2010 will be unavailable until the user is moved to Lync Server 2013.</span></span>

<span data-ttu-id="37027-189">Le tableau suivant compare la disponibilité des fonctionnalités dans les sessions d’égal à égal où le client est connecté à Lync Server 2013 ou Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="37027-189">The following table compares feature availability in peer-to-peer sessions where the client is signed in to either Lync Server 2013 or Lync Server 2010.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="37027-190">Lync Web App et Lync 2010 ne sont pas des clients de réunion et ne sont pas inclus dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="37027-190">Lync Web App and Lync 2010 Attendee are meeting-only clients and aren’t included in this table.</span></span>



</div>


<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37027-191">Client</span><span class="sxs-lookup"><span data-stu-id="37027-191">Client</span></span></th>
<th><span data-ttu-id="37027-192">Messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="37027-192">Instant Messaging</span></span></th>
<th><span data-ttu-id="37027-193">Présence</span><span class="sxs-lookup"><span data-stu-id="37027-193">Presence</span></span></th>
<th><span data-ttu-id="37027-194">Voix</span><span class="sxs-lookup"><span data-stu-id="37027-194">Voice</span></span></th>
<th><span data-ttu-id="37027-195">Vidéo</span><span class="sxs-lookup"><span data-stu-id="37027-195">Video</span></span></th>
<th><span data-ttu-id="37027-196">Partage d’application</span><span class="sxs-lookup"><span data-stu-id="37027-196">Application Sharing</span></span></th>
<th><span data-ttu-id="37027-197">Transfert de fichiers</span><span class="sxs-lookup"><span data-stu-id="37027-197">File Transfer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37027-198">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="37027-198">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="37027-199">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-199">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-200">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-200">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-201">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-201">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-202">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-202">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-203">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-203">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-204">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37027-205">Lync 2013 de base</span><span class="sxs-lookup"><span data-stu-id="37027-205">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="37027-206">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-206">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-207">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-207">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-208">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-208">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-209">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-209">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-210">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-210">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-211">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-211">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37027-212">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="37027-212">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="37027-213">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-213">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-214">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-214">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-215">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-215">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-216">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-216">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-217">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-217">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-218">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-218">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37027-219">Lync 2010 attendant</span><span class="sxs-lookup"><span data-stu-id="37027-219">Lync 2010 Attendant</span></span></p></td>
<td><p><span data-ttu-id="37027-220">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-220">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-221">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-221">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-222">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-222">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37027-223">Lync 2010 mobile</span><span class="sxs-lookup"><span data-stu-id="37027-223">Lync 2010 Mobile</span></span></p></td>
<td><p><span data-ttu-id="37027-224">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-224">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-225">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-225">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37027-226">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="37027-226">Lync Phone Edition</span></span></p></td>
<td><p><span data-ttu-id="37027-227">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-227">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-228">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-228">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-229">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-229">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37027-230">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="37027-230">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="37027-231">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-231">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-232">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-232">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-233">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-233">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-234">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-234">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-235">Oui 1</span><span class="sxs-lookup"><span data-stu-id="37027-235">Yes1</span></span></p></td>
<td><p><span data-ttu-id="37027-236">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-236">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37027-237">Messagerie instantanée publique (AOL, Yahoo !)</span><span class="sxs-lookup"><span data-stu-id="37027-237">Public IM (AOL, Yahoo!)</span></span></p></td>
<td><p><span data-ttu-id="37027-238">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-238">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-239">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-239">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37027-240">Messagerie instantanée publique (MSN, Windows Live Messenger)</span><span class="sxs-lookup"><span data-stu-id="37027-240">Public IM (MSN, Windows Live Messenger)</span></span></p></td>
<td><p><span data-ttu-id="37027-241">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-241">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-242">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-242">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-243">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-243">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-244">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-244">Yes</span></span></p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="37027-245">À compter du 1er septembre 2012, la licence de l’abonnement à l’utilisateur de la connectivité PIC (Public IM Connectivity) de Microsoft Lync n’est plus disponible pour l’achat de contrats de nouveau ou de renouvellement.</span><span class="sxs-lookup"><span data-stu-id="37027-245">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (PIC USL) is no longer available for the purchase for new or renewing agreements.</span></span> <span data-ttu-id="37027-246">Les clients disposant de licences actives seront en mesure de continuer à fédérer avec Yahoo !</span><span class="sxs-lookup"><span data-stu-id="37027-246">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="37027-247">Messenger jusqu’à la date d’arrêt du service.</span><span class="sxs-lookup"><span data-stu-id="37027-247">Messenger until the service shutdown date.</span></span> <span data-ttu-id="37027-248">Date de fin de vie du 2014 juin pour AOL et Yahoo !</span><span class="sxs-lookup"><span data-stu-id="37027-248">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="37027-249">a été annoncé.</span><span class="sxs-lookup"><span data-stu-id="37027-249">has been announced.</span></span> <span data-ttu-id="37027-250">Pour plus d’informations, voir <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">prise en charge de la connectivité de messagerie instantanée publique dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="37027-250">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>..</span></span></P>
> <LI>
> <P><span data-ttu-id="37027-251">La fonction USL (PIC) est une licence d’abonnement par utilisateur et par mois requise pour la Fédération de Lync Server ou d’Office Communications Server avec Yahoo !</span><span class="sxs-lookup"><span data-stu-id="37027-251">The PIC USL is a per-user, per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="37027-252">Messenger.</span><span class="sxs-lookup"><span data-stu-id="37027-252">Messenger.</span></span> <span data-ttu-id="37027-253">La capacité de Microsoft à fournir ce service est subordonné à la prise en charge de Yahoo !, qui n’est pas renouvelé.</span><span class="sxs-lookup"><span data-stu-id="37027-253">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which will not be renewed.</span></span></P>
> <LI>
> <P><span data-ttu-id="37027-254">Plus que jamais, Lync est un outil puissant de connexion entre organisations et de personnes dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="37027-254">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="37027-255">La Fédération avec Windows Live Messenger ne nécessite aucune licence d’utilisateur/appareil supplémentaire au-delà de la CAL standard Lync.</span><span class="sxs-lookup"><span data-stu-id="37027-255">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="37027-256">Skype Federation sera ajouté à cette liste, ce qui permettra aux utilisateurs de Lync de joindre des centaines de millions de personnes par messagerie instantanée et vocale.</span><span class="sxs-lookup"><span data-stu-id="37027-256">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people through IM and voice.</span></span></P></LI></UL>



</div>

<span data-ttu-id="37027-257">1 dans Office Communicator 2007 R2, seul le partage de bureau (et non le partage de programme) est disponible.</span><span class="sxs-lookup"><span data-stu-id="37027-257">1 In Office Communicator 2007 R2, only desktop sharing (and not program sharing) is available.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="37027-258">Le partage de bureau entre Office Communicator 2007 R2 et Skype entreprise 2015 ne peut pas être démarré à partir du client plus récent lorsque l’interface utilisateur du client Skype entreprise 2015 est appliquée.</span><span class="sxs-lookup"><span data-stu-id="37027-258">Desktop sharing between Office Communicator 2007 R2 and Skype for Business 2015 cannot be initiated from the newer client when the Skype for Business 2015 client user interface is enforced.</span></span>



</div>

</div>

<div>

## <a name="conferencing-feature-support-for-lync-2013-clients-in-lync-server-2010-meetings"></a><span data-ttu-id="37027-259">Prise en charge des fonctionnalités de conférence pour les clients Lync 2013 dans les réunions Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="37027-259">Conferencing Feature Support for Lync 2013 Clients in Lync Server 2010 Meetings</span></span>

<span data-ttu-id="37027-260">Lorsque des utilisateurs rejoignent des réunions Lync Server 2010 avec un client Lync 2013, ils ont accès aux fonctionnalités du client Lync 2013 avec les exceptions suivantes :</span><span class="sxs-lookup"><span data-stu-id="37027-260">When users join Lync Server 2010 meetings with a Lync 2013 client, they have access to Lync 2013 client features with the following exceptions:</span></span>

  - <span data-ttu-id="37027-261">Dans les options de gestion des **participants** accessibles en pointant sur l’icône personnes dans la fenêtre de la réunion, l’option **aucun message instantané** ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="37027-261">In the **Participants** management options, which are accessible by pointing to the people icon in the meeting window, the **No Meeting IM** option does not function.</span></span>

  - <span data-ttu-id="37027-262">Le mode Galerie ne fonctionne pas dans les conférences vidéo.</span><span class="sxs-lookup"><span data-stu-id="37027-262">Gallery View does not function in video conferences.</span></span> <span data-ttu-id="37027-263">L’utilisateur ne voit que le haut-parleur actif au lieu de ses haut-parleurs.</span><span class="sxs-lookup"><span data-stu-id="37027-263">The user sees only the active speaker instead of all speakers.</span></span> <span data-ttu-id="37027-264">Dans la liste des options **choisir une disposition, la** **vue Galerie** n’est pas disponible</span><span class="sxs-lookup"><span data-stu-id="37027-264">In the list of **Pick a Layout** options, **Gallery View** is unavailable</span></span>

  - <span data-ttu-id="37027-265">La liste des participants s’affiche par défaut dans les conférences vidéo.</span><span class="sxs-lookup"><span data-stu-id="37027-265">The participant list displays by default in video conferences.</span></span>

  - <span data-ttu-id="37027-266">Lorsque vous cliquez avec le bouton droit sur un utilisateur dans la liste des participants, les options **verrouiller les actualités vidéo** et **épingler aux participants à la Galerie** ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="37027-266">When right-clicking a user in the participants list, the **Lock the Video Spotlight** and **Pin to Gallery** participant management options are unavailable.</span></span>

</div>

<div>

## <a name="conferencing-feature-support-in-lync-server-2013-meetings"></a><span data-ttu-id="37027-267">Prise en charge des fonctionnalités de conférence dans les réunions Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37027-267">Conferencing Feature Support in Lync Server 2013 Meetings</span></span>

<span data-ttu-id="37027-268">Lync Server 2013 fournit de nouvelles fonctionnalités de conférence qui deviennent accessibles aux utilisateurs une fois leur compte déplacé vers Lync Server 2013 et se connectant avec le client Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="37027-268">Lync Server 2013 provides new conferencing features that become available to users after their accounts are moved to Lync Server 2013 and they sign in with the Lync 2013 client.</span></span> <span data-ttu-id="37027-269">Il s’agit notamment de l’affichage Galerie de vidéos, de la vidéo HD, du partage PowerPoint et de l’option désactiver l’audio et la vidéo des participants à la réunion.</span><span class="sxs-lookup"><span data-stu-id="37027-269">Examples include video gallery view, HD video, PowerPoint sharing, and the option to mute all attendee audio and video upon meeting entry.</span></span> <span data-ttu-id="37027-270">Les nouvelles fonctionnalités sont présentées dans les [nouvelles fonctionnalités de conférence de Lync server 2013](lync-server-2013-new-conferencing-features.md) et [les nouveautés pour les clients de Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span><span class="sxs-lookup"><span data-stu-id="37027-270">The new features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="37027-271">Dans les réunions Lync Server 2013, certaines fonctions de conférence sont prises en charge pour les utilisateurs qui sont hébergés sur des versions différentes du serveur et qui utilisent des clients et des versions de clients différents.</span><span class="sxs-lookup"><span data-stu-id="37027-271">In Lync Server 2013 meetings, certain conferencing features are supported for users who are homed on different versions of the server and who are using different clients and client versions.</span></span> <span data-ttu-id="37027-272">Lorsque des clients rejoignent une réunion Lync Server 2013, les utilisateurs ont accès aux fonctionnalités et fonctionnalités présentées dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="37027-272">When clients join a Lync Server 2013 meeting, users have access to the features and capabilities shown in this table.</span></span>


<table style="width:100%;">
<colgroup>
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37027-273">Client</span><span class="sxs-lookup"><span data-stu-id="37027-273">Client</span></span></th>
<th><span data-ttu-id="37027-274">Messagerie instantanée d’égal à égal</span><span class="sxs-lookup"><span data-stu-id="37027-274">Peer-to-peer IM</span></span></th>
<th><span data-ttu-id="37027-275">Voix</span><span class="sxs-lookup"><span data-stu-id="37027-275">Voice</span></span></th>
<th><span data-ttu-id="37027-276">Vidéo</span><span class="sxs-lookup"><span data-stu-id="37027-276">Video</span></span></th>
<th><span data-ttu-id="37027-277">Partage d’application</span><span class="sxs-lookup"><span data-stu-id="37027-277">Application Sharing</span></span></th>
<th><span data-ttu-id="37027-278">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="37027-278">PowerPoint</span></span></th>
<th><span data-ttu-id="37027-279">Transfert de fichiers</span><span class="sxs-lookup"><span data-stu-id="37027-279">File Transfer</span></span></th>
<th><span data-ttu-id="37027-280">Tableau blanc</span><span class="sxs-lookup"><span data-stu-id="37027-280">Whiteboard</span></span></th>
<th><span data-ttu-id="37027-281">Interrogation</span><span class="sxs-lookup"><span data-stu-id="37027-281">Polling</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37027-282">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="37027-282">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="37027-283">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-283">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-284">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-284">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-285">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-285">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-286">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-286">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-287">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-287">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-288">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-288">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-289">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-289">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-290">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-290">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37027-291">Lync 2013 de base</span><span class="sxs-lookup"><span data-stu-id="37027-291">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="37027-292">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-292">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-293">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-293">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-294">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-294">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-295">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-295">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-296">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-296">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-297">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-297">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-298">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-298">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-299">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-299">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37027-300">Lync Web App</span><span class="sxs-lookup"><span data-stu-id="37027-300">Lync Web App</span></span></p></td>
<td><p><span data-ttu-id="37027-301">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-301">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-302">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-302">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-303">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-303">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-304">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-304">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-305">Oui2</span><span class="sxs-lookup"><span data-stu-id="37027-305">Yes2</span></span></p></td>
<td><p><span data-ttu-id="37027-306">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-306">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-307">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-307">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-308">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-308">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37027-309">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="37027-309">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="37027-310">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-310">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-311">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-311">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-312">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-312">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-313">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-313">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-314">Oui3</span><span class="sxs-lookup"><span data-stu-id="37027-314">Yes3</span></span></p></td>
<td><p><span data-ttu-id="37027-315">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-315">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-316">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-316">Yes</span></span></p></td>
<td><p><span data-ttu-id="37027-317">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-317">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37027-318">Office Communicator 2007 R2 4</span><span class="sxs-lookup"><span data-stu-id="37027-318">Office Communicator 2007 R2 4</span></span></p></td>
<td><p><span data-ttu-id="37027-319">Oui</span><span class="sxs-lookup"><span data-stu-id="37027-319">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="37027-320">1 dans Office Communicator 2007 R2, seul le partage de bureau (et non le partage de programme) est disponible.</span><span class="sxs-lookup"><span data-stu-id="37027-320">1 In Office Communicator 2007 R2, only desktop sharing (and not program sharing) is available.</span></span>

<span data-ttu-id="37027-321">2 Lync Server 2013 utilise un mécanisme de mise à jour pour télécharger des fichiers PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="37027-321">2 Lync Server 2013 uses an updated mechanism for uploading PowerPoint files.</span></span> <span data-ttu-id="37027-322">Les utilisateurs Lync Web App qui rejoignent une réunion planifiée à l’origine sur Lync Server 2010 peuvent afficher et parcourir les présentations PowerPoint, mais ne peuvent pas télécharger de fichiers PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="37027-322">Lync Web App users who join a meeting that was originally scheduled on Lync Server 2010 can view and navigate PowerPoint presentations, but cannot upload PowerPoint files.</span></span>

<span data-ttu-id="37027-323">3 Si la réunion a été planifiée sur Lync Server 2013 et les diapositives PowerPoint téléchargées par un client 2013 Lync, les utilisateurs de Lync 2010 disposent d’un accès en affichage seul aux diapositives.</span><span class="sxs-lookup"><span data-stu-id="37027-323">3 If the meeting was scheduled on Lync Server 2013 and PowerPoint slides were uploaded by a Lync 2013 client, Lync 2010 users have view-only access to the slides.</span></span> <span data-ttu-id="37027-324">À l’inverse, si les diapositives PowerPoint sont téléchargées par un utilisateur de Lync 2010, les utilisateurs de Lync Server 2013 pourront afficher et des diapositives et, si Office Web Apps Server est configuré, accéder aux nouvelles fonctionnalités, telles que l’affichage d’une résolution supérieure, des animations, des transitions entre les diapositives et la vidéo incorporée.</span><span class="sxs-lookup"><span data-stu-id="37027-324">Conversely, if the PowerPoint slides were uploaded by a Lync 2010 user, Lync Server 2013 users will be able to view and slides and, if Office Web Apps Server is configured, access new capabilities such as higher resolution display, animations, slide transitions, and embedded video.</span></span> <span data-ttu-id="37027-325">Pour plus d’informations, reportez-vous à la rubrique [configuration de l’intégration avec Office Web Apps Server et Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="37027-325">For more information, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

<span data-ttu-id="37027-326">4Synthèse les fonctionnalités de présence et de messagerie instantanée d’Office Communicator 2007 R2 sont compatibles avec Lync Server 2013, mais pas les fonctionnalités de conférence.</span><span class="sxs-lookup"><span data-stu-id="37027-326">4The presence and IM features in Office Communicator 2007 R2 are compatible with Lync Server 2013, but conferencing features are not.</span></span> <span data-ttu-id="37027-327">Lors de la migration à partir d’Office Communications Server 2007 R2, Office Communicator 2007 R2 est approprié pour l’interopérabilité de la présence et de la messagerie instantanée, mais les utilisateurs doivent utiliser Lync Web App 2013 pour participer aux réunions Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="37027-327">During migration from Office Communications Server 2007 R2, Office Communicator 2007 R2 is suitable for presence and IM interoperability, but users should use Lync Web App 2013 to join Lync Server 2013 meetings.</span></span>

</div>

</div>

<div>

## <a name="scheduling-add-in-support"></a><span data-ttu-id="37027-328">Planification de la prise en charge des compléments</span><span class="sxs-lookup"><span data-stu-id="37027-328">Scheduling Add-in Support</span></span>

<span data-ttu-id="37027-329">La prise en charge du serveur pour les divers compléments de planification est cohérente avec la compatibilité entre les versions serveur et client.</span><span class="sxs-lookup"><span data-stu-id="37027-329">Server support for the various scheduling add-ins is consistent with server and client version compatibility.</span></span> <span data-ttu-id="37027-330">En général, les compléments de planification suivants sont pris en charge sur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="37027-330">In general, the following scheduling add-ins are supported on Lync Server 2013.</span></span> <span data-ttu-id="37027-331">Toutefois, les versions précédentes des compléments ne fournissent pas de nouvelles fonctionnalités de complément Lync 2013, comme l’option permettant de désactiver l’audio et la vidéo de tous les participants lors de la réunion.</span><span class="sxs-lookup"><span data-stu-id="37027-331">However, previous versions of add-ins do not provide new Lync 2013 add-in features, such as the option to mute all attendee audio and video upon meeting entry.</span></span>

  - <span data-ttu-id="37027-332">**Complément réunion en ligne pour Lync 2013**   Fournit les mêmes fonctionnalités que le complément réunion en ligne pour Lync 2010, ainsi que les contrôles de désactivation des participants, qui permettent aux organisateurs de la réunion de programmer des conférences dont l’audio ou la vidéo est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="37027-332">**Online Meeting Add-in for Lync 2013**   Provides the same features as the Online Meeting Add-in for Lync 2010, with the addition of attendee mute controls, which allow meeting organizers to schedule conferences that have attendee audio and video muted by default.</span></span> <span data-ttu-id="37027-333">Les administrateurs peuvent également personnaliser les invitations aux réunions de l’organisation en ajoutant un logo personnalisé, une URL d’assistance, une URL d’exclusion de responsabilité ou un texte de pied de page personnalisé.</span><span class="sxs-lookup"><span data-stu-id="37027-333">Administrators can also customize the organization’s meeting invitations by adding a custom logo, a support URL, a legal disclaimer URL, or custom footer text.</span></span>

  - <span data-ttu-id="37027-334">**Complément réunion en ligne pour Lync 2010**   Permet de planifier des réunions Lync et de supprimer la possibilité de planifier des conférences Office Live Meeting.</span><span class="sxs-lookup"><span data-stu-id="37027-334">**Online Meeting Add-in for Lync 2010**   Provides scheduling for Lync meetings and removes the capability to schedule Office Live Meeting conferences.</span></span>

  - <span data-ttu-id="37027-335">**Complément de conférence Office communicator 2007 R2**   Fournit une planification pour les conférences Office Live Meeting et les conférences Office Communicator 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="37027-335">**Office Communicator 2007 R2 Conferencing Add-in**   Provides scheduling for both Office Live Meeting conferences and Office Communicator 2007 R2 conferences.</span></span> 

<div>


> [!NOTE]  
> <span data-ttu-id="37027-336">Les conférences Live Meeting ne peuvent pas être planifiées sur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="37027-336">Live Meeting conferences cannot be scheduled on Lync Server 2013.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37027-337">Client de planification</span><span class="sxs-lookup"><span data-stu-id="37027-337">Scheduling Client</span></span></th>
<th><span data-ttu-id="37027-338">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37027-338">Lync Server 2013</span></span></th>
<th><span data-ttu-id="37027-339">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="37027-339">Lync Server 2010</span></span></th>
<th><span data-ttu-id="37027-340">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="37027-340">Office Communications Server 2007 R2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37027-341">Complément réunion en ligne pour Lync 2013 (peut être utilisé avec Office 2013, Outlook 2010 et Outlook 2007)</span><span class="sxs-lookup"><span data-stu-id="37027-341">Online Meeting Add-in for Lync 2013 (can be used with Office 2013, Outlook 2010, and Outlook 2007)</span></span></p></td>
<td><p><span data-ttu-id="37027-342">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-342">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-343">Pris en charge (les nouvelles fonctionnalités des compléments ne sont pas disponibles)</span><span class="sxs-lookup"><span data-stu-id="37027-343">Supported (new add-in features not available)</span></span></p></td>
<td><p><span data-ttu-id="37027-344">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-344">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37027-345">Lync 2013 Web Scheduler</span><span class="sxs-lookup"><span data-stu-id="37027-345">Lync 2013 Web Scheduler</span></span></p></td>
<td><p><span data-ttu-id="37027-346">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-346">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-347">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-347">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-348">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-348">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37027-349">Complément réunion en ligne pour Lync 2010</span><span class="sxs-lookup"><span data-stu-id="37027-349">Online Meeting Add-in for Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="37027-350">Pris en charge </span><span class="sxs-lookup"><span data-stu-id="37027-350">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-351">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-351">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-352">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-352">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37027-353">Complément de conférence Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="37027-353">Office Communicator 2007 R2 Conferencing Add-in</span></span></p></td>
<td><p><span data-ttu-id="37027-354">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-354">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-355">Pris en charge </span><span class="sxs-lookup"><span data-stu-id="37027-355">Supported</span></span></p></td>
<td><p><span data-ttu-id="37027-356">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="37027-356">Supported</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="support-for-joining-meetings"></a><span data-ttu-id="37027-357">Prise en charge de la participation aux réunions</span><span class="sxs-lookup"><span data-stu-id="37027-357">Support for Joining Meetings</span></span>

<span data-ttu-id="37027-358">Tous les clients pris en charge par Lync Server 2013 sont autorisés à participer à des réunions Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="37027-358">All of the clients that Lync Server 2013 supports are allowed to join Lync 2013 meetings.</span></span> <span data-ttu-id="37027-359">Comme Lync Web App est un composant Web du serveur, dans les cas où Lync Web App est utilisé pour participer à une réunion Lync Server 2013, la version la plus récente de Lync Web App est toujours utilisée.</span><span class="sxs-lookup"><span data-stu-id="37027-359">Because Lync Web App is a web component of the server, in cases where Lync Web App is used to join a Lync Server 2013 meeting, the newer version of Lync Web App is always used.</span></span>

<span data-ttu-id="37027-360">Les clients 2013 Lync peuvent rejoindre des réunions hébergées sur Lync 2010 et Office Communications Server 2007 R2 avec des fonctionnalités mises à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="37027-360">Lync 2013 clients can join meetings hosted on Lync 2010 and Office Communications Server 2007 R2 with scaled-down functionality.</span></span> <span data-ttu-id="37027-361">Les fonctionnalités en réunion sont limitées par la version du serveur sur lequel la réunion est hébergée.</span><span class="sxs-lookup"><span data-stu-id="37027-361">In-meeting features are limited by the version of the server on which the meeting is hosted.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="37027-362">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37027-362">See Also</span></span>


[<span data-ttu-id="37027-363">Configuration requise pour l’application Lync du Windows Store pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37027-363">Lync Windows Store app requirements for Lync Server 2013</span></span>](lync-server-2013-lync-windows-store-app-requirements.md)  
[<span data-ttu-id="37027-364">Nouvelles fonctionnalités de conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37027-364">New conferencing features in Lync Server 2013</span></span>](lync-server-2013-new-conferencing-features.md)  
[<span data-ttu-id="37027-365">Nouveautés pour les clients dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37027-365">What's new for clients in Lync Server 2013</span></span>](lync-server-2013-what-s-new-for-clients.md)  
  

<span data-ttu-id="37027-366"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="37027-366"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

