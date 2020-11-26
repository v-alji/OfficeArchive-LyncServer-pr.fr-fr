---
title: 'Lync Server 2013 : rapport de diagnostic de la Conférence'
description: 'Lync Server 2013 : rapport de diagnostic de la Conférence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Diagnostic Report
ms:assetid: e9edc23c-8ce8-4ab8-8786-9d22e1e51e14
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615042(v=OCS.15)
ms:contentKeyID: 48185901
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9d3ef3c78bc2145d907d5a40e1aed95a2f4cb4c4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434543"
---
# <a name="conference-diagnostic-report-in-lync-server-2013"></a><span data-ttu-id="27a1a-103">Rapport de diagnostic de conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27a1a-103">Conference Diagnostic Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="27a1a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="27a1a-104">

<span> </span></span></span>

<span data-ttu-id="27a1a-105">_**Dernière modification de la rubrique :** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="27a1a-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="27a1a-106">Le rapport de diagnostic de conférence fournit des informations sur la réussite ou l’échec de toutes les sessions de conférence.</span><span class="sxs-lookup"><span data-stu-id="27a1a-106">The Conference Diagnostic Report provides information about the success and failure of all conferencing sessions.</span></span> <span data-ttu-id="27a1a-107">Notez que Microsoft Lync Server distingue différentes sortes d’échecs :</span><span class="sxs-lookup"><span data-stu-id="27a1a-107">Note that Microsoft Lync Server distinguishes between different kinds of failure:</span></span>

  - <span data-ttu-id="27a1a-p102">**échec attendu**. Un échec attendu est généralement une erreur au sens technique seulement. Par exemple, supposons que quelqu’un démarre une conférence, mais raccroche avant que des personnes puissent participer. Techniquement, c’est une erreur : la conférence a été lancée, mais n’a pas été achevée. Cependant, il s’agit d’une erreur à laquelle on peut s’attendre : si l’organisateur annule la conférence avant que des personnes puissent participer, on ne s’attend pas à ce que cette conférence soit achevée.</span><span class="sxs-lookup"><span data-stu-id="27a1a-p102">**Expected failure**. An expected failure is typically a failure only in the most technical sense. For example, suppose someone starts a conference but hangs up before anyone can join. Technically that's a failure: the conference was initiated, but not completed. However, that's a failure that you would expect to happen: if the organizer cancels the conference before anyone can join then you would not expect that conference to be completed.</span></span>

  - <span data-ttu-id="27a1a-p103">**échec inattendu**. Un échec inattendu constitue exactement ce que son nom indique : une erreur à laquelle on ne s’attend pas, compte tenu des circonstances. Par exemple, supposons qu’une conférence ne puisse pas avoir lieu parce que la stratégie de réunion de l’organisateur n’a pas pu être récupérée. Il s’agit d’une erreur inattendue : la stratégie de réunion d’un utilisateur doit toujours pouvoir être récupérée.</span><span class="sxs-lookup"><span data-stu-id="27a1a-p103">**Unexpected failure**. An unexpected error is exactly what the name implies: an error that, based on the circumstances, you would not expect to occur. For example, suppose a conference could not be held because the organizer's meeting policy could not be retrieved. That's an unexpected error: after all, you should always be able to retrieve a user's meeting policy.</span></span>

