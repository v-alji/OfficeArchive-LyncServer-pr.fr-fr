---
title: 'Rapport de distribution d’échec Lync Server 2013 :'
description: 'Lync Server 2013 : rapport de distribution d’échecs.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failure Distribution Report
ms:assetid: 365c7beb-24d4-40f5-92e7-4978b9688916
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558635(v=OCS.15)
ms:contentKeyID: 48183849
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5a87f779f87d6b7002fa108f1969c33739eed9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428215"
---
# <a name="failure-distribution-report-in-lync-server-2013"></a><span data-ttu-id="e28e2-103">Rapport de distribution des échecs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e28e2-103">Failure Distribution Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e28e2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e28e2-104">

<span> </span></span></span>

<span data-ttu-id="e28e2-105">_**Dernière modification de la rubrique :** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="e28e2-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="e28e2-106">Le rapport de répartition des défaillances classe les sessions ayant échoué selon les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="e28e2-106">The Failure Distribution Report ranks failed sessions in the following categories:</span></span>

  - <span data-ttu-id="e28e2-107">Motifs de diagnostic principaux</span><span class="sxs-lookup"><span data-stu-id="e28e2-107">Top diagnostic reasons</span></span>

  - <span data-ttu-id="e28e2-108">Modalités principales</span><span class="sxs-lookup"><span data-stu-id="e28e2-108">Top modalities</span></span>

  - <span data-ttu-id="e28e2-109">Pools principaux</span><span class="sxs-lookup"><span data-stu-id="e28e2-109">Top pools</span></span>

  - <span data-ttu-id="e28e2-110">Sources principales</span><span class="sxs-lookup"><span data-stu-id="e28e2-110">Top sources</span></span>

  - <span data-ttu-id="e28e2-111">Composants principaux</span><span class="sxs-lookup"><span data-stu-id="e28e2-111">Top components</span></span>

  - <span data-ttu-id="e28e2-112">Utilisateurs émetteurs principaux</span><span class="sxs-lookup"><span data-stu-id="e28e2-112">Top from users</span></span>

  - <span data-ttu-id="e28e2-113">Utilisateurs destinataires principaux</span><span class="sxs-lookup"><span data-stu-id="e28e2-113">Top to users</span></span>

  - <span data-ttu-id="e28e2-114">Agents utilisateurs émetteurs principaux</span><span class="sxs-lookup"><span data-stu-id="e28e2-114">Top from user agents</span></span>

<span data-ttu-id="e28e2-p101">Vous pouvez utiliser ces catégories pour rechercher exactement le problème et, dans certains cas, déterminer la raison de ce problème. Par exemple, supposons que vous avez enregistré 242 sessions audio/vidéo ayant échoué au cours d’une journée donnée. Si vous examinez le rapport de répartition des défaillances, il peut indiquer que 237 de ces sessions ont eu lieu dans le pool Dublin. C’est un bon point de départ pour rechercher et diagnostiquer les causes à l’origine de ces défaillances. Si vous cliquez sur le pool Dublin sous la catégorie **Pools principaux**, vous y trouverez un rapport de répartition des défaillances spécifique à ce pool. Vous pouvez ensuite commencer à analyser les raisons qui ont entraîné autant de difficultés dans le pool.</span><span class="sxs-lookup"><span data-stu-id="e28e2-p101">You can use these categories to determine exactly where a problem is occurring and, in some cases, why the problem is occurring. For example, suppose you recorded 242 failed audio/video sessions during a given day. If you look at the Failure Distribution Report, it might show that 237 of those failed sessions took place in your Dublin pool. That gives you a good place to start when it comes to tracking down and diagnosing the causes behind those failures. If you click on the Dublin pool under the **Top pools** category, you will see a Failure Distribution Report just for that pool. You can then begin analyzing why the Dublin pool was experiencing so many difficulties.</span></span>

<div>

