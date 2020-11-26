---
title: 'Lync Server 2013 : rapport de contrôle d’admission des appels'
description: 'Lync Server 2013 : rapport de contrôle d’admission des appels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Admission Control Report
ms:assetid: ea4b0c9f-7f93-4b8a-b901-01e1636c44fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615043(v=OCS.15)
ms:contentKeyID: 48185933
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8764e51603e7097095894bc1230c2a2bb1126b9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435781"
---
# <a name="call-admission-control-report-in-lync-server-2013"></a><span data-ttu-id="9fb16-103">Rapport de contrôle d’admission des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9fb16-103">Call Admission Control Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9fb16-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9fb16-104">

<span> </span></span></span>

<span data-ttu-id="9fb16-105">_**Dernière modification de la rubrique :** 2012-06-29_</span><span class="sxs-lookup"><span data-stu-id="9fb16-105">_**Topic Last Modified:** 2012-06-29_</span></span>

<span data-ttu-id="9fb16-106">Le rapport du contrôle d’admission des appels fournit des informations sur les sessions P2P et de conférence menées avec des restrictions mises en place par le contrôle d’admission des appels.</span><span class="sxs-lookup"><span data-stu-id="9fb16-106">The Call Admission Control Report provides information about peer-to-peer and conferencing sessions that were conducted under restrictions set in place by Call Admission Control.</span></span> <span data-ttu-id="9fb16-107">Le contrôle d’admission des appels, présenté dans Microsoft Lync Server 2010, permet aux administrateurs d’autoriser (ou non) les sessions de communication en fonction de contraintes de bande passante.</span><span class="sxs-lookup"><span data-stu-id="9fb16-107">Call Admission Control, introduced in Microsoft Lync Server 2010, provides a way for administrators to allow (or not allow) communication sessions based on bandwidth constraints.</span></span> <span data-ttu-id="9fb16-108">Par exemple, les administrateurs peuvent créer des stratégies qui imposent une quantité limite de bande passante disponible pour les appels vocaux et vidéo.</span><span class="sxs-lookup"><span data-stu-id="9fb16-108">For example, administrators can create policies that impose a limit on the amount of bandwidth available for voice and video calls.</span></span> <span data-ttu-id="9fb16-109">Si cette limite est atteinte, aucun nouvel appel vocal ou vidéo ne peut être effectué tant que l’un des appels en cours n’est pas terminé et que les ressources réseau requises ne sont pas libérées.</span><span class="sxs-lookup"><span data-stu-id="9fb16-109">If that bandwidth limit has been reached, then no new voice or video calls can be placed until one of the current calls has ended and freed up the required network resources.</span></span>

<div>

## <a name="accessing-the-call-admission-control-report"></a><span data-ttu-id="9fb16-110">Accès au rapport du contrôle d’admission des appels</span><span class="sxs-lookup"><span data-stu-id="9fb16-110">Accessing the Call Admission Control Report</span></span>

<span data-ttu-id="9fb16-p102">Le rapport du contrôle d’admission des appels est accessible à partir de la page d’accueil des Rapports de suivi. De ce rapport, vous pouvez atteindre l’un des rapports suivants :</span><span class="sxs-lookup"><span data-stu-id="9fb16-p102">The Call Admission Control Report is accessed from the Monitoring Reports home page. From the Call Admission Control Report you can drill down to either of the following reports:</span></span>

  - <span data-ttu-id="9fb16-113">Rapport détaillé de conférence – Pour accéder à ce rapport, cliquez sur la mesure Détails à partir d’une session de conférence.</span><span class="sxs-lookup"><span data-stu-id="9fb16-113">Conference Detail Report – To access this report, click the Details metric from a conference session.</span></span>

  - <span data-ttu-id="9fb16-114">Rapport détaillé de session P2P – Pour accéder à ce rapport, cliquez sur la mesure Détails d’une session P2P.</span><span class="sxs-lookup"><span data-stu-id="9fb16-114">Peer-to-Peer Session Detail Report – To access this report, click the Details metric for a peer-to-peer session.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-admission-control-report"></a><span data-ttu-id="9fb16-115">Utilisation optimale du rapport du contrôle d’admission des appels</span><span class="sxs-lookup"><span data-stu-id="9fb16-115">Making the Best Use of the Call Admission Control Report</span></span>

