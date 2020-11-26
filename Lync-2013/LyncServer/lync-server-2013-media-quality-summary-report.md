---
title: 'Lync Server 2013 : rapport de synthèse sur la qualité multimédia'
description: 'Lync Server 2013 : rapport de synthèse sur la qualité multimédia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media Quality Summary Report
ms:assetid: 8bd59ad6-3087-49c8-b692-5573fe2ffcd8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615012(v=OCS.15)
ms:contentKeyID: 48184776
ms.date: 06/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2616b7e3cdea9df7b004745a5c407188870903c7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446044"
---
# <a name="media-quality-summary-report-in-lync-server-2013"></a><span data-ttu-id="06680-103">Rapport synthèse qualité multimédia dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="06680-103">Media Quality Summary Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="06680-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="06680-104">

<span> </span></span></span>

<span data-ttu-id="06680-105">_**Dernière modification de la rubrique :** 2016-06-29_</span><span class="sxs-lookup"><span data-stu-id="06680-105">_**Topic Last Modified:** 2016-06-29_</span></span>

<span data-ttu-id="06680-106">Le rapport de synthèse de la qualité des médias permet d’analyser la qualité des appels au sein de votre organisation : ce rapport fournit des mesures d’appel de qualité de l’expérience (QoE) détaillées décomposées selon les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="06680-106">The Media Quality Summary Report is perhaps your best bet for analyzing call quality in your organization: this report provides detailed Quality of Experience (QoE) call metrics broken down into the following categories:</span></span>

  - <span data-ttu-id="06680-107">Appels d’égal à égal (par exemple, Microsoft Lync 2013 vers Microsoft Lync 2013)</span><span class="sxs-lookup"><span data-stu-id="06680-107">UC Peer to Peer Calls (such as a Microsoft Lync 2013 to Microsoft Lync 2013 call)</span></span>

  - <span data-ttu-id="06680-108">Sessions de conférence UC</span><span class="sxs-lookup"><span data-stu-id="06680-108">UC Conference Sessions</span></span>

  - <span data-ttu-id="06680-109">Sessions de conférence RTC</span><span class="sxs-lookup"><span data-stu-id="06680-109">PSTN Conference Sessions</span></span>

  - <span data-ttu-id="06680-110">Appels RTC : contournement du média</span><span class="sxs-lookup"><span data-stu-id="06680-110">PSTN Calls: Media Bypass</span></span>

  - <span data-ttu-id="06680-111">Appels RTC (sans contournement) : partie UC</span><span class="sxs-lookup"><span data-stu-id="06680-111">PSTN Calls (Non-Bypass): UC Leg</span></span>

  - <span data-ttu-id="06680-112">Appels RTC (sans contournement) : partie passerelle</span><span class="sxs-lookup"><span data-stu-id="06680-112">PSTN Calls (Non-Bypass): Gateway Leg</span></span>

  - <span data-ttu-id="06680-113">Autres types d’appels</span><span class="sxs-lookup"><span data-stu-id="06680-113">Other Call Types</span></span>

<span data-ttu-id="06680-114">Quand vous ouvrez le rapport pour la première fois, une synthèse des informations pour chaque catégorie s’affiche.</span><span class="sxs-lookup"><span data-stu-id="06680-114">When you first open the report, you see summary information for each of these categories.</span></span> <span data-ttu-id="06680-115">Sans quitter le rapport, vous pouvez développer chaque catégorie pour afficher des sous-catégories, comme les appels passés à partir d’Office Communicator 2007 R2 vers Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="06680-115">Without leaving the report, you can expand each category to look at subcategories such as calls made from Office Communicator 2007 R2 to Lync 2013.</span></span> <span data-ttu-id="06680-116">Vous pouvez développer également ces sous-catégories pour afficher des détails sur chaque appel passé dans cette sous-catégorie.</span><span class="sxs-lookup"><span data-stu-id="06680-116">In turn, you can then drill down into these subcategories to see details about each call made within that subcategory.</span></span>

<span data-ttu-id="06680-117">Dans Microsoft Lync Server 2013, le rapport synthèse qualité multimédia répartit les données en trois types d’appels : les appels audio, les appels vidéo et les appels de partage d’application.</span><span class="sxs-lookup"><span data-stu-id="06680-117">In Microsoft Lync Server 2013 the Media Quality Summary Report further breaks the data down into three call types: audio calls, video calls, and application sharing calls.</span></span> <span data-ttu-id="06680-118">Chaque type d’appel correspond à une section du rapport, et dispose d’un ensemble personnalisé de mesures des appels.</span><span class="sxs-lookup"><span data-stu-id="06680-118">Each call type has its own section in the report, and its own custom set of call metrics.</span></span>

