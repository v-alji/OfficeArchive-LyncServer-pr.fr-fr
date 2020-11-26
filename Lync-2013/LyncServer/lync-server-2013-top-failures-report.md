---
title: 'Lync Server 2013 : rapport sur les principaux échecs'
description: 'Lync Server 2013 : rapport sur les principaux échecs.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Top Failures Report
ms:assetid: 438942e2-580a-4b67-9d42-f116111fb26a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558640(v=OCS.15)
ms:contentKeyID: 48184021
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 768c9a99916dece9eb76877b0cd65b057697ff95
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440912"
---
# <a name="top-failures-report-in-lync-server-2013"></a><span data-ttu-id="8e3f4-103">Rapport sur les principaux échecs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e3f4-103">Top Failures Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8e3f4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8e3f4-104">

<span> </span></span></span>

<span data-ttu-id="8e3f4-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="8e3f4-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="8e3f4-p101">Le rapport des principales défaillances expose les défaillances les plus fréquentes et leur évolution dans le temps. Les défaillances sont basées sur une combinaison des deux métriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e3f4-p101">The Top Failures Report provides a look at the most-commonly reported failures and their trends over time. Failures are based on a combination of the following two metrics:</span></span>

  - <span data-ttu-id="8e3f4-p102">**ID de diagnostic**. Identificateur unique (sous la forme d’un en-tête ms-diagnostics) joint à un message SIP. Les ID de diagnostic fournissent des informations utiles pour résoudre les problèmes liés aux appels.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-p102">**Diagnostic ID**. Unique identifier (in the form of an ms-diagnostics header) that is attached to a SIP message. Diagnostic IDs provide information useful in troubleshooting call-related problems.</span></span>

  - <span data-ttu-id="8e3f4-111">**Code de réponse**.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-111">**Response code**.</span></span> <span data-ttu-id="8e3f4-112">Les codes de réponse sont utilisés dans les sessions de communication SIP pour répondre aux demandes SIP.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-112">Response codes are used in SIP communication sessions to respond to SIP requests.</span></span> <span data-ttu-id="8e3f4-113">Par exemple, supposons que Ken envoie la demande d’invitation à Pilar Arès (autrement dit, il appelle Ken Myer Pilar Arès).</span><span class="sxs-lookup"><span data-stu-id="8e3f4-113">For example, suppose Ken sends the INVITE request to Pilar Ackerman (that is, suppose Ken Myer calls Pilar Ackerman).</span></span> <span data-ttu-id="8e3f4-114">Si Pilar répond, son numéro envoie le code de réponse 200 (OK), en laissant le téléphone de Ken savoir que Pilar a répondu.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-114">If Pilar answers, her phone will send the response code 200 (OK), letting Ken's phone know that Pilar has answered.</span></span> <span data-ttu-id="8e3f4-115">Le rapport pannes principales inclut uniquement les codes de réponse envoyés en réponse à un échec de l’appel. Le serveur Lync n’effectue pas le suivi de tous les codes de réponse émis pendant un appel.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-115">The Top Failures Report only includes response codes that were sent in response to a call failure; Lync Server does not keep track of all the response codes issued during the course of a call.</span></span>

<span data-ttu-id="8e3f4-116">Les informations sont signalées pour le nombre total de sessions où une défaillance s’est produite, ainsi que pour le nombre total d’utilisateurs affectés par la panne.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-116">Information is reported not only for the total number of sessions where a failure occurred but also for the total number of users who were impacted by the failure.</span></span>

<div>

## <a name="accessing-the-top-failures-report"></a><span data-ttu-id="8e3f4-117">Accès au rapport des principales défaillances</span><span class="sxs-lookup"><span data-stu-id="8e3f4-117">Accessing the Top Failures Report</span></span>