<span data-ttu-id="9fb16-p103">Pour obtenir une liste des appels ayant échoué en raison d’une bande passante insuffisante, sélectionnez Appels rejetés en raison du contrôle d’admission des appels dans la liste déroulante Catégorie d’appel. La plupart des appels renvoyés auront probablement un ID de diagnostic de 5 :</span><span class="sxs-lookup"><span data-stu-id="9fb16-p103">To get a list of calls that failed because of insufficient bandwidth, select Calls rejected because of call admission control from the Call category dropdown list. Most of the returned calls will likely have a diagnostic ID of 5:</span></span>

<span data-ttu-id="9fb16-p104">Bande passante insuffisante pour établir une session. Essayez le réacheminement RTC.</span><span class="sxs-lookup"><span data-stu-id="9fb16-p104">Insufficient bandwidth to establish session. Attempt PSTN re-route.</span></span>

<span data-ttu-id="9fb16-120">Cela indique que les limitations du contrôle d’admission des appels empêchaient l’appel d’être effectué sur le réseau VoIP.</span><span class="sxs-lookup"><span data-stu-id="9fb16-120">That indicates that Call Admission Control limitations were preventing the call from being made on the VoIP network.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="9fb16-121">Filtres</span><span class="sxs-lookup"><span data-stu-id="9fb16-121">Filters</span></span>

<span data-ttu-id="9fb16-p105">Les filtres vous offrent la possibilité de renvoyer un ensemble de données mieux ciblées ou de visualiser les données renvoyées de différentes manières. Par exemple, le rapport de contrôle d’admission des appels vous permet de filtrer des appels en fonction de l’utilisateur qui les a émis ou qui a été appelé. Vous pouvez également choisir le mode de groupement des données. Dans ce cas, les appels sont groupés par heure, jour, semaine ou mois.</span><span class="sxs-lookup"><span data-stu-id="9fb16-p105">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Call Admission Control Report enables you to filter calls by the user who initiated the call or by the user who was being called. You can also choose how data should be grouped. In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="9fb16-126">Le tableau qui suit dresse la liste des filtres que vous pouvez utiliser avec le rapport de contrôle d’admission des appels.</span><span class="sxs-lookup"><span data-stu-id="9fb16-126">The following table lists the filters that you can use with the Call Admission Control Report.</span></span>

