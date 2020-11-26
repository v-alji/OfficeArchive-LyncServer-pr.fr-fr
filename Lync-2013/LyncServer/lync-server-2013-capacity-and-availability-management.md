---
title: 'Lync Server 2013 : gestion des capacités et de la disponibilité'
description: 'Lync Server 2013 : gestion des capacités et de la disponibilité.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity and availability management
ms:assetid: 207a2997-f482-4bee-892d-d2b112294481
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720325(v=OCS.15)
ms:contentKeyID: 63969586
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d498649651f8cfbccc65f5b1b5f010025ac418e7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435599"
---
# <a name="capacity-and-availability-management-in-lync-server-2013"></a><span data-ttu-id="28c92-103">Gestion de la capacité et de la disponibilité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="28c92-103">Capacity and availability management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="28c92-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="28c92-104">

<span> </span></span></span>

<span data-ttu-id="28c92-105">_**Dernière modification de la rubrique :** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="28c92-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="28c92-106">L’objectif de la gestion de la capacité et de la gestion de la disponibilité est de mesurer et de contrôler les performances du système.</span><span class="sxs-lookup"><span data-stu-id="28c92-106">The purpose of capacity management and availability management is to measure and control system performance.</span></span> <span data-ttu-id="28c92-107">Nous vous recommandons de mettre en œuvre des procédures de gestion de la capacité et de gestion de la disponibilité pour pouvoir mesurer et contrôler les performances du système.</span><span class="sxs-lookup"><span data-stu-id="28c92-107">We recommend that you implement capacity management and availability management procedures so that you can measure and control system performance.</span></span> <span data-ttu-id="28c92-108">Vous devez savoir si le système est disponible et s’il peut gérer les demandes actuelles et projetées en définissant des plannings de référence et en analysant le système pour trouver des tendances.</span><span class="sxs-lookup"><span data-stu-id="28c92-108">You have to know whether the system is available and if it can handle the current and the projected demands by setting baselines and monitoring the system to look for trends.</span></span>

<div>

## <a name="capacity-management"></a><span data-ttu-id="28c92-109">Gestion de la capacité</span><span class="sxs-lookup"><span data-stu-id="28c92-109">Capacity management</span></span>

<span data-ttu-id="28c92-110">La gestion de la capacité implique la planification, le dimensionnement et la gestion de la capacité de service pour garantir que les niveaux de performance minimum spécifiés dans votre SLA soient dépassés.</span><span class="sxs-lookup"><span data-stu-id="28c92-110">Capacity management involves planning, sizing, and controlling service capacity to help guarantee that the minimum performance levels specified in your SLA are exceeded.</span></span> <span data-ttu-id="28c92-111">La gestion de la capacité est un bon moyen de garantir que vous pouvez fournir des services informatiques à un tarif raisonnable tout en respectant les niveaux de performance définis dans les SLA avec le client.</span><span class="sxs-lookup"><span data-stu-id="28c92-111">Good capacity management helps ensure that you can provide IT services at a reasonable cost and still meet the levels of performance defined in your SLAs with the client.</span></span> <span data-ttu-id="28c92-112">Ces critères peuvent être les suivants :</span><span class="sxs-lookup"><span data-stu-id="28c92-112">These criteria can include the following:</span></span>

  - <span data-ttu-id="28c92-113">**Temps de réponse du système**   Il s’agit de la durée mesurée que le système exécute pour effectuer des actions courantes.</span><span class="sxs-lookup"><span data-stu-id="28c92-113">**System Response Time**   This is the measured time that the system takes to do typical actions.</span></span> <span data-ttu-id="28c92-114">Par exemple, le temps nécessaire au rôle du serveur audio/vidéo pour le traitement du trafic audio et vidéo, le temps nécessaire à un client pour la création et la participation à une conférence, ou le temps nécessaire pour la mise à jour de la présence dans tous les clients FileSystemWatcher.</span><span class="sxs-lookup"><span data-stu-id="28c92-114">Examples include the time that is required for the audio/video server role to process audio/video traffic, the time that is required for a client to create and join a conference, or the time taken for presence to be updated in all watcher clients.</span></span>

  - <span data-ttu-id="28c92-115">**Capacité de stockage**   Il s’agit de la capacité d’un système de stockage, qu’il s’agisse d’une base de données de contenu, d’un périphérique de sauvegarde ou d’un disque local.</span><span class="sxs-lookup"><span data-stu-id="28c92-115">**Storage Capacity**   This is the capacity of a storage system, whether it is a content database, a backup device, or a local drive.</span></span> <span data-ttu-id="28c92-116">Par exemple, vous pouvez inclure le volume maximal d’espace de stockage par site, ainsi que l’heure de stockage des copies de sauvegarde avant leur remplacement.</span><span class="sxs-lookup"><span data-stu-id="28c92-116">Examples include the maximum amount of storage space to be provided per site and the time that backups should be stored before they are overwritten.</span></span>