<span data-ttu-id="8e3f4-118">Le rapport des principales défaillances est accessible à partir de la page d’accueil Rapports de surveillance.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-118">The Top Failures Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="8e3f4-119">Le fait de cliquer sur la métrique de sessions signalées vous permet d’atteindre le [rapport de distribution des échecs dans Lync Server 2013](lync-server-2013-failure-distribution-report.md).</span><span class="sxs-lookup"><span data-stu-id="8e3f4-119">Clicking the Reported sessions metric will take you to the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md).</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-top-failures-report"></a><span data-ttu-id="8e3f4-120">Optimisation de l’utilisation du rapport des principales défaillances</span><span class="sxs-lookup"><span data-stu-id="8e3f4-120">Making the Best Use of the Top Failures Report</span></span>

<span data-ttu-id="8e3f4-p105">Le rapport des principales défaillances est particulier : il vous permet de filtrer jusqu’à 5 ID de diagnostic à la fois. En règle générale, vous ne pouvez filtrer qu’un élément (par exemple, une adresse SIP d’utilisateur) à la fois. Pour filtrer plusieurs ID de diagnostic, il suffit d’entrer chaque ID dans la zone ID de diagnostic, en séparant les ID par des virgules. Si vous le souhaitez, vous pouvez laisser un espace vide après chaque virgule. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="8e3f4-p105">The Top Failures Report is unusual in one regard: it allows you to filter on as many as 5 diagnostic IDs at once. (Typically you can only filter on one item – such as one user SIP address – at a time.) To filter on multiple diagnostic IDs, simply enter each ID in the Diagnostic IDs box, separating the IDs by using commas. (If you want to, you can leave a blank space after each comma.) For example:</span></span>

<span data-ttu-id="8e3f4-124">1011, 2412, 1033, 52116, 1008</span><span class="sxs-lookup"><span data-stu-id="8e3f4-124">1011, 2412, 1033, 52116, 1008</span></span>

<span data-ttu-id="8e3f4-125">Procédez ainsi pour afficher uniquement les appels défaillants qui correspondent à l’un de ces cinq ID de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-125">Do that, and only failed calls that reported at least one of those five diagnostic IDs will be displayed.</span></span>

<span data-ttu-id="8e3f4-p106">Si vous pointez le curseur de la souris sur un code de réponse, vous voyez s’afficher une info-bulle qui vous indique la signification de ce code de réponse. Par exemple, si vous pointez sur le code de réponse 486, vous voyez s’afficher le message suivant :</span><span class="sxs-lookup"><span data-stu-id="8e3f4-p106">If you hold your mouse over a Response code you'll see a tooltip that tells you what the Response code in question means. For example, if you hold the mouse over the Response code 486 you'll see this message:</span></span>

<span data-ttu-id="8e3f4-128">Occupé ici.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-128">Busy Here.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="8e3f4-129">Filtres</span><span class="sxs-lookup"><span data-stu-id="8e3f4-129">Filters</span></span>

<span data-ttu-id="8e3f4-p107">Les filtres vous offrent la possibilité de renvoyer un ensemble de données mieux ciblées ou de visualiser les données renvoyées de différentes manières. Par exemple, le rapport d’activité de l’utilisateur vous permet de filtrer les données renvoyées sur la base d’éléments tels que le type d’activité (session P2P ou session de conférence) ou le code de réponse SIP qui accompagnait la session en échec. Vous pouvez également choisir le mode de groupement des données. Dans ce cas, les utilisations sont groupées par heure, jour, semaine ou mois.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-p107">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Top Failures Report enables you to filter the returned data based on such things as the activity type (peer-to-peer session or conferencing session) or by the SIP response code that accompanied the failed session. You can also choose how data should be grouped. In this case, usages are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="8e3f4-134">Le tableau qui suit dresse la liste des filtres que vous pouvez utiliser avec le rapport des principales défaillances.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-134">The following table lists the filters that you can use with the Top Failures Report.</span></span>