<span data-ttu-id="06680-119">Le rapport de synthèse de la qualité des médias vous permet d’appliquer des filtres pour comparer la qualité des appels entre les appels câblés et les appels sans fil, les appels internes et externes, les appels VPN et non VPN.</span><span class="sxs-lookup"><span data-stu-id="06680-119">The Media Quality Summary Report also allows you to apply filters that enable you to compare the call quality of wired calls vs. wireless calls, internal calls vs. external calls, and VPN calls vs. non-VPN calls.</span></span>

<div>

## <a name="accessing-the-media-quality-summary-report"></a><span data-ttu-id="06680-120">Accès au rapport de synthèse de la qualité des médias</span><span class="sxs-lookup"><span data-stu-id="06680-120">Accessing the Media Quality Summary Report</span></span>

<span data-ttu-id="06680-121">Le rapport de synthèse de la qualité des médias est accessible à partir de la page d’accueil Rapports de surveillance.</span><span class="sxs-lookup"><span data-stu-id="06680-121">The Media Quality Summary Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="06680-122">Vous pouvez explorer le rapport de la [liste d’appels dans Lync Server 2013](lync-server-2013-call-list-report.md) en cliquant sur l’une des mesures suivantes :</span><span class="sxs-lookup"><span data-stu-id="06680-122">You can drill down to the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="06680-123">Volume d’appels</span><span class="sxs-lookup"><span data-stu-id="06680-123">Call volume</span></span>

  - <span data-ttu-id="06680-124">Pourcentage d’appels médiocres</span><span class="sxs-lookup"><span data-stu-id="06680-124">Poor call percentage</span></span>

<span data-ttu-id="06680-125">De plus, vous pouvez accéder au Rapport de distribution des mesures de qualité des médias en cliquant sur l’une des mesures d’appel audio suivantes :</span><span class="sxs-lookup"><span data-stu-id="06680-125">In addition, you can access the Media Quality Metrics Distribution Report by clicking any of the following audio call metrics:</span></span>

  - <span data-ttu-id="06680-126">Boucle (ms)</span><span class="sxs-lookup"><span data-stu-id="06680-126">Round trip (ms)</span></span>

  - <span data-ttu-id="06680-127">Dégradation (MOS)</span><span class="sxs-lookup"><span data-stu-id="06680-127">Degradation (MOS)</span></span>

  - <span data-ttu-id="06680-128">Perte de paquets</span><span class="sxs-lookup"><span data-stu-id="06680-128">Packet loss</span></span>

  - <span data-ttu-id="06680-129">Gigue (ms)</span><span class="sxs-lookup"><span data-stu-id="06680-129">Jitter (ms)</span></span>

  - <span data-ttu-id="06680-130">Taux de masquage de la réparation</span><span class="sxs-lookup"><span data-stu-id="06680-130">Healer concealed ratio</span></span>

  - <span data-ttu-id="06680-131">Taux d’étirement de la réparation</span><span class="sxs-lookup"><span data-stu-id="06680-131">Healer stretched ratio</span></span>

  - <span data-ttu-id="06680-132">Taux de compression de la réparation</span><span class="sxs-lookup"><span data-stu-id="06680-132">Healer compressed ratio</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="06680-133">Filtres</span><span class="sxs-lookup"><span data-stu-id="06680-133">Filters</span></span>

<span data-ttu-id="06680-p104">Les filtres vous offrent la possibilité de renvoyer un ensemble de données mieux ciblées ou de visualiser les données renvoyées de différentes manières. Par exemple, grâce au rapport de synthèse de la qualité des médias, vous pouvez filtrer les données renvoyées selon des éléments précis, tels que le type d’accès (à savoir « accès interne » par comparaison à « accès externe ») ou la connexion réseau câblée/sans fil. Vous pouvez également choisir le mode de groupement des données. Dans ce cas, les appels sont groupés par heure, jour, semaine ou mois.</span><span class="sxs-lookup"><span data-stu-id="06680-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Media Quality Summary Report enables you to filter the returned data by such things as access type (that is, interval access vs. external access) or by wired/wireless network connection. You can also choose how data should be grouped. In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="06680-138">Le tableau qui suit dresse la liste des filtres que vous pouvez utiliser avec le rapport de synthèse de la qualité des médias.</span><span class="sxs-lookup"><span data-stu-id="06680-138">The following table lists the filters that you can use with the Media Quality Summary Report.</span></span>

