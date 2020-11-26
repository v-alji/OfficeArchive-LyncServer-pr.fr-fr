---
title: 'Lync Server 2013 : rapport de synthèse des conférences'
description: 'Lync Server 2013 : rapport de synthèse des conférences.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Summary Report
ms:assetid: 62f54812-5700-45a3-8526-8f58b0f77fbc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558656(v=OCS.15)
ms:contentKeyID: 48184299
ms.date: 09/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2d9c0b8ad7280d2c7336282c14f46e6b5d6a1aec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434493"
---
# <a name="conference-summary-report-in-lync-server-2013"></a><span data-ttu-id="ed1c6-103">Rapport de synthèse de conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ed1c6-103">Conference Summary Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ed1c6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ed1c6-104">

<span> </span></span></span>

<span data-ttu-id="ed1c6-105">_**Dernière modification de la rubrique :** 2014-09-03_</span><span class="sxs-lookup"><span data-stu-id="ed1c6-105">_**Topic Last Modified:** 2014-09-03_</span></span>

<span data-ttu-id="ed1c6-106">Le rapport de synthèse de conférence fournit une vue d’ensemble de vos sessions de conférence en ligne.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-106">The Conference Summary Report provides an overall view of your online conferencing sessions.</span></span> <span data-ttu-id="ed1c6-107">En règle générale, une conférence implique plus de 2 utilisateurs et nécessite l’utilisation de Microsoft Lync Server 2013 Conferencing services.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-107">A conference typically involves more than 2 users and requires the use of Microsoft Lync Server 2013 conferencing services.</span></span> <span data-ttu-id="ed1c6-108">En comparaison, une session d’égal à égal implique généralement 2 utilisateurs et ne nécessite pas l’utilisation des services de conférence de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-108">By comparison, a peer-to-peer session typically involves just 2 users and does not require the use of Lync Server's conferencing services.</span></span> <span data-ttu-id="ed1c6-109">Les activités d’égal à égal sont signalées sur le [rapport de synthèse des activités d’égal à égal dans Lync Server 2013](lync-server-2013-peer-to-peer-activity-summary-report.md).</span><span class="sxs-lookup"><span data-stu-id="ed1c6-109">Peer-to-peer activities are reported on the [Peer-to-Peer Activity Summary Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-summary-report.md).</span></span>

<span data-ttu-id="ed1c6-110">Le rapport de synthèse de conférence ne vous indique pas seulement le nombre de conférences qui ont été tenues au cours d’une période donnée (horaire, quotidienne, hebdomadaire, mensuelle), mais vous indique également le nombre total de personnes qui ont participé à ces conférences et le nombre total de organisateurs de conférences uniques.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-110">The Conference Summary Report not only tells you how many conferences were held during a given time period (hourly, daily, weekly, monthly) but also tells you the total number of people who took part in those conferences, and the total number of unique conference organizers.</span></span>

<span data-ttu-id="ed1c6-111">Un organisateur « unique » est une personne qui planifie au moins une conférence.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-111">A "unique” organizer is anyone who schedules at least one conference.</span></span> <span data-ttu-id="ed1c6-112">Par exemple, si Pilar Ackerman planifie une conférence, elle compte comme un organisateur unique.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-112">For example, if Pilar Ackerman schedules one conference she counts as one unique organizer.</span></span> <span data-ttu-id="ed1c6-113">Si Ken Myer planifie 148 conférences, il compte aussi comme un organisateur unique.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-113">If Ken Myer schedules 148 conferences he, too counts as one unique organizer.</span></span> <span data-ttu-id="ed1c6-114">Par exemple, le tableau ci-dessous montre huit conférences programmées, mais uniquement trois organisateurs uniques (Ken Myer, Pilar Arès et David AHS).</span><span class="sxs-lookup"><span data-stu-id="ed1c6-114">For example, the table below shows 8 conferences scheduled, but just three unique organizers (Ken Myer, Pilar Ackerman, and David Ahs).</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed1c6-115">Organisateur de la conférence</span><span class="sxs-lookup"><span data-stu-id="ed1c6-115">Conference Organizer</span></span></th>
<th><span data-ttu-id="ed1c6-116">Date de la conférence</span><span class="sxs-lookup"><span data-stu-id="ed1c6-116">Conference Date</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed1c6-117">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="ed1c6-117">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-118">7/7/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-118">7/7/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1c6-119">David Ahs</span><span class="sxs-lookup"><span data-stu-id="ed1c6-119">David Ahs</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-120">7/7/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-120">7/7/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1c6-121">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="ed1c6-121">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-122">7/7/2012 11:00 AM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-122">7/7/2012 11:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1c6-123">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="ed1c6-123">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-124">7/7/2012 11:00 AM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-124">7/7/2012 11:00 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1c6-125">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="ed1c6-125">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-126">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-126">7/7/2012 1:00 PM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1c6-127">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="ed1c6-127">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-128">7/7/2012 2:00 PM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-128">7/7/2012 2:00 PM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1c6-129">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="ed1c6-129">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-130">7/2/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-130">7/2/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1c6-131">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="ed1c6-131">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-132">7/2/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-132">7/2/2012 10:00 AM</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ed1c6-133">Le rapport de synthèse de conférence indique également le nombre de conférences incluant l’audio et/ou la vidéo.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-133">The Conference Summary Report also indicates how many conferences included audio and/or video.</span></span>

