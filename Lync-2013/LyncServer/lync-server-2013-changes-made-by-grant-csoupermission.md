---
title: 'Lync Server 2013 : modifications apportées par Grant-CsOUPermission'
description: 'Lync Server 2013 : modifications apportées par Grant-CsOUPermission.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by Grant-CsOUPermission
ms:assetid: d744d352-1ad9-4447-8e2b-28e768d2ed1b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205310(v=OCS.15)
ms:contentKeyID: 48185564
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 10d3db0e9dde380628690bc016e2b4bd2ec85b54
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435053"
---
# <a name="changes-made-by-grant-csoupermission-in-lync-server-2013"></a><span data-ttu-id="22acc-103">Modifications apportées par Grant-CsOUPermission dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22acc-103">Changes made by Grant-CsOUPermission in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="22acc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="22acc-104">

<span> </span></span></span>

<span data-ttu-id="22acc-105">_**Dernière modification de la rubrique :** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="22acc-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="22acc-106">Pour déléguer l’administration de Lync Server 2013, vous pouvez ajouter des autorisations aux unités d’organisation (UO) spécifiées de sorte que les membres des groupes universels RTC créés par la préparation de la forêt puissent accéder aux UO sans être membres du groupe administrateurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="22acc-106">To delegate Lync Server 2013 administration, you can add permissions to specified organizational units (OUs) so that members of the RTC universal groups created by forest preparation can access the OUs without being members of the Domain Admins group.</span></span>

<span data-ttu-id="22acc-107">L’applet **de commande Grant-CsOuPermission** accorde des autorisations aux objets de l’unité d’organisation spécifiée, comme indiqué dans les tableaux suivants.</span><span class="sxs-lookup"><span data-stu-id="22acc-107">The **Grant-CsOuPermission** cmdlet grants permissions to objects in the specified OU as specified in the following tables.</span></span>

<div>

## <a name="granting-permission-for-user-objects"></a><span data-ttu-id="22acc-108">Octroi d’autorisations pour les objets utilisateur</span><span class="sxs-lookup"><span data-stu-id="22acc-108">Granting Permission for User Objects</span></span>

