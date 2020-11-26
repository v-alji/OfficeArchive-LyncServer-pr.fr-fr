---
title: 'Lync Server 2013 : sous-état synthèse de la Conférence'
description: 'Lync Server 2013 : sous-état synthèse de la Conférence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Summary Subreport
ms:assetid: 2fc1d2bf-34f5-4093-a6e2-250ec1f1b004
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204779(v=OCS.15)
ms:contentKeyID: 48183742
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0612ce1adb8a6b0fdea5e3bf70b88346f7c08044
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434486"
---
# <a name="conference-summary-subreport-in-lync-server-2013"></a><span data-ttu-id="11a7c-103">Sous-état synthèse de la Conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="11a7c-103">Conference Summary Subreport in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="11a7c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="11a7c-104">

<span> </span></span></span>

<span data-ttu-id="11a7c-105">_**Dernière modification de la rubrique :** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="11a7c-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="11a7c-p101">Le sous-rapport de synthèse de conférence fournit une vision générale des sessions de conférence ayant échoué. Ces échecs de session sont répartis par type de session : sessions Focus et les sessions MCU.</span><span class="sxs-lookup"><span data-stu-id="11a7c-p101">The Conference Summary Subreport provides an overall view of failed conference sessions. These failed sessions are further broken down by session type: Focus sessions and MCU sessions.</span></span>

<div>

## <a name="filters"></a><span data-ttu-id="11a7c-108">Filtres</span><span class="sxs-lookup"><span data-stu-id="11a7c-108">Filters</span></span>

<span data-ttu-id="11a7c-p102">Les filtres vous offrent la possibilité de retourner un ensemble de données mieux ciblées ou de visualiser les données retournées de différentes manières. Le tableau suivant dresse la liste des filtres que vous pouvez utiliser avec le sous-rapport de synthèse de conférence.</span><span class="sxs-lookup"><span data-stu-id="11a7c-p102">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Conference Summary Subreport.</span></span>

### <a name="conference-summary-subreport-filters"></a><span data-ttu-id="11a7c-111">Filtres du sous-rapport de synthèse de conférence</span><span class="sxs-lookup"><span data-stu-id="11a7c-111">Conference Summary Subreport Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11a7c-112">Nom</span><span class="sxs-lookup"><span data-stu-id="11a7c-112">Name</span></span></th>
<th><span data-ttu-id="11a7c-113">Description</span><span class="sxs-lookup"><span data-stu-id="11a7c-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11a7c-114"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="11a7c-114"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="11a7c-p103">Date/heure de début de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de début comme suit :</span><span class="sxs-lookup"><span data-stu-id="11a7c-p103">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="11a7c-117">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="11a7c-117">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="11a7c-p104">Si vous ne précisez aucune heure de début, le rapport commence automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="11a7c-p104">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="11a7c-120">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="11a7c-120">7/7/2012</span></span></p>
<p><span data-ttu-id="11a7c-121">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="11a7c-121">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="11a7c-122">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="11a7c-122">7/3/2012</span></span></p>
<p><span data-ttu-id="11a7c-123">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="11a7c-123">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11a7c-124"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="11a7c-124"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="11a7c-p105">Date/heure de fin de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de fin comme suit :</span><span class="sxs-lookup"><span data-stu-id="11a7c-p105">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="11a7c-127">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="11a7c-127">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="11a7c-p106">Si vous ne précisez aucune heure de fin, le rapport se termine automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="11a7c-p106">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="11a7c-130">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="11a7c-130">7/7/2012</span></span></p>
<p><span data-ttu-id="11a7c-131">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="11a7c-131">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="11a7c-132">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="11a7c-132">7/3/2012</span></span></p>
<p><span data-ttu-id="11a7c-133">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="11a7c-133">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11a7c-134"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="11a7c-134"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="11a7c-p107">Nom de domaine complet (FQDN) du pool de serveurs d’inscriptions. Vous pouvez soit sélectionner un pool particulier, soit cliquer sur <strong>[Tous]</strong> pour afficher les données de tous les pools. Cette liste déroulante se renseigne automatiquement en fonction des enregistrements que contient la base de données.</span><span class="sxs-lookup"><span data-stu-id="11a7c-p107">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="11a7c-138">Mesures</span><span class="sxs-lookup"><span data-stu-id="11a7c-138">Metrics</span></span>

<span data-ttu-id="11a7c-139">Le tableau suivant répertorie les informations fournies dans le sous-rapport de synthèse de conférence.</span><span class="sxs-lookup"><span data-stu-id="11a7c-139">The following table lists the information provided in the Conference Summary Subreport.</span></span>

