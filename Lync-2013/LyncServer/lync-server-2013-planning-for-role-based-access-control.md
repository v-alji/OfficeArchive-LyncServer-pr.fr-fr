---
title: 'Lync Server 2013 : Planification du contrôle d’accès basé sur un rôle'
description: 'Lync Server 2013 : planification du contrôle d’accès basé sur un rôle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for role-based access control (RBAC)
ms:assetid: 41204ba3-ce5b-41a8-a6c3-b444468fa328
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425917(v=OCS.15)
ms:contentKeyID: 48183962
ms.date: 01/28/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 971b3353694a1cdd53d88452717e6a9a360c6870
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395316"
---
# <a name="planning-for-role-based-access-control-in-lync-server-2013"></a><span data-ttu-id="e8d0f-103">Planification du contrôle d’accès basé sur un rôle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e8d0f-103">Planning for role-based access control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e8d0f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e8d0f-104">

<span> </span></span></span>

<span data-ttu-id="e8d0f-105">_**Dernière modification de la rubrique :** 2015-01-27_</span><span class="sxs-lookup"><span data-stu-id="e8d0f-105">_**Topic Last Modified:** 2015-01-27_</span></span>

<span data-ttu-id="e8d0f-106">Pour vous permettre de déléguer des tâches administratives tout en préservant la sécurité, Lync Server 2013 offre le contrôle d’accès basé sur les rôles (RBAC).</span><span class="sxs-lookup"><span data-stu-id="e8d0f-106">To enable you to delegate administrative tasks while maintaining high standards for security, Lync Server 2013 offers role-based access control (RBAC).</span></span> <span data-ttu-id="e8d0f-107">Avec le RBAC, le privilège administratif est accordé en attribuant aux utilisateurs des rôles d’administration.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-107">With RBAC, administrative privilege is granted by assigning users to administrative roles.</span></span> <span data-ttu-id="e8d0f-108">Lync Server 2013 inclut un ensemble étendu de rôles d’administrateur intégrés, et vous permet également de créer de nouveaux rôles et de spécifier une liste personnalisée d’applets de construction pour chaque nouveau rôle.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-108">Lync Server 2013 includes a rich set of built-in administrative roles, and also enables you to create new roles and specify a custom list of cmdlets for each new role.</span></span> <span data-ttu-id="e8d0f-109">Vous pouvez également ajouter des scripts d’applets de commande aux tâches autorisées des rôles RBAC prédéfinis et personnalisés.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-109">You can also add scripts of cmdlets to the allowed tasks of both predefined and custom RBAC roles.</span></span>

<div>

## <a name="better-server-security-and-centralization"></a><span data-ttu-id="e8d0f-110">Meilleure sécurité serveur et centralisation</span><span class="sxs-lookup"><span data-stu-id="e8d0f-110">Better Server Security and Centralization</span></span>

<span data-ttu-id="e8d0f-111">Le RBAC, l’accès et l’autorisation sont basés précisément sur le rôle de serveur Lync de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-111">With RBAC, access and authorization is based precisely on a user’s Lync Server role.</span></span> <span data-ttu-id="e8d0f-112">Cela permet de recourir à la sécurité de « privilèges minimum », en accordant aux administrateurs et aux utilisateurs uniquement les droits nécessaires à leur travail.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-112">This enables use of the security practice of "least privilege," granting administrators and users only the rights that are necessary for their job.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="e8d0f-113">Les restrictions RBAC fonctionnent uniquement pour les administrateurs travaillant à distance à l’aide du panneau de configuration de Lync Server ou de Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-113">RBAC restrictions work only on administrators working remotely, using either the Lync Server Control Panel or Lync Server Management Shell.</span></span> <span data-ttu-id="e8d0f-114">Un utilisateur assis sur un serveur exécutant Lync Server n’est pas limité par le RBAC.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-114">A user sitting at a server running Lync Server is not restricted by RBAC.</span></span> <span data-ttu-id="e8d0f-115">Par conséquent, la sécurité physique de votre serveur Lync est importante pour préserver les restrictions RBAC.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-115">Therefore, physical security of your Lync Server is important to preserve RBAC restrictions.</span></span>



