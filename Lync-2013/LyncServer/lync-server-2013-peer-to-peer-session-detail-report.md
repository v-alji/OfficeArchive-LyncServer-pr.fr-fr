---
title: 'Lync Server 2013 : rapport détaillé sur la session d’égal à égal'
description: 'Lync Server 2013 : rapport détaillé sur la session d’égal à égal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Peer-to-Peer Session Detail Report
ms:assetid: 6be1d676-68f7-4a53-a72a-de73296c5571
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558659(v=OCS.15)
ms:contentKeyID: 48184416
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e712225fddabb646cc3b862f59601857a7df8eff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445035"
---
# <a name="peer-to-peer-session-detail-report-in-lync-server-2013"></a><span data-ttu-id="7ec08-103">Rapport détaillé sur la session d’égal à égal dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7ec08-103">Peer-to-Peer Session Detail Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7ec08-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7ec08-104">

<span> </span></span></span>

<span data-ttu-id="7ec08-105">_**Dernière modification de la rubrique :** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="7ec08-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="7ec08-p101">Le rapport détaillé de session P2P renvoie des informations détaillées sur une session P2P. Par exemple, si vous sélectionnez une session de messagerie instantanée, le rapport indique le nombre de messages envoyés par chacun des deux utilisateurs dans la session.</span><span class="sxs-lookup"><span data-stu-id="7ec08-p101">The Peer-to-Peer Session Detail Report returns detailed information about a peer-to-peer session. For example, if you select an instant messaging session, the report will tell you the number of messages sent by each of the two users in the session.</span></span>

<div>

## <a name="accessing-the-peer-to-peer-session-detail-report"></a><span data-ttu-id="7ec08-108">Accès au rapport détaillé de session P2P</span><span class="sxs-lookup"><span data-stu-id="7ec08-108">Accessing the Peer-to-Peer Session Detail Report</span></span>

<span data-ttu-id="7ec08-109">Vous pouvez accéder au rapport de détails de session P2P à partir de l’un des rapports suivants (disponibles en totalité dans la page d’accueil Rapports de surveillance) :</span><span class="sxs-lookup"><span data-stu-id="7ec08-109">The Peer-to-Peer Session Detail Report can be accessed from any of the following reports (all of which can be accessed from the Monitoring Reports home page):</span></span>

  - <span data-ttu-id="7ec08-110">Rapport d’inventaire de téléphonie IP</span><span class="sxs-lookup"><span data-stu-id="7ec08-110">IP Phone Inventory Report</span></span>

  - <span data-ttu-id="7ec08-111">Rapport d’activité de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="7ec08-111">User Activity Report</span></span>

  - <span data-ttu-id="7ec08-112">Rapport de contrôle d’admission des appels</span><span class="sxs-lookup"><span data-stu-id="7ec08-112">Call Admission Control Report</span></span>

  - <span data-ttu-id="7ec08-113">Rapport de liste des échecs</span><span class="sxs-lookup"><span data-stu-id="7ec08-113">Failure List Report</span></span>

<span data-ttu-id="7ec08-114">Dans le rapport détaillé de la session d’égal à égal, vous pouvez accéder au [rapport de diagnostic dans Lync Server 2013](lync-server-2013-diagnostic-report.md) en cliquant sur le rapport de diagnostic (détails) métrique.</span><span class="sxs-lookup"><span data-stu-id="7ec08-114">From within the Peer-to-Peer Session Detail Report you can access the [Diagnostic Report in Lync Server 2013](lync-server-2013-diagnostic-report.md) by clicking the Diagnostic Report (Details) metric.</span></span> <span data-ttu-id="7ec08-115">Vous pouvez aussi accéder au rapport des principales défaillances en cliquant sur l’une de ces deux mesures :</span><span class="sxs-lookup"><span data-stu-id="7ec08-115">You can also access the Top Failures Report by clicking either of these two metrics:</span></span>

  - <span data-ttu-id="7ec08-116">Réponse</span><span class="sxs-lookup"><span data-stu-id="7ec08-116">Response</span></span>

  - <span data-ttu-id="7ec08-117">ID de diagnostic</span><span class="sxs-lookup"><span data-stu-id="7ec08-117">Diagnostic ID</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-peer-to-peer-session-detail-report"></a><span data-ttu-id="7ec08-118">Exploiter au mieux le rapport détaillé de session P2P</span><span class="sxs-lookup"><span data-stu-id="7ec08-118">Making the Best Use of the Peer-to-Peer session Detail Report</span></span>

