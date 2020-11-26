---
title: 'Lync Server 2013 : modifications apportées par la préparation du domaine'
description: 'Lync Server 2013 : modifications apportées par la préparation du domaine.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by domain preparation
ms:assetid: 9191221e-6166-4c2b-837e-fa73d90fdf80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398742(v=OCS.15)
ms:contentKeyID: 48184845
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26400bd1c72c6ae3b8dc1f2d2d8f6c6906b80595
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435116"
---
# <a name="changes-made-by-domain-preparation-in-lync-server-2013"></a><span data-ttu-id="78a51-103">Modifications apportées par la préparation du domaine dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="78a51-103">Changes made by domain preparation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="78a51-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="78a51-104">

<span> </span></span></span>

<span data-ttu-id="78a51-105">_**Dernière modification de la rubrique :** 2010-10-18_</span><span class="sxs-lookup"><span data-stu-id="78a51-105">_**Topic Last Modified:** 2010-10-18_</span></span>

<span data-ttu-id="78a51-106">Le tableau suivant répertorie les entrées de contrôle d’accès (ACE) créées par la préparation du domaine à la racine du domaine.</span><span class="sxs-lookup"><span data-stu-id="78a51-106">The following table lists the access control entries (ACEs) that domain preparation creates on the domain root.</span></span> <span data-ttu-id="78a51-107">Toutes les entrées ACE sont héritées sauf mention contraire.</span><span class="sxs-lookup"><span data-stu-id="78a51-107">All ACEs are inherited unless otherwise noted.</span></span>

<div id="sectionSection0" class="section">