</div>

</div>

<div>

## <a name="roles-and-scope"></a><span data-ttu-id="e8d0f-116">Rôles et étendue</span><span class="sxs-lookup"><span data-stu-id="e8d0f-116">Roles and Scope</span></span>

<span data-ttu-id="e8d0f-117">Dans le RBAC, un *rôle* est activé pour utiliser une liste de cmdlets, conçue pour être utile à un certain type d’administrateur ou de technicien.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-117">In RBAC, a *role* is enabled to use a list of cmdlets, designed to be useful for a certain type of administrator or technician.</span></span> <span data-ttu-id="e8d0f-118">Une *étendue* est le jeu d’objets sur lequel les applets de action définis dans un rôle peuvent opérer.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-118">A *scope* is the set of objects which the cmdlets defined in a role can operate on.</span></span> <span data-ttu-id="e8d0f-119">Les objets concernés par une étendue peuvent être des comptes d’utilisateurs (regroupés par unité d’organisation) ou des serveurs (regroupés par site).</span><span class="sxs-lookup"><span data-stu-id="e8d0f-119">The objects that scope affects can be either user accounts (grouped by organizational unit) or servers (grouped by site).</span></span>

<span data-ttu-id="e8d0f-120">Le tableau suivant répertorie les rôles prédéfinis dans Lync Server et offre une vue d’ensemble des types de tâches que vous pouvez effectuer.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-120">The following table lists the predefined roles in Lync Server, and gives a general overview of the types of tasks each can do.</span></span> <span data-ttu-id="e8d0f-121">La quatrième colonne indique le rôle Microsoft Exchange Server similaire pour chaque rôle serveur Lync, s’il en existe une.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-121">The fourth column shows the similar Microsoft Exchange Server role for each Lync Server role, if there is one.</span></span>