<span data-ttu-id="7ec08-p103">Le rapport détaillé de session P2P comprend un grand nombre de mesures, dont bon nombre peuvent être inconnues des administrateurs système. Cependant, dans bien des cas, vous pouvez afficher une info-bulle qui offre une brève description de cette mesure en maintenant simplement votre souris sur l’étiquette de la mesure.</span><span class="sxs-lookup"><span data-stu-id="7ec08-p103">The Peer-to-Peer Session Detail Report includes a large number of metrics, many of which might not be familiar to system administrators. Often-times, however, you can view a tooltip that offers a brief description of that metric simply by holding your mouse over the metric label.</span></span>

<span data-ttu-id="7ec08-p104">Note que les mesures qui s’affichent sur un rapport donné dépendent du type de session P2P que vous avez sélectionné. Une session audio/vidéo et une session de messagerie instantanée n’affichent pas le même ensemble de mesures.</span><span class="sxs-lookup"><span data-stu-id="7ec08-p104">Note that the actual metrics shown on a given report will depend on the type of peer-to-peer session you selected. An audio/video session will report a different set of metrics than an instant messaging session.</span></span>

<span data-ttu-id="7ec08-123">Vous pouvez également pointer votre souris sur les mesures Code de réponse et ID de diagnostic pour obtenir une description de ces valeurs :</span><span class="sxs-lookup"><span data-stu-id="7ec08-123">You can also hold your mouse over the Response code and Diagnostic ID metrics in order to obtain a description of those values:</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="7ec08-124">Filtres</span><span class="sxs-lookup"><span data-stu-id="7ec08-124">Filters</span></span>

<span data-ttu-id="7ec08-p105">Aucun. Vous ne pouvez pas filtrer le Rapport détaillé de session P2P.</span><span class="sxs-lookup"><span data-stu-id="7ec08-p105">None. You cannot filter the Peer-to-Peer Session Detail Report.</span></span>

</div>

<div>

## <a name="session-information-metrics"></a><span data-ttu-id="7ec08-127">Mesures des informations de session</span><span class="sxs-lookup"><span data-stu-id="7ec08-127">Session Information Metrics</span></span>

<span data-ttu-id="7ec08-128">Le tableau ci-dessous liste les informations fournies dans le Rapport détaillé de session P2P de chaque session.</span><span class="sxs-lookup"><span data-stu-id="7ec08-128">The following table lists the information provided in the Peer-to-Peer Session Detail Report for each session.</span></span>