<span data-ttu-id="22acc-109">Lorsque vous exécutez l’applet de commande **Grant-CsOuPermission** pour les objets utilisateur sur une unité d’organisation, les autorisations de groupe sont accordées, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="22acc-109">When you run the **Grant-CsOuPermission** cmdlet for User objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-user-objects"></a><span data-ttu-id="22acc-110">Autorisations accordées pour les objets utilisateur</span><span class="sxs-lookup"><span data-stu-id="22acc-110">Permissions Granted for User Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22acc-111">Groupe</span><span class="sxs-lookup"><span data-stu-id="22acc-111">Group</span></span></th>
<th><span data-ttu-id="22acc-112">Permission</span><span class="sxs-lookup"><span data-stu-id="22acc-112">Permission</span></span></th>
<th><span data-ttu-id="22acc-113">S’applique à</span><span class="sxs-lookup"><span data-stu-id="22acc-113">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22acc-114">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="22acc-114">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="22acc-115">Répliquer les modifications de l’annuaire</span><span class="sxs-lookup"><span data-stu-id="22acc-115">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="22acc-116">Cet objet uniquement</span><span class="sxs-lookup"><span data-stu-id="22acc-116">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22acc-117">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="22acc-117">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="22acc-118">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="22acc-118">List contents</span></span></p>
<p><span data-ttu-id="22acc-119">Lire toutes les propriétés</span><span class="sxs-lookup"><span data-stu-id="22acc-119">Read all properties</span></span></p>
<p><span data-ttu-id="22acc-120">Autorisations de lecture</span><span class="sxs-lookup"><span data-stu-id="22acc-120">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="22acc-121">Cet objet uniquement</span><span class="sxs-lookup"><span data-stu-id="22acc-121">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22acc-122">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="22acc-122">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="22acc-123">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="22acc-123">List contents</span></span></p>
<p><span data-ttu-id="22acc-124">Lire toutes les propriétés</span><span class="sxs-lookup"><span data-stu-id="22acc-124">Read all properties</span></span></p>
<p><span data-ttu-id="22acc-125">Autorisations de lecture</span><span class="sxs-lookup"><span data-stu-id="22acc-125">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="22acc-126">Cet objet uniquement</span><span class="sxs-lookup"><span data-stu-id="22acc-126">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22acc-127">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="22acc-127">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="22acc-128">Lecture de RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-128">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="22acc-129">Lecture de RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-129">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="22acc-130">Lecture de RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-130">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="22acc-131">Lire Public-Information</span><span class="sxs-lookup"><span data-stu-id="22acc-131">Read Public-Information</span></span></p>
<p><span data-ttu-id="22acc-132">Lire General-Information</span><span class="sxs-lookup"><span data-stu-id="22acc-132">Read General-Information</span></span></p>
<p><span data-ttu-id="22acc-133">Lire le compte d’utilisateur-restrictions</span><span class="sxs-lookup"><span data-stu-id="22acc-133">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="22acc-134">Objets utilisateur descendants</span><span class="sxs-lookup"><span data-stu-id="22acc-134">Descendant User objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22acc-135">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="22acc-135">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="22acc-136">Écrire RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-136">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="22acc-137">Écrire msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="22acc-137">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="22acc-138">Écrire RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-138">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="22acc-139">Écrire RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-139">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="22acc-140">Écrire proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="22acc-140">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="22acc-141">Objets utilisateur descendants</span><span class="sxs-lookup"><span data-stu-id="22acc-141">Descendant User objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-computer-objects"></a><span data-ttu-id="22acc-142">Octroi d’autorisations pour les objets ordinateur</span><span class="sxs-lookup"><span data-stu-id="22acc-142">Granting Permission for Computer Objects</span></span>

<span data-ttu-id="22acc-143">Lorsque vous exécutez l’applet de commande **Grant-CsOuPermission** pour les objets ordinateur sur une unité d’organisation, les autorisations de groupe sont accordées, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="22acc-143">When you run the **Grant-CsOuPermission** cmdlet for Computer objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-computer-objects"></a><span data-ttu-id="22acc-144">Autorisations accordées pour les objets ordinateur</span><span class="sxs-lookup"><span data-stu-id="22acc-144">Permissions Granted for Computer Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22acc-145">Groupe</span><span class="sxs-lookup"><span data-stu-id="22acc-145">Group</span></span></th>
<th><span data-ttu-id="22acc-146">Permission</span><span class="sxs-lookup"><span data-stu-id="22acc-146">Permission</span></span></th>
<th><span data-ttu-id="22acc-147">S’applique à</span><span class="sxs-lookup"><span data-stu-id="22acc-147">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22acc-148">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="22acc-148">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="22acc-149">Répliquer les modifications de l’annuaire</span><span class="sxs-lookup"><span data-stu-id="22acc-149">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="22acc-150">Cet objet uniquement</span><span class="sxs-lookup"><span data-stu-id="22acc-150">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22acc-151">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="22acc-151">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="22acc-152">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="22acc-152">List contents</span></span></p>
<p><span data-ttu-id="22acc-153">Lire toutes les propriétés</span><span class="sxs-lookup"><span data-stu-id="22acc-153">Read all properties</span></span></p>
<p><span data-ttu-id="22acc-154">Autorisations de lecture</span><span class="sxs-lookup"><span data-stu-id="22acc-154">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="22acc-155">Cet objet uniquement</span><span class="sxs-lookup"><span data-stu-id="22acc-155">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22acc-156">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="22acc-156">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="22acc-157">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="22acc-157">List contents</span></span></p>
<p><span data-ttu-id="22acc-158">Lire toutes les propriétés</span><span class="sxs-lookup"><span data-stu-id="22acc-158">Read all properties</span></span></p>
<p><span data-ttu-id="22acc-159">Autorisations de lecture</span><span class="sxs-lookup"><span data-stu-id="22acc-159">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="22acc-160">Cet objet uniquement</span><span class="sxs-lookup"><span data-stu-id="22acc-160">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22acc-161">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="22acc-161">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="22acc-162">Lire Public-Information</span><span class="sxs-lookup"><span data-stu-id="22acc-162">Read Public-Information</span></span></p>
<p><span data-ttu-id="22acc-163">Lecture validée de DNS-nom d’hôte-nom</span><span class="sxs-lookup"><span data-stu-id="22acc-163">Read Validated-DNS-Host-Name</span></span></p></td>
<td><p><span data-ttu-id="22acc-164">Objets ordinateur descendants</span><span class="sxs-lookup"><span data-stu-id="22acc-164">Descendant Computer objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22acc-165">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="22acc-165">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="22acc-166">Lire Public-Information</span><span class="sxs-lookup"><span data-stu-id="22acc-166">Read Public-Information</span></span></p>
<p><span data-ttu-id="22acc-167">Lecture validée de DNS-nom d’hôte-nom</span><span class="sxs-lookup"><span data-stu-id="22acc-167">Read Validated-DNS-Host-Name</span></span></p></td>
<td><p><span data-ttu-id="22acc-168">Objets ordinateur descendants</span><span class="sxs-lookup"><span data-stu-id="22acc-168">Descendant Computer objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-contact-or-appcontact-objects"></a><span data-ttu-id="22acc-169">Octroi d’autorisations de contact ou d’objets AppContact</span><span class="sxs-lookup"><span data-stu-id="22acc-169">Granting Permission for Contact or AppContact Objects</span></span>

