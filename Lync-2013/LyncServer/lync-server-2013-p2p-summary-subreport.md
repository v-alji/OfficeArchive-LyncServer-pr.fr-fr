---
title: 'Lync Server 2013 : sous-état synthèse P2P'
description: 'Serveur Lync Server 2013 : sous-état récapitulative P2P.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: P2P Summary Subreport
ms:assetid: fc36185a-3cc5-4167-8c93-8a755fa75ac7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205416(v=OCS.15)
ms:contentKeyID: 48185950
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eda51e76c4ed7b62535a2a2e4ab52982aa6381f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424701"
---
# <a name="p2p-summary-subreport-in-lync-server-2013"></a><span data-ttu-id="0331b-103">Sous-état synthèse P2P de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0331b-103">P2P Summary Subreport in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0331b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0331b-104">

<span> </span></span></span>

<span data-ttu-id="0331b-105">_**Dernière modification de la rubrique :** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="0331b-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="0331b-106">Le sous-rapport de résumé P2P offre un aperçu général de vos sessions de communication pair au pair ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="0331b-106">The P2P Summary Subreport provides an overall view of your failed peer-to-peer communication sessions.</span></span>

<div>

## <a name="filters"></a><span data-ttu-id="0331b-107">Filtres</span><span class="sxs-lookup"><span data-stu-id="0331b-107">Filters</span></span>

<span data-ttu-id="0331b-p101">Les filtres vous offrent la possibilité de retourner un ensemble de données mieux ciblées ou de visualiser les données retournées de différentes manières. Le tableau suivant dresse la liste des filtres que vous pouvez utiliser avec le sous-rapport de résumé P2P.</span><span class="sxs-lookup"><span data-stu-id="0331b-p101">Filters provide a way for you to return a more finely targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the P2P Summary Subreport.</span></span>

### <a name="p2p-summary-subreport-filters"></a><span data-ttu-id="0331b-110">Filtres de sous-rapport de résumé P2P</span><span class="sxs-lookup"><span data-stu-id="0331b-110">P2P Summary Subreport Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0331b-111">Nom</span><span class="sxs-lookup"><span data-stu-id="0331b-111">Name</span></span></th>
<th><span data-ttu-id="0331b-112">Description</span><span class="sxs-lookup"><span data-stu-id="0331b-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0331b-113"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="0331b-113"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="0331b-p102">Date/heure de début de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de début comme suit :</span><span class="sxs-lookup"><span data-stu-id="0331b-p102">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="0331b-116">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="0331b-116">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="0331b-p103">Si vous ne précisez aucune heure de début, le rapport commence automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="0331b-p103">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="0331b-119">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="0331b-119">7/7/2012</span></span></p>
<p><span data-ttu-id="0331b-120">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="0331b-120">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="0331b-121">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="0331b-121">7/3/2012</span></span></p>
<p><span data-ttu-id="0331b-122">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="0331b-122">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0331b-123"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="0331b-123"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="0331b-p104">Date/heure de fin de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de fin comme suit :</span><span class="sxs-lookup"><span data-stu-id="0331b-p104">End date and time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="0331b-126">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="0331b-126">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="0331b-p105">Si vous ne précisez aucune heure de fin, le rapport se termine automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="0331b-p105">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="0331b-129">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="0331b-129">7/7/2012</span></span></p>
<p><span data-ttu-id="0331b-130">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="0331b-130">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="0331b-131">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="0331b-131">7/3/2012</span></span></p>
<p><span data-ttu-id="0331b-132">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="0331b-132">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0331b-133"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="0331b-133"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="0331b-p106">Nom de domaine complet (FQDN) du pool de serveurs d’inscriptions. Vous pouvez soit sélectionner un pool particulier, soit cliquer sur <strong>[Tous]</strong> pour afficher les données de tous les pools. Cette liste déroulante se renseigne automatiquement en fonction des enregistrements que contient la base de données.</span><span class="sxs-lookup"><span data-stu-id="0331b-p106">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="0331b-137">Mesures</span><span class="sxs-lookup"><span data-stu-id="0331b-137">Metrics</span></span>

<span data-ttu-id="0331b-138">Le tableau qui suit répertorie les informations fournies dans le sous-rapport de résumé P2P.</span><span class="sxs-lookup"><span data-stu-id="0331b-138">The following table lists the information provided in the P2P Summary Subreport.</span></span>

### <a name="p2p-summary-subreport-metrics"></a><span data-ttu-id="0331b-139">Mesures de sous-rapport de résumé P2P</span><span class="sxs-lookup"><span data-stu-id="0331b-139">P2P Summary Subreport Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0331b-140">Nom</span><span class="sxs-lookup"><span data-stu-id="0331b-140">Name</span></span></th>
<th><span data-ttu-id="0331b-141">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="0331b-141">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="0331b-142">Description</span><span class="sxs-lookup"><span data-stu-id="0331b-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0331b-143"><strong>Nombre total de sessions</strong></span><span class="sxs-lookup"><span data-stu-id="0331b-143"><strong>Total sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="0331b-144">Non</span><span class="sxs-lookup"><span data-stu-id="0331b-144">No</span></span></p></td>
<td><p><span data-ttu-id="0331b-145">Nombre total de sessions qui comprend les sessions réussies, les sessions qui ont échoué (à la fois les échecs attendus et les échecs inattendus) et les sessions non catégorisées.</span><span class="sxs-lookup"><span data-stu-id="0331b-145">Total number of sessions, including successful sessions, failed sessions (both expected failures and unexpected failures), and uncategorized sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0331b-146"><strong>Taux d’échec</strong></span><span class="sxs-lookup"><span data-stu-id="0331b-146"><strong>Failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="0331b-147">Non</span><span class="sxs-lookup"><span data-stu-id="0331b-147">No</span></span></p></td>
<td><p><span data-ttu-id="0331b-148">Pourcentage de sessions P2P ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="0331b-148">Percentage of peer-to-peer sessions that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0331b-149"><strong>Sessions par modalité</strong></span><span class="sxs-lookup"><span data-stu-id="0331b-149"><strong>Sessions by Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="0331b-150">Non</span><span class="sxs-lookup"><span data-stu-id="0331b-150">No</span></span></p></td>
<td><p><span data-ttu-id="0331b-151">Nombre total de sessions groupées par modalité (par exemple, messagerie instantanée).</span><span class="sxs-lookup"><span data-stu-id="0331b-151">Total number of sessions grouped by modality (for example, instant messaging).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0331b-152"><strong>Taux d’échec par modalité</strong></span><span class="sxs-lookup"><span data-stu-id="0331b-152"><strong>Failure rate by modality</strong></span></span></p></td>
<td><p><span data-ttu-id="0331b-153">Non</span><span class="sxs-lookup"><span data-stu-id="0331b-153">No</span></span></p></td>
<td><p><span data-ttu-id="0331b-154">Nombre total de sessions ayant échoué groupées par modalité (par exemple, messagerie instantanée).</span><span class="sxs-lookup"><span data-stu-id="0331b-154">Total number of failed sessions grouped by modality (for example, instant messaging).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0331b-155">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0331b-155">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