### <a name="session-information-metrics"></a><span data-ttu-id="7ec08-129">Mesures des informations de session</span><span class="sxs-lookup"><span data-stu-id="7ec08-129">Session Information Metrics</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ec08-130">Nom</span><span class="sxs-lookup"><span data-stu-id="7ec08-130">Name</span></span></th>
<th><span data-ttu-id="7ec08-131">Description</span><span class="sxs-lookup"><span data-stu-id="7ec08-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ec08-132"><strong>FQDN du pool</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-132"><strong>Pool FQDN</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-133">Nom de domaine complet (FQDN) du pool de serveurs d’inscriptions ou serveur Edge impliqué dans la session.</span><span class="sxs-lookup"><span data-stu-id="7ec08-133">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server involved in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec08-134"><strong>Heure d’invitation</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-134"><strong>Invite time</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-135">Date et heure auxquelles l’invitation a été envoyée à l’origine.</span><span class="sxs-lookup"><span data-stu-id="7ec08-135">Date and time the session invitation was originally sent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ec08-136"><strong>Heure de réponse</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-136"><strong>Response time</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-137">Date et heure auxquelles l’acceptation de l’invitation a été reçue.</span><span class="sxs-lookup"><span data-stu-id="7ec08-137">Date and time that the invitation acceptance was received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec08-138"><strong>De l’utilisateur</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-138"><strong>From user</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-139">Adresse SIP de l’utilisateur ayant initié la session.</span><span class="sxs-lookup"><span data-stu-id="7ec08-139">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ec08-140"><strong>Agent utilisateur d’origine</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-140"><strong>From user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-141">Logiciel utilisé par le point de terminaison de l’utilisateur ayant initié la session.</span><span class="sxs-lookup"><span data-stu-id="7ec08-141">Software used by the endpoint of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec08-142"><strong>Interne à l’utilisateur d’origine</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-142"><strong>Is From user internal</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-143">Indique si l’utilisateur qui a initié la session était connecté au réseau interne.</span><span class="sxs-lookup"><span data-stu-id="7ec08-143">Indicates whether the user who initiated the session was logged on to the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ec08-144"><strong>Utilisateur d’origine intégré au téléphone de bureau</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-144"><strong>Is From user integrated with desk phone</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-145">Indique si le point de terminaison utilisé par l’utilisateur qui a démarré la session est intégré à son téléphone de bureau.</span><span class="sxs-lookup"><span data-stu-id="7ec08-145">Indicates whether the endpoint used by the user who initiated the session is integrated with his or her desktop phone.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec08-146"><strong>Priorité de la session</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-146"><strong>Session Priority</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-p106">Priorité affectée à la session. Les priorités valides sont : Inconnu, Non urgent, Normal, Urgent et Urgence.</span><span class="sxs-lookup"><span data-stu-id="7ec08-p106">Priority assigned to the session. Valid priorities are: Unknown; Non-Urgent; Normal; Urgent; and Emergency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ec08-149"><strong>Code de réponse</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-149"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-150">Code de réponse SIP envoyé lors de l’échec de session.</span><span class="sxs-lookup"><span data-stu-id="7ec08-150">SIP response code sent when the session failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec08-151"><strong>Serveur frontal</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-151"><strong>Front end</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-152">Nom du serveur frontal utilisé dans la conférence.</span><span class="sxs-lookup"><span data-stu-id="7ec08-152">Name of the Front End Server used in the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ec08-153"><strong>Délai de capture</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-153"><strong>Capture time</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-154">Date et heure auxquelles les informations de session ont été enregistrées.</span><span class="sxs-lookup"><span data-stu-id="7ec08-154">Date and time that the session information was recorded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec08-155"><strong>Heure de fin</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-155"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-156">Date et heure de fin de la session.</span><span class="sxs-lookup"><span data-stu-id="7ec08-156">Date and time the session ended.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ec08-157"><strong>À l’utilisateur</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-157"><strong>To user</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-158">Adresse IP de l’utilisateur ayant été invité à participer à la session.</span><span class="sxs-lookup"><span data-stu-id="7ec08-158">SIP address of the user who was invited to the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec08-159"><strong>Agent utilisateur de destination</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-159"><strong>To user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-160">Logiciel utilisé par le point de terminaison de l’utilisateur qui a été invité à la session.</span><span class="sxs-lookup"><span data-stu-id="7ec08-160">Software used by the endpoint of the user who was invited to the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ec08-161"><strong>Interne à l’utilisateur de destination</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-161"><strong>Is To user internal</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-162">Indique si l’utilisateur qui a été invité à la session était connecté au réseau interne.</span><span class="sxs-lookup"><span data-stu-id="7ec08-162">Indicates whether the user who was invited to the session was logged on to the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec08-163"><strong>Utilisateur de destination intégré au téléphone de bureau</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-163"><strong>Is To user integrated with desk phone</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-164">Indique si le point de terminaison utilisé par l’utilisateur qui a été invité à la session est intégré à son téléphone de bureau.</span><span class="sxs-lookup"><span data-stu-id="7ec08-164">Indicates whether the endpoint used by the user who was invited to the session is integrated with his or her desktop phone.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ec08-165"><strong>Nouvelle tentative de session</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-165"><strong>Is retried session</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-166">Indique si la session est une nouvelle tentative de session qui a précédemment échoué.</span><span class="sxs-lookup"><span data-stu-id="7ec08-166">Indicates whether the session is an attempt to retry a session that previously failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec08-167"><strong>ID de diagnostic</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-167"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-p107">Identificateur unique (sous la forme d’un en-tête ms-diagnostics) joint à un message SIP qui fournit souvent des informations utiles à l’identification et à la résolution des erreurs. Placez la souris au-dessus du numéro d’ID pour afficher des informations supplémentaires sur cet ID.</span><span class="sxs-lookup"><span data-stu-id="7ec08-p107">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Hold the mouse over the ID number to view additional information about that ID.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-modalities"></a><span data-ttu-id="7ec08-170">Mesures des modalités</span><span class="sxs-lookup"><span data-stu-id="7ec08-170">Metrics for Modalities</span></span>

