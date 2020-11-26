---
title: 'Lync Server 2013 : gérer la collecte d’appels de groupe lors de la récupération d’urgence'
description: 'Lync Server 2013 : gérer la collecte d’appels de groupe lors de la récupération d’urgence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage Group Call Pickup during disaster recovery
ms:assetid: 2d32f19f-c649-4a72-a4fb-edd338e3a7cc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945618(v=OCS.15)
ms:contentKeyID: 51541455
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 04d85bc83cfe35571c2b0f47f707c9dcd8037d80
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426103"
---
# <a name="manage-group-call-pickup-during-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="d9714-103">Gérer la cueillette des appels de groupe lors de la récupération après sinistre dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d9714-103">Manage Group Call Pickup during disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d9714-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d9714-104">

<span> </span></span></span>

<span data-ttu-id="d9714-105">_**Dernière modification de la rubrique :** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="d9714-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="d9714-106">Lorsqu’un pool frontal devient indisponible en raison d’un incident imprévu, le service n’a pas pu être placé sur le pool de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="d9714-106">When a Front End pool becomes unavailable due an unplanned incident, service is failed over to the backup pool.</span></span> <span data-ttu-id="d9714-107">Pendant le basculement vers le pool de sauvegarde, les utilisateurs sont redirigés vers le pool de sauvegarde et sont en mode de résilience.</span><span class="sxs-lookup"><span data-stu-id="d9714-107">During failover to the backup pool, users are redirected to the backup pool and are in resiliency mode.</span></span> <span data-ttu-id="d9714-108">Dans le mode de résilience, les utilisateurs ne peuvent pas capter les appels d’autres utilisateurs ou avoir leurs appels sélectionnés par d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d9714-108">While in resiliency mode, users cannot pick up other users' calls or have their calls picked up by other users.</span></span> <span data-ttu-id="d9714-109">Lorsque le basculement est terminé, l’utilisateur peut à nouveau utiliser le prélèvement d’appel de groupe, comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="d9714-109">When failover is complete, users can again use Group Call Pickup as usual.</span></span>

<span data-ttu-id="d9714-110">Pendant la restauration automatique vers le pool principal, les utilisateurs sont redirigés vers le pool principal et sont de nouveau en mode de résilience.</span><span class="sxs-lookup"><span data-stu-id="d9714-110">During failback to the primary pool, users are redirected to the primary pool and are again in resiliency mode.</span></span> <span data-ttu-id="d9714-111">La fonctionnalité de cueillette des appels de groupe n’est pas disponible tant que les utilisateurs n’ont pas le mode de résilience.</span><span class="sxs-lookup"><span data-stu-id="d9714-111">Group Call Pickup functionality is not available until the users are out of resiliency mode.</span></span>

<span data-ttu-id="d9714-112">Cette section présente certaines considérations relatives à la collecte d’appels de groupe lors de la récupération après incident et décrit également l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d9714-112">This section discusses some considerations for Group Call Pickup during disaster recovery and also describes the user experience.</span></span>

<div>

## <a name="considerations-for-group-call-pickup-during-disaster-recovery"></a><span data-ttu-id="d9714-113">Éléments à prendre en compte lors d’une reprise d’appel de groupe</span><span class="sxs-lookup"><span data-stu-id="d9714-113">Considerations for Group Call Pickup During Disaster Recovery</span></span>

<span data-ttu-id="d9714-114">Lors de la récupération d’urgence, les utilisateurs qui ont été redirigés vers le pool de sauvegarde dans le cadre du processus de basculement utilisent l’application de parc d’appels qui s’exécute dans le pool de sauvegarde pour les numéros de groupe de capture d’appel.</span><span class="sxs-lookup"><span data-stu-id="d9714-114">During disaster recovery, users who have been redirected to the backup pool as part of the failover process use the Call Park application running in the backup pool for the call pickup group numbers.</span></span> <span data-ttu-id="d9714-115">Par conséquent, la prise en charge de la collecte des appels de groupe lors de la récupération d’urgence nécessite le déploiement et l’activation de l’application de stationnement d’appel dans le pool principal et le pool de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="d9714-115">Therefore, support for Group Call Pickup during disaster recovery requires the Call Park application to be deployed and enabled in both the primary pool and the backup pool.</span></span>