<span data-ttu-id="27a1a-p104">Notez que les mesures de Réussite, d’Échec attendu et d’Échec inattendu peuvent ne pas être comptabilisées dans la mesure Nombre total de sessions. Par exemple, vous pouvez voir les valeurs suivantes dans le rapport :</span><span class="sxs-lookup"><span data-stu-id="27a1a-p104">Note that the Success, Expected failure, and Unexpected failure metrics might not add up to the Total sessions metric. For example, you might see the following values in the Report:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="27a1a-119">Réussites</span><span class="sxs-lookup"><span data-stu-id="27a1a-119">Successes</span></span></th>
<th><span data-ttu-id="27a1a-120">Échecs attendus</span><span class="sxs-lookup"><span data-stu-id="27a1a-120">Expected failures</span></span></th>
<th><span data-ttu-id="27a1a-121">Échecs inattendus</span><span class="sxs-lookup"><span data-stu-id="27a1a-121">Unexpected failures</span></span></th>
<th><span data-ttu-id="27a1a-122">Nombre total de sessions</span><span class="sxs-lookup"><span data-stu-id="27a1a-122">Total sessions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27a1a-123">2024</span><span class="sxs-lookup"><span data-stu-id="27a1a-123">2024</span></span></p></td>
<td><p><span data-ttu-id="27a1a-124">469</span><span class="sxs-lookup"><span data-stu-id="27a1a-124">469</span></span></p></td>
<td><p><span data-ttu-id="27a1a-125">Seiz</span><span class="sxs-lookup"><span data-stu-id="27a1a-125">16</span></span></p></td>
<td><p><span data-ttu-id="27a1a-126">2521</span><span class="sxs-lookup"><span data-stu-id="27a1a-126">2521</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="27a1a-127">Si vous ajoutez 2 024 + 469 + 16, vous obtenez un total de 2 509 sessions alors que la colonne Nombre total de sessions indique 2 521 sessions.</span><span class="sxs-lookup"><span data-stu-id="27a1a-127">If you add 2024 + 469 + 16 you get a total of 2,509 sessions and yet, the Total sessions column shows a total of 2,521 sessions.</span></span> <span data-ttu-id="27a1a-128">Les 12 sessions « manquantes » sont celles que le système n’a pas pu catégoriser comme réussies ou non.</span><span class="sxs-lookup"><span data-stu-id="27a1a-128">The "missing" 12 sessions for are sessions that the system was unable to categorize as successful or unsuccessful.</span></span> <span data-ttu-id="27a1a-129">Ce peut arriver parfois quand un produit tiers introduit un nouveau code de diagnostic qui n’est pas connu de surveiller le serveur.</span><span class="sxs-lookup"><span data-stu-id="27a1a-129">That will sometimes be the case when a third-party product introduces a new diagnostic code that is unfamiliar to Monitoring Server.</span></span> <span data-ttu-id="27a1a-130">Dans ce cas, les appels effectués à l’aide de ce produit et reportant ce code de diagnostic ne peuvent pas toujours être catégorisés en tant que réussite, échec attendu ou échec inattendu.</span><span class="sxs-lookup"><span data-stu-id="27a1a-130">When that happens, calls made using that product, and reporting that diagnostic code, cannot always be categorized as being a Success, an Expected failure, or an Unexpected failure.</span></span>

<div>

## <a name="accessing-the-conference-diagnostic-report"></a><span data-ttu-id="27a1a-131">Accès au rapport de diagnostic de conférence</span><span class="sxs-lookup"><span data-stu-id="27a1a-131">Accessing the Conference Diagnostic Report</span></span>

<span data-ttu-id="27a1a-132">Le rapport des de diagnostic de conférence est accessible à partir de la page d’accueil des Rapports de suivi.</span><span class="sxs-lookup"><span data-stu-id="27a1a-132">The Conference Diagnostic Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="27a1a-133">Vous pouvez accéder au [rapport de distribution des échecs dans Lync Server 2013](lync-server-2013-failure-distribution-report.md) en cliquant sur l’une des mesures suivantes :</span><span class="sxs-lookup"><span data-stu-id="27a1a-133">You can access the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="27a1a-134">Nombre d’échecs inattendus</span><span class="sxs-lookup"><span data-stu-id="27a1a-134">Unexpected failure volume</span></span>

  - <span data-ttu-id="27a1a-135">Nombre d’échecs attendus</span><span class="sxs-lookup"><span data-stu-id="27a1a-135">Expected failure volume</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-conference-diagnostic-report"></a><span data-ttu-id="27a1a-136">Utilisation optimale du rapport de diagnostic de conférence</span><span class="sxs-lookup"><span data-stu-id="27a1a-136">Making the Best Use of the Conference Diagnostic Report</span></span>

<span data-ttu-id="27a1a-137">Le rapport de diagnostic de conférence inclut une série de graphiques.</span><span class="sxs-lookup"><span data-stu-id="27a1a-137">The Conference Diagnostic Report includes a series of graphs.</span></span> <span data-ttu-id="27a1a-138">Chaque colonne de graphique constitue un lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="27a1a-138">Each of the columns shown in the graph is actually a hyperlink.</span></span> <span data-ttu-id="27a1a-139">Si vous cliquez sur une colonne, vous accédez au rapport de [distribution des échecs dans Lync Server 2013](lync-server-2013-failure-distribution-report.md) pour cette période et ce type de conférence.</span><span class="sxs-lookup"><span data-stu-id="27a1a-139">If you click a column, you'll drill down to the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md) for that time period and that conference type.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="27a1a-140">Filtres</span><span class="sxs-lookup"><span data-stu-id="27a1a-140">Filters</span></span>

