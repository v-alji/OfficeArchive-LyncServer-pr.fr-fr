---
title: 'Lync Server 2013 : modifications apportées par Grant-CsSetupPermission'
description: 'Lync Server 2013 : modifications apportées par Grant-CsSetupPermission.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by Grant-CsSetupPermission
ms:assetid: c5801f48-14e3-4fdd-8f14-d52e7af07a57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205250(v=OCS.15)
ms:contentKeyID: 48185360
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d2a9156c977c993dd32e38fc6816bd08d3f65c1f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435067"
---
# <a name="changes-made-by-grant-cssetuppermission-in-lync-server-2013"></a><span data-ttu-id="ce535-103">Modifications apportées par Grant-CsSetupPermission dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce535-103">Changes made by Grant-CsSetupPermission in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ce535-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ce535-104">

<span> </span></span></span>

<span data-ttu-id="ce535-105">_**Dernière modification de la rubrique :** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="ce535-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="ce535-106">Pour déléguer le programme d’installation, vous pouvez accorder des autorisations au groupe universel RTCUniversalServerAdmins pour une unité d’organisation Active Directory spécifique (UO), ce qui permet aux membres du groupe RTCUniversalServerAdmins dans cette UO d’installer Lync Server 2013 dans le domaine spécifié sans être membre du groupe administrateurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="ce535-106">To delegate setup, you can grant permissions to the RTCUniversalServerAdmins universal group for a specific Active Directory organizational unit (OU), enabling members of the RTCUniversalServerAdmins group in that OU to install Lync Server 2013 in the specified domain without being members of the Domain Admins group.</span></span>

<span data-ttu-id="ce535-107">L’applet de commande **Grant-CsSetupPermission** accorde aux autorisations de groupe RTCUniversalServerAdmins sur une unité d’organisation, comme indiqué dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="ce535-107">The **Grant-CsSetupPermission** cmdlet grants the RTCUniversalServerAdmins group permissions on an OU, as specified in the following table:</span></span>