### <a name="predefined-administrative-roles"></a><span data-ttu-id="e8d0f-122">Rôles d’administration prédéfinis</span><span class="sxs-lookup"><span data-stu-id="e8d0f-122">Predefined Administrative Roles</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8d0f-123">Rôle</span><span class="sxs-lookup"><span data-stu-id="e8d0f-123">Role</span></span></th>
<th><span data-ttu-id="e8d0f-124">Tâches autorisées</span><span class="sxs-lookup"><span data-stu-id="e8d0f-124">Tasks allowed</span></span></th>
<th><span data-ttu-id="e8d0f-125">Groupe Active Directory sous-jacent</span><span class="sxs-lookup"><span data-stu-id="e8d0f-125">Underlying Active Directory group</span></span></th>
<th><span data-ttu-id="e8d0f-126">Équivalent Exchange</span><span class="sxs-lookup"><span data-stu-id="e8d0f-126">Exchange equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8d0f-127">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-127">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-128">Peut effectuer toutes les tâches administratives et modifier tous les paramètres, y compris la création de rôles et l’attribution d’utilisateurs aux rôles.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-128">Can perform all administrative tasks and modify all settings, including creating roles and assigning users to roles.</span></span> <span data-ttu-id="e8d0f-129">Peut développer un déploiement en ajoutant de nouveaux sites, groupes et services.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-129">Can expand a deployment by adding new sites, pools, and services.</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-130">CSAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-130">CSAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-131">Gestion de l’Organisation</span><span class="sxs-lookup"><span data-stu-id="e8d0f-131">Organization Management</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8d0f-132">CsUserAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-132">CsUserAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-133">Possibilité d’activer et de désactiver des utilisateurs pour Lync Server, de déplacer des utilisateurs et d’affecter des stratégies existantes aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-133">Can enable and disable users for Lync Server, move users and assign existing policies to users.</span></span> <span data-ttu-id="e8d0f-134">Impossible de modifier les stratégies.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-134">Cannot modify policies.</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-135">CSUserAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-135">CSUserAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-136">Destinataires du courrier</span><span class="sxs-lookup"><span data-stu-id="e8d0f-136">Mail Recipients</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8d0f-137">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-137">CsVoiceAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-138">Peut créer, configurer et gérer les paramètres et les stratégies relatives à la voix.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-138">Can create, configure, and manage voice-related settings and policies.</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-139">CSVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-139">CSVoiceAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-140">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e8d0f-140">Not applicable</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8d0f-141">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-141">CsServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-142">Peut gérer, surveiller et résoudre les problèmes liés aux serveurs et services.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-142">Can manage, monitor, and troubleshoot servers and services.</span></span> <span data-ttu-id="e8d0f-143">Peut empêcher de nouvelles connexions aux serveurs, d’arrêter et de démarrer des services et d’appliquer des mises à jour logicielles.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-143">Can prevent new connections to servers, stop and start services, and apply software updates.</span></span> <span data-ttu-id="e8d0f-144">Ne peut pas apporter de modifications avec un impact sur la configuration globale.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-144">Cannot make changes with global configuration impact.</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-145">CSServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-145">CSServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-146">Gestion du serveur</span><span class="sxs-lookup"><span data-stu-id="e8d0f-146">Server Management</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8d0f-147">CsViewOnlyAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-147">CsViewOnlyAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-148">Peut afficher le déploiement, y compris des informations sur l’utilisateur et le serveur, afin d’analyser l’intégrité du déploiement.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-148">Can view the deployment, including user and server information, in order to monitor deployment health.</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-149">CSViewOnlyAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-149">CSViewOnlyAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-150">Gestion de l’organisation View-Only</span><span class="sxs-lookup"><span data-stu-id="e8d0f-150">View-Only Organization Management</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8d0f-151">CsHelpDesk</span><span class="sxs-lookup"><span data-stu-id="e8d0f-151">CsHelpDesk</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-152">Peut afficher le déploiement, y compris les propriétés et les stratégies de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-152">Can view the deployment, including user's properties and policies.</span></span> <span data-ttu-id="e8d0f-153">Peut exécuter des tâches de résolution des problèmes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-153">Can run specific troubleshooting tasks.</span></span> <span data-ttu-id="e8d0f-154">Impossible de modifier les propriétés de l’utilisateur ou les stratégies, la configuration du serveur ou les services.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-154">Cannot change user properties or policies, server configuration, or services.</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-155">CSHelpDesk</span><span class="sxs-lookup"><span data-stu-id="e8d0f-155">CSHelpDesk</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-156">Support technique</span><span class="sxs-lookup"><span data-stu-id="e8d0f-156">HelpDesk</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8d0f-157">CsArchivingAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-157">CsArchivingAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-158">Peut modifier la configuration et les stratégies d’archivage.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-158">Can modify archiving configuration and policies.</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-159">CSArchivingAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-159">CSArchivingAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-160">Gestion de la rétention, conservation légale</span><span class="sxs-lookup"><span data-stu-id="e8d0f-160">Retention Management, Legal Hold</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8d0f-161">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-161">CsResponseGroupAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-162">Peut gérer la configuration de l’application Response Group dans un site.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-162">Can manage the configuration of the Response Group application within a site.</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-163">CSResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-163">CSResponseGroupAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-164">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e8d0f-164">Not applicable</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8d0f-165">CsLocationAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-165">CsLocationAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-166">Niveau de droits le plus faible pour une gestion améliorée de 9-1-1 (E9-1-1), y compris la création d’emplacements E9-1-1</span><span class="sxs-lookup"><span data-stu-id="e8d0f-166">Lowest level of rights for Enhanced 9-1-1 (E9-1-1) management, including creating E9-1-1 locations and network identifiers, and associating these with each other.</span></span> <span data-ttu-id="e8d0f-167">Ce rôle est toujours affecté avec une étendue globale.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-167">This role is always assigned with a global scope.</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-168">CSLocationAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-168">CSLocationAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-169">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e8d0f-169">Not applicable</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8d0f-170">CsResponseGroupManager</span><span class="sxs-lookup"><span data-stu-id="e8d0f-170">CsResponseGroupManager</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-171">Peut gérer des groupes de réponse spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-171">Can manage specific response groups.</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-172">CSResponseGroupManager</span><span class="sxs-lookup"><span data-stu-id="e8d0f-172">CSResponseGroupManager</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-173">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e8d0f-173">Not applicable</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8d0f-174">CsPersistentChatAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-174">CsPersistentChatAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-175">Peut gérer la fonctionnalité de conversation permanente et des salles de conversation permanentes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-175">Can manage the Persistent Chat feature and specific Persistent Chat rooms.</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-176">CSPersistentChatAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8d0f-176">CSPersistentChatAdministrator</span></span></p></td>
<td><p><span data-ttu-id="e8d0f-177">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e8d0f-177">Not applicable</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e8d0f-178">Tous les rôles prédéfinis fournis dans Lync Server ont une étendue globale.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-178">All predefined roles shipped in Lync Server have a global scope.</span></span> <span data-ttu-id="e8d0f-179">Pour suivre les pratiques de gestion des privilèges minimum, vous ne devez pas affecter des utilisateurs aux rôles avec l’étendue globale s’ils ne peuvent gérer qu’un ensemble limité de serveurs ou d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-179">To follow least privilege practices, you should not assign users to roles with global scope if they are going to administer only a limited set of servers or users.</span></span> <span data-ttu-id="e8d0f-180">Pour ce faire, vous pouvez créer des rôles basés sur un rôle existant, mais avec une étendue plus limitée.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-180">To accomplish this, you can create roles which are based on an existing role, but with a more limited scope.</span></span>