<span data-ttu-id="27a1a-p108">Les filtres vous offrent la possibilité de renvoyer un ensemble de données mieux ciblées ou de visualiser les données renvoyées de différentes manières. Par exemple, le rapport de diagnostic de conférence vous permet de filtrer les éléments tels que le type de conférence mené (par exemple, une conférence Focus) pour le serveur Edge utilisé dans la conférence. Vous pouvez également choisir le mode de groupement des données. Dans ce cas, les conférences sont groupées par heure, jour, semaine ou mois.</span><span class="sxs-lookup"><span data-stu-id="27a1a-p108">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Conference Diagnostic Report enables you to filter on such things as the type of conference being conducted (for example, a Focus-based conference) or by the Edge Server used in the conference. You can also choose how data should be grouped. In this case, conferences are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="27a1a-145">Le tableau qui suit dresse la liste des filtres que vous pouvez utiliser avec le rapport de diagnostic de conférence.</span><span class="sxs-lookup"><span data-stu-id="27a1a-145">The following table lists the filters that you can use with the Conference Diagnostic Report.</span></span>

### <a name="conference-diagnostic-report-filters"></a><span data-ttu-id="27a1a-146">Filtres du rapport de diagnostic de conférence</span><span class="sxs-lookup"><span data-stu-id="27a1a-146">Conference Diagnostic Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="27a1a-147">Nom</span><span class="sxs-lookup"><span data-stu-id="27a1a-147">Name</span></span></th>
<th><span data-ttu-id="27a1a-148">Description</span><span class="sxs-lookup"><span data-stu-id="27a1a-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27a1a-149"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="27a1a-149"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="27a1a-p109">Date/heure de début de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de début comme suit :</span><span class="sxs-lookup"><span data-stu-id="27a1a-p109">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="27a1a-152">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="27a1a-152">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="27a1a-p110">Si vous ne précisez aucune heure de début, le rapport commence automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="27a1a-p110">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="27a1a-155">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="27a1a-155">7/7/2012</span></span></p>
<p><span data-ttu-id="27a1a-156">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="27a1a-156">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="27a1a-157">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="27a1a-157">7/3/2012</span></span></p>
<p><span data-ttu-id="27a1a-158">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="27a1a-158">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27a1a-159"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="27a1a-159"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="27a1a-p111">Date/heure de fin de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de fin comme suit :</span><span class="sxs-lookup"><span data-stu-id="27a1a-p111">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="27a1a-162">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="27a1a-162">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="27a1a-p112">Si vous ne précisez aucune heure de fin, le rapport se termine automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="27a1a-p112">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="27a1a-165">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="27a1a-165">7/7/2012</span></span></p>
<p><span data-ttu-id="27a1a-166">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="27a1a-166">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="27a1a-167">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="27a1a-167">7/3/2012</span></span></p>
<p><span data-ttu-id="27a1a-168">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="27a1a-168">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27a1a-169"><strong>Intervalle</strong></span><span class="sxs-lookup"><span data-stu-id="27a1a-169"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="27a1a-p113">Intervalle de temps. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="27a1a-p113">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="27a1a-172">Toutes les heures (il est possible d’afficher un maximum de 25 heures)</span><span class="sxs-lookup"><span data-stu-id="27a1a-172">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="27a1a-173">Tous les jours (il est possible d’afficher un maximum de 31 jours)</span><span class="sxs-lookup"><span data-stu-id="27a1a-173">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="27a1a-174">Toutes les semaines (il est possible d’afficher un maximum de 12 semaines)</span><span class="sxs-lookup"><span data-stu-id="27a1a-174">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="27a1a-175">Tous les mois (il est possible d’afficher un maximum de 12 mois)</span><span class="sxs-lookup"><span data-stu-id="27a1a-175">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="27a1a-176">Si la période comprise entre les dates de début et de fin dépasse le nombre maximal de valeurs autorisé pour l’intervalle sélectionné, seul le nombre maximal de valeurs (à compter de la date de début) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="27a1a-176">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="27a1a-177">Par exemple, si vous sélectionnez l’intervalle quotidien avec une date de début de 7/7/2012 et une date de fin de 2/28/2012, les données sont affichées pour les jours de 8/7/2012 12:00 AM à 9/7/2012 12:00 AM (c’est-à-dire un total de 31 jours de données).</span><span class="sxs-lookup"><span data-stu-id="27a1a-177">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27a1a-178"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="27a1a-178"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="27a1a-p115">Nom de domaine complet (FQDN) du pool de serveurs d’inscriptions. Vous pouvez soit sélectionner un pool particulier, soit cliquer sur <strong>[Tous]</strong> pour afficher les données de tous les pools. Cette liste déroulante se renseigne automatiquement en fonction des enregistrements que contient la base de données.</span><span class="sxs-lookup"><span data-stu-id="27a1a-p115">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27a1a-182"><strong>Sessions de conférence</strong></span><span class="sxs-lookup"><span data-stu-id="27a1a-182"><strong>Conference sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="27a1a-p116">Indique le type de session de conférence. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="27a1a-p116">Indicates the type of conferencing session. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="27a1a-185">[Tous]</span><span class="sxs-lookup"><span data-stu-id="27a1a-185">[All]</span></span></p></li>
<li><p><span data-ttu-id="27a1a-186">Sessions Focus</span><span class="sxs-lookup"><span data-stu-id="27a1a-186">Focus sessions</span></span></p></li>
<li><p><span data-ttu-id="27a1a-187">Toutes les sessions MCU</span><span class="sxs-lookup"><span data-stu-id="27a1a-187">All MCU sessions</span></span></p></li>
<li><p><span data-ttu-id="27a1a-188">Conférence par messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="27a1a-188">IM conferencing</span></span></p></li>
<li><p><span data-ttu-id="27a1a-189">Partage d’application</span><span class="sxs-lookup"><span data-stu-id="27a1a-189">Application sharing</span></span></p></li>
<li><p><span data-ttu-id="27a1a-190">Conférence A/V</span><span class="sxs-lookup"><span data-stu-id="27a1a-190">A/V conferencing</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="27a1a-191">Mesures</span><span class="sxs-lookup"><span data-stu-id="27a1a-191">Metrics</span></span>

