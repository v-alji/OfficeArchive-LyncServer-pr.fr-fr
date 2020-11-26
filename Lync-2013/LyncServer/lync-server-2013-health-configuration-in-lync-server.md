---
title: 'Lync Server 2013 : configuration d’intégrité dans Lync Server'
description: 'Lync Server 2013 : configuration du fonctionnement sur Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Health configuration in Lync Server 2013
ms:assetid: c00a8c8e-c2d2-4557-8c42-211c7cc96550
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205234(v=OCS.15)
ms:contentKeyID: 48185305
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 999a6d5401cb34382a4120f9255c91c846f72422
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427646"
---
# <a name="health-configuration-in-lync-server-2013"></a><span data-ttu-id="7eee4-103">Configuration de l’intégrité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7eee4-103">Health configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7eee4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7eee4-104">

<span> </span></span></span>

<span data-ttu-id="7eee4-105">_**Dernière modification de la rubrique :** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="7eee4-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="7eee4-106">Entre les différents sites Web, les Articles de la base de connaissances Microsoft et les outils du kit de ressources Lync Server, les administrateurs rencontrant des problèmes d’exécution de Lync Server ne sont jamais loin d’une solution pour résoudre ces problèmes.</span><span class="sxs-lookup"><span data-stu-id="7eee4-106">Between various websites, Microsoft Knowledge Base articles, and Lync Server Resource Kit tools, administrators who encounter problems when running Lync Server are never far from a way to solve those problems.</span></span>

<span data-ttu-id="7eee4-107">Évidemment, il n’existe aucun moyen de garantir que vous ne rencontrerez jamais de problèmes avec Lync Server 2013, car Lync Server peut être touché par de nombreux éléments tels que le blocage du réseau et les défaillances matérielles, que le produit lui-même ne peut pas contrôler.</span><span class="sxs-lookup"><span data-stu-id="7eee4-107">Obviously there is no way to guarantee that you will never encounter problems with Lync Server 2013 because Lync Server can be affected by many things—like network crashes and hardware failures—that the product itself cannot control.</span></span> <span data-ttu-id="7eee4-108">En implémentant le contrôle d’intégrité, les administrateurs peuvent identifier les problèmes potentiels avant qu’ils ne deviennent des problèmes réels.</span><span class="sxs-lookup"><span data-stu-id="7eee4-108">By implementing health monitoring, administrators can identify potential problems before they turn into actual problems.</span></span> <span data-ttu-id="7eee4-109">Par exemple, les administrateurs peuvent utiliser le contrôle du serveur Lync pour identifier les tendances et tendances des.</span><span class="sxs-lookup"><span data-stu-id="7eee4-109">For example, administrators can use Lync Server monitoring to identify trends and tendencies.</span></span> <span data-ttu-id="7eee4-110">Par exemple, une augmentation constante du nombre de conférences audio/vidéo peut vous suggérer de devoir ajouter de la capacité avant que le système ne soit surchargé.</span><span class="sxs-lookup"><span data-stu-id="7eee4-110">For example, a steady increase in the number of audio/video conferences might suggest a need to add capacity before the system becomes overloaded.</span></span>