<span data-ttu-id="7ec08-171">Le tableau ci-dessous liste les informations fournies dans le Rapport détaillé de session P2P de chaque modalité de session.</span><span class="sxs-lookup"><span data-stu-id="7ec08-171">The following table lists the information provided in the Peer-to-Peer Session Detail Report for each session modality.</span></span>

### <a name="metrics-for-modalities"></a><span data-ttu-id="7ec08-172">Mesures des modalités</span><span class="sxs-lookup"><span data-stu-id="7ec08-172">Metrics for Modalities</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ec08-173">Nom</span><span class="sxs-lookup"><span data-stu-id="7ec08-173">Name</span></span></th>
<th><span data-ttu-id="7ec08-174">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="7ec08-174">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="7ec08-175">Description</span><span class="sxs-lookup"><span data-stu-id="7ec08-175">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ec08-176"><strong>Modalités</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-176"><strong>Modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-177">Non</span><span class="sxs-lookup"><span data-stu-id="7ec08-177">No</span></span></p></td>
<td><p><span data-ttu-id="7ec08-p108">Modalités utilisées dans la session. Par exemple, messagerie instantanée ou transfert de fichier.</span><span class="sxs-lookup"><span data-stu-id="7ec08-p108">Modalities used in the session. For example, instant messaging (IM) or file transfer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec08-180"><strong>Messages de l’expéditeur</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-180"><strong>From user messages</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-181">Non</span><span class="sxs-lookup"><span data-stu-id="7ec08-181">No</span></span></p></td>
<td><p><span data-ttu-id="7ec08-182">Nombre de messages envoyés par l’utilisateur qui a démarré la session.</span><span class="sxs-lookup"><span data-stu-id="7ec08-182">Number of messages sent by the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ec08-183"><strong>Messages du destinataire</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-183"><strong>To user messages</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-184">Non</span><span class="sxs-lookup"><span data-stu-id="7ec08-184">No</span></span></p></td>
<td><p><span data-ttu-id="7ec08-185">Nombre de messages envoyés par l’utilisateur qui a été invité à rejoindre la session.</span><span class="sxs-lookup"><span data-stu-id="7ec08-185">Number of messages sent by the user who was invited to join the session.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-diagnostic-reports"></a><span data-ttu-id="7ec08-186">Mesures pour les rapports de diagnostic</span><span class="sxs-lookup"><span data-stu-id="7ec08-186">Metrics for Diagnostic Reports</span></span>