<span data-ttu-id="28c92-117">La modification de la capacité est souvent le cas pour garantir la disponibilité de ressources physiques suffisantes, telles que l’espace disque et la bande passante réseau.</span><span class="sxs-lookup"><span data-stu-id="28c92-117">Adjusting capacity is frequently a case of making sure that enough physical resources are available, such as disk space and network bandwidth.</span></span> <span data-ttu-id="28c92-118">Le tableau suivant répertorie les résolutions typiques des problèmes liés à la capacité.</span><span class="sxs-lookup"><span data-stu-id="28c92-118">The following table lists typical resolutions for capacity-related issues.</span></span>

### <a name="typical-resolutions-for-capacity-related-issues"></a><span data-ttu-id="28c92-119">Résolution standard pour les problèmes liés à la capacité</span><span class="sxs-lookup"><span data-stu-id="28c92-119">Typical resolutions for capacity-related issues</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="28c92-120">Problème</span><span class="sxs-lookup"><span data-stu-id="28c92-120">Issue</span></span></th>
<th><span data-ttu-id="28c92-121">Résolution possible</span><span class="sxs-lookup"><span data-stu-id="28c92-121">Possible resolution</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28c92-122">Utilisateurs distants ayant des performances audio/vidéo médiocres</span><span class="sxs-lookup"><span data-stu-id="28c92-122">Remote users having poor audio/video performance</span></span></p></td>
<td><p><span data-ttu-id="28c92-123">Vérifiez si la bande passante appropriée est disponible sur les liaisons WAN et si la QoS est activée et configurée correctement.</span><span class="sxs-lookup"><span data-stu-id="28c92-123">Check to see whether appropriate bandwidth is available on the WAN links and if QoS is enabled and appropriately configured.</span></span> <span data-ttu-id="28c92-124">Vérifiez les données QoE.</span><span class="sxs-lookup"><span data-stu-id="28c92-124">Check QoE data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28c92-125">La réponse globale de l’environnement Lync est lente.</span><span class="sxs-lookup"><span data-stu-id="28c92-125">Overall response of the Lync environment is slow.</span></span></p></td>
<td><p><span data-ttu-id="28c92-126">Exécutez des tests pour vérifier que les serveurs frontaux existants peuvent gérer le chargement.</span><span class="sxs-lookup"><span data-stu-id="28c92-126">Run tests to check that the existing front-end servers can deal with the load.</span></span> <span data-ttu-id="28c92-127">Introduisez un nouveau serveur frontal le cas échéant. Vérifiez les temps de réponse de la base de données SQL et résolvez les causes des retards (par exemple, amélioration du disque e/s).</span><span class="sxs-lookup"><span data-stu-id="28c92-127">Introduce a new front-end server if it is needed.Check SQL database response times and fix the causes for the delays (for example, improve disk I/O).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="28c92-128">Pour plus d’informations, reportez-vous à la section Guide de mise en réseau de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="28c92-128">Troubleshooting in greater detail is covered in the Lync Server Networking Guide.</span></span>

<span data-ttu-id="28c92-129">La capacité est affectée par la configuration du système et dépend des ressources physiques telles que la bande passante réseau.</span><span class="sxs-lookup"><span data-stu-id="28c92-129">Capacity is affected by system configuration and depends on physical resources such as network bandwidth.</span></span> <span data-ttu-id="28c92-130">Par exemple, si un environnement Lync est configuré pour effectuer une sauvegarde complète nocturne, il est nécessaire de veiller à ce qu’il soit possible de réduire l’impact sur les performances interactives de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="28c92-130">For example, if a Lync environment is configured to perform a full backup nightly, care must be taken to help guarantee that the effect on the interactive performance experienced by end-users is minimized.</span></span>

