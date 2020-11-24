---
title: 'Lync Server 2013 : tblPrincipalType'
description: 'Lync Server 2013 : tblPrincipalType.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalType
ms:assetid: 32e1c1d6-80f4-4624-bf4e-b4c77d3982fa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558633(v=OCS.15)
ms:contentKeyID: 48183787
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba0f607d4499b54b16d7ecf8a4e7de603e874788
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393909"
---
# <a name="tblprincipaltype-in-lync-server-2013"></a><span data-ttu-id="614a1-103">tblPrincipalType dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="614a1-103">tblPrincipalType in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="614a1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="614a1-104">

<span> </span></span></span>

<span data-ttu-id="614a1-105">_**Dernière modification de la rubrique :** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="614a1-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="614a1-106">tblPrincipalType contient des types de principaux pour classer ce qui se trouve dans la table tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="614a1-106">tblPrincipalType contains principal types to categorize what is in the tblPrincipal table.</span></span>

### <a name="columns"></a><span data-ttu-id="614a1-107">Celles</span><span class="sxs-lookup"><span data-stu-id="614a1-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="614a1-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="614a1-108">Column</span></span></th>
<th><span data-ttu-id="614a1-109">Type</span><span class="sxs-lookup"><span data-stu-id="614a1-109">Type</span></span></th>
<th><span data-ttu-id="614a1-110">Description</span><span class="sxs-lookup"><span data-stu-id="614a1-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="614a1-111">ptypeID</span><span class="sxs-lookup"><span data-stu-id="614a1-111">ptypeID</span></span></p></td>
<td><p><span data-ttu-id="614a1-112">smallint, pas null</span><span class="sxs-lookup"><span data-stu-id="614a1-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="614a1-113">ID de type principal.</span><span class="sxs-lookup"><span data-stu-id="614a1-113">Principal type ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="614a1-114">ptypeDesc</span><span class="sxs-lookup"><span data-stu-id="614a1-114">ptypeDesc</span></span></p></td>
<td><p><span data-ttu-id="614a1-115">nvarchar (256), pas null</span><span class="sxs-lookup"><span data-stu-id="614a1-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="614a1-116">Description du type.</span><span class="sxs-lookup"><span data-stu-id="614a1-116">Description of the type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="614a1-117">ptypeIsSystemUser</span><span class="sxs-lookup"><span data-stu-id="614a1-117">ptypeIsSystemUser</span></span></p></td>
<td><p><span data-ttu-id="614a1-118">bit, pas null</span><span class="sxs-lookup"><span data-stu-id="614a1-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="614a1-119">True si le type correspond aux éléments principaux utilisés à des fins internes.</span><span class="sxs-lookup"><span data-stu-id="614a1-119">True if the type corresponds to the principals that are used for internal purposes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="614a1-120">ptypeIsUser</span><span class="sxs-lookup"><span data-stu-id="614a1-120">ptypeIsUser</span></span></p></td>
<td><p><span data-ttu-id="614a1-121">bit, pas null</span><span class="sxs-lookup"><span data-stu-id="614a1-121">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="614a1-122">True si le type est un type d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614a1-122">True if the type is a user type.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="614a1-123">Clé</span><span class="sxs-lookup"><span data-stu-id="614a1-123">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="614a1-124">Colonne</span><span class="sxs-lookup"><span data-stu-id="614a1-124">Column</span></span></th>
<th><span data-ttu-id="614a1-125">Description</span><span class="sxs-lookup"><span data-stu-id="614a1-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="614a1-126">ptypeID</span><span class="sxs-lookup"><span data-stu-id="614a1-126">ptypeID</span></span></p></td>
<td><p><span data-ttu-id="614a1-127">Clé primaire.</span><span class="sxs-lookup"><span data-stu-id="614a1-127">Primary key.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="principal-values"></a><span data-ttu-id="614a1-128">Valeurs principales</span><span class="sxs-lookup"><span data-stu-id="614a1-128">Principal Values</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="614a1-129">ID</span><span class="sxs-lookup"><span data-stu-id="614a1-129">ID</span></span></th>
<th><span data-ttu-id="614a1-130">Rôle</span><span class="sxs-lookup"><span data-stu-id="614a1-130">Role</span></span></th>
<th><span data-ttu-id="614a1-131">Description</span><span class="sxs-lookup"><span data-stu-id="614a1-131">Description</span></span></th>
<th><span data-ttu-id="614a1-132">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="614a1-132">User</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="614a1-133">1</span><span class="sxs-lookup"><span data-stu-id="614a1-133">1</span></span></p></td>
<td><p><span data-ttu-id="614a1-134">Indifférente</span><span class="sxs-lookup"><span data-stu-id="614a1-134">Any</span></span></p></td>
<td><p><span data-ttu-id="614a1-135">Principal générique sans type connu.</span><span class="sxs-lookup"><span data-stu-id="614a1-135">Generic principal with no known type.</span></span> <span data-ttu-id="614a1-136">Non utilisé dans la table tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="614a1-136">Not used in tblPrincipal table.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="614a1-137">2</span><span class="sxs-lookup"><span data-stu-id="614a1-137">2</span></span></p></td>
<td><p><span data-ttu-id="614a1-138">AnyUser</span><span class="sxs-lookup"><span data-stu-id="614a1-138">AnyUser</span></span></p></td>
<td><p><span data-ttu-id="614a1-139">Principal générique de type d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614a1-139">Generic principal of user type.</span></span> <span data-ttu-id="614a1-140">Non utilisé dans la table tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="614a1-140">Not used in tblPrincipal table.</span></span></p></td>
<td><p><span data-ttu-id="614a1-141">Oui</span><span class="sxs-lookup"><span data-stu-id="614a1-141">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="614a1-142">3</span><span class="sxs-lookup"><span data-stu-id="614a1-142">3</span></span></p></td>
<td><p><span data-ttu-id="614a1-143">AnyGroup</span><span class="sxs-lookup"><span data-stu-id="614a1-143">AnyGroup</span></span></p></td>
<td><p><span data-ttu-id="614a1-144">Principal générique avec la sémantique de groupe.</span><span class="sxs-lookup"><span data-stu-id="614a1-144">Generic principal with group semantic.</span></span> <span data-ttu-id="614a1-145">Non utilisé dans la table tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="614a1-145">Not used in tblPrincipal table.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="614a1-146">4</span><span class="sxs-lookup"><span data-stu-id="614a1-146">4</span></span></p></td>
<td><p><span data-ttu-id="614a1-147">SystemUser</span><span class="sxs-lookup"><span data-stu-id="614a1-147">SystemUser</span></span></p></td>
<td><p><span data-ttu-id="614a1-148">Principal utilisé par le serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="614a1-148">Principal used internally by Persistent Chat Server.</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="614a1-149">5</span><span class="sxs-lookup"><span data-stu-id="614a1-149">5</span></span></p></td>
<td><p><span data-ttu-id="614a1-150">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="614a1-150">User</span></span></p></td>
<td><p><span data-ttu-id="614a1-151">Utilisateur ordinaire.</span><span class="sxs-lookup"><span data-stu-id="614a1-151">Regular user.</span></span></p></td>
<td><p><span data-ttu-id="614a1-152">Oui</span><span class="sxs-lookup"><span data-stu-id="614a1-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="614a1-153">version8</span><span class="sxs-lookup"><span data-stu-id="614a1-153">8</span></span></p></td>
<td><p><span data-ttu-id="614a1-154">CD</span><span class="sxs-lookup"><span data-stu-id="614a1-154">DC</span></span></p></td>
<td><p><span data-ttu-id="614a1-155">Contrôleur de domaine Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="614a1-155">Active Directory Domain Services domain controller.</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="614a1-156">09</span><span class="sxs-lookup"><span data-stu-id="614a1-156">9</span></span></p></td>
<td><p><span data-ttu-id="614a1-157">Groupe</span><span class="sxs-lookup"><span data-stu-id="614a1-157">Group</span></span></p></td>
<td><p><span data-ttu-id="614a1-158">Groupe de sécurité Active Directory.</span><span class="sxs-lookup"><span data-stu-id="614a1-158">Active Directory security group.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="614a1-159">0,10</span><span class="sxs-lookup"><span data-stu-id="614a1-159">10</span></span></p></td>
<td><p><span data-ttu-id="614a1-160">Dossier</span><span class="sxs-lookup"><span data-stu-id="614a1-160">Folder</span></span></p></td>
<td><p><span data-ttu-id="614a1-161">Conteneur Active Directory ou unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="614a1-161">Active Directory container or organizational unit.</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="614a1-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="614a1-162">See Also</span></span>


[<span data-ttu-id="614a1-163">tblPrincipal dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="614a1-163">tblPrincipal in Lync Server 2013</span></span>](lync-server-2013-tblprincipal.md)  
  

<span data-ttu-id="614a1-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="614a1-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