<span data-ttu-id="7ec08-187">Le tableau ci-dessous liste les informations fournies dans le Rapport détaillé de session P2P pour chaque rapport de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="7ec08-187">The following table lists the information provided in the Peer-to-Peer Session Detail Report for each diagnostic report.</span></span>

### <a name="metrics-for-diagnostic-reports"></a><span data-ttu-id="7ec08-188">Mesures pour les rapports de diagnostic</span><span class="sxs-lookup"><span data-stu-id="7ec08-188">Metrics for Diagnostic Reports</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ec08-189">Nom</span><span class="sxs-lookup"><span data-stu-id="7ec08-189">Name</span></span></th>
<th><span data-ttu-id="7ec08-190">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="7ec08-190">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="7ec08-191">Description</span><span class="sxs-lookup"><span data-stu-id="7ec08-191">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ec08-192"><strong>Détails</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-192"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-193">Non</span><span class="sxs-lookup"><span data-stu-id="7ec08-193">No</span></span></p></td>
<td><p><span data-ttu-id="7ec08-194">Lorsque vous cliquez sur cet élément, le rapport montre le rapport de diagnostic pour la session.</span><span class="sxs-lookup"><span data-stu-id="7ec08-194">When you click this item, the report shows the Diagnostic Report for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec08-195"><strong>Heure du rapport</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-195"><strong>Report time</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-196">Non</span><span class="sxs-lookup"><span data-stu-id="7ec08-196">No</span></span></p></td>
<td><p><span data-ttu-id="7ec08-197">Date et heure d’enregistrement du rapport.</span><span class="sxs-lookup"><span data-stu-id="7ec08-197">Date and time the report was recorded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ec08-198"><strong>Demande</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-198"><strong>Request</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-199">Non</span><span class="sxs-lookup"><span data-stu-id="7ec08-199">No</span></span></p></td>
<td><p><span data-ttu-id="7ec08-p109">Type de demande SIP. Par exemple, INVITE ou BYE.</span><span class="sxs-lookup"><span data-stu-id="7ec08-p109">SIP request type. For example, INVITE or BYE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec08-202"><strong>ID de diagnostic</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-202"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-203">Non</span><span class="sxs-lookup"><span data-stu-id="7ec08-203">No</span></span></p></td>
<td><p><span data-ttu-id="7ec08-204">Identificateur unique (sous la forme d’un en-tête ms-diagnostics) attaché à un message SIP qui fournit souvent des informations utiles pour résoudre des erreurs.</span><span class="sxs-lookup"><span data-stu-id="7ec08-204">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ec08-205"><strong>Type de contenu</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-205"><strong>Content type</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-206">Non</span><span class="sxs-lookup"><span data-stu-id="7ec08-206">No</span></span></p></td>
<td><p><span data-ttu-id="7ec08-p110">Type de contenu multimédia utilisé dans la conférence. Par exemple, Application/sdp est un type de contenu commun. Le protocole SDP (Session Description Protocol) est un protocole Internet standard utilisé pour les annonces de session, les invitations aux sessions et autres formes de démarrage de session multimédia.</span><span class="sxs-lookup"><span data-stu-id="7ec08-p110">Type of media content used in the conference. For example, a common content type is Application/sdp. Session Description Protocol (SDP) is a standard Internet protocol used for session announcements, session invitations, and other forms of multimedia session initiation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec08-210"><strong>Auteur du rapport</strong></span><span class="sxs-lookup"><span data-stu-id="7ec08-210"><strong>Reported by</strong></span></span></p></td>
<td><p><span data-ttu-id="7ec08-211">Non</span><span class="sxs-lookup"><span data-stu-id="7ec08-211">No</span></span></p></td>
<td><p><span data-ttu-id="7ec08-212">Ordinateur (c’est-à-dire, client ou serveur) qui a signalé le problème.</span><span class="sxs-lookup"><span data-stu-id="7ec08-212">Computer (that is, client or server) that reported the problem.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7ec08-213">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7ec08-213">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