<span data-ttu-id="28c92-131">La gestion de la capacité est le processus de conservation de la capacité d’un système dans des niveaux acceptables et répond aux problèmes suivants :</span><span class="sxs-lookup"><span data-stu-id="28c92-131">Capacity management is the process of keeping the capacity of a system within acceptable levels and addresses the following issues:</span></span>

  - <span data-ttu-id="28c92-132">**Réaction aux modifications apportées aux spécifications**   Les exigences de capacité doivent être ajustées de façon à ce qu’elles soient modifiées au sein du système ou de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="28c92-132">**Reacting to changes in requirements**   Capacity requirements have to be adjusted to account for changes in the system or the organization.</span></span> <span data-ttu-id="28c92-133">Par exemple, si votre environnement décide de mettre en place une voix entreprise, le nombre et l’emplacement des passerelles de réseau téléphonique commuté (PSTN) et du réseau public commuté (RTC) seront très importants.</span><span class="sxs-lookup"><span data-stu-id="28c92-133">For example, if your environment decides to implement Enterprise Voice, the number and placement of Mediation Servers and public switched telephone network (PSTN) gateways will be very important.</span></span> <span data-ttu-id="28c92-134">Si vous enverrez le trunking SIP (Session Initiation Protocol) ou le SIP direct, le design global sera considérablement modifié pour offrir les meilleures performances vocales pour l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="28c92-134">If you'll be doing Session Initiation Protocol (SIP) trunking or direct SIP, the overall design will be significantly changed to provide the best Enterprise Voice performance.</span></span>

  - <span data-ttu-id="28c92-135">**Prévision des exigences futures**   Certaines exigences de capacité changent en prévision dans le temps.</span><span class="sxs-lookup"><span data-stu-id="28c92-135">**Predicting future requirements**   Some capacity requirements change predictably over time.</span></span> <span data-ttu-id="28c92-136">En effectuant le suivi des tendances, vous pouvez planifier des mises à jour à l’avance.</span><span class="sxs-lookup"><span data-stu-id="28c92-136">By tracking trends you can plan upgrades in advance.</span></span> <span data-ttu-id="28c92-137">Par exemple, la bande passante disponible entre divers sites Lync doit être contrôlée pour créer un planning de référence.</span><span class="sxs-lookup"><span data-stu-id="28c92-137">For example, available bandwidth between various Lync sites must be monitored to create a baseline.</span></span> <span data-ttu-id="28c92-138">Ce planning de référence vous permettra d’augmenter la quantité de bande passante que vous devez ajouter à ces liens, car le nombre d’utilisateurs dans ces sites distants augmente avec le temps.</span><span class="sxs-lookup"><span data-stu-id="28c92-138">This baseline will allow you to predict when you have to add more bandwidth to these links as user count in these remote sites increases with time.</span></span>

</div>

<div>

## <a name="availability-management"></a><span data-ttu-id="28c92-139">Gestion de la disponibilité</span><span class="sxs-lookup"><span data-stu-id="28c92-139">Availability management</span></span>

<span data-ttu-id="28c92-140">La gestion de la disponibilité est le processus qui permet de garantir le bon respect de tout service informatique et d’offrir le niveau de service cohérent et fiable requis par le client.</span><span class="sxs-lookup"><span data-stu-id="28c92-140">Availability management is the process of making sure that any IT service consistently and cost effectively delivers the level of consistent, reliable service that is required by the customer.</span></span> <span data-ttu-id="28c92-141">La gestion de la disponibilité implique de limiter la perte de services et de vérifier que l’action appropriée est effectuée en cas de perte de service.</span><span class="sxs-lookup"><span data-stu-id="28c92-141">Availability management deals with minimizing loss of service and with making sure that appropriate action is taken if service is lost.</span></span> <span data-ttu-id="28c92-142">Dans un environnement Lync, vous voudrez peut-être savoir si le service voix entreprise est disponible, si les utilisateurs peuvent participer à des conférences planifiées, etc.</span><span class="sxs-lookup"><span data-stu-id="28c92-142">In a Lync environment, you may be concerned about whether the Enterprise Voice service is available, whether users can join scheduled conferences, and so on.</span></span> <span data-ttu-id="28c92-143">Un SLA définit une fréquence et une durée acceptables d’arrêts et autorise des périodes lorsque le système n’est pas disponible pour la maintenance planifiée.</span><span class="sxs-lookup"><span data-stu-id="28c92-143">An SLA defines an acceptable frequency and length of outages and allows for certain periods when the system is unavailable for planned maintenance.</span></span>

