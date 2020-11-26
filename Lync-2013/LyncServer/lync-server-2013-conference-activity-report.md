---
title: 'Lync Server 2013 : rapport d’activité de conférence'
description: 'Lync Server 2013 : rapport d’activité de conférence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Activity Report
ms:assetid: 22ddb509-af16-4fc8-9b98-6f58caa6f37e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558627(v=OCS.15)
ms:contentKeyID: 48183618
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b7a2b23a08970defaec62b98d075ad1167527fd7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434549"
---
# <a name="conference-activity-report-in-lync-server-2013"></a><span data-ttu-id="067aa-103">Rapport d’activité de conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="067aa-103">Conference Activity Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="067aa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="067aa-104">

<span> </span></span></span>

<span data-ttu-id="067aa-105">_**Dernière modification de la rubrique :** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="067aa-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="067aa-106">Le rapport des activités de conférence vous permet de répondre facilement à des questions telles que : combien y a-t-il de conférences organisées chaque jour et à quel moments ces conférences sont-elles organisées ?</span><span class="sxs-lookup"><span data-stu-id="067aa-106">The Conference Activity Report makes it easy for you to answer questions like these: how many conferences are being held each day, and when are those conferences being held?</span></span> <span data-ttu-id="067aa-107">Ce genre d’information n’est pas seulement utile en tant que tel, il peut également permettre de résoudre des problèmes.</span><span class="sxs-lookup"><span data-stu-id="067aa-107">Information like this is useful not only in its own right, but also as a troubleshooting tool.</span></span> <span data-ttu-id="067aa-108">Par exemple, imaginons que des utilisateurs se plaignent de la lenteur du réseau en milieu de journée.</span><span class="sxs-lookup"><span data-stu-id="067aa-108">For example, suppose users are complaining that the network seems particularly slow in the middle of the day.</span></span> <span data-ttu-id="067aa-109">Un bref coup d’œil sur les rapports d’activité de conférence peut suggérer une raison possible : beaucoup plus de conférences sont prévues entre les heures de 10:00 AM et 2:00 PM à tout moment.</span><span class="sxs-lookup"><span data-stu-id="067aa-109">A quick glance at the Conference Activity reports might suggest one possible reason: far more conferences are being scheduled between the hours of 10:00 AM and 2:00 PM then at any other time.</span></span>

<span data-ttu-id="067aa-110">Si la lenteur du réseau engendre des problèmes, vous pouvez encourager les utilisateurs à replanifier certaines de leurs conférences à un moment de la journée où le trafic est moins important.</span><span class="sxs-lookup"><span data-stu-id="067aa-110">If the slow network is causing problems, you can encourage users to reschedule some of their conferences during the less-heavily trafficked times of the day.</span></span>

<div>

## <a name="accessing-the-conference-activity-report"></a><span data-ttu-id="067aa-111">Accès au rapport des activités de conférence</span><span class="sxs-lookup"><span data-stu-id="067aa-111">Accessing the Conference Activity Report</span></span>

<span data-ttu-id="067aa-112">Le rapport d’activité de conférence est accessible à partir du [rapport de synthèse de conférences dans Lync Server 2013](lync-server-2013-conference-summary-report.md) en cliquant sur l’une des mesures suivantes :</span><span class="sxs-lookup"><span data-stu-id="067aa-112">The Conference Activity Report is accessed from the [Conference Summary Report in Lync Server 2013](lync-server-2013-conference-summary-report.md) by clicking either one of the following metrics:</span></span>

  - <span data-ttu-id="067aa-113">Nombre total de conférences</span><span class="sxs-lookup"><span data-stu-id="067aa-113">Total conferences</span></span>

  - <span data-ttu-id="067aa-114">Nombre total de participants</span><span class="sxs-lookup"><span data-stu-id="067aa-114">Total participants</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-conference-activity-report"></a><span data-ttu-id="067aa-115">Utilisation optimale du rapport des activités de conférence</span><span class="sxs-lookup"><span data-stu-id="067aa-115">Making the Best Use of the Conference Activity Report</span></span>