### <a name="call-admission-control-report-filters"></a><span data-ttu-id="9fb16-127">Filtres du rapport de contrôle d’admission des appels</span><span class="sxs-lookup"><span data-stu-id="9fb16-127">Call Admission Control Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9fb16-128">Nom</span><span class="sxs-lookup"><span data-stu-id="9fb16-128">Name</span></span></th>
<th><span data-ttu-id="9fb16-129">Description</span><span class="sxs-lookup"><span data-stu-id="9fb16-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9fb16-130"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-130"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-p106">Date/heure de début de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de début comme suit :</span><span class="sxs-lookup"><span data-stu-id="9fb16-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="9fb16-133">7/17/12012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="9fb16-133">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="9fb16-p107">Si vous ne précisez aucune heure de début, le rapport commence automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="9fb16-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="9fb16-136">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="9fb16-136">7/17/12012</span></span></p>
<p><span data-ttu-id="9fb16-137">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="9fb16-137">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="9fb16-138">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="9fb16-138">7/13/2012</span></span></p>
<p><span data-ttu-id="9fb16-139">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="9fb16-139">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fb16-140"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-140"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-p108">Date/heure de fin de la période. Pour afficher les données par heures, entrez à la fois la date et l’heure de fin comme suit :</span><span class="sxs-lookup"><span data-stu-id="9fb16-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="9fb16-143">7/17/12012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="9fb16-143">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="9fb16-p109">Si vous ne précisez aucune heure de fin, le rapport se termine automatiquement à midi (12:00 AM) à la date du jour défini. Pour afficher les données par jour, entrez simplement la date :</span><span class="sxs-lookup"><span data-stu-id="9fb16-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="9fb16-146">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="9fb16-146">7/17/12012</span></span></p>
<p><span data-ttu-id="9fb16-147">Pour afficher les données par semaine ou mois, entrez une date tombant un jour quelconque de la semaine ou du mois que vous souhaitez visualiser (nul besoin d’entrer le premier jour de la semaine ou du mois) :</span><span class="sxs-lookup"><span data-stu-id="9fb16-147">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="9fb16-148">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="9fb16-148">7/13/2012</span></span></p>
<p><span data-ttu-id="9fb16-149">Les semaines s’étalent toujours du dimanche au samedi.</span><span class="sxs-lookup"><span data-stu-id="9fb16-149">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fb16-150"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-150"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-p110">Nom de domaine complet (FQDN) du pool de serveurs d’inscriptions. Vous pouvez soit sélectionner un pool particulier, soit cliquer sur <strong>[Tous]</strong> pour afficher les données de tous les pools. Cette liste déroulante se renseigne automatiquement en fonction des enregistrements que contient la base de données.</span><span class="sxs-lookup"><span data-stu-id="9fb16-p110">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fb16-154"><strong>Type d’activité</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-154"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-p111">Type d’activité. Sélectionnez l’une des activités suivantes :</span><span class="sxs-lookup"><span data-stu-id="9fb16-p111">Type of activity. Select one of the following activities:</span></span></p>
<ul>
<li><p><span data-ttu-id="9fb16-157">[Tous]</span><span class="sxs-lookup"><span data-stu-id="9fb16-157">[All]</span></span></p></li>
<li><p><span data-ttu-id="9fb16-158">P2P</span><span class="sxs-lookup"><span data-stu-id="9fb16-158">Peer-to-Peer</span></span></p></li>
<li><p><span data-ttu-id="9fb16-159">Conférence</span><span class="sxs-lookup"><span data-stu-id="9fb16-159">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fb16-160"><strong>Catégorie d’appel</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-160"><strong>Call category</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-p112">Indique la raison pour laquelle le contrôle d’admission des appels a été utilisé pour l’appel. Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="9fb16-p112">Indicates the reason that CAC was used for the call. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="9fb16-163">[Tous]</span><span class="sxs-lookup"><span data-stu-id="9fb16-163">[All]</span></span></p></li>
<li><p><span data-ttu-id="9fb16-164">Appels rejetés en raison du contrôle d’admission des appels</span><span class="sxs-lookup"><span data-stu-id="9fb16-164">Call rejected because of call admission control</span></span></p></li>
<li><p><span data-ttu-id="9fb16-165">Appels réacheminés via RTC en raison du contrôle d’admission des appels</span><span class="sxs-lookup"><span data-stu-id="9fb16-165">Calls rerouted through PSTN because of call admission control</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="9fb16-166">Mesures pour les sessions P2P</span><span class="sxs-lookup"><span data-stu-id="9fb16-166">Metrics for Peer-to-Peer Sessions</span></span>

<span data-ttu-id="9fb16-167">Le tableau ci-dessous répertorie les informations fournies par le rapport de contrôle d’admission des appels pour les sessions P2P (c’est-à-dire, les sessions qui n’impliquent que deux participants).</span><span class="sxs-lookup"><span data-stu-id="9fb16-167">The following table lists the information provided in the Call Admission Control Report for peer-to-peer sessions (that is, sessions involving just two participants).</span></span>