<span data-ttu-id="28c92-144">Si vous devez fournir des rapports à votre gestion concernant la disponibilité des systèmes, ou si vous avez des pénalités financières ou d’autres pénalités associées à des cibles de disponibilité manquantes, vous devez enregistrer les données de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="28c92-144">If you have to provide reports to your management about the availability of systems, or if you have financial or other penalties associated with missing availability targets, you must record availability data.</span></span> <span data-ttu-id="28c92-145">Même si vous n’avez pas cette configuration, il est conseillé de savoir au moins le nombre d’échecs d’un système pendant une période donnée.</span><span class="sxs-lookup"><span data-stu-id="28c92-145">Even if you do not have such formal requirements, it is a good idea to at least know how frequently a system has failed in a certain time period.</span></span> <span data-ttu-id="28c92-146">Par exemple, la disponibilité du système au cours des 12 derniers mois et le temps nécessaire à la récupération de chaque échec.</span><span class="sxs-lookup"><span data-stu-id="28c92-146">For example, system availability in the last 12 months and how long it took to recover from each failure.</span></span> <span data-ttu-id="28c92-147">Ces informations vous permettront de mesurer et d’améliorer l’efficacité de votre équipe en réponse à une panne système.</span><span class="sxs-lookup"><span data-stu-id="28c92-147">This information will help you measure and improve your team’s effectiveness in responding to a system failure.</span></span> <span data-ttu-id="28c92-148">Il peut également vous fournir des informations utiles en cas de litige.</span><span class="sxs-lookup"><span data-stu-id="28c92-148">It can also give you useful information if there is a dispute.</span></span>

<span data-ttu-id="28c92-149">Les mesures liées à la disponibilité sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="28c92-149">Measures related to availability are as follows:</span></span>

  - <span data-ttu-id="28c92-150">**Disponibilité**   En règle générale, il s’agit du moment où le système ou service est accessible par rapport au temps qu’il est fixé.</span><span class="sxs-lookup"><span data-stu-id="28c92-150">**Availability**   This is typically expressed as the time that a system or service can be accessed compared to the time that it is down.</span></span> <span data-ttu-id="28c92-151">Elle est généralement exprimée en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="28c92-151">It is typically expressed as a percentage.</span></span> <span data-ttu-id="28c92-152">(Il est possible que vous voyiez des références à « trois neuf » ou « cinq neuf ».</span><span class="sxs-lookup"><span data-stu-id="28c92-152">(You may see references to “three nines” or “five nines”.</span></span> <span data-ttu-id="28c92-153">Celles-ci se réfèrent à la disponibilité de 99,9% ou 99,999%.)</span><span class="sxs-lookup"><span data-stu-id="28c92-153">These refer to 99.9 percent or 99.999 percent availability.)</span></span>

  - <span data-ttu-id="28c92-154">**Fiabilité**   Il s’agit d’une mesure du temps entre les échecs d’un système et est parfois exprimée en temps moyenne (ou moyenne) entre les échecs (MTBF).</span><span class="sxs-lookup"><span data-stu-id="28c92-154">**Reliability**   This is a measure of the time between failures of a system and is sometimes expressed as mean (or average) time between failures (MTBF).</span></span>

  - <span data-ttu-id="28c92-155">**Durée de la réparation**   Il s’agit du temps nécessaire pour récupérer un service après une panne et est souvent exprimée en tant que moyen (moyenne) temps de réparation (MTTR).</span><span class="sxs-lookup"><span data-stu-id="28c92-155">**Time to Repair**   This is the time taken to recover a service after a failure has occurred and is often expressed as mean (meaning average) time to repair (MTTR).</span></span>

<span data-ttu-id="28c92-156">La disponibilité, la fiabilité et le temps de réparation sont liés comme suit :</span><span class="sxs-lookup"><span data-stu-id="28c92-156">Availability, reliability, and time to repair are related as follows:</span></span>