<span data-ttu-id="22acc-170">Lorsque vous exécutez l’applet de commande **Grant-CsOuPermission** pour les objets de contact ou les objets AppContact sur une unité d’organisation, les autorisations de groupe sont accordées, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="22acc-170">When you run the **Grant-CsOuPermission** cmdlet for Contact objects or AppContact objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-contact-or-appcontact-objects"></a><span data-ttu-id="22acc-171">Autorisations accordées pour les objets contact ou AppContact</span><span class="sxs-lookup"><span data-stu-id="22acc-171">Permissions Granted for Contact or AppContact Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22acc-172">Groupe</span><span class="sxs-lookup"><span data-stu-id="22acc-172">Group</span></span></th>
<th><span data-ttu-id="22acc-173">Permission</span><span class="sxs-lookup"><span data-stu-id="22acc-173">Permission</span></span></th>
<th><span data-ttu-id="22acc-174">S’applique à</span><span class="sxs-lookup"><span data-stu-id="22acc-174">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22acc-175">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="22acc-175">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="22acc-176">Répliquer les modifications de l’annuaire</span><span class="sxs-lookup"><span data-stu-id="22acc-176">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="22acc-177">Cet objet uniquement</span><span class="sxs-lookup"><span data-stu-id="22acc-177">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22acc-178">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="22acc-178">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="22acc-179">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="22acc-179">List contents</span></span></p>
<p><span data-ttu-id="22acc-180">Lire toutes les propriétés</span><span class="sxs-lookup"><span data-stu-id="22acc-180">Read all properties</span></span></p>
<p><span data-ttu-id="22acc-181">Autorisations de lecture</span><span class="sxs-lookup"><span data-stu-id="22acc-181">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="22acc-182">Cet objet uniquement</span><span class="sxs-lookup"><span data-stu-id="22acc-182">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22acc-183">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="22acc-183">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="22acc-184">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="22acc-184">List contents</span></span></p>
<p><span data-ttu-id="22acc-185">Lire toutes les propriétés</span><span class="sxs-lookup"><span data-stu-id="22acc-185">Read all properties</span></span></p>
<p><span data-ttu-id="22acc-186">Autorisations de lecture</span><span class="sxs-lookup"><span data-stu-id="22acc-186">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="22acc-187">Cet objet uniquement</span><span class="sxs-lookup"><span data-stu-id="22acc-187">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22acc-188">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="22acc-188">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="22acc-189">Lecture de RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-189">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="22acc-190">Lecture de RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-190">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="22acc-191">Lecture de RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-191">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="22acc-192">Lire Public-Information</span><span class="sxs-lookup"><span data-stu-id="22acc-192">Read Public-Information</span></span></p>
<p><span data-ttu-id="22acc-193">Lire General-Information</span><span class="sxs-lookup"><span data-stu-id="22acc-193">Read General-Information</span></span></p>
<p><span data-ttu-id="22acc-194">Lire Personal-Information</span><span class="sxs-lookup"><span data-stu-id="22acc-194">Read Personal-Information</span></span></p>
<p><span data-ttu-id="22acc-195">Lire le compte d’utilisateur-restrictions</span><span class="sxs-lookup"><span data-stu-id="22acc-195">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="22acc-196">Objets contact descendants</span><span class="sxs-lookup"><span data-stu-id="22acc-196">Descendant Contact objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22acc-197">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="22acc-197">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="22acc-198">Écrire RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-198">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="22acc-199">Écrire otherIpPhone</span><span class="sxs-lookup"><span data-stu-id="22acc-199">Write otherIpPhone</span></span></p>
<p><span data-ttu-id="22acc-200">Écrire displayName</span><span class="sxs-lookup"><span data-stu-id="22acc-200">Write displayName</span></span></p>
<p><span data-ttu-id="22acc-201">Entrer une description</span><span class="sxs-lookup"><span data-stu-id="22acc-201">Write description</span></span></p>
<p><span data-ttu-id="22acc-202">Écrire telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="22acc-202">Write telephoneNumber</span></span></p>
<p><span data-ttu-id="22acc-203">Écrire msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="22acc-203">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="22acc-204">Écrire RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-204">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="22acc-205">Écrire RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-205">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="22acc-206">Écrire proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="22acc-206">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="22acc-207">Objets contact descendants</span><span class="sxs-lookup"><span data-stu-id="22acc-207">Descendant Contact objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-device-objects"></a><span data-ttu-id="22acc-208">Octroi d’autorisations pour les objets appareil</span><span class="sxs-lookup"><span data-stu-id="22acc-208">Granting Permission for Device Objects</span></span>

