---
title: 'Rapport de performances du serveur Lync Server 2013 :'
description: 'Lync Server 2013 : rapport sur les performances du serveur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server Performance Report
ms:assetid: 942bb39a-1790-498e-9d99-8f6ce2d155c3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615018(v=OCS.15)
ms:contentKeyID: 48184879
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aed9b3b9eeec4487dce4d401df0d70ffba89677b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441878"
---
# <a name="server-performance-report-in-lync-server-2013"></a><span data-ttu-id="e14c5-103">Rapport sur les performances du serveur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e14c5-103">Server Performance Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e14c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e14c5-104">

<span> </span></span></span>

<span data-ttu-id="e14c5-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="e14c5-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="e14c5-106">Le rapport sur les performances du serveur fournit une liste de serveurs Microsoft Lync Server 2013 ayant constaté le plus grand pourcentage d’appels médiocres.</span><span class="sxs-lookup"><span data-stu-id="e14c5-106">The Server Performance Report provides a list of Microsoft Lync Server 2013 servers that have experienced the highest-percentage of poor calls.</span></span> <span data-ttu-id="e14c5-107">Ce rapport est décomposé en fonction des types de serveur, et propose des statistiques distinctes pour les types suivants :</span><span class="sxs-lookup"><span data-stu-id="e14c5-107">The report breaks down servers by server type, reporting separate statistics for the following types:</span></span>

  - <span data-ttu-id="e14c5-108">Serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="e14c5-108">Mediation Server</span></span>

  - <span data-ttu-id="e14c5-109">Serveur de conférence A/V</span><span class="sxs-lookup"><span data-stu-id="e14c5-109">A/V Conferencing Server</span></span>

  - <span data-ttu-id="e14c5-110">Serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="e14c5-110">A/V Edge Server</span></span>

  - <span data-ttu-id="e14c5-111">Passerelle (serveur de médiation)</span><span class="sxs-lookup"><span data-stu-id="e14c5-111">Gateway (Mediation Server)</span></span>

  - <span data-ttu-id="e14c5-112">Passerelle (contournement du serveur de médiation)</span><span class="sxs-lookup"><span data-stu-id="e14c5-112">Gateway (Mediation Server bypass)</span></span>

  - <span data-ttu-id="e14c5-113">Vidéo (y compris les mesures vidéo pour les serveurs de conférence A/V et les serveurs Edge A/V)</span><span class="sxs-lookup"><span data-stu-id="e14c5-113">Video (including video metrics for A/V Conferencing servers and A/V Edge servers)</span></span>

  - <span data-ttu-id="e14c5-114">Partage d’application (y compris les mesures de partage d’application pour les serveurs de conférence A/V et les serveurs Edge A/V)</span><span class="sxs-lookup"><span data-stu-id="e14c5-114">Application Sharing (including application sharing metrics for A/V Conferencing servers and A/V Edge servers)</span></span>

<span data-ttu-id="e14c5-p102">Il est important de noter que le classement indiqué dans le rapport est relatif. Par exemple, supposons que le serveur ayant les pires performances a reçu un appel médiocre sur les 1 000 passés. Ce pourcentage de 0,1 est plus qu’acceptable. Cependant, s’il s’agit du serveur ayant les pires performances (c’est-à-dire que les autres serveurs ont un pourcentage d’appels médiocres inférieur à 0,1 %), ce serveur s’affichera dans le rapport de performances du serveur.</span><span class="sxs-lookup"><span data-stu-id="e14c5-p102">It’s important to note that the ranking shown in this report as relative rankings. For example, suppose your worst-performing server had one poor call among its 1,000 placed calls. That's a more-than-acceptable percentage of .1%. However, if that's the worst-performing server you have (that is, if all your other servers have a poor call percentage even lower than .1%), then that server will still appear on the Server Performance Report.</span></span>

<div>

## <a name="accessing-the-server-performance-report"></a><span data-ttu-id="e14c5-119">Accès au rapport de performances du serveur</span><span class="sxs-lookup"><span data-stu-id="e14c5-119">Accessing the Server Performance Report</span></span>