<span data-ttu-id="d9714-116">Le numéro de capture des appels de groupe dans la table d’orbite du parc d’appels doit être redirigé vers le pool de sauvegarde après le processus de basculement vers le pool de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="d9714-116">The Group Call Pickup number ranges in the call park orbit table must be redirected to the backup pool after the failover process to the backup pool is complete.</span></span> <span data-ttu-id="d9714-117">Les plages de chiffres doivent être redirigées vers le pool principal après le processus de restauration automatique vers le pool principal.</span><span class="sxs-lookup"><span data-stu-id="d9714-117">The number ranges must be redirected back to the primary pool after the failback process to the primary pool is complete.</span></span> <span data-ttu-id="d9714-118">Pour rediriger les plages de capture des appels de groupe, utilisez la cmdlet **Set-CsCallParkOrbit** .</span><span class="sxs-lookup"><span data-stu-id="d9714-118">To redirect the Group Call Pickup ranges, use the **Set-CsCallParkOrbit** cmdlet.</span></span>

<span data-ttu-id="d9714-119">Si vous déployez un nouveau pool avec un nom de domaine complet différent (FQDN) pour remplacer le pool principal, vous devez réaffecter toutes les plages de numéros de la liste des appels de groupe associés au pool principal au FQDN du nouveau pool.</span><span class="sxs-lookup"><span data-stu-id="d9714-119">If you deploy a new pool with a different fully qualified domain name (FQDN) to replace the primary pool, you need to reassign all the Group Call Pickup number ranges that were associated with the primary pool to the FQDN of the new pool.</span></span> <span data-ttu-id="d9714-120">Pour réattribuer des plages de nombres à la nouvelle liste, vous pouvez utiliser l’applet de cmdlet **Set-CsCallParkOrbit** .</span><span class="sxs-lookup"><span data-stu-id="d9714-120">To reassign number ranges to the new pool, you can use the **Set-CsCallParkOrbit** cmdlet.</span></span> <span data-ttu-id="d9714-121">Pour plus d’informations sur l’applet **de connexion Set-CsCallParkOrbit** , reportez-vous à [Set-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit).</span><span class="sxs-lookup"><span data-stu-id="d9714-121">For details about the **Set-CsCallParkOrbit** cmdlet, see [Set-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit).</span></span>

</div>

<div>

## <a name="group-call-pickup-experience-during-pool-failure"></a><span data-ttu-id="d9714-122">Capture d’écran d’un appel de groupe lors d’une panne de réserve</span><span class="sxs-lookup"><span data-stu-id="d9714-122">Group Call Pickup Experience During Pool Failure</span></span>

<span data-ttu-id="d9714-123">Le tableau suivant résume la fonction de découverte des appels de groupe lors des phases de reprise après sinistre.</span><span class="sxs-lookup"><span data-stu-id="d9714-123">The following table summarizes the Group Call Pickup experience through the phases of disaster recovery.</span></span>