### <a name="media-quality-summary-report-filters"></a><span data-ttu-id="06680-139">Filtres du rapport de synthèse de la qualité des médias</span><span class="sxs-lookup"><span data-stu-id="06680-139">Media Quality Summary Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06680-140">Nom</span><span class="sxs-lookup"><span data-stu-id="06680-140">Name</span></span></th>
<th><span data-ttu-id="06680-141">Description</span><span class="sxs-lookup"><span data-stu-id="06680-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06680-142"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="06680-142"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-p105">Date/heure de début de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de début comme suit :</span><span class="sxs-lookup"><span data-stu-id="06680-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="06680-145">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="06680-145">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="06680-p106">Si vous ne précisez aucune heure de début, le rapport commence automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="06680-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="06680-148">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="06680-148">7/7/2012</span></span></p>
<p><span data-ttu-id="06680-149">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="06680-149">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="06680-150">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="06680-150">7/3/2012</span></span></p>
<p><span data-ttu-id="06680-151">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="06680-151">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-152"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="06680-152"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-p107">Date/heure de fin de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de fin comme suit :</span><span class="sxs-lookup"><span data-stu-id="06680-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="06680-155">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="06680-155">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="06680-p108">Si vous ne précisez aucune heure de fin, le rapport se termine automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="06680-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="06680-158">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="06680-158">7/7/2012</span></span></p>
<p><span data-ttu-id="06680-159">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="06680-159">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="06680-160">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="06680-160">7/3/2012</span></span></p>
<p><span data-ttu-id="06680-161">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="06680-161">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-162"><strong>Type d’accès</strong></span><span class="sxs-lookup"><span data-stu-id="06680-162"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-p109">Indique si le client était connecté au réseau interne ou au réseau externe au moment de passer l’appel. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="06680-p109">Indicates whether the client was logged on to the internal network or the external network when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="06680-165">[Tous]</span><span class="sxs-lookup"><span data-stu-id="06680-165">[All]</span></span></p></li>
<li><p><span data-ttu-id="06680-166">Interne</span><span class="sxs-lookup"><span data-stu-id="06680-166">Internal</span></span></p></li>
<li><p><span data-ttu-id="06680-167">Externe</span><span class="sxs-lookup"><span data-stu-id="06680-167">External</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-168"><strong>Type de réseau</strong></span><span class="sxs-lookup"><span data-stu-id="06680-168"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-p110">Indique le type de réseau auquel le client était connecté au moment où l’appel a été émis. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="06680-p110">Indicates the type of network the client was connected to when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="06680-171">[Tous]</span><span class="sxs-lookup"><span data-stu-id="06680-171">[All]</span></span></p></li>
<li><p><span data-ttu-id="06680-172">Câblé</span><span class="sxs-lookup"><span data-stu-id="06680-172">Wired</span></span></p></li>
<li><p><span data-ttu-id="06680-173">Sans fil</span><span class="sxs-lookup"><span data-stu-id="06680-173">Wireless</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-174"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="06680-174"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-p111">Indique si un client externe utilisait une connexion de réseau privé virtuel (VPN) au moment d’effectuer l’appel. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="06680-p111">Indicates whether an external client was using a virtual private network (VPN) connection when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="06680-177">[Tous]</span><span class="sxs-lookup"><span data-stu-id="06680-177">[All]</span></span></p></li>
<li><p><span data-ttu-id="06680-178">VPN</span><span class="sxs-lookup"><span data-stu-id="06680-178">VPN</span></span></p></li>
<li><p><span data-ttu-id="06680-179">Non-VPN</span><span class="sxs-lookup"><span data-stu-id="06680-179">Non-VPN</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="06680-180">Mesures</span><span class="sxs-lookup"><span data-stu-id="06680-180">Metrics</span></span>

<span data-ttu-id="06680-181">Le tableau qui suit répertorie les informations fournies dans le rapport de synthèse de la qualité des médias.</span><span class="sxs-lookup"><span data-stu-id="06680-181">The following table lists the information provided in the Media Quality Summary Report.</span></span>