<span data-ttu-id="e14c5-120">Le rapport de performances du serveur est accessible à partir de la page d’accueil Rapports de surveillance.</span><span class="sxs-lookup"><span data-stu-id="e14c5-120">The Server Performance Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="e14c5-121">Vous pouvez explorer le rapport de la [liste d’appels dans Lync Server 2013](lync-server-2013-call-list-report.md) en cliquant sur l’une des mesures suivantes :</span><span class="sxs-lookup"><span data-stu-id="e14c5-121">You can drill down to the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="e14c5-122">Volume d’appels</span><span class="sxs-lookup"><span data-stu-id="e14c5-122">Call volume</span></span>

  - <span data-ttu-id="e14c5-123">Pourcentage d’appels médiocres</span><span class="sxs-lookup"><span data-stu-id="e14c5-123">Poor call percentage</span></span>

<span data-ttu-id="e14c5-124">De plus, vous pouvez accéder au rapport de tendance de la qualité des médias serveur en cliquant sur la mesure suivante :</span><span class="sxs-lookup"><span data-stu-id="e14c5-124">In addition, you can drill down to the Server Media Quality Trend Report by clicking the following metric:</span></span>

  - <span data-ttu-id="e14c5-125">Tendance</span><span class="sxs-lookup"><span data-stu-id="e14c5-125">Trend</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-server-performance-report"></a><span data-ttu-id="e14c5-126">Optimiser l’utilisation du rapport sur les performances du serveur</span><span class="sxs-lookup"><span data-stu-id="e14c5-126">Making the Best Use of the Server Performance Report</span></span>

<span data-ttu-id="e14c5-p104">Le rapport de performances du serveur fournit plusieurs moyens pour filtrer les données ; par exemple, vous pouvez filtrer sur un type de réseau (appels passés via une connexion câblée ou sans fil) et un type d’accès (appels passés à l’intérieur du pare-feu ou à l’extérieur). Il est conseillé d’utiliser ces filtres quand vous affichez le rapport de performances du serveur. Par exemple, vous avez un serveur de médiation avec un pourcentage d’appels médiocre de 3,24 %. Si vous considérez uniquement les appels sans fil, ce même serveur peut avoir un pourcentage d’appels médiocres de 20 %. Cela signifie que ce serveur ne gère pas bien les appels sans fil, mais ce problème peut être partiellement masqué par les appels câblés qui ne posent pas de problème.</span><span class="sxs-lookup"><span data-stu-id="e14c5-p104">The Server Performance Report provides a number of ways to filter data; for example, you can filter on network type (calls made from a wired connection vs. calls made from a wireless connection) and access type (calls made from inside the firewall vs. calls made from outside the firewall). It's a good idea when viewing the server performance report to make use of these filters. For example, suppose you have a Mediation Server that has a poor call percentage of 3.24%. If you look solely at wireless calls, that same server might have a poor call percentage approaching 20%. That means that the server was having difficulty with wireless calls, a problem that is partially obscured because the server was not having problems with wired calls.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="e14c5-132">Filtres</span><span class="sxs-lookup"><span data-stu-id="e14c5-132">Filters</span></span>

<span data-ttu-id="e14c5-p105">Les filtres vous offrent la possibilité de renvoyer un ensemble de données mieux ciblées ou de visualiser les données renvoyées de différentes manières. Le rapport de performances du serveur vous permet par exemple, de filtrer les données renvoyées par type de serveur ou type de réseau (câblé ou sans fil). Vous pouvez également choisir le mode de groupement des données. Dans ce cas, les données sont groupées par heure, jour, semaine ou mois.</span><span class="sxs-lookup"><span data-stu-id="e14c5-p105">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Server Performance Report enables you to do such things as filter the returned data by server type or by network type (that is, wired or wireless). You can also choose how data should be grouped. In this case, data is grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="e14c5-137">Le tableau qui suit dresse la liste des filtres que vous pouvez utiliser avec le rapport de performances du serveur.</span><span class="sxs-lookup"><span data-stu-id="e14c5-137">The following table lists the filters that you can use with the Server Performance Report.</span></span>

