---
title: 'Lync Server 2013 : rapport de synthèse des conférences RTC'
description: 'Lync Server 2013 : rapport de synthèse des conférences RTC.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN Conference Summary Report
ms:assetid: 8e2f0862-4dfa-4c2b-bf8d-ad71419f15d2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615014(v=OCS.15)
ms:contentKeyID: 48184764
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c3bc468e494577c229562a1cb7cfddaf839f946f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436726"
---
# <a name="pstn-conference-summary-report-in-lync-server-2013"></a><span data-ttu-id="bf602-103">Rapport de synthèse des conférences RTC dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf602-103">PSTN Conference Summary Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bf602-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bf602-104">

<span> </span></span></span>

<span data-ttu-id="bf602-105">_**Dernière modification de la rubrique :** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="bf602-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="bf602-106">Dans Microsoft Lync Server 2013, une conférence RTC est une conférence dans laquelle au moins un participant compose un numéro de téléphone à l’aide d’un téléphone RTC (réseau téléphonique commuté).</span><span class="sxs-lookup"><span data-stu-id="bf602-106">In Microsoft Lync Server 2013, a PSTN conference is any conference in which at least one participant dials in to the audio portion by a using a PSTN (public switched telephone network) phone.</span></span> <span data-ttu-id="bf602-107">(Un téléphone RTC est un téléphone mobile, un téléphone mobile ou un autre téléphone qui n’utilise pas le protocole voix sur IP.) Même s’il est appelé conférences RTC dans les rapports de surveillance, ces conférences peuvent être plus fréquemment appelées conférences rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="bf602-107">(A PSTN phone is a "landline," a cell phone, or any other phone which does not make use of Voice over IP.) Although referred to as PSTN conferences in the Monitoring Reports, these conferences are perhaps more-commonly known as dial-in conferences.</span></span>

<span data-ttu-id="bf602-p102">Le rapport de synthèse de conférence RTC fournit des informations sur toutes les conférences RTC qui ont lieu au sein de votre organisation (c’est-à-dire, toutes les conférences comportant au moins un utilisateur connecté). Ce rapport comprend des informations sur le nombre total de conférences RTC, le nombre total de personnes ayant participé à ces conférences, et, peut-être plus important, le nombre total d’utilisateurs connectés (la mesure Nombre total de participants RTC).</span><span class="sxs-lookup"><span data-stu-id="bf602-p102">The PSTN Conference Summary Report provides information about all the PSTN conferences held in your organization (that is, all the conferences that had at least one dial-in user). The report includes information about the total number of PSTN conferences, the total number of people who participated in those conferences, and, perhaps, most important, the total number of dial-in users (the Total PSTN participants metric).</span></span>

<div>

## <a name="accessing-the-pstn-conference-summary-report"></a><span data-ttu-id="bf602-110">Accès au rapport de synthèse de conférence RTC</span><span class="sxs-lookup"><span data-stu-id="bf602-110">Accessing the PSTN Conference Summary Report</span></span>

<span data-ttu-id="bf602-p103">Le rapport de synthèse de conférence RTC est accessible uniquement à partir de la page d’accueil Rapports de surveillance. Ce rapport n’est lié à aucun autre rapport. Vous ne pouvez pas obtenir d’informations détaillées sur les appels pour une conférence RTC, en partie parce que les points de terminaison individuels sont responsables de l’envoi de ces informations. Les téléphones RTC ne sont pas capables d’effectuer le suivi ou d’envoyer des informations détaillées sur les appels.</span><span class="sxs-lookup"><span data-stu-id="bf602-p103">The PSTN Conference Summary Report can only be accessed from the Monitoring Reports home page. This report is not linked to any other reports. Note that you cannot retrieve detailed call information for a PSTN conference, in part because individual endpoints are responsible for submitting this information. PSTN phones are not capable of tracking or submitting call detail information.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-pstn-conference-summary-report"></a><span data-ttu-id="bf602-115">Utilisation efficace du rapport de synthèse de conférence RTC</span><span class="sxs-lookup"><span data-stu-id="bf602-115">Making the Best Use of the PSTN Conference Summary Report</span></span>

<span data-ttu-id="bf602-116">Pour déterminer le pourcentage de toutes vos conférences qui incluent des utilisateurs rendez-vous, comparez la valeur de la métrique du total des conférences RTC avec la mesure du total des conférences trouvées dans le [rapport récapitulatif de la Conférence dans Lync Server 2013](lync-server-2013-conference-summary-report.md).</span><span class="sxs-lookup"><span data-stu-id="bf602-116">To determine the percentage of all your conferences that include dial-in users, compare the value of the Total PSTN conferences metric with the Total conferences metric found on the [Conference Summary Report in Lync Server 2013](lync-server-2013-conference-summary-report.md).</span></span>

