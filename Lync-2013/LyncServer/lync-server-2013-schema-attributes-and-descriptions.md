---
title: 'Lync Server 2013 : attributs et descriptions de schéma'
description: 'Lync Server 2013 : attributs et descriptions de schéma.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema attributes and descriptions
ms:assetid: b009df76-9c22-471d-b57a-bda009a98261
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412841(v=OCS.15)
ms:contentKeyID: 48185083
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 18888d20a772b3e84970e7d874bd6b6964affc75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444958"
---
# <a name="schema-attributes-and-descriptions-in-lync-server-2013"></a><span data-ttu-id="85b40-103">Attributs et descriptions de schéma dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85b40-103">Schema attributes and descriptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85b40-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85b40-104">

<span> </span></span></span>

<span data-ttu-id="85b40-105">_**Dernière modification de la rubrique :** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="85b40-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="85b40-106">Cette section décrit tous les attributs de schéma utilisés par Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="85b40-106">This section describes all the schema attributes used by Lync Server 2013.</span></span> <span data-ttu-id="85b40-107">Pour les classes associées à des attributs, voir [attributs de schéma par classe dans Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span><span class="sxs-lookup"><span data-stu-id="85b40-107">For the classes associated with attributes, see [Schema attributes by class in Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span></span> <span data-ttu-id="85b40-108">Pour obtenir la liste des classes et attributs qui sont des nouveautés de Lync Server 2013, voir [modifications de schéma dans Lync server 2013](lync-server-2013-schema-changes-in-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="85b40-108">For a list of classes and attributes that are new in Lync Server 2013, see [Schema changes in Lync Server 2013](lync-server-2013-schema-changes-in-lync-server-2013.md).</span></span>

<span data-ttu-id="85b40-109">Les attributs qui sont des paires liées sont spécifiés en tant que liens de renvoi ou liens d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="85b40-109">Attributes that are linked pairs are specified as forward links or back links.</span></span> <span data-ttu-id="85b40-110">Un attribut qui fait référence à un autre objet est un lien de transfert ; l’attribut de l’autre objet qui fait référence au premier objet est un lien précédent.</span><span class="sxs-lookup"><span data-stu-id="85b40-110">An attribute that refers to another object is a forward link; the attribute of the other object that refers back to the first object is a back link.</span></span> <span data-ttu-id="85b40-111">Les liens de renvoi peuvent être mis à jour de façon à être en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="85b40-111">Forward links are updatable, while back links are read-only.</span></span>

<span data-ttu-id="85b40-112">Certains attributs ont une valeur de masque de bits.</span><span class="sxs-lookup"><span data-stu-id="85b40-112">Some attributes have a bit-mask value.</span></span> <span data-ttu-id="85b40-113">Pour ces attributs, chaque paramètre est représenté par un bit et la valeur décimale affichée représente la position en bits.</span><span class="sxs-lookup"><span data-stu-id="85b40-113">For these attributes, each setting is represented by a bit, and the displayed decimal value represents the bit position.</span></span> <span data-ttu-id="85b40-114">Les positions de bits commencent par le bit 0.</span><span class="sxs-lookup"><span data-stu-id="85b40-114">Bit positions start with bit 0.</span></span> <span data-ttu-id="85b40-115">Par exemple, 1 (binaire) est du bit 0 défini et 10000 (binaire) est le bit 4 défini.</span><span class="sxs-lookup"><span data-stu-id="85b40-115">For example, 1 (binary) is bit 0 set and 10000 (binary) is bit 4 set.</span></span> <span data-ttu-id="85b40-116">Chaque bit représente une propriété.</span><span class="sxs-lookup"><span data-stu-id="85b40-116">Each bit represents a property.</span></span> <span data-ttu-id="85b40-117">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="85b40-117">The following are some examples:</span></span>

  - <span data-ttu-id="85b40-118">10000 (binaire) a une valeur décimale de 16 (c’est-à-dire que le bit 4 est défini).</span><span class="sxs-lookup"><span data-stu-id="85b40-118">10000 (binary) has a decimal value of 16 (that is, bit 4 is set).</span></span>

  - <span data-ttu-id="85b40-119">100 millions (binaire) a une valeur décimale de 256 (c’est-à-dire que le bit 8 est défini).</span><span class="sxs-lookup"><span data-stu-id="85b40-119">100000000 (binary) has a decimal value of 256 (that is, bit 8 is set).</span></span>

  - <span data-ttu-id="85b40-120">1100 (binaire) a une valeur décimale de 12 (autrement dit, les bits 2 et 3 sont définis ; les propriétés représentées par les deux bits sont activées).</span><span class="sxs-lookup"><span data-stu-id="85b40-120">1100 (binary) has a decimal value of 12 (that is, bits 2 and 3 are set; properties represented by both bits are enabled).</span></span>

  - <span data-ttu-id="85b40-121">1111000001 (binaire) a une valeur décimale de 961 (autrement dit, les bits 0, 6, 7, 8 et 9 sont définis ; les propriétés de chacun de ces bits sont activées).</span><span class="sxs-lookup"><span data-stu-id="85b40-121">1111000001 (binary) has a decimal value of 961 (that is, bits 0, 6, 7, 8, and 9 are set; properties for each of these bits are enabled).</span></span>

<div id="sectionSection0" class="section">