<div>

## <a name="creating-a-scoped-role"></a><span data-ttu-id="e8d0f-181">Création d’un rôle à l’étendue</span><span class="sxs-lookup"><span data-stu-id="e8d0f-181">Creating a Scoped Role</span></span>

<span data-ttu-id="e8d0f-182">Lorsque vous créez un rôle avec une étendue limitée (un rôle étendu), vous spécifiez l’étendue, ainsi que le rôle existant sur lequel elle est basée, et le groupe Active Directory doit être affecté au rôle.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-182">When you create a role with limited scope (a scoped role), you specify the scope, along with the existing role it is based on and the Active Directory group to be assigned the role.</span></span> <span data-ttu-id="e8d0f-183">Le groupe Active Directory que vous spécifiez doit déjà être créé.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-183">The Active Directory group you specify must already be created.</span></span> <span data-ttu-id="e8d0f-184">L’applet de commande suivante est un exemple de création d’un rôle qui dispose des autorisations de l’un des rôles d’administration prédéfinis, mais avec une étendue limitée.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-184">The following cmdlet is an example of a creating a role which has the privileges of one of the pre-defined administrative roles, but with limited scope.</span></span> <span data-ttu-id="e8d0f-185">Il crée un nouveau rôle appelé `Site01 Server Administrators` .</span><span class="sxs-lookup"><span data-stu-id="e8d0f-185">It creates a new role called `Site01 Server Administrators`.</span></span> <span data-ttu-id="e8d0f-186">Le rôle est doté des capacités du rôle CsServerAdministrator prédéfini, mais uniquement pour les serveurs situés dans le site Site01.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-186">The role has the abilities of the predefined CsServerAdministrator role, but only for the servers located in the Site01 site.</span></span> <span data-ttu-id="e8d0f-187">Pour que cette applet de action fonctionne, le site Site01 doit déjà être défini et un groupe de sécurité universelle nommé `Site01 Server Administrators` doit déjà exister.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-187">For this cmdlet to work, the Site01 site must already be defined, and a universal security group named `Site01 Server Administrators` must already exist.</span></span>

    New-CsAdminRole -Identity "Site01 Server Administrators" -Template CsServerAdministrator -ConfigScopes "site:Site01"