<span data-ttu-id="067aa-p102">Par défaut, le rapport des activités de conférence indique le nombre total de conférences pour une période spécifiée (par exemple, le nombre total de conférences par jour ou le nombre total de conférences par heure pour une journée). Cependant, vous pouvez choisir d’afficher également le nombre total de participants pour cette même période ou le nombre total de minutes de participant. Pour ce faire, cliquez sur le bouton Afficher/Masquer les paramètres pour afficher les options de filtrage, puis en sélectionner une dans la liste déroulante Établir un rapport par :</span><span class="sxs-lookup"><span data-stu-id="067aa-p102">By default the Conference Activity Report shows you the total number of conferences for the specified time period (for example, the total number of conferences per day, or the total number of conferences per hour of the day). However, you can also choose to display the total number of participants for that time period or the total number of participant minutes. To do that, click the Show/Hide Parameters button to display the filtering options, and then select one of the following from the Report by dropdown list:</span></span>

  - <span data-ttu-id="067aa-119">Nombre de participants</span><span class="sxs-lookup"><span data-stu-id="067aa-119">Participant count</span></span>

  - <span data-ttu-id="067aa-120">Minutes de participant</span><span class="sxs-lookup"><span data-stu-id="067aa-120">Participant minutes</span></span>

  - <span data-ttu-id="067aa-121">Nombre de conférences</span><span class="sxs-lookup"><span data-stu-id="067aa-121">Conference count</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="067aa-122">Filtres</span><span class="sxs-lookup"><span data-stu-id="067aa-122">Filters</span></span>

<span data-ttu-id="067aa-p103">Les filtres vous offrent la possibilité de renvoyer un ensemble de données mieux ciblées ou de visualiser les données renvoyées de différentes manières. Le tableau ci-dessous dresse la liste des filtres que vous pouvez utiliser avec le rapport des activités de conférence.</span><span class="sxs-lookup"><span data-stu-id="067aa-p103">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Conference Activity Report.</span></span>