<span data-ttu-id="bf602-117">Si les conférences RTC que vous vous attendiez à voir ne s’affichent pas, n’oubliez pas que la possibilité d’organiser une conférence qui autorise les utilisateurs connectés dépend de la stratégie de conférence affectée à un utilisateur : si peu d’utilisateurs sont autorisés à organiser des conférences RTC, vous verrez peu de conférences RTC.</span><span class="sxs-lookup"><span data-stu-id="bf602-117">If you don't see as many PSTN conferences as you might have expected to see, keep in mind that the ability to organize a conference that allows dial-in users depends on the conferencing policy that has been assigned to a user: if very few of your users are allowed to hold PSTN conferences you would obviously see very few PSTN conferences.</span></span> <span data-ttu-id="bf602-118">Vous pouvez rapidement vérifier les stratégies de conférence (le cas échéant) permettre aux utilisateurs de planifier des conférences RTC en exécutant la commande suivante à partir de Lync Server Management Shell :</span><span class="sxs-lookup"><span data-stu-id="bf602-118">You can quickly verify which of your conferencing policies (if any) allow users to schedule PSTN conferences by running the following command from within the Lync Server Management Shell:</span></span>

    Get-CsConferencingPolicy | Select-Object Identity, EnableDialInConferencing

<span data-ttu-id="bf602-119">Des données semblables à ceci sont renvoyées :</span><span class="sxs-lookup"><span data-stu-id="bf602-119">That will return data similar to this:</span></span>

    Identity                                EnableDialInConferencing
    --------                                ------------------------
    Global                                                      True
    site:Redmond                                               False
    site:Dublin                                                False
    Tag:RedmondDialInUsers                                      True
    Tag:DublinDialInUsers                                       True

<span data-ttu-id="bf602-120">Des données semblables à ceci sont renvoyées :</span><span class="sxs-lookup"><span data-stu-id="bf602-120">That will return data similar to this:</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="bf602-121">Filtres</span><span class="sxs-lookup"><span data-stu-id="bf602-121">Filters</span></span>

<span data-ttu-id="bf602-122">Les filtres vous offrent la possibilité de renvoyer un ensemble de données mieux ciblées ou de visualiser les données renvoyées de différentes manières.</span><span class="sxs-lookup"><span data-stu-id="bf602-122">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways.</span></span> <span data-ttu-id="bf602-123">Par exemple, le rapport de synthèse des conférences RTC vous permet de choisir la façon dont les données doivent être groupées.</span><span class="sxs-lookup"><span data-stu-id="bf602-123">For example, the PSTN Conference Summary Report enables you to choose how data should be grouped.</span></span> <span data-ttu-id="bf602-124">Dans ce cas, les conférences sont groupées par heure, jour, semaine ou mois.</span><span class="sxs-lookup"><span data-stu-id="bf602-124">In this case, conferences are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="bf602-125">Le tableau qui suit dresse la liste des filtres que vous pouvez utiliser avec le rapport de synthèse des conférences RTC.</span><span class="sxs-lookup"><span data-stu-id="bf602-125">The following table lists the filters that you can use with the PSTN Conference Summary Report.</span></span>