<div>

## <a name="accessing-the-conference-summary-report"></a><span data-ttu-id="ed1c6-134">Accès au rapport de synthèse de conférence</span><span class="sxs-lookup"><span data-stu-id="ed1c6-134">Accessing the Conference Summary Report</span></span>

<span data-ttu-id="ed1c6-p103">Le rapport de synthèse de conférence est accessible depuis la page d’accueil Rapports de surveillance. Vous pouvez accéder au rapport des activités de conférence en cliquant sur l’une ou l’autre des mesures suivantes :</span><span class="sxs-lookup"><span data-stu-id="ed1c6-p103">The Conference Summary Report is accessed from the Monitoring Reports home page. You can drill down to the Conference Activity report by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="ed1c6-137">Nombre total de conférences</span><span class="sxs-lookup"><span data-stu-id="ed1c6-137">Total conferences</span></span>

  - <span data-ttu-id="ed1c6-138">Nombre total de participants</span><span class="sxs-lookup"><span data-stu-id="ed1c6-138">Total participants</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-conference-summary-report"></a><span data-ttu-id="ed1c6-139">Exploiter au mieux le rapport de synthèse de conférence</span><span class="sxs-lookup"><span data-stu-id="ed1c6-139">Making the Best Use of the Conference Summary Report</span></span>

<span data-ttu-id="ed1c6-140">Les valeurs totales pour la plupart des métriques utilisées sur le rapport de synthèse de la Conférence sont accessibles au bas du rapport. Faites défiler vers le bas pour afficher les valeurs telles que le nombre total de conférences organisées pendant la période spécifiée et le nombre total de personnes ayant participé à ces conférences.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-140">Total values for most of the metrics used on the Conference Summary Report can be found at the bottom of the report; scroll down to see values such as the total number of conferences held during the specified time period, and the total number of people who participated in those conferences.</span></span> <span data-ttu-id="ed1c6-141">Une métrique qui n’est pas totalisée en bas du rapport est le nombre total d’organisateurs de conférences uniques.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-141">One metric that is not totaled at the bottom of the report is Total unique conference organizers.</span></span> <span data-ttu-id="ed1c6-142">Pourquoi ?</span><span class="sxs-lookup"><span data-stu-id="ed1c6-142">Why not?</span></span> <span data-ttu-id="ed1c6-143">Voici une raison.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-143">Here’s one reason.</span></span> <span data-ttu-id="ed1c6-144">Imaginons que vous recherchiez un mois de données.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-144">Suppose you are looking at a month's worth of data.</span></span> <span data-ttu-id="ed1c6-145">Le jour 1, vous avez obtenu 34 organisateurs de conférences uniques. le jour 2, vous avez 27 organisateurs de conférences uniques.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-145">On day 1 you had 34 unique conference organizers; on day 2 you had 27 unique conference organizers.</span></span> <span data-ttu-id="ed1c6-146">Est-ce que cela signifie que vous avez 61 de conférences de conférences uniques depuis deux jours ?</span><span class="sxs-lookup"><span data-stu-id="ed1c6-146">Does that mean you had 61 unique conference organizers for those two days?</span></span> <span data-ttu-id="ed1c6-147">Pas nécessairement.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-147">Not necessarily.</span></span> <span data-ttu-id="ed1c6-148">Après tout, les 27 personnes qui ont organisé des conférences le jour 2 peuvent être parmi les 34 personnes qui ont organisé des conférences le jour 1.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-148">After all, all 27 people who organized conferences on day 2 might be among the 34 people who organized conferences on day 1.</span></span> <span data-ttu-id="ed1c6-149">Par exemple, dans ce rapport simple, vous remarquerez les conférences de Ken Myer et Pilar Arès programmées sur 7/7/2012 et 7/2/2012 :</span><span class="sxs-lookup"><span data-stu-id="ed1c6-149">For example, in this simple report, note that Ken Myer and Pilar Ackerman scheduled conferences both on 7/7/2012 and on 7/2/2012:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed1c6-150">Organisateur de la conférence</span><span class="sxs-lookup"><span data-stu-id="ed1c6-150">Conference Organizer</span></span></th>
<th><span data-ttu-id="ed1c6-151">Date de la conférence</span><span class="sxs-lookup"><span data-stu-id="ed1c6-151">Conference Date</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed1c6-152">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="ed1c6-152">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-153">7/7/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-153">7/7/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1c6-154">David Ahs</span><span class="sxs-lookup"><span data-stu-id="ed1c6-154">David Ahs</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-155">7/7/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-155">7/7/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1c6-156">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="ed1c6-156">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-157">7/7/2012 11:00 AM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-157">7/7/2012 11:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1c6-158">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="ed1c6-158">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-159">7/7/2012 11:00 AM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-159">7/7/2012 11:00 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1c6-160">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="ed1c6-160">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-161">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-161">7/7/2012 1:00 PM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1c6-162">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="ed1c6-162">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-163">7/7/2012 2:00 PM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-163">7/7/2012 2:00 PM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1c6-164">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="ed1c6-164">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-165">7/2/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-165">7/2/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1c6-166">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="ed1c6-166">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-167">7/2/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-167">7/2/2012 10:00 AM</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ed1c6-168">Pour vous faire une meilleure idée du nombre total d’utilisateurs uniques qui ont organisé des conférences, modifiez votre intervalle de temps. Par exemple, au lieu d’examiner les données par mois, examinez-les par jour.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-168">To get a better idea of the total number of unique users who organized conferences, change your time interval; for example, look at the data by month instead of by day.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="ed1c6-169">Filtres</span><span class="sxs-lookup"><span data-stu-id="ed1c6-169">Filters</span></span>

