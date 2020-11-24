---
title: 'Rapport de distribution de métriques de qualité multimédia Lync Server 2013 :'
description: 'Lync Server 2013 : rapport de distribution des métriques de qualité multimédia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media Quality Metrics Distribution Report
ms:assetid: d07996e6-b0a5-4ff8-9512-ab707762b4e2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205262(v=OCS.15)
ms:contentKeyID: 48185409
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: def56580477dadf989268e1fc24fcec7776c00d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394989"
---
# <a name="the-media-quality-metrics-distribution-report-in-lync-server-2013"></a><span data-ttu-id="38972-103">Rapport de distribution des métriques de qualité multimédia dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="38972-103">The Media Quality Metrics Distribution Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="38972-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="38972-104">

<span> </span></span></span>

<span data-ttu-id="38972-105">_**Dernière modification de la rubrique :** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="38972-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="38972-p101">Le rapport de distribution des mesures de qualité des médias vous permet de consulter un graphique qui affiche les valeurs de distribution pour une mesure de la qualité de l’expérience, comme la gigue ou la perte de paquets. Par exemple, supposons que vos utilisateurs passent un total de 10 appels téléphoniques. Ces 10 appels présentent les délais d’aller-retour suivants :</span><span class="sxs-lookup"><span data-stu-id="38972-p101">The Media Quality Metrics Distribution Report enables you to see a graph that shows the distribution values for a Quality of Experience metric such as jitter or packet loss. For example, suppose your users make a total of 10 phone calls; those 10 calls report the following roundtrip times:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="38972-108">Numéro de l’appel</span><span class="sxs-lookup"><span data-stu-id="38972-108">Call Number</span></span></th>
<th><span data-ttu-id="38972-109">Durée d’aller-retour (millisecondes)</span><span class="sxs-lookup"><span data-stu-id="38972-109">Roundtrip Time (milliseconds)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38972-110">1</span><span class="sxs-lookup"><span data-stu-id="38972-110">1</span></span></p></td>
<td><p><span data-ttu-id="38972-111">50</span><span class="sxs-lookup"><span data-stu-id="38972-111">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38972-112">2</span><span class="sxs-lookup"><span data-stu-id="38972-112">2</span></span></p></td>
<td><p><span data-ttu-id="38972-113">50</span><span class="sxs-lookup"><span data-stu-id="38972-113">50</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38972-114">3</span><span class="sxs-lookup"><span data-stu-id="38972-114">3</span></span></p></td>
<td><p><span data-ttu-id="38972-115">50</span><span class="sxs-lookup"><span data-stu-id="38972-115">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38972-116">4</span><span class="sxs-lookup"><span data-stu-id="38972-116">4</span></span></p></td>
<td><p><span data-ttu-id="38972-117">50</span><span class="sxs-lookup"><span data-stu-id="38972-117">50</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38972-118">5</span><span class="sxs-lookup"><span data-stu-id="38972-118">5</span></span></p></td>
<td><p><span data-ttu-id="38972-119">50</span><span class="sxs-lookup"><span data-stu-id="38972-119">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38972-120">6</span><span class="sxs-lookup"><span data-stu-id="38972-120">6</span></span></p></td>
<td><p><span data-ttu-id="38972-121">50</span><span class="sxs-lookup"><span data-stu-id="38972-121">50</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38972-122">7</span><span class="sxs-lookup"><span data-stu-id="38972-122">7</span></span></p></td>
<td><p><span data-ttu-id="38972-123">50</span><span class="sxs-lookup"><span data-stu-id="38972-123">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38972-124">version8</span><span class="sxs-lookup"><span data-stu-id="38972-124">8</span></span></p></td>
<td><p><span data-ttu-id="38972-125">4550</span><span class="sxs-lookup"><span data-stu-id="38972-125">4550</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38972-126">09</span><span class="sxs-lookup"><span data-stu-id="38972-126">9</span></span></p></td>
<td><p><span data-ttu-id="38972-127">50</span><span class="sxs-lookup"><span data-stu-id="38972-127">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38972-128">0,10</span><span class="sxs-lookup"><span data-stu-id="38972-128">10</span></span></p></td>
<td><p><span data-ttu-id="38972-129">50</span><span class="sxs-lookup"><span data-stu-id="38972-129">50</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="38972-130">La moyenne de ces temps d’aller-retour est de 500 millisecondes (5000 divisée par 10).</span><span class="sxs-lookup"><span data-stu-id="38972-130">The average for those roundtrip times is 500 milliseconds (5000 divided by 10).</span></span> <span data-ttu-id="38972-131">500 millisecondes est une durée de roundtrip très importante ; par conséquent, il est possible que vous rencontriez un problème sérieux avec la congestion du réseau.</span><span class="sxs-lookup"><span data-stu-id="38972-131">Five hundred milliseconds is an extremely large roundtrip time; as a result, you might believe that you have a serious problem with network congestion.</span></span> <span data-ttu-id="38972-132">(Les temps de roundtrip longs sont généralement le résultat de réseaux surchargés.)</span><span class="sxs-lookup"><span data-stu-id="38972-132">(Long roundtrip times are typically the result of overloaded networks.)</span></span>

