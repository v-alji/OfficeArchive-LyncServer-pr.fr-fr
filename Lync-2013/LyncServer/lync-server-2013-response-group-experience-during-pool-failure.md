---
title: Expérience de Response Group en cas de défaillance d’un pool dans Lync Server 2013
description: Application de groupe de réponse Lync Server 2013 en cas d’échec du pool.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Response group experience during pool failure
ms:assetid: 4e00fb38-64b1-4fd9-903d-7639177bc303
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204886(v=OCS.15)
ms:contentKeyID: 48184116
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d8d5904bc6934d4c330202bafa66d6dd8a16ff5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436243"
---
# <a name="response-group-experience-in-lync-server-2013-during-pool-failure"></a><span data-ttu-id="639cb-103">Expérience de Response Group en cas de défaillance d’un pool dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="639cb-103">Response group experience in Lync Server 2013 during pool failure</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="639cb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="639cb-104">

<span> </span></span></span>

<span data-ttu-id="639cb-105">_**Dernière modification de la rubrique :** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="639cb-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="639cb-106">Cette section décrit en détail la façon dont l’activité du groupe de réponses est affectée aux étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="639cb-106">This section describes in detail how response group activity is affected in the following stages:</span></span>

  - <span data-ttu-id="639cb-107">Une panne se produit dans le pool principal, mais le basculement n’est pas encore lancé.</span><span class="sxs-lookup"><span data-stu-id="639cb-107">An outage occurs in the primary pool, but failover is not yet initiated.</span></span>

  - <span data-ttu-id="639cb-108">Le service est en échec sur le pool de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="639cb-108">Service is failed over to the backup pool.</span></span>

  - <span data-ttu-id="639cb-109">Le service n’a pas pu revenir au pool principal.</span><span class="sxs-lookup"><span data-stu-id="639cb-109">Service is failed back to the primary pool.</span></span>

<div>

## <a name="user-experience-when-outage-occurs"></a><span data-ttu-id="639cb-110">Utilisation de l’interface utilisateur en cas d’interruption</span><span class="sxs-lookup"><span data-stu-id="639cb-110">User Experience When Outage Occurs</span></span>