<span data-ttu-id="28c92-157">**Disponibilité = (MTBF-MTTR)/MTBF**   Par exemple, si un serveur tombe en panne deux fois sur une période de six mois et n’est pas disponible pour une moyenne de 20 minutes, le temps de MTBF est de trois mois ou 90, et le MTTR est de 20 minutes.</span><span class="sxs-lookup"><span data-stu-id="28c92-157">**Availability = (MTBF – MTTR) / MTBF**   For example, if a server fails two times over a six-month period and is unavailable for an average of 20 minutes, the MTBF is three months or 90 days and the MTTR is 20 minutes.</span></span> <span data-ttu-id="28c92-158">Par conséquent, la disponibilité = (90 jours – 20 minutes)/90 jours = 99,985%.</span><span class="sxs-lookup"><span data-stu-id="28c92-158">Therefore, Availability = (90 days – 20 minutes) / 90 days = 99.985 percent.</span></span>

<span data-ttu-id="28c92-159">La gestion de la disponibilité est le processus de vérification de l’agrandissement et de la disponibilité de la disponibilité dans les paramètres définis dans les SLA.</span><span class="sxs-lookup"><span data-stu-id="28c92-159">Availability management is the process of making sure that availability is maximized and kept within the parameters that are defined in SLAs.</span></span> <span data-ttu-id="28c92-160">La gestion de la disponibilité comprend les processus suivants :</span><span class="sxs-lookup"><span data-stu-id="28c92-160">Availability management includes the following processes:</span></span>

  - <span data-ttu-id="28c92-161">**Surveiller**    Examen du temps et des services indisponibles.</span><span class="sxs-lookup"><span data-stu-id="28c92-161">**Monitoring**    Examining when and for how long services are unavailable.</span></span>

  - <span data-ttu-id="28c92-162">**Création de rapports**   Les chiffres de disponibilité doivent être fournis régulièrement aux équipes gestion, utilisateurs et opérations.</span><span class="sxs-lookup"><span data-stu-id="28c92-162">**Reporting**   Availability figures should be regularly provided to management, users, and operations teams.</span></span> <span data-ttu-id="28c92-163">Ce rapport doit mettre en évidence des tendances et identifier les domaines qui nécessitent une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="28c92-163">These reports should highlight trends and identify areas that are doing well and areas that require attention.</span></span> <span data-ttu-id="28c92-164">Le rapport doit résumer la conformité aux cibles définies dans les SLA.</span><span class="sxs-lookup"><span data-stu-id="28c92-164">The report should summarize compliance with targets set in the SLAs.</span></span>

  - <span data-ttu-id="28c92-165">**Amélioration**   Si la disponibilité ne correspond pas aux cibles définies dans les SLA ou lorsque la tendance est une disponibilité réduite, le processus de gestion de la disponibilité doit planifier les étapes de remédiation.</span><span class="sxs-lookup"><span data-stu-id="28c92-165">**Improvement**   If availability does not meet targets that are defined in the SLAs or where the trend is toward reduced availability, the availability management process should plan remedial steps.</span></span> <span data-ttu-id="28c92-166">Cela devrait inclure le fait de travailler avec d’autres équipes responsables pour mettre en évidence les raisons des pannes et de planifier des actions de remédiation pour éviter toute réapparition des pannes.</span><span class="sxs-lookup"><span data-stu-id="28c92-166">This should include working with other responsible teams to highlight reasons for outages and to plan remedial actions to prevent a recurrence of the outages.</span></span>

<span data-ttu-id="28c92-167">Les mesures de capacité et de disponibilité sont des tâches répétées qui conviennent idéalement aux outils et scripts automatisés tels que Microsoft System Center Operations Manager (anciennement Microsoft Operations Manager), qui est abordé plus loin dans ce document.</span><span class="sxs-lookup"><span data-stu-id="28c92-167">Capacity and availability measurements are repetitive tasks that are ideally suited to automated tools and scripts such as Microsoft System Center Operations Manager (formerly Microsoft Operations Manager), which is discussed later in this document.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="28c92-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28c92-168">See Also</span></span>


[<span data-ttu-id="28c92-169">Surveiller Lync Server 2013 avec System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="28c92-169">Monitoring Lync Server 2013 with System Center Operations Manager</span></span>](lync-server-2013-monitoring-lync-server-with-system-center-operations-manager.md)  
  

<span data-ttu-id="28c92-170"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="28c92-170"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