<span data-ttu-id="ed1c6-p105">Les filtres vous offrent la possibilité de renvoyer un ensemble de données mieux ciblées ou de visualiser les données renvoyées de différentes manières. Par exemple, le Rapport de synthèse de conférence vous permet de choisir le type de groupement des données. Dans le cas présent, les conférences sont groupées par heure, jour, semaine ou mois.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-p105">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Conference Summary Report enables you to choose how data should be grouped. In this case, conferences grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="ed1c6-173">Le tableau qui suit dresse la liste des filtres que vous pouvez utiliser avec le rapport de synthèse de conférence.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-173">The following table lists the filters that you can use with the Conference Summary Report.</span></span>

### <a name="conference-summary-report-filters"></a><span data-ttu-id="ed1c6-174">Filtres du rapport de synthèse de conférence</span><span class="sxs-lookup"><span data-stu-id="ed1c6-174">Conference Summary Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed1c6-175">Nom</span><span class="sxs-lookup"><span data-stu-id="ed1c6-175">Name</span></span></th>
<th><span data-ttu-id="ed1c6-176">Description</span><span class="sxs-lookup"><span data-stu-id="ed1c6-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed1c6-177"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="ed1c6-177"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1c6-p106">Date/heure de début de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de début comme suit :</span><span class="sxs-lookup"><span data-stu-id="ed1c6-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="ed1c6-180">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-180">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="ed1c6-p107">Si vous ne précisez aucune heure de début, le rapport commence automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="ed1c6-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="ed1c6-183">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="ed1c6-183">7/7/2012</span></span></p>
<p><span data-ttu-id="ed1c6-184">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="ed1c6-184">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="ed1c6-185">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="ed1c6-185">7/3/2012</span></span></p>
<p><span data-ttu-id="ed1c6-186">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-186">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1c6-187"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="ed1c6-187"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1c6-p108">Date/heure de fin de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de fin comme suit :</span><span class="sxs-lookup"><span data-stu-id="ed1c6-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="ed1c6-190">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="ed1c6-190">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="ed1c6-p109">Si vous ne précisez aucune heure de fin, le rapport se termine automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="ed1c6-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="ed1c6-193">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="ed1c6-193">7/7/2012</span></span></p>
<p><span data-ttu-id="ed1c6-194">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="ed1c6-194">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="ed1c6-195">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="ed1c6-195">7/3/2012</span></span></p>
<p><span data-ttu-id="ed1c6-196">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-196">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1c6-197"><strong>Intervalle</strong></span><span class="sxs-lookup"><span data-stu-id="ed1c6-197"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1c6-p110">Intervalle de temps. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="ed1c6-p110">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ed1c6-200">Toutes les heures (il est possible d’afficher un maximum de 25 heures)</span><span class="sxs-lookup"><span data-stu-id="ed1c6-200">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="ed1c6-201">Tous les jours (il est possible d’afficher un maximum de 31 jours)</span><span class="sxs-lookup"><span data-stu-id="ed1c6-201">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="ed1c6-202">Toutes les semaines (il est possible d’afficher un maximum de 12 semaines)</span><span class="sxs-lookup"><span data-stu-id="ed1c6-202">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="ed1c6-203">Tous les mois (il est possible d’afficher un maximum de 12 mois)</span><span class="sxs-lookup"><span data-stu-id="ed1c6-203">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="ed1c6-204">Si la période comprise entre les dates de début et de fin dépasse le nombre maximal de valeurs autorisé pour l’intervalle sélectionné, seul le nombre maximal de valeurs (à compter de la date de début) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-204">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) are displayed.</span></span> <span data-ttu-id="ed1c6-205">Par exemple, si vous sélectionnez l’intervalle quotidien avec une date de début de 7/7/2012 et une date de fin de 2/28/2012, les données sont affichées pour les jours de 8/7/2012 12:00 AM à 9/7/2012 12:00 AM (c’est-à-dire un total de 31 jours de données).</span><span class="sxs-lookup"><span data-stu-id="ed1c6-205">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="ed1c6-206">Mesures</span><span class="sxs-lookup"><span data-stu-id="ed1c6-206">Metrics</span></span>