### <a name="permissions-granted-to-objects-in-the-ou"></a><span data-ttu-id="ce535-108">Autorisations accordées aux objets dans l’unité d’organisation</span><span class="sxs-lookup"><span data-stu-id="ce535-108">Permissions granted to Objects in the OU</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce535-109">Les autorisations s’appliquent à :</span><span class="sxs-lookup"><span data-stu-id="ce535-109">Permissions apply to:</span></span></th>
<th><span data-ttu-id="ce535-110">Les autorisations accordées sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce535-110">Permissions granted are:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce535-111">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="ce535-111">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="ce535-112">Accès spécial :</span><span class="sxs-lookup"><span data-stu-id="ce535-112">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="ce535-113">Lire servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ce535-113">Read servicePrincipalName</span></span></p></li>
<li><p><span data-ttu-id="ce535-114">Écrire le servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ce535-114">Write servicePrincipalName</span></span></p></li>
<li><p><span data-ttu-id="ce535-115">Supprimer l’arborescence</span><span class="sxs-lookup"><span data-stu-id="ce535-115">Delete tree</span></span></p></li>
<li><p><span data-ttu-id="ce535-116">Répliquer les modifications de l’annuaire</span><span class="sxs-lookup"><span data-stu-id="ce535-116">Replicating directory changes</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce535-117">Objets serviceConnectionPoint descendants</span><span class="sxs-lookup"><span data-stu-id="ce535-117">Descendant serviceConnectionPoint objects</span></span></p></td>
<td><p><span data-ttu-id="ce535-118">Accès spécial :</span><span class="sxs-lookup"><span data-stu-id="ce535-118">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="ce535-119">Autorisations de lecture</span><span class="sxs-lookup"><span data-stu-id="ce535-119">Read permissions</span></span></p></li>
<li><p><span data-ttu-id="ce535-120">Autorisations d’écriture</span><span class="sxs-lookup"><span data-stu-id="ce535-120">Write permissions</span></span></p></li>
<li><p><span data-ttu-id="ce535-121">Créer un enfant</span><span class="sxs-lookup"><span data-stu-id="ce535-121">Create child</span></span></p></li>
<li><p><span data-ttu-id="ce535-122">Supprimer un enfant</span><span class="sxs-lookup"><span data-stu-id="ce535-122">Delete child</span></span></p></li>
<li><p><span data-ttu-id="ce535-123">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="ce535-123">List contents</span></span></p></li>
<li><p><span data-ttu-id="ce535-124">Propriété Write</span><span class="sxs-lookup"><span data-stu-id="ce535-124">Write property</span></span></p></li>
<li><p><span data-ttu-id="ce535-125">Propriété de lecture</span><span class="sxs-lookup"><span data-stu-id="ce535-125">Read property</span></span></p></li>
<li><p><span data-ttu-id="ce535-126">Supprimer l’arborescence</span><span class="sxs-lookup"><span data-stu-id="ce535-126">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce535-127">Objets enfants msRTCSIP-Server</span><span class="sxs-lookup"><span data-stu-id="ce535-127">Descendant msRTCSIP-Server objects</span></span></p></td>
<td><p><span data-ttu-id="ce535-128">Accès spécial :</span><span class="sxs-lookup"><span data-stu-id="ce535-128">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="ce535-129">Propriété Write</span><span class="sxs-lookup"><span data-stu-id="ce535-129">Write property</span></span></p></li>
<li><p><span data-ttu-id="ce535-130">Propriété de lecture</span><span class="sxs-lookup"><span data-stu-id="ce535-130">Read property</span></span></p></li>
<li><p><span data-ttu-id="ce535-131">Supprimer l’arborescence</span><span class="sxs-lookup"><span data-stu-id="ce535-131">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce535-132">Objets enfants msRTCSIP-webcomposants</span><span class="sxs-lookup"><span data-stu-id="ce535-132">Descendant msRTCSIP-WebComponents objects</span></span></p></td>
<td><p><span data-ttu-id="ce535-133">Accès spécial :</span><span class="sxs-lookup"><span data-stu-id="ce535-133">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="ce535-134">Propriété Write</span><span class="sxs-lookup"><span data-stu-id="ce535-134">Write property</span></span></p></li>
<li><p><span data-ttu-id="ce535-135">Propriété de lecture</span><span class="sxs-lookup"><span data-stu-id="ce535-135">Read property</span></span></p></li>
<li><p><span data-ttu-id="ce535-136">Supprimer l’arborescence</span><span class="sxs-lookup"><span data-stu-id="ce535-136">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce535-137">Objets descendants msRTCSIP-MCU</span><span class="sxs-lookup"><span data-stu-id="ce535-137">Descendant msRTCSIP-MCU objects</span></span></p></td>
<td><p><span data-ttu-id="ce535-138">Accès spécial :</span><span class="sxs-lookup"><span data-stu-id="ce535-138">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="ce535-139">Propriété Write</span><span class="sxs-lookup"><span data-stu-id="ce535-139">Write property</span></span></p></li>
<li><p><span data-ttu-id="ce535-140">Propriété de lecture</span><span class="sxs-lookup"><span data-stu-id="ce535-140">Read property</span></span></p></li>
<li><p><span data-ttu-id="ce535-141">Supprimer l’arborescence</span><span class="sxs-lookup"><span data-stu-id="ce535-141">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce535-142">Objets MediationServer en descendant</span><span class="sxs-lookup"><span data-stu-id="ce535-142">Descendant msRTCSIP-MediationServer objects</span></span></p></td>
<td><p><span data-ttu-id="ce535-143">Accès spécial :</span><span class="sxs-lookup"><span data-stu-id="ce535-143">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="ce535-144">Propriété Write</span><span class="sxs-lookup"><span data-stu-id="ce535-144">Write property</span></span></p></li>
<li><p><span data-ttu-id="ce535-145">Propriété de lecture</span><span class="sxs-lookup"><span data-stu-id="ce535-145">Read property</span></span></p></li>
<li><p><span data-ttu-id="ce535-146">Supprimer l’arborescence</span><span class="sxs-lookup"><span data-stu-id="ce535-146">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce535-147">Objets ApplicationServer en descendant</span><span class="sxs-lookup"><span data-stu-id="ce535-147">Descendant msRTCSIP-ApplicationServer objects</span></span></p></td>
<td><p><span data-ttu-id="ce535-148">Accès spécial :</span><span class="sxs-lookup"><span data-stu-id="ce535-148">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="ce535-149">Propriété Write</span><span class="sxs-lookup"><span data-stu-id="ce535-149">Write property</span></span></p></li>
<li><p><span data-ttu-id="ce535-150">Propriété de lecture</span><span class="sxs-lookup"><span data-stu-id="ce535-150">Read property</span></span></p></li>
<li><p><span data-ttu-id="ce535-151">Supprimer l’arborescence</span><span class="sxs-lookup"><span data-stu-id="ce535-151">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce535-152">Objets descendants de msRTCSIP-ConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="ce535-152">Descendant msRTCSIP-ConnectionPoint objects</span></span></p></td>
<td><p><span data-ttu-id="ce535-153">Accès spécial :</span><span class="sxs-lookup"><span data-stu-id="ce535-153">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="ce535-154">Propriété Write</span><span class="sxs-lookup"><span data-stu-id="ce535-154">Write property</span></span></p></li>
<li><p><span data-ttu-id="ce535-155">Propriété de lecture</span><span class="sxs-lookup"><span data-stu-id="ce535-155">Read property</span></span></p></li>
<li><p><span data-ttu-id="ce535-156">Supprimer l’arborescence</span><span class="sxs-lookup"><span data-stu-id="ce535-156">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce535-157">Objets ordinateur descendants</span><span class="sxs-lookup"><span data-stu-id="ce535-157">Descendant Computer objects</span></span></p></td>
<td><p><span data-ttu-id="ce535-158">Accès spécial pour serviceConnectionPoint :</span><span class="sxs-lookup"><span data-stu-id="ce535-158">Special access for serviceConnectionPoint:</span></span></p>
<ul>
<li><p><span data-ttu-id="ce535-159">Créer des objets enfants</span><span class="sxs-lookup"><span data-stu-id="ce535-159">Create child objects</span></span></p></li>
<li><p><span data-ttu-id="ce535-160">Supprimer des objets enfants</span><span class="sxs-lookup"><span data-stu-id="ce535-160">Delete child objects</span></span></p></li>
<li><p><span data-ttu-id="ce535-161">Supprimer l’arborescence</span><span class="sxs-lookup"><span data-stu-id="ce535-161">Delete tree</span></span></p></li>
</ul>
<p><span data-ttu-id="ce535-162">Accès spécial pour les informations publiques :</span><span class="sxs-lookup"><span data-stu-id="ce535-162">Special access for public information:</span></span></p>
<ul>
<li><p><span data-ttu-id="ce535-163">Propriété de lecture</span><span class="sxs-lookup"><span data-stu-id="ce535-163">Read property</span></span></p></li>
</ul>
<p><span data-ttu-id="ce535-164">Accès spécial pour le nom d’hôte DNS :</span><span class="sxs-lookup"><span data-stu-id="ce535-164">Special access for DNS host name:</span></span></p>
<ul>
<li><p><span data-ttu-id="ce535-165">Propriété de lecture</span><span class="sxs-lookup"><span data-stu-id="ce535-165">Read property</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="ce535-166">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ce535-166">


</div>

<span> </span>

</div>

</div>

</span></span></div>