<span data-ttu-id="7eee4-111">De la même façon, les administrateurs peuvent utiliser System Center Operations Manager pour effectuer les actions suivantes lors de l’exécution d’alertes en temps réel lors de l’exécution d’événements spécifiques et de l’exécution de transactions de synthèse qui testent activement le système.</span><span class="sxs-lookup"><span data-stu-id="7eee4-111">In a similar fashion, administrators can use System Center Operations Manager to do such things as issue real-time alerts when specified events occur, and to run synthetic transactions that proactively test the system.</span></span> <span data-ttu-id="7eee4-112">Les transactions synthétiques sont utilisées dans Lync Server pour vérifier que les utilisateurs sont en mesure de réaliser des tâches courantes, telles que la connexion au système, l’échange de messages instantanés ou l’appel d’appels vers un téléphone figurant sur le réseau téléphonique public commuté (RTC).</span><span class="sxs-lookup"><span data-stu-id="7eee4-112">Synthetic transactions are used in Lync Server to verify that users are able to successfully complete common tasks such as logging on to the system, exchanging instant messages, or making calls to a phone located on the public switched telephone network (PSTN).</span></span> <span data-ttu-id="7eee4-113">Par exemple, l’exécution périodique de ces tests peut vous avertir en cas de problème avec les utilisateurs qui se connectent à Lync Server et vous permet de corriger le problème avant que votre équipe de support ne puisse se connecter.</span><span class="sxs-lookup"><span data-stu-id="7eee4-113">For example, periodically running these tests can alert you to potential problems with users logging on to Lync Server, and give you a chance to correct the problem before your support team is flooded with calls from users unable to make a connection.</span></span> <span data-ttu-id="7eee4-114">L’utilisation de System Center Operations Manager pour exécuter ces transactions synthétiques peut surveiller régulièrement le déploiement de Lync Server pour 24 heures sur 24 sans avoir à faire beaucoup de choses au-delà de répondre à des alertes éventuellement émises.</span><span class="sxs-lookup"><span data-stu-id="7eee4-114">By using System Center Operations Manager to run these synthetic transactions, administrators can routinely monitor their deployment of Lync Server continuously for 24 hours every day without having to do much of anything beyond responding to any alerts that might be issued.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7eee4-115">Pour Lync Server 2013, le pack d’administration pour System Center Operations Manager est également capable de détecter les problèmes « externes » qui peuvent avoir un impact sur Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7eee4-115">For Lync Server 2013, the Management Pack for System Center Operations Manager is also able to detect "external" issues that can adversely affect Lync Server.</span></span> <span data-ttu-id="7eee4-116">Par exemple, les administrateurs peuvent être avertis si Internet Information Services (IIS) se déconnecte, les ressources système sur un ordinateur Lync Server sont inférieures à un certain nombre de ressources ou un ordinateur serveur Lync rencontre une défaillance matérielle.</span><span class="sxs-lookup"><span data-stu-id="7eee4-116">For example, administrators can be notified if Internet Information Services (IIS) goes offline, system resources on a Lync Server computer fall below a specified amount, or a Lync Server computer experiences a hardware failure.</span></span>



</div>