### <a name="pstn-conference-summary-report-filters"></a><span data-ttu-id="bf602-126">Filtres du rapport de synthèse des conférences RTC</span><span class="sxs-lookup"><span data-stu-id="bf602-126">PSTN Conference Summary Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf602-127">Nom</span><span class="sxs-lookup"><span data-stu-id="bf602-127">Name</span></span></th>
<th><span data-ttu-id="bf602-128">Description</span><span class="sxs-lookup"><span data-stu-id="bf602-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf602-129"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="bf602-129"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="bf602-p106">Date/heure de début de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de début comme suit :</span><span class="sxs-lookup"><span data-stu-id="bf602-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="bf602-132">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="bf602-132">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="bf602-p107">Si vous ne précisez aucune heure de début, le rapport commence automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="bf602-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="bf602-135">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="bf602-135">7/7/2012</span></span></p>
<p><span data-ttu-id="bf602-136">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="bf602-136">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="bf602-137">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="bf602-137">7/3/2012</span></span></p>
<p><span data-ttu-id="bf602-138">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="bf602-138">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf602-139"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="bf602-139"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="bf602-p108">Date/heure de fin de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de fin comme suit :</span><span class="sxs-lookup"><span data-stu-id="bf602-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="bf602-142">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="bf602-142">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="bf602-p109">Si vous ne précisez aucune heure de fin, le rapport se termine automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="bf602-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="bf602-145">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="bf602-145">7/7/2012</span></span></p>
<p><span data-ttu-id="bf602-146">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="bf602-146">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="bf602-147">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="bf602-147">7/3/2012</span></span></p>
<p><span data-ttu-id="bf602-148">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="bf602-148">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf602-149"><strong>Intervalle</strong></span><span class="sxs-lookup"><span data-stu-id="bf602-149"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="bf602-p110">Intervalle de temps. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="bf602-p110">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="bf602-152">Toutes les heures (il est possible d’afficher un maximum de 25 heures)</span><span class="sxs-lookup"><span data-stu-id="bf602-152">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="bf602-153">Tous les jours (il est possible d’afficher un maximum de 31 jours)</span><span class="sxs-lookup"><span data-stu-id="bf602-153">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="bf602-154">Toutes les semaines (il est possible d’afficher un maximum de 12 semaines)</span><span class="sxs-lookup"><span data-stu-id="bf602-154">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="bf602-155">Tous les mois (il est possible d’afficher un maximum de 12 mois)</span><span class="sxs-lookup"><span data-stu-id="bf602-155">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="bf602-156">Si la période comprise entre les dates de début et de fin dépasse le nombre maximal de valeurs autorisé pour l’intervalle sélectionné, seul le nombre maximal de valeurs (à compter de la date de début) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="bf602-156">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="bf602-157">Par exemple, si vous sélectionnez l’intervalle quotidien avec une date de début de 7/7/2012 et une date de fin de 2/28/2012, les données sont affichées pour les jours de 8/7/2012 12:00 AM à 9/7/2012 12:00 AM (c’est-à-dire un total de 31 jours de données).</span><span class="sxs-lookup"><span data-stu-id="bf602-157">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="bf602-158">Mesures</span><span class="sxs-lookup"><span data-stu-id="bf602-158">Metrics</span></span>

<span data-ttu-id="bf602-159">Le tableau qui suit répertorie les informations fournies dans le rapport de synthèse des conférences RTC</span><span class="sxs-lookup"><span data-stu-id="bf602-159">The following table lists the information in the PSTN Conference Summary Report.</span></span>