<span data-ttu-id="38972-133">Pour le moment, le nombre de fois que 90% de vos appels avait des temps d’aller-retour exceptionnels. il vous suffit d’un appel incorrect qui a faussé les résultats globaux.</span><span class="sxs-lookup"><span data-stu-id="38972-133">In reality, of course, 90% of your calls had excellent round trip times; you merely had one bad call that skewed the overall results.</span></span> <span data-ttu-id="38972-134">Si vous observez uniquement la durée de l’aller-retour moyenne, vous risquez de sauter une erreur de conclusion.</span><span class="sxs-lookup"><span data-stu-id="38972-134">If you only look at the average roundtrip time you might jump to a very wrong conclusion.</span></span>

<span data-ttu-id="38972-p104">Le rapport de distribution des mesures de qualité des médias vous permet de ne pas tirer de conclusions hâtives et erronées : il vous présente une répartition graphique d’une mesure précise (comme le délai d’aller-retour). Ces graphiques permettent de clarifier la situation, à savoir que vous avez passé neuf appels de très bonne qualité et un de mauvaise qualité. Vous souhaitez peut-être examiner plus en détail cet appel-ci. Cependant, le fait que 9 appels sur 10 étaient de bonne qualité semble indiquer qu’il n’existe aucune raison d’apporter des modifications radicales à votre réseau, au moins pas pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="38972-p104">The Media Quality Metrics Distribution Report helps you avoid jumping to wrong conclusions by showing you a graphical distribution of a specified metric (such as round trip time). These graphs can help make it clear that you had nine very good calls and one very bad call. Admittedly, you might still want to further investigate that one call; however, the fact that 9 out of the 10 calls were very good suggests that there is no reason to make any drastic changes to your network, at least not at this point in time.</span></span>

<div>

## <a name="filters"></a><span data-ttu-id="38972-138">Filtres</span><span class="sxs-lookup"><span data-stu-id="38972-138">Filters</span></span>

<span data-ttu-id="38972-p105">Les filtres vous offrent la possibilité de renvoyer un ensemble de données mieux ciblées ou de visualiser les données renvoyées de différentes manières. Le tableau suivant dresse la liste des filtres que vous pouvez utiliser avec le rapport de distribution des mesures de qualité des médias.</span><span class="sxs-lookup"><span data-stu-id="38972-p105">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Media Quality Metrics Distribution Report.</span></span>