<span data-ttu-id="e8d0f-188">Après l’exécution de cette cmdlet, tous les utilisateurs membres du `Site01 Server Administrators` groupe disposent de privilèges d’administrateur serveur pour les serveurs dans Site01.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-188">After this cmdlet runs, all users who are members of the `Site01 Server Administrators` group will have server administrator privileges for the servers in Site01.</span></span> <span data-ttu-id="e8d0f-189">De plus, tous les utilisateurs ajoutés par le biais de ce groupe de sécurité universelle disposent également des privilèges de ce rôle.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-189">Additionally, any users who are later added to this universal security group also gain the privileges of this role.</span></span> <span data-ttu-id="e8d0f-190">Notez que le rôle lui-même et le groupe de sécurité universel auquel il est affecté sont appelés `Site01 Server Administrators` .</span><span class="sxs-lookup"><span data-stu-id="e8d0f-190">Note that both the role itself, and the universal security group it is assigned to are called `Site01 Server Administrators`.</span></span>

<span data-ttu-id="e8d0f-191">Dans l’exemple suivant, la portée utilisateur est limitée au lieu de l’étendue du serveur.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-191">The following example limits user scope instead of server scope.</span></span> <span data-ttu-id="e8d0f-192">Il crée un `Sales Users Administrator` rôle pour gérer les comptes d’utilisateur dans l’unité d’organisation ventes.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-192">It creates a `Sales Users Administrator` role to administer the user accounts in the Sales organizational unit.</span></span> <span data-ttu-id="e8d0f-193">Le groupe de sécurité universelle SalesUsersAdministrator doit déjà être créé pour que cette applet de action fonctionne.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-193">The SalesUsersAdministrator universal security group must already be created for this cmdlet to work.</span></span>

    New-CsAdminRole -Identity "Sales Users Administrator " -Template CsUserAdministrator -UserScopes "OU:OU=Sales, OU=Lync Tenants, DC=Domain, DC=com"

</div>

<div>

## <a name="creating-a-new-role"></a><span data-ttu-id="e8d0f-194">Création d’un nouveau rôle</span><span class="sxs-lookup"><span data-stu-id="e8d0f-194">Creating a New Role</span></span>

<span data-ttu-id="e8d0f-195">Pour créer un rôle ayant accès à un ensemble d’applets de fonction qui ne figurent pas dans l’un des rôles prédéfinis, ou à un ensemble de scripts ou de modules, vous commencez par utiliser l’un des rôles prédéfinis en tant que modèle.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-195">To create a role that has access to a set of cmdlets not in one of the predefined roles, or to a set of scripts or modules, you again start by using one of the predefined roles as a template.</span></span> <span data-ttu-id="e8d0f-196">Notez que les scripts et les modules que vous pouvez exécuter doivent être stockés dans les emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="e8d0f-196">Note that scripts and modules that roles are to be able to run must be stored in the following locations:</span></span>

  - <span data-ttu-id="e8d0f-197">Le chemin d’accès au module Lync, qui est par défaut C : \\ Program Files fichiers \\ communs \\ Microsoft Lync Server 2013 \\ modules \\ Lync</span><span class="sxs-lookup"><span data-stu-id="e8d0f-197">The Lync module path, which is by default C:\\Program Files\\Common Files\\Microsoft Lync Server 2013\\Modules\\Lync</span></span>

  - <span data-ttu-id="e8d0f-198">Le chemin d’accès du script utilisateur, qui est par défaut C : \\ fichiers programme fichiers \\ communs \\ Microsoft Lync Server 2013 \\ Adminscripts</span><span class="sxs-lookup"><span data-stu-id="e8d0f-198">The user script path, which is by default C:\\Program Files\\Common Files\\Microsoft Lync Server 2013\\AdminScripts</span></span>

<span data-ttu-id="e8d0f-199">Pour créer un nouveau rôle, vous devez utiliser l’applet **de nouvelle applet de nouveau-CsAdminRole** .</span><span class="sxs-lookup"><span data-stu-id="e8d0f-199">To make a new role, you use the **New-CsAdminRole** cmdlet.</span></span> <span data-ttu-id="e8d0f-200">Avant d’exécuter **New-CsAdminRole**, vous devez commencer par créer le groupe de sécurité universelle sous-jacent qui sera associé à ce rôle.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-200">Before running **New-CsAdminRole**, you must first create the underlying universal security group that will be associated with this role.</span></span>

