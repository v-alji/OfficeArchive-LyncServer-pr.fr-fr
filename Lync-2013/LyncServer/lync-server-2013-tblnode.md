---
title: 'Lync Server 2013 : tblNode'
description: 'Lync Server 2013 : tblNode.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblNode
ms:assetid: a31d2961-aa83-4286-a12e-15d279c95f19
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615024(v=OCS.15)
ms:contentKeyID: 48184960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0a5d630621c32cbc54501249c7a679bf4023c60
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423518"
---
# <a name="tblnode-in-lync-server-2013"></a><span data-ttu-id="40e8f-103">tblNode dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="40e8f-103">tblNode in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="40e8f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="40e8f-104">

<span> </span></span></span>

<span data-ttu-id="40e8f-105">_**Dernière modification de la rubrique :** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="40e8f-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="40e8f-106">tblNode contient l’arborescence d’objets (avec des nœuds de catégorie ou de salle de conversation) qui est gérée dans le panneau de configuration et les applets de commande d’administration de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="40e8f-106">tblNode contains the object tree (with category or chat room nodes) as managed in the Lync Server 2013 Control Panel and administrative cmdlets.</span></span>

### <a name="columns"></a><span data-ttu-id="40e8f-107">Celles</span><span class="sxs-lookup"><span data-stu-id="40e8f-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40e8f-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="40e8f-108">Column</span></span></th>
<th><span data-ttu-id="40e8f-109">Type</span><span class="sxs-lookup"><span data-stu-id="40e8f-109">Type</span></span></th>
<th><span data-ttu-id="40e8f-110">Description</span><span class="sxs-lookup"><span data-stu-id="40e8f-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40e8f-111">ID</span><span class="sxs-lookup"><span data-stu-id="40e8f-111">nodeID</span></span></p></td>
<td><p><span data-ttu-id="40e8f-112">ent, non null</span><span class="sxs-lookup"><span data-stu-id="40e8f-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="40e8f-113">ID de nœud (numéro unique).</span><span class="sxs-lookup"><span data-stu-id="40e8f-113">Node ID (unique number).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40e8f-114">nodeGuid</span><span class="sxs-lookup"><span data-stu-id="40e8f-114">nodeGuid</span></span></p></td>
<td><p><span data-ttu-id="40e8f-115">GUID, pas null</span><span class="sxs-lookup"><span data-stu-id="40e8f-115">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="40e8f-116">GUID du nœud.</span><span class="sxs-lookup"><span data-stu-id="40e8f-116">Node GUID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40e8f-117">Parent</span><span class="sxs-lookup"><span data-stu-id="40e8f-117">parentID</span></span></p></td>
<td><p><span data-ttu-id="40e8f-118">int</span><span class="sxs-lookup"><span data-stu-id="40e8f-118">int</span></span></p></td>
<td><p><span data-ttu-id="40e8f-119">ID de nœud du parent.</span><span class="sxs-lookup"><span data-stu-id="40e8f-119">Node ID of parent.</span></span> <span data-ttu-id="40e8f-120">Le nœud racine (avec l’ID 1) s’intègre également en tant que parent.</span><span class="sxs-lookup"><span data-stu-id="40e8f-120">The root node (with ID 1) includes itself as parent as well.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40e8f-121">nodeType</span><span class="sxs-lookup"><span data-stu-id="40e8f-121">nodeType</span></span></p></td>
<td><p><span data-ttu-id="40e8f-122">bit, pas null</span><span class="sxs-lookup"><span data-stu-id="40e8f-122">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="40e8f-123">True si le nœud est une catégorie.</span><span class="sxs-lookup"><span data-stu-id="40e8f-123">True if the node is a category.</span></span></p>
<p><span data-ttu-id="40e8f-124">Faux si le nœud est une salle de conversation.</span><span class="sxs-lookup"><span data-stu-id="40e8f-124">False if the node is a chat room.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40e8f-125">nodeName</span><span class="sxs-lookup"><span data-stu-id="40e8f-125">nodeName</span></span></p></td>
<td><p><span data-ttu-id="40e8f-126">nvarchar (256), pas null</span><span class="sxs-lookup"><span data-stu-id="40e8f-126">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="40e8f-127">Nom du nœud.</span><span class="sxs-lookup"><span data-stu-id="40e8f-127">Node name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40e8f-128">nodeDesc</span><span class="sxs-lookup"><span data-stu-id="40e8f-128">nodeDesc</span></span></p></td>
<td><p><span data-ttu-id="40e8f-129">nvarchar (256), pas null</span><span class="sxs-lookup"><span data-stu-id="40e8f-129">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="40e8f-130">Description du nœud.</span><span class="sxs-lookup"><span data-stu-id="40e8f-130">Node description.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40e8f-131">inviter</span><span class="sxs-lookup"><span data-stu-id="40e8f-131">invite</span></span></p></td>
<td><p><span data-ttu-id="40e8f-132">bit</span><span class="sxs-lookup"><span data-stu-id="40e8f-132">bit</span></span></p></td>
<td><p><span data-ttu-id="40e8f-133">Pour les catégories :</span><span class="sxs-lookup"><span data-stu-id="40e8f-133">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="40e8f-134">True si les invitations sont activées.</span><span class="sxs-lookup"><span data-stu-id="40e8f-134">True if invites are on.</span></span></p></li>
<li><p><span data-ttu-id="40e8f-135">Faux si les invitations sont désdésactivées.</span><span class="sxs-lookup"><span data-stu-id="40e8f-135">False if invites are off.</span></span></p></li>
</ul>
<p><span data-ttu-id="40e8f-136">Pour les salles :</span><span class="sxs-lookup"><span data-stu-id="40e8f-136">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="40e8f-137">Faux si les invitations sont désactivées (ignore la catégorie parent).</span><span class="sxs-lookup"><span data-stu-id="40e8f-137">False if invites are off (overrides the parent category).</span></span></p></li>
<li><p><span data-ttu-id="40e8f-138">NULL si le paramètre d’invitations est hérité de la catégorie parent.</span><span class="sxs-lookup"><span data-stu-id="40e8f-138">Null if the invites setting is inherited from the parent category.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40e8f-139">utilisé</span><span class="sxs-lookup"><span data-stu-id="40e8f-139">logged</span></span></p></td>
<td><p><span data-ttu-id="40e8f-140">bit</span><span class="sxs-lookup"><span data-stu-id="40e8f-140">bit</span></span></p></td>
<td><p><span data-ttu-id="40e8f-141">Pour les catégories :</span><span class="sxs-lookup"><span data-stu-id="40e8f-141">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="40e8f-142">True si l’historique des conversations est activé.</span><span class="sxs-lookup"><span data-stu-id="40e8f-142">True if chat history is on.</span></span></p></li>
<li><p><span data-ttu-id="40e8f-143">Faux si l’historique des conversations est désactivé.</span><span class="sxs-lookup"><span data-stu-id="40e8f-143">False if chat history is off.</span></span></p></li>
</ul>
<p><span data-ttu-id="40e8f-144">Pour les salles :</span><span class="sxs-lookup"><span data-stu-id="40e8f-144">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="40e8f-145">Valeur.</span><span class="sxs-lookup"><span data-stu-id="40e8f-145">Null.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40e8f-146">filePost</span><span class="sxs-lookup"><span data-stu-id="40e8f-146">filePost</span></span></p></td>
<td><p><span data-ttu-id="40e8f-147">bit</span><span class="sxs-lookup"><span data-stu-id="40e8f-147">bit</span></span></p></td>
<td><p><span data-ttu-id="40e8f-148">Pour les catégories :</span><span class="sxs-lookup"><span data-stu-id="40e8f-148">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="40e8f-149">True si les téléchargements de fichiers sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="40e8f-149">True if file uploads are allowed.</span></span></p></li>
<li><p><span data-ttu-id="40e8f-150">False si les téléchargements de fichiers ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="40e8f-150">False if file uploads are disallowed.</span></span></p></li>
</ul>
<p><span data-ttu-id="40e8f-151">Pour les salles :</span><span class="sxs-lookup"><span data-stu-id="40e8f-151">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="40e8f-152">Valeur.</span><span class="sxs-lookup"><span data-stu-id="40e8f-152">Null.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40e8f-153">désactivé</span><span class="sxs-lookup"><span data-stu-id="40e8f-153">disabled</span></span></p></td>
<td><p><span data-ttu-id="40e8f-154">bit, pas null</span><span class="sxs-lookup"><span data-stu-id="40e8f-154">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="40e8f-155">True si la salle de conversation est désactivée.</span><span class="sxs-lookup"><span data-stu-id="40e8f-155">True if the chat room is disabled.</span></span> <span data-ttu-id="40e8f-156">S’applique uniquement aux salles de conversation.</span><span class="sxs-lookup"><span data-stu-id="40e8f-156">Applies only to chat rooms.</span></span> <span data-ttu-id="40e8f-157">(Faux pour les catégories.)</span><span class="sxs-lookup"><span data-stu-id="40e8f-157">(False for categories.)</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40e8f-158">fonctionnement</span><span class="sxs-lookup"><span data-stu-id="40e8f-158">behavior</span></span></p></td>
<td><p><span data-ttu-id="40e8f-159">smallint, pas null</span><span class="sxs-lookup"><span data-stu-id="40e8f-159">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="40e8f-160">Comportement (recherché dans la table EnumValue) :</span><span class="sxs-lookup"><span data-stu-id="40e8f-160">Behavior (looked up in EnumValue table):</span></span></p>
<ul>
<li><p><span data-ttu-id="40e8f-161">4 : normal (salles de conversation normales).</span><span class="sxs-lookup"><span data-stu-id="40e8f-161">4: Normal (normal chat rooms).</span></span></p></li>
<li><p><span data-ttu-id="40e8f-162">5 : Auditorium (salles de conversation d’Auditorium ; seuls les présentateurs peuvent collaborer).</span><span class="sxs-lookup"><span data-stu-id="40e8f-162">5: Auditorium (auditorium chat rooms, only presenters can contribute).</span></span></p></li>
</ul>
<p><span data-ttu-id="40e8f-163">S’applique uniquement aux salles de conversation.</span><span class="sxs-lookup"><span data-stu-id="40e8f-163">Applies only to chat rooms.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40e8f-164">notoriété</span><span class="sxs-lookup"><span data-stu-id="40e8f-164">visibility</span></span></p></td>
<td><p><span data-ttu-id="40e8f-165">smallint, pas null</span><span class="sxs-lookup"><span data-stu-id="40e8f-165">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="40e8f-166">Visibility (recherché sur la table EnumValue) :</span><span class="sxs-lookup"><span data-stu-id="40e8f-166">Visibility (looked up on EnumValue table):</span></span></p>
<ul>
<li><p><span data-ttu-id="40e8f-167">2 : privé</span><span class="sxs-lookup"><span data-stu-id="40e8f-167">2: Private</span></span></p></li>
<li><p><span data-ttu-id="40e8f-168">3 : étendue</span><span class="sxs-lookup"><span data-stu-id="40e8f-168">3: Scoped</span></span></p></li>
<li><p><span data-ttu-id="40e8f-169">6 : ouvrir</span><span class="sxs-lookup"><span data-stu-id="40e8f-169">6: Open</span></span></p></li>
</ul>
<p><span data-ttu-id="40e8f-170">S’applique uniquement aux salles de conversation.</span><span class="sxs-lookup"><span data-stu-id="40e8f-170">Applies only to chat rooms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40e8f-171">siopID</span><span class="sxs-lookup"><span data-stu-id="40e8f-171">siopID</span></span></p></td>
<td><p><span data-ttu-id="40e8f-172">GUID</span><span class="sxs-lookup"><span data-stu-id="40e8f-172">GUID</span></span></p></td>
<td><p><span data-ttu-id="40e8f-173">Add-In GUID si un complément est associé à cette salle de conversation.</span><span class="sxs-lookup"><span data-stu-id="40e8f-173">Add-In GUID if an add-in is associated with this chat room.</span></span> <span data-ttu-id="40e8f-174">(Les catégories n’ont pas de compléments.)</span><span class="sxs-lookup"><span data-stu-id="40e8f-174">(Categories do not have add-ins.)</span></span></p>
<p><span data-ttu-id="40e8f-175">Les informations de complément sont recherchées dans la table SiopWhiteList.</span><span class="sxs-lookup"><span data-stu-id="40e8f-175">The add-in information is looked up in SiopWhiteList table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40e8f-176">nodeAddedBy</span><span class="sxs-lookup"><span data-stu-id="40e8f-176">nodeAddedBy</span></span></p></td>
<td><p><span data-ttu-id="40e8f-177">ent, non null</span><span class="sxs-lookup"><span data-stu-id="40e8f-177">int, not null</span></span></p></td>
<td><p><span data-ttu-id="40e8f-178">ID de l’élément principal qui a créé ce nœud.</span><span class="sxs-lookup"><span data-stu-id="40e8f-178">ID of the principal that created this node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40e8f-179">nodeAddedOn</span><span class="sxs-lookup"><span data-stu-id="40e8f-179">nodeAddedOn</span></span></p></td>
<td><p><span data-ttu-id="40e8f-180">bigint, pas null</span><span class="sxs-lookup"><span data-stu-id="40e8f-180">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="40e8f-181">Horodatage de la création du nœud.</span><span class="sxs-lookup"><span data-stu-id="40e8f-181">Time stamp of the node creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40e8f-182">nodeUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="40e8f-182">nodeUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="40e8f-183">ent, non null</span><span class="sxs-lookup"><span data-stu-id="40e8f-183">int, not null</span></span></p></td>
<td><p><span data-ttu-id="40e8f-184">ID de l’entité de l’utilisateur qui a effectué la dernière mise à jour de ce nœud.</span><span class="sxs-lookup"><span data-stu-id="40e8f-184">ID of the principal that did the latest update of this node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40e8f-185">nodeUpdatedOn</span><span class="sxs-lookup"><span data-stu-id="40e8f-185">nodeUpdatedOn</span></span></p></td>
<td><p><span data-ttu-id="40e8f-186">bigint, pas null</span><span class="sxs-lookup"><span data-stu-id="40e8f-186">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="40e8f-187">Horodatage de la dernière mise à jour de ce nœud.</span><span class="sxs-lookup"><span data-stu-id="40e8f-187">Time stamp of the latest update of this node.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40e8f-188">purgedOn</span><span class="sxs-lookup"><span data-stu-id="40e8f-188">purgedOn</span></span></p></td>
<td><p><span data-ttu-id="40e8f-189">DateHeure</span><span class="sxs-lookup"><span data-stu-id="40e8f-189">datetime</span></span></p></td>
<td><p><span data-ttu-id="40e8f-190">Heure de la dernière opération de purge (la suppression des étendues de la table tblScopedPrincipal et des rôles de la table tblPrincipalRole) qui ont affecté ce nœud.</span><span class="sxs-lookup"><span data-stu-id="40e8f-190">Time of the latest purge operation (removal of scopes from tblScopedPrincipal table and roles from tblPrincipalRole table) that affected this node.</span></span> <span data-ttu-id="40e8f-191">Ce mode est utilisé par le mécanisme de mise à jour du cache interne du service de conversation.</span><span class="sxs-lookup"><span data-stu-id="40e8f-191">This is used by the Chat service’s internal cache update mechanism.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="40e8f-192">Permettent</span><span class="sxs-lookup"><span data-stu-id="40e8f-192">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40e8f-193">Colonne</span><span class="sxs-lookup"><span data-stu-id="40e8f-193">Column</span></span></th>
<th><span data-ttu-id="40e8f-194">Description</span><span class="sxs-lookup"><span data-stu-id="40e8f-194">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40e8f-195">ID</span><span class="sxs-lookup"><span data-stu-id="40e8f-195">nodeID</span></span></p></td>
<td><p><span data-ttu-id="40e8f-196">Clé primaire.</span><span class="sxs-lookup"><span data-stu-id="40e8f-196">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40e8f-197">fonctionnement</span><span class="sxs-lookup"><span data-stu-id="40e8f-197">behavior</span></span></p></td>
<td><p><span data-ttu-id="40e8f-198">Clé étrangère avec recherche dans la table tblEnumValue. valueID.</span><span class="sxs-lookup"><span data-stu-id="40e8f-198">Foreign key with lookup in tblEnumValue.valueID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40e8f-199">notoriété</span><span class="sxs-lookup"><span data-stu-id="40e8f-199">visibility</span></span></p></td>
<td><p><span data-ttu-id="40e8f-200">Clé étrangère avec recherche dans la table tblEnumValue. valueID.</span><span class="sxs-lookup"><span data-stu-id="40e8f-200">Foreign key with lookup in tblEnumValue.valueID table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40e8f-201">Parent</span><span class="sxs-lookup"><span data-stu-id="40e8f-201">parentID</span></span></p></td>
<td><p><span data-ttu-id="40e8f-202">Clé étrangère avec recherche dans la table tblNode. nodeID.</span><span class="sxs-lookup"><span data-stu-id="40e8f-202">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40e8f-203">siopID</span><span class="sxs-lookup"><span data-stu-id="40e8f-203">siopID</span></span></p></td>
<td><p><span data-ttu-id="40e8f-204">Clé étrangère avec recherche dans la table tblSiopWhiteList. siopId.</span><span class="sxs-lookup"><span data-stu-id="40e8f-204">Foreign key with lookup in tblSiopWhiteList.siopId table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="40e8f-205">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="40e8f-205">


</div>

<span> </span>

</div>

</div>

</span></span></div>