<span data-ttu-id="ed1c6-207">Le tableau ci-dessous contient les informations fournies par le rapport de synthèse de conférence.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-207">The following table the information provided by the Conferences Summary Report.</span></span>

### <a name="conference-summary-report-metrics"></a><span data-ttu-id="ed1c6-208">Mesures du rapport de synthèse de conférence</span><span class="sxs-lookup"><span data-stu-id="ed1c6-208">Conference Summary Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed1c6-209">Nom</span><span class="sxs-lookup"><span data-stu-id="ed1c6-209">Name</span></span></th>
<th><span data-ttu-id="ed1c6-210">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="ed1c6-210">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="ed1c6-211">Description</span><span class="sxs-lookup"><span data-stu-id="ed1c6-211">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed1c6-212"><strong>Toutes les heures</strong></span><span class="sxs-lookup"><span data-stu-id="ed1c6-212"><strong>Hourly</strong></span></span></p>
<p><span data-ttu-id="ed1c6-213"><strong>Jour</strong></span><span class="sxs-lookup"><span data-stu-id="ed1c6-213"><strong>Daily</strong></span></span></p>
<p><span data-ttu-id="ed1c6-214"><strong>Toutes les semaines</strong></span><span class="sxs-lookup"><span data-stu-id="ed1c6-214"><strong>Weekly</strong></span></span></p>
<p><span data-ttu-id="ed1c6-215"><strong>Mois</strong></span><span class="sxs-lookup"><span data-stu-id="ed1c6-215"><strong>Monthly</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1c6-216">Non</span><span class="sxs-lookup"><span data-stu-id="ed1c6-216">No</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-217">Indique l’intervalle de temps que vous avez sélectionné dans la barre d’outils des filtres.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-217">Indicates the time interval that you selected on the filter toolbar.</span></span> <span data-ttu-id="ed1c6-218">Le cas échéant, vous pouvez cliquer sur un intervalle de temps donné pour afficher des informations détaillées pour cet intervalle.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-218">Where applicable, you can click a given time interval to view detailed information for that interval.</span></span> <span data-ttu-id="ed1c6-219">Par exemple, si vous utilisez l’intervalle quotidien et que vous cliquez sur 7/7/2012, vous pouvez voir une répartition horaire de l’activité d’inscription des utilisateurs à cette date.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-219">For example, if you are using the Daily interval and you click 7/7/2012, you see an hourly breakdown of user registration activity for that date.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1c6-220"><strong>Nombre total de conférences</strong></span><span class="sxs-lookup"><span data-stu-id="ed1c6-220"><strong>Total conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1c6-221">Non</span><span class="sxs-lookup"><span data-stu-id="ed1c6-221">No</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-p113">Nombre total de conférences (de quelque type que ce soit) qui se sont tenues. Lorsque vous cliquez sur cet élément, le rapport vous montre le Rapport des activités de conférence pour la période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-p113">Total number of conferences (regardless of conference type) that were held. When you click this item, the report shows you the Conference Activity Report for the selected time period.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1c6-224"><strong>Nombre total de participants</strong></span><span class="sxs-lookup"><span data-stu-id="ed1c6-224"><strong>Total participants</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1c6-225">Non</span><span class="sxs-lookup"><span data-stu-id="ed1c6-225">No</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-p114">Nombre total de personnes ayant participé aux conférences. Lorsque vous cliquez sur cet élément, le rapport vous montre le Rapport des activités de conférence pour la période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-p114">Total number of people who took part in the conferences. When you click this item, the report shows you the Conference Activity Report for the selected time period.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1c6-228"><strong>Nombre moyen de participants par conférence</strong></span><span class="sxs-lookup"><span data-stu-id="ed1c6-228"><strong>Average participants per conference</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1c6-229">Non</span><span class="sxs-lookup"><span data-stu-id="ed1c6-229">No</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-p115">Nombre moyen de personnes ayant assisté à une conférence donnée. Valeur obtenue en divisant le nombre total de conférences par le nombre total de participants.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-p115">Average number of people who took part in a given conference. Determined by dividing the total conferences by the total participants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1c6-232"><strong>Nombre total de conférences A/V</strong></span><span class="sxs-lookup"><span data-stu-id="ed1c6-232"><strong>Total A/V conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1c6-233">Non</span><span class="sxs-lookup"><span data-stu-id="ed1c6-233">No</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-234">Nombre total de conférences ayant fait usage de son ou de vidéo.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-234">Total number of conferences that included audio or video.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1c6-235"><strong>Nombre total de minutes par conférence A/V</strong></span><span class="sxs-lookup"><span data-stu-id="ed1c6-235"><strong>Total A/V conference minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1c6-236">Non</span><span class="sxs-lookup"><span data-stu-id="ed1c6-236">No</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-237">Nombre total de minutes consacrées à la conférence audio/vidéo.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-237">Total number of minutes devoted to audio/video conferencing.</span></span></p>
<p><span data-ttu-id="ed1c6-238">Le nombre total de minutes de conférence A/V résume l’ensemble des types de conférences audio/vidéo, y compris : conférences A/V ; Conférences de messagerie instantanée ; Conférences de partage d’application ; Conférences de données ; et conférences RTC.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-238">The Total A/V conference minutes metric summarizes all the audio/visual conference types, including: A/V conferences; IM conferences; app sharing conferences; data conferences; and PSTN conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1c6-239"><strong>Nombre total de minutes par participant à la conférence A/V</strong></span><span class="sxs-lookup"><span data-stu-id="ed1c6-239"><strong>Total A/V conference participant minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1c6-240">Non</span><span class="sxs-lookup"><span data-stu-id="ed1c6-240">No</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-p116">Nombre total de minutes consacrées par les participants à la conférence audio/vidéo. Supposons par exemple, qu’un utilisateur passe 5 minutes dans une conférence audio/vidéo et qu’un deuxième utilisateur y passe 3 minutes, nous obtenons un total de 8 minutes de participant.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-p116">Total number of participant minutes devoted to audio/video conferencing. For example, suppose one user spends 5 minutes in an audio/video conference and a second user spends 3 minutes in that same conference. That makes a total of 8 participant minutes: 5 minutes plus 3 minutes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1c6-244"><strong>Nombre moyen de minutes par conférence A/V</strong></span><span class="sxs-lookup"><span data-stu-id="ed1c6-244"><strong>Average A/V conference minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1c6-245">Non</span><span class="sxs-lookup"><span data-stu-id="ed1c6-245">No</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-246">Nombre de minutes moyen par conférence audio/vidéo.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-246">Average number of minutes per audio/video conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1c6-247"><strong>Nombre total d’organisateurs uniques de conférences</strong></span><span class="sxs-lookup"><span data-stu-id="ed1c6-247"><strong>Total number of unique organizers of conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1c6-248">Non</span><span class="sxs-lookup"><span data-stu-id="ed1c6-248">No</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-p117">Nombre total d’utilisateurs ayant organisé au moins une conférence. Les utilisateurs ayant organisé plusieurs conférences sont comptabilisés comme des organisateurs uniques, à l’instar de ceux qui n’en ont organisées qu’une seule.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-p117">Total number of users who organized at least one conference. Users who organized more than one conference are counted as one unique organizer, just like users who only organized a single conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1c6-251"><strong>Nombre total de messages de conférence</strong></span><span class="sxs-lookup"><span data-stu-id="ed1c6-251"><strong>Total conference messages</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1c6-252">Non</span><span class="sxs-lookup"><span data-stu-id="ed1c6-252">No</span></span></p></td>
<td><p><span data-ttu-id="ed1c6-253">Nombre total de messages instantanés envoyés au cours des conférences.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-253">Total number of instant messages sent during the conferences.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ed1c6-254">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ed1c6-254">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