### <a name="user-experience-during-disaster-recovery"></a><span data-ttu-id="d9714-124">Utilisation de l’utilisateur pendant une reprise après sinistre</span><span class="sxs-lookup"><span data-stu-id="d9714-124">User Experience During Disaster Recovery</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9714-125">État de l’appel</span><span class="sxs-lookup"><span data-stu-id="d9714-125">Call state</span></span></th>
<th><span data-ttu-id="d9714-126">Basculement vers le pool de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="d9714-126">Failover to backup pool</span></span></th>
<th><span data-ttu-id="d9714-127">Restauration automatique vers le pool principal</span><span class="sxs-lookup"><span data-stu-id="d9714-127">Failback to primary pool</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9714-128">Nouveaux appels</span><span class="sxs-lookup"><span data-stu-id="d9714-128">New calls</span></span></p></td>
<td><p><span data-ttu-id="d9714-129"><strong>Pendant le processus de basculement :</strong></span><span class="sxs-lookup"><span data-stu-id="d9714-129"><strong>During failover process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="d9714-130">Le prélèvement d’appels de groupe n’est pas disponible pour les utilisateurs en mode de résilience</span><span class="sxs-lookup"><span data-stu-id="d9714-130">Group Call Pickup not available for users in resiliency mode</span></span></p></li>
</ul>
<p><span data-ttu-id="d9714-131"><strong>Après le basculement complet :</strong></span><span class="sxs-lookup"><span data-stu-id="d9714-131"><strong>After failover is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="d9714-132">Le choix d’appel de groupe est disponible lorsque les utilisateurs ont des plages de résilience et de groupe redirigées vers le pool de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="d9714-132">Group Call Pickup available when users out of resiliency and Group Call Pickup number ranges are redirected to backup pool</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d9714-133"><strong>Pendant le processus de restauration automatique :</strong></span><span class="sxs-lookup"><span data-stu-id="d9714-133"><strong>During failback process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="d9714-134">Le prélèvement d’appels de groupe n’est pas disponible pour les utilisateurs en mode de résilience</span><span class="sxs-lookup"><span data-stu-id="d9714-134">Group Call Pickup not available for users in resiliency mode</span></span></p></li>
</ul>
<p><span data-ttu-id="d9714-135"><strong>Après la restauration automatique :</strong></span><span class="sxs-lookup"><span data-stu-id="d9714-135"><strong>After failback is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="d9714-136">Le prélèvement d’appel de groupe est disponible lorsque les utilisateurs ont des plages de résilience et de redirection des appels de groupe redirigés vers le pool principal</span><span class="sxs-lookup"><span data-stu-id="d9714-136">Group Call Pickup available when users out of resiliency and Group Call Pickup number ranges are redirected back to primary pool</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9714-137">Appels dans la file d’attente de cueillette des appels de groupe</span><span class="sxs-lookup"><span data-stu-id="d9714-137">Calls in Group Call Pickup queue</span></span></p></td>
<td><p><span data-ttu-id="d9714-138"><strong>Pendant le processus de basculement :</strong></span><span class="sxs-lookup"><span data-stu-id="d9714-138"><strong>During failover process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="d9714-139">Les appels dans la file d’attente ne peuvent pas être traités par le biais du prélèvement d’appels de groupe.</span><span class="sxs-lookup"><span data-stu-id="d9714-139">Calls in queue cannot be answered through Group Call Pickup.</span></span></p></li>
</ul>
<p><span data-ttu-id="d9714-140"><strong>Après le basculement complet :</strong></span><span class="sxs-lookup"><span data-stu-id="d9714-140"><strong>After failover is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="d9714-141">Aucun appel dans cet État</span><span class="sxs-lookup"><span data-stu-id="d9714-141">No calls in this state</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d9714-142"><strong>Pendant le processus de restauration automatique :</strong></span><span class="sxs-lookup"><span data-stu-id="d9714-142"><strong>During failback process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="d9714-143">Les appels dans la file d’attente ne peuvent pas être traités par le biais du prélèvement d’appels de groupe.</span><span class="sxs-lookup"><span data-stu-id="d9714-143">Calls in queue cannot be answered through Group Call Pickup.</span></span></p></li>
</ul>
<p><span data-ttu-id="d9714-144"><strong>Après la restauration automatique :</strong></span><span class="sxs-lookup"><span data-stu-id="d9714-144"><strong>After failback is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="d9714-145">Les appels dans la file d’attente ne peuvent pas être traités par le biais du prélèvement d’appels de groupe.</span><span class="sxs-lookup"><span data-stu-id="d9714-145">Calls in queue cannot be answered through Group Call Pickup.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9714-146">Appel établi</span><span class="sxs-lookup"><span data-stu-id="d9714-146">Established call</span></span></p></td>
<td><p><span data-ttu-id="d9714-147"><strong>Pendant le processus de basculement :</strong></span><span class="sxs-lookup"><span data-stu-id="d9714-147"><strong>During failover process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="d9714-148">Appels Restez connectés</span><span class="sxs-lookup"><span data-stu-id="d9714-148">Calls stay connected</span></span></p></li>
</ul>
<p><span data-ttu-id="d9714-149"><strong>Après le basculement complet :</strong></span><span class="sxs-lookup"><span data-stu-id="d9714-149"><strong>After failover is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="d9714-150">Appels Restez connectés</span><span class="sxs-lookup"><span data-stu-id="d9714-150">Calls stay connected</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d9714-151"><strong>Pendant le processus de restauration automatique :</strong></span><span class="sxs-lookup"><span data-stu-id="d9714-151"><strong>During failback process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="d9714-152">Appels Restez connectés</span><span class="sxs-lookup"><span data-stu-id="d9714-152">Calls stay connected</span></span></p></li>
</ul>
<p><span data-ttu-id="d9714-153"><strong>Après la restauration automatique :</strong></span><span class="sxs-lookup"><span data-stu-id="d9714-153"><strong>After failback is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="d9714-154">Appels Restez connectés</span><span class="sxs-lookup"><span data-stu-id="d9714-154">Calls stay connected</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="d9714-155">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d9714-155">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