### <a name="conference-activity-report-filters"></a><span data-ttu-id="067aa-125">Filtres du rapport des activités de conférence</span><span class="sxs-lookup"><span data-stu-id="067aa-125">Conference Activity Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="067aa-126">Nom</span><span class="sxs-lookup"><span data-stu-id="067aa-126">Name</span></span></th>
<th><span data-ttu-id="067aa-127">Description</span><span class="sxs-lookup"><span data-stu-id="067aa-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="067aa-128"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="067aa-128"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="067aa-p104">Date/heure de début de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de début comme suit :</span><span class="sxs-lookup"><span data-stu-id="067aa-p104">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="067aa-131">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="067aa-131">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="067aa-p105">Si vous ne précisez aucune heure de début, le rapport commence automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="067aa-p105">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="067aa-134">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="067aa-134">7/7/2012</span></span></p>
<p><span data-ttu-id="067aa-135">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="067aa-135">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="067aa-136">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="067aa-136">7/3/2012</span></span></p>
<p><span data-ttu-id="067aa-137">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="067aa-137">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="067aa-138"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="067aa-138"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="067aa-p106">Date/heure de fin de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de fin comme suit :</span><span class="sxs-lookup"><span data-stu-id="067aa-p106">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="067aa-141">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="067aa-141">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="067aa-p107">Si vous ne précisez aucune heure de fin, le rapport se termine automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="067aa-p107">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="067aa-144">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="067aa-144">7/7/2012</span></span></p>
<p><span data-ttu-id="067aa-145">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="067aa-145">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="067aa-146">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="067aa-146">7/3/2012</span></span></p>
<p><span data-ttu-id="067aa-147">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="067aa-147">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="067aa-148"><strong>Intervalle</strong></span><span class="sxs-lookup"><span data-stu-id="067aa-148"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="067aa-p108">Intervalle de temps. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="067aa-p108">Time interval. Select any of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="067aa-151">Toutes les heures (il est possible d’afficher un maximum de 25 heures)</span><span class="sxs-lookup"><span data-stu-id="067aa-151">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="067aa-152">Tous les jours (il est possible d’afficher un maximum de 31 jours)</span><span class="sxs-lookup"><span data-stu-id="067aa-152">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="067aa-153">Toutes les semaines (il est possible d’afficher un maximum de 12 semaines)</span><span class="sxs-lookup"><span data-stu-id="067aa-153">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="067aa-154">Tous les mois (il est possible d’afficher un maximum de 12 mois)</span><span class="sxs-lookup"><span data-stu-id="067aa-154">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="067aa-155">Si la période comprise entre les dates de début et de fin dépasse le nombre maximal de valeurs autorisé pour l’intervalle sélectionné, seul le nombre maximal de valeurs (à compter de la date de début) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="067aa-155">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="067aa-156">Par exemple, si vous sélectionnez l’intervalle quotidien avec une date de début de 7/7/2012 et une date de fin de 2/28/2012, les données sont affichées pour les jours de 8/7/2012 12:00 AM à 9/7/2012 12:00 AM (c’est-à-dire un total de 31 jours de données).</span><span class="sxs-lookup"><span data-stu-id="067aa-156">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="067aa-157"><strong>Établir un rapport par</strong></span><span class="sxs-lookup"><span data-stu-id="067aa-157"><strong>Report by</strong></span></span></p></td>
<td><p><span data-ttu-id="067aa-p110">Indique les valeurs qu’il convient d’utiliser dans le rapport. Vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="067aa-p110">Indicates the values to be used in the report. You can select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="067aa-160">Nombre de participants</span><span class="sxs-lookup"><span data-stu-id="067aa-160">Participant Count</span></span></p></li>
<li><p><span data-ttu-id="067aa-161">Minutes de participant</span><span class="sxs-lookup"><span data-stu-id="067aa-161">Participant Minutes</span></span></p></li>
<li><p><span data-ttu-id="067aa-162">Nombre de conférences</span><span class="sxs-lookup"><span data-stu-id="067aa-162">Conference Count</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferences-by-pool"></a><span data-ttu-id="067aa-163">Mesure des conférences par pool</span><span class="sxs-lookup"><span data-stu-id="067aa-163">Metrics for Conferences by Pool</span></span>

<span data-ttu-id="067aa-164">Le tableau qui suit répertorie les informations dans le rapport des activités de conférence pour chaque pool.</span><span class="sxs-lookup"><span data-stu-id="067aa-164">The following table lists the information in the Conference Activity Report for each pool.</span></span>

### <a name="metrics-for-conferences-by-pool"></a><span data-ttu-id="067aa-165">Mesure des conférences par pool</span><span class="sxs-lookup"><span data-stu-id="067aa-165">Metrics for Conferences by Pool</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="067aa-166">Nom</span><span class="sxs-lookup"><span data-stu-id="067aa-166">Name</span></span></th>
<th><span data-ttu-id="067aa-167">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="067aa-167">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="067aa-168">Description</span><span class="sxs-lookup"><span data-stu-id="067aa-168">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="067aa-169"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="067aa-169"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="067aa-170">Non</span><span class="sxs-lookup"><span data-stu-id="067aa-170">No</span></span></p></td>
<td><p><span data-ttu-id="067aa-171">Nom du pool de serveurs d’inscriptions ou du serveur Edge utilisés dans la conférence.</span><span class="sxs-lookup"><span data-stu-id="067aa-171">Name of the Registrar pool or Edge Server used in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="067aa-172"><strong>Date/Heure</strong></span><span class="sxs-lookup"><span data-stu-id="067aa-172"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="067aa-173">Non</span><span class="sxs-lookup"><span data-stu-id="067aa-173">No</span></span></p></td>
<td><p><span data-ttu-id="067aa-174">Date et heure auxquelles la conférence s’est tenue.</span><span class="sxs-lookup"><span data-stu-id="067aa-174">Date and time when the conference was held.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="067aa-175"><strong>Total</strong></span><span class="sxs-lookup"><span data-stu-id="067aa-175"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="067aa-176">Non</span><span class="sxs-lookup"><span data-stu-id="067aa-176">No</span></span></p></td>
<td><p><span data-ttu-id="067aa-177">Nombre total de participants, nombre total de minutes par participant ou nombre total de conférences.</span><span class="sxs-lookup"><span data-stu-id="067aa-177">Total participant count, total participant minutes, or total conference count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferences-by-server-type"></a><span data-ttu-id="067aa-178">Mesure des conférences par type de serveur</span><span class="sxs-lookup"><span data-stu-id="067aa-178">Metrics for Conferences by Server Type</span></span>