### <a name="aces-added-to-domain-root"></a><span data-ttu-id="78a51-108">ACE ajoutés à la racine du domaine</span><span class="sxs-lookup"><span data-stu-id="78a51-108">ACEs Added to Domain Root</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78a51-109">MAILLOTS</span><span class="sxs-lookup"><span data-stu-id="78a51-109">ACE</span></span></th>
<th><span data-ttu-id="78a51-110">RTCUniversal-UserReadOnly-groupe</span><span class="sxs-lookup"><span data-stu-id="78a51-110">RTCUniversal-UserReadOnly-Group</span></span></th>
<th><span data-ttu-id="78a51-111">RTCUniversal-ServerReadOnly-groupe</span><span class="sxs-lookup"><span data-stu-id="78a51-111">RTCUniversal-ServerReadOnly-Group</span></span></th>
<th><span data-ttu-id="78a51-112">RTCUniversal-UserAdmins</span><span class="sxs-lookup"><span data-stu-id="78a51-112">RTCUniversal-UserAdmins</span></span></th>
<th><span data-ttu-id="78a51-113">RTCHSUniversal-Services</span><span class="sxs-lookup"><span data-stu-id="78a51-113">RTCHSUniversal-Services</span></span></th>
<th><span data-ttu-id="78a51-114">Authenticated-Users</span><span class="sxs-lookup"><span data-stu-id="78a51-114">Authenticated-Users</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78a51-115">Lire le conteneur (non hérité)</span><span class="sxs-lookup"><span data-stu-id="78a51-115">Read Container (not inherited)</span></span></p></td>
<td><p><span data-ttu-id="78a51-116"><strong>Oui</strong></span><span class="sxs-lookup"><span data-stu-id="78a51-116"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="78a51-117"><strong>Oui</strong></span><span class="sxs-lookup"><span data-stu-id="78a51-117"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="78a51-118">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-118">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-119">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-119">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-120">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-120">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78a51-121">Lire User PropertySet-compte-restrictions</span><span class="sxs-lookup"><span data-stu-id="78a51-121">Read User PropertySet User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="78a51-122"><strong>Oui</strong></span><span class="sxs-lookup"><span data-stu-id="78a51-122"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="78a51-123">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-123">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-124">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-124">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-125">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-125">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-126">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78a51-127">Lire les Personal-Information utilisateur PropertySet</span><span class="sxs-lookup"><span data-stu-id="78a51-127">Read User PropertySet Personal-Information</span></span></p></td>
<td><p><span data-ttu-id="78a51-128"><strong>Oui</strong></span><span class="sxs-lookup"><span data-stu-id="78a51-128"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="78a51-129">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-129">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-130">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-130">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-131">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-131">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-132">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-132">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78a51-133">Lire les General-Information utilisateur PropertySet</span><span class="sxs-lookup"><span data-stu-id="78a51-133">Read User PropertySet General-Information</span></span></p></td>
<td><p><span data-ttu-id="78a51-134"><strong>Oui</strong></span><span class="sxs-lookup"><span data-stu-id="78a51-134"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="78a51-135">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-135">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-136">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-136">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-137">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-137">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-138">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-138">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78a51-139">Lire les Public-Information utilisateur PropertySet</span><span class="sxs-lookup"><span data-stu-id="78a51-139">Read User PropertySet Public-Information</span></span></p></td>
<td><p><span data-ttu-id="78a51-140"><strong>Oui</strong></span><span class="sxs-lookup"><span data-stu-id="78a51-140"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="78a51-141">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-141">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-142">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-142">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-143">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-143">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-144">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-144">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78a51-145">Lire les RTCUserSearchProperty-Set utilisateur PropertySet</span><span class="sxs-lookup"><span data-stu-id="78a51-145">Read User PropertySet RTCUserSearchProperty-Set</span></span></p></td>
<td><p><span data-ttu-id="78a51-146"><strong>Oui</strong></span><span class="sxs-lookup"><span data-stu-id="78a51-146"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="78a51-147">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-147">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-148">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-148">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-149">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-149">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-150"><strong>Oui</strong></span><span class="sxs-lookup"><span data-stu-id="78a51-150"><strong>Yes</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78a51-151">Lire User PropertySet RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="78a51-151">Read User PropertySet RTCPropertySet</span></span></p></td>
<td><p><span data-ttu-id="78a51-152"><strong>Oui</strong></span><span class="sxs-lookup"><span data-stu-id="78a51-152"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="78a51-153">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-153">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-154">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-154">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-155">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-155">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-156">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78a51-157">Écrire Proxy-Addresses de propriété d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="78a51-157">Write User Property Proxy-Addresses</span></span></p></td>
<td><p><span data-ttu-id="78a51-158">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-158">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-159">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-159">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-160"><strong>Oui</strong></span><span class="sxs-lookup"><span data-stu-id="78a51-160"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="78a51-161">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-161">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-162">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-162">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78a51-163">Écrire RTCUserSearchProperty-Set utilisateur PropertySet</span><span class="sxs-lookup"><span data-stu-id="78a51-163">Write User PropertySet RTCUserSearchProperty-Set</span></span></p></td>
<td><p><span data-ttu-id="78a51-164">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-164">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-165">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-165">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-166"><strong>Oui</strong></span><span class="sxs-lookup"><span data-stu-id="78a51-166"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="78a51-167">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-167">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-168">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-168">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78a51-169">Écrire RTCPropertySet utilisateur</span><span class="sxs-lookup"><span data-stu-id="78a51-169">Write User PropertySet RTCPropertySet</span></span></p></td>
<td><p><span data-ttu-id="78a51-170">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-170">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-171">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-171">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-172"><strong>Oui</strong></span><span class="sxs-lookup"><span data-stu-id="78a51-172"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="78a51-173">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-173">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-174">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-174">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78a51-175">Lecture de PropertySet DS-réplication-obtention-modification de tous les objets Active Directory</span><span class="sxs-lookup"><span data-stu-id="78a51-175">Read PropertySet DS-Replication-Get-Changes of all Active Directory objects</span></span></p></td>
<td><p><span data-ttu-id="78a51-176">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-176">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-177">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-177">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-178">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-178">No</span></span></p></td>
<td><p><span data-ttu-id="78a51-179"><strong>Oui</strong></span><span class="sxs-lookup"><span data-stu-id="78a51-179"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="78a51-180">Non</span><span class="sxs-lookup"><span data-stu-id="78a51-180">No</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="78a51-181">Le tableau suivant répertorie les entrées de contrôle d’accès qu’il est créé dans les trois conteneurs intégrés : utilisateurs, ordinateurs et contrôleurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="78a51-181">The following table lists the ACEs that domain preparation creates in the three built-in containers: Users, Computers, and Domain Controllers.</span></span> <span data-ttu-id="78a51-182">Toutes les entrées ACE sont héritées sauf mention contraire.</span><span class="sxs-lookup"><span data-stu-id="78a51-182">All ACEs are inherited unless otherwise noted.</span></span>

### <a name="aces-added-to-built-in-containers"></a><span data-ttu-id="78a51-183">ACE ajoutés aux conteneurs intégrés</span><span class="sxs-lookup"><span data-stu-id="78a51-183">ACEs Added to Built-in Containers</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78a51-184">MAILLOTS</span><span class="sxs-lookup"><span data-stu-id="78a51-184">ACE</span></span></th>
<th><span data-ttu-id="78a51-185">RTCUniversal-UserReadOnly-groupe</span><span class="sxs-lookup"><span data-stu-id="78a51-185">RTCUniversal-UserReadOnly-Group</span></span></th>
<th><span data-ttu-id="78a51-186">RTCUniversal-ServerReadOnly-groupe</span><span class="sxs-lookup"><span data-stu-id="78a51-186">RTCUniversal-ServerReadOnly-Group</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78a51-187">Lire le conteneur (non hérité)</span><span class="sxs-lookup"><span data-stu-id="78a51-187">Read Container (not inherited)</span></span></p></td>
<td><p><span data-ttu-id="78a51-188"><strong>Oui</strong></span><span class="sxs-lookup"><span data-stu-id="78a51-188"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="78a51-189"><strong>Oui</strong></span><span class="sxs-lookup"><span data-stu-id="78a51-189"><strong>Yes</strong></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="78a51-190">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="78a51-190">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

