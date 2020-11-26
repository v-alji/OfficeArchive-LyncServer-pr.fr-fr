---
title: 'Lync Server 2013 : tblPrincipal'
description: 'Lync Server 2013 : tblPrincipal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipal
ms:assetid: 79a24502-b4ce-41f0-8979-8caddf535338
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558667(v=OCS.15)
ms:contentKeyID: 48184571
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f07b37ac4c8ceed5c044b5c263eeee6370adfdc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444412"
---
# <a name="tblprincipal-in-lync-server-2013"></a><span data-ttu-id="d7945-103">tblPrincipal dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7945-103">tblPrincipal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d7945-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d7945-104">

<span> </span></span></span>

<span data-ttu-id="d7945-105">_**Dernière modification de la rubrique :** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="d7945-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="d7945-106">tblPrincipal contient l’ensemble des principaux, y compris des utilisateurs, des dossiers et des groupes.</span><span class="sxs-lookup"><span data-stu-id="d7945-106">tblPrincipal contains all principals, including users, folders, and groups.</span></span>

### <a name="columns"></a><span data-ttu-id="d7945-107">Celles</span><span class="sxs-lookup"><span data-stu-id="d7945-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7945-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="d7945-108">Column</span></span></th>
<th><span data-ttu-id="d7945-109">Type</span><span class="sxs-lookup"><span data-stu-id="d7945-109">Type</span></span></th>
<th><span data-ttu-id="d7945-110">Description</span><span class="sxs-lookup"><span data-stu-id="d7945-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7945-111">prinID</span><span class="sxs-lookup"><span data-stu-id="d7945-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="d7945-112">ent, non null</span><span class="sxs-lookup"><span data-stu-id="d7945-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="d7945-113">ID du principal.</span><span class="sxs-lookup"><span data-stu-id="d7945-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7945-114">prinGuid</span><span class="sxs-lookup"><span data-stu-id="d7945-114">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="d7945-115">GUID, pas null</span><span class="sxs-lookup"><span data-stu-id="d7945-115">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="d7945-116">GUID principal.</span><span class="sxs-lookup"><span data-stu-id="d7945-116">Principal GUID.</span></span> <span data-ttu-id="d7945-117">Cette opération est globalement utilisée comme clé primaire alternative, car sa signification croise l’espace des services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d7945-117">This is broadly used as an alternate primary key because its meaning crosses over into the Active Directory Domain Services space.</span></span> <span data-ttu-id="d7945-118">(Le GUID d’un principal mis en cache est égal au GUID d’objet Active Directory correspondant.)</span><span class="sxs-lookup"><span data-stu-id="d7945-118">(The GUID for a cached principal is equal to the corresponding Active Directory object GUID.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7945-119">prinUri</span><span class="sxs-lookup"><span data-stu-id="d7945-119">prinUri</span></span></p></td>
<td><p><span data-ttu-id="d7945-120">nvarchar (256), pas null</span><span class="sxs-lookup"><span data-stu-id="d7945-120">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="d7945-121">URI principal.</span><span class="sxs-lookup"><span data-stu-id="d7945-121">Principal URI.</span></span> <span data-ttu-id="d7945-122">Le schéma SIP est utilisé pour les utilisateurs et ma-GRP est utilisé pour presque tout le reste.</span><span class="sxs-lookup"><span data-stu-id="d7945-122">The SIP scheme is used for users, and ma-grp is used for almost everything else.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7945-123">prinName</span><span class="sxs-lookup"><span data-stu-id="d7945-123">prinName</span></span></p></td>
<td><p><span data-ttu-id="d7945-124">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="d7945-124">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="d7945-125">Nom usuel.</span><span class="sxs-lookup"><span data-stu-id="d7945-125">Common name.</span></span> <span data-ttu-id="d7945-126">Utilisées uniquement par les types d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d7945-126">Used only by user types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7945-127">prinDisplayName</span><span class="sxs-lookup"><span data-stu-id="d7945-127">prinDisplayName</span></span></p></td>
<td><p><span data-ttu-id="d7945-128">Nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="d7945-128">Nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="d7945-129">Nom d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d7945-129">Display name.</span></span> <span data-ttu-id="d7945-130">Utilisées uniquement par les types d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d7945-130">Used only by user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7945-131">prinCompanyName</span><span class="sxs-lookup"><span data-stu-id="d7945-131">prinCompanyName</span></span></p></td>
<td><p><span data-ttu-id="d7945-132">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="d7945-132">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="d7945-133">Nom de la société.</span><span class="sxs-lookup"><span data-stu-id="d7945-133">Company name.</span></span> <span data-ttu-id="d7945-134">Utilisées uniquement par les types d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d7945-134">Used only by user types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7945-135">prinEmail</span><span class="sxs-lookup"><span data-stu-id="d7945-135">prinEmail</span></span></p></td>
<td><p><span data-ttu-id="d7945-136">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="d7945-136">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="d7945-137">Messagerie.</span><span class="sxs-lookup"><span data-stu-id="d7945-137">Email.</span></span> <span data-ttu-id="d7945-138">Utilisées uniquement par les types d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d7945-138">Used only by user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7945-139">prinADPath</span><span class="sxs-lookup"><span data-stu-id="d7945-139">prinADPath</span></span></p></td>
<td><p><span data-ttu-id="d7945-140">nvarchar (384)</span><span class="sxs-lookup"><span data-stu-id="d7945-140">nvarchar (384)</span></span></p></td>
<td><p><span data-ttu-id="d7945-141">Nom de domaine de l’objet Active Directory dont le principal est une version mise en cache.</span><span class="sxs-lookup"><span data-stu-id="d7945-141">Domain name of the Active Directory object that the principal is a cached version of.</span></span> <span data-ttu-id="d7945-142">Il peut s’agir de valeurs NULL pour les types qui ne sont pas des objets Active Directory (par exemple, utilisateurs système).</span><span class="sxs-lookup"><span data-stu-id="d7945-142">Can be Null for types that are not Active Directory objects (such as system users).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7945-143">prinADUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d7945-143">prinADUserPrincipalName</span></span></p></td>
<td><p><span data-ttu-id="d7945-144">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="d7945-144">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="d7945-145">Nom d’utilisateur principal (UPN) de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d7945-145">User’s user principal name (UPN).</span></span> <span data-ttu-id="d7945-146">Utilisé uniquement par les types d’utilisateurs normaux.</span><span class="sxs-lookup"><span data-stu-id="d7945-146">Used only by regular user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7945-147">prinDisabled</span><span class="sxs-lookup"><span data-stu-id="d7945-147">prinDisabled</span></span></p></td>
<td><p><span data-ttu-id="d7945-148">smallint, pas null</span><span class="sxs-lookup"><span data-stu-id="d7945-148">smallint, not null</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="d7945-149">0 : le principal est actif.</span><span class="sxs-lookup"><span data-stu-id="d7945-149">0: Principal is active.</span></span></p></li>
<li><p><span data-ttu-id="d7945-150">1 : le principal est désactivé car les fonctionnalités SIP de l’utilisateur sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="d7945-150">1: Principal is disabled because user’s SIP capabilities are disabled.</span></span></p></li>
<li><p><span data-ttu-id="d7945-151">2 : le principal est supprimé, car l’objet publicitaire associé a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="d7945-151">2: Principal is deleted because associated AD object has been deleted.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7945-152">prinTypeID</span><span class="sxs-lookup"><span data-stu-id="d7945-152">prinTypeID</span></span></p></td>
<td><p><span data-ttu-id="d7945-153">smallint, pas null</span><span class="sxs-lookup"><span data-stu-id="d7945-153">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="d7945-154">Type principal (issu de la table tblPrincipalType)</span><span class="sxs-lookup"><span data-stu-id="d7945-154">Principal type (from tblPrincipalType table).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7945-155">prinPoolID</span><span class="sxs-lookup"><span data-stu-id="d7945-155">prinPoolID</span></span></p></td>
<td><p><span data-ttu-id="d7945-156">Ent</span><span class="sxs-lookup"><span data-stu-id="d7945-156">Int</span></span></p></td>
<td><p><span data-ttu-id="d7945-157">Attribution du pool Lync au principal.</span><span class="sxs-lookup"><span data-stu-id="d7945-157">Lync pool assignment for the principal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7945-158">prinPolicyID</span><span class="sxs-lookup"><span data-stu-id="d7945-158">prinPolicyID</span></span></p></td>
<td><p><span data-ttu-id="d7945-159">Ent</span><span class="sxs-lookup"><span data-stu-id="d7945-159">Int</span></span></p></td>
<td><p><span data-ttu-id="d7945-160">Valeur de la stratégie de serveur de chat permanent pour l’utilisateur, si la stratégie de type balise est présente.</span><span class="sxs-lookup"><span data-stu-id="d7945-160">Persistent Chat Server policy value for user, if tag type policy is present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7945-161">prinAddedBy</span><span class="sxs-lookup"><span data-stu-id="d7945-161">prinAddedBy</span></span></p></td>
<td><p><span data-ttu-id="d7945-162">int</span><span class="sxs-lookup"><span data-stu-id="d7945-162">int</span></span></p></td>
<td><p><span data-ttu-id="d7945-163">ID principal du créateur.</span><span class="sxs-lookup"><span data-stu-id="d7945-163">Principal ID of the creator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7945-164">prinAddedOn</span><span class="sxs-lookup"><span data-stu-id="d7945-164">prinAddedOn</span></span></p></td>
<td><p><span data-ttu-id="d7945-165">bigint, pas null</span><span class="sxs-lookup"><span data-stu-id="d7945-165">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="d7945-166">Horodatage de l’heure de création.</span><span class="sxs-lookup"><span data-stu-id="d7945-166">Time stamp for the creation time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7945-167">prinUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="d7945-167">prinUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="d7945-168">int</span><span class="sxs-lookup"><span data-stu-id="d7945-168">int</span></span></p></td>
<td><p><span data-ttu-id="d7945-169">ID de l’entité de confiance qui a mis à jour pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="d7945-169">ID of the principal that last updated this.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7945-170">prinUpdatedOn</span><span class="sxs-lookup"><span data-stu-id="d7945-170">prinUpdatedOn</span></span></p></td>
<td><p><span data-ttu-id="d7945-171">bigint, pas null</span><span class="sxs-lookup"><span data-stu-id="d7945-171">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="d7945-172">Horodatage de la dernière mise à jour.</span><span class="sxs-lookup"><span data-stu-id="d7945-172">Time stamp for the last update.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7945-173">prinVerifiedOn</span><span class="sxs-lookup"><span data-stu-id="d7945-173">prinVerifiedOn</span></span></p></td>
<td><p><span data-ttu-id="d7945-174">DATEHEURE, pas null</span><span class="sxs-lookup"><span data-stu-id="d7945-174">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="d7945-175">Date et heure de la dernière actualisation de la synchronisation Active Directory de l’utilisateur principal.</span><span class="sxs-lookup"><span data-stu-id="d7945-175">Date and time of the last Active Directory Sync refresh for the principal.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="d7945-176">Permettent</span><span class="sxs-lookup"><span data-stu-id="d7945-176">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7945-177">Colonne</span><span class="sxs-lookup"><span data-stu-id="d7945-177">Column</span></span></th>
<th><span data-ttu-id="d7945-178">Description</span><span class="sxs-lookup"><span data-stu-id="d7945-178">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7945-179">prinID</span><span class="sxs-lookup"><span data-stu-id="d7945-179">prinID</span></span></p></td>
<td><p><span data-ttu-id="d7945-180">Clé primaire.</span><span class="sxs-lookup"><span data-stu-id="d7945-180">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7945-181">prinTypeID</span><span class="sxs-lookup"><span data-stu-id="d7945-181">prinTypeID</span></span></p></td>
<td><p><span data-ttu-id="d7945-182">Clé étrangère avec recherche dans la table tblPrincipalType. ptypeID.</span><span class="sxs-lookup"><span data-stu-id="d7945-182">Foreign key with lookup in tblPrincipalType.ptypeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d7945-183">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d7945-183">


</div>

<span> </span>

</div>

</div>

</span></span></div>