### <a name="media-quality-metrics-distribution-report-filters"></a><span data-ttu-id="38972-141">Filtres du rapport de distribution des mesures de qualité des médias</span><span class="sxs-lookup"><span data-stu-id="38972-141">Media Quality Metrics Distribution Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="38972-142">Nom</span><span class="sxs-lookup"><span data-stu-id="38972-142">Name</span></span></th>
<th><span data-ttu-id="38972-143">Description</span><span class="sxs-lookup"><span data-stu-id="38972-143">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38972-144"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="38972-144"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="38972-p106">Date/heure de début de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de début comme suit :</span><span class="sxs-lookup"><span data-stu-id="38972-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="38972-147">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="38972-147">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="38972-p107">Si vous ne précisez aucune heure de début, le rapport commence automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="38972-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="38972-150">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="38972-150">7/7/2012</span></span></p>
<p><span data-ttu-id="38972-151">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="38972-151">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="38972-152">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="38972-152">7/3/2012</span></span></p>
<p><span data-ttu-id="38972-153">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="38972-153">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38972-154"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="38972-154"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="38972-p108">Date/heure de fin de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de fin comme suit :</span><span class="sxs-lookup"><span data-stu-id="38972-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="38972-157">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="38972-157">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="38972-p109">Si vous ne précisez aucune heure de fin, le rapport se termine automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="38972-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="38972-160">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="38972-160">7/7/2012</span></span></p>
<p><span data-ttu-id="38972-161">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="38972-161">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="38972-162">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="38972-162">7/3/2012</span></span></p>
<p><span data-ttu-id="38972-163">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="38972-163">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38972-164"><strong>Minimum sur l’axe x</strong></span><span class="sxs-lookup"><span data-stu-id="38972-164"><strong>Minimum in x axis</strong></span></span></p></td>
<td><p><span data-ttu-id="38972-165">Plus petite valeur à afficher sur l’axe X du graphique.</span><span class="sxs-lookup"><span data-stu-id="38972-165">Lowest value to be displayed on the X axis of the graph.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38972-166"><strong>Maximum sur l’axe x</strong></span><span class="sxs-lookup"><span data-stu-id="38972-166"><strong>Maximum in x axis</strong></span></span></p></td>
<td><p><span data-ttu-id="38972-167">Plus grande valeur à afficher sur l’axe X du graphique.</span><span class="sxs-lookup"><span data-stu-id="38972-167">Highest value to be displayed on the X axis of the graph.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38972-168"><strong>Type d’accès</strong></span><span class="sxs-lookup"><span data-stu-id="38972-168"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="38972-p110">Indique si le client était connecté au réseau interne ou au réseau externe au moment de passer l’appel. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="38972-p110">Indicates whether the client was logged on to the internal network or the external network when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="38972-171">[Tous]</span><span class="sxs-lookup"><span data-stu-id="38972-171">[All]</span></span></p></li>
<li><p><span data-ttu-id="38972-172">Interne</span><span class="sxs-lookup"><span data-stu-id="38972-172">Internal</span></span></p></li>
<li><p><span data-ttu-id="38972-173">Externe</span><span class="sxs-lookup"><span data-stu-id="38972-173">External</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38972-174"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="38972-174"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="38972-p111">Indique si un client externe utilisait une connexion de réseau privé virtuel (VPN) au moment d’effectuer l’appel. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="38972-p111">Indicates whether an external client was using a virtual private network (VPN) connection when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="38972-177">[Tous]</span><span class="sxs-lookup"><span data-stu-id="38972-177">[All]</span></span></p></li>
<li><p><span data-ttu-id="38972-178">VPN</span><span class="sxs-lookup"><span data-stu-id="38972-178">VPN</span></span></p></li>
<li><p><span data-ttu-id="38972-179">Non-VPN</span><span class="sxs-lookup"><span data-stu-id="38972-179">Non-VPN</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38972-180"><strong>Type de réseau</strong></span><span class="sxs-lookup"><span data-stu-id="38972-180"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="38972-p112">Indique le type de réseau auquel le client était connecté au moment où l’appel a été émis. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="38972-p112">Indicates the type of network the client was connected to when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="38972-183">[Tous]</span><span class="sxs-lookup"><span data-stu-id="38972-183">[All]</span></span></p></li>
<li><p><span data-ttu-id="38972-184">Câblé</span><span class="sxs-lookup"><span data-stu-id="38972-184">Wired</span></span></p></li>
<li><p><span data-ttu-id="38972-185">Sans fil</span><span class="sxs-lookup"><span data-stu-id="38972-185">Wireless</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="38972-186">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="38972-186">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