<span data-ttu-id="e8d0f-201">Les applets de commande suivantes constituent un exemple de création d’un nouveau rôle.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-201">The following cmdlets serve as an example of a creating a new role.</span></span> <span data-ttu-id="e8d0f-202">Ils créent un nouveau type de rôle appelé `MyHelpDeskScriptRole` .</span><span class="sxs-lookup"><span data-stu-id="e8d0f-202">They create a new role type called `MyHelpDeskScriptRole`.</span></span> <span data-ttu-id="e8d0f-203">Le nouveau rôle est doté des capacités du rôle CsHelpDesk prédéfini et peut également exécuter les fonctions dans un script appelé « TestScript ».</span><span class="sxs-lookup"><span data-stu-id="e8d0f-203">The new role has the abilities of the predefined CsHelpDesk role, and can additionally run the functions in a script named “testscript”.</span></span>

    New-CsAdminRole -Identity "MyHelpDeskScriptRole" -Template CsHelpDesk -ScriptModules @{Add="testScript.ps1"}

<span data-ttu-id="e8d0f-204">Pour que cette applet de action fonctionne, vous devez commencer par créer le groupe de sécurité MyHelpDeskScriptRole.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-204">For this cmdlet to work, you must have first created the universal security group MyHelpDeskScriptRole.</span></span>

<span data-ttu-id="e8d0f-205">Après l’exécution de cette cmdlet, vous pouvez attribuer des utilisateurs directement à ce rôle (auquel cas il s’agit d’une étendue globale), ou créer un rôle d’étendue en fonction de ce rôle, comme décrit dans la rubrique Création d’un rôle d’étendue, précédemment dans ce document.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-205">After this cmdlet runs, you can assign users directly to this role (in which case they have global scope), or create a scoped role based on this role, as explained in Creating a Scoped Role, previously in this document.</span></span>

</div>

<div>

## <a name="assigning-roles-to-users"></a><span data-ttu-id="e8d0f-206">Attribution de rôles aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e8d0f-206">Assigning Roles to Users</span></span>

<span data-ttu-id="e8d0f-207">Chaque rôle serveur Lync est associé à un groupe de sécurité universelle Active Directory sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-207">Each Lync Server role is associated with an underlying Active Directory universal security group.</span></span> <span data-ttu-id="e8d0f-208">Tout utilisateur que vous ajoutez au groupe sous-jacent obtient les compétences de ce rôle.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-208">Any users who you add to the underlying group gain the abilities of that role.</span></span>

<span data-ttu-id="e8d0f-209">Les exemples figurant dans les sections précédentes ont créé un nouveau rôle et ont attribué un groupe de sécurité universelle existant au nouveau rôle.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-209">The examples in the preceding sections both created a new role and assigned an existing universal security group to the new role.</span></span> <span data-ttu-id="e8d0f-210">Pour attribuer un rôle existant à un ou plusieurs utilisateurs, ajoutez ces utilisateurs au groupe associé au rôle.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-210">To assign an existing role to one or more users, add those users to the group associated with the role.</span></span> <span data-ttu-id="e8d0f-211">Vous pouvez ajouter des utilisateurs individuels et des groupes de sécurité universelle à ces groupes.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-211">You can add both individual users and universal security groups to these groups.</span></span>

<span data-ttu-id="e8d0f-212">Par exemple, le rôle **CsAdministrator** est automatiquement accordé au groupe de sécurité universelle **administrateurs CS** dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-212">For example, the **CsAdministrator** role is automatically granted to the **CS Administrators** universal security group in Active Directory.</span></span> <span data-ttu-id="e8d0f-213">Ce groupe de sécurité universel est créé dans Active Directory lorsque vous déployez Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-213">This universal security group is created in Active Directory when you deploy Lync Server.</span></span> <span data-ttu-id="e8d0f-214">Pour accorder ce privilège à un utilisateur ou à un groupe, vous pouvez simplement l’ajouter au groupe **administrateurs CS** .</span><span class="sxs-lookup"><span data-stu-id="e8d0f-214">To grant a user or group this privilege, you can simply add them to the **CS Administrators** group.</span></span>