### <a name="top-failures-report-filters"></a><span data-ttu-id="8e3f4-135">Filtres du rapport des principales défaillances</span><span class="sxs-lookup"><span data-stu-id="8e3f4-135">Top Failures Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e3f4-136">Nom</span><span class="sxs-lookup"><span data-stu-id="8e3f4-136">Name</span></span></th>
<th><span data-ttu-id="8e3f4-137">Description</span><span class="sxs-lookup"><span data-stu-id="8e3f4-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e3f4-138"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f4-138"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="8e3f4-p108">Date/heure de début de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de début comme suit :</span><span class="sxs-lookup"><span data-stu-id="8e3f4-p108">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="8e3f4-141">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="8e3f4-141">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="8e3f4-p109">Si vous ne précisez aucune heure de début, le rapport commence automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="8e3f4-p109">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="8e3f4-144">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="8e3f4-144">7/7/2012</span></span></p>
<p><span data-ttu-id="8e3f4-145">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="8e3f4-145">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="8e3f4-146">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="8e3f4-146">7/3/2012</span></span></p>
<p><span data-ttu-id="8e3f4-147">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-147">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e3f4-148"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f4-148"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="8e3f4-p110">Date/heure de fin de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de fin comme suit :</span><span class="sxs-lookup"><span data-stu-id="8e3f4-p110">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="8e3f4-151">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="8e3f4-151">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="8e3f4-p111">Si vous ne précisez aucune heure de fin, le rapport se termine automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="8e3f4-p111">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="8e3f4-154">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="8e3f4-154">7/7/2012</span></span></p>
<p><span data-ttu-id="8e3f4-155">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="8e3f4-155">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="8e3f4-156">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="8e3f4-156">7/3/2012</span></span></p>
<p><span data-ttu-id="8e3f4-157">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-157">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e3f4-158"><strong>Type d’activité</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f4-158"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="8e3f4-p112">Type d’activité. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e3f4-p112">Type of activity. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="8e3f4-161">[Tous]</span><span class="sxs-lookup"><span data-stu-id="8e3f4-161">[All]</span></span></p></li>
<li><p><span data-ttu-id="8e3f4-162">Égal à égal</span><span class="sxs-lookup"><span data-stu-id="8e3f4-162">Peer-to-peer</span></span></p></li>
<li><p><span data-ttu-id="8e3f4-163">Conférence</span><span class="sxs-lookup"><span data-stu-id="8e3f4-163">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e3f4-164"><strong>Modalité</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f4-164"><strong>Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="8e3f4-165">À ce stade, la seule option disponible est <strong>[Tous]</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-165">At this time the only option available is <strong>[All]</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e3f4-166"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f4-166"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="8e3f4-p113">Nom de domaine complet (FQDN) du pool de serveurs d’inscriptions. Vous pouvez soit sélectionner un pool particulier, soit cliquer sur <strong>[Tous]</strong> pour afficher les données de tous les pools. Cette liste déroulante se renseigne automatiquement en fonction des enregistrements que contient la base de données.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-p113">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e3f4-170"><strong>Catégorie</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f4-170"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="8e3f4-p114">Type de défaillance rencontrée. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e3f4-p114">Type of failure experienced. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="8e3f4-173">Échecs attendus et inattendus</span><span class="sxs-lookup"><span data-stu-id="8e3f4-173">Both expected and unexpected failure</span></span></p></li>
<li><p><span data-ttu-id="8e3f4-174">Échec inattendu</span><span class="sxs-lookup"><span data-stu-id="8e3f4-174">Unexpected failure</span></span></p></li>
</ul>
<p><span data-ttu-id="8e3f4-175">Un &quot; échec attendu &quot; est un échec censé se produire.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-175">An &quot;expected failure&quot; is a failure that is expected to happen.</span></span> <span data-ttu-id="8e3f4-176">Par exemple, si un utilisateur a défini son statut sur Ne pas déranger, les appels passés à cet utilisateur échouent.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-176">For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span> <span data-ttu-id="8e3f4-177">Un &quot; échec inattendu &quot; est une défaillance qui peut se produire dans un système de bon fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-177">An &quot;unexpected failure&quot; is a failure that occurs in what would appear to be an otherwise healthy system.</span></span> <span data-ttu-id="8e3f4-178">Par exemple, un appel n’est pas censé s’interrompre lorsque l’appelant est mis en attente.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-178">For example, a call should not be terminated if the caller is placed on hold.</span></span> <span data-ttu-id="8e3f4-179">Si cela se produit, l’incident est marqué comme un échec inattendu.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-179">If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e3f4-180"><strong>Code de réponse</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f4-180"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="8e3f4-p116">Code de réponse SIP envoyé lors de l’échec de la conférence. Entrez le code de réponse entier. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="8e3f4-p116">SIP response code sent when the conference failed. Enter the entire response code For example:</span></span></p>
<p><span data-ttu-id="8e3f4-183">400</span><span class="sxs-lookup"><span data-stu-id="8e3f4-183">400</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e3f4-184"><strong>ID de diagnostic</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f4-184"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="8e3f4-p117">Identificateur unique (sous la forme d’un en-tête ms-diagnostics) attaché à un message SIP qui fournit souvent des informations utiles pour résoudre des erreurs. Les en-têtes de diagnostic sont facultatifs (il est possible que des sessions SIP n’incluent pas ces en-têtes) et les ID de diagnostic sont uniquement signalés pour les sessions qui ont rencontré des problèmes, quels qu’ils soient.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-p117">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="8e3f4-187">Mesures</span><span class="sxs-lookup"><span data-stu-id="8e3f4-187">Metrics</span></span>