### <a name="media-quality-summary-report-metrics-audio-call-summary"></a><span data-ttu-id="06680-182">Mesures du rapport de synthèse de la qualité des médias : synthèse des appels audio</span><span class="sxs-lookup"><span data-stu-id="06680-182">Media Quality Summary Report Metrics: Audio Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06680-183">Nom</span><span class="sxs-lookup"><span data-stu-id="06680-183">Name</span></span></th>
<th><span data-ttu-id="06680-184">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="06680-184">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="06680-185">Description</span><span class="sxs-lookup"><span data-stu-id="06680-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06680-186"><strong>Type d’appel/type de point de terminaison</strong></span><span class="sxs-lookup"><span data-stu-id="06680-186"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-187">Non</span><span class="sxs-lookup"><span data-stu-id="06680-187">No</span></span></p></td>
<td><p><span data-ttu-id="06680-p112">Lorsque vous cliquez sur cet élément, le rapport affiche des informations détaillées sur les appels en fonction de ce type. Les types d’appels sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="06680-p112">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="06680-190">Appels P2P UC</span><span class="sxs-lookup"><span data-stu-id="06680-190">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="06680-191">Sessions de conférence UC</span><span class="sxs-lookup"><span data-stu-id="06680-191">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="06680-192">Sessions de conférence RTC</span><span class="sxs-lookup"><span data-stu-id="06680-192">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="06680-193">Appels RTC : contournement du média</span><span class="sxs-lookup"><span data-stu-id="06680-193">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="06680-194">Appels RTC (sans contournement) : partie UC</span><span class="sxs-lookup"><span data-stu-id="06680-194">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="06680-195">Appels RTC (sans contournement) : partie passerelle</span><span class="sxs-lookup"><span data-stu-id="06680-195">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="06680-196">Autres types d’appels</span><span class="sxs-lookup"><span data-stu-id="06680-196">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-197"><strong>Volume d’appels</strong></span><span class="sxs-lookup"><span data-stu-id="06680-197"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-198">Non</span><span class="sxs-lookup"><span data-stu-id="06680-198">No</span></span></p></td>
<td><p><span data-ttu-id="06680-199">Nombre total d’appels par type d’appel.</span><span class="sxs-lookup"><span data-stu-id="06680-199">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-200"><strong>Pourcentage d’appels médiocres</strong></span><span class="sxs-lookup"><span data-stu-id="06680-200"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-201">Non</span><span class="sxs-lookup"><span data-stu-id="06680-201">No</span></span></p></td>
<td><p><span data-ttu-id="06680-p113">Nombre total d’appels jugés et classés comme étant médiocres. Un appel médiocre désigne un appel dont l’une des valeurs mesurées est supérieure à la valeur autorisée (par exemple, un appel soumis à un phénomène de gigue excessive).</span><span class="sxs-lookup"><span data-stu-id="06680-p113">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-204"><strong>Volume d’appels (appels sans fil)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-204"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-205">Non</span><span class="sxs-lookup"><span data-stu-id="06680-205">No</span></span></p></td>
<td><p><span data-ttu-id="06680-206">Nombre total d’appels qui utilisaient une connexion sans fil.</span><span class="sxs-lookup"><span data-stu-id="06680-206">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-207"><strong>Volume d’appels (appels VPN)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-207"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-208">Non</span><span class="sxs-lookup"><span data-stu-id="06680-208">No</span></span></p></td>
<td><p><span data-ttu-id="06680-209">Nombre total d’appels qui utilisaient une connexion VPN.</span><span class="sxs-lookup"><span data-stu-id="06680-209">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-210"><strong>Volume d’appels (appels externes)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-210"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-211">Non</span><span class="sxs-lookup"><span data-stu-id="06680-211">No</span></span></p></td>
<td><p><span data-ttu-id="06680-212">Nombre d’appels qui utilisaient une connexion externe (c’est-à-dire une connexion en dehors du réseau interne).</span><span class="sxs-lookup"><span data-stu-id="06680-212">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-213"><strong>Boucle (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-213"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-214">Non</span><span class="sxs-lookup"><span data-stu-id="06680-214">No</span></span></p></td>
<td><p><span data-ttu-id="06680-p114">Temps moyen (en millisecondes) nécessaire à un package RTP (Real-Time Transport Protocol) pour effectuer un aller-retour vers un autre point de terminaison. Des boucles de 100 millisecondes ou moins sont considérées qualitativement acceptables.</span><span class="sxs-lookup"><span data-stu-id="06680-p114">Average amount of (in milliseconds) required for a real-time transport protocol (RTP) packet to travel to another endpoint and then back. Round-trip times of 100 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="06680-p115">Des boucles avec des temps plus élevés peuvent être causées par le routage international des appels, une mauvaise configuration du routage ou un serveur multimédia surchargé. Les temps d’aller-retour élevés créent des difficultés dans le cadre de conversations audio bidirectionnelles réalisées en temps réel.</span><span class="sxs-lookup"><span data-stu-id="06680-p115">High round-trip values can be caused by international call routing, a routing misconfiguration, or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-219"><strong>Dégradation (MOS)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-219"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-220">Non</span><span class="sxs-lookup"><span data-stu-id="06680-220">No</span></span></p></td>
<td><p><span data-ttu-id="06680-221">Taux moyen de dégradation de la note moyenne d’opinion (MOS) observé au cours d’un appel.</span><span class="sxs-lookup"><span data-stu-id="06680-221">Average amount of mean opinion score (MOS) degradation experienced during a call.</span></span> <span data-ttu-id="06680-222">Les valeurs de dégradation peuvent aller de 0,0 (la plus faible) à 5,0 (la plus élevée).</span><span class="sxs-lookup"><span data-stu-id="06680-222">Degradation values can range from a low of 0.0 to a high of 5.0.</span></span> <span data-ttu-id="06680-223">Une valeur de 0,5 ou moins signifie une dégradation acceptable.</span><span class="sxs-lookup"><span data-stu-id="06680-223">A value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="06680-224">Traditionnellement, les notes moyennes d’opinion sont calculées en demandant aux utilisateurs d’évaluer la qualité d’un appel sur une échelle de 1 à 5.</span><span class="sxs-lookup"><span data-stu-id="06680-224">Historically, mean options scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="06680-225">Dans Lync Server, Lync Server utilise un ensemble d’algorithmes pour prévoir la façon dont les utilisateurs auraient noté un appel.</span><span class="sxs-lookup"><span data-stu-id="06680-225">In Lync Server, Lync Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="06680-p117">Les valeurs de dégradation élevées peuvent provenir d’une congestion, d’un dépassement de la bande passante disponible, d’une congestion/interférence dans la liaison sans fil ou bien d’un serveur multimédia ou d’un point de terminaison surchargé, ce qui se traduit par une distorsion ou une perte de l’audio.</span><span class="sxs-lookup"><span data-stu-id="06680-p117">High degradation values can be caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-228"><strong>Perte de paquets</strong></span><span class="sxs-lookup"><span data-stu-id="06680-228"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-229">Non</span><span class="sxs-lookup"><span data-stu-id="06680-229">No</span></span></p></td>
<td><p><span data-ttu-id="06680-p118">Taux moyen de pertes de paquets RTP. (La perte de paquets survient lorsque des paquets RTP, protocole employé pour la transmission audio et vidéo sur Internet, n’atteignent pas leur point de destination.) Les valeurs de perte élevées peuvent provenir d’une congestion, d’un dépassement de la bande passante disponible, d’une congestion/interférence dans la liaison sans fil ou d’un serveur multimédia surchargé, ce qui se traduit par une distorsion ou une perte de l’audio.</span><span class="sxs-lookup"><span data-stu-id="06680-p118">Average rate of RTP packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-233"><strong>Gigue (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-233"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-234">Non</span><span class="sxs-lookup"><span data-stu-id="06680-234">No</span></span></p></td>
<td><p><span data-ttu-id="06680-235">Gigue moyenne détectée entre les arrivées de paquets RTP.</span><span class="sxs-lookup"><span data-stu-id="06680-235">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="06680-236">(Gigue est une mesure du &quot; shakiness &quot; d’un appel.) Les valeurs de gigue élevée sont généralement provoquées par une congestion ou un serveur multimédia surchargé, ce qui a pour effet de déformer ou de perdre du son.</span><span class="sxs-lookup"><span data-stu-id="06680-236">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-237"><strong>Taux de masquage de la réparation</strong></span><span class="sxs-lookup"><span data-stu-id="06680-237"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-238">Non</span><span class="sxs-lookup"><span data-stu-id="06680-238">No</span></span></p></td>
<td><p><span data-ttu-id="06680-p120">Ratio moyen d’échantillons audio masqués par rapport au nombre total d’échantillons. (Un échantillon audio masqué est une technique employée pour adoucir les effets de transition violents généralement causés par des paquets réseau perdus.) Des valeurs élevées indiquent des niveaux importants de masquage des pertes appliqués suite à la perte de paquets ou des phénomènes de gigue. Elles se traduisent par une distorsion ou une perte de l’audio.</span><span class="sxs-lookup"><span data-stu-id="06680-p120">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-241"><strong>Taux d’étirement de la réparation</strong></span><span class="sxs-lookup"><span data-stu-id="06680-241"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-242">Non</span><span class="sxs-lookup"><span data-stu-id="06680-242">No</span></span></p></td>
<td><p><span data-ttu-id="06680-p121">Ratio moyen d’échantillons audio étirés par rapport au nombre total d’échantillons. (Un échantillon audio étiré est un composant audio qui a été étendu dans le but de maintenir la qualité des appels lorsqu’un paquet réseau perdu est détecté.) Les valeurs élevées indiquent l’existence de niveaux importants d’étirement d’échantillons dus au phénomène de gigue, ce qui se traduit par un effet de robotisation ou de distorsion de l’audio.</span><span class="sxs-lookup"><span data-stu-id="06680-p121">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-245"><strong>Taux de compression de la réparation</strong></span><span class="sxs-lookup"><span data-stu-id="06680-245"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-246">Non</span><span class="sxs-lookup"><span data-stu-id="06680-246">No</span></span></p></td>
<td><p><span data-ttu-id="06680-p122">Ratio moyen d’échantillons audio compressés par rapport au nombre total d’échantillons. (Un échantillon audio compressé est un composant audio qui a été compressé dans le but de maintenir la qualité des appels lorsqu’un paquet réseau perdu est détecté.) Les valeurs élevées indiquent l’existence de niveaux importants de compression d’échantillons dus au phénomène de gigue, ce qui se traduit par un effet d’accélération ou de distorsion de l’audio.</span><span class="sxs-lookup"><span data-stu-id="06680-p122">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="media-quality-summary-report-metrics-video-call-summary"></a><span data-ttu-id="06680-249">Mesures du rapport de synthèse de la qualité des médias : synthèse des appels vidéo</span><span class="sxs-lookup"><span data-stu-id="06680-249">Media Quality Summary Report Metrics: Video Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06680-250">Nom</span><span class="sxs-lookup"><span data-stu-id="06680-250">Name</span></span></th>
<th><span data-ttu-id="06680-251">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="06680-251">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="06680-252">Description</span><span class="sxs-lookup"><span data-stu-id="06680-252">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06680-253"><strong>Type d’appel/type de point de terminaison</strong></span><span class="sxs-lookup"><span data-stu-id="06680-253"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-254">Non</span><span class="sxs-lookup"><span data-stu-id="06680-254">No</span></span></p></td>
<td><p><span data-ttu-id="06680-p123">Lorsque vous cliquez sur cet élément, le rapport affiche des informations détaillées sur les appels en fonction de ce type. Les types d’appels sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="06680-p123">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="06680-257">Appels P2P UC</span><span class="sxs-lookup"><span data-stu-id="06680-257">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="06680-258">Sessions de conférence UC</span><span class="sxs-lookup"><span data-stu-id="06680-258">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="06680-259">Sessions de conférence RTC</span><span class="sxs-lookup"><span data-stu-id="06680-259">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="06680-260">Appels RTC : contournement du média</span><span class="sxs-lookup"><span data-stu-id="06680-260">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="06680-261">Appels RTC (sans contournement) : partie UC</span><span class="sxs-lookup"><span data-stu-id="06680-261">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="06680-262">Appels RTC (sans contournement) : partie passerelle</span><span class="sxs-lookup"><span data-stu-id="06680-262">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="06680-263">Autres types d’appels</span><span class="sxs-lookup"><span data-stu-id="06680-263">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-264"><strong>Volume d’appels</strong></span><span class="sxs-lookup"><span data-stu-id="06680-264"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-265">Non</span><span class="sxs-lookup"><span data-stu-id="06680-265">No</span></span></p></td>
<td><p><span data-ttu-id="06680-266">Nombre total d’appels par type d’appel.</span><span class="sxs-lookup"><span data-stu-id="06680-266">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-267"><strong>Pourcentage d’appels médiocres</strong></span><span class="sxs-lookup"><span data-stu-id="06680-267"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-268">Non</span><span class="sxs-lookup"><span data-stu-id="06680-268">No</span></span></p></td>
<td><p><span data-ttu-id="06680-p124">Nombre total d’appels jugés et classés comme étant médiocres. Un appel médiocre désigne un appel dont l’une des valeurs mesurées est supérieure à la valeur autorisée (par exemple, un appel soumis à un phénomène de gigue excessive).</span><span class="sxs-lookup"><span data-stu-id="06680-p124">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-271"><strong>Volume d’appels (appels sans fil)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-271"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-272">Non</span><span class="sxs-lookup"><span data-stu-id="06680-272">No</span></span></p></td>
<td><p><span data-ttu-id="06680-273">Nombre total d’appels qui utilisaient une connexion sans fil.</span><span class="sxs-lookup"><span data-stu-id="06680-273">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-274"><strong>Volume d’appels (appels VPN)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-274"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-275">Non</span><span class="sxs-lookup"><span data-stu-id="06680-275">No</span></span></p></td>
<td><p><span data-ttu-id="06680-276">Nombre total d’appels qui utilisaient une connexion VPN.</span><span class="sxs-lookup"><span data-stu-id="06680-276">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-277"><strong>Volume d’appels (appels externes)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-277"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-278">Non</span><span class="sxs-lookup"><span data-stu-id="06680-278">No</span></span></p></td>
<td><p><span data-ttu-id="06680-279">Nombre d’appels qui utilisaient une connexion externe (c’est-à-dire une connexion en dehors du réseau interne).</span><span class="sxs-lookup"><span data-stu-id="06680-279">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-280"><strong>Vitesse de transmission moyenne (Kbit/s)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-280"><strong>Avg bit-rate (Kbits/s)</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-281">Non</span><span class="sxs-lookup"><span data-stu-id="06680-281">No</span></span></p></td>
<td><p><span data-ttu-id="06680-282">Vitesse de transmission vidéo moyenne (en kilobits par seconde).</span><span class="sxs-lookup"><span data-stu-id="06680-282">Average video bit rate (in kilobits per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-283"><strong>Vitesse de transmission faible (%)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-283"><strong>Low bit-rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-284">Non</span><span class="sxs-lookup"><span data-stu-id="06680-284">No</span></span></p></td>
<td><p><span data-ttu-id="06680-285">Pourcentage de l’appel où la vitesse de transmission était faible.</span><span class="sxs-lookup"><span data-stu-id="06680-285">Percentage of the call where the bit rate was low.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-286"><strong>Perte de paquets sortante</strong></span><span class="sxs-lookup"><span data-stu-id="06680-286"><strong>Outbound packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-287">Non</span><span class="sxs-lookup"><span data-stu-id="06680-287">No</span></span></p></td>
<td><p><span data-ttu-id="06680-p125">Perte de paquets RTP (Real-Time Transport Protocol) pour les paquets sortants. (La perte de paquets survient lorsque des paquets RTP, protocole employé pour la transmission audio et vidéo sur Internet, n’atteignent pas leur point de destination.) Les valeurs de perte élevées peuvent provenir d’une congestion, d’un dépassement de la bande passante disponible, d’une congestion/interférence dans la liaison sans fil ou d’un serveur multimédia surchargé, ce qui se traduit par une distorsion ou une perte de l’audio.</span><span class="sxs-lookup"><span data-stu-id="06680-p125">Real-Time Transport Protocol (RTP) packet loss for outbound packets. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-291"><strong>Image figée (%)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-291"><strong>Frozen frame %</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-292">Non</span><span class="sxs-lookup"><span data-stu-id="06680-292">No</span></span></p></td>
<td><p><span data-ttu-id="06680-p126">Pourcentage d’images « figées ». Dans une image figée, la vidéo cesse d’avancer tandis que la partie audio de l’appel continue.</span><span class="sxs-lookup"><span data-stu-id="06680-p126">Percentage of “frozen” frames. In a frozen frame, the video stops advancing while the audio portion of the call continues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-295"><strong>Fréquence d’images moyenne sortante</strong></span><span class="sxs-lookup"><span data-stu-id="06680-295"><strong>Outbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-296">Non</span><span class="sxs-lookup"><span data-stu-id="06680-296">No</span></span></p></td>
<td><p><span data-ttu-id="06680-297">Fréquence d’images moyenne pour les transmissions sortantes pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="06680-297">Average frame rate for outbound transmissions during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-298"><strong>Fréquence d’images moyenne entrante</strong></span><span class="sxs-lookup"><span data-stu-id="06680-298"><strong>Inbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-299">Non</span><span class="sxs-lookup"><span data-stu-id="06680-299">No</span></span></p></td>
<td><p><span data-ttu-id="06680-300">Fréquence d’images moyenne pour les transmissions entrantes pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="06680-300">Average frame rate for incoming transmissions during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-301"><strong>Fréquence d’images basse entrante (%)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-301"><strong>Inbound low frame rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-302">Non</span><span class="sxs-lookup"><span data-stu-id="06680-302">No</span></span></p></td>
<td><p><span data-ttu-id="06680-303">Pourcentage de l’appel où la vitesse de transmission pour la vidéo entrante était faible.</span><span class="sxs-lookup"><span data-stu-id="06680-303">Percentage of the call where the bit rate for incoming video was low.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-304"><strong>Intégrité des clients (%)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-304"><strong>Client health %</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="06680-305">Indique l’intégrité relative du périphérique client pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="06680-305">Indicates the relative health of the client device during the call.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="media-quality-summary-report-metrics-application-sharing-call-summary"></a><span data-ttu-id="06680-306">Mesures du rapport de synthèse de la qualité des médias : synthèse des appels de partage d’application</span><span class="sxs-lookup"><span data-stu-id="06680-306">Media Quality Summary Report Metrics: Application Sharing Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06680-307">Nom</span><span class="sxs-lookup"><span data-stu-id="06680-307">Name</span></span></th>
<th><span data-ttu-id="06680-308">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="06680-308">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="06680-309">Description</span><span class="sxs-lookup"><span data-stu-id="06680-309">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06680-310"><strong>Type d’appel/type de point de terminaison</strong></span><span class="sxs-lookup"><span data-stu-id="06680-310"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-311">Non</span><span class="sxs-lookup"><span data-stu-id="06680-311">No</span></span></p></td>
<td><p><span data-ttu-id="06680-p127">Lorsque vous cliquez sur cet élément, le rapport affiche des informations détaillées sur les appels en fonction de ce type. Les types d’appels sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="06680-p127">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="06680-314">Appels P2P UC</span><span class="sxs-lookup"><span data-stu-id="06680-314">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="06680-315">Sessions de conférence UC</span><span class="sxs-lookup"><span data-stu-id="06680-315">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="06680-316">Sessions de conférence RTC</span><span class="sxs-lookup"><span data-stu-id="06680-316">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="06680-317">Appels RTC : contournement du média</span><span class="sxs-lookup"><span data-stu-id="06680-317">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="06680-318">Appels RTC (sans contournement) : partie UC</span><span class="sxs-lookup"><span data-stu-id="06680-318">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="06680-319">Appels RTC (sans contournement) : partie passerelle</span><span class="sxs-lookup"><span data-stu-id="06680-319">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="06680-320">Autres types d’appels</span><span class="sxs-lookup"><span data-stu-id="06680-320">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-321"><strong>Volume d’appels</strong></span><span class="sxs-lookup"><span data-stu-id="06680-321"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-322">Non</span><span class="sxs-lookup"><span data-stu-id="06680-322">No</span></span></p></td>
<td><p><span data-ttu-id="06680-323">Nombre total d’appels par type d’appel.</span><span class="sxs-lookup"><span data-stu-id="06680-323">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-324"><strong>Pourcentage d’appels médiocres</strong></span><span class="sxs-lookup"><span data-stu-id="06680-324"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-325">Non</span><span class="sxs-lookup"><span data-stu-id="06680-325">No</span></span></p></td>
<td><p><span data-ttu-id="06680-p128">Nombre total d’appels jugés et classés comme étant médiocres. Un appel médiocre désigne un appel dont l’une des valeurs mesurées est supérieure à la valeur autorisée (par exemple, un appel soumis à un phénomène de gigue excessive).</span><span class="sxs-lookup"><span data-stu-id="06680-p128">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-328"><strong>Volume d’appels (appels sans fil)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-328"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-329">Non</span><span class="sxs-lookup"><span data-stu-id="06680-329">No</span></span></p></td>
<td><p><span data-ttu-id="06680-330">Nombre total d’appels qui utilisaient une connexion sans fil.</span><span class="sxs-lookup"><span data-stu-id="06680-330">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-331"><strong>Volume d’appels (appels VPN)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-331"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-332">Non</span><span class="sxs-lookup"><span data-stu-id="06680-332">No</span></span></p></td>
<td><p><span data-ttu-id="06680-333">Nombre total d’appels qui utilisaient une connexion VPN.</span><span class="sxs-lookup"><span data-stu-id="06680-333">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-334"><strong>Volume d’appels (appels externes)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-334"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-335">Non</span><span class="sxs-lookup"><span data-stu-id="06680-335">No</span></span></p></td>
<td><p><span data-ttu-id="06680-336">Nombre d’appels qui utilisaient une connexion externe (c’est-à-dire une connexion en dehors du réseau interne).</span><span class="sxs-lookup"><span data-stu-id="06680-336">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-337"><strong>Gigue (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-337"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-338">Non</span><span class="sxs-lookup"><span data-stu-id="06680-338">No</span></span></p></td>
<td><p><span data-ttu-id="06680-339">Gigue moyenne détectée entre les arrivées de paquets RTP.</span><span class="sxs-lookup"><span data-stu-id="06680-339">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="06680-340">(Gigue est une mesure du &quot; shakiness &quot; d’un appel.) Les valeurs de gigue élevée sont généralement provoquées par une congestion ou un serveur multimédia surchargé, ce qui a pour effet de déformer ou de perdre du son.</span><span class="sxs-lookup"><span data-stu-id="06680-340">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-341"><strong>Unilatéral relatif moyen</strong></span><span class="sxs-lookup"><span data-stu-id="06680-341"><strong>Avg. relative one way</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-342">Non</span><span class="sxs-lookup"><span data-stu-id="06680-342">No</span></span></p></td>
<td><p><span data-ttu-id="06680-p130">Retard unilatéral relatif moyen entre deux points de terminaison du média. Il s’agit d’une mesure de latence sur un seul tronçon.</span><span class="sxs-lookup"><span data-stu-id="06680-p130">Average relative one-way delay between two media endpoints. This is a single-hop latency measure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06680-345"><strong>Latence moyenne de traitement des mosaïques RDP</strong></span><span class="sxs-lookup"><span data-stu-id="06680-345"><strong>Avg. RDP tile processing latency</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-346">Non</span><span class="sxs-lookup"><span data-stu-id="06680-346">No</span></span></p></td>
<td><p><span data-ttu-id="06680-p131">Latence moyenne de traitement des mosaïques RDP sur le serveur de conférence AS par rapport à la durée de la session de visionnage. Une moyenne élevée équivaut à une expérience de visionnage plus longue et inclut une latence du réseau. Un serveur de conférence surchargé peut rencontrer des délais moyens plus élevés.</span><span class="sxs-lookup"><span data-stu-id="06680-p131">The average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session. A high average reflects a longer delay in the viewing experience, and includes network latency. An overloaded conferencing server may experience higher average delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06680-350"><strong>Nombre total de mosaïques altérées (%)</strong></span><span class="sxs-lookup"><span data-stu-id="06680-350"><strong>Total spoiled tile %</strong></span></span></p></td>
<td><p><span data-ttu-id="06680-351">Non</span><span class="sxs-lookup"><span data-stu-id="06680-351">No</span></span></p></td>
<td><p><span data-ttu-id="06680-352">Pourcentage total de mosaïques RDP altérées.</span><span class="sxs-lookup"><span data-stu-id="06680-352">Total percentage of spoiled RDP tiles.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="06680-353">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="06680-353">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