<span data-ttu-id="e8d0f-215">Plusieurs rôles RBAC peuvent être attribués à un utilisateur en étant ajoutés aux groupes Active Directory sous-jacents correspondant à chaque rôle.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-215">A user can be given multiple RBAC roles by being added to the underlying Active Directory groups that correspond to each role.</span></span>

<span data-ttu-id="e8d0f-216">Notez que lorsque vous créez un rôle, les utilisateurs qui ont été ajoutés par la suite au groupe Active Directory sous-jacent tirent parti des capacités de ce rôle.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-216">Note that when you create a role, users who are later added to the underlying Active Directory group gain the abilities of that role.</span></span>

</div>

<div>

## <a name="modifying-the-abilities-of-a-role"></a><span data-ttu-id="e8d0f-217">Modification des capacités d’un rôle</span><span class="sxs-lookup"><span data-stu-id="e8d0f-217">Modifying the Abilities of a Role</span></span>

<span data-ttu-id="e8d0f-218">Vous pouvez modifier la liste des cmdlets et des scripts qu’un rôle peut exécuter.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-218">You can modify the list of cmdlets and scripts that a role can run.</span></span> <span data-ttu-id="e8d0f-219">Vous pouvez modifier les applets de souscription et les scripts que les rôles personnalisés peuvent exécuter, mais vous pouvez uniquement modifier les scripts pour les rôles prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-219">You can modify both the cmdlets and scripts that custom roles can run, but you can modify only the scripts for predefined roles.</span></span> <span data-ttu-id="e8d0f-220">Chaque cmdlet que vous entrez peut ajouter, supprimer ou remplacer des cmdlets ou des scripts.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-220">Each cmdlet you type can add, remove, or replace cmdlets or scripts.</span></span>

<span data-ttu-id="e8d0f-221">Pour modifier un rôle, utilisez l’applet **de cmdlet Set-CsAdminRole** .</span><span class="sxs-lookup"><span data-stu-id="e8d0f-221">To modify a role, use the **Set-CsAdminRole** cmdlet.</span></span> <span data-ttu-id="e8d0f-222">L’applet de commande suivante supprime un script du rôle.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-222">The following cmdlet removes one script from the role.</span></span>

    Set-CsAdminRole -Identity "MyHelpDeskScriptRole" -ScriptModules @{Remove="testScript.ps1"}

</div>

</div>

<div>

## <a name="planning-for-rbac"></a><span data-ttu-id="e8d0f-223">Planification de RBAC</span><span class="sxs-lookup"><span data-stu-id="e8d0f-223">Planning for RBAC</span></span>

<span data-ttu-id="e8d0f-224">Pour chaque personne qui doit être disposant de droits d’administration pour votre déploiement de Lync Server, envisagez les tâches que vous devez effectuer, puis affectez-les aux rôles possédant le moins de privilèges et d’étendue nécessaires pour leur travail.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-224">For each person who is to be given any kind of administrative rights for your Lync Server deployment, consider exactly which tasks they need to perform, then assign them to roles with the least privilege and scope necessary for their job.</span></span> <span data-ttu-id="e8d0f-225">Le cas échéant, vous pouvez utiliser l’applet de cmdlet **Set-CsAdminRole** pour créer un nouveau rôle uniquement pour les applets de applet nécessaires aux tâches de cette personne.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-225">If necessary, you can use the **Set-CsAdminRole** cmdlet to create a new role with only the cmdlets necessary for this person’s tasks.</span></span>

<span data-ttu-id="e8d0f-226">Les utilisateurs disposant du rôle CsAdministrator peuvent créer tous types de rôles, y compris des rôles basés sur CsAdministrator, et leur affecter des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-226">Users who have the CsAdministrator role can create all types of roles, including roles based on CsAdministrator, and assign users to them.</span></span> <span data-ttu-id="e8d0f-227">Il est recommandé d’affecter le rôle CsAdministrator à un très petit ensemble d’utilisateurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="e8d0f-227">The best practice is to assign the CsAdministrator role to a very small set of trusted users.</span></span>

<span data-ttu-id="e8d0f-228"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e8d0f-228"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