<span data-ttu-id="8e3f4-188">Le tableau qui suit répertorie les informations fournies dans le rapport des principales défaillances.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-188">The following table lists the information provided in the Top Failures Report.</span></span>

### <a name="top-failures-report-metrics"></a><span data-ttu-id="8e3f4-189">Mesures du rapport des principales défaillances</span><span class="sxs-lookup"><span data-stu-id="8e3f4-189">Top Failures Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e3f4-190">Nom</span><span class="sxs-lookup"><span data-stu-id="8e3f4-190">Name</span></span></th>
<th><span data-ttu-id="8e3f4-191">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="8e3f4-191">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="8e3f4-192">Description</span><span class="sxs-lookup"><span data-stu-id="8e3f4-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e3f4-193"><strong>Classement</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f4-193"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="8e3f4-194">Oui</span><span class="sxs-lookup"><span data-stu-id="8e3f4-194">Yes</span></span></p></td>
<td><p><span data-ttu-id="8e3f4-195">Classement relatif sur la base du nombre de sessions signalées.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-195">Relative rank based on the number of reported sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e3f4-196"><strong>Sessions signalées</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f4-196"><strong>Reported sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="8e3f4-197">Oui</span><span class="sxs-lookup"><span data-stu-id="8e3f4-197">Yes</span></span></p></td>
<td><p><span data-ttu-id="8e3f4-198">Nombre total de sessions en échec sur la base de l’ID de diagnostic et du code de réponse SIP.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-198">Total number of failed sessions based on diagnostic ID and SIP response code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e3f4-199"><strong>Utilisateurs affectés</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f4-199"><strong>Users impacted</strong></span></span></p></td>
<td><p><span data-ttu-id="8e3f4-200">Oui</span><span class="sxs-lookup"><span data-stu-id="8e3f4-200">Yes</span></span></p></td>
<td><p><span data-ttu-id="8e3f4-201">Nombre total d’utilisateurs affectés par l’échec de la session.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-201">Total number of users affected by the failed session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e3f4-202"><strong>Informations sur l’échec</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f4-202"><strong>Failure information</strong></span></span></p></td>
<td><p><span data-ttu-id="8e3f4-203">Non</span><span class="sxs-lookup"><span data-stu-id="8e3f4-203">No</span></span></p></td>
<td><p><span data-ttu-id="8e3f4-204">Informations détaillées sur l’échec, notamment ID de diagnostic, code de réponse SIP et description de la cause de l’échec de la session.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-204">Detailed information about the failure, including diagnostic ID, SIP response code, and description of why the session failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e3f4-205"><strong>Tendance dans le passé</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f4-205"><strong>Trend in the past</strong></span></span></p></td>
<td><p><span data-ttu-id="8e3f4-206">Non</span><span class="sxs-lookup"><span data-stu-id="8e3f4-206">No</span></span></p></td>
<td><p><span data-ttu-id="8e3f4-207">Propose un graphique des échecs de session dans le temps.</span><span class="sxs-lookup"><span data-stu-id="8e3f4-207">Graphs failed sessions over time.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8e3f4-208">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8e3f4-208">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