<span data-ttu-id="639cb-111">En cas d’interruption d’une réserve ou d’un site, mais que l’administrateur n’a pas encore lancé le basculement, l’activité du groupe de réponses est gérée comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="639cb-111">When a pool or site outage occurs, but the administrator has not yet initiated failover, response group activity is handled as described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="639cb-112">Lors de la récupération après incident, les appels se comportent différemment selon que les groupes de réponses de la liste principale ont été importés au pool de sauvegarde lors de la récupération.</span><span class="sxs-lookup"><span data-stu-id="639cb-112">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="639cb-113">Dans le tableau suivant, les références aux groupes de réponse importés impliquent que les groupes de réponse de pool principal aient été importés dans le pool de sauvegarde lors du mode de récupération d’urgence.</span><span class="sxs-lookup"><span data-stu-id="639cb-113">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="outage-occurs"></a><span data-ttu-id="639cb-114">Une panne survient</span><span class="sxs-lookup"><span data-stu-id="639cb-114">Outage Occurs</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="639cb-115">Type d’appel ou d’action de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="639cb-115">Type of call or user action</span></span></th>
<th><span data-ttu-id="639cb-116">Pendant la période d’interruption</span><span class="sxs-lookup"><span data-stu-id="639cb-116">During outage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="639cb-117">Appels connectés à un agent</span><span class="sxs-lookup"><span data-stu-id="639cb-117">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="639cb-118">Les appels ordinaires restent connectés.</span><span class="sxs-lookup"><span data-stu-id="639cb-118">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="639cb-119">Les appels anonymes sont déconnectés.</span><span class="sxs-lookup"><span data-stu-id="639cb-119">Anonymous calls are disconnected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="639cb-120">Appels en cours non encore connectés à un agent</span><span class="sxs-lookup"><span data-stu-id="639cb-120">In progress calls not yet connected to an agent</span></span></p></td>
<td><p><span data-ttu-id="639cb-121">Les appels sont déconnectés.</span><span class="sxs-lookup"><span data-stu-id="639cb-121">Calls are disconnected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="639cb-122">Nouveaux appels</span><span class="sxs-lookup"><span data-stu-id="639cb-122">New calls</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="639cb-123">Les appels sont déconnectés.</span><span class="sxs-lookup"><span data-stu-id="639cb-123">Calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="639cb-124">Si les groupes de réponse étaient importés, les appels se connectent à un pool de sauvegarde, mais les agents hébergés dans le pool principal sont injoignables.</span><span class="sxs-lookup"><span data-stu-id="639cb-124">If response groups were imported, calls connect to backup pool, but agents homed in primary pool are unreachable.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="639cb-125">Appels d’agent de la part de Response Group</span><span class="sxs-lookup"><span data-stu-id="639cb-125">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="639cb-126">Cette fonctionnalité est désactivée pendant cette étape.</span><span class="sxs-lookup"><span data-stu-id="639cb-126">Feature is disabled during this stage.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="639cb-127">Informations de connexion et d’agent</span><span class="sxs-lookup"><span data-stu-id="639cb-127">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="639cb-128">Les groupes d’agents appartenant au pool principal peuvent être affichés sur la console de l’agent, mais les agents ne peuvent pas se connecter.</span><span class="sxs-lookup"><span data-stu-id="639cb-128">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="639cb-129">Les groupes d’agents appartenant au pool de sauvegarde peuvent être affichés sur la console de l’agent et les agents peuvent se connecter.</span><span class="sxs-lookup"><span data-stu-id="639cb-129">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="639cb-130">Les groupes d’agent importés ne sont pas affichés dans la console de l’agent.</span><span class="sxs-lookup"><span data-stu-id="639cb-130">Imported agent groups are not displayed on agent console.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="639cb-131">Configuration de Response Group</span><span class="sxs-lookup"><span data-stu-id="639cb-131">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="639cb-132">Il est possible d’afficher les groupes de réponse appartenant au pool principal en fonction de la disponibilité de la base de données principale du pool principal, mais pas de les modifier.</span><span class="sxs-lookup"><span data-stu-id="639cb-132">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="639cb-133">Les groupes de réponse appartenant au pool de sauvegarde peuvent être affichés et modifiés.</span><span class="sxs-lookup"><span data-stu-id="639cb-133">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="639cb-134">Les groupes de réponse importés ne peuvent pas être affichés dans le panneau de configuration de Lync Server ou dans l’outil de configuration de groupe de réponse, mais ils peuvent être configurés en utilisant des applets de commande Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="639cb-134">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-experience-during-failover"></a><span data-ttu-id="639cb-135">Utilisation de l’interface utilisateur pendant le basculement</span><span class="sxs-lookup"><span data-stu-id="639cb-135">User Experience During Failover</span></span>

