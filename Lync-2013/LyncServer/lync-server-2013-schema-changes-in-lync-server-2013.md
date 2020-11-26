---
title: 'Lync Server 2013 : modifications de schéma dans Lync Server 2013'
description: 'Lync Server 2013 : modifications de schéma dans Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema changes in Lync Server 2013
ms:assetid: d760cb93-77d4-4d64-adb7-416b808f36f8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398944(v=OCS.15)
ms:contentKeyID: 48185575
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9e914de48ace80fd2611f2d05b092894b11c534a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444923"
---
# <a name="schema-changes-in-lync-server-2013"></a><span data-ttu-id="b4ddd-103">Modifications de schéma dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b4ddd-103">Schema changes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b4ddd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b4ddd-104">

<span> </span></span></span>

<span data-ttu-id="b4ddd-105">_**Dernière modification de la rubrique :** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="b4ddd-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="b4ddd-106">Avant de déployer et d’utiliser Lync Server 2013, vous devez préparer les services de domaine Active Directory en étendant le schéma.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-106">Before you deploy and operate Lync Server 2013, you must prepare Active Directory Domain Services by extending the schema.</span></span> <span data-ttu-id="b4ddd-107">Les extensions de schéma ajoutent les classes et attributs requis par Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-107">The schema extensions add the classes and attributes that are required by Lync Server 2013.</span></span>

<span data-ttu-id="b4ddd-108">Lync Server 2013 nécessite plusieurs classes et attributs, et modifie quelques classes et attributs existants.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-108">Lync Server 2013 requires several new classes and attributes and modifies some existing classes and attributes.</span></span> <span data-ttu-id="b4ddd-109">Par ailleurs, de nombreuses informations de configuration pour Lync Server 2013 sont stockées dans le magasin de gestion central plutôt que dans AD DS comme dans les versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-109">In addition, much configuration information for Lync Server 2013 is stored in the Central Management store instead of in AD DS as in previous versions.</span></span> <span data-ttu-id="b4ddd-110">Les informations suivantes sont toujours stockées dans AD DS dans Lync Server 2013 :</span><span class="sxs-lookup"><span data-stu-id="b4ddd-110">The following information is still stored in AD DS in Lync Server 2013:</span></span>

  - <span data-ttu-id="b4ddd-111">**Extensions de schéma**:</span><span class="sxs-lookup"><span data-stu-id="b4ddd-111">**Schema extensions**:</span></span>
    
      - <span data-ttu-id="b4ddd-112">Extensions de l’objet utilisateur</span><span class="sxs-lookup"><span data-stu-id="b4ddd-112">User object extensions</span></span>
    
      - <span data-ttu-id="b4ddd-113">Extensions pour les classes Office Communications Server 2007 et Office Communications Server 2007 R2 pour garantir la compatibilité descendante avec les versions précédentes prises en charge</span><span class="sxs-lookup"><span data-stu-id="b4ddd-113">Extensions for Office Communications Server 2007 and Office Communications Server 2007 R2 classes to maintain backward compatibility with supported previous versions</span></span>

<!-- end list -->

  - <span data-ttu-id="b4ddd-114">**Données** (stockées dans le schéma étendu de Lync Server et dans les classes de schéma existantes) :</span><span class="sxs-lookup"><span data-stu-id="b4ddd-114">**Data** (stored in Lync Server extended schema and in existing schema classes):</span></span>
    
      - <span data-ttu-id="b4ddd-115">URL (Uniform Resource Identifier) de l’utilisateur SIP et autres paramètres utilisateur</span><span class="sxs-lookup"><span data-stu-id="b4ddd-115">User SIP Uniform Resource Identifier (URI) and other user settings</span></span>
    
      - <span data-ttu-id="b4ddd-116">Objets de contact pour des applications telles que Response Group et attendant</span><span class="sxs-lookup"><span data-stu-id="b4ddd-116">Contact objects for applications such as Response Group and Conferencing Attendant</span></span>
    
      - <span data-ttu-id="b4ddd-117">Pointeur vers le magasin de gestion central</span><span class="sxs-lookup"><span data-stu-id="b4ddd-117">A pointer to the Central Management store</span></span>
    
      - <span data-ttu-id="b4ddd-118">Compte d’authentification Kerberos (objet facultatif de l’ordinateur)</span><span class="sxs-lookup"><span data-stu-id="b4ddd-118">Kerberos Authentication Account (an optional computer object)</span></span>