<span data-ttu-id="067aa-179">Le tableau qui suit répertorie les informations dans le rapport des activités de conférence pour chaque type de serveur.</span><span class="sxs-lookup"><span data-stu-id="067aa-179">The following table lists the information in the Conference Activity Report for each type of server.</span></span>

### <a name="metrics-for-conferences-by-server-type"></a><span data-ttu-id="067aa-180">Mesure des conférences par type de serveur</span><span class="sxs-lookup"><span data-stu-id="067aa-180">Metrics for Conferences by Server Type</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="067aa-181">Nom</span><span class="sxs-lookup"><span data-stu-id="067aa-181">Name</span></span></th>
<th><span data-ttu-id="067aa-182">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="067aa-182">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="067aa-183">Description</span><span class="sxs-lookup"><span data-stu-id="067aa-183">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="067aa-184"><strong>Type de serveur de conférence</strong></span><span class="sxs-lookup"><span data-stu-id="067aa-184"><strong>Conferencing server type</strong></span></span></p></td>
<td><p><span data-ttu-id="067aa-185">Non</span><span class="sxs-lookup"><span data-stu-id="067aa-185">No</span></span></p></td>
<td><p><span data-ttu-id="067aa-186">Type de serveur utilisé dans la conférence, généralement l’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="067aa-186">Type of server used in the conference, typically one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="067aa-187">Serveur de conférence web</span><span class="sxs-lookup"><span data-stu-id="067aa-187">Web Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="067aa-188">Service de conférence de messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="067aa-188">IM Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="067aa-189">Service de téléconférence</span><span class="sxs-lookup"><span data-stu-id="067aa-189">Telephony Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="067aa-190">Serveur de conférence A/V</span><span class="sxs-lookup"><span data-stu-id="067aa-190">AV Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="067aa-191">Partage d’application</span><span class="sxs-lookup"><span data-stu-id="067aa-191">Application Sharing</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="067aa-192"><strong>Date/Heure</strong></span><span class="sxs-lookup"><span data-stu-id="067aa-192"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="067aa-193">Non</span><span class="sxs-lookup"><span data-stu-id="067aa-193">No</span></span></p></td>
<td><p><span data-ttu-id="067aa-194">Date et heure auxquelles la conférence s’est tenue.</span><span class="sxs-lookup"><span data-stu-id="067aa-194">Date and time when the conference was held.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="067aa-195"><strong>Total</strong></span><span class="sxs-lookup"><span data-stu-id="067aa-195"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="067aa-196">Non</span><span class="sxs-lookup"><span data-stu-id="067aa-196">No</span></span></p></td>
<td><p><span data-ttu-id="067aa-197">Nombre total de participants, nombre total de minutes par participant ou nombre total de conférences.</span><span class="sxs-lookup"><span data-stu-id="067aa-197">Total participant count, total participant minutes, or total conference count.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="067aa-198">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="067aa-198">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