### <a name="server-performance-report-filters"></a><span data-ttu-id="e14c5-138">Filtres de rapport de performances du serveur</span><span class="sxs-lookup"><span data-stu-id="e14c5-138">Server Performance Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e14c5-139">Nom</span><span class="sxs-lookup"><span data-stu-id="e14c5-139">Name</span></span></th>
<th><span data-ttu-id="e14c5-140">Description</span><span class="sxs-lookup"><span data-stu-id="e14c5-140">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-141"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-141"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-p106">Date/heure de début de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de début comme suit :</span><span class="sxs-lookup"><span data-stu-id="e14c5-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="e14c5-144">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="e14c5-144">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="e14c5-p107">Si vous ne précisez aucune heure de début, le rapport commence automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="e14c5-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="e14c5-147">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="e14c5-147">7/7/2012</span></span></p>
<p><span data-ttu-id="e14c5-148">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="e14c5-148">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="e14c5-149">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="e14c5-149">7/3/2012</span></span></p>
<p><span data-ttu-id="e14c5-150">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="e14c5-150">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-151"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-151"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-p108">Date/heure de fin de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de fin comme suit :</span><span class="sxs-lookup"><span data-stu-id="e14c5-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="e14c5-154">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="e14c5-154">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="e14c5-p109">Si vous ne précisez aucune heure de fin, le rapport se termine automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="e14c5-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="e14c5-157">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="e14c5-157">7/7/2012</span></span></p>
<p><span data-ttu-id="e14c5-158">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="e14c5-158">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="e14c5-159">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="e14c5-159">7/3/2012</span></span></p>
<p><span data-ttu-id="e14c5-160">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="e14c5-160">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-161"><strong>Type de serveur</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-161"><strong>Server type</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-p110">Indique le type de serveur dont les performances doivent être rapportées. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="e14c5-p110">Indicates the type of server whose performance should be reported. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="e14c5-164">[Tous]</span><span class="sxs-lookup"><span data-stu-id="e14c5-164">[All]</span></span></p></li>
<li><p><span data-ttu-id="e14c5-165">Serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="e14c5-165">Mediation Server</span></span></p></li>
<li><p><span data-ttu-id="e14c5-166">Serveur de conférence A/V</span><span class="sxs-lookup"><span data-stu-id="e14c5-166">A/V Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="e14c5-167">Serveur Edge A/V</span><span class="sxs-lookup"><span data-stu-id="e14c5-167">A/V Edge Server</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-168"><strong>N premiers</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-168"><strong>Top N</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-p111">Indique le nombre de serveurs (sur la base du pourcentage d’appels médiocres) à afficher dans chaque catégorie. Par exemple, si vous sélectionnez <strong>5</strong>, les cinq serveurs ayant les performances les plus médiocres sont affichés. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="e14c5-p111">Indicates the number of servers (based on their poor call percentage) to be displayed in each category. For example, if you select <strong>5</strong> then the five poorest-performing servers are displayed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="e14c5-172">[Tous]</span><span class="sxs-lookup"><span data-stu-id="e14c5-172">[All]</span></span></p></li>
<li><p><span data-ttu-id="e14c5-173">5</span><span class="sxs-lookup"><span data-stu-id="e14c5-173">5</span></span></p></li>
<li><p><span data-ttu-id="e14c5-174">0,10</span><span class="sxs-lookup"><span data-stu-id="e14c5-174">10</span></span></p></li>
</ol></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-175"><strong>Type d’accès</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-175"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-p112">Indique si le client était connecté au réseau interne ou au réseau externe au moment de passer l’appel. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="e14c5-p112">Indicates whether the client was logged on to the internal network or the external network when the call was placed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="e14c5-178">[Tous]</span><span class="sxs-lookup"><span data-stu-id="e14c5-178">[All]</span></span></p></li>
<li><p><span data-ttu-id="e14c5-179">Interne</span><span class="sxs-lookup"><span data-stu-id="e14c5-179">Internal</span></span></p></li>
<li><p><span data-ttu-id="e14c5-180">Externe</span><span class="sxs-lookup"><span data-stu-id="e14c5-180">External</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-181"><strong>Type de réseau</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-181"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-p113">Indique le type de réseau auquel le client était connecté au moment où l’appel a été émis. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="e14c5-p113">Indicates the type of network the client was connected to when the call was placed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="e14c5-184">[Tous]</span><span class="sxs-lookup"><span data-stu-id="e14c5-184">[All]</span></span></p></li>
<li><p><span data-ttu-id="e14c5-185">Câblé</span><span class="sxs-lookup"><span data-stu-id="e14c5-185">Wired</span></span></p></li>
<li><p><span data-ttu-id="e14c5-186">Sans fil</span><span class="sxs-lookup"><span data-stu-id="e14c5-186">Wireless</span></span></p></li>
</ol></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-187"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-187"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-p114">Indique si un client externe utilisait une connexion de réseau privé virtuel (VPN) au moment d’effectuer l’appel. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="e14c5-p114">Indicates whether an external client was using a virtual private network (VPN) connection when the call was placed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="e14c5-190">[Tous]</span><span class="sxs-lookup"><span data-stu-id="e14c5-190">[All]</span></span></p></li>
<li><p><span data-ttu-id="e14c5-191">VPN</span><span class="sxs-lookup"><span data-stu-id="e14c5-191">VPN</span></span></p></li>
<li><p><span data-ttu-id="e14c5-192">Non-VPN</span><span class="sxs-lookup"><span data-stu-id="e14c5-192">Non-VPN</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="e14c5-193">Mesures</span><span class="sxs-lookup"><span data-stu-id="e14c5-193">Metrics</span></span>