<span data-ttu-id="27a1a-192">Le tableau qui suit répertorie les informations fournies dans le rapport de diagnostic de conférence pour chaque type de session de conférence.</span><span class="sxs-lookup"><span data-stu-id="27a1a-192">The following table lists the information provided in the Conference Diagnostic Report for each type of conferencing session.</span></span>

### <a name="conference-diagnostic-report-metrics"></a><span data-ttu-id="27a1a-193">Mesures du rapport de diagnostic de conférence</span><span class="sxs-lookup"><span data-stu-id="27a1a-193">Conference Diagnostic Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="27a1a-194">Nom</span><span class="sxs-lookup"><span data-stu-id="27a1a-194">Name</span></span></th>
<th><span data-ttu-id="27a1a-195">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="27a1a-195">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="27a1a-196">Description</span><span class="sxs-lookup"><span data-stu-id="27a1a-196">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27a1a-197"><strong>Nombre de réussites</strong></span><span class="sxs-lookup"><span data-stu-id="27a1a-197"><strong>Success volume</strong></span></span></p></td>
<td><p><span data-ttu-id="27a1a-198">Non</span><span class="sxs-lookup"><span data-stu-id="27a1a-198">No</span></span></p></td>
<td><p><span data-ttu-id="27a1a-199">Nombre total de conférences réussies.</span><span class="sxs-lookup"><span data-stu-id="27a1a-199">Total number of successful conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27a1a-200"><strong>Pourcentage de réussite</strong></span><span class="sxs-lookup"><span data-stu-id="27a1a-200"><strong>Success percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="27a1a-201">Non</span><span class="sxs-lookup"><span data-stu-id="27a1a-201">No</span></span></p></td>
<td><p><span data-ttu-id="27a1a-p117">Pourcentage de conférences qui se sont déroulées sans problème majeur. Calculé en divisant le nombre de réussites par le nombre total de sessions.</span><span class="sxs-lookup"><span data-stu-id="27a1a-p117">Percentage of conferences that completed with significant problems. Calculated by dividing the Success volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27a1a-204"><strong>Nombre d’échecs attendus</strong></span><span class="sxs-lookup"><span data-stu-id="27a1a-204"><strong>Expected failure volume</strong></span></span></p></td>
<td><p><span data-ttu-id="27a1a-205">Non</span><span class="sxs-lookup"><span data-stu-id="27a1a-205">No</span></span></p></td>
<td><p><span data-ttu-id="27a1a-206">Nombre total de conférences pour lesquelles un &quot; échec inattendu &quot; s’est produit.</span><span class="sxs-lookup"><span data-stu-id="27a1a-206">Total number of conferences where an &quot;expected failure&quot; occurred.</span></span></p>
<p><span data-ttu-id="27a1a-p118">Un échec attendu est un échec auquel il faut s’attendre. Par exemple, si un utilisateur a défini son statut sur Ne pas déranger, il faut s’attendre à ce que tout appel émis vers cet utilisateur échoue.</span><span class="sxs-lookup"><span data-stu-id="27a1a-p118">An expected failure is a failure that is expected to happen. For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27a1a-209"><strong>Pourcentage d’échec attendu</strong></span><span class="sxs-lookup"><span data-stu-id="27a1a-209"><strong>Expected failure percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="27a1a-210">Non</span><span class="sxs-lookup"><span data-stu-id="27a1a-210">No</span></span></p></td>
<td><p><span data-ttu-id="27a1a-p119">Pourcentage de conférences qui ont rencontré une erreur attendue. Calculé en divisant le nombre d’échecs attendus par le nombre total de sessions.</span><span class="sxs-lookup"><span data-stu-id="27a1a-p119">Percentage of conferences that experienced an expected error. Calculated by dividing the Expected failure volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27a1a-213"><strong>Nombre d’échecs inattendus</strong></span><span class="sxs-lookup"><span data-stu-id="27a1a-213"><strong>Unexpected failure volume</strong></span></span></p></td>
<td><p><span data-ttu-id="27a1a-214">Non</span><span class="sxs-lookup"><span data-stu-id="27a1a-214">No</span></span></p></td>
<td><p><span data-ttu-id="27a1a-215">Nombre total de conférences pour lesquelles un &quot; échec inattendu &quot; s’est produit.</span><span class="sxs-lookup"><span data-stu-id="27a1a-215">Total number of conferences where an &quot;unexpected failure&quot; occurred.</span></span></p>
<p><span data-ttu-id="27a1a-p120">Un échec inattendu est un échec qui se produit alors que le système semble intègre. Par exemple, un appel ne doit pas être coupé si l’appelant est mis en attente. Dans le cas contraire, ce problème est considéré comme un échec inattendu.</span><span class="sxs-lookup"><span data-stu-id="27a1a-p120">An unexpected failure is a failure that occurs in what would appear to be an otherwise healthy system. For example, a call should not be terminated if the caller is placed on hold. If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27a1a-219"><strong>Pourcentage d’échec inattendu</strong></span><span class="sxs-lookup"><span data-stu-id="27a1a-219"><strong>Unexpected failure percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="27a1a-220">Non</span><span class="sxs-lookup"><span data-stu-id="27a1a-220">No</span></span></p></td>
<td><p><span data-ttu-id="27a1a-p121">Pourcentage de conférences qui ont rencontré une erreur inattendue. Calculé en divisant le nombre d’échecs inattendus par le nombre total de sessions.</span><span class="sxs-lookup"><span data-stu-id="27a1a-p121">Percentage of conferences that experienced an unexpected error. Calculated by dividing the Unexpected failure volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27a1a-223"><strong>Nombre total de sessions</strong></span><span class="sxs-lookup"><span data-stu-id="27a1a-223"><strong>Total sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="27a1a-224">Non</span><span class="sxs-lookup"><span data-stu-id="27a1a-224">No</span></span></p></td>
<td><p><span data-ttu-id="27a1a-225">Nombre total de conférences, incluant les conférences qui ont réussi et celles qui ont échoué (à la fois les échecs attendus et les échecs inattendus), ainsi que les conférences qui n’appartiennent à aucune catégorie.</span><span class="sxs-lookup"><span data-stu-id="27a1a-225">Total number of conferences, including successful conferences, failed conferences (both expected failures and unexpected failures), and uncategorized conferences.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="27a1a-226">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="27a1a-226">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