### <a name="schema-attributes-for-lync-server-2013"></a><span data-ttu-id="85b40-122">Attributs de schéma pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85b40-122">Schema Attributes for Lync Server 2013</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85b40-123">Attribut</span><span class="sxs-lookup"><span data-stu-id="85b40-123">Attribute</span></span></th>
<th><span data-ttu-id="85b40-124">Description</span><span class="sxs-lookup"><span data-stu-id="85b40-124">Description</span></span></th>
<th><span data-ttu-id="85b40-125">Commentaires</span><span class="sxs-lookup"><span data-stu-id="85b40-125">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85b40-126">dnsHostName</span><span class="sxs-lookup"><span data-stu-id="85b40-126">dnsHostName</span></span></p></td>
<td><p><span data-ttu-id="85b40-127">Un attribut existant dans les services de domaine Active Directory, désormais associé aux classes <strong>msRTCSIP-pool</strong> et <strong>msRTCSIP-MonitoringServer</strong> .</span><span class="sxs-lookup"><span data-stu-id="85b40-127">An existing attribute in Active Directory Domain Services that is now associated with the <strong>msRTCSIP-Pool</strong> and <strong>msRTCSIP-MonitoringServer</strong> classes.</span></span> <span data-ttu-id="85b40-128">Cet attribut spécifie le nom de domaine complet (FQDN) d’un pool ou d’un serveur de surveillance.</span><span class="sxs-lookup"><span data-stu-id="85b40-128">This attribute specifies the fully qualified domain name (FQDN) of a pool or Monitoring Server.</span></span></p>
<p><span data-ttu-id="85b40-129">La valeur valide de chaque segment est de 63 caractères. une valeur valide pour le nom de domaine complet est de 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="85b40-129">A valid value for each segment is 63 characters; a valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="85b40-130">Nouveautés de Microsoft Office Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-130">New in Microsoft Office Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-131">msDS-SourceObjectDN</span><span class="sxs-lookup"><span data-stu-id="85b40-131">msDS-SourceObjectDN</span></span></p></td>
<td><p><span data-ttu-id="85b40-132">Cet attribut contient la représentation de chaîne du nom unique (DN) de l’objet d’une autre forêt qui correspond à cet objet.</span><span class="sxs-lookup"><span data-stu-id="85b40-132">This attribute contains the string representation of the distinguished name (DN) of the object in another forest that corresponds to this object.</span></span> <span data-ttu-id="85b40-133">Cet attribut est utilisé pour l’extension du groupe de distribution et la présence automatique.</span><span class="sxs-lookup"><span data-stu-id="85b40-133">This attribute is used for distribution group expansion and auto attendance.</span></span> <span data-ttu-id="85b40-134">Cet attribut est défini dans le schéma Active Directory par défaut de Windows Server 2003 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-134">This attribute is defined in the default Active Directory schema for Windows Server 2003 R2.</span></span></p>
<p><span data-ttu-id="85b40-135">Pour éviter d’avoir besoin d’une mise à niveau d’AD DS vers Windows Server 2003 R2, la préparation du schéma Active Directory étend le schéma Windows Server 2003 avec cette définition d’attribut.</span><span class="sxs-lookup"><span data-stu-id="85b40-135">To avoid requiring an upgrade of AD DS to Windows Server 2003 R2, Active Directory schema preparation extends the Windows Server 2003 schema with this attribute definition.</span></span></p></td>
<td><p><span data-ttu-id="85b40-136">Nouveautés de Microsoft Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-136">New in Microsoft Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-137">msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="85b40-137">msExchUCVoiceMailSettings</span></span></p></td>
<td><p><span data-ttu-id="85b40-138">Cet attribut à valeurs multiples contient les paramètres de la messagerie vocale.</span><span class="sxs-lookup"><span data-stu-id="85b40-138">This multi-valued attribute holds voice mail settings.</span></span> <span data-ttu-id="85b40-139">Cet attribut est partagé avec la messagerie unifiée Exchange.</span><span class="sxs-lookup"><span data-stu-id="85b40-139">This attribute is shared with Exchange Unified Messaging (UM).</span></span></p></td>
<td><p><span data-ttu-id="85b40-140">Nouveautés de Microsoft Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-140">New in Microsoft Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-141">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="85b40-141">msExchUserHoldPolicies</span></span></p></td>
<td><p><span data-ttu-id="85b40-142">Cet attribut à plusieurs valeurs contient des identificateurs pour les stratégies de conservation qui s’appliquent à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-142">This multi-value attribute holds identifiers for hold policies that apply to the user.</span></span> <span data-ttu-id="85b40-143">Les stratégies de blocage préservent les éléments de boîte aux lettres de l’utilisateur pendant la durée de la conservation.</span><span class="sxs-lookup"><span data-stu-id="85b40-143">Hold policies preserve mailbox items for the user for the duration of the hold.</span></span> <span data-ttu-id="85b40-144">Cet attribut est partagé avec Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="85b40-144">This attribute is shared with Exchange 2013.</span></span></p></td>
<td><p><span data-ttu-id="85b40-145">Nouveautés de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="85b40-145">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-146">msRTCSIP-AcpInfo</span><span class="sxs-lookup"><span data-stu-id="85b40-146">msRTCSIP-AcpInfo</span></span></p></td>
<td><p><span data-ttu-id="85b40-147">Cet attribut stocke les informations du fournisseur de services d’audioconférence pour un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-147">This attribute stores audio conferencing provider information for a user.</span></span></p></td>
<td><p><span data-ttu-id="85b40-148">Nouveautés de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-148">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-149">msRTCSIP-ApplicationDestination</span><span class="sxs-lookup"><span data-stu-id="85b40-149">msRTCSIP-ApplicationDestination</span></span></p></td>
<td><p><span data-ttu-id="85b40-150">Cet attribut pointe sur l’entrée de service approuvé pour le contact de l’application.</span><span class="sxs-lookup"><span data-stu-id="85b40-150">This attribute points to the trusted service entry for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="85b40-151">Nouveautés de Microsoft Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-151">New in Microsoft Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-152">msRTCSIP-ApplicationList</span><span class="sxs-lookup"><span data-stu-id="85b40-152">msRTCSIP-ApplicationList</span></span></p></td>
<td><p><span data-ttu-id="85b40-153">Cet attribut contient une liste des applications hébergées sur le serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="85b40-153">This attribute contains a list of hosted applications on the application server.</span></span></p></td>
<td><p><span data-ttu-id="85b40-154">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-154">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-155">msRTCSIP-ApplicationOptions</span><span class="sxs-lookup"><span data-stu-id="85b40-155">msRTCSIP-ApplicationOptions</span></span></p></td>
<td><p><span data-ttu-id="85b40-156">Cet attribut spécifie les options du contact de l’application.</span><span class="sxs-lookup"><span data-stu-id="85b40-156">This attribute specifies the options for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="85b40-157">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-157">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-158">msRTCSIP-ApplicationPrimaryLanguage</span><span class="sxs-lookup"><span data-stu-id="85b40-158">msRTCSIP-ApplicationPrimaryLanguage</span></span></p></td>
<td><p><span data-ttu-id="85b40-159">Cet attribut contient la langue principale du contact de l’application.</span><span class="sxs-lookup"><span data-stu-id="85b40-159">This attribute contains the primary language for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="85b40-160">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-160">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-161">msRTCSIP-ApplicationSecondaryLanguages</span><span class="sxs-lookup"><span data-stu-id="85b40-161">msRTCSIP-ApplicationSecondaryLanguages</span></span></p></td>
<td><p><span data-ttu-id="85b40-162">Cet attribut à plusieurs valeurs contient les langues secondaires du contact de l’application.</span><span class="sxs-lookup"><span data-stu-id="85b40-162">This multiple value attribute contains the secondary languages for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="85b40-163">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-163">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-164">msRTCSIP-ApplicationServerBL</span><span class="sxs-lookup"><span data-stu-id="85b40-164">msRTCSIP-ApplicationServerBL</span></span></p></td>
<td><p><span data-ttu-id="85b40-165">Cet attribut contient une liste des serveurs d’application appartenant à ce pool.</span><span class="sxs-lookup"><span data-stu-id="85b40-165">This attribute contains a list of application servers that belong to this pool.</span></span> <span data-ttu-id="85b40-166">Le lien transférer correspondant à cet attribut de lien précédent est <strong>msRTCSIP-ApplicationServerPoolLink</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-166">The corresponding forward link to this back link attribute is <strong>msRTCSIP-ApplicationServerPoolLink</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-167">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-167">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-168">msRTCSIP-ApplicationServerPoolLink</span><span class="sxs-lookup"><span data-stu-id="85b40-168">msRTCSIP-ApplicationServerPoolLink</span></span></p></td>
<td><p><span data-ttu-id="85b40-169">Cet attribut pointe vers le pool auquel appartient ce serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="85b40-169">This attribute points to the pool to which this application server belongs.</span></span> <span data-ttu-id="85b40-170">Il s’agit du lien transférer.</span><span class="sxs-lookup"><span data-stu-id="85b40-170">This is the forward link.</span></span> <span data-ttu-id="85b40-171">Le lien inverse correspondant est <strong>msRTCSIP-ApplicationServerBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-171">The corresponding backward link is <strong>msRTCSIP-ApplicationServerBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-172">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-172">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-173">msRTCSIP-ArchiveDefault (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-173">msRTCSIP-ArchiveDefault (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="85b40-174">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-174">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="85b40-175">Obsolète dans Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-175">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-176">msRTCSIP-ArchiveDefaultFlags (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-176">msRTCSIP-ArchiveDefaultFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-177">Cet attribut spécifie la valeur par défaut globale dans la limite de la forêt pour l’archivage de toutes les communications utilisateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-177">This attribute specifies the global default within the forest boundary for archiving all user communications.</span></span> <span data-ttu-id="85b40-178">Cette opération est appliquée par la couche agent d’archivage.</span><span class="sxs-lookup"><span data-stu-id="85b40-178">This is enforced by the archiving agent layer.</span></span> <span data-ttu-id="85b40-179">La plage de valeurs de cet attribut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="85b40-179">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-180"><strong>Vrai</strong>: archiver tous les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="85b40-180"><strong>TRUE</strong>: Archive all users</span></span></p></li>
<li><p><span data-ttu-id="85b40-181"><strong>False</strong>: ne pas archiver tous les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="85b40-181"><strong>FALSE</strong>: Do not archive all users</span></span></p></li>
</ul>
<p><span data-ttu-id="85b40-182">Cet attribut contrôle globalement, au sein de la frontière de la forêt, le mode d’archivage des communications utilisateur au sein d’un réseau interne.</span><span class="sxs-lookup"><span data-stu-id="85b40-182">This attribute globally controls, within the forest boundary, how user communications within an internal network are archived.</span></span></p>
<p><span data-ttu-id="85b40-183"><strong>Comportement 2005 de Live Communications Server (désormais obsolète)</strong></span><span class="sxs-lookup"><span data-stu-id="85b40-183"><strong>Live Communications Server 2005 behavior (now retired)</strong></span></span></p>
<p><span data-ttu-id="85b40-184">La plage de valeurs de cet attribut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="85b40-184">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-185">0 : archiver le corps du message [bit 0]</span><span class="sxs-lookup"><span data-stu-id="85b40-185">0: Archive the message body [bit 0]</span></span></p></li>
<li><p><span data-ttu-id="85b40-186">1 : ne pas archiver le corps du message [bit 0]</span><span class="sxs-lookup"><span data-stu-id="85b40-186">1: Do not archive the message body [bit 0]</span></span></p></li>
</ul>
<p><span data-ttu-id="85b40-187"><strong>Comportement 2007 d’Office Communications Server</strong></span><span class="sxs-lookup"><span data-stu-id="85b40-187"><strong>Office Communications Server 2007 behavior</strong></span></span></p>
<p><span data-ttu-id="85b40-188">La plage de valeurs de cet attribut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="85b40-188">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-189">0 : ArchiveFederationDefaultWithoutBody (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-189">0: ArchiveFederationDefaultWithoutBody (retired)</span></span></p></li>
<li><p><span data-ttu-id="85b40-190">1-2 : ArchiveInternalCommunications</span><span class="sxs-lookup"><span data-stu-id="85b40-190">1-2: ArchiveInternalCommunications</span></span></p></li>
<li><p><span data-ttu-id="85b40-191">3-4 : ArchiveFederatedCommunications</span><span class="sxs-lookup"><span data-stu-id="85b40-191">3-4: ArchiveFederatedCommunications</span></span></p></li>
<li><p><span data-ttu-id="85b40-192">5 : RecordPresenceRegistrations</span><span class="sxs-lookup"><span data-stu-id="85b40-192">5: RecordPresenceRegistrations</span></span></p></li>
<li><p><span data-ttu-id="85b40-193">6 : RecordIMCallDetails</span><span class="sxs-lookup"><span data-stu-id="85b40-193">6: RecordIMCallDetails</span></span></p></li>
<li><p><span data-ttu-id="85b40-194">7 : RecordGroupIMCallDetails</span><span class="sxs-lookup"><span data-stu-id="85b40-194">7: RecordGroupIMCallDetails</span></span></p></li>
<li><p><span data-ttu-id="85b40-195">8 : RecordFileTransferInstances</span><span class="sxs-lookup"><span data-stu-id="85b40-195">8: RecordFileTransferInstances</span></span></p></li>
<li><p><span data-ttu-id="85b40-196">9 : RecordAudioCallDetails</span><span class="sxs-lookup"><span data-stu-id="85b40-196">9: RecordAudioCallDetails</span></span></p></li>
<li><p><span data-ttu-id="85b40-197">10 : RecordVideoCallDetails</span><span class="sxs-lookup"><span data-stu-id="85b40-197">10: RecordVideoCallDetails</span></span></p></li>
<li><p><span data-ttu-id="85b40-198">11 : RecordRemoteAssistanceCallDetails</span><span class="sxs-lookup"><span data-stu-id="85b40-198">11: RecordRemoteAssistanceCallDetails</span></span></p></li>
<li><p><span data-ttu-id="85b40-199">12 : RecordApplicationSharingDetails</span><span class="sxs-lookup"><span data-stu-id="85b40-199">12: RecordApplicationSharingDetails</span></span></p></li>
<li><p><span data-ttu-id="85b40-200">13 : RecordMeetingInstantiations</span><span class="sxs-lookup"><span data-stu-id="85b40-200">13: RecordMeetingInstantiations</span></span></p></li>
<li><p><span data-ttu-id="85b40-201">14 : RecordMeetingJoins</span><span class="sxs-lookup"><span data-stu-id="85b40-201">14: RecordMeetingJoins</span></span></p></li>
<li><p><span data-ttu-id="85b40-202">15 : RecordDataJoins</span><span class="sxs-lookup"><span data-stu-id="85b40-202">15: RecordDataJoins</span></span></p></li>
<li><p><span data-ttu-id="85b40-203">16 : RecordAVJoins</span><span class="sxs-lookup"><span data-stu-id="85b40-203">16: RecordAVJoins</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="85b40-204">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-204">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="85b40-205">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-205">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-206">msRTCSIP-ArchiveFederationDefault (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-206">msRTCSIP-ArchiveFederationDefault (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="85b40-207">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-207">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="85b40-208">Obsolète dans Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-208">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-209">msRTCSIP-ArchiveFederationDefaultFlags (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-209">msRTCSIP-ArchiveFederationDefaultFlags (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="85b40-210">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-210">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="85b40-211">Obsolète dans Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-211">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-212">msRTCSIP-ArchivingEnabled</span><span class="sxs-lookup"><span data-stu-id="85b40-212">msRTCSIP-ArchivingEnabled</span></span></p></td>
<td><p><span data-ttu-id="85b40-213">Cet attribut est un entier utilisé comme champ de bits pour contrôler si les communications d’un utilisateur unique doivent être archivées.</span><span class="sxs-lookup"><span data-stu-id="85b40-213">This attribute is an integer used as a bit field to control whether a single user’s communications are to be archived.</span></span> <span data-ttu-id="85b40-214">Ce contrôle est appliqué par la couche de l’agent d’archivage.</span><span class="sxs-lookup"><span data-stu-id="85b40-214">This control is enforced by the archiving agent layer.</span></span> <span data-ttu-id="85b40-215">Il est marqué pour la réplication de catalogue global.</span><span class="sxs-lookup"><span data-stu-id="85b40-215">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="85b40-216">L’objectif de cet attribut est spécifique à un utilisateur ou à un contact unique.</span><span class="sxs-lookup"><span data-stu-id="85b40-216">The scope of this attribute is specific to a single user or contact.</span></span> <span data-ttu-id="85b40-217">Les valeurs valides (et positions de bits associées) dans Lync Server sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="85b40-217">The valid values (and associated bit positions) in Lync Server are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-218">0 : do not Archive (aucun jeu de bits)</span><span class="sxs-lookup"><span data-stu-id="85b40-218">0: Do not archive (no bit set)</span></span></p></li>
<li><p><span data-ttu-id="85b40-219">1 : retrait (position de bit 0)</span><span class="sxs-lookup"><span data-stu-id="85b40-219">1: Retired (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="85b40-220">2 : obsolète (position de bit 1)</span><span class="sxs-lookup"><span data-stu-id="85b40-220">2: Retired (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="85b40-221">4 : archiver des communications internes (position binaire 2)</span><span class="sxs-lookup"><span data-stu-id="85b40-221">4: Archive internal communications (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="85b40-222">8 : archiver des communications fédérées (position binaire 3)</span><span class="sxs-lookup"><span data-stu-id="85b40-222">8: Archive federated communications (bit position 3)</span></span></p></li>
</ul>
<p><span data-ttu-id="85b40-223">Les valeurs précédemment valides dans Live Communications Server 2005 sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="85b40-223">Previously valid values in Live Communications Server 2005 are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-224">0 : utilisez la valeur par défaut définie par <strong>msRTCSIP-ArchiveDefault</strong> et <strong>msRTCSIP-ArchiveFederation</strong> dans cet ordre de priorité :</span><span class="sxs-lookup"><span data-stu-id="85b40-224">0:Use the default value defined by <strong>msRTCSIP-ArchiveDefault</strong> and <strong>msRTCSIP-ArchiveFederation</strong> in this order of precedence:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-225">1 : Archive</span><span class="sxs-lookup"><span data-stu-id="85b40-225">1: Archive</span></span></p></li>
<li><p><span data-ttu-id="85b40-226">2 : ne pas archiver</span><span class="sxs-lookup"><span data-stu-id="85b40-226">2: Do not archive</span></span></p></li>
<li><p><span data-ttu-id="85b40-227">3 : archiver sans le corps du message</span><span class="sxs-lookup"><span data-stu-id="85b40-227">3: Archive without the message body</span></span></p></li>
</ul></li>
</ul></td>
<td><p><span data-ttu-id="85b40-228">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-228">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-229">msRTCSIP-ArchivingServerData (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-229">msRTCSIP-ArchivingServerData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-230">Cet attribut est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85b40-230">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="85b40-231">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-231">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-232">msRTCSIP-ArchivingServerVersion (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-232">msRTCSIP-ArchivingServerVersion (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-233">Cet attribut définit la version du service d’archivage.</span><span class="sxs-lookup"><span data-stu-id="85b40-233">This attribute defines the version of the Archiving service.</span></span> <span data-ttu-id="85b40-234">Il s’agit d’un monotonously qui augmente de manière à chaque publication officielle du produit.</span><span class="sxs-lookup"><span data-stu-id="85b40-234">This attribute is a monotonously increasing integer type that increments with each official product release.</span></span> <span data-ttu-id="85b40-235">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="85b40-235">The possible valid values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-236">Non défini : Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="85b40-236">Undefined: Live Communications Server 2003</span></span></p>
<p>                 <span data-ttu-id="85b40-237">Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="85b40-237">Live Communications Server 2005</span></span></p>
<p>                 <span data-ttu-id="85b40-238">Live Communications Server 2005 avec SP1</span><span class="sxs-lookup"><span data-stu-id="85b40-238">Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="85b40-239">3 : Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="85b40-239">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="85b40-240">4 : Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="85b40-240">4: Office Communications Server 2007 R2</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="85b40-241">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-241">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-242">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-242">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-243">msRTCSIP-BackEndServer</span><span class="sxs-lookup"><span data-stu-id="85b40-243">msRTCSIP-BackEndServer</span></span></p></td>
<td><p><span data-ttu-id="85b40-244">Cet attribut spécifie le nom de domaine complet (FQDN) du serveur principal du pool.</span><span class="sxs-lookup"><span data-stu-id="85b40-244">This attribute specifies the FQDN of the Back End Server of the pool.</span></span> <span data-ttu-id="85b40-245">Étant donné qu’il ne peut exister qu’un serveur principal unique par pool, il s’agit d’un attribut à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="85b40-245">Because there can only be a single Back End Server per pool, this is a single-valued attribute.</span></span></p>
<p><span data-ttu-id="85b40-246">La valeur valide de chaque segment est de 63 caractères. la valeur valide pour le nom de domaine complet est de 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="85b40-246">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="85b40-247">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-247">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-248">msRTCSIP-ConferenceDirectoryHomePool</span><span class="sxs-lookup"><span data-stu-id="85b40-248">msRTCSIP-ConferenceDirectoryHomePool</span></span></p></td>
<td><p><span data-ttu-id="85b40-249">Cet attribut contient l’identificateur du pool qui héberge l’annuaire de conférences.</span><span class="sxs-lookup"><span data-stu-id="85b40-249">This attribute contains the identifier of the pool that hosts the conference directory.</span></span></p></td>
<td><p><span data-ttu-id="85b40-250">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-250">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-251">msRTCSIP-ConferenceDirectoryId</span><span class="sxs-lookup"><span data-stu-id="85b40-251">msRTCSIP-ConferenceDirectoryId</span></span></p></td>
<td><p><span data-ttu-id="85b40-252">Cet attribut contient l’identificateur d’un annuaire de conférences.</span><span class="sxs-lookup"><span data-stu-id="85b40-252">This attribute contains the identifier of a conference directory.</span></span></p></td>
<td><p><span data-ttu-id="85b40-253">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-253">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-254">msRTCSIP-ConferenceDirectoryTargetPool</span><span class="sxs-lookup"><span data-stu-id="85b40-254">msRTCSIP-ConferenceDirectoryTargetPool</span></span></p></td>
<td><p><span data-ttu-id="85b40-255">Cet attribut contient l’identificateur du pool dans lequel le répertoire de conférences est déplacé.</span><span class="sxs-lookup"><span data-stu-id="85b40-255">This attribute contains the identifier of the pool to which the conference directory is being moved.</span></span></p></td>
<td><p><span data-ttu-id="85b40-256">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-256">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-257">msRTCSIP-par défaut</span><span class="sxs-lookup"><span data-stu-id="85b40-257">msRTCSIP-Default</span></span></p></td>
<td><p><span data-ttu-id="85b40-258">Cet attribut booléen définit si l’utilisation du téléphone est une utilisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="85b40-258">This Boolean attribute defines whether the phone usage is a default usage.</span></span> <span data-ttu-id="85b40-259">Si cet attribut est défini sur <strong>true</strong>, l’utilisation du téléphone est une utilisation par défaut qui ne peut pas être supprimée par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-259">If this attribute is set to <strong>TRUE</strong>, the phone usage is a default usage and cannot be deleted by the administrator.</span></span> <span data-ttu-id="85b40-260">Si cet attribut est défini sur <strong>false</strong>, l’utilisation peut être supprimée.</span><span class="sxs-lookup"><span data-stu-id="85b40-260">If this attribute is set to <strong>FALSE</strong>, the usage can be deleted.</span></span></p></td>
<td><p><span data-ttu-id="85b40-261">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-261">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-262">msRTCSIP-DefaultCWAExternalURL</span><span class="sxs-lookup"><span data-stu-id="85b40-262">msRTCSIP-DefaultCWAExternalURL</span></span></p></td>
<td><p><span data-ttu-id="85b40-263">Cet attribut identifie l’URL Communicator Web Access pour les utilisateurs extérieurs à l’organisation.</span><span class="sxs-lookup"><span data-stu-id="85b40-263">This attribute identifies the Communicator Web Access URL for users who are outside the organization.</span></span></p></td>
<td><p><span data-ttu-id="85b40-264">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-264">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-265">msRTCSIP-DefaultCWAInternalURL</span><span class="sxs-lookup"><span data-stu-id="85b40-265">msRTCSIP-DefaultCWAInternalURL</span></span></p></td>
<td><p><span data-ttu-id="85b40-266">Cet attribut identifie l’URL Communicator Web Access pour les utilisateurs qui se trouvent au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="85b40-266">This attribute identifies the Communicator Web Access URL for users who are inside the organization.</span></span></p></td>
<td><p><span data-ttu-id="85b40-267">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-267">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-268">msRTCSIP-DefaultLocationProfileLink (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-268">msRTCSIP-DefaultLocationProfileLink (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-269">Cet attribut à valeur unique contient le nom unique (DN) d’un objet de classe de profil d’emplacement qui lui est affecté.</span><span class="sxs-lookup"><span data-stu-id="85b40-269">This single-valued attribute contains the distinguished name (DN) of a location profile class object assigned to it.</span></span></p>
<p><span data-ttu-id="85b40-270">Lien suivant : <strong>ID de lien 11036</strong></span><span class="sxs-lookup"><span data-stu-id="85b40-270">Forward link: <strong>Link ID 11036</strong></span></span></p>
<p><span data-ttu-id="85b40-271">Le lien inverse correspondant est <strong>msRTCSIP-ServerReferenceBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-271">The corresponding backward link is <strong>msRTCSIP-ServerReferenceBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-272">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-272">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-273">msRTCSIP-DefaultPolicy (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-273">msRTCSIP-DefaultPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-274">Cet attribut booléen spécifie si la stratégie est une stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="85b40-274">This Boolean attribute specifies whether the policy is a default policy.</span></span> <span data-ttu-id="85b40-275">La stratégie est une stratégie par défaut définie sur <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-275">The policy is a default policy when set to <strong>TRUE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-276">Nouveautés d’Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="85b40-276">New in Office Communications Server 2007</span></span></p>
<p><span data-ttu-id="85b40-277">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-277">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-278">msRTCSIP-DefaultRouteToEdgeProxy (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-278">msRTCSIP-DefaultRouteToEdgeProxy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-279">Cet attribut spécifie le nom de domaine complet (FQDN) du serveur de périphérie exécutant le service Edge d’accès, s’il est accessible directement ou à partir de l’équilibrage de charge matérielle d’un pool de serveurs exécutant le service Edge d’accès.</span><span class="sxs-lookup"><span data-stu-id="85b40-279">This attribute specifies the FQDN of either the Edge Server running the Access Edge service, if it can be accessed directly, or of the hardware load balancer for a pool of servers running Access Edge service.</span></span> <span data-ttu-id="85b40-280">Si les serveurs exécutant le service Edge d’accès ne peuvent être utilisés que par le biais d’un ou de plusieurs directeurs, cet attribut spécifie le nom de domaine complet et, éventuellement, le numéro de port du réalisateur ou du système d’équilibrage de la charge matérielle servant un pool de directeurs.</span><span class="sxs-lookup"><span data-stu-id="85b40-280">If the servers running Access Edge service can be accessed only through one or more Directors, this attribute specifies the FQDN and, optionally, the port number of the Director or of the hardware load balancer serving a Director pool.</span></span></p>
<p><span data-ttu-id="85b40-281">La valeur valide de chaque segment est de 63 caractères. la valeur valide pour le nom de domaine complet est de 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="85b40-281">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="85b40-282">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-282">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="85b40-283">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-283">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-284">msRTCSIP-DefaultRouteToEdgeProxyPort (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-284">msRTCSIP-DefaultRouteToEdgeProxyPort (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-285">Cet attribut représente le numéro de port qui doit être utilisé pour la connexion au serveur exécutant le service Edge d’accès.</span><span class="sxs-lookup"><span data-stu-id="85b40-285">This attribute represents the port number that should be used to connect to the server running Access Edge service.</span></span></p>
<p><span data-ttu-id="85b40-286">La valeur valide est une valeur entière spécifiant le port à utiliser.</span><span class="sxs-lookup"><span data-stu-id="85b40-286">The valid value is an integer value specifying the port to be used.</span></span> <span data-ttu-id="85b40-287">La valeur par défaut est 5061.</span><span class="sxs-lookup"><span data-stu-id="85b40-287">The default value is 5061.</span></span></p></td>
<td><p><span data-ttu-id="85b40-288">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-288">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="85b40-289">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-289">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-290">msRTCSIP-DefPresenceSubscriptionTimeout (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-290">msRTCSIP-DefPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-291">Cet attribut représente le délai d’expiration de l’abonnement de présence par défaut.</span><span class="sxs-lookup"><span data-stu-id="85b40-291">This attribute represents the default presence subscription time-out period.</span></span></p></td>
<td><p><span data-ttu-id="85b40-292">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-292">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-293">msRTCSIP-DefRegistrationTimeout (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-293">msRTCSIP-DefRegistrationTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-294">Cet attribut représente la fenêtre délai d’inscription par défaut.</span><span class="sxs-lookup"><span data-stu-id="85b40-294">This attribute represents the default registration time-out window.</span></span></p></td>
<td><p><span data-ttu-id="85b40-295">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-295">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-296">msRTCSIP-DefRoamingDataSubscriptionTimeout (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-296">msRTCSIP-DefRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-297">Cet attribut représente la fenêtre délai d’abonnement aux données itinérantes par défaut.</span><span class="sxs-lookup"><span data-stu-id="85b40-297">This attribute represents the default roaming data subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="85b40-298">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-298">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-299">msRTCSIP-DeploymentLocator</span><span class="sxs-lookup"><span data-stu-id="85b40-299">msRTCSIP-DeploymentLocator</span></span></p></td>
<td><p><span data-ttu-id="85b40-300">Cet attribut est utilisé dans une topologie de domaine fractionné et contient un nom de domaine complet (FQDN).</span><span class="sxs-lookup"><span data-stu-id="85b40-300">This attribute is used in a split domain topology and contains a fully qualified domain name (FQDN).</span></span></p></td>
<td><p><span data-ttu-id="85b40-301">Nouveautés de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-301">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-302">msRTCSIP-Description (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-302">msRTCSIP-Description (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-303">Cet attribut de chaîne UNICODE à valeur unique contient une description conviviale de ce type de route ou de la règle de normalisation.</span><span class="sxs-lookup"><span data-stu-id="85b40-303">This single-valued UNICODE string attribute contains a friendly description of this phone route or normalization rule.</span></span></p></td>
<td><p><span data-ttu-id="85b40-304">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-304">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-305">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-305">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-306">msRTCSIP-DomainData</span><span class="sxs-lookup"><span data-stu-id="85b40-306">msRTCSIP-DomainData</span></span></p></td>
<td><p><span data-ttu-id="85b40-307">Cet attribut est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85b40-307">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-308">msRTCSIP-nom_domaine</span><span class="sxs-lookup"><span data-stu-id="85b40-308">msRTCSIP-DomainName</span></span></p></td>
<td><p><span data-ttu-id="85b40-309">Cet attribut représente un domaine configuré pour le Bureau d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="85b40-309">This attribute represents a domain configured for the Registrar.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-310">msRTCSIP-EdgeProxyData</span><span class="sxs-lookup"><span data-stu-id="85b40-310">msRTCSIP-EdgeProxyData</span></span></p></td>
<td><p><span data-ttu-id="85b40-311">Cet attribut est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85b40-311">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="85b40-312">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-312">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-313">msRTCSIP-EdgeProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="85b40-313">msRTCSIP-EdgeProxyFQDN</span></span></p></td>
<td><p><span data-ttu-id="85b40-314">Cet attribut spécifie le nom de domaine complet du serveur exécutant le service Edge d’accès.</span><span class="sxs-lookup"><span data-stu-id="85b40-314">This attribute specifies the FQDN of the server running Access Edge service.</span></span></p>
<p><span data-ttu-id="85b40-315">La valeur valide de chaque segment est de 63 caractères. la valeur valide pour le nom de domaine complet est de 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="85b40-315">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="85b40-316">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-316">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-317">msRTCSIP-EnableBestEffortNotify (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-317">msRTCSIP-EnableBestEffortNotify (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-318">Cet attribut détermine si un serveur génère une demande de notification d’utilisation optimale, au lieu d’une demande de notification, en réponse à une demande s’ABONNer à partir d’un client.</span><span class="sxs-lookup"><span data-stu-id="85b40-318">This attribute controls whether a server generates a Best Effort NOTIFY (BENOTIFY) request, instead of a NOTIFY request, in response to a SUBSCRIBE request from a client.</span></span> <span data-ttu-id="85b40-319">BENOTIFY est une extension d’amélioration des performances du protocole de notification d’abonnement où le serveur génère des demandes BENOTIFY au lieu de demandes de notification normales.</span><span class="sxs-lookup"><span data-stu-id="85b40-319">BENOTIFY is a performance-enhancing extension to the subscribe notification handshake where the server generates BENOTIFY requests, instead of regular NOTIFY requests.</span></span> <span data-ttu-id="85b40-320">Le gain de performance réside dans le fait qu’une demande BENOTIFY ne nécessite pas de réponse de 200 OK du client en fonction de la demande de notification.</span><span class="sxs-lookup"><span data-stu-id="85b40-320">The performance benefit is that a BENOTIFY request does not require a 200 OK response from the client as the NOTIFY request does.</span></span></p>
<p><span data-ttu-id="85b40-321">Les valeurs valides sont <strong>true</strong> ou <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-321">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="85b40-322">Live Communications Server 2003 ne prend pas en charge les demandes BENOTIFY.</span><span class="sxs-lookup"><span data-stu-id="85b40-322">Live Communications Server 2003 does not support BENOTIFY requests.</span></span> <span data-ttu-id="85b40-323">Pour interagir avec des applications serveur écrites à l’aide de l’API serveur Live Communications Server 2003 exécutée sur Live Communications Server 2005 et des serveurs tiers, les demandes BENOTIFY peuvent être désactivées en définissant la valeur sur <STRONG>false</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="85b40-323">To interoperate with server applications written with the Live Communications Server 2003 server API running on Live Communications Server 2005 and third-party servers, BENOTIFY requests can be disabled by setting its value to <STRONG>FALSE</STRONG>.</span></span> <span data-ttu-id="85b40-324">BENOTIFY ne fait actuellement pas partie du processus de normalisation SIP de l’IETF (Internet Engineering Task Force).</span><span class="sxs-lookup"><span data-stu-id="85b40-324">BENOTIFY is not currently part of the IETF (Internet Engineering Task Force) SIP standardization process.</span></span>


</div></td>
<td><p><span data-ttu-id="85b40-325">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-325">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="85b40-326">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-326">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-327">msRTCSIP-EnableFederation (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-327">msRTCSIP-EnableFederation (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-328">Cet attribut est un commutateur global utilisé par les administrateurs informatiques pour déterminer si les utilisateurs sont autorisés à communiquer avec des utilisateurs d’autres organisations.</span><span class="sxs-lookup"><span data-stu-id="85b40-328">This attribute is a global switch that IT administrators use to configure whether users are allowed to communicate with users from other organizations.</span></span> <span data-ttu-id="85b40-329">Il permet à un administrateur de remplacer l’attribut <strong>FederationEnabled</strong> d’un utilisateur individuel.</span><span class="sxs-lookup"><span data-stu-id="85b40-329">It enables an administrator to overwrite an individual user’s <strong>FederationEnabled</strong> attribute.</span></span> <span data-ttu-id="85b40-330">Cet attribut peut vous aider à protéger le réseau interne contre les attaques via Internet qui peuvent être causées par des vers, des virus ou des attaques ciblées au niveau de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="85b40-330">This attribute can be useful to help protect the internal network from Internet attacks that may be caused by worms, viruses, or targeted attacks on the company.</span></span></p>
<p><span data-ttu-id="85b40-331">Les valeurs valides (et positions de bits associées) sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="85b40-331">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-332">1 : activé pour la connectivité PIC (Public IM Connectivity)</span><span class="sxs-lookup"><span data-stu-id="85b40-332">1: Enabled for public IM connectivity (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="85b40-333">2 : réservé (position binaire 1)</span><span class="sxs-lookup"><span data-stu-id="85b40-333">2: Reserved (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="85b40-334">4 : réservé (position binaire 2)</span><span class="sxs-lookup"><span data-stu-id="85b40-334">4: Reserved (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="85b40-335">8 : réservé (position binaire 3)</span><span class="sxs-lookup"><span data-stu-id="85b40-335">8: Reserved (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="85b40-336">16 : le contrôle d’appel distant a été activé [téléphonie] (position bit 4)</span><span class="sxs-lookup"><span data-stu-id="85b40-336">16: Remote call control Enabled [Telephony] (bit position 4)</span></span></p></li>
<li><p><span data-ttu-id="85b40-337">64 : AllowOrganizeMeetingWithAnonymousParticipants (permettre aux utilisateurs d’inviter des utilisateurs anonymes à des réunions (position de bit 6)</span><span class="sxs-lookup"><span data-stu-id="85b40-337">64: AllowOrganizeMeetingWithAnonymousParticipants (allow users to invite anonymous users to meetings (bit position 6)</span></span></p></li>
<li><p><span data-ttu-id="85b40-338">128 : UCEnabled (permettre aux utilisateurs pour les communications unifiées) (position binaire 7)</span><span class="sxs-lookup"><span data-stu-id="85b40-338">128: UCEnabled (enable users for unified communications) (bit position 7)</span></span></p></li>
<li><p><span data-ttu-id="85b40-339">256 : EnabledForEnhancedPresence (activer l’utilisateur pour la connectivité de messagerie instantanée publique) (position de bit 8)</span><span class="sxs-lookup"><span data-stu-id="85b40-339">256: EnabledForEnhancedPresence (enable user for public IM connectivity) (bit position 8)</span></span></p></li>
<li><p><span data-ttu-id="85b40-340">512 : RemoteCallControlDualMode (position binaire 9)</span><span class="sxs-lookup"><span data-stu-id="85b40-340">512: RemoteCallControlDualMode (bit position 9)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="85b40-341">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-341">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="85b40-342">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-342">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-343">msRTCSIP-EnterpriseServices</span><span class="sxs-lookup"><span data-stu-id="85b40-343">msRTCSIP-EnterpriseServices</span></span></p></td>
<td><p><span data-ttu-id="85b40-344">Cet attribut indique si les services d’entreprise sont chargés sur le serveur donné.</span><span class="sxs-lookup"><span data-stu-id="85b40-344">This attribute indicates whether the Enterprise Services are loaded on the given server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-345">msRTCSIP-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="85b40-345">msRTCSIP-ExtensionData</span></span></p></td>
<td><p><span data-ttu-id="85b40-346">Cet attribut est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85b40-346">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-347">msRTCSIP-ExternalAccessCode</span><span class="sxs-lookup"><span data-stu-id="85b40-347">msRTCSIP-ExternalAccessCode</span></span></p></td>
<td><p><span data-ttu-id="85b40-348">Cet attribut contient le code de numérotation pour l’accès externe.</span><span class="sxs-lookup"><span data-stu-id="85b40-348">This attribute contains the dial code for external access.</span></span></p></td>
<td><p><span data-ttu-id="85b40-349">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-349">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-350">msRTCSIP-FederationEnabled</span><span class="sxs-lookup"><span data-stu-id="85b40-350">msRTCSIP-FederationEnabled</span></span></p></td>
<td><p><span data-ttu-id="85b40-351">Cet attribut détermine si un utilisateur unique est activé pour la Fédération.</span><span class="sxs-lookup"><span data-stu-id="85b40-351">This attribute controls whether a single user is enabled for federation.</span></span> <span data-ttu-id="85b40-352">Elle est appliquée par la couche services d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="85b40-352">It is enforced by the Enterprise Services layer.</span></span> <span data-ttu-id="85b40-353">Il est marqué pour la réplication de catalogue global.</span><span class="sxs-lookup"><span data-stu-id="85b40-353">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="85b40-354">Les valeurs valides sont <strong>true</strong> ou <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-354">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-355">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-355">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-356">msRTCSIP-FrontEndServers</span><span class="sxs-lookup"><span data-stu-id="85b40-356">msRTCSIP-FrontEndServers</span></span></p></td>
<td><p><span data-ttu-id="85b40-357">Cet attribut est une liste à plusieurs valeurs des noms de domaine de tous les serveurs Enterprise Edition associés à un pool.</span><span class="sxs-lookup"><span data-stu-id="85b40-357">This attribute is a multi-valued list of the domain names of all Enterprise Edition servers associated with a pool.</span></span></p>
<p><span data-ttu-id="85b40-358">Lien précédent : <strong>ID de lien 11023</strong></span><span class="sxs-lookup"><span data-stu-id="85b40-358">Back link: <strong>Link ID 11023</strong></span></span></p>
<p><span data-ttu-id="85b40-359">Le lien transférer correspondant à ce lien précédent est <strong>msRTCSIP-PoolAddress</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-359">The corresponding forward link to this back link is <strong>msRTCSIP-PoolAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-360">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-360">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-361">msRTCSIP-passerelles (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-361">msRTCSIP-Gateways (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-362">Cet attribut de chaîne à valeurs multiples contient une liste des passerelles et des ports (par passerelle).</span><span class="sxs-lookup"><span data-stu-id="85b40-362">This multi-valued string attribute contains a list of gateways and ports (per gateway).</span></span></p></td>
<td><p><span data-ttu-id="85b40-363">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-363">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-364">msRTCSIP-GlobalSettingsData (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-364">msRTCSIP-GlobalSettingsData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-365">Cet attribut stocke les paires nom : valeur.</span><span class="sxs-lookup"><span data-stu-id="85b40-365">This attribute stores name:value pairs.</span></span> <span data-ttu-id="85b40-366">Le nom déjà défini : paire de valeurs correspond au paramètre <strong>autoriser l’interrogation pour la présence</strong> .</span><span class="sxs-lookup"><span data-stu-id="85b40-366">The already-defined name:value pair is for the <strong>allow polling for presence</strong> setting.</span></span></p></td>
<td><p><span data-ttu-id="85b40-367">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-367">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-368">msRTCSIP-GroupingID</span><span class="sxs-lookup"><span data-stu-id="85b40-368">msRTCSIP-GroupingID</span></span></p></td>
<td><p><span data-ttu-id="85b40-369">Cet attribut est un identificateur unique d’un groupe qui est utilisé pour regrouper les entrées du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="85b40-369">This attribute is a unique identifier of a group that is used to group address book entries.</span></span></p></td>
<td><p><span data-ttu-id="85b40-370">Nouveautés de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-370">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-371">msRTCSIP-HomeServer (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-371">msRTCSIP-HomeServer (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="85b40-372">Nouveautés de Live Communications Server 2003 (non utilisés).</span><span class="sxs-lookup"><span data-stu-id="85b40-372">New in Live Communications Server 2003 (not used).</span></span></p>
<p><span data-ttu-id="85b40-373">Obsolète dans Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-373">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-374">msRTCSIP-HomeServerString (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-374">msRTCSIP-HomeServerString (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="85b40-375">Nouveautés de Live Communications Server 2003.</span><span class="sxs-lookup"><span data-stu-id="85b40-375">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="85b40-376">Obsolète dans Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-376">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-377">msRTCSIP-HomeUsers (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-377">msRTCSIP-HomeUsers (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="85b40-378">Nouveautés de Live Communications Server 2003 (non utilisés).</span><span class="sxs-lookup"><span data-stu-id="85b40-378">New in Live Communications Server 2003 (not used).</span></span></p>
<p><span data-ttu-id="85b40-379">Obsolète dans Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-379">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-380">msRTCSIP-InternetAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="85b40-380">msRTCSIP-InternetAccessEnabled</span></span></p></td>
<td><p><span data-ttu-id="85b40-381">Cet attribut détermine si un utilisateur unique est activé pour l’accès extérieur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-381">This attribute controls whether a single user is enabled for outside user access.</span></span> <span data-ttu-id="85b40-382">Elle est appliquée par la couche services d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="85b40-382">It is enforced by the Enterprise Services layer.</span></span> <span data-ttu-id="85b40-383">Il est marqué pour la réplication de catalogue global.</span><span class="sxs-lookup"><span data-stu-id="85b40-383">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="85b40-384">Les valeurs valides sont <strong>true</strong> ou <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-384">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-385">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-385">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-386">msRTCSIP-IsMaster (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-386">msRTCSIP-IsMaster (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="85b40-387">Nouveautés de Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="85b40-387">New in Live Communications Server 2003</span></span></p>
<p><span data-ttu-id="85b40-388">Obsolète dans Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-388">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-389">msRTCSIP-ligne</span><span class="sxs-lookup"><span data-stu-id="85b40-389">msRTCSIP-Line</span></span></p></td>
<td><p><span data-ttu-id="85b40-390">Cet attribut à valeur unique contient l’ID de l’appareil (URI SIP ou URI TEL du téléphone contrôles) utilisé par Lync pour la téléphonie.</span><span class="sxs-lookup"><span data-stu-id="85b40-390">This single-valued attribute contains the device ID (either the SIP URI or the TEL URI of the phone the user controls) used by Lync for telephony.</span></span> <span data-ttu-id="85b40-391">Cet attribut est marqué pour la réplication de catalogue global et est indexé.</span><span class="sxs-lookup"><span data-stu-id="85b40-391">This attribute is marked for Global Catalog replication and is indexed.</span></span> <span data-ttu-id="85b40-392">Si un utilisateur est activé pour voix entreprise, cet attribut stocke la version normalisée E. 164 du numéro de téléphone de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-392">If a user is enabled for Enterprise Voice, this attribute stores the E.164 normalized version of the user’s phone number.</span></span></p></td>
<td><p><span data-ttu-id="85b40-393">Nouveautés de Microsoft Office Live Communications Server 2005 avec SP1</span><span class="sxs-lookup"><span data-stu-id="85b40-393">New in Microsoft Office Live Communications Server 2005 with SP1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-394">msRTCSIP-LineServer</span><span class="sxs-lookup"><span data-stu-id="85b40-394">msRTCSIP-LineServer</span></span></p></td>
<td><p><span data-ttu-id="85b40-395">Cet attribut à valeur unique contient l’URI SIP du serveur de passerelle CSTA-SIP.</span><span class="sxs-lookup"><span data-stu-id="85b40-395">This single-valued attribute contains the SIP URI of the CSTA-SIP gateway server.</span></span> <span data-ttu-id="85b40-396">Cet attribut est marqué pour la réplication de catalogue global, mais n’est pas indexé.</span><span class="sxs-lookup"><span data-stu-id="85b40-396">This attribute is marked for Global Catalog replication but is not indexed.</span></span></p></td>
<td><p><span data-ttu-id="85b40-397">Nouveautés de Microsoft Office Live Communications Server 2005 avec SP1</span><span class="sxs-lookup"><span data-stu-id="85b40-397">New in Microsoft Office Live Communications Server 2005 with SP1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-398">msRTCSIP-LocalNormalizationData (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-398">msRTCSIP-LocalNormalizationData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-399">Cet attribut est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85b40-399">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="85b40-400">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-400">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-401">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-401">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-402">msRTCSIP-LocalNormalizationLinks (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-402">msRTCSIP-LocalNormalizationLinks (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-403">Cet attribut à valeurs multiples contient une liste de noms uniques (ND) de normalisation locale associés à ce profil d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="85b40-403">This multi-valued attribute contains a list of local normalization distinguished names (DN) associated with this location profile.</span></span> <span data-ttu-id="85b40-404">Le type de cet attribut est un fichier binaire DN.</span><span class="sxs-lookup"><span data-stu-id="85b40-404">The type of this attribute is a DN binary.</span></span> <span data-ttu-id="85b40-405">Il existe une relation un-à-plusieurs entre le profil d’emplacement et les règles de normalisation locales.</span><span class="sxs-lookup"><span data-stu-id="85b40-405">There is a one-to-many relationship between location profile and local normalization rules.</span></span> <span data-ttu-id="85b40-406">Le classement de la liste du DNs de normalisation local doit être maintenu dans l’ordre indiqué par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-406">The ordering of the list of local normalization DNs must be maintained in the order specified by the administrator.</span></span> <span data-ttu-id="85b40-407">La conservation de l’ordre est gérée par la partie binaire du fichier binaire du DN, qui spécifie l’index de l’ordre.</span><span class="sxs-lookup"><span data-stu-id="85b40-407">The preservation of order is maintained by the binary portion of the DN binary, which specifies the order index.</span></span></p>
<p><span data-ttu-id="85b40-408">Lien suivant : <strong>ID de lien 11034</strong></span><span class="sxs-lookup"><span data-stu-id="85b40-408">Forward link: <strong>Link ID 11034</strong></span></span></p>
<p><span data-ttu-id="85b40-409">Le lien précédent correspondant à cet attribut de lien suivant est <strong>msRTCSIP-LocationProfileBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-409">The corresponding back link to this forward link attribute is <strong>msRTCSIP-LocationProfileBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-410">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-410">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-411">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-411">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-412">msRTCSIP-LocalNormalizationOptions</span><span class="sxs-lookup"><span data-stu-id="85b40-412">msRTCSIP-LocalNormalizationOptions</span></span></p></td>
<td><p><span data-ttu-id="85b40-413">Cet attribut contient une liste des options de la règle de normalisation.</span><span class="sxs-lookup"><span data-stu-id="85b40-413">This attribute contains a list of options for the normalization rule.</span></span></p></td>
<td><p><span data-ttu-id="85b40-414">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-414">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-415">msRTCSIP-LocationName (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-415">msRTCSIP-LocationName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-416">Cet attribut à valeur unique contient un nom convivial pour le profil d’emplacement indiquant l’emplacement que ce profil représente.</span><span class="sxs-lookup"><span data-stu-id="85b40-416">This single-valued attribute contains a friendly name for the location profile that indicates which location this profile represents.</span></span> <span data-ttu-id="85b40-417">Dans la mesure où il existe plusieurs profils d’emplacement, l’administrateur a besoin d’une méthode pour distinguer les différents profils.</span><span class="sxs-lookup"><span data-stu-id="85b40-417">Because there can be multiple location profiles, the administrator needs a way to distinguish between different profiles.</span></span></p></td>
<td><p><span data-ttu-id="85b40-418">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-418">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-419">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-419">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-420">msRTCSIP-locationProfileBL (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-420">msRTCSIP-locationProfileBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-421">Cet attribut à valeurs multiples contient une liste de noms uniques de profils d’emplacements.</span><span class="sxs-lookup"><span data-stu-id="85b40-421">This multi-valued attribute contains a list of location profile distinguished names.</span></span> <span data-ttu-id="85b40-422">Cet attribut spécifie le lien précédent vers un ou plusieurs profils d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="85b40-422">This attribute specifies the back link to one or more location profiles.</span></span></p>
<p><span data-ttu-id="85b40-423">Lien précédent : <strong>ID de lien 11035</strong></span><span class="sxs-lookup"><span data-stu-id="85b40-423">Back link: <strong>Link ID 11035</strong></span></span></p>
<p><span data-ttu-id="85b40-424">Cet attribut correspond à la liaison suivante <strong>msRTCSIP-LocalNormalizationLinks</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-424">This attribute corresponds to the forward link <strong>msRTCSIP-LocalNormalizationLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-425">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-425">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-426">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-426">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-427">msRTCSIP-LocationProfileData (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-427">msRTCSIP-LocationProfileData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-428">Cet attribut est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85b40-428">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="85b40-429">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-429">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-430">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-430">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-431">msRTCSIP-LocationProfileOptions</span><span class="sxs-lookup"><span data-stu-id="85b40-431">msRTCSIP-LocationProfileOptions</span></span></p></td>
<td><p><span data-ttu-id="85b40-432">Cet attribut contient les options du profil d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="85b40-432">This attribute contains the options for the location profile.</span></span></p></td>
<td><p><span data-ttu-id="85b40-433">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-433">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-434">msRTCSIP-MappingContact</span><span class="sxs-lookup"><span data-stu-id="85b40-434">msRTCSIP-MappingContact</span></span></p></td>
<td><p><span data-ttu-id="85b40-435">Cet attribut à plusieurs valeurs contient une liste des contacts de l’application.</span><span class="sxs-lookup"><span data-stu-id="85b40-435">This multiple-value attribute holds a list of application contacts.</span></span></p></td>
<td><p><span data-ttu-id="85b40-436">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-436">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-437">msRTCSIP-MappingLocation</span><span class="sxs-lookup"><span data-stu-id="85b40-437">msRTCSIP-MappingLocation</span></span></p></td>
<td><p><span data-ttu-id="85b40-438">Cet attribut à valeurs multiples comporte une liste de profils d’emplacements.</span><span class="sxs-lookup"><span data-stu-id="85b40-438">This multiple-value attribute holds a list of location profiles.</span></span></p></td>
<td><p><span data-ttu-id="85b40-439">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-439">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-440">msRTCSIP-MaxNumOutstandingSearchPerServer (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-440">msRTCSIP-MaxNumOutstandingSearchPerServer (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-441">Cet attribut représente le nombre maximal de demandes de recherche en suspens par serveur.</span><span class="sxs-lookup"><span data-stu-id="85b40-441">This attribute represents the maximum number of outstanding search requests per server.</span></span></p></td>
<td><p><span data-ttu-id="85b40-442">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-442">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-443">msRTCSIP-MaxNumSubscriptionsPerUser (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-443">msRTCSIP-MaxNumSubscriptionsPerUser (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-444">L’attribut représente le nombre maximal d’abonnements par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-444">The attribute represents the maximum number of subscriptions per user.</span></span></p></td>
<td><p><span data-ttu-id="85b40-445">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-445">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-446">msRTCSIP-MaxPresenceSubscriptionTimeout (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-446">msRTCSIP-MaxPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-447">Cet attribut représente la fenêtre délai d’abonnement maximal.</span><span class="sxs-lookup"><span data-stu-id="85b40-447">This attribute represents the maximum subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="85b40-448">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-448">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-449">msRTCSIP-MaxRegistrationsTimeout (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-449">msRTCSIP-MaxRegistrationsTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-450">Cet attribut représente la fenêtre délai maximal d’inscriptions.</span><span class="sxs-lookup"><span data-stu-id="85b40-450">This attribute represents the maximum registrations time-out window.</span></span></p></td>
<td><p><span data-ttu-id="85b40-451">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-451">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-452">msRTCSIP-MaxRoamingDataSubscriptionTimeout (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-452">msRTCSIP-MaxRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-453">Cet attribut représente la fenêtre délai maximal d’abonnements aux données itinérantes.</span><span class="sxs-lookup"><span data-stu-id="85b40-453">This attribute represents the maximum roaming data subscriptions time-out window.</span></span></p></td>
<td><p><span data-ttu-id="85b40-454">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-454">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-455">msRTCSIP-MCUData</span><span class="sxs-lookup"><span data-stu-id="85b40-455">msRTCSIP-MCUData</span></span></p></td>
<td><p><span data-ttu-id="85b40-456">Cet attribut est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85b40-456">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="85b40-457">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-457">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-458">msRTCSIP-MCUFactoryAddress</span><span class="sxs-lookup"><span data-stu-id="85b40-458">msRTCSIP-MCUFactoryAddress</span></span></p></td>
<td><p><span data-ttu-id="85b40-459">Cet attribut est un attribut de point de contrôle de service sous la classe ordinateur qui spécifie un lien vers une fabrique de contrôle multipoint (MCU) auquel il appartient.</span><span class="sxs-lookup"><span data-stu-id="85b40-459">This attribute is a service control point attribute under the computer class that specifies a link back to the multipoint control unit (MCU) Factory to which it belongs.</span></span> <span data-ttu-id="85b40-460">Ce point et cet attribut de contrôle de service est créé pour chaque MCU Microsoft.</span><span class="sxs-lookup"><span data-stu-id="85b40-460">This service control point and attribute is created for every Microsoft MCU.</span></span> <span data-ttu-id="85b40-461">Chaque MCU Microsoft doit trouver le serveur principal du pool auquel il appartient, afin de récupérer les paramètres au niveau du pool.</span><span class="sxs-lookup"><span data-stu-id="85b40-461">Each Microsoft MCU must find the Back End Server of the pool to which it belongs, in order to retrieve pool-level settings from it.</span></span></p>
<p><span data-ttu-id="85b40-462">La valeur de cet attribut est le nom unique (DN) de la fabrique MCU.</span><span class="sxs-lookup"><span data-stu-id="85b40-462">The value of this attribute is the distinguished name (DN) of the MCU Factory.</span></span> <span data-ttu-id="85b40-463">Il s’agit d’un attribut à valeur unique qui est marqué pour la réplication de catalogue global.</span><span class="sxs-lookup"><span data-stu-id="85b40-463">This is a single-valued attribute and marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="85b40-464">Lien suivant : <strong>ID de lien 11026</strong></span><span class="sxs-lookup"><span data-stu-id="85b40-464">Forward link: <strong>Link ID 11026</strong></span></span></p>
<p><span data-ttu-id="85b40-465">Le lien précédent correspondant à cet attribut de lien suivant est <strong>msRTCSIP-MCUServers</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-465">The corresponding back link to this forward link attribute is <strong>msRTCSIP-MCUServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-466">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-466">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-467">msRTCSIP-MCUFactoryData</span><span class="sxs-lookup"><span data-stu-id="85b40-467">msRTCSIP-MCUFactoryData</span></span></p></td>
<td><p><span data-ttu-id="85b40-468">Il s’agit d’un attribut réservé multichaîne.</span><span class="sxs-lookup"><span data-stu-id="85b40-468">This is a multi-string reserved attribute.</span></span> <span data-ttu-id="85b40-469">Les paramètres stockés dans cet attribut sont représentés par des paires name = value.</span><span class="sxs-lookup"><span data-stu-id="85b40-469">Settings stored in this attribute are represented as name=value pairs.</span></span> <span data-ttu-id="85b40-470">Nom actuellement défini = paires de valeurs :</span><span class="sxs-lookup"><span data-stu-id="85b40-470">Currently defined name=value pairs are:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-471">FactoryURL = &lt; URL&gt;</span><span class="sxs-lookup"><span data-stu-id="85b40-471">FactoryURL = &lt;URL&gt;</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="85b40-472">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-472">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-473">msRTCSIP-MCUFactoryPath</span><span class="sxs-lookup"><span data-stu-id="85b40-473">msRTCSIP-MCUFactoryPath</span></span></p></td>
<td><p><span data-ttu-id="85b40-474">Il s’agit d’un attribut à valeur unique qui contient le nom unique (DN) d’une fabrique MCU unique associée à un pool.</span><span class="sxs-lookup"><span data-stu-id="85b40-474">This is a single-valued attribute that contains the distinguished name (DN) of a single MCU factory associated with a pool.</span></span></p>
<p><span data-ttu-id="85b40-475">Lien suivant : <strong>ID de lien 11024</strong></span><span class="sxs-lookup"><span data-stu-id="85b40-475">Forward link: <strong>Link ID 11024</strong></span></span></p>
<p><span data-ttu-id="85b40-476">Le lien précédent correspondant à cet attribut de lien suivant est <strong>msRTCSIP-PoolAddresses</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-476">The corresponding back link to this forward link attribute is <strong>msRTCSIP-PoolAddresses</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-477">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-477">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-478">msRTCSIP-MCUFactoryProviderID</span><span class="sxs-lookup"><span data-stu-id="85b40-478">msRTCSIP-MCUFactoryProviderID</span></span></p></td>
<td><p><span data-ttu-id="85b40-479">Cet attribut est une chaîne à valeur unique qui spécifie le GUID du fournisseur de fabrique MCU.</span><span class="sxs-lookup"><span data-stu-id="85b40-479">This attribute is a single-valued string that specifies the GUID of the MCU factory provider.</span></span> <span data-ttu-id="85b40-480">En fonction de la valeur GUID, le processus de fabrique MCU détermine si ce type MCU doit être desservi.</span><span class="sxs-lookup"><span data-stu-id="85b40-480">Based on the GUID value, the MCU factory process determines whether to service this MCU type.</span></span> <span data-ttu-id="85b40-481">Si la valeur GUID est <strong>{F0810510-424F-46ef-84fe-6CC720DF1791}</strong>, le processus de fabrique MCU (disponible par défaut dans Lync Server) la traitera.</span><span class="sxs-lookup"><span data-stu-id="85b40-481">If the GUID value is <strong>{F0810510-424F-46ef-84FE-6CC720DF1791}</strong>, then the MCU factory process (available by default in Lync Server) will process it.</span></span> <span data-ttu-id="85b40-482">Pour toute autre valeur GUID, le processus de fabrique MCU ne traitera pas le type MCU.</span><span class="sxs-lookup"><span data-stu-id="85b40-482">For any other GUID value, the MCU factory process will not service the MCU type.</span></span></p></td>
<td><p><span data-ttu-id="85b40-483">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-483">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-484">msRTCSIP-MCUServers</span><span class="sxs-lookup"><span data-stu-id="85b40-484">msRTCSIP-MCUServers</span></span></p></td>
<td><p><span data-ttu-id="85b40-485">Cet attribut est une liste à plusieurs valeurs de noms uniques (DN).</span><span class="sxs-lookup"><span data-stu-id="85b40-485">This attribute is a multi-valued list of distinguished names (DN).</span></span> <span data-ttu-id="85b40-486">Cet attribut contient la liste de tous les serveurs MCU du même type et fournisseur associé à cette fabrique MCU.</span><span class="sxs-lookup"><span data-stu-id="85b40-486">This attribute contains a list of all MCU servers of the same type and vendor associated with this MCU factory.</span></span> <span data-ttu-id="85b40-487">La valeur valide de chaque segment est de 63 caractères. la valeur valide pour le nom de domaine complet est de 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="85b40-487">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p>
<p><span data-ttu-id="85b40-488">Lien précédent : ID de lien 11027</span><span class="sxs-lookup"><span data-stu-id="85b40-488">Back link: Link ID 11027</span></span></p>
<p><span data-ttu-id="85b40-489">Le lien transférer correspondant à ce lien précédent est <strong>msRTCSIP-MCUFactoryAddress</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-489">The corresponding forward link to this back link is <strong>msRTCSIP-MCUFactoryAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-490">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-490">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-491">msRTCSIP-MCUType</span><span class="sxs-lookup"><span data-stu-id="85b40-491">msRTCSIP-MCUType</span></span></p></td>
<td><p><span data-ttu-id="85b40-492">Cet attribut est une chaîne à valeur unique qui spécifie le média que la MCU peut gérer.</span><span class="sxs-lookup"><span data-stu-id="85b40-492">This attribute is a single-valued string that specifies the medium the MCU can handle.</span></span></p>
<p><span data-ttu-id="85b40-493">Les types valides pris en charge sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="85b40-493">Supported valid types are:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-494">répond</span><span class="sxs-lookup"><span data-stu-id="85b40-494">meeting</span></span></p></li>
<li><p><span data-ttu-id="85b40-495">audio-vidéo</span><span class="sxs-lookup"><span data-stu-id="85b40-495">audio-video</span></span></p></li>
<li><p><span data-ttu-id="85b40-496">salons</span><span class="sxs-lookup"><span data-stu-id="85b40-496">chat</span></span></p></li>
<li><p><span data-ttu-id="85b40-497">Téléphone-CONF</span><span class="sxs-lookup"><span data-stu-id="85b40-497">phone-conf</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="85b40-498">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-498">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-499">msRTCSIP-MCUVendor</span><span class="sxs-lookup"><span data-stu-id="85b40-499">msRTCSIP-MCUVendor</span></span></p></td>
<td><p><span data-ttu-id="85b40-500">Cet attribut est une chaîne à valeur unique qui spécifie le nom d’un fournisseur MCU.</span><span class="sxs-lookup"><span data-stu-id="85b40-500">This attribute is a single-valued string that specifies an MCU vendor’s name.</span></span> <span data-ttu-id="85b40-501">Tous les Microsoft MCU doivent spécifier cet attribut en tant que <strong>Microsoft Corporation</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-501">All Microsoft MCUs will specify this attribute to be <strong>Microsoft Corporation</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-502">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-502">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-503">msRTCSIP-MeetingFlags (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-503">msRTCSIP-MeetingFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-504">Cet attribut définit différentes options de réunion qui sont activées globalement pour tous les utilisateurs ou objets de contact.</span><span class="sxs-lookup"><span data-stu-id="85b40-504">This attribute defines different meeting options that are enabled globally for all users or contact objects.</span></span> <span data-ttu-id="85b40-505">Cet attribut est une valeur de masque de bits de type entier.</span><span class="sxs-lookup"><span data-stu-id="85b40-505">This attribute is a bit-mask value of integer type.</span></span></p>
<p><span data-ttu-id="85b40-506">Les valeurs valides (et positions de bits associées) sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="85b40-506">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-507">0 : AllowOrganizeMeetingWithAnonymousParticipants est défini sur aucun (ne pas autoriser les utilisateurs à inviter des utilisateurs anonymes à des réunions) (aucun bit)</span><span class="sxs-lookup"><span data-stu-id="85b40-507">0: AllowOrganizeMeetingWithAnonymousParticipants is None (do not allow users to invite anonymous users to meetings) (no bits set)</span></span></p></li>
<li><p><span data-ttu-id="85b40-508">4 : AllowOrganizeMeetingWithAnonymousParticipants est tout le monde (permettre à tous les utilisateurs d’inviter des utilisateurs anonymes à des réunions) (position de bit 2)</span><span class="sxs-lookup"><span data-stu-id="85b40-508">4: AllowOrganizeMeetingWithAnonymousParticipants is Everyone (allow all users to invite anonymous users to meetings) (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="85b40-509">8 : AllowOrganizeMeetingWithAnonymousParticipants est UsePerUserSetting (permet aux utilisateurs d’inviter des utilisateurs anonymes à des réunions en fonction de leur paramètre par utilisateur) (position de bit 3)</span><span class="sxs-lookup"><span data-stu-id="85b40-509">8: AllowOrganizeMeetingWithAnonymousParticipants is UsePerUserSetting (allow users to invite anonymous users to meetings based on per user setting) (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="85b40-510">16 : UserPerUserMeetingPolicy (la stratégie de réunion est définie par l’utilisateur) (position binaire 4)</span><span class="sxs-lookup"><span data-stu-id="85b40-510">16: UserPerUserMeetingPolicy (meeting policy is defined per user) (bit position 4)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="85b40-511">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-511">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-512">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-512">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-513">msRTCSIP-MeetingPolicy (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-513">msRTCSIP-MeetingPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-514">Cet attribut spécifie le nom unique (DN) de la stratégie affectée à l’administrateur pour cet utilisateur en tant qu’attribut à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="85b40-514">This attribute specifies the distinguished name (DN) of the policy the administrator has assigned for this user as a single-valued attribute.</span></span></p></td>
<td><p><span data-ttu-id="85b40-515">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-515">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-516">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-516">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-517">msRTCSIP-MinPresenceSubscriptionTimeout (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-517">msRTCSIP-MinPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-518">Cet attribut représente la fenêtre délai d’expiration de l’abonnement de présence minimum.</span><span class="sxs-lookup"><span data-stu-id="85b40-518">This attribute represents the minimum presence subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="85b40-519">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-519">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-520">msRTCSIP-MinRegistrationTimeout (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-520">msRTCSIP-MinRegistrationTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-521">Cet attribut représente la fenêtre délai d’inscription minimum.</span><span class="sxs-lookup"><span data-stu-id="85b40-521">This attribute represents the minimum registration time-out window.</span></span></p></td>
<td><p><span data-ttu-id="85b40-522">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-522">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-523">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-523">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-524">msRTCSIP-MinRoamingDataSubscriptionTimeout (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-524">msRTCSIP-MinRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-525">Cet attribut représente la fenêtre délai d’abonnement aux données itinérantes minimum.</span><span class="sxs-lookup"><span data-stu-id="85b40-525">This attribute represents the minimum roaming data subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="85b40-526">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-526">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-527">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-527">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-528">msRTCSIP-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="85b40-528">msRTCSIP-MirrorBackEndServer</span></span></p></td>
<td><p><span data-ttu-id="85b40-529">Cet attribut est utilisé pour stocker le serveur principal SQL Server utilisé par le pool frontal.</span><span class="sxs-lookup"><span data-stu-id="85b40-529">This attribute is used to store the mirrored SQL Server backend used by the Front End pool.</span></span></p></td>
<td><p><span data-ttu-id="85b40-530">Nouveautés de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="85b40-530">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-531">msRTCSIP-MobilityFlags</span><span class="sxs-lookup"><span data-stu-id="85b40-531">msRTCSIP-MobilityFlags</span></span></p></td>
<td><p><span data-ttu-id="85b40-532">Cet attribut contient des options et des indicateurs qui définissent les paramètres de mobilité.</span><span class="sxs-lookup"><span data-stu-id="85b40-532">This attribute contains options and flags that define mobility settings.</span></span></p></td>
<td><p><span data-ttu-id="85b40-533">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-533">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-534">msRTCSIP-MobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="85b40-534">msRTCSIP-MobilityPolicy</span></span></p></td>
<td><p><span data-ttu-id="85b40-535">Cet attribut contient le DN d’un objet de stratégie de mobilité.</span><span class="sxs-lookup"><span data-stu-id="85b40-535">This attribute contains the DN for a mobility policy object.</span></span></p></td>
<td><p><span data-ttu-id="85b40-536">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-536">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-537">msRTCSIP-NumDevicesPerUser (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-537">msRTCSIP-NumDevicesPerUser (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-538">Cet attribut représente le nombre autorisé d’appareils sur lesquels un utilisateur peut s’inscrire pour les communications SIP et s’abonner à la présence.</span><span class="sxs-lookup"><span data-stu-id="85b40-538">This attribute represents the allowed number of devices on which a user can register for SIP communications and subscribe to presence.</span></span></p></td>
<td><p><span data-ttu-id="85b40-539">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-539">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-540">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-540">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-541">msRTCSIP-OptionFlags</span><span class="sxs-lookup"><span data-stu-id="85b40-541">msRTCSIP-OptionFlags</span></span></p></td>
<td><p><span data-ttu-id="85b40-542">Cet attribut spécifie les options qui sont activées pour l’objet utilisateur ou contact.</span><span class="sxs-lookup"><span data-stu-id="85b40-542">This attribute specifies the options that are enabled for the user or contact object.</span></span> <span data-ttu-id="85b40-543">Cet attribut est une valeur de masquage de type binaire de type entier.</span><span class="sxs-lookup"><span data-stu-id="85b40-543">This attribute is a bit-mask value of type integer.</span></span> <span data-ttu-id="85b40-544">Chaque option est représentée par un bit.</span><span class="sxs-lookup"><span data-stu-id="85b40-544">Each option is represented by a bit.</span></span> <span data-ttu-id="85b40-545">Cet attribut est marqué pour la réplication de catalogue global.</span><span class="sxs-lookup"><span data-stu-id="85b40-545">This attribute is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="85b40-546">Les valeurs valides (et positions de bits associées) sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="85b40-546">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-547">1 : activé pour la connectivité de messagerie instantanée publique (position de bit 0)</span><span class="sxs-lookup"><span data-stu-id="85b40-547">1: Enabled for public instant messaging (IM) connectivity (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="85b40-548">2 : réservé (position binaire 1)</span><span class="sxs-lookup"><span data-stu-id="85b40-548">2: Reserved (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="85b40-549">4 : réservé (position binaire 2)</span><span class="sxs-lookup"><span data-stu-id="85b40-549">4: Reserved (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="85b40-550">8 : réservé (position binaire 3)</span><span class="sxs-lookup"><span data-stu-id="85b40-550">8: Reserved (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="85b40-551">16 : le contrôle d’appel distant a été activé [téléphonie] (position bit 4)</span><span class="sxs-lookup"><span data-stu-id="85b40-551">16: Remote call control Enabled [Telephony] (bit position 4)</span></span></p></li>
<li><p><span data-ttu-id="85b40-552">64 : AllowOrganizeMeetingWithAnonymousParticipants (permettre aux utilisateurs d’inviter des utilisateurs anonymes à des réunions (position de bit 6)</span><span class="sxs-lookup"><span data-stu-id="85b40-552">64: AllowOrganizeMeetingWithAnonymousParticipants (allow users to invite anonymous users to meetings (bit position 6)</span></span></p></li>
<li><p><span data-ttu-id="85b40-553">128 : UCEnabled (permettre aux utilisateurs pour les communications unifiées) (position bit 7)</span><span class="sxs-lookup"><span data-stu-id="85b40-553">128: UCEnabled (enable users for UC) (bit position 7)</span></span></p></li>
<li><p><span data-ttu-id="85b40-554">256 : EnabledForEnhancedPresence (activer l’utilisateur pour la connectivité de messagerie instantanée publique) (position de bit 8)</span><span class="sxs-lookup"><span data-stu-id="85b40-554">256: EnabledForEnhancedPresence (enable user for public IM connectivity) (bit position 8)</span></span></p></li>
<li><p><span data-ttu-id="85b40-555">512 : RemoteCallControlDualMode (position binaire 9)</span><span class="sxs-lookup"><span data-stu-id="85b40-555">512: RemoteCallControlDualMode (bit position 9)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="85b40-556">Nouveautés de Live Communications Server 2005 avec SP1.</span><span class="sxs-lookup"><span data-stu-id="85b40-556">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-557">msRTCSIP-OriginatorSID</span><span class="sxs-lookup"><span data-stu-id="85b40-557">msRTCSIP-OriginatorSID</span></span></p></td>
<td><p><span data-ttu-id="85b40-558">Cet attribut est utilisé dans les topologies de ressources et de forêts centrales pour activer l’authentification unique lorsque l’objet ObjectSID d’un utilisateur à partir du compte principal du serveur Windows NT est copié dans cet attribut de l’objet utilisateur ou contact correspondant dans la ressource ou la forêt centrale.</span><span class="sxs-lookup"><span data-stu-id="85b40-558">This attribute is used in resource and central forest topologies to enable single sign-on when a user’s ObjectSID from the Windows NT Server principal account is copied into this attribute of the corresponding user or contact object in the resource or central forest.</span></span> <span data-ttu-id="85b40-559">Office Communicator Web Access recherche un utilisateur dans AD DS en utilisant cet attribut ou l’ObjectSID de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-559">Communicator Web Access searches for a user in AD DS using this attribute or the user’s ObjectSID.</span></span> <span data-ttu-id="85b40-560">Cet attribut est marqué pour la réplication de catalogue global.</span><span class="sxs-lookup"><span data-stu-id="85b40-560">This attribute is marked for global catalog replication.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-561">msRTCSIP-OwnerUrn</span><span class="sxs-lookup"><span data-stu-id="85b40-561">msRTCSIP-OwnerUrn</span></span></p></td>
<td><p><span data-ttu-id="85b40-562">Cet attribut est le nom de ressource uniforme (URN) du propriétaire d’un contact d’application.</span><span class="sxs-lookup"><span data-stu-id="85b40-562">This attribute is the Uniform Resource Name (URN) of the owner for an application contact.</span></span></p></td>
<td><p><span data-ttu-id="85b40-563">Nouveautés de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-563">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-564">msRTCSIP-pattern (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-564">msRTCSIP-Pattern (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-565">Cet attribut de chaîne à une seule valeur contient un modèle utilisé pour faire correspondre les numéros de téléphone au format E. 164.</span><span class="sxs-lookup"><span data-stu-id="85b40-565">This single-valued string attribute contains a pattern used for matching dial numbers into E.164 format.</span></span> <span data-ttu-id="85b40-566">Si le numéro de téléphone correspond à ce modèle, la traduction est appliquée au numéro composé.</span><span class="sxs-lookup"><span data-stu-id="85b40-566">If the dial number matches this pattern, the translation is applied to the dialed number.</span></span></p></td>
<td><p><span data-ttu-id="85b40-567">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-567">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-568">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-568">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-569">msRTCSIP-PhoneRouteBL (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-569">msRTCSIP-PhoneRouteBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-570">Cet attribut à valeurs multiples contient une liste de noms uniques d’itinéraires téléphoniques.</span><span class="sxs-lookup"><span data-stu-id="85b40-570">This multi-valued attribute contains a list of phone route distinguished names (DN).</span></span> <span data-ttu-id="85b40-571">Cet attribut spécifie le lien précédent vers un ou plusieurs itinéraires téléphoniques.</span><span class="sxs-lookup"><span data-stu-id="85b40-571">This attribute specifies the back link to one or more phone routes.</span></span></p>
<p><span data-ttu-id="85b40-572">Lien précédent : <strong>ID de lien 11033</strong></span><span class="sxs-lookup"><span data-stu-id="85b40-572">Back link: <strong>Link ID 11033</strong></span></span></p>
<p><span data-ttu-id="85b40-573">Cet attribut correspond à la liaison suivante <strong>msRTCSIP-RouteUsageLinks</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-573">This attribute corresponds to the forward link <strong>msRTCSIP-RouteUsageLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-574">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-574">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-575">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-575">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-576">msRTCSIP-PhoneRouteData (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-576">msRTCSIP-PhoneRouteData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-577">Cet attribut est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85b40-577">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="85b40-578">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-578">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-579">msRTCSIP-PhoneRouteName (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-579">msRTCSIP-PhoneRouteName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-580">Cet attribut de chaîne UNICODE à valeur unique spécifie le nom convivial de l’itinéraire téléphonique, de sorte qu’il puisse facilement être référencé par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-580">This single valued UNICODE string attribute specifies the friendly name of the phone route, so it can easily be referenced by the administrator.</span></span></p></td>
<td><p><span data-ttu-id="85b40-581">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-581">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-582">msRTCSIP-PhoneUsageData (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-582">msRTCSIP-PhoneUsageData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-583">Cet attribut est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85b40-583">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="85b40-584">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-584">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-585">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-585">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-586">msRTCSIP-PolicyContent (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-586">msRTCSIP-PolicyContent (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-587">Cet attribut est une chaîne Unicode à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="85b40-587">This attribute is a single-valued Unicode string.</span></span> <span data-ttu-id="85b40-588">Cet attribut de chaîne contient la définition de la stratégie au format XML.</span><span class="sxs-lookup"><span data-stu-id="85b40-588">This string attribute contains the policy definition in XML format.</span></span> <span data-ttu-id="85b40-589">La définition de schéma XML est courante dans les différents types de stratégies, seuls les paramètres sont différents pour chaque type de stratégie.</span><span class="sxs-lookup"><span data-stu-id="85b40-589">The XML schema definition is common across different policy types, only the settings are different for each policy type.</span></span></p>
<p><span data-ttu-id="85b40-590">La définition de schéma XML (XSD) est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="85b40-590">The XML schema definition (XSD) is defined as follows:</span></span></p>
<pre><code>&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;
&lt;xs:schema id=&quot;instance&quot; xmlns=&quot;&quot; xmlns:xs=&quot;http://www.w3.org/2001/XMLSchema&quot; xmlns:msdata=&quot;urn:schemas-microsoft-com:xml-msdata&quot;&gt;
  &lt;xs:element name=&quot;instance&quot; msdata:IsDataSet=&quot;true&quot;&gt;
    &lt;xs:complexType&gt;
      &lt;xs:choice maxOccurs=&quot;unbounded&quot;&gt;
        &lt;xs:element name=&quot;property&quot; nillable=&quot;true&quot;&gt;
          &lt;xs:complexType&gt;
            &lt;xs:simpleContent msdata:ColumnName=&quot;property_Text&quot; msdata:Ordinal=&quot;1&quot;&gt;
              &lt;xs:extension base=&quot;xs:string&quot;&gt;
                &lt;xs:attribute name=&quot;name&quot; type=&quot;xs:string&quot; /&gt;
              &lt;/xs:extension&gt;
            &lt;/xs:simpleContent&gt;
          &lt;/xs:complexType&gt;
        &lt;/xs:element&gt;
      &lt;/xs:choice&gt;
    &lt;/xs:complexType&gt;
  &lt;/xs:element&gt;
&lt;/xs:schema&gt;</code></pre></td>
<td><p><span data-ttu-id="85b40-591">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-591">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-592">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-592">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-593">msRTCSIP-PolicyData (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-593">msRTCSIP-PolicyData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-594">Cet attribut est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85b40-594">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="85b40-595">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-595">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-596">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-596">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-597">msRTCSIP-PolicyType (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-597">msRTCSIP-PolicyType (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-598">Cet attribut de chaîne Unicode à valeur unique contient le type de stratégie.</span><span class="sxs-lookup"><span data-stu-id="85b40-598">This single-valued Unicode string attribute contains the policy type.</span></span> <span data-ttu-id="85b40-599">Les types de stratégie valides sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="85b40-599">Valid policy types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-600">répond</span><span class="sxs-lookup"><span data-stu-id="85b40-600">meeting</span></span></p></li>
<li><p><span data-ttu-id="85b40-601">téléphonie</span><span class="sxs-lookup"><span data-stu-id="85b40-601">telephony</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="85b40-602">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-602">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-603">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-603">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-604">msRTCSIP-PoolAddress</span><span class="sxs-lookup"><span data-stu-id="85b40-604">msRTCSIP-PoolAddress</span></span></p></td>
<td><p><span data-ttu-id="85b40-605">Cet attribut spécifie un lien vers le pool auquel appartient un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-605">This attribute specifies a link back to the pool to which a computer belongs.</span></span> <span data-ttu-id="85b40-606">Cet attribut est défini, que l’ordinateur exécute l’édition standard ou l’édition Enterprise de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="85b40-606">This attribute is set regardless of whether the computer is running the Standard Edition or the Enterprise Edition of Lync Server.</span></span> <span data-ttu-id="85b40-607">Cet attribut est marqué pour la réplication de catalogue global.</span><span class="sxs-lookup"><span data-stu-id="85b40-607">This attribute is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="85b40-608">La valeur valide est le nom de domaine du pool.</span><span class="sxs-lookup"><span data-stu-id="85b40-608">The valid value is the domain name of the pool.</span></span></p>
<p><span data-ttu-id="85b40-609">Lien suivant : <strong>ID de lien 11022</strong></span><span class="sxs-lookup"><span data-stu-id="85b40-609">Forward link: <strong>Link ID 11022</strong></span></span></p>
<p><span data-ttu-id="85b40-610">Le lien précédent correspondant à cet attribut de lien suivant est <strong>msRTCSIP-FrontEndServers</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-610">The corresponding back link to this forward link attribute is <strong>msRTCSIP-FrontEndServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-611">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-611">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-612">msRTCSIP-PoolAddresses</span><span class="sxs-lookup"><span data-stu-id="85b40-612">msRTCSIP-PoolAddresses</span></span></p></td>
<td><p><span data-ttu-id="85b40-613">Il s’agit d’un attribut à valeurs multiples qui contient une liste de noms uniques (DN) de pools avec lesquels la fabrique MCU est associée.</span><span class="sxs-lookup"><span data-stu-id="85b40-613">This is a multi-valued attribute that contains a list of the distinguished names (DN) of pools with which the MCU factory is associated.</span></span></p>
<p><span data-ttu-id="85b40-614">Lien précédent : <strong>ID de lien 11025</strong></span><span class="sxs-lookup"><span data-stu-id="85b40-614">Back link: <strong>Link ID 11025</strong></span></span></p>
<p><span data-ttu-id="85b40-615">Le lien transférer correspondant à ce lien précédent est <strong>msRTCSIP-MCUFactoryPath</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-615">The corresponding forward link to this back link is <strong>msRTCSIP-MCUFactoryPath</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-616">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-616">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-617">msRTCSIP-PoolData</span><span class="sxs-lookup"><span data-stu-id="85b40-617">msRTCSIP-PoolData</span></span></p></td>
<td><p><span data-ttu-id="85b40-618">Cet attribut est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85b40-618">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="85b40-619">Nouveautés de Live Communications Server 2005 avec SP1.</span><span class="sxs-lookup"><span data-stu-id="85b40-619">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-620">msRTCSIP-PoolDisplayName</span><span class="sxs-lookup"><span data-stu-id="85b40-620">msRTCSIP-PoolDisplayName</span></span></p></td>
<td><p><span data-ttu-id="85b40-621">Cet attribut spécifie un nom arbitraire pour un pool affiché par la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="85b40-621">This attribute specifies an arbitrary name for a pool that is displayed by the management console.</span></span> <span data-ttu-id="85b40-622">Ce nom peut être modifié par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-622">This name can be changed by the administrator.</span></span></p>
<p><span data-ttu-id="85b40-623">La valeur valide est une chaîne qui représente le nom d’un pool.</span><span class="sxs-lookup"><span data-stu-id="85b40-623">The valid value is a string representing the name of a pool.</span></span></p></td>
<td><p><span data-ttu-id="85b40-624">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-624">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-625">msRTCSIP-PoolDomainFQDN</span><span class="sxs-lookup"><span data-stu-id="85b40-625">msRTCSIP-PoolDomainFQDN</span></span></p></td>
<td><p><span data-ttu-id="85b40-626">Cet attribut est une valeur de chaîne à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="85b40-626">This attribute is a single-valued string value.</span></span> <span data-ttu-id="85b40-627">La valeur de cet attribut, le cas échéant, représente le nom de domaine complet (FQDN) du pool si l’administrateur souhaite créer un pool frontal à l’aide d’un nom de domaine complet qui n’est pas conforme à la structure de domaine Active Directory dans laquelle le pool frontal est créé (par exemple, un espace de noms SIP disjoint d’un espace de noms DNS).</span><span class="sxs-lookup"><span data-stu-id="85b40-627">The value of this attribute, when present, represents the pool’s domain FQDN if the administrator wants to create a Front End pool with an FQDN that does not conform to the Active Directory domain structure in which the Front End pool is created (for example, a SIP namespace disjoined from Domain Name System (DNS) namespace).</span></span></p>
<p><span data-ttu-id="85b40-628">Nous vous recommandons de mapper le nom de domaine complet (FQDN) du pool frontal à la partie nom de domaine en tant que domaine Active Directory dans lequel réside le pool.</span><span class="sxs-lookup"><span data-stu-id="85b40-628">We recommend that you map the Front End pool domain FQDN to the domain name portion as the Active Directory domain in which the pool resides.</span></span> <span data-ttu-id="85b40-629">Par conséquent, quand aucune valeur n’est présente dans cet attribut, le nom de domaine complet du pool frontal est défini par défaut sur la structure de nom de domaine Active Directory, tel qu’il est indiqué par l’attribut <strong>dNSHostName</strong> .</span><span class="sxs-lookup"><span data-stu-id="85b40-629">Therefore, when no value is present in this attribute, the Front End pool FQDN will default to the Active Directory domain name structure, as denoted by the <strong>dnsHostName</strong> attribute.</span></span></p></td>
<td><p><span data-ttu-id="85b40-630">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-630">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-631">msRTCSIP-PoolFunctionality</span><span class="sxs-lookup"><span data-stu-id="85b40-631">msRTCSIP-PoolFunctionality</span></span></p></td>
<td><p><span data-ttu-id="85b40-632">Liste à plusieurs valeurs des noms de domaine de tous les serveurs Lync Server Enterprise Edition associés à un pool.</span><span class="sxs-lookup"><span data-stu-id="85b40-632">A multi-valued list of the domain names of all Lync Server, Enterprise Edition servers associated with a pool.</span></span> <span data-ttu-id="85b40-633">Cet attribut de type entier détermine si le pool est compatible avec la messagerie instantanée (mi) et la présence et les réunions.</span><span class="sxs-lookup"><span data-stu-id="85b40-633">This attribute of type integer defines whether the pool is capable of instant messaging (IM) and presence, and meetings.</span></span></p>
<p><span data-ttu-id="85b40-634">Les types de valeurs valides possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="85b40-634">The possible valid value types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-635">Non défini : service de messagerie instantanée et de présence (Live Communications Server 2005 et 2003)</span><span class="sxs-lookup"><span data-stu-id="85b40-635">Undefined: IM and Presence Service (Live Communications Server 2005 and 2003)</span></span></p></li>
<li><p><span data-ttu-id="85b40-636">1 : service de messagerie instantanée et de présence (Lync Server)</span><span class="sxs-lookup"><span data-stu-id="85b40-636">1: IM and Presence Service (Lync Server)</span></span></p></li>
<li><p><span data-ttu-id="85b40-637">2 : messagerie instantanée, présence et service de réunion (Lync Server)</span><span class="sxs-lookup"><span data-stu-id="85b40-637">2: IM and Presence and Meeting Service (Lync Server)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="85b40-638">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-638">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-639">msRTCSIP-PoolType</span><span class="sxs-lookup"><span data-stu-id="85b40-639">msRTCSIP-PoolType</span></span></p></td>
<td><p><span data-ttu-id="85b40-640">Cet attribut spécifie si un pool de serveurs exécute Standard Edition Server ou Server Enterprise Edition Server.</span><span class="sxs-lookup"><span data-stu-id="85b40-640">This attribute specifies whether a server pool is running Standard Edition server or Enterprise Edition server.</span></span> <span data-ttu-id="85b40-641">Cet attribut est une valeur de masquage de type binaire de type entier.</span><span class="sxs-lookup"><span data-stu-id="85b40-641">This attribute is a bit-mask value of type integer.</span></span> <span data-ttu-id="85b40-642">Chaque option est représentée par un bit.</span><span class="sxs-lookup"><span data-stu-id="85b40-642">Each option is represented by a bit.</span></span></p>
<p><span data-ttu-id="85b40-643">Les valeurs valides (et positions de bits associées) sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="85b40-643">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-644">1 : Standard Edition Server, hébergement des utilisateurs (position de bit 0)</span><span class="sxs-lookup"><span data-stu-id="85b40-644">1: Standard Edition server, hosts users (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="85b40-645">2 : serveur Enterprise Edition, hébergement des utilisateurs (position binaire 1)</span><span class="sxs-lookup"><span data-stu-id="85b40-645">2: Enterprise Edition server, hosts users (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="85b40-646">4 : Standard Edition Server et applications hébergées (position binaire 2)</span><span class="sxs-lookup"><span data-stu-id="85b40-646">4: Standard Edition server, hosts applications (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="85b40-647">8 : serveur Enterprise Edition, applications d’hébergement (position de bit 3)</span><span class="sxs-lookup"><span data-stu-id="85b40-647">8: Enterprise Edition server, hosts applications (bit position 3)</span></span></p></li>
</ul>
<p><span data-ttu-id="85b40-648">Dans la mesure où Lync Server ne prend pas en charge les pools hébergeant uniquement des applications, les seules valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="85b40-648">Because Lync Server does not support pools that host only applications, the only valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-649">5 : Standard Edition Server, hébergement des utilisateurs et des applications (positions de bit 0 et 2)</span><span class="sxs-lookup"><span data-stu-id="85b40-649">5: Standard Edition server, hosts users and applications (bit positions 0 and 2)</span></span></p></li>
<li><p><span data-ttu-id="85b40-650">10 : serveur Enterprise Edition, héberge les utilisateurs et les applications (emplacements des points 1 et 3)</span><span class="sxs-lookup"><span data-stu-id="85b40-650">10: Enterprise Edition server, hosts users and applications (bit positions 1 and 3)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="85b40-651">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-651">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-652">msRTCSIP-PoolVersion</span><span class="sxs-lookup"><span data-stu-id="85b40-652">msRTCSIP-PoolVersion</span></span></p></td>
<td><p><span data-ttu-id="85b40-653">Cet attribut définit la version du pool.</span><span class="sxs-lookup"><span data-stu-id="85b40-653">This attribute defines the pool version.</span></span> <span data-ttu-id="85b40-654">Il s’agit d’un type entier qui est incrémenté avec chaque version de produit majeure.</span><span class="sxs-lookup"><span data-stu-id="85b40-654">It is an integer type that is incremented with each major product release.</span></span></p>
<p><span data-ttu-id="85b40-655">Les types de valeurs valides possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="85b40-655">The possible valid value types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-656">0 : Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="85b40-656">0: Live Communications Server 2003</span></span></p></li>
<li><p><span data-ttu-id="85b40-657">1 : Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="85b40-657">1: Live Communications Server 2005</span></span></p></li>
<li><p><span data-ttu-id="85b40-658">2 : Live Communications Server 2005 avec SP1</span><span class="sxs-lookup"><span data-stu-id="85b40-658">2: Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="85b40-659">3 : Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="85b40-659">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="85b40-660">4 : Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="85b40-660">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="85b40-661">5 : Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="85b40-661">5: Lync Server 2010</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="85b40-662">Live Communications Server 2005 avec SP1.</span><span class="sxs-lookup"><span data-stu-id="85b40-662">Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-663">msRTCSIP-PresenceFlags</span><span class="sxs-lookup"><span data-stu-id="85b40-663">msRTCSIP-PresenceFlags</span></span></p></td>
<td><p><span data-ttu-id="85b40-664">Cet attribut contient des options et des indicateurs permettant de définir les paramètres de présence.</span><span class="sxs-lookup"><span data-stu-id="85b40-664">This attribute contains options and flags that define presence settings.</span></span></p></td>
<td><p><span data-ttu-id="85b40-665">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-665">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-666">msRTCSIP-PresencePolicy</span><span class="sxs-lookup"><span data-stu-id="85b40-666">msRTCSIP-PresencePolicy</span></span></p></td>
<td><p><span data-ttu-id="85b40-667">Cet attribut contient le DN d’un objet de stratégie de présence.</span><span class="sxs-lookup"><span data-stu-id="85b40-667">This attribute contains the DN for a presence policy object.</span></span></p></td>
<td><p><span data-ttu-id="85b40-668">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-668">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-669">msRTCSIP-PrimaryHomeServer</span><span class="sxs-lookup"><span data-stu-id="85b40-669">msRTCSIP-PrimaryHomeServer</span></span></p></td>
<td><p><span data-ttu-id="85b40-670">Cet attribut autorise un utilisateur ou un contact à la messagerie SIP.</span><span class="sxs-lookup"><span data-stu-id="85b40-670">This attribute enables a user or contact for SIP messaging.</span></span> <span data-ttu-id="85b40-671">Il est ajouté à la classe contact, car dans la topologie centrale de la forêt, les objets de contact, pas les objets utilisateur, sont activés par SIP.</span><span class="sxs-lookup"><span data-stu-id="85b40-671">It is added to the contact class because in the central forest topology, contact objects, not user objects, are SIP enabled.</span></span></p>
<p><span data-ttu-id="85b40-672">La valeur valide est le nom de domaine principal du serveur Standard Edition Server ou du pool frontal d’Enterprise Edition dans lequel un utilisateur est hébergé.</span><span class="sxs-lookup"><span data-stu-id="85b40-672">The valid value is the DN of the Standard Edition server or Enterprise Edition Front End pool where a user is homed.</span></span></p></td>
<td><p><span data-ttu-id="85b40-673">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-673">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-674">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="85b40-674">msRTCSIP-PrimaryUserAddress</span></span></p></td>
<td><p><span data-ttu-id="85b40-675">Cet attribut contient l’adresse SIP d’un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="85b40-675">This attribute contains the SIP address of a given user.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-676">msRTCSIP-PrivateLine</span><span class="sxs-lookup"><span data-stu-id="85b40-676">msRTCSIP-PrivateLine</span></span></p></td>
<td><p><span data-ttu-id="85b40-677">Cet attribut contient l’ID d’appareil de l’appareil de lignes privées.</span><span class="sxs-lookup"><span data-stu-id="85b40-677">This attribute contains the device ID of the private line device.</span></span></p></td>
<td><p><span data-ttu-id="85b40-678">Nouveautés de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-678">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-679">msRTCSIP-routable</span><span class="sxs-lookup"><span data-stu-id="85b40-679">msRTCSIP-Routable</span></span></p></td>
<td><p><span data-ttu-id="85b40-680">Cet attribut est un attribut booléen utilisé pour déterminer si Lync Server est autorisé à router vers ce service en utilisant son adresse GRUU.</span><span class="sxs-lookup"><span data-stu-id="85b40-680">This attribute is a Boolean attribute used to determine whether Lync Server is authorized to route to this service using its GRUU address.</span></span> <span data-ttu-id="85b40-681">Si cette valeur est définie sur <strong>true</strong>, Lync Server est autorisé à effectuer le routage vers ce service.</span><span class="sxs-lookup"><span data-stu-id="85b40-681">If this value is set to <strong>TRUE</strong>, Lync Server is authorized to route to this service.</span></span> <span data-ttu-id="85b40-682">Si cette valeur est définie sur <strong>false</strong>, le serveur Lync n’est pas autorisé à router vers ce service.</span><span class="sxs-lookup"><span data-stu-id="85b40-682">If this value is set to <strong>FALSE</strong>, Lync Server is not authorized to route to this service.</span></span></p></td>
<td><p><span data-ttu-id="85b40-683">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-683">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-684">msRTCSIP-RouteUsageAttribute (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-684">msRTCSIP-RouteUsageAttribute (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-685">Cet attribut de chaîne UNICODE à valeur unique définit un attribut qui qualifie l’utilisation pour un itinéraire téléphonique.</span><span class="sxs-lookup"><span data-stu-id="85b40-685">This single-valued UNICODE string attribute defines an attribute that qualifies the usage for a phone route.</span></span> <span data-ttu-id="85b40-686">La sélection d’un itinéraire de téléphone est déterminée en fonction de deux éléments : l’attribut utilisation attribué à l’itinéraire du téléphone et les attributs d’utilisation de stratégie autorisés de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="85b40-686">Selection of a phone route is determined based on two elements: the usage attribute assigned to the phone route and the caller’s allowed policy usage attributes.</span></span> <span data-ttu-id="85b40-687">Le premier itinéraire téléphonique avec un attribut utilisation qui correspond à l’utilisation autorisée de l’appelant est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="85b40-687">The first phone route with a usage attribute that matches the caller’s allowed usage is selected.</span></span></p></td>
<td><p><span data-ttu-id="85b40-688">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-688">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-689">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-689">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-690">msRTCSIP-RouteUsageLinks (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-690">msRTCSIP-RouteUsageLinks (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-691">Cet attribut de nom unique (DN) à valeurs multiples contient une liste des noms uniques de l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="85b40-691">This multi-valued distinguished name (DN) attribute contains a list of route usage distinguished names.</span></span></p>
<p><span data-ttu-id="85b40-692">Lien suivant : <strong>ID de lien 11032</strong></span><span class="sxs-lookup"><span data-stu-id="85b40-692">Forward link: <strong>Link ID 11032</strong></span></span></p>
<p><span data-ttu-id="85b40-693">Cet attribut est un lien de transfert vers la liaison de renvoi correspondante de <strong>msRTCSIP-PhoneRouteBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-693">This attribute is a forward link to the corresponding back link <strong>msRTCSIP-PhoneRouteBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-694">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-694">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-695">msRTCSIP-RoutingPoolDN</span><span class="sxs-lookup"><span data-stu-id="85b40-695">msRTCSIP-RoutingPoolDN</span></span></p></td>
<td><p><span data-ttu-id="85b40-696">Cet attribut contient le DN qui pointe vers le pool sur lequel tout le trafic SIP adressé à ce MCU ou à ce service approuvé doit traverser.</span><span class="sxs-lookup"><span data-stu-id="85b40-696">This attribute contains the DN that points to the pool that all SIP traffic addressed to this MCU or Trusted Service must go through.</span></span></p></td>
<td><p><span data-ttu-id="85b40-697">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-697">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-698">msRTCSIP-RuleName (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-698">msRTCSIP-RuleName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-699">Cet attribut de chaîne UNICODE à valeur unique spécifie le nom convivial de la règle de normalisation, afin qu’il puisse facilement être référencé par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-699">This single-valued UNICODE string attribute specifies the friendly name of the normalization rule, so it can easily be referenced by an administrator.</span></span></p></td>
<td><p><span data-ttu-id="85b40-700">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-700">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-701">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-701">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-702">msRTCSIP-SchemaVersion</span><span class="sxs-lookup"><span data-stu-id="85b40-702">msRTCSIP-SchemaVersion</span></span></p></td>
<td><p><span data-ttu-id="85b40-703">Cet attribut représente la version de schéma actuellement déployée au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="85b40-703">This attribute represents the schema version currently deployed in the organization.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-704">msRTCSIP-SearchMaxRequests (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-704">msRTCSIP-SearchMaxRequests (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-705">Cet attribut limite le nombre de résultats de recherche à retourner à partir d’une recherche dans l’annuaire lorsqu’un utilisateur recherche un contact à l’aide de Communicator.</span><span class="sxs-lookup"><span data-stu-id="85b40-705">This attribute limits the number of search results to be returned from a directory search when a user searches for a contact using Communicator.</span></span> <span data-ttu-id="85b40-706">Cet attribut remplace la valeur fournie par le client.</span><span class="sxs-lookup"><span data-stu-id="85b40-706">This attribute will override the value provided by the client.</span></span></p></td>
<td><p><span data-ttu-id="85b40-707">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-707">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-708">msRTCSIP-SearchMaxResults (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-708">msRTCSIP-SearchMaxResults (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-709">Cet attribut limite le nombre de demandes de recherche renvoyées.</span><span class="sxs-lookup"><span data-stu-id="85b40-709">This attribute limits the number of search requests returned.</span></span></p></td>
<td><p><span data-ttu-id="85b40-710">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-710">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-711">msRTCSIP-ServerBL</span><span class="sxs-lookup"><span data-stu-id="85b40-711">msRTCSIP-ServerBL</span></span></p></td>
<td><p><span data-ttu-id="85b40-712">Cet attribut à valeurs multiples est un lien précédent contenant une liste de noms uniques (DN).</span><span class="sxs-lookup"><span data-stu-id="85b40-712">This multi-valued attribute is a back link that contains a list of distinguished names (DN).</span></span> <span data-ttu-id="85b40-713">Ces DN pointent vers un objet pool ou <strong>TrustedService</strong> .</span><span class="sxs-lookup"><span data-stu-id="85b40-713">These DNs point to a pool or <strong>TrustedService</strong> object.</span></span></p>
<p><span data-ttu-id="85b40-714">Cet attribut correspond à la liaison suivante <strong>msRTCSIP-TrustedServiceLinks</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-714">This attribute corresponds to the forward link <strong>msRTCSIP-TrustedServiceLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-715">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-715">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-716">msRTCSIP-ServerData</span><span class="sxs-lookup"><span data-stu-id="85b40-716">msRTCSIP-ServerData</span></span></p></td>
<td><p><span data-ttu-id="85b40-717">Cet attribut est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85b40-717">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-718">msRTCSIP-ServerReferenceBL (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-718">msRTCSIP-ServerReferenceBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-719">Cet attribut à valeurs multiples contient une liste de noms uniques.</span><span class="sxs-lookup"><span data-stu-id="85b40-719">This multi-valued attribute contains a list of distinguished names.</span></span> <span data-ttu-id="85b40-720">Ces noms uniques sont des liens de retour qui font référence à d’autres objets serveur qui peuvent être affectés à un profil d’emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="85b40-720">These distinguished names are back links that reference other server objects that can be assigned a default location profile.</span></span></p>
<p><span data-ttu-id="85b40-721">Lien précédent : <strong>ID de lien 11037</strong></span><span class="sxs-lookup"><span data-stu-id="85b40-721">Back link: <strong>Link ID 11037</strong></span></span></p>
<p><span data-ttu-id="85b40-722">Le lien transférer correspondant à ce lien précédent est <strong>msRTCSIP-DefaultLocationProfileLink</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-722">The corresponding forward link to this back link is <strong>msRTCSIP-DefaultLocationProfileLink</strong>.</span></span></p>
<p><span data-ttu-id="85b40-723">Cet attribut de lien précédent fait référence uniquement aux pools et aux serveurs de médiation.</span><span class="sxs-lookup"><span data-stu-id="85b40-723">This back link attribute references pools and Mediation Servers only.</span></span></p></td>
<td><p><span data-ttu-id="85b40-724">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-724">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-725">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-725">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-726">msRTCSIP-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="85b40-726">msRTCSIP-ServerVersion</span></span></p></td>
<td><p><span data-ttu-id="85b40-727">Cet attribut définit les informations de version du serveur.</span><span class="sxs-lookup"><span data-stu-id="85b40-727">This attribute defines the version information of the server.</span></span> <span data-ttu-id="85b40-728">Ce numéro de version s’applique à tous les rôles de serveur.</span><span class="sxs-lookup"><span data-stu-id="85b40-728">This version number applies to all server roles.</span></span> <span data-ttu-id="85b40-729">Il s’agit d’un entier monotonously croissant qui s’incrémente avec chaque publication officielle du produit.</span><span class="sxs-lookup"><span data-stu-id="85b40-729">It is a monotonously increasing integer that increments with each official product release.</span></span></p>
<p><span data-ttu-id="85b40-730">Les valeurs valides possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="85b40-730">The possible valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-731">Non défini : Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="85b40-731">Undefined: Live Communications Server 2003</span></span></p>
<p>                 <span data-ttu-id="85b40-732">Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="85b40-732">Live Communications Server 2005</span></span></p>
<p>                 <span data-ttu-id="85b40-733">Live Communications Server 2005 avec SP1</span><span class="sxs-lookup"><span data-stu-id="85b40-733">Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="85b40-734">3 : Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="85b40-734">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="85b40-735">4 : Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="85b40-735">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="85b40-736">5 : Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="85b40-736">5: Lync Server 2010</span></span></p></li>
<li><p><span data-ttu-id="85b40-737">6 : Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85b40-737">6: Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="85b40-738">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-738">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-739">msRTCSIP-SourceObjectType</span><span class="sxs-lookup"><span data-stu-id="85b40-739">msRTCSIP-SourceObjectType</span></span></p></td>
<td><p><span data-ttu-id="85b40-740">Cet attribut à une seule valeur de type entier spécifie le type d’objet sur lequel pointe <strong>MSDS-SourceObjectDN</strong> , comme suit :</span><span class="sxs-lookup"><span data-stu-id="85b40-740">This single-valued attribute of integer type specifies the type of object the <strong>msDS-SourceObjectDN</strong> points to, as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-741">null | 0x00000001 : représente un objet utilisateur principal du serveur Windows NT d’une autre forêt</span><span class="sxs-lookup"><span data-stu-id="85b40-741">null | 0x00000001: Represents a Windows NT Server principal user object from a different forest</span></span></p></li>
<li><p><span data-ttu-id="85b40-742">Les attributs suivants représentent un type de groupe à partir d’une autre forêt pour l’extension du groupe de distribution :</span><span class="sxs-lookup"><span data-stu-id="85b40-742">The following attributes represent a group type from a different forest for distribution group expansion:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-743">0x00000002 : ADS_GROUP_TYPE_GLOBAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="85b40-743">0x00000002: ADS_GROUP_TYPE_GLOBAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="85b40-744">0x00000004 : ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="85b40-744">0x00000004: ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="85b40-745">0x00000004 : ADS_GROUP_TYPE_LOCAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="85b40-745">0x00000004: ADS_GROUP_TYPE_LOCAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="85b40-746">0x00000008 : ADS_GROUP_TYPE_UNIVERSAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="85b40-746">0x00000008: ADS_GROUP_TYPE_UNIVERSAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="85b40-747">0x80000000 : ADS_GROUP_TYPE_SECURITY_ENABLED</span><span class="sxs-lookup"><span data-stu-id="85b40-747">0x80000000: ADS_GROUP_TYPE_SECURITY_ENABLED</span></span></p></li>
<li><p><span data-ttu-id="85b40-748">0x90000000 : représente un objet de standard automatique ou d’accès d’abonné de la même forêt ou d’une autre forêt.</span><span class="sxs-lookup"><span data-stu-id="85b40-748">0x90000000: Represents an Auto-Attendant or subscriber access object from the same forest or a different forest</span></span></p></li>
</ul></li>
</ul></td>
<td><p><span data-ttu-id="85b40-749">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-749">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-750">msRTCSIP-SubscriptionAuthRequired (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-750">msRTCSIP-SubscriptionAuthRequired (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="85b40-751">Nouveautés de Live Communications Server 2003.</span><span class="sxs-lookup"><span data-stu-id="85b40-751">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="85b40-752">Obsolète dans Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-752">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-753">msRTCSIP-TargetHomeServer</span><span class="sxs-lookup"><span data-stu-id="85b40-753">msRTCSIP-TargetHomeServer</span></span></p></td>
<td><p><span data-ttu-id="85b40-754">Cet attribut vous permet de déplacer un utilisateur ou un objet contact d’un pool de serveurs Lync vers un autre.</span><span class="sxs-lookup"><span data-stu-id="85b40-754">This attribute enables you to move a user or contact object from one Lync Server pool to another.</span></span> <span data-ttu-id="85b40-755">Cet attribut est ajouté à la classe contact en raison de l’activation de l’option SIP dans la topologie centrale de la forêt.</span><span class="sxs-lookup"><span data-stu-id="85b40-755">This attribute is added to the contact class, because in the central forest topology, contact objects, not user objects, are SIP enabled.</span></span></p>
<p><span data-ttu-id="85b40-756">La valeur valide est le nom d’utilisateur de l’emplacement du serveur Standard Edition Server ou du pool frontal vers lequel un utilisateur doit être déplacé.</span><span class="sxs-lookup"><span data-stu-id="85b40-756">The valid value is the DN of the destination Standard Edition server or Front End pool to which a user is to be moved.</span></span></p></td>
<td><p><span data-ttu-id="85b40-757">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-757">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-758">msRTCSIP-TargetPhoneNumber (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-758">msRTCSIP-TargetPhoneNumber (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-759">Cet attribut de chaîne à une seule valeur contient un modèle de numéro de téléphone ou une plage pour diriger vers les passerelles spécifiées définies dans <strong>msRTCSIP-passerelles</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-759">This single-valued string attribute contains a phone number pattern or range to route to the specified gateways defined in <strong>msRTCSIP-Gateways</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-760">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-760">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-761">msRTCSIP-TargetUserPolicies</span><span class="sxs-lookup"><span data-stu-id="85b40-761">msRTCSIP-TargetUserPolicies</span></span></p></td>
<td><p><span data-ttu-id="85b40-762">Cet attribut stocke les paires nom-valeur pour les stratégies cibles pour les utilisateurs de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="85b40-762">This attribute stores name-value pairs for target policies for Lync Server users.</span></span></p></td>
<td><p><span data-ttu-id="85b40-763">Nouveautés de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-763">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-764">msRTCSIP-IDClient</span><span class="sxs-lookup"><span data-stu-id="85b40-764">msRTCSIP-TenantId</span></span></p></td>
<td><p><span data-ttu-id="85b40-765">Cet attribut stocke l’identificateur unique d’un client.</span><span class="sxs-lookup"><span data-stu-id="85b40-765">This attribute stores the unique identifier for a tenant.</span></span></p></td>
<td><p><span data-ttu-id="85b40-766">Nouveautés de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-766">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-767">msRTCSIP-traduction (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-767">msRTCSIP-Translation (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-768">Cet attribut est utilisé par la fonctionnalité voix de Lync Server et contient la chaîne de traduction à appliquer sur le numéro composé, si une correspondance est trouvée.</span><span class="sxs-lookup"><span data-stu-id="85b40-768">This attribute is used by the voice feature of Lync Server and contains the translation string to apply on the dialed number, if a match is found.</span></span></p></td>
<td><p><span data-ttu-id="85b40-769">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-769">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="85b40-770">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-770">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-771">msRTCSIP-TrustedMCUData</span><span class="sxs-lookup"><span data-stu-id="85b40-771">msRTCSIP-TrustedMCUData</span></span></p></td>
<td><p><span data-ttu-id="85b40-772">Cet attribut est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85b40-772">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="85b40-773">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-773">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-774">msRTCSIP-TrustedMCUFQDN</span><span class="sxs-lookup"><span data-stu-id="85b40-774">msRTCSIP-TrustedMCUFQDN</span></span></p></td>
<td><p><span data-ttu-id="85b40-775">Cet attribut est une valeur de chaîne qui contient le nom de domaine complet de la MCU.</span><span class="sxs-lookup"><span data-stu-id="85b40-775">This attribute is a string value that contains the FQDN of the MCU.</span></span> <span data-ttu-id="85b40-776">Il s’agit d’un attribut à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="85b40-776">This is a single-valued attribute.</span></span> <span data-ttu-id="85b40-777">La valeur valide de chaque segment est de 63 caractères. la valeur valide pour le nom de domaine complet est de 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="85b40-777">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="85b40-778">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-778">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-779">msRTCSIP-TrustedProxyData</span><span class="sxs-lookup"><span data-stu-id="85b40-779">msRTCSIP-TrustedProxyData</span></span></p></td>
<td><p><span data-ttu-id="85b40-780">Cet attribut est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85b40-780">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="85b40-781">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-781">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-782">msRTCSIP-TrustedProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="85b40-782">msRTCSIP-TrustedProxyFQDN</span></span></p></td>
<td><p><span data-ttu-id="85b40-783">Cet attribut est une valeur de chaîne contenant le nom de domaine complet du serveur proxy exécutant.</span><span class="sxs-lookup"><span data-stu-id="85b40-783">This attribute is a string value that contains the FQDN of the server running Proxy Server.</span></span> <span data-ttu-id="85b40-784">Cet attribut a une valeur unique.</span><span class="sxs-lookup"><span data-stu-id="85b40-784">This attribute is single-valued.</span></span> <span data-ttu-id="85b40-785">La valeur valide de chaque segment est de 63 caractères. la valeur valide pour le nom de domaine complet est de 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="85b40-785">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="85b40-786">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-786">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-787">msRTCSIP-TrustedServerData</span><span class="sxs-lookup"><span data-stu-id="85b40-787">msRTCSIP-TrustedServerData</span></span></p></td>
<td><p><span data-ttu-id="85b40-788">Cet attribut est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85b40-788">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-789">msRTCSIP-TrustedServerFQDN</span><span class="sxs-lookup"><span data-stu-id="85b40-789">msRTCSIP-TrustedServerFQDN</span></span></p></td>
<td><p><span data-ttu-id="85b40-790">Cet attribut est un attribut à valeur unique qui représente le nom de domaine complet d’un serveur approuvé.</span><span class="sxs-lookup"><span data-stu-id="85b40-790">This attribute is a single-valued attribute that represents the FQDN of a trusted server.</span></span></p></td>
<td><p><span data-ttu-id="85b40-791">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-791">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-792">msRTCSIP-TrustedServerVersion</span><span class="sxs-lookup"><span data-stu-id="85b40-792">msRTCSIP-TrustedServerVersion</span></span></p></td>
<td><p><span data-ttu-id="85b40-793">Cet attribut spécifie le numéro de version d’un serveur dans la liste des serveurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="85b40-793">This attribute specifies the version number of a server in the trusted server list.</span></span></p>
<p><span data-ttu-id="85b40-794">Les valeurs valides possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="85b40-794">The possible valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-795">NULL : Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="85b40-795">NULL: Live Communications Server 2003</span></span></p></li>
<li><p><span data-ttu-id="85b40-796">2 : Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="85b40-796">2: Live Communications Server 2005</span></span></p></li>
<li><p><span data-ttu-id="85b40-797">3 : Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="85b40-797">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="85b40-798">4 : Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="85b40-798">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="85b40-799">5 : Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="85b40-799">5: Lync Server 2010</span></span></p></li>
<li><p><span data-ttu-id="85b40-800">6 : Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85b40-800">6: Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="85b40-801">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-801">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-802">msRTCSIP-TrustedServiceFlags</span><span class="sxs-lookup"><span data-stu-id="85b40-802">msRTCSIP-TrustedServiceFlags</span></span></p></td>
<td><p><span data-ttu-id="85b40-803">Cet attribut définit les options qui sont activées pour le service approuvé.</span><span class="sxs-lookup"><span data-stu-id="85b40-803">This attribute defines the options that are enabled for the trusted service.</span></span></p></td>
<td><p><span data-ttu-id="85b40-804">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-804">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-805">msRTCSIP-TrustedServiceLinks</span><span class="sxs-lookup"><span data-stu-id="85b40-805">msRTCSIP-TrustedServiceLinks</span></span></p></td>
<td><p><span data-ttu-id="85b40-806">Cet attribut à valeurs multiples contient une liste de noms uniques (ND) qui font référence à un objet de service approuvé, tel qu’un service d’authentification par relais de média.</span><span class="sxs-lookup"><span data-stu-id="85b40-806">This multi-valued attribute contains a list of distinguished names (DN) that reference a trusted service object, such as a Media Relay Authentication Service.</span></span> <span data-ttu-id="85b40-807">Un service d’authentification de relais de média (physiquement localisé sur le serveur Edge exécutant le service de conférence A/V) doit être associé à un pool pour prendre en charge les scénarios audio des utilisateurs distants.</span><span class="sxs-lookup"><span data-stu-id="85b40-807">A Media Relay Authentication Service (physically collocated on the Edge Server running the A/V Conferencing service) must be associated with a pool to support audio scenarios for remote users.</span></span></p>
<p><span data-ttu-id="85b40-808">Le lien précédent correspondant à cet attribut de lien suivant est <strong>msRTCSIP-ServerBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-808">The corresponding back link to this forward link attribute is <strong>msRTCSIP-ServerBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-809">CITÉ</span><span class="sxs-lookup"><span data-stu-id="85b40-809">UC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-810">msRTCSIP-TrustedServicePort</span><span class="sxs-lookup"><span data-stu-id="85b40-810">msRTCSIP-TrustedServicePort</span></span></p></td>
<td><p><span data-ttu-id="85b40-811">Cet attribut est un entier qui définit le numéro de port utilisé pour la connexion à ce service GRUU.</span><span class="sxs-lookup"><span data-stu-id="85b40-811">This attribute is an integer that defines the port number used to connect to this GRUU service.</span></span></p></td>
<td><p><span data-ttu-id="85b40-812">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-812">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-813">msRTCSIP-TrustedServiceType</span><span class="sxs-lookup"><span data-stu-id="85b40-813">msRTCSIP-TrustedServiceType</span></span></p></td>
<td><p><span data-ttu-id="85b40-814">Cet attribut est une valeur de chaîne qui définit le type de service GRUU qu’il représente.</span><span class="sxs-lookup"><span data-stu-id="85b40-814">This attribute is a string value that defines the type of GRUU service it represents.</span></span></p>
<p><span data-ttu-id="85b40-815">Les types de services GRUU valides sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="85b40-815">The valid GRUU service types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-816">Le serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="85b40-816">MediationServer</span></span></p></li>
<li><p><span data-ttu-id="85b40-817">Passerelle</span><span class="sxs-lookup"><span data-stu-id="85b40-817">Gateway</span></span></p></li>
<li><p><span data-ttu-id="85b40-818">Service d’authentification de relais de média (MRAS)</span><span class="sxs-lookup"><span data-stu-id="85b40-818">Media Relay Authentication Service (MRAS)</span></span></p></li>
<li><p><span data-ttu-id="85b40-819">QoSM</span><span class="sxs-lookup"><span data-stu-id="85b40-819">QoSM</span></span></p></li>
<li><p><span data-ttu-id="85b40-820">msRTCSIP-UserExtension CWA</span><span class="sxs-lookup"><span data-stu-id="85b40-820">msRTCSIP-UserExtension CWA</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="85b40-821">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-821">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-822">msRTCSIP-TrustedWebComponentsServerData</span><span class="sxs-lookup"><span data-stu-id="85b40-822">msRTCSIP-TrustedWebComponentsServerData</span></span></p></td>
<td><p><span data-ttu-id="85b40-823">Cet attribut est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85b40-823">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="85b40-824">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-824">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-825">msRTCSIP-TrustedWebComponentsServerFQDN</span><span class="sxs-lookup"><span data-stu-id="85b40-825">msRTCSIP-TrustedWebComponentsServerFQDN</span></span></p></td>
<td><p><span data-ttu-id="85b40-826">Cet attribut est une valeur de chaîne qui contient le nom de domaine complet (FQDN) du serveur IIS exécutant les services Web de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="85b40-826">This attribute is a string value that contains the FQDN of the IIS running Lync Server Web Services.</span></span> <span data-ttu-id="85b40-827">Il s’agit d’un attribut à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="85b40-827">This is a single-valued attribute.</span></span> <span data-ttu-id="85b40-828">La valeur valide de chaque segment est de 63 caractères. la valeur valide pour le nom de domaine complet est de 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="85b40-828">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="85b40-829">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-829">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-830">msRTCSIP-UCFlags (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-830">msRTCSIP-UCFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-831">Cet attribut définit différentes options de communications unifiées qui sont activées globalement pour tous les objets utilisateur ou contact.</span><span class="sxs-lookup"><span data-stu-id="85b40-831">This attribute defines different UC options that are enabled globally to all user or contact objects.</span></span> <span data-ttu-id="85b40-832">Cet attribut est une valeur de masque de bits de type entier.</span><span class="sxs-lookup"><span data-stu-id="85b40-832">This attribute is a bit-mask value of integer type.</span></span> <span data-ttu-id="85b40-833">Chaque option est représentée par la présence d’un bit.</span><span class="sxs-lookup"><span data-stu-id="85b40-833">Each option is represented by the presence of a bit.</span></span></p>
<p><span data-ttu-id="85b40-834">La valeur valide possible (et la position de bit associée) sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="85b40-834">The possible valid value (and associated bit position) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-835">4 : UsePerUserUCPolicy (position binaire 2)</span><span class="sxs-lookup"><span data-stu-id="85b40-835">4: UsePerUserUCPolicy (bit position 2)</span></span></p></li>
</ul>
<p><span data-ttu-id="85b40-836">Lorsque ce bit est défini, la stratégie de Cu est définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-836">When this bit is set, the UC policy is defined per user.</span></span></p></td>
<td><p><span data-ttu-id="85b40-837">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-837">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-838">msRTCSIP-UCPolicy (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-838">msRTCSIP-UCPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-839">Cet attribut à valeur unique contient le nom unique (DN) de la stratégie de Cu attribuée par l’administrateur pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-839">This single-valued attribute contains the distinguished name (DN) of the UC policy that the administrator has assigned for this user.</span></span></p></td>
<td><p><span data-ttu-id="85b40-840">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-840">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-841">msRTCSIP-UserDomainList (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-841">msRTCSIP-UserDomainList (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="85b40-842">Cet attribut fournit une liste de tous les domaines d’une forêt qui hébergent des utilisateurs compatibles SIP.</span><span class="sxs-lookup"><span data-stu-id="85b40-842">This attribute provides a list of all the domains in a forest that host SIP-enabled users.</span></span> <span data-ttu-id="85b40-843">La valeur par défaut est une liste vide, ce qui signifie que tous les domaines de la forêt sont compatibles SIP.</span><span class="sxs-lookup"><span data-stu-id="85b40-843">The default is an empty list, indicating that all domains in the forest are SIP-enabled.</span></span></p>
<p><span data-ttu-id="85b40-844">Les valeurs valides sont des chaînes multiples qui représentent le nom de domaine de chaque domaine.</span><span class="sxs-lookup"><span data-stu-id="85b40-844">Valid values are multiple strings representing the domain names of individual domains.</span></span></p></td>
<td><p><span data-ttu-id="85b40-845">Nouveautés de Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-845">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="85b40-846">Obsolète dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-846">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-847">msRTCSIP-UserEnabled</span><span class="sxs-lookup"><span data-stu-id="85b40-847">msRTCSIP-UserEnabled</span></span></p></td>
<td><p><span data-ttu-id="85b40-848">Cet attribut détermine si l’utilisateur est actuellement activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="85b40-848">This attribute determines whether the user is currently enabled for Lync Server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-849">msRTCSIP-UserExtension</span><span class="sxs-lookup"><span data-stu-id="85b40-849">msRTCSIP-UserExtension</span></span></p></td>
<td><p><span data-ttu-id="85b40-850">Cet attribut à valeurs multiples contient une liste de paires nom-valeur au format de &quot; nom = valeur. &quot; Cet attribut est marqué pour la réplication de catalogue global.</span><span class="sxs-lookup"><span data-stu-id="85b40-850">This multi-valued attribute contains a list of name-value pairs in the format of &quot;name=value.&quot; This attribute is marked for global catalog replication.</span></span></p></td>
<td><p><span data-ttu-id="85b40-851">Nouveautés de Live Communications Server 2005 avec SP1.</span><span class="sxs-lookup"><span data-stu-id="85b40-851">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-852">msRTCSIP-UserLocationProfile</span><span class="sxs-lookup"><span data-stu-id="85b40-852">msRTCSIP-UserLocationProfile</span></span></p></td>
<td><p><span data-ttu-id="85b40-853">Cet attribut contient le nom unique (DN) qui pointe vers un objet de profil d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="85b40-853">This attribute contains the distinguished name (DN) that points to a location profile object.</span></span></p></td>
<td><p><span data-ttu-id="85b40-854">Nouveauté d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="85b40-854">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-855">msRTCSIP-UserPolicies</span><span class="sxs-lookup"><span data-stu-id="85b40-855">msRTCSIP-UserPolicies</span></span></p></td>
<td><p><span data-ttu-id="85b40-856">Cet attribut stocke les paires nom-valeur pour les stratégies utilisateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-856">This attribute stores name-value pairs for user policies.</span></span></p></td>
<td><p><span data-ttu-id="85b40-857">Nouveautés de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="85b40-857">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-858">msRTCSIP-UserPolicy</span><span class="sxs-lookup"><span data-stu-id="85b40-858">msRTCSIP-UserPolicy</span></span></p></td>
<td><p><span data-ttu-id="85b40-859">Il s’agit d’un attribut à valeurs multiples contenant une liste de noms uniques avec des valeurs binaires (DN_WITH_BINARY) pointant vers des stratégies utilisateur globales de différents types.</span><span class="sxs-lookup"><span data-stu-id="85b40-859">This is a multi-valued attribute containing a list of distinguished names with binary (DN_WITH_BINARY) pointing to global user policies of different types.</span></span> <span data-ttu-id="85b40-860">La partie binaire indique le type de stratégie auquel la partie du DN pointe.</span><span class="sxs-lookup"><span data-stu-id="85b40-860">The binary part indicates the type of policy to which the DN portion points.</span></span></p>
<p><span data-ttu-id="85b40-861">Les valeurs binaires valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="85b40-861">The valid binary values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-862">0x00000001 : stratégie de réunion</span><span class="sxs-lookup"><span data-stu-id="85b40-862">0x00000001: Meeting policy</span></span></p></li>
<li><p><span data-ttu-id="85b40-863">0x00000002 : stratégie d’UC</span><span class="sxs-lookup"><span data-stu-id="85b40-863">0x00000002: UC policy</span></span></p></li>
<li><p><span data-ttu-id="85b40-864">0x00000005 : politique de présence</span><span class="sxs-lookup"><span data-stu-id="85b40-864">0x00000005: Presence policy</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="85b40-865">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-865">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-866">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="85b40-866">msRTCSIP-UserRoutingGroupId</span></span></p></td>
<td><p><span data-ttu-id="85b40-867">Il s’agit de l’ID du groupe de routage SIP.</span><span class="sxs-lookup"><span data-stu-id="85b40-867">This is the SIP routing group ID.</span></span> <span data-ttu-id="85b40-868">Les utilisateurs du même groupe seront enregistrés sur le même serveur principal.</span><span class="sxs-lookup"><span data-stu-id="85b40-868">Users in the same group will register to the same Front End Server.</span></span></p></td>
<td><p><span data-ttu-id="85b40-869">Nouveautés de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="85b40-869">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-870">msRTCSIP-WebComponentsData</span><span class="sxs-lookup"><span data-stu-id="85b40-870">msRTCSIP-WebComponentsData</span></span></p></td>
<td><p><span data-ttu-id="85b40-871">Il s’agit d’un attribut à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="85b40-871">This is a multi-valued attribute.</span></span> <span data-ttu-id="85b40-872">Cet attribut est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85b40-872">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="85b40-873">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-873">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-874">msRTCSIP-WebComponentsPoolAddress</span><span class="sxs-lookup"><span data-stu-id="85b40-874">msRTCSIP-WebComponentsPoolAddress</span></span></p></td>
<td><p><span data-ttu-id="85b40-875">Cet attribut à valeur unique pointe vers le pool ou le serveur Standard Edition auquel appartiennent les composants Web.</span><span class="sxs-lookup"><span data-stu-id="85b40-875">This single-valued attribute points to the pool or Standard Edition server to which the web components belong.</span></span></p>
<p><span data-ttu-id="85b40-876">Lien suivant : <strong>ID de lien 11028</strong></span><span class="sxs-lookup"><span data-stu-id="85b40-876">Forward link: <strong>Link ID 11028</strong></span></span></p>
<p><span data-ttu-id="85b40-877">Le lien précédent correspondant à cet attribut de lien suivant est <strong>msRTCSIP-WebComponentsServers</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-877">The corresponding back link to this forward link attribute is <strong>msRTCSIP-WebComponentsServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-878">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-878">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-879">msRTCSIP-WebComponentsServers</span><span class="sxs-lookup"><span data-stu-id="85b40-879">msRTCSIP-WebComponentsServers</span></span></p></td>
<td><p><span data-ttu-id="85b40-880">Cet attribut est une liste à plusieurs valeurs de noms uniques.</span><span class="sxs-lookup"><span data-stu-id="85b40-880">This attribute is a multi-valued list of distinguished names.</span></span> <span data-ttu-id="85b40-881">Cet attribut contient la liste de tous les serveurs Web associés à ce pool.</span><span class="sxs-lookup"><span data-stu-id="85b40-881">This attribute contains a list of all Web servers associated with this pool.</span></span></p>
<p><span data-ttu-id="85b40-882">Lien précédent : <strong>ID de lien 11029</strong></span><span class="sxs-lookup"><span data-stu-id="85b40-882">Back link: <strong>Link ID 11029</strong></span></span></p>
<p><span data-ttu-id="85b40-883">Le lien transférer correspondant à ce lien précédent est <strong>msRTCSIP-WebComponentsPoolAddress</strong>.</span><span class="sxs-lookup"><span data-stu-id="85b40-883">The corresponding forward link to this back link is <strong>msRTCSIP-WebComponentsPoolAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="85b40-884">Nouveautés d’Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="85b40-884">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-885">msRTCSIP-WMIInstanceId (obsolète)</span><span class="sxs-lookup"><span data-stu-id="85b40-885">msRTCSIP-WMIInstanceId (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="85b40-886">Nouveautés de Live Communications Server 2003.</span><span class="sxs-lookup"><span data-stu-id="85b40-886">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="85b40-887">Obsolète dans Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="85b40-887">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-888">OtherIPPhone</span><span class="sxs-lookup"><span data-stu-id="85b40-888">OtherIPPhone</span></span></p></td>
<td><p><span data-ttu-id="85b40-889">Cet attribut Active Directory existant est utilisé par la téléphonie pour spécifier la liste d’adresses IP supplémentaires pour un téléphone.</span><span class="sxs-lookup"><span data-stu-id="85b40-889">This existing Active Directory attribute is used by telephony to specify the list of alternate TCP/IP addresses for a phone.</span></span></p></td>
<td><p><span data-ttu-id="85b40-890">Nouveauté du système d’exploitation Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="85b40-890">New in Windows Server 2008 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-891">PhoneOfficeOther</span><span class="sxs-lookup"><span data-stu-id="85b40-891">PhoneOfficeOther</span></span></p></td>
<td><p><span data-ttu-id="85b40-892">Cet attribut Active Directory existant est utilisé par les composants vocaux de Lync Server, uniquement pour les objets contact, dans le but de router les appels vers les numéros d’accès d’abonné et de standard de messagerie unifiée.</span><span class="sxs-lookup"><span data-stu-id="85b40-892">This existing Active Directory attribute is used by the voice components in Lync Server, for contact objects only, for the purpose of routing calls to the unified messaging auto-attendant and subscriber access numbers.</span></span> <span data-ttu-id="85b40-893">L’adresse de transfert d’appel sans condition est stockée dans cet attribut à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="85b40-893">The unconditional call forwarding address is stored in this multi-valued attribute.</span></span> <span data-ttu-id="85b40-894">Ce compte est créé pour l’objet spécifique du standard automatique et de l’accès abonné.</span><span class="sxs-lookup"><span data-stu-id="85b40-894">This account is created for the specific purpose of auto-attendant and subscriber access.</span></span> <span data-ttu-id="85b40-895">Les attributs de ce compte ne doivent pas être modifiés par les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="85b40-895">This account’s attributes should not be modified by administrators.</span></span></p></td>
<td><p><span data-ttu-id="85b40-896">Nouveauté du système d’exploitation Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="85b40-896">New in Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b40-897">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="85b40-897">ProxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="85b40-898">Cet attribut multivaleur Active Directory existant fait partie du schéma Active Directory de base introduit dans Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="85b40-898">This existing Active Directory multi-valued attribute is part of the base Active Directory schema introduced in Windows 2000.</span></span> <span data-ttu-id="85b40-899">Cet attribut contient les différentes adresses x400, X500 et SMTP de l’adresse de messagerie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-899">This attribute contains the various X400, X500, and SMTP addresses of the user’s email.</span></span> <span data-ttu-id="85b40-900">Dans Live Communications Server 2003 et versions ultérieures, l’URI SIP de l’utilisateur est ajouté à cette liste à l’aide de la &quot; &quot; balise SIP :.</span><span class="sxs-lookup"><span data-stu-id="85b40-900">In Live Communications Server 2003 and later, the user’s SIP URI is added to this list, using the &quot;sip:&quot; tag.</span></span></p>
<p><span data-ttu-id="85b40-901">Les applications suivantes recherchent l’URI SIP de l’utilisateur à partir de cet attribut :</span><span class="sxs-lookup"><span data-stu-id="85b40-901">The following applications search the user’s SIP URI from this attribute:</span></span></p>
<ul>
<li><p><span data-ttu-id="85b40-902">Client de messagerie et de collaboration de Microsoft Office Outlook 2003</span><span class="sxs-lookup"><span data-stu-id="85b40-902">Microsoft Office Outlook 2003 messaging and collaboration client</span></span></p></li>
<li><p><span data-ttu-id="85b40-903">Microsoft Office SharePoint Server 2007</span><span class="sxs-lookup"><span data-stu-id="85b40-903">Microsoft Office SharePoint Server 2007</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="85b40-904">Nouveauté du système d’exploitation Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="85b40-904">New in Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b40-905">TelephoneNumber</span><span class="sxs-lookup"><span data-stu-id="85b40-905">TelephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="85b40-906">Cet attribut Active Directory existant contient le numéro de téléphone de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="85b40-906">This existing Active Directory attribute contains the telephone number for the user.</span></span></p></td>
<td><p><span data-ttu-id="85b40-907">Nouveauté du système d’exploitation Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="85b40-907">New in Windows 2000 operating system.</span></span></p></td>
</tr><span data-ttu-id="85b40-908">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85b40-908">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