<span data-ttu-id="22acc-209">Lorsque vous exécutez l’applet de commande **Grant-CsOuPermission** pour les objets d’appareil sur une unité d’organisation, les autorisations de groupe sont accordées, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="22acc-209">When you run the **Grant-CsOuPermission** cmdlet for Device objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-device-objects"></a><span data-ttu-id="22acc-210">Autorisations accordées pour les objets appareil</span><span class="sxs-lookup"><span data-stu-id="22acc-210">Permissions Granted for Device Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22acc-211">Groupe</span><span class="sxs-lookup"><span data-stu-id="22acc-211">Group</span></span></th>
<th><span data-ttu-id="22acc-212">Permission</span><span class="sxs-lookup"><span data-stu-id="22acc-212">Permission</span></span></th>
<th><span data-ttu-id="22acc-213">S’applique à</span><span class="sxs-lookup"><span data-stu-id="22acc-213">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22acc-214">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="22acc-214">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="22acc-215">Répliquer les modifications de l’annuaire</span><span class="sxs-lookup"><span data-stu-id="22acc-215">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="22acc-216">Cet objet uniquement</span><span class="sxs-lookup"><span data-stu-id="22acc-216">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22acc-217">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="22acc-217">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="22acc-218">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="22acc-218">List contents</span></span></p>
<p><span data-ttu-id="22acc-219">Lire toutes les propriétés</span><span class="sxs-lookup"><span data-stu-id="22acc-219">Read all properties</span></span></p>
<p><span data-ttu-id="22acc-220">Autorisations de lecture</span><span class="sxs-lookup"><span data-stu-id="22acc-220">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="22acc-221">Cet objet uniquement</span><span class="sxs-lookup"><span data-stu-id="22acc-221">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22acc-222">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="22acc-222">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="22acc-223">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="22acc-223">List contents</span></span></p>
<p><span data-ttu-id="22acc-224">Lire toutes les propriétés</span><span class="sxs-lookup"><span data-stu-id="22acc-224">Read all properties</span></span></p>
<p><span data-ttu-id="22acc-225">Autorisations de lecture</span><span class="sxs-lookup"><span data-stu-id="22acc-225">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="22acc-226">Cet objet uniquement</span><span class="sxs-lookup"><span data-stu-id="22acc-226">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22acc-227">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="22acc-227">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="22acc-228">Lecture de RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-228">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="22acc-229">Lecture de RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-229">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="22acc-230">Lecture de RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-230">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="22acc-231">Lire Public-Information</span><span class="sxs-lookup"><span data-stu-id="22acc-231">Read Public-Information</span></span></p>
<p><span data-ttu-id="22acc-232">Lire Personal-Information</span><span class="sxs-lookup"><span data-stu-id="22acc-232">Read Personal-Information</span></span></p>
<p><span data-ttu-id="22acc-233">Lire General-Information</span><span class="sxs-lookup"><span data-stu-id="22acc-233">Read General-Information</span></span></p>
<p><span data-ttu-id="22acc-234">Lire le compte d’utilisateur-restrictions</span><span class="sxs-lookup"><span data-stu-id="22acc-234">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="22acc-235">Objets contact descendants</span><span class="sxs-lookup"><span data-stu-id="22acc-235">Descendant Contact objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22acc-236">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="22acc-236">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="22acc-237">Créer un enfant</span><span class="sxs-lookup"><span data-stu-id="22acc-237">Create child</span></span></p>
<p><span data-ttu-id="22acc-238">Supprimer un enfant</span><span class="sxs-lookup"><span data-stu-id="22acc-238">Delete child</span></span></p>
<p><span data-ttu-id="22acc-239">Supprimer l’arborescence</span><span class="sxs-lookup"><span data-stu-id="22acc-239">Delete tree</span></span></p></td>
<td><p><span data-ttu-id="22acc-240">Locuteur</span><span class="sxs-lookup"><span data-stu-id="22acc-240">Contact</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22acc-241">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="22acc-241">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="22acc-242">Écrire displayName</span><span class="sxs-lookup"><span data-stu-id="22acc-242">Write displayName</span></span></p>
<p><span data-ttu-id="22acc-243">Entrer une description</span><span class="sxs-lookup"><span data-stu-id="22acc-243">Write description</span></span></p>
<p><span data-ttu-id="22acc-244">Écrire telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="22acc-244">Write telephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="22acc-245">Objets utilisateur descendants</span><span class="sxs-lookup"><span data-stu-id="22acc-245">Descendant User objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22acc-246">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="22acc-246">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="22acc-247">Écrire RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-247">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="22acc-248">Écrire otherIpPhone</span><span class="sxs-lookup"><span data-stu-id="22acc-248">Write otherIpPhone</span></span></p>
<p><span data-ttu-id="22acc-249">Écrire displayName</span><span class="sxs-lookup"><span data-stu-id="22acc-249">Write displayName</span></span></p>
<p><span data-ttu-id="22acc-250">Entrer une description</span><span class="sxs-lookup"><span data-stu-id="22acc-250">Write description</span></span></p>
<p><span data-ttu-id="22acc-251">Écrire telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="22acc-251">Write telephoneNumber</span></span></p>
<p><span data-ttu-id="22acc-252">Écrire msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="22acc-252">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="22acc-253">Écrire RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-253">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="22acc-254">Écrire RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-254">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="22acc-255">Écrire proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="22acc-255">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="22acc-256">Objets contact descendants</span><span class="sxs-lookup"><span data-stu-id="22acc-256">Descendant Contact objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-inetorgperson-objects"></a><span data-ttu-id="22acc-257">Octroi d’autorisations pour les objets InetOrgPerson</span><span class="sxs-lookup"><span data-stu-id="22acc-257">Granting Permission for InetOrgPerson Objects</span></span>