<span data-ttu-id="b4ddd-119">Cette rubrique décrit les modifications de schéma Active Directory requises par Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-119">This topic describes the Active Directory schema changes required by Lync Server 2013.</span></span> <span data-ttu-id="b4ddd-120">Elle ne décrit pas les modifications de schéma introduites par des versions antérieures d’Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-120">It does not describe schema changes that were introduced by previous versions of Office Communications Server.</span></span> <span data-ttu-id="b4ddd-121">Pour obtenir la liste des classes et leurs descriptions, voir [classes et descriptions de schéma dans Lync Server 2013](lync-server-2013-schema-classes-and-descriptions.md).</span><span class="sxs-lookup"><span data-stu-id="b4ddd-121">For a list of classes and their descriptions, see [Schema classes and descriptions in Lync Server 2013](lync-server-2013-schema-classes-and-descriptions.md).</span></span> <span data-ttu-id="b4ddd-122">Pour obtenir la liste des attributs et leur description, voir [attributs et descriptions de schéma dans Lync Server 2013](lync-server-2013-schema-attributes-and-descriptions.md).</span><span class="sxs-lookup"><span data-stu-id="b4ddd-122">For a list of attributes and their descriptions, see [Schema attributes and descriptions in Lync Server 2013](lync-server-2013-schema-attributes-and-descriptions.md).</span></span> <span data-ttu-id="b4ddd-123">Pour obtenir la liste des classes avec les attributs qu’ils peuvent contenir, voir [attributs de schéma par classe dans Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span><span class="sxs-lookup"><span data-stu-id="b4ddd-123">For a list of classes with the attributes they may contain, see [Schema attributes by class in Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span></span>

<span data-ttu-id="b4ddd-124">Le préfixe msRTCSIP identifie les classes et attributs spécifiques à Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-124">The msRTCSIP prefix identifies classes and attributes that are specific to Lync Server.</span></span>

<div>

## <a name="new-active-directory-attributes"></a><span data-ttu-id="b4ddd-125">Nouveaux attributs Active Directory</span><span class="sxs-lookup"><span data-stu-id="b4ddd-125">New Active Directory Attributes</span></span>

<span data-ttu-id="b4ddd-126">Le tableau suivant décrit les attributs Active Directory ajoutés par Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-126">The following table describes the Active Directory attributes that are added by Lync Server 2013.</span></span>

### <a name="attributes-added-by-lync-server-2013"></a><span data-ttu-id="b4ddd-127">Attributs ajoutés par Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b4ddd-127">Attributes Added by Lync Server 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4ddd-128">Attribut</span><span class="sxs-lookup"><span data-stu-id="b4ddd-128">Attribute</span></span></th>
<th><span data-ttu-id="b4ddd-129">Description</span><span class="sxs-lookup"><span data-stu-id="b4ddd-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4ddd-130">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="b4ddd-130">msExchUserHoldPolicies</span></span></p></td>
<td><p><span data-ttu-id="b4ddd-131">Cet attribut à plusieurs valeurs contient des identificateurs pour les stratégies de conservation qui s’appliquent à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-131">This multi-value attribute holds identifiers for hold policies that apply to the user.</span></span> <span data-ttu-id="b4ddd-132">Les stratégies de blocage préservent les éléments de boîte aux lettres de l’utilisateur pendant la durée de la conservation.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-132">Hold policies preserve mailbox items for the user for the duration of the hold.</span></span> <span data-ttu-id="b4ddd-133">Cet attribut est partagé avec Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-133">This attribute is shared with Exchange 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4ddd-134">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="b4ddd-134">msRTCSIP-UserRoutingGroupId</span></span></p></td>
<td><p><span data-ttu-id="b4ddd-135">Il s’agit de l’ID du groupe de routage SIP.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-135">This is the SIP routing group ID.</span></span> <span data-ttu-id="b4ddd-136">Les utilisateurs du même groupe seront enregistrés sur le même serveur principal.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-136">Users in the same group will register to the same Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4ddd-137">msRTCSIP-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="b4ddd-137">msRTCSIP-MirrorBackEndServer</span></span></p></td>
<td><p><span data-ttu-id="b4ddd-138">Cet attribut est utilisé pour stocker le serveur principal SQL Server utilisé par le pool frontal.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-138">This attribute is used to store the mirrored SQL Server backend used by the Front End pool.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="modified-active-directory-classes"></a><span data-ttu-id="b4ddd-139">Classes Active Directory modifiées</span><span class="sxs-lookup"><span data-stu-id="b4ddd-139">Modified Active Directory Classes</span></span>

<span data-ttu-id="b4ddd-140">Le tableau suivant décrit les classes Active Directory modifiées par Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-140">The following table describes the Active Directory classes that are modified by Lync Server 2013.</span></span>

### <a name="classes-modified-by-lync-server-2013"></a><span data-ttu-id="b4ddd-141">Classes modifiées par Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b4ddd-141">Classes Modified by Lync Server 2013</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4ddd-142">Cours</span><span class="sxs-lookup"><span data-stu-id="b4ddd-142">Class</span></span></th>
<th><span data-ttu-id="b4ddd-143">Modification</span><span class="sxs-lookup"><span data-stu-id="b4ddd-143">Change</span></span></th>
<th><span data-ttu-id="b4ddd-144">Classe ou attribut</span><span class="sxs-lookup"><span data-stu-id="b4ddd-144">Class or Attribute</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4ddd-145">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="b4ddd-145">User</span></span></p></td>
<td><p><span data-ttu-id="b4ddd-146">Ajouter : mayContain</span><span class="sxs-lookup"><span data-stu-id="b4ddd-146">add: mayContain</span></span></p>
<p><span data-ttu-id="b4ddd-147">Ajouter : mayContain</span><span class="sxs-lookup"><span data-stu-id="b4ddd-147">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="b4ddd-148">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="b4ddd-148">ProxyAddresses</span></span></p>
<p><span data-ttu-id="b4ddd-149">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="b4ddd-149">msRTCSIP-UserRoutingGroupId</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4ddd-150">Locuteur</span><span class="sxs-lookup"><span data-stu-id="b4ddd-150">Contact</span></span></p></td>
<td><p><span data-ttu-id="b4ddd-151">Ajouter : mayContain</span><span class="sxs-lookup"><span data-stu-id="b4ddd-151">add: mayContain</span></span></p>
<p><span data-ttu-id="b4ddd-152">Ajouter : mayContain</span><span class="sxs-lookup"><span data-stu-id="b4ddd-152">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="b4ddd-153">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="b4ddd-153">ProxyAddresses</span></span></p>
<p><span data-ttu-id="b4ddd-154">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="b4ddd-154">msRTCSIP-UserRoutingGroupId</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4ddd-155">Mail-Recipient</span><span class="sxs-lookup"><span data-stu-id="b4ddd-155">Mail-Recipient</span></span></p></td>
<td><p><span data-ttu-id="b4ddd-156">Ajouter : mayContain</span><span class="sxs-lookup"><span data-stu-id="b4ddd-156">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="b4ddd-157">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="b4ddd-157">msExchUserHoldPolicies</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4ddd-158">msRTCSIP-GlobalTopologySetting</span><span class="sxs-lookup"><span data-stu-id="b4ddd-158">msRTCSIP-GlobalTopologySetting</span></span></p></td>
<td><p><span data-ttu-id="b4ddd-159">Ajouter : mayContain</span><span class="sxs-lookup"><span data-stu-id="b4ddd-159">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="b4ddd-160">msRTCSIP-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="b4ddd-160">msRTCSIP-MirrorBackEndServer</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b4ddd-161">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b4ddd-161">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