### <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="9fb16-168">Mesures pour les sessions P2P</span><span class="sxs-lookup"><span data-stu-id="9fb16-168">Metrics for Peer-to-Peer Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9fb16-169">Nom</span><span class="sxs-lookup"><span data-stu-id="9fb16-169">Name</span></span></th>
<th><span data-ttu-id="9fb16-170">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="9fb16-170">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="9fb16-171">Description</span><span class="sxs-lookup"><span data-stu-id="9fb16-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9fb16-172"><strong>Détails</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-172"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-173">Non</span><span class="sxs-lookup"><span data-stu-id="9fb16-173">No</span></span></p></td>
<td><p><span data-ttu-id="9fb16-174">Lorsque vous cliquez sur cet élément, le rapport présente un rapport détaillé de session P2P pour la session spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9fb16-174">When you click this item, the report shows you a Peer-to-Peer Session Detail Report for the specified session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fb16-175"><strong>De l’utilisateur</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-175"><strong>From user</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-176">Oui</span><span class="sxs-lookup"><span data-stu-id="9fb16-176">Yes</span></span></p></td>
<td><p><span data-ttu-id="9fb16-177">Adresse SIP de l’utilisateur ayant initié la session.</span><span class="sxs-lookup"><span data-stu-id="9fb16-177">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fb16-178"><strong>À l’utilisateur</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-178"><strong>To user</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-179">Oui</span><span class="sxs-lookup"><span data-stu-id="9fb16-179">Yes</span></span></p></td>
<td><p><span data-ttu-id="9fb16-180">Adresse SIP de l’utilisateur qui a été invité à participer à la session.</span><span class="sxs-lookup"><span data-stu-id="9fb16-180">SIP address of the user who was invited to join the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fb16-181"><strong>Modalités</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-181"><strong>Modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-182">Oui</span><span class="sxs-lookup"><span data-stu-id="9fb16-182">Yes</span></span></p></td>
<td><p><span data-ttu-id="9fb16-183">Modalités de communication (audio et vidéo) qui ont été utilisées pendant la session.</span><span class="sxs-lookup"><span data-stu-id="9fb16-183">Communication modalities (such as audio and video) that were used during the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fb16-184"><strong>Heure d’invitation</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-184"><strong>Invite time</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-185">Oui</span><span class="sxs-lookup"><span data-stu-id="9fb16-185">Yes</span></span></p></td>
<td><p><span data-ttu-id="9fb16-186">Date et heure auxquelles l’invitation initiale à la session a été envoyée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9fb16-186">Date and time the initial session invitation was sent to the From user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fb16-187"><strong>Heure de réponse</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-187"><strong>Response time</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-188">Oui</span><span class="sxs-lookup"><span data-stu-id="9fb16-188">Yes</span></span></p></td>
<td><p><span data-ttu-id="9fb16-189">Date et heure auxquelles l’acceptation de l’invitation a été reçue.</span><span class="sxs-lookup"><span data-stu-id="9fb16-189">Date and time that the invitation acceptance was received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fb16-190"><strong>Heure de fin</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-190"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-191">Oui</span><span class="sxs-lookup"><span data-stu-id="9fb16-191">Yes</span></span></p></td>
<td><p><span data-ttu-id="9fb16-192">Date et heure auxquelles la session s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="9fb16-192">Date and time that the session ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fb16-193"><strong>ID de diagnostic</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-193"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-194">Oui</span><span class="sxs-lookup"><span data-stu-id="9fb16-194">Yes</span></span></p></td>
<td><p><span data-ttu-id="9fb16-p113">Identificateur unique (sous la forme d’un en-tête ms-diagnostics) attaché à un message SIP qui fournit souvent des informations utiles pour résoudre des erreurs. Les en-têtes de diagnostic sont facultatifs (il est possible que des sessions SIP n’incluent pas ces en-têtes) et les ID de diagnostic sont uniquement signalés pour les sessions qui ont rencontré des problèmes, quels qu’ils soient.</span><span class="sxs-lookup"><span data-stu-id="9fb16-p113">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="9fb16-197">Mesures pour les sessions de conférence</span><span class="sxs-lookup"><span data-stu-id="9fb16-197">Metrics for Conferencing Sessions</span></span>