<span data-ttu-id="7eee4-117">La configuration de l’intégrité de Lync Server 2013 est basée sur System Center Operations Manager et sur l’utilisation des packs de gestion de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7eee4-117">Health configuration in Lync Server 2013 is built around System Center Operations Manager and the use of Lync Server Management Packs.</span></span> <span data-ttu-id="7eee4-118">Les packs d’administration suivants incluent un certain nombre de nouvelles fonctionnalités et améliorations, notamment :</span><span class="sxs-lookup"><span data-stu-id="7eee4-118">These Management Packs include a number of new features and enhancements, including:</span></span>

  - <span data-ttu-id="7eee4-119">**Disponibilité des scénarios à partir de n’importe quel emplacement.**</span><span class="sxs-lookup"><span data-stu-id="7eee4-119">**Scenario availability from any location.**</span></span> <span data-ttu-id="7eee4-120">Le pack d’administration de Lync Server 2010 a présenté le concept de surveillance de la disponibilité des scénarios des utilisateurs finaux aux transactions synthétiques.</span><span class="sxs-lookup"><span data-stu-id="7eee4-120">The Lync Server 2010 Management Pack introduced the concept of monitoring end user scenario availability with synthetic transactions.</span></span> <span data-ttu-id="7eee4-121">Dans Lync Server 2013, ces agents présentent de plus en plus de transactions synthétiques et peuvent être exécutés à partir de différents emplacements au sein de l’entreprise, d’emplacements géographiques distants en dehors de l’entreprise, d’applications de succursale et de déploiements de Lync Server 2010 pour ajouter une couverture aux déploiements de périphérie héritée.</span><span class="sxs-lookup"><span data-stu-id="7eee4-121">In Lync Server 2013, these agents have more synthetic transactions and can be run from a variety of locations inside the enterprise, from remote geographic locations outside of the enterprise, against branch office appliances and against Lync Server 2010 deployments to add coverage to legacy Edge deployments.</span></span>

  - <span data-ttu-id="7eee4-122">**Journaux de transactions synthétiques.**</span><span class="sxs-lookup"><span data-stu-id="7eee4-122">**Synthetic transaction logs.**</span></span> <span data-ttu-id="7eee4-123">En cas d’échec d’une transaction synthétique, les administrateurs ont accès aux journaux HTML pour vous aider à déterminer les échecs.</span><span class="sxs-lookup"><span data-stu-id="7eee4-123">When a synthetic transaction fails, administrators have access to HTML logs to help determine what failed.</span></span> <span data-ttu-id="7eee4-124">Il s’agit notamment de savoir quelle action a échoué, la latence de chaque action, la ligne de commande utilisée pour exécuter le test et l’erreur rencontrée.</span><span class="sxs-lookup"><span data-stu-id="7eee4-124">This includes understanding which action failed, the latency of each action, the command-line used to run the test, and the error that was encountered.</span></span>

  - <span data-ttu-id="7eee4-125">**Meilleure couverture de la fiabilité des appels.**</span><span class="sxs-lookup"><span data-stu-id="7eee4-125">**Increased call reliability coverage.**</span></span> <span data-ttu-id="7eee4-126">Le pack d’administration de Lync Server 2010 a présenté une alerte de fiabilité des appels pour détecter des problèmes de connectivité importants qui affectent les appels audio des utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="7eee4-126">The Lync Server 2010 Management Pack introduced call reliability alerting to detect severe connectivity issues that affect the audio calls of end users.</span></span> <span data-ttu-id="7eee4-127">Les packs d’administration de Lync Server 2013 ajoutent une couverture pour la messagerie instantanée et d’autres fonctions de base pour la couverture tout en réduisant le bruit.</span><span class="sxs-lookup"><span data-stu-id="7eee4-127">The Lync Server 2013 Management Packs add coverage for peer-to-peer instant messaging (IM) and other basic conferencing features to maximize coverage while reducing noise.</span></span>

  - <span data-ttu-id="7eee4-128">**Analyse des dépendances.**</span><span class="sxs-lookup"><span data-stu-id="7eee4-128">**Dependency monitoring.**</span></span> <span data-ttu-id="7eee4-129">Les scénarios Lync Server peuvent échouer en raison d’un large éventail de facteurs externes tels que les services Internet (IIS) qui sont déconnectés, les ressources de mémoire et d’UC limitées, et les problèmes de disque.</span><span class="sxs-lookup"><span data-stu-id="7eee4-129">Lync Server scenarios can fail due to a variety of external factors such as IIS being offline, limited CPU and memory resources, and disk issues.</span></span> <span data-ttu-id="7eee4-130">Les nouveaux packs de gestion vérifient plusieurs dépendances critiques pour s’assurer que les administrateurs connaissent leurs répercussions.</span><span class="sxs-lookup"><span data-stu-id="7eee4-130">The new management packs check several critical dependencies to ensure administrators are aware of their impact.</span></span>

  - <span data-ttu-id="7eee4-131">**Rapports améliorés.**</span><span class="sxs-lookup"><span data-stu-id="7eee4-131">**Enhanced reporting.**</span></span> <span data-ttu-id="7eee4-132">Un ensemble de rapports permettant aux administrateurs d’évaluer la disponibilité des scénarios, de planifier la capacité et de voir quels composants rencontrent le plus de problèmes.</span><span class="sxs-lookup"><span data-stu-id="7eee4-132">A set of reports to help administrators estimate scenario availability, plan for capacity, and see which components are experiencing the most issues.</span></span>