### <a name="pstn-conference-summary-report-metrics"></a><span data-ttu-id="bf602-160">Mesures du rapport de synthèse des conférences RTC</span><span class="sxs-lookup"><span data-stu-id="bf602-160">PSTN Conference Summary Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf602-161">Nom</span><span class="sxs-lookup"><span data-stu-id="bf602-161">Name</span></span></th>
<th><span data-ttu-id="bf602-162">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="bf602-162">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="bf602-163">Description</span><span class="sxs-lookup"><span data-stu-id="bf602-163">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf602-164"><strong>Toutes les heures</strong></span><span class="sxs-lookup"><span data-stu-id="bf602-164"><strong>Hourly</strong></span></span></p>
<p><span data-ttu-id="bf602-165"><strong>Jour</strong></span><span class="sxs-lookup"><span data-stu-id="bf602-165"><strong>Daily</strong></span></span></p>
<p><span data-ttu-id="bf602-166"><strong>Toutes les semaines</strong></span><span class="sxs-lookup"><span data-stu-id="bf602-166"><strong>Weekly</strong></span></span></p>
<p><span data-ttu-id="bf602-167"><strong>Mois</strong></span><span class="sxs-lookup"><span data-stu-id="bf602-167"><strong>Monthly</strong></span></span></p></td>
<td><p><span data-ttu-id="bf602-168">Non</span><span class="sxs-lookup"><span data-stu-id="bf602-168">No</span></span></p></td>
<td><p><span data-ttu-id="bf602-169">Indique l’intervalle de temps sélectionné.</span><span class="sxs-lookup"><span data-stu-id="bf602-169">Indicates the selected time interval.</span></span> <span data-ttu-id="bf602-170">Le cas échéant, vous pouvez cliquer sur un intervalle de temps donné pour afficher des informations détaillées pour cet intervalle.</span><span class="sxs-lookup"><span data-stu-id="bf602-170">Where applicable, you can click a given time interval to view detailed information for that interval.</span></span> <span data-ttu-id="bf602-171">Par exemple, si vous utilisez l’intervalle quotidien et que vous cliquez sur 7/7/2012, vous pouvez voir une répartition horaire de l’activité d’inscription des utilisateurs à cette date.</span><span class="sxs-lookup"><span data-stu-id="bf602-171">For example, if you are using the Daily interval and you click 7/7/2012, you see an hourly breakdown of user registration activity for that date.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf602-172"><strong>Nombre total de conférences RTC</strong></span><span class="sxs-lookup"><span data-stu-id="bf602-172"><strong>Total PSTN conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="bf602-173">Non</span><span class="sxs-lookup"><span data-stu-id="bf602-173">No</span></span></p></td>
<td><p><span data-ttu-id="bf602-174">Nombre total de conférences ayant autorisé l’accès de rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="bf602-174">Total number conferences that allowed dial-in access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf602-175"><strong>Nombre total de participants</strong></span><span class="sxs-lookup"><span data-stu-id="bf602-175"><strong>Total participants</strong></span></span></p></td>
<td><p><span data-ttu-id="bf602-176">Non</span><span class="sxs-lookup"><span data-stu-id="bf602-176">No</span></span></p></td>
<td><p><span data-ttu-id="bf602-177">Nombre total de personnes ayant participé à des conférences ayant autorisé l’accès de rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="bf602-177">Total number of people who participated in conferences that allowed dial-in access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf602-178"><strong>Nombre total de minutes par conférence A/V</strong></span><span class="sxs-lookup"><span data-stu-id="bf602-178"><strong>Total A/V conference minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="bf602-179">Non</span><span class="sxs-lookup"><span data-stu-id="bf602-179">No</span></span></p></td>
<td><p><span data-ttu-id="bf602-180">Durée totale de conférence audio/vidéo.</span><span class="sxs-lookup"><span data-stu-id="bf602-180">Total amount of audio/visual conference time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf602-181"><strong>Nombre total de minutes par participant à la conférence A/V</strong></span><span class="sxs-lookup"><span data-stu-id="bf602-181"><strong>Total A/V conference participant minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="bf602-182">Non</span><span class="sxs-lookup"><span data-stu-id="bf602-182">No</span></span></p></td>
<td><p><span data-ttu-id="bf602-p113">Durée totale de participants audio/vidéo. Par exemple, si un participant a passé cinq minutes dans une conférence A/V et qu’un autre participant a passé trois minutes dans la même conférence, la durée totale de participants de conférences A/V sera de huit minutes.</span><span class="sxs-lookup"><span data-stu-id="bf602-p113">Total amount of audio/visual participant time. For example, if one participant spent five minutes in an A/V conference and another participant spent three minutes in the same conference, the total A/V conference participant time would be eight minutes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf602-185"><strong>Nombre total de participants RTC</strong></span><span class="sxs-lookup"><span data-stu-id="bf602-185"><strong>Total PSTN participants</strong></span></span></p></td>
<td><p><span data-ttu-id="bf602-186">Non</span><span class="sxs-lookup"><span data-stu-id="bf602-186">No</span></span></p></td>
<td><p><span data-ttu-id="bf602-187">Nombre total d’utilisateurs qui se sont connectés à des conférences ayant autorisé l’accès de rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="bf602-187">Total number of users who dialed in to conferences that allowed dial-in access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf602-188"><strong>Nombre total de minutes par participant RTC</strong></span><span class="sxs-lookup"><span data-stu-id="bf602-188"><strong>Total PSTN participant minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="bf602-189">Non</span><span class="sxs-lookup"><span data-stu-id="bf602-189">No</span></span></p></td>
<td><p><span data-ttu-id="bf602-p114">Durée totale de conférence passée par les utilisateurs de rendez-vous. Par exemple, si un participant de rendez-vous a passé cinq minutes dans une conférence et qu’un autre participant a passé trois minutes dans la même conférence, la durée totale de participants RTC sera de huit minutes.</span><span class="sxs-lookup"><span data-stu-id="bf602-p114">Total amount of conference time spent by dial-in users. For example, if one dial-in participant spent five minutes in a conference and another participant spent three minutes in the same conference, the total PSTN participant time would be eight minutes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf602-192"><strong>Organisateurs de conférence uniques</strong></span><span class="sxs-lookup"><span data-stu-id="bf602-192"><strong>Unique conference organizers</strong></span></span></p></td>
<td><p><span data-ttu-id="bf602-193">Non</span><span class="sxs-lookup"><span data-stu-id="bf602-193">No</span></span></p></td>
<td><p><span data-ttu-id="bf602-p115">Nombre total d’utilisateurs qui ont organisé au moins une conférence ayant autorisé l’accès de rendez-vous. Les utilisateurs qui ont organisé plusieurs conférences sont comptabilisés comme un organisateur unique, tout comme les utilisateurs ayant organisé une seule conférence.</span><span class="sxs-lookup"><span data-stu-id="bf602-p115">Total number of users who organized at least one conference that allowed dial-in access. Users who organized more than one conference are counted as one unique organizer, just like users who only organized a single conference.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="bf602-196">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bf602-196">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