<span data-ttu-id="22acc-258">Lorsque vous exécutez l’applet de commande **Grant-CsOuPermission** pour les objets InetOrgPerson sur une unité d’organisation, les autorisations de groupe sont accordées, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="22acc-258">When you run the **Grant-CsOuPermission** cmdlet for InetOrgPerson objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-inetorgperson-objects"></a><span data-ttu-id="22acc-259">Autorisations accordées pour les objets InetOrgPerson</span><span class="sxs-lookup"><span data-stu-id="22acc-259">Permissions Granted for InetOrgPerson Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22acc-260">Groupe</span><span class="sxs-lookup"><span data-stu-id="22acc-260">Group</span></span></th>
<th><span data-ttu-id="22acc-261">Permission</span><span class="sxs-lookup"><span data-stu-id="22acc-261">Permission</span></span></th>
<th><span data-ttu-id="22acc-262">S’applique à</span><span class="sxs-lookup"><span data-stu-id="22acc-262">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22acc-263">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="22acc-263">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="22acc-264">Répliquer les modifications de l’annuaire</span><span class="sxs-lookup"><span data-stu-id="22acc-264">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="22acc-265">Cet objet uniquement</span><span class="sxs-lookup"><span data-stu-id="22acc-265">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22acc-266">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="22acc-266">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="22acc-267">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="22acc-267">List contents</span></span></p>
<p><span data-ttu-id="22acc-268">Lire toutes les propriétés</span><span class="sxs-lookup"><span data-stu-id="22acc-268">Read all properties</span></span></p>
<p><span data-ttu-id="22acc-269">Autorisations de lecture</span><span class="sxs-lookup"><span data-stu-id="22acc-269">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="22acc-270">Cet objet uniquement</span><span class="sxs-lookup"><span data-stu-id="22acc-270">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22acc-271">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="22acc-271">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="22acc-272">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="22acc-272">List contents</span></span></p>
<p><span data-ttu-id="22acc-273">Lire toutes les propriétés</span><span class="sxs-lookup"><span data-stu-id="22acc-273">Read all properties</span></span></p>
<p><span data-ttu-id="22acc-274">Autorisations de lecture</span><span class="sxs-lookup"><span data-stu-id="22acc-274">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="22acc-275">Cet objet uniquement</span><span class="sxs-lookup"><span data-stu-id="22acc-275">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22acc-276">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="22acc-276">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="22acc-277">Lecture de RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-277">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="22acc-278">Lecture de RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-278">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="22acc-279">Lecture de RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-279">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="22acc-280">Lire Personal-Information</span><span class="sxs-lookup"><span data-stu-id="22acc-280">Read Personal-Information</span></span></p>
<p><span data-ttu-id="22acc-281">Lire Public-Information</span><span class="sxs-lookup"><span data-stu-id="22acc-281">Read Public-Information</span></span></p>
<p><span data-ttu-id="22acc-282">Lire General-Information</span><span class="sxs-lookup"><span data-stu-id="22acc-282">Read General-Information</span></span></p>
<p><span data-ttu-id="22acc-283">Lire le compte d’utilisateur-restrictions</span><span class="sxs-lookup"><span data-stu-id="22acc-283">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="22acc-284">Objets inetOrgPerson descendants</span><span class="sxs-lookup"><span data-stu-id="22acc-284">Descendant inetOrgPerson objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22acc-285">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="22acc-285">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="22acc-286">Écrire RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-286">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="22acc-287">Écrire RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-287">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="22acc-288">Écrire RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="22acc-288">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="22acc-289">Écrire proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="22acc-289">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="22acc-290">Objets inetOrgPerson descendants</span><span class="sxs-lookup"><span data-stu-id="22acc-290">Descendant inetOrgPerson objects</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="22acc-291">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="22acc-291">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