<span data-ttu-id="7eee4-133">Les packs de gestion incluent également diverses fonctionnalités qui permettent de détecter et de diagnostiquer une visibilité en temps réel dans le déploiement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7eee4-133">The Management Packs also include a variety of features to help detect and diagnose provide real-time visibility into the health your Lync Server deployment.</span></span> <span data-ttu-id="7eee4-134">Ces fonctionnalités sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7eee4-134">These features are listed in the following table.</span></span>

### <a name="management-pack-features"></a><span data-ttu-id="7eee4-135">Fonctionnalités du pack d’administration</span><span class="sxs-lookup"><span data-stu-id="7eee4-135">Management Pack Features</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7eee4-136">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="7eee4-136">Feature</span></span></th>
<th><span data-ttu-id="7eee4-137">Description</span><span class="sxs-lookup"><span data-stu-id="7eee4-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7eee4-138">Transactions synthétiques</span><span class="sxs-lookup"><span data-stu-id="7eee4-138">Synthetic Transactions</span></span></p></td>
<td><p><span data-ttu-id="7eee4-139">Les applets de connexion Windows PowerShell peuvent être exécutées à partir de différents emplacements pour s’assurer que les scénarios utilisateur finaux tels que la connexion, la présence, la messagerie instantanée et les conférences sont facilement accessibles aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="7eee4-139">Windows PowerShell cmdlets that can be run from various locations to ensure that end user scenarios such as sign-in, presence, IM, and conferencing are readily available to end users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eee4-140">Alertes de fiabilité des appels</span><span class="sxs-lookup"><span data-stu-id="7eee4-140">Call Reliability Alerts</span></span></p></td>
<td><p><span data-ttu-id="7eee4-141">Requêtes de base de données pour les enregistrements des détails des appels (CDR).</span><span class="sxs-lookup"><span data-stu-id="7eee4-141">Database queries for Call Detail Records (CDR).</span></span> <span data-ttu-id="7eee4-142">Ces enregistrements sont écrits par des serveurs frontaux pour indiquer si les utilisateurs finaux étaient en mesure de se connecter à un appel ou la fin d’un appel.</span><span class="sxs-lookup"><span data-stu-id="7eee4-142">These records are written by Front End Servers to reflect whether end users were able to connect to a call or why a call was terminated.</span></span> <span data-ttu-id="7eee4-143">Ces requêtes génèrent des alertes indiquant qu’un grand nombre d’utilisateurs finaux rencontrent des problèmes de connectivité pour les appels d’égal à égal ou les fonctionnalités de conférence de base.</span><span class="sxs-lookup"><span data-stu-id="7eee4-143">These queries result in alerts that indicate when a wide range of end users are experiencing connectivity issues for peer-to-peer calls or basic conferencing functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eee4-144">Alertes de qualité multimédia</span><span class="sxs-lookup"><span data-stu-id="7eee4-144">Media Quality Alerts</span></span></p></td>
<td><p><span data-ttu-id="7eee4-145">Requêtes de base de données qui observent les rapports de qualité d’expérimentation (QoE) publiés par les clients à la fin de chaque appel.</span><span class="sxs-lookup"><span data-stu-id="7eee4-145">Database queries that look at Quality of Experience (QoE) reports published by clients at the end of each call.</span></span> <span data-ttu-id="7eee4-146">Ces requêtes génèrent des alertes qui identifient les scénarios dans lesquels les utilisateurs risquent de rencontrer des problèmes de qualité de média lors des appels et des conférences.</span><span class="sxs-lookup"><span data-stu-id="7eee4-146">These queries result in alerts that pinpoint scenarios where users are likely to be experiencing poor media quality during calls and conferences.</span></span> <span data-ttu-id="7eee4-147">Les données sont bâties sur des indicateurs clés, comme la latence et la perte de paquets, des métriques connues pour contribuer directement à la qualité des appels.</span><span class="sxs-lookup"><span data-stu-id="7eee4-147">The data is built upon key metrics such as packet latency and loss, metrics that are known to directly contribute to call quality.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eee4-148">État du composant</span><span class="sxs-lookup"><span data-stu-id="7eee4-148">Component Health</span></span></p></td>
<td><p><span data-ttu-id="7eee4-149">Les composants serveur individuels déclenchent des alertes à l’aide de journaux d’événements et de compteurs de performance.</span><span class="sxs-lookup"><span data-stu-id="7eee4-149">Individual server components raise alerts by using event logs and performance counters.</span></span> <span data-ttu-id="7eee4-150">Ces alertes indiquent des conditions d’échec qui peuvent avoir un impact important sur un ou plusieurs scénarios utilisateur finaux.</span><span class="sxs-lookup"><span data-stu-id="7eee4-150">These alerts indicate failure conditions that can severely impact one or more end user scenarios.</span></span> <span data-ttu-id="7eee4-151">Ces alertes peuvent également indiquer un grand nombre de conditions d’échec, y compris les services qui ne sont pas en cours d’exécution, les taux d’échec élevés, la latence des messages importants ou les problèmes de connectivité.</span><span class="sxs-lookup"><span data-stu-id="7eee4-151">These alerts can also indicate a variety of other failure conditions, including services not running, high failure rates, high message latency, or connectivity issues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eee4-152">État de dépendance</span><span class="sxs-lookup"><span data-stu-id="7eee4-152">Dependency Health</span></span></p></td>
<td><p><span data-ttu-id="7eee4-153">Des échecs peuvent se produire pour diverses raisons externes.</span><span class="sxs-lookup"><span data-stu-id="7eee4-153">Failures can occur for a variety of external reasons.</span></span> <span data-ttu-id="7eee4-154">Les packs de gestion contrôlent et recueillent désormais des données pour certaines des dépendances externes critiques susceptibles d’indiquer des problèmes importants, y compris la disponibilité d’IIS, l’utilisation du processeur et de la mémoire de serveurs et de processus, et des métriques de disque.</span><span class="sxs-lookup"><span data-stu-id="7eee4-154">The management packs now monitor and collect data for some of the critical external dependencies that might indicate severe issues, including IIS availability, CPU and memory usage of servers and processes, and disk metrics.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7eee4-155">Les alertes émises par le système sont classées en trois catégories générales :</span><span class="sxs-lookup"><span data-stu-id="7eee4-155">The alerts issued by the system have been classified into three general categories:</span></span>

  - <span data-ttu-id="7eee4-156">**Alertes à priorité élevée.**</span><span class="sxs-lookup"><span data-stu-id="7eee4-156">**High-priority Alerts.**</span></span> <span data-ttu-id="7eee4-157">Ces alertes indiquent des conditions qui engendreront des interruptions de service pour de grands groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7eee4-157">These alerts indicate conditions that will cause service outages for large groups of users.</span></span> <span data-ttu-id="7eee4-158">Par exemple, une défaillance de composant sur un seul ordinateur n’est pas une alerte de priorité élevée, car Lync Server 2013 inclut des fonctionnalités de haute disponibilité intégrées.</span><span class="sxs-lookup"><span data-stu-id="7eee4-158">For example, a component failure on a single machine is not a high-priority alert because Lync Server 2013 has built-in high availability features.</span></span> <span data-ttu-id="7eee4-159">Au lieu de cela, les alertes de priorité élevée représentent des problèmes importants» pour réactiver les administrateurs de la journée.»</span><span class="sxs-lookup"><span data-stu-id="7eee4-159">Instead, high-priority alerts represent problems serious enough “to wake up administrators at night.”</span></span> <span data-ttu-id="7eee4-160">Les pannes détectées par les transactions synthétiques et les services hors connexion (par exemple, les conférences audio/vidéo) sont éligibles en tant qu’alertes à priorité élevée.</span><span class="sxs-lookup"><span data-stu-id="7eee4-160">Outages detected by synthetic transactions and offline services (for example, audio/video conferencing) qualify as high-priority alerts.</span></span>

  - <span data-ttu-id="7eee4-161">**Alertes de priorité moyenne.**..</span><span class="sxs-lookup"><span data-stu-id="7eee4-161">**Medium-priority alerts.**.</span></span> <span data-ttu-id="7eee4-162">Ces alertes indiquent des conditions qui affectent un sous-ensemble d’utilisateurs ou indiquent la dégradation de la qualité d’appel.</span><span class="sxs-lookup"><span data-stu-id="7eee4-162">These alerts indicate conditions that affect a subset of users or indicate call quality degradation.</span></span> <span data-ttu-id="7eee4-163">Cela inclut les problèmes tels que les défaillances de composant, la latence dans l’établissement d’appel ou la qualité audio détériorée lors d’un appel.</span><span class="sxs-lookup"><span data-stu-id="7eee4-163">That includes problems such as component failures, latency in call establishment, or degraded audio quality in call.</span></span> <span data-ttu-id="7eee4-164">Les alertes de cette catégorie sont avec état et indiquent l’état actuel du problème.</span><span class="sxs-lookup"><span data-stu-id="7eee4-164">Alerts in this category are stateful and indicate the current status of the issue.</span></span> <span data-ttu-id="7eee4-165">Par exemple, supposons que la durée de votre établissement d’appel dépasse le seuil d’alerte.</span><span class="sxs-lookup"><span data-stu-id="7eee4-165">For example, suppose your call establishment times exceed the alert threshold.</span></span> <span data-ttu-id="7eee4-166">Si les heures d’établissement d’appel retournent à normal, ces alertes sont résolues automatiquement dans System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="7eee4-166">If call establishment times return to normal, these alerts will be auto-resolved in System Center Operations Manager.</span></span> <span data-ttu-id="7eee4-167">Le préversion de ces alertes est qu’un administrateur le verra sur la même journée de travail.</span><span class="sxs-lookup"><span data-stu-id="7eee4-167">The expectation for these alerts is that an administrator will look at them on the same business day.</span></span>

  - <span data-ttu-id="7eee4-168">**Autres alertes.**</span><span class="sxs-lookup"><span data-stu-id="7eee4-168">**Other alerts.**</span></span> <span data-ttu-id="7eee4-169">Il s’agit d’alertes provenant de composants susceptibles d’affecter un utilisateur ou un sous-ensemble d’utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="7eee4-169">These are alerts from components that might affect a specific user or subset of users.</span></span> <span data-ttu-id="7eee4-170">Par exemple, il est possible que le service de carnet d’adresses ne puisse pas analyser l’entrée Active Directory d’un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="7eee4-170">For example, perhaps the Address Book service could not parse the Active Directory entry of a given user.</span></span> <span data-ttu-id="7eee4-171">L’attente de ces alertes est que les administrateurs y accrire lorsque le temps est disponible.</span><span class="sxs-lookup"><span data-stu-id="7eee4-171">The expectation for these alerts is that administrators will get to them when they have time available.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7eee4-172">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7eee4-172">In This Section</span></span>

  - [<span data-ttu-id="7eee4-173">Configuration de Lync Server 2013 pour fonctionner avec System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="7eee4-173">Configuring Lync Server 2013 to work with System Center Operations Manager</span></span>](lync-server-2013-configuring-lync-server-to-work-with-system-center-operations-manager.md)

  - [<span data-ttu-id="7eee4-174">Utilisation de la journalisation détaillée pour les transactions synthétiques dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7eee4-174">Using rich logging for synthetic transactions in Lync Server 2013</span></span>](lync-server-2013-using-rich-logging-for-synthetic-transactions.md)

  - [<span data-ttu-id="7eee4-175">Utilisation de Microsoft SQL Server 2008 R2 en tant que base de données Gestionnaire d’opérations System Center pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7eee4-175">Using Microsoft SQL Server 2008 R2 as your System Center Operations Manager database for Lync Server 2013</span></span>](lync-server-2013-using-microsoft-sql-server-2008-r2-as-your-system-center-operations-manager-database.md)

<span data-ttu-id="7eee4-176"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7eee4-176"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