## <a name="viewing-the-failure-distribution-report"></a><span data-ttu-id="e28e2-121">Affichage du rapport de répartition des défaillances</span><span class="sxs-lookup"><span data-stu-id="e28e2-121">Viewing the Failure Distribution Report</span></span>

<span data-ttu-id="e28e2-122">Vous pouvez accéder au rapport de répartition des défaillances à partir de n’importe lequel des rapports suivants en cliquant sur la mesure **Nombre d’échecs attendus** ou **Nombre d’échecs inattendus** :</span><span class="sxs-lookup"><span data-stu-id="e28e2-122">You can access the Failure Distribution Report from any of the following reports by clicking either the **Expected failure volume** or the **Unexpected failure volume** metric:</span></span>

  - [<span data-ttu-id="e28e2-123">Rapport sur les principaux échecs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e28e2-123">Top Failures Report in Lync Server 2013</span></span>](lync-server-2013-top-failures-report.md)

  - [<span data-ttu-id="e28e2-124">Rapport de diagnostic de conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e28e2-124">Conference Diagnostic Report in Lync Server 2013</span></span>](lync-server-2013-conference-diagnostic-report.md)

  - [<span data-ttu-id="e28e2-125">Rapport de diagnostic d’activité d’égal à égal dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e28e2-125">Peer-to-Peer Activity Diagnostic Report in Lync Server 2013</span></span>](lync-server-2013-peer-to-peer-activity-diagnostic-report.md)

<span data-ttu-id="e28e2-126">Dans le rapport de distribution des échecs, vous pouvez cliquer sur l’une des mesures suivantes pour afficher le [rapport de liste d’échecs dans Lync Server 2013](lync-server-2013-failure-list-report.md):</span><span class="sxs-lookup"><span data-stu-id="e28e2-126">From the Failure Distribution Report, you can click any of the following metrics to view the [Failure List Report in Lync Server 2013](lync-server-2013-failure-list-report.md):</span></span>

  - <span data-ttu-id="e28e2-127">Motifs de diagnostic principaux (sessions)</span><span class="sxs-lookup"><span data-stu-id="e28e2-127">Top diagnostic reasons (sessions)</span></span>

  - <span data-ttu-id="e28e2-128">Modalités principales (sessions)</span><span class="sxs-lookup"><span data-stu-id="e28e2-128">Top modalities (sessions)</span></span>

  - <span data-ttu-id="e28e2-129">Pools principaux (sessions)</span><span class="sxs-lookup"><span data-stu-id="e28e2-129">Top pools (sessions)</span></span>

  - <span data-ttu-id="e28e2-130">Sources principales (sessions)</span><span class="sxs-lookup"><span data-stu-id="e28e2-130">Top sources (sessions)</span></span>

  - <span data-ttu-id="e28e2-131">Composants principaux (sessions)</span><span class="sxs-lookup"><span data-stu-id="e28e2-131">Top components (sessions)</span></span>

  - <span data-ttu-id="e28e2-132">Utilisateurs émetteurs principaux (sessions)</span><span class="sxs-lookup"><span data-stu-id="e28e2-132">Top from users (sessions)</span></span>

  - <span data-ttu-id="e28e2-133">Utilisateurs destinataires principaux (sessions)</span><span class="sxs-lookup"><span data-stu-id="e28e2-133">Top to users (sessions)</span></span>

  - <span data-ttu-id="e28e2-134">Agents utilisateurs émetteurs principaux (sessions)</span><span class="sxs-lookup"><span data-stu-id="e28e2-134">Top from user agents (sessions)</span></span>

</div>

<div>

## <a name="using-the-failure-distribution-report"></a><span data-ttu-id="e28e2-135">Utilisation du rapport de répartition des défaillances</span><span class="sxs-lookup"><span data-stu-id="e28e2-135">Using the Failure Distribution Report</span></span>

<span data-ttu-id="e28e2-p102">Selon la taille de votre moniteur et sa résolution d’écran, il est possible que certaines des données indiquées dans le rapport de répartition des défaillances soient tronquées à l’écran. Cela se vérifie en particulier pour les mesures comme les agents utilisateurs qui ont des libellés très longs. Par exemple, un agent utilisateur dont le nom est « UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Lync 2013) » peut ne s’afficher que partiellement à l’écran :</span><span class="sxs-lookup"><span data-stu-id="e28e2-p102">Depending on your monitor size and screen resolution, it's possible that some of the data shown in the Failure Distribution Report might be truncated when you view it onscreen. This is especially true for metrics such as user agents, which can have very long labels. For example, a user agent with a name like "UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Lync 2013)" might only partially appear onscreen:</span></span>

<span data-ttu-id="e28e2-139">UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Ly...</span><span class="sxs-lookup"><span data-stu-id="e28e2-139">UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Ly...</span></span>

<span data-ttu-id="e28e2-140">Fort heureusement, vous pouvez voir le libellé en entier en maintenant votre souris au-dessus de la valeur tronquée.</span><span class="sxs-lookup"><span data-stu-id="e28e2-140">Fortunately, you can see the entire label simply by holding your mouse over the truncated value.</span></span>

<span data-ttu-id="e28e2-p103">L’ID de diagnostic est une mesure intéressante sur laquelle vous pouvez filtrer dans le rapport de répartition des défaillances. Si le même ID de diagnostic s’affiche dans d’autres rapports, vous pouvez filtrer sur cet ID dans le rapport de répartition des défaillances et obtenir des informations très détaillées sur l’emplacement exact où a été signalé cet ID pendant une session ayant échoué et sa fréquence.</span><span class="sxs-lookup"><span data-stu-id="e28e2-p103">One interesting metric that you can filter on by using the Failure Distribution Report is Diagnostic ID. If you see the same Diagnostic ID cropping up in other reports you can filter on that ID in the Failure Distribution Report and get a very detailed look at exactly where, and how often, that ID has been reported during a failed session.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="e28e2-143">Filtres</span><span class="sxs-lookup"><span data-stu-id="e28e2-143">Filters</span></span>

<span data-ttu-id="e28e2-p104">Les filtres vous offrent la possibilité de renvoyer un ensemble de données mieux ciblées ou de visualiser les données renvoyées de différentes manières. Par exemple, le rapport de répartition des défaillances vous permet de filtrer sur des critères tels que le type d’activité (session entre homologues ou session de conférence) ou à l’aide de l’ID de diagnostic qui a accompagné chaque session ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="e28e2-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Failed Distribution Report enables you to filter on such things as the activity type (peer-to-peer session or conferencing session) or by the diagnostic ID that accompanied each failed session.</span></span>

<span data-ttu-id="e28e2-146">Le tableau qui suit dresse la liste des filtres que vous pouvez utiliser avec le rapport de répartition des défaillances.</span><span class="sxs-lookup"><span data-stu-id="e28e2-146">The following table lists the filters that you can use with the Failure Distribution Report.</span></span>

### <a name="failure-distribution-report-filters"></a><span data-ttu-id="e28e2-147">Filtres du rapport de répartition des défaillances</span><span class="sxs-lookup"><span data-stu-id="e28e2-147">Failure Distribution Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e28e2-148">Nom</span><span class="sxs-lookup"><span data-stu-id="e28e2-148">Name</span></span></th>
<th><span data-ttu-id="e28e2-149">Description</span><span class="sxs-lookup"><span data-stu-id="e28e2-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-150"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-150"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-p105">Date/heure de début de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de début comme suit :</span><span class="sxs-lookup"><span data-stu-id="e28e2-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="e28e2-153">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="e28e2-153">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="e28e2-p106">Si vous ne précisez aucune heure de début, le rapport commence automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="e28e2-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="e28e2-156">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="e28e2-156">7/7/2012</span></span></p>
<p><span data-ttu-id="e28e2-157">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="e28e2-157">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="e28e2-158">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="e28e2-158">7/3/2012</span></span></p>
<p><span data-ttu-id="e28e2-159">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="e28e2-159">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e28e2-160"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-160"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-p107">Date/heure de fin de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de fin comme suit :</span><span class="sxs-lookup"><span data-stu-id="e28e2-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="e28e2-163">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="e28e2-163">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="e28e2-p108">Si vous ne précisez aucune heure de fin, le rapport se termine automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="e28e2-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="e28e2-166">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="e28e2-166">7/7/2012</span></span></p>
<p><span data-ttu-id="e28e2-167">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="e28e2-167">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="e28e2-168">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="e28e2-168">7/3/2012</span></span></p>
<p><span data-ttu-id="e28e2-169">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="e28e2-169">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-170"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-170"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-p109">Nom de domaine complet (FQDN) du pool de serveurs d’inscriptions. Vous pouvez soit sélectionner un pool particulier, soit cliquer sur <strong>[Tous]</strong> pour afficher les données de tous les pools. Cette liste déroulante se renseigne automatiquement en fonction des enregistrements que contient la base de données.</span><span class="sxs-lookup"><span data-stu-id="e28e2-p109">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e28e2-174"><strong>Type d’activité</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-174"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-p110">Type d’activité sur laquelle filtrer. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="e28e2-p110">Type of activity to filter on. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="e28e2-177">[Tous]</span><span class="sxs-lookup"><span data-stu-id="e28e2-177">[All]</span></span></p></li>
<li><p><span data-ttu-id="e28e2-178">Égal à égal</span><span class="sxs-lookup"><span data-stu-id="e28e2-178">Peer-to-peer</span></span></p></li>
<li><p><span data-ttu-id="e28e2-179">Conférence</span><span class="sxs-lookup"><span data-stu-id="e28e2-179">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-180"><strong>Catégorie de session</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-180"><strong>Session category</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-p111">Indique si l’activité en question a réussi ou échoué. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="e28e2-p111">Indicates whether the activity in question succeeded or failed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="e28e2-183">[Tous]</span><span class="sxs-lookup"><span data-stu-id="e28e2-183">[All]</span></span></p></li>
<li><p><span data-ttu-id="e28e2-184">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="e28e2-184">Success</span></span></p></li>
<li><p><span data-ttu-id="e28e2-185">Échec attendu</span><span class="sxs-lookup"><span data-stu-id="e28e2-185">Expected failure</span></span></p></li>
<li><p><span data-ttu-id="e28e2-186">Échec inattendu</span><span class="sxs-lookup"><span data-stu-id="e28e2-186">Unexpected failure</span></span></p></li>
</ul>
<p><span data-ttu-id="e28e2-187">Un &quot; échec attendu &quot; est un échec censé se produire.</span><span class="sxs-lookup"><span data-stu-id="e28e2-187">An &quot;expected failure&quot; is a failure that is expected to happen.</span></span> <span data-ttu-id="e28e2-188">Par exemple, si un utilisateur a défini son statut sur Ne pas déranger, les appels passés à cet utilisateur échouent.</span><span class="sxs-lookup"><span data-stu-id="e28e2-188">For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span> <span data-ttu-id="e28e2-189">Un &quot; échec inattendu &quot; est une défaillance qui peut se produire dans un système de bon fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="e28e2-189">An &quot;unexpected failure&quot; is a failure that occurs in what would appear to be an otherwise healthy system.</span></span> <span data-ttu-id="e28e2-190">Par exemple, un appel n’est pas censé s’interrompre lorsque l’appelant est mis en attente.</span><span class="sxs-lookup"><span data-stu-id="e28e2-190">For example, a call should not be terminated if the caller is placed on hold.</span></span> <span data-ttu-id="e28e2-191">Si cela se produit, l’incident est marqué comme un échec inattendu.</span><span class="sxs-lookup"><span data-stu-id="e28e2-191">If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e28e2-192"><strong>ID de diagnostic</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-192"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-p113">Identificateur unique (sous la forme d’un en-tête ms-diagnostics) attaché à un message SIP qui fournit souvent des informations utiles pour résoudre des erreurs. Les en-têtes de diagnostic sont facultatifs (il est possible que des sessions SIP n’incluent pas ces en-têtes) et les ID de diagnostic sont uniquement signalés pour les sessions qui ont rencontré des problèmes, quels qu’ils soient.</span><span class="sxs-lookup"><span data-stu-id="e28e2-p113">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-diagnostic-reasons"></a><span data-ttu-id="e28e2-195">Mesures pour les motifs de diagnostic principaux</span><span class="sxs-lookup"><span data-stu-id="e28e2-195">Metrics for Top Diagnostic Reasons</span></span>

<span data-ttu-id="e28e2-196">Le tableau ci-dessous liste les informations fournies dans le rapport de répartition des défaillances sur la base de l’ID de diagnostic le plus fréquemment signalé.</span><span class="sxs-lookup"><span data-stu-id="e28e2-196">The following table lists the information provided in the Failure Distribution Report based on the most frequently reported diagnostic ID.</span></span>

### <a name="metrics-for-top-diagnostic-reasons"></a><span data-ttu-id="e28e2-197">Mesures pour les motifs de diagnostic principaux</span><span class="sxs-lookup"><span data-stu-id="e28e2-197">Metrics for Top Diagnostic Reasons</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e28e2-198">Nom</span><span class="sxs-lookup"><span data-stu-id="e28e2-198">Name</span></span></th>
<th><span data-ttu-id="e28e2-199">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="e28e2-199">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e28e2-200">Description</span><span class="sxs-lookup"><span data-stu-id="e28e2-200">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-201"><strong>Classement</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-201"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-202">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-202">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-p114">Classement relatif des sessions ayant échoué sur la base des ID de diagnostic. Identificateur unique (sous la forme d’un en-tête ms-diagnostics) joint à un message SIP qui fournit souvent des informations utiles à l’identification et à la résolution des erreurs.</span><span class="sxs-lookup"><span data-stu-id="e28e2-p114">Relative ranking of failed sessions based on diagnostic IDs. The diagnostic ID is a unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e28e2-205"><strong>Motifs de diagnostic principaux</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-205"><strong>Top diagnostic reasons</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-206">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-206">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-207">ID de diagnostic généré dans une session.</span><span class="sxs-lookup"><span data-stu-id="e28e2-207">Diagnostic ID generated in a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-208"><strong>Sessions</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-208"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-209">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-209">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-210">Nombre total de sessions ayant échoué où l’ID de diagnostic spécifié a été généré.</span><span class="sxs-lookup"><span data-stu-id="e28e2-210">Total number of failed sessions where the specified diagnostic ID was generated.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-modalities"></a><span data-ttu-id="e28e2-211">Mesures pour les modalités principales</span><span class="sxs-lookup"><span data-stu-id="e28e2-211">Metrics for Top Modalities</span></span>

<span data-ttu-id="e28e2-212">Le tableau ci-dessous liste les informations fournies dans le rapport de répartition des défaillances sur la base des modalités de session ayant rencontré le plus d’échecs.</span><span class="sxs-lookup"><span data-stu-id="e28e2-212">The following table lists the information provided in the Failure Distribution Report based on the session modalities that experienced the most failures.</span></span>

### <a name="metrics-for-top-modalities"></a><span data-ttu-id="e28e2-213">Mesures pour les modalités principales</span><span class="sxs-lookup"><span data-stu-id="e28e2-213">Metrics for Top Modalities</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e28e2-214">Nom</span><span class="sxs-lookup"><span data-stu-id="e28e2-214">Name</span></span></th>
<th><span data-ttu-id="e28e2-215">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="e28e2-215">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e28e2-216">Description</span><span class="sxs-lookup"><span data-stu-id="e28e2-216">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-217"><strong>Classement</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-217"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-218">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-218">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-219">Classement relatif des sessions ayant échoué sur la base du type de session (par exemple, une conférence audio/vidéo ou une session de transfert de fichiers entre homologues).</span><span class="sxs-lookup"><span data-stu-id="e28e2-219">Relative ranking based of failed session based on session type (for example, an audio/video conference or a peer-to-peer file transfer session).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e28e2-220"><strong>Modalités principales</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-220"><strong>Top modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-221">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-221">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-222">Type de session.</span><span class="sxs-lookup"><span data-stu-id="e28e2-222">Session type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-223"><strong>Sessions</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-223"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-224">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-224">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-225">Nombre total de sessions ayant échoué impliquant la modalité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e28e2-225">Total number of failed sessions involving the specified modality.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-pools"></a><span data-ttu-id="e28e2-226">Mesures pour les pools principaux</span><span class="sxs-lookup"><span data-stu-id="e28e2-226">Metrics for Top Pools</span></span>

<span data-ttu-id="e28e2-227">Le tableau ci-dessous liste les informations fournies dans le rapport de répartition des défaillances sur la base des pools ayant rencontré le plus d’échecs.</span><span class="sxs-lookup"><span data-stu-id="e28e2-227">The following table lists the information provided in the Failure Distribution Report based on the pools that experienced the most failures.</span></span>

### <a name="metrics-for-top-pools"></a><span data-ttu-id="e28e2-228">Mesures pour les pools principaux</span><span class="sxs-lookup"><span data-stu-id="e28e2-228">Metrics for Top Pools</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e28e2-229">Nom</span><span class="sxs-lookup"><span data-stu-id="e28e2-229">Name</span></span></th>
<th><span data-ttu-id="e28e2-230">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="e28e2-230">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e28e2-231">Description</span><span class="sxs-lookup"><span data-stu-id="e28e2-231">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-232"><strong>Classement</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-232"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-233">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-233">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-234">Classement relatif de sessions ayant échoué en fonction du pool d’inscriptions ou du serveur Edge sur lequel la session a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="e28e2-234">Relative ranking of failed sessions based on the Registrar pool or Edge Server where the session was conducted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e28e2-235"><strong>Pools principaux</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-235"><strong>Top pools</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-236">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-236">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-237">Nom du pool d’inscriptions ou du serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="e28e2-237">Name of the Registrar pool or Edge Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-238"><strong>Sessions</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-238"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-239">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-239">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-240">Nombre total de sessions ayant échoué par pool d’inscriptions ou serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="e28e2-240">Total number of failed sessions per Registrar pool or Edge Server.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-sources"></a><span data-ttu-id="e28e2-241">Mesures pour les sources principales</span><span class="sxs-lookup"><span data-stu-id="e28e2-241">Metrics for Top Sources</span></span>

<span data-ttu-id="e28e2-242">Le tableau ci-dessous liste les informations fournies dans le rapport de répartition des défaillances sur la base des ordinateurs ayant rencontré le plus d’échecs.</span><span class="sxs-lookup"><span data-stu-id="e28e2-242">The following table lists the information provided in the Failure Distribution Report based on the computers that experienced the most failures.</span></span>

### <a name="metrics-for-top-sources"></a><span data-ttu-id="e28e2-243">Mesures pour les sources principales</span><span class="sxs-lookup"><span data-stu-id="e28e2-243">Metrics for Top Sources</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e28e2-244">Nom</span><span class="sxs-lookup"><span data-stu-id="e28e2-244">Name</span></span></th>
<th><span data-ttu-id="e28e2-245">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="e28e2-245">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e28e2-246">Description</span><span class="sxs-lookup"><span data-stu-id="e28e2-246">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-247"><strong>Classement</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-247"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-248">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-248">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-249">Classement relatif des sessions ayant échoué par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e28e2-249">Relative ranking failed sessions per computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e28e2-250"><strong>Sources principales</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-250"><strong>Top sources</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-251">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-251">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-252">Nom de l’ordinateur impliqué dans la session ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="e28e2-252">Name of the computer involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-253"><strong>Sessions</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-253"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-254">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-254">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-255">Nombre total de sessions ayant échoué par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e28e2-255">Total number of failed sessions per computer.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-components"></a><span data-ttu-id="e28e2-256">Mesures pour les composants principaux</span><span class="sxs-lookup"><span data-stu-id="e28e2-256">Metrics for Top Components</span></span>

<span data-ttu-id="e28e2-257">Le tableau suivant répertorie les informations fournies dans le rapport de distribution d’échec basées sur les composants Microsoft Lync Server 2010 ayant rencontré le plus de problèmes.</span><span class="sxs-lookup"><span data-stu-id="e28e2-257">The following table lists the information provided in the Failure Distribution Report based on the Microsoft Lync Server 2010 components that experienced the most failures.</span></span>

### <a name="metrics-for-top-components"></a><span data-ttu-id="e28e2-258">Mesures pour les composants principaux</span><span class="sxs-lookup"><span data-stu-id="e28e2-258">Metrics for Top Components</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e28e2-259">Nom</span><span class="sxs-lookup"><span data-stu-id="e28e2-259">Name</span></span></th>
<th><span data-ttu-id="e28e2-260">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="e28e2-260">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e28e2-261">Description</span><span class="sxs-lookup"><span data-stu-id="e28e2-261">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-262"><strong>Classement</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-262"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-263">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-263">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-264">Classement relatif de sessions ayant échoué en fonction du composant Lync Server 2010 (par exemple, ExumRouting, GroupChat ou MediationServer).</span><span class="sxs-lookup"><span data-stu-id="e28e2-264">Relative ranking of failed sessions based on Lync Server 2010 component (for example, ExumRouting, GroupChat, or MediationServer).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e28e2-265"><strong>Composants principaux</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-265"><strong>Top components</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-266">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-266">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-267">Nom du composant impliqué dans la session ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="e28e2-267">Name of the component involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-268"><strong>Sessions</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-268"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-269">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-269">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-270">Nombre total de sessions ayant échoué par composant.</span><span class="sxs-lookup"><span data-stu-id="e28e2-270">Total number of failed sessions per component.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-from-users"></a><span data-ttu-id="e28e2-271">Mesures pour les utilisateurs émetteurs principaux</span><span class="sxs-lookup"><span data-stu-id="e28e2-271">Metrics for Top From Users</span></span>

<span data-ttu-id="e28e2-272">Le tableau ci-dessous liste les informations fournies dans le rapport de répartition des défaillances sur la base des utilisateurs ayant connu le plus d’échecs en essayant d’appeler quelqu’un d’autre (dénommés utilisateurs « De »).</span><span class="sxs-lookup"><span data-stu-id="e28e2-272">The following table lists the information provided in the Failure Distribution Report based on users who experienced the most failures when they tried to call someone else (known as "From" users).</span></span>

### <a name="metrics-for-top-from-users"></a><span data-ttu-id="e28e2-273">Mesures pour les utilisateurs émetteurs principaux</span><span class="sxs-lookup"><span data-stu-id="e28e2-273">Metrics for Top From Users</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e28e2-274">Nom</span><span class="sxs-lookup"><span data-stu-id="e28e2-274">Name</span></span></th>
<th><span data-ttu-id="e28e2-275">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="e28e2-275">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e28e2-276">Description</span><span class="sxs-lookup"><span data-stu-id="e28e2-276">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-277"><strong>Classement</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-277"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-278">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-278">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-279">Classement relatif des sessions ayant échoué sur la base de l’utilisateur qui a été invité à se joindre à la session.</span><span class="sxs-lookup"><span data-stu-id="e28e2-279">Relative ranking of failed sessions based on the user who was invited to join the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e28e2-280"><strong>Utilisateurs émetteurs principaux</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-280"><strong>Top from users</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-281">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-281">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-282">Adresse SIP de l’utilisateur invité à se joindre à la session.</span><span class="sxs-lookup"><span data-stu-id="e28e2-282">SIP address of the user invited to join the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-283"><strong>Sessions</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-283"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-284">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-284">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-285">Nombre total de sessions ayant échoué par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e28e2-285">Total number of failed sessions per user.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-to-users"></a><span data-ttu-id="e28e2-286">Mesures pour les utilisateurs destinataires principaux</span><span class="sxs-lookup"><span data-stu-id="e28e2-286">Metrics for Top To Users</span></span>

<span data-ttu-id="e28e2-287">Le tableau ci-dessous liste les informations fournies dans le rapport de répartition des défaillances sur la base des utilisateurs ayant connu le plus d’échecs après avoir été appelés par quelqu’un d’autre (dénommés utilisateurs « À »).</span><span class="sxs-lookup"><span data-stu-id="e28e2-287">The following table lists the information provided in the Failure Distribution Report based on the users who experienced the most failures when another user tried to call them (known as "To" users).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e28e2-288">Nom</span><span class="sxs-lookup"><span data-stu-id="e28e2-288">Name</span></span></th>
<th><span data-ttu-id="e28e2-289">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="e28e2-289">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e28e2-290">Description</span><span class="sxs-lookup"><span data-stu-id="e28e2-290">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-291"><strong>Classement</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-291"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-292">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-292">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-293">Classement relatif des sessions ayant échoué sur la base de l’utilisateur qui a initié la session.</span><span class="sxs-lookup"><span data-stu-id="e28e2-293">Relative ranking of failed sessions based on the user who initiated the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e28e2-294"><strong>Utilisateurs destinataires principaux</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-294"><strong>Top to users</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-295">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-295">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-296">Adresse SIP de l’utilisateur ayant initié la session.</span><span class="sxs-lookup"><span data-stu-id="e28e2-296">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-297"><strong>Sessions</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-297"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-298">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-298">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-299">Nombre total de sessions ayant échoué par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e28e2-299">Total number of failed sessions per user.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-user-agents"></a><span data-ttu-id="e28e2-300">Mesures pour les principaux agents d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="e28e2-300">Metrics for Top User Agents</span></span>

<span data-ttu-id="e28e2-301">Le tableau ci-dessous liste les informations fournies dans le rapport de répartition des défaillances sur la base du logiciel de point de terminaison ayant rencontré le plus d’échecs.</span><span class="sxs-lookup"><span data-stu-id="e28e2-301">The following table lists the information provided in the Failure Distribution Report based on the endpoint software that experienced the most failures.</span></span>

### <a name="metrics-for-top-user-agents"></a><span data-ttu-id="e28e2-302">Mesures pour les principaux agents d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="e28e2-302">Metrics for Top User Agents</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e28e2-303">Nom</span><span class="sxs-lookup"><span data-stu-id="e28e2-303">Name</span></span></th>
<th><span data-ttu-id="e28e2-304">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="e28e2-304">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e28e2-305">Description</span><span class="sxs-lookup"><span data-stu-id="e28e2-305">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-306"><strong>Classement</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-306"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-307">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-307">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-p115">Classement relatif des sessions ayant échoué sur la base de l’agent d’utilisateur (logiciel) impliqué dans la session. Par exemple : RTCC/4.0.0.0 Inbound Routing/4.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="e28e2-p115">Relative ranking of failed sessions based on the user agent (software) involved in the session. For example: RTCC/4.0.0.0 Inbound Routing/4.0.0.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e28e2-310"><strong>Principaux agents d’utilisateurs</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-310"><strong>Top user agents</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-311">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-311">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-312">Nom de l’agent d’utilisateur impliqué dans la session ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="e28e2-312">Name of the user agent involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e28e2-313"><strong>Sessions</strong></span><span class="sxs-lookup"><span data-stu-id="e28e2-313"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="e28e2-314">Non</span><span class="sxs-lookup"><span data-stu-id="e28e2-314">No</span></span></p></td>
<td><p><span data-ttu-id="e28e2-315">Nombre total de sessions ayant échoué par agent.</span><span class="sxs-lookup"><span data-stu-id="e28e2-315">Total number of failed sessions per user agent.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e28e2-316">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e28e2-316">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