<span data-ttu-id="639cb-136">Lorsqu’un administrateur appelle le basculement vers un pool de sauvegarde, l’activité du groupe de réponses est gérée durant et après le basculement, comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="639cb-136">When an administrator invokes failover to a backup pool, response group activity is handled during and after the failover as described in the following table.</span></span> <span data-ttu-id="639cb-137">La première colonne décrit le type d’activité qui peut avoir lieu.</span><span class="sxs-lookup"><span data-stu-id="639cb-137">The first column describes the type of activity that might be taking place.</span></span> <span data-ttu-id="639cb-138">La colonne du milieu décrit la façon dont chaque activité est gérée au cours de la période de reprise du pool de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="639cb-138">The middle column describes how each activity is handled during the brief time that it takes to fail over to the backup pool.</span></span> <span data-ttu-id="639cb-139">La dernière colonne décrit le mode de gestion de l’activité pour la durée, une fois le processus de basculement terminé et le pool de sauvegarde en cours pour le pool principal.</span><span class="sxs-lookup"><span data-stu-id="639cb-139">The last column describes how the activity is handled for the duration, after the failover process is complete and the backup pool is standing in for the primary pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="639cb-140">Lors de la récupération après incident, les appels se comportent différemment selon que les groupes de réponses de la liste principale ont été importés au pool de sauvegarde lors de la récupération.</span><span class="sxs-lookup"><span data-stu-id="639cb-140">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="639cb-141">Dans le tableau suivant, les références aux groupes de réponse importés impliquent que les groupes de réponse de pool principal aient été importés dans le pool de sauvegarde lors du mode de récupération d’urgence.</span><span class="sxs-lookup"><span data-stu-id="639cb-141">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="failover-is-initiated"></a><span data-ttu-id="639cb-142">Le basculement est lancé</span><span class="sxs-lookup"><span data-stu-id="639cb-142">Failover Is Initiated</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="639cb-143">Type d’appel ou d’action de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="639cb-143">Type of call or user action</span></span></th>
<th><span data-ttu-id="639cb-144">Lors du basculement</span><span class="sxs-lookup"><span data-stu-id="639cb-144">During Failover</span></span></th>
<th><span data-ttu-id="639cb-145">Après le basculement</span><span class="sxs-lookup"><span data-stu-id="639cb-145">After Failover Completes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="639cb-146">Appels connectés à un agent</span><span class="sxs-lookup"><span data-stu-id="639cb-146">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="639cb-147">Les appels ordinaires restent connectés.</span><span class="sxs-lookup"><span data-stu-id="639cb-147">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="639cb-148">Les appels anonymes sont déconnectés.</span><span class="sxs-lookup"><span data-stu-id="639cb-148">Anonymous calls are disconnected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="639cb-149">Les appels ordinaires restent connectés.</span><span class="sxs-lookup"><span data-stu-id="639cb-149">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="639cb-150">Pour les groupes de réponse importés, les appels anonymes ayant atteint le pool de sauvegarde restent connectés.</span><span class="sxs-lookup"><span data-stu-id="639cb-150">For imported response groups, anonymous calls that have reached the backup pool remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="639cb-151">Appels en cours non encore connectés à un agent</span><span class="sxs-lookup"><span data-stu-id="639cb-151">In progress calls not yet connected to an agent</span></span></p></td>
<td><p><span data-ttu-id="639cb-152">Les appels sont déconnectés.</span><span class="sxs-lookup"><span data-stu-id="639cb-152">Calls are disconnected.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="639cb-153">Si les Response Groups n’ont pas été importés, aucun appel n’est dans ce statut.</span><span class="sxs-lookup"><span data-stu-id="639cb-153">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="639cb-154">Pour les groupes de réponse importés, les appels ayant atteint le pool de sauvegarde restent connectés.</span><span class="sxs-lookup"><span data-stu-id="639cb-154">For imported response groups, calls that have reached the backup pool remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="639cb-155">Nouveaux appels</span><span class="sxs-lookup"><span data-stu-id="639cb-155">New calls</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="639cb-156">Les appels sont déconnectés.</span><span class="sxs-lookup"><span data-stu-id="639cb-156">Calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="639cb-157">S’il s’agit de groupes de réponse importés, les appels se connectent au pool de sauvegarde, mais les agents hébergés dans le pool principal sont injoignables.</span><span class="sxs-lookup"><span data-stu-id="639cb-157">For imported response groups, calls connect to the backup pool, but agents homed in the primary pool are unreachable.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="639cb-158">Si les Response Groups n’ont pas été importés, les appels sont interrompus.</span><span class="sxs-lookup"><span data-stu-id="639cb-158">If response groups were not imported, calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="639cb-159">Pour les groupes de réponse importés, les appels se connectent au pool de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="639cb-159">For imported response groups, calls connect to the backup pool.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="639cb-160">Appels d’agent de la part de Response Group</span><span class="sxs-lookup"><span data-stu-id="639cb-160">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="639cb-161">Cette fonctionnalité est désactivée pendant cette étape</span><span class="sxs-lookup"><span data-stu-id="639cb-161">Feature is disabled during this stage</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="639cb-162">Si les Response Groups n’ont pas été importés, les appels échouent.</span><span class="sxs-lookup"><span data-stu-id="639cb-162">If response groups were not imported, calls fail.</span></span></p></li>
<li><p><span data-ttu-id="639cb-163">Pour les groupes de réponse importés, les appels aboutissent.</span><span class="sxs-lookup"><span data-stu-id="639cb-163">For imported response groups, calls succeed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="639cb-164">Informations de connexion et d’agent</span><span class="sxs-lookup"><span data-stu-id="639cb-164">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="639cb-165">Les groupes d’agents appartenant au pool principal peuvent être affichés sur la console de l’agent, mais les agents ne peuvent pas se connecter.</span><span class="sxs-lookup"><span data-stu-id="639cb-165">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="639cb-166">Les groupes d’agents appartenant au pool de sauvegarde peuvent être affichés sur la console de l’agent et les agents peuvent se connecter.</span><span class="sxs-lookup"><span data-stu-id="639cb-166">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="639cb-167">Les groupes d’agent importés s’affichent dans la console d’agent et les agents peuvent se connecter.</span><span class="sxs-lookup"><span data-stu-id="639cb-167">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="639cb-168">Les groupes d’agents appartenant au pool principal peuvent être affichés sur la console de l’agent, mais les agents ne peuvent pas se connecter.</span><span class="sxs-lookup"><span data-stu-id="639cb-168">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="639cb-169">Les groupes d’agents appartenant au pool de sauvegarde peuvent être affichés sur la console de l’agent et les agents peuvent se connecter.</span><span class="sxs-lookup"><span data-stu-id="639cb-169">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="639cb-170">Les groupes d’agent importés s’affichent dans la console d’agent et les agents peuvent se connecter.</span><span class="sxs-lookup"><span data-stu-id="639cb-170">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="639cb-171">Configuration de Response Group</span><span class="sxs-lookup"><span data-stu-id="639cb-171">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="639cb-172">Il est possible d’afficher les groupes de réponse appartenant au pool principal en fonction de la disponibilité de la base de données principale du pool principal, mais pas de les modifier.</span><span class="sxs-lookup"><span data-stu-id="639cb-172">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="639cb-173">Les groupes de réponse appartenant au pool de sauvegarde peuvent être affichés et modifiés.</span><span class="sxs-lookup"><span data-stu-id="639cb-173">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="639cb-174">Les groupes de réponse importés ne peuvent pas être affichés dans le panneau de configuration de Lync Server ou dans l’outil de configuration de groupe de réponse, mais ils peuvent être configurés en utilisant des applets de commande Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="639cb-174">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="639cb-175">En fonction de la disponibilité de la base de données principale, vous pouvez afficher les groupes de réponses détenus par le pool principal, mais ils ne peuvent pas être modifiés.</span><span class="sxs-lookup"><span data-stu-id="639cb-175">Response groups owned by the primary pool can be viewed, depending on the availability of the back end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="639cb-176">Les groupes de réponse appartenant au pool de sauvegarde peuvent être affichés et modifiés.</span><span class="sxs-lookup"><span data-stu-id="639cb-176">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="639cb-177">Les groupes de réponse importés ne peuvent pas être affichés dans le panneau de configuration de Lync Server ou dans l’outil de configuration de groupe de réponse, mais ils peuvent être configurés en utilisant des applets de commande Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="639cb-177">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-experience-during-failback"></a><span data-ttu-id="639cb-178">Utilisation des utilisateurs lors du retour arrière</span><span class="sxs-lookup"><span data-stu-id="639cb-178">User Experience During Failback</span></span>