<span data-ttu-id="9fb16-198">Le tableau ci-dessous répertorie les informations fournies par le rapport de contrôle d’admission des appels pour les sessions de conférence (c’est-à-dire, les sessions qui impliquent trois participants ou plus).</span><span class="sxs-lookup"><span data-stu-id="9fb16-198">The following table lists the information provided in the Call Admission Control Report for conferencing sessions (that is, sessions involving three or more participants).</span></span>

### <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="9fb16-199">Mesures pour les sessions de conférence</span><span class="sxs-lookup"><span data-stu-id="9fb16-199">Metrics for Conferencing Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9fb16-200">Nom</span><span class="sxs-lookup"><span data-stu-id="9fb16-200">Name</span></span></th>
<th><span data-ttu-id="9fb16-201">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="9fb16-201">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="9fb16-202">Description</span><span class="sxs-lookup"><span data-stu-id="9fb16-202">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9fb16-203"><strong>URI de la conférence</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-203"><strong>Conference URI</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-204">Oui</span><span class="sxs-lookup"><span data-stu-id="9fb16-204">Yes</span></span></p></td>
<td><p><span data-ttu-id="9fb16-p114">Identificateur unique de la conférence. Lorsque vous cliquez sur cet élément, le rapport présente les participants individuels de la conférence.</span><span class="sxs-lookup"><span data-stu-id="9fb16-p114">Unique identifier for the conference. When you click this item, the report shows the individual conference participants.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fb16-207"><strong>Organisateur</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-207"><strong>Organizer</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-208">Oui</span><span class="sxs-lookup"><span data-stu-id="9fb16-208">Yes</span></span></p></td>
<td><p><span data-ttu-id="9fb16-209">Adresse SIP de l’utilisateur qui a organisé la conférence.</span><span class="sxs-lookup"><span data-stu-id="9fb16-209">SIP address of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fb16-210"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-210"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-211">Oui</span><span class="sxs-lookup"><span data-stu-id="9fb16-211">Yes</span></span></p></td>
<td><p><span data-ttu-id="9fb16-212">Serveur Edge utilisé pour la conférence.</span><span class="sxs-lookup"><span data-stu-id="9fb16-212">Edge Server used in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fb16-213"><strong>Heure de début</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-213"><strong>Start time</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-214">Oui</span><span class="sxs-lookup"><span data-stu-id="9fb16-214">Yes</span></span></p></td>
<td><p><span data-ttu-id="9fb16-215">Date et heure auxquelles la conférence a commencé.</span><span class="sxs-lookup"><span data-stu-id="9fb16-215">Date and time that the conference started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fb16-216"><strong>Heure de fin</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-216"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-217">Oui</span><span class="sxs-lookup"><span data-stu-id="9fb16-217">Yes</span></span></p></td>
<td><p><span data-ttu-id="9fb16-218">Date et heure de fin de la conférence.</span><span class="sxs-lookup"><span data-stu-id="9fb16-218">Date and time that the conference ended.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-individual-conference-participants"></a><span data-ttu-id="9fb16-219">Mesures pour les participants individuels de la conférence</span><span class="sxs-lookup"><span data-stu-id="9fb16-219">Metrics for Individual Conference Participants</span></span>

<span data-ttu-id="9fb16-220">Le tableau qui suit répertorie les informations fournies dans le rapport de contrôle d’admission des appels pour chaque participant d’une conférence.</span><span class="sxs-lookup"><span data-stu-id="9fb16-220">The following table lists the information provided in the Call Admission Control Report for individual conference participants.</span></span>