<span data-ttu-id="e14c5-194">Le tableau qui suit répertorie les informations fournies dans le rapport de performances du serveur.</span><span class="sxs-lookup"><span data-stu-id="e14c5-194">The following table lists the information provided in the Server Performance Report.</span></span>

### <a name="server-performance-report-metrics-audio-call-summary"></a><span data-ttu-id="e14c5-195">Mesures du rapport de performances du serveur : synthèse des appels audio</span><span class="sxs-lookup"><span data-stu-id="e14c5-195">Server Performance Report Metrics: Audio Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e14c5-196">Nom</span><span class="sxs-lookup"><span data-stu-id="e14c5-196">Name</span></span></th>
<th><span data-ttu-id="e14c5-197">Tri possible</span><span class="sxs-lookup"><span data-stu-id="e14c5-197">Can Sort On</span></span></th>
<th><span data-ttu-id="e14c5-198">Description</span><span class="sxs-lookup"><span data-stu-id="e14c5-198">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-199"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-200">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-200">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-201">Nom/adresse IP du serveur</span><span class="sxs-lookup"><span data-stu-id="e14c5-201">Name/IP address of the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-202"><strong>Volume d’appels</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-202"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-203">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-203">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-204">Nombre total d’appels effectués.</span><span class="sxs-lookup"><span data-stu-id="e14c5-204">Total number of calls made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-205"><strong>Pourcentage d’appels médiocres</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-205"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-206">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-206">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-p115">Nombre total d’appels jugés et classés comme étant médiocres. Un appel médiocre désigne un appel dont l’une des valeurs mesurées est supérieure à la valeur autorisée (par exemple, un appel soumis à un phénomène de gigue excessive).</span><span class="sxs-lookup"><span data-stu-id="e14c5-p115">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-209"><strong>Boucle (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-209"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-210">Oui</span><span class="sxs-lookup"><span data-stu-id="e14c5-210">Yes</span></span></p></td>
<td><p><span data-ttu-id="e14c5-p116">Temps moyen (en millisecondes) nécessaire à un package RTP (Real-Time Transport Protocol) pour effectuer un aller-retour vers un autre point de terminaison. Des boucles de 100 millisecondes ou moins sont considérées qualitativement acceptables.</span><span class="sxs-lookup"><span data-stu-id="e14c5-p116">Average amount of (in milliseconds) required for a real-time transport protocol (RTP) packet to travel to another endpoint and then back. Round-trip times of 100 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="e14c5-p117">Des boucles de durée plus élevée peuvent être causées par le routage international des appels, une mauvaise configuration du routage ou un serveur multimédia surchargé. Les durées d’aller-retour élevées créent des difficultés dans le cadre de conversations audio bidirectionnelles réalisées en temps réel.</span><span class="sxs-lookup"><span data-stu-id="e14c5-p117">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-215"><strong>Dégradation (MOS)</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-215"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-216">Oui</span><span class="sxs-lookup"><span data-stu-id="e14c5-216">Yes</span></span></p></td>
<td><p><span data-ttu-id="e14c5-217">Taux moyen de dégradation de la note moyenne d’opinion (MOS) observé au cours d’un appel.</span><span class="sxs-lookup"><span data-stu-id="e14c5-217">Average amount of mean opinion score (MOS) degradation experienced during a call.</span></span> <span data-ttu-id="e14c5-218">Les valeurs de dégradation peuvent aller de 0,0 (la plus faible) à 5,0 (la plus élevée).</span><span class="sxs-lookup"><span data-stu-id="e14c5-218">Degradation values can range from a low of 0.0 to a high of 5.0.</span></span> <span data-ttu-id="e14c5-219">Une valeur de 0,5 ou moins signifie une dégradation acceptable.</span><span class="sxs-lookup"><span data-stu-id="e14c5-219">A value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="e14c5-220">Traditionnellement, les notes moyennes d’opinion sont calculées en demandant aux utilisateurs d’évaluer la qualité d’un appel sur une échelle de 1 à 5.</span><span class="sxs-lookup"><span data-stu-id="e14c5-220">Historically, mean options scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="e14c5-221">Dans Lync Server, le serveur de surveillance utilise un ensemble d’algorithmes pour prévoir la façon dont les utilisateurs auraient noté un appel.</span><span class="sxs-lookup"><span data-stu-id="e14c5-221">In Lync Server, the Monitoring Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="e14c5-p119">Les valeurs de dégradation élevées peuvent provenir d’une congestion, d’un dépassement de la bande passante disponible, d’une congestion/interférence dans la liaison sans fil ou bien d’un serveur multimédia ou d’un point de terminaison surchargé, ce qui se traduit par une distorsion ou une perte de l’audio.</span><span class="sxs-lookup"><span data-stu-id="e14c5-p119">High degradation values can be caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-224"><strong>Perte de paquets</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-224"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-225">Oui</span><span class="sxs-lookup"><span data-stu-id="e14c5-225">Yes</span></span></p></td>
<td><p><span data-ttu-id="e14c5-p120">Taux moyen de pertes de paquets RTP. (La perte de paquets survient lorsque des paquets RTP, protocole employé pour la transmission audio et vidéo sur Internet, n’atteignent pas leur point de destination.) Les valeurs de perte élevées peuvent provenir d’une congestion, d’un dépassement de la bande passante disponible, d’une congestion/interférence dans la liaison sans fil ou d’un serveur multimédia surchargé, ce qui se traduit par une distorsion ou une perte de l’audio.</span><span class="sxs-lookup"><span data-stu-id="e14c5-p120">Average rate of real-time transport protocol (RTP) packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-229"><strong>Gigue (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-229"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-230">Oui</span><span class="sxs-lookup"><span data-stu-id="e14c5-230">Yes</span></span></p></td>
<td><p><span data-ttu-id="e14c5-231">Gigue moyenne détectée entre les arrivées de paquets RTP.</span><span class="sxs-lookup"><span data-stu-id="e14c5-231">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="e14c5-232">(Gigue est une mesure du &quot; shakiness &quot; d’un appel.) Les valeurs de gigue élevée sont généralement provoquées par une congestion ou un serveur multimédia surchargé, ce qui a pour effet de déformer ou de perdre du son.</span><span class="sxs-lookup"><span data-stu-id="e14c5-232">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-233"><strong>Taux de masquage de la réparation</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-233"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-234">Oui</span><span class="sxs-lookup"><span data-stu-id="e14c5-234">Yes</span></span></p></td>
<td><p><span data-ttu-id="e14c5-p122">Ratio moyen d’échantillons audio masqués par rapport au nombre total d’échantillons. (Un échantillon audio masqué est une technique employée pour adoucir les effets de transition violents généralement causés par des paquets réseau perdus.) Des valeurs élevées indiquent des niveaux importants de masquage des pertes appliqués suite à la perte de paquets ou des phénomènes de gigue. Elles se traduisent par une distorsion ou une perte de l’audio.</span><span class="sxs-lookup"><span data-stu-id="e14c5-p122">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-237"><strong>Taux d’étirement de la réparation</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-237"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-238">Oui</span><span class="sxs-lookup"><span data-stu-id="e14c5-238">Yes</span></span></p></td>
<td><p><span data-ttu-id="e14c5-p123">Ratio moyen d’échantillons audio étirés par rapport au nombre total d’échantillons. (Un échantillon audio étiré est un composant audio qui a été étendu dans le but de maintenir la qualité des appels lorsqu’un paquet réseau perdu est détecté.) Les valeurs élevées indiquent l’existence de niveaux importants d’étirement d’échantillons dus au phénomène de gigue, ce qui se traduit par un effet de robotisation ou de distorsion de l’audio.</span><span class="sxs-lookup"><span data-stu-id="e14c5-p123">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-241"><strong>Taux de compression de la réparation</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-241"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-242">Oui</span><span class="sxs-lookup"><span data-stu-id="e14c5-242">Yes</span></span></p></td>
<td><p><span data-ttu-id="e14c5-p124">Ratio moyen d’échantillons audio compressés par rapport au nombre total d’échantillons. (Un échantillon audio compressé est un composant audio qui a été compressé dans le but de maintenir la qualité des appels lorsqu’un paquet réseau perdu est détecté.) Les valeurs élevées indiquent l’existence de niveaux importants de compression d’échantillons dus au phénomène de gigue, ce qui se traduit par un effet d’accélération ou de distorsion de l’audio.</span><span class="sxs-lookup"><span data-stu-id="e14c5-p124">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="server-performance-report-metrics-video-call-summary"></a><span data-ttu-id="e14c5-245">Mesures du rapport de performances du serveur : synthèse des appels vidéo</span><span class="sxs-lookup"><span data-stu-id="e14c5-245">Server Performance Report Metrics: Video Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e14c5-246">Nom</span><span class="sxs-lookup"><span data-stu-id="e14c5-246">Name</span></span></th>
<th><span data-ttu-id="e14c5-247">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="e14c5-247">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e14c5-248">Description</span><span class="sxs-lookup"><span data-stu-id="e14c5-248">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-249"><strong>Type d’appel/type de point de terminaison</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-249"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-250">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-250">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-p125">Lorsque vous cliquez sur cet élément, le rapport affiche des informations détaillées sur les appels en fonction de ce type. Les types d’appels sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="e14c5-p125">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="e14c5-253">Appels P2P UC</span><span class="sxs-lookup"><span data-stu-id="e14c5-253">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="e14c5-254">Sessions de conférence UC</span><span class="sxs-lookup"><span data-stu-id="e14c5-254">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="e14c5-255">Sessions de conférence RTC</span><span class="sxs-lookup"><span data-stu-id="e14c5-255">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="e14c5-256">Appels RTC : contournement du média</span><span class="sxs-lookup"><span data-stu-id="e14c5-256">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="e14c5-257">Appels RTC (sans contournement) : partie UC</span><span class="sxs-lookup"><span data-stu-id="e14c5-257">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="e14c5-258">Appels RTC (sans contournement) : partie passerelle</span><span class="sxs-lookup"><span data-stu-id="e14c5-258">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="e14c5-259">Autres types d’appels</span><span class="sxs-lookup"><span data-stu-id="e14c5-259">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-260"><strong>Volume d’appels</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-260"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-261">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-261">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-262">Nombre total d’appels par type d’appel.</span><span class="sxs-lookup"><span data-stu-id="e14c5-262">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-263"><strong>Pourcentage d’appels médiocres</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-263"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-264">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-264">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-p126">Nombre total d’appels jugés et classés comme étant médiocres. Un appel médiocre désigne un appel dont l’une des valeurs mesurées est supérieure à la valeur autorisée (par exemple, un appel soumis à un phénomène de gigue excessive).</span><span class="sxs-lookup"><span data-stu-id="e14c5-p126">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-267"><strong>Volume d’appels (appels sans fil)</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-267"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-268">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-268">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-269">Nombre total d’appels qui utilisaient une connexion sans fil.</span><span class="sxs-lookup"><span data-stu-id="e14c5-269">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-270"><strong>Volume d’appels (appels VPN)</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-270"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-271">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-271">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-272">Nombre total d’appels qui utilisaient une connexion VPN.</span><span class="sxs-lookup"><span data-stu-id="e14c5-272">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-273"><strong>Volume d’appels (appels externes)</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-273"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-274">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-274">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-275">Nombre d’appels qui utilisaient une connexion externe (c’est-à-dire une connexion en dehors du réseau interne).</span><span class="sxs-lookup"><span data-stu-id="e14c5-275">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-276"><strong>Vitesse de transmission moyenne (Kbit/s)</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-276"><strong>Avg bit-rate (Kbits/s)</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-277">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-277">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-278">Vitesse de transmission vidéo moyenne (en kilobits par seconde).</span><span class="sxs-lookup"><span data-stu-id="e14c5-278">Average video bit rate (in kilobits per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-279"><strong>Vitesse de transmission faible (%)</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-279"><strong>Low bit-rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-280">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-280">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-281">Pourcentage de l’appel où la vitesse de transmission était faible.</span><span class="sxs-lookup"><span data-stu-id="e14c5-281">Percentage of the call where the bit rate was low.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-282"><strong>Perte de paquets sortante</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-282"><strong>Outbound packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-283">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-283">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-p127">Perte de paquets RTP (Real-Time Transport Protocol) pour les paquets sortants. (La perte de paquets survient lorsque des paquets RTP, protocole employé pour la transmission audio et vidéo sur Internet, n’atteignent pas leur point de destination.) Les valeurs de perte élevées peuvent provenir d’une congestion, d’un dépassement de la bande passante disponible, d’une congestion/interférence dans la liaison sans fil ou d’un serveur multimédia surchargé, ce qui se traduit par une distorsion ou une perte de l’audio.</span><span class="sxs-lookup"><span data-stu-id="e14c5-p127">Real-Time Transport Protocol (RTP) packet loss for outbound packets. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-287"><strong>Image figée (%)</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-287"><strong>Frozen frame %</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-288">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-288">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-p128">Pourcentage d’images « figées ». Dans une image figée, la vidéo cesse d’avancer tandis que la partie audio de l’appel continue.</span><span class="sxs-lookup"><span data-stu-id="e14c5-p128">Percentage of “frozen” frames. In a frozen frame, the video stops advancing while the audio portion of the call continues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-291"><strong>Fréquence d’images moyenne sortante</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-291"><strong>Outbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-292">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-292">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-293">Fréquence d’images moyenne pour les transmissions sortantes pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="e14c5-293">Average frame rate for outbound transmissions during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-294"><strong>Fréquence d’images moyenne entrante</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-294"><strong>Inbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-295">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-295">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-296">Fréquence d’images moyenne pour les transmissions entrantes pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="e14c5-296">Average frame rate for incoming transmissions during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-297"><strong>Fréquence d’images basse entrante (%)</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-297"><strong>Inbound low frame rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-298">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-298">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-299">Pourcentage de l’appel où la vitesse de transmission pour la vidéo entrante était faible.</span><span class="sxs-lookup"><span data-stu-id="e14c5-299">Percentage of the call where the bit rate for incoming video was low.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-300"><strong>Intégrité des clients (%)</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-300"><strong>Client health %</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e14c5-301">Indique l’intégrité relative du périphérique client pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="e14c5-301">Indicates the relative health of the client device during the call.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="server-performance-report-metrics-application-sharing-call-summary"></a><span data-ttu-id="e14c5-302">Mesures du rapport de performances du serveur : synthèse des appels de partage d’application</span><span class="sxs-lookup"><span data-stu-id="e14c5-302">Server Performance Report Metrics: Application Sharing Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e14c5-303">Nom</span><span class="sxs-lookup"><span data-stu-id="e14c5-303">Name</span></span></th>
<th><span data-ttu-id="e14c5-304">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="e14c5-304">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e14c5-305">Description</span><span class="sxs-lookup"><span data-stu-id="e14c5-305">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-306"><strong>Type d’appel/type de point de terminaison</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-306"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-307">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-307">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-p129">Lorsque vous cliquez sur cet élément, le rapport affiche des informations détaillées sur les appels en fonction de ce type. Les types d’appels sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="e14c5-p129">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="e14c5-310">Appels P2P UC</span><span class="sxs-lookup"><span data-stu-id="e14c5-310">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="e14c5-311">Sessions de conférence UC</span><span class="sxs-lookup"><span data-stu-id="e14c5-311">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="e14c5-312">Sessions de conférence RTC</span><span class="sxs-lookup"><span data-stu-id="e14c5-312">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="e14c5-313">Appels RTC : contournement du média</span><span class="sxs-lookup"><span data-stu-id="e14c5-313">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="e14c5-314">Appels RTC (sans contournement) : partie UC</span><span class="sxs-lookup"><span data-stu-id="e14c5-314">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="e14c5-315">Appels RTC (sans contournement) : partie passerelle</span><span class="sxs-lookup"><span data-stu-id="e14c5-315">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="e14c5-316">Autres types d’appels</span><span class="sxs-lookup"><span data-stu-id="e14c5-316">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-317"><strong>Volume d’appels</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-317"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-318">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-318">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-319">Nombre total d’appels par type d’appel.</span><span class="sxs-lookup"><span data-stu-id="e14c5-319">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-320"><strong>Pourcentage d’appels médiocres</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-320"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-321">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-321">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-p130">Nombre total d’appels jugés et classés comme étant médiocres. Un appel médiocre désigne un appel dont l’une des valeurs mesurées est supérieure à la valeur autorisée (par exemple, un appel soumis à un phénomène de gigue excessive).</span><span class="sxs-lookup"><span data-stu-id="e14c5-p130">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-324"><strong>Volume d’appels (appels sans fil)</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-324"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-325">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-325">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-326">Nombre total d’appels qui utilisaient une connexion sans fil.</span><span class="sxs-lookup"><span data-stu-id="e14c5-326">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-327"><strong>Volume d’appels (appels VPN)</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-327"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-328">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-328">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-329">Nombre total d’appels qui utilisaient une connexion VPN.</span><span class="sxs-lookup"><span data-stu-id="e14c5-329">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-330"><strong>Volume d’appels (appels externes)</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-330"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-331">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-331">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-332">Nombre d’appels qui utilisaient une connexion externe (c’est-à-dire une connexion en dehors du réseau interne).</span><span class="sxs-lookup"><span data-stu-id="e14c5-332">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-333"><strong>Gigue (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-333"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-334">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-334">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-335">Gigue moyenne détectée entre les arrivées de paquets RTP.</span><span class="sxs-lookup"><span data-stu-id="e14c5-335">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="e14c5-336">(Gigue est une mesure du &quot; shakiness &quot; d’un appel.) Les valeurs de gigue élevée sont généralement provoquées par une congestion ou un serveur multimédia surchargé, ce qui a pour effet de déformer ou de perdre du son.</span><span class="sxs-lookup"><span data-stu-id="e14c5-336">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-337"><strong>Unilatéral relatif moyen</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-337"><strong>Avg. relative one way</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-338">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-338">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-p132">Retard unilatéral relatif moyen entre deux points de terminaison du média. Il s’agit d’une mesure de latence sur un seul tronçon.</span><span class="sxs-lookup"><span data-stu-id="e14c5-p132">Average relative one-way delay between two media endpoints. This is a single-hop latency measure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e14c5-341"><strong>Latence moyenne de traitement des mosaïques RDP</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-341"><strong>Avg. RDP tile processing latency</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-342">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-342">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-p133">Latence moyenne de traitement des mosaïques RDP sur le serveur de conférence AS par rapport à la durée de la session de visionnage. Cette mesure ne couvre pas la latence du réseau. Une moyenne élevée indique un délai plus long pour l’expérience de visionnage. Un serveur de conférence surchargé peut rencontrer des délais moyens plus élevés.</span><span class="sxs-lookup"><span data-stu-id="e14c5-p133">The average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session. This metric does not cover network latency. A high average reflects a longer delay in the viewing experience. An overloaded conferencing server may experience higher average delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e14c5-347"><strong>Nombre total de mosaïques altérées (%)</strong></span><span class="sxs-lookup"><span data-stu-id="e14c5-347"><strong>Total spoiled tile %</strong></span></span></p></td>
<td><p><span data-ttu-id="e14c5-348">Non</span><span class="sxs-lookup"><span data-stu-id="e14c5-348">No</span></span></p></td>
<td><p><span data-ttu-id="e14c5-349">Pourcentage total de mosaïques RDP altérées.</span><span class="sxs-lookup"><span data-stu-id="e14c5-349">Total percentage of spoiled RDP tiles.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e14c5-350">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e14c5-350">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