### <a name="conference-summary-subreport-metrics"></a><span data-ttu-id="11a7c-140">Mesures du sous-rapport de synthèse de conférence</span><span class="sxs-lookup"><span data-stu-id="11a7c-140">Conference Summary Subreport Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11a7c-141">Nom</span><span class="sxs-lookup"><span data-stu-id="11a7c-141">Name</span></span></th>
<th><span data-ttu-id="11a7c-142">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="11a7c-142">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="11a7c-143">Description</span><span class="sxs-lookup"><span data-stu-id="11a7c-143">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11a7c-144"><strong>Nombre total de conférences</strong></span><span class="sxs-lookup"><span data-stu-id="11a7c-144"><strong>Total conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="11a7c-145">Non</span><span class="sxs-lookup"><span data-stu-id="11a7c-145">No</span></span></p></td>
<td><p><span data-ttu-id="11a7c-146">Nombre total de conférences ayant eu lieu.</span><span class="sxs-lookup"><span data-stu-id="11a7c-146">Total number of conferences held.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11a7c-147"><strong>Nombre total de sessions de conférence</strong></span><span class="sxs-lookup"><span data-stu-id="11a7c-147"><strong>Total conference sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="11a7c-148">Non</span><span class="sxs-lookup"><span data-stu-id="11a7c-148">No</span></span></p></td>
<td><p><span data-ttu-id="11a7c-p108">Nombre total de sessions de conférence. Une seule conférence peut avoir plusieurs sessions : par exemple, elle peut inclure à la fois une session Focus et une session MCU.</span><span class="sxs-lookup"><span data-stu-id="11a7c-p108">Total number of conference sessions. A single conference can have multiple sessions; for example, a conference might include both a Focus session and an MCU session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11a7c-151"><strong>Taux d’échec de session global</strong></span><span class="sxs-lookup"><span data-stu-id="11a7c-151"><strong>Overall session failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="11a7c-152">Non</span><span class="sxs-lookup"><span data-stu-id="11a7c-152">No</span></span></p></td>
<td><p><span data-ttu-id="11a7c-153">Pourcentage de tous les échecs de conférence.</span><span class="sxs-lookup"><span data-stu-id="11a7c-153">Percentage of all conferences that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11a7c-154"><strong>Sessions Focus</strong></span><span class="sxs-lookup"><span data-stu-id="11a7c-154"><strong>Focus sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="11a7c-155">Non</span><span class="sxs-lookup"><span data-stu-id="11a7c-155">No</span></span></p></td>
<td><p><span data-ttu-id="11a7c-156">Nombre total de sessions Focus.</span><span class="sxs-lookup"><span data-stu-id="11a7c-156">Total number of Focus sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11a7c-157"><strong>Taux d’échec de focus</strong></span><span class="sxs-lookup"><span data-stu-id="11a7c-157"><strong>Focus failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="11a7c-158">Non</span><span class="sxs-lookup"><span data-stu-id="11a7c-158">No</span></span></p></td>
<td><p><span data-ttu-id="11a7c-159">Pourcentage d’échec des sessions Focus.</span><span class="sxs-lookup"><span data-stu-id="11a7c-159">Percentage of Focus sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11a7c-160">Sessions MCU</span><span class="sxs-lookup"><span data-stu-id="11a7c-160">MCU sessions</span></span></p></td>
<td><p><span data-ttu-id="11a7c-161">Non</span><span class="sxs-lookup"><span data-stu-id="11a7c-161">No</span></span></p></td>
<td><p><span data-ttu-id="11a7c-162">Nombre total de sessions MCU.</span><span class="sxs-lookup"><span data-stu-id="11a7c-162">Total number of MCU sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11a7c-163"><strong>Taux d’échec MCU</strong></span><span class="sxs-lookup"><span data-stu-id="11a7c-163"><strong>MCU failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="11a7c-164">Non</span><span class="sxs-lookup"><span data-stu-id="11a7c-164">No</span></span></p></td>
<td><p><span data-ttu-id="11a7c-165">Pourcentage d’échec des sessions MCU.</span><span class="sxs-lookup"><span data-stu-id="11a7c-165">Percentage of MCU sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11a7c-166"><strong>Sessions MCU par modalité</strong></span><span class="sxs-lookup"><span data-stu-id="11a7c-166"><strong>MCU sessions by modality</strong></span></span></p></td>
<td><p><span data-ttu-id="11a7c-167">Non</span><span class="sxs-lookup"><span data-stu-id="11a7c-167">No</span></span></p></td>
<td><p><span data-ttu-id="11a7c-168">Nombre total de sessions MCU, groupées par modalité (par exemple, les conférences de messagerie instantanée).</span><span class="sxs-lookup"><span data-stu-id="11a7c-168">Total number of MCU sessions, grouped by modality (for example, IM conferencing).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11a7c-169"><strong>Taux d’échec par modalité</strong></span><span class="sxs-lookup"><span data-stu-id="11a7c-169"><strong>Failure rate by modality</strong></span></span></p></td>
<td><p><span data-ttu-id="11a7c-170">Non</span><span class="sxs-lookup"><span data-stu-id="11a7c-170">No</span></span></p></td>
<td><p><span data-ttu-id="11a7c-171">Pourcentage d’échec des sessions MCU, groupées par modalité (par exemple, les conférences de messagerie instantanée).</span><span class="sxs-lookup"><span data-stu-id="11a7c-171">Percentage of MCU sessions that failed, grouped by modality (for example, IM conferencing).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="11a7c-172">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="11a7c-172">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