### <a name="metrics-for-individual-conference-participants"></a><span data-ttu-id="9fb16-221">Mesures pour les participants individuels de la conférence</span><span class="sxs-lookup"><span data-stu-id="9fb16-221">Metrics for Individual Conference Participants</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9fb16-222">Nom</span><span class="sxs-lookup"><span data-stu-id="9fb16-222">Name</span></span></th>
<th><span data-ttu-id="9fb16-223">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="9fb16-223">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="9fb16-224">Description</span><span class="sxs-lookup"><span data-stu-id="9fb16-224">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9fb16-225"><strong>Rôle</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-225"><strong>Role</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-226">Non</span><span class="sxs-lookup"><span data-stu-id="9fb16-226">No</span></span></p></td>
<td><p><span data-ttu-id="9fb16-227">Rôle (par exemple, présentateur) joué par le participant à la conférence.</span><span class="sxs-lookup"><span data-stu-id="9fb16-227">Role (for example, Presenter) played by the conference participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fb16-228"><strong>Participant</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-228"><strong>Participant</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-229">Non</span><span class="sxs-lookup"><span data-stu-id="9fb16-229">No</span></span></p></td>
<td><p><span data-ttu-id="9fb16-230">Adresse SIP du participant à la conférence.</span><span class="sxs-lookup"><span data-stu-id="9fb16-230">SIP address of the conference participant.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fb16-231"><strong>Connectivité</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-231"><strong>Connectivity</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-232">Non</span><span class="sxs-lookup"><span data-stu-id="9fb16-232">No</span></span></p></td>
<td><p><span data-ttu-id="9fb16-233">Connectivité réseau (généralement Depuis interne ou Depuis externe) du participant.</span><span class="sxs-lookup"><span data-stu-id="9fb16-233">Network connectivity (typically From Internal or From External) for the participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fb16-234"><strong>Modalité</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-234"><strong>Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-235">Non</span><span class="sxs-lookup"><span data-stu-id="9fb16-235">No</span></span></p></td>
<td><p><span data-ttu-id="9fb16-236">Type de conférence (par exemple, conférence A/V).</span><span class="sxs-lookup"><span data-stu-id="9fb16-236">Conference type (for example, A/V conferencing).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fb16-237"><strong>Heure d’arrivée</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-237"><strong>Join time</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-238">Non</span><span class="sxs-lookup"><span data-stu-id="9fb16-238">No</span></span></p></td>
<td><p><span data-ttu-id="9fb16-239">Date et heure auxquelles le participant a rejoint la conférence.</span><span class="sxs-lookup"><span data-stu-id="9fb16-239">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fb16-240"><strong>Heure de départ</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-240"><strong>Leave time</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-241">Non</span><span class="sxs-lookup"><span data-stu-id="9fb16-241">No</span></span></p></td>
<td><p><span data-ttu-id="9fb16-242">Date et heure auxquelles le participant a quitté la conférence.</span><span class="sxs-lookup"><span data-stu-id="9fb16-242">Date and time that the participant left the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fb16-243"><strong>ID de diagnostic</strong></span><span class="sxs-lookup"><span data-stu-id="9fb16-243"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="9fb16-244">Non</span><span class="sxs-lookup"><span data-stu-id="9fb16-244">No</span></span></p></td>
<td><p><span data-ttu-id="9fb16-p115">Identificateur unique (sous la forme d’un en-tête ms-diagnostics) attaché à un message SIP qui fournit souvent des informations utiles pour résoudre des erreurs. Les en-têtes de diagnostic sont facultatifs (il est possible que des sessions SIP n’incluent pas ces en-têtes) et les ID de diagnostic sont uniquement signalés pour les sessions qui ont rencontré des problèmes, quels qu’ils soient.</span><span class="sxs-lookup"><span data-stu-id="9fb16-p115">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9fb16-247">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9fb16-247">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