<span data-ttu-id="639cb-179">Lorsqu’un administrateur appelle la restauration automatique vers le pool principal, l’activité de groupe de réponses est gérée pendant et après le retour automatique comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="639cb-179">When an administrator invokes failback to the primary pool, response group activity is handled during and after the failback as described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="639cb-180">Lors de la récupération après incident, les appels se comportent différemment selon que les groupes de réponses de la liste principale ont été importés au pool de sauvegarde lors de la récupération.</span><span class="sxs-lookup"><span data-stu-id="639cb-180">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="639cb-181">Dans le tableau suivant, les références aux groupes de réponse importés impliquent que les groupes de réponse de pool principal aient été importés dans le pool de sauvegarde lors du mode de récupération d’urgence.</span><span class="sxs-lookup"><span data-stu-id="639cb-181">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="call-handling-in-failback"></a><span data-ttu-id="639cb-182">Gestion des appels en retour automatique</span><span class="sxs-lookup"><span data-stu-id="639cb-182">Call Handling in Failback</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="639cb-183">Type d’appel ou d’action de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="639cb-183">Type of call or user action</span></span></th>
<th><span data-ttu-id="639cb-184">Pendant la restauration automatique</span><span class="sxs-lookup"><span data-stu-id="639cb-184">During Failback</span></span></th>
<th><span data-ttu-id="639cb-185">Après la restauration automatique</span><span class="sxs-lookup"><span data-stu-id="639cb-185">After Failback Completes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="639cb-186">Appels connectés à un agent</span><span class="sxs-lookup"><span data-stu-id="639cb-186">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="639cb-187">Les appels ordinaires restent connectés.</span><span class="sxs-lookup"><span data-stu-id="639cb-187">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="639cb-188">Si les Response Groups n’ont pas été importés, il n’y a pas de statut anonyme.</span><span class="sxs-lookup"><span data-stu-id="639cb-188">If response groups were not imported, no anonymous calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="639cb-189">Pour les groupes de réponse importés, les appels anonymes restent connectés.</span><span class="sxs-lookup"><span data-stu-id="639cb-189">For imported response groups, anonymous calls remain connected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="639cb-190">Les appels ordinaires restent connectés.</span><span class="sxs-lookup"><span data-stu-id="639cb-190">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="639cb-191">Si les Response Groups n’ont pas été importés, il n’y a pas de statut anonyme.</span><span class="sxs-lookup"><span data-stu-id="639cb-191">If response groups were not imported, no anonymous calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="639cb-192">Pour les groupes de réponse importés, les appels anonymes restent connectés.</span><span class="sxs-lookup"><span data-stu-id="639cb-192">For imported response groups, anonymous calls remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="639cb-193">Appels en cours non encore connectés à un agent</span><span class="sxs-lookup"><span data-stu-id="639cb-193">In progress calls not yet connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="639cb-194">Si les Response Groups n’ont pas été importés, aucun appel n’est dans ce statut.</span><span class="sxs-lookup"><span data-stu-id="639cb-194">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="639cb-195">Pour les groupes de réponse importés, les appels seront déconnectés.</span><span class="sxs-lookup"><span data-stu-id="639cb-195">For imported response groups, calls will be disconnected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="639cb-196">Si les Response Groups n’ont pas été importés, aucun appel n’est dans ce statut.</span><span class="sxs-lookup"><span data-stu-id="639cb-196">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="639cb-197">Pour les groupes de réponse importés, les appels seront déconnectés.</span><span class="sxs-lookup"><span data-stu-id="639cb-197">For imported response groups, calls will be disconnected.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="639cb-198">Nouveaux appels</span><span class="sxs-lookup"><span data-stu-id="639cb-198">New calls</span></span></p></td>
<td><p><span data-ttu-id="639cb-199">Les appels se connectent au pool principal, mais les agents hébergés dans le pool principal sont injoignables.</span><span class="sxs-lookup"><span data-stu-id="639cb-199">Calls connect to the primary pool, but agents homed in the primary pool are unreachable.</span></span></p></td>
<td><p><span data-ttu-id="639cb-200">Les appels se connectent à la liste principale.</span><span class="sxs-lookup"><span data-stu-id="639cb-200">Calls connect to the primary pool.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="639cb-201">Appels d’agent de la part de Response Group</span><span class="sxs-lookup"><span data-stu-id="639cb-201">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="639cb-202">Cette fonctionnalité est désactivée pendant cette étape.</span><span class="sxs-lookup"><span data-stu-id="639cb-202">Feature is disabled during this stage.</span></span></p></td>
<td><p><span data-ttu-id="639cb-203">Appels réussis.</span><span class="sxs-lookup"><span data-stu-id="639cb-203">Calls succeed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="639cb-204">Informations de connexion et d’agent</span><span class="sxs-lookup"><span data-stu-id="639cb-204">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="639cb-205">Les groupes d’agents appartenant au pool principal peuvent être affichés sur la console de l’agent, mais les agents ne peuvent pas se connecter.</span><span class="sxs-lookup"><span data-stu-id="639cb-205">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="639cb-206">Les groupes d’agents appartenant au pool de sauvegarde peuvent être affichés sur la console de l’agent et les agents peuvent se connecter.</span><span class="sxs-lookup"><span data-stu-id="639cb-206">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="639cb-207">Les groupes d’agent importés s’affichent dans la console d’agent et les agents peuvent se connecter.</span><span class="sxs-lookup"><span data-stu-id="639cb-207">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="639cb-208">Les groupes d’agents appartenant au pool principal peuvent être affichés sur la console de l’agent et les agents peuvent se connecter.</span><span class="sxs-lookup"><span data-stu-id="639cb-208">Agent groups owned by the primary pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="639cb-209">Les groupes d’agents appartenant au pool de sauvegarde peuvent être affichés sur la console de l’agent et les agents peuvent se connecter.</span><span class="sxs-lookup"><span data-stu-id="639cb-209">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="639cb-210">Les groupes d’agent importés ne sont pas affichés dans la console de l’agent.</span><span class="sxs-lookup"><span data-stu-id="639cb-210">Imported agent groups are not displayed on agent console.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="639cb-211">Configuration de Response Group</span><span class="sxs-lookup"><span data-stu-id="639cb-211">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="639cb-212">Il est possible d’afficher les groupes de réponse appartenant au pool principal en fonction de la disponibilité de la base de données principale du pool principal, mais pas de les modifier.</span><span class="sxs-lookup"><span data-stu-id="639cb-212">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="639cb-213">Les groupes de réponse appartenant au pool de sauvegarde peuvent être affichés et modifiés.</span><span class="sxs-lookup"><span data-stu-id="639cb-213">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="639cb-214">Les groupes de réponse importés ne peuvent pas être affichés dans le panneau de configuration de Lync Server ou dans l’outil de configuration de groupe de réponse, mais ils peuvent être configurés en utilisant des applets de commande Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="639cb-214">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="639cb-215">Les groupes de réponse appartenant au pool principal peuvent être affichés et modifiés.</span><span class="sxs-lookup"><span data-stu-id="639cb-215">Response groups owned by the primary pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="639cb-216">Les groupes de réponse appartenant au pool de sauvegarde peuvent être affichés et modifiés.</span><span class="sxs-lookup"><span data-stu-id="639cb-216">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="639cb-217">Les groupes de réponse importés ne peuvent pas être affichés dans le panneau de configuration de Lync Server ou dans l’outil de configuration de groupe de réponse, mais ils peuvent être configurés en utilisant des applets de commande Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="639cb-217">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="639cb-218">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="639cb-218">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

