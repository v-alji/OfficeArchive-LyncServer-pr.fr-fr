---
title: 'Lync Server 2013 : rapport Détails de la Conférence'
description: 'Lync Server 2013 : rapport détaillé sur la Conférence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Detail Report
ms:assetid: 1d61cd81-dcfe-40b4-9a41-a73b038bc216
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204728(v=OCS.15)
ms:contentKeyID: 48183565
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07c50b545f4a9ee3308a840fc2aa5a15e617a5bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394205"
---
# <a name="conference-detail-report-in-lync-server-2013"></a><span data-ttu-id="c9a08-103">Rapport Détails de la Conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c9a08-103">Conference Detail Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c9a08-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c9a08-104">

<span> </span></span></span>

<span data-ttu-id="c9a08-105">_**Dernière modification de la rubrique :** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="c9a08-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="c9a08-p101">Le rapport détaillé de conférence donne des informations détaillées sur tous les utilisateurs qui ont participé à une conférence. Vous pouvez par exemple voir des informations, telles que la date et l’heure auxquelles un utilisateur s’est joint à la conférence, la date et l’heure auxquelles l’utilisateur a quitté la conférence et l’agent utilisateur du point de terminaison qui a permis à l’utilisateur de se connecter à la conférence. Vous pouvez également afficher des informations sur le rôle de l’utilisateur dans chaque conférence (par exemple présentateur ou participant). Ce qui est peut-être le plus important, vous pouvez voir rapidement quels utilisateurs ont réussi à rejoindre et suivre la conférence et quels utilisateurs n’ont pas réussi à rejoindre et suivre la conférence.</span><span class="sxs-lookup"><span data-stu-id="c9a08-p101">The Conference Detail Report provides detailed information about all the users who participated in a conference. For example, you can see such information as the date and time that a user joined the conference, the date and time that the user left the conference, and the user agent of the endpoint that was used to connect that user to the conference. You can also see information the user's role in each conference (for example, Presenter or Attendee). Perhaps most important, you get quickly see which users successfully join and complete the conference, and which users were not able to successfully join and complete the conference.</span></span>

<div>

## <a name="accessing-the-conference-detail-report"></a><span data-ttu-id="c9a08-110">Accès au rapport détaillé de conférence</span><span class="sxs-lookup"><span data-stu-id="c9a08-110">Accessing the Conference Detail Report</span></span>

<span data-ttu-id="c9a08-111">Le rapport détaillé de conférence est accessible à partir des rapports suivants :</span><span class="sxs-lookup"><span data-stu-id="c9a08-111">The Conference Detail Report can be accessed from the following reports:</span></span>

  - <span data-ttu-id="c9a08-112">[Rapport de contrôle d’admission des appels dans Lync Server 2013](lync-server-2013-call-admission-control-report.md) (en cliquant sur la métrique détaillée pour une conférence)</span><span class="sxs-lookup"><span data-stu-id="c9a08-112">The [Call Admission Control Report in Lync Server 2013](lync-server-2013-call-admission-control-report.md) (by clicking the Detail metric for a conference)</span></span>

  - <span data-ttu-id="c9a08-113">[Rapport de la liste des échecs dans Lync Server 2013](lync-server-2013-failure-list-report.md) (en cliquant sur la mesure de conférence)</span><span class="sxs-lookup"><span data-stu-id="c9a08-113">The [Failure List Report in Lync Server 2013](lync-server-2013-failure-list-report.md) (by clicking the Conference metric)</span></span>

  - <span data-ttu-id="c9a08-114">[Rapport activité de l’utilisateur dans Lync Server 2013](lync-server-2013-user-activity-report.md) (en cliquant sur la métrique de l’URI de la Conférence)</span><span class="sxs-lookup"><span data-stu-id="c9a08-114">The [User Activity Report in Lync Server 2013](lync-server-2013-user-activity-report.md) (by clicking the Conference URI metric)</span></span>

<span data-ttu-id="c9a08-115">À partir du rapport Détails de la Conférence, vous pouvez accéder au [rapport de diagnostic dans Lync Server 2013](lync-server-2013-diagnostic-report.md) en cliquant sur le rapport de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="c9a08-115">From the Conference Detail Report you can access the [Diagnostic Report in Lync Server 2013](lync-server-2013-diagnostic-report.md) by clicking the Diagnostic Report (Detail) metric.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="c9a08-116">Filtres</span><span class="sxs-lookup"><span data-stu-id="c9a08-116">Filters</span></span>

<span data-ttu-id="c9a08-p102">Aucun. Vous ne pouvez pas filtrer sur le rapport détaillé de conférence.</span><span class="sxs-lookup"><span data-stu-id="c9a08-p102">None. You cannot filter on the Conference Detail Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="c9a08-119">Mesures</span><span class="sxs-lookup"><span data-stu-id="c9a08-119">Metrics</span></span>

<span data-ttu-id="c9a08-120">Le tableau qui suit répertorie les informations fournies dans la section Informations de conférence du rapport détaillé de conférence.</span><span class="sxs-lookup"><span data-stu-id="c9a08-120">The following table lists the information provided in the Conference Information section of the Conference Detail Report.</span></span>

### <a name="conference-information-metrics"></a><span data-ttu-id="c9a08-121">Mesures des informations de conférence</span><span class="sxs-lookup"><span data-stu-id="c9a08-121">Conference Information Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9a08-122">Nom</span><span class="sxs-lookup"><span data-stu-id="c9a08-122">Name</span></span></th>
<th><span data-ttu-id="c9a08-123">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="c9a08-123">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="c9a08-124">Description</span><span class="sxs-lookup"><span data-stu-id="c9a08-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9a08-125"><strong>URI de la conférence</strong></span><span class="sxs-lookup"><span data-stu-id="c9a08-125"><strong>Conference URI</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9a08-p103">URI affectée à la conférence. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="c9a08-p103">URI assigned to the conference. For example:</span></span></p>
<p><span data-ttu-id="c9a08-128">sip:kmyer@litwareinc.com;gruu;opaque=app:conf:focus:id:drg2y8v4</span><span class="sxs-lookup"><span data-stu-id="c9a08-128">sip:kmyer@litwareinc.com;gruu;opaque=app:conf:focus:id:drg2y8v4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9a08-129"><strong>FQDN du pool</strong></span><span class="sxs-lookup"><span data-stu-id="c9a08-129"><strong>Pool FQDN</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9a08-130">Nom de domaine complet du pool de serveurs d’inscriptions ou serveur Edge impliqué dans une session.</span><span class="sxs-lookup"><span data-stu-id="c9a08-130">Fully-qualified domain name of the Registrar pool or Edge Server involved in a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9a08-131"><strong>Heure de début</strong></span><span class="sxs-lookup"><span data-stu-id="c9a08-131"><strong>Start time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9a08-132">Date et heure auxquelles la conférence a commencé.</span><span class="sxs-lookup"><span data-stu-id="c9a08-132">Date and time that the conference started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9a08-133"><strong>Organisateur</strong></span><span class="sxs-lookup"><span data-stu-id="c9a08-133"><strong>Organizer</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9a08-134">Adresse SIP de l’utilisateur qui a organisé la conférence.</span><span class="sxs-lookup"><span data-stu-id="c9a08-134">SIP address of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9a08-135"><strong>Heure de fin</strong></span><span class="sxs-lookup"><span data-stu-id="c9a08-135"><strong>End time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9a08-136">Date et heure de fin de la conférence.</span><span class="sxs-lookup"><span data-stu-id="c9a08-136">Date and time that the conference ended.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c9a08-137">Le tableau qui suit répertorie les informations fournies dans la section Participation à la conférence du rapport détaille de conférence.</span><span class="sxs-lookup"><span data-stu-id="c9a08-137">The following table lists the information provided in the Conference Participation Section of the Conference Detail Report.</span></span>

### <a name="conference-participation-metrics"></a><span data-ttu-id="c9a08-138">Mesures de participation à la conférence</span><span class="sxs-lookup"><span data-stu-id="c9a08-138">Conference Participation Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9a08-139">Nom</span><span class="sxs-lookup"><span data-stu-id="c9a08-139">Name</span></span></th>
<th><span data-ttu-id="c9a08-140">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="c9a08-140">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="c9a08-141">Description</span><span class="sxs-lookup"><span data-stu-id="c9a08-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9a08-142"><strong>Utilisateur</strong></span><span class="sxs-lookup"><span data-stu-id="c9a08-142"><strong>User</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9a08-143">Adresse SIP de l’utilisateur qui a participé à la conférence.</span><span class="sxs-lookup"><span data-stu-id="c9a08-143">SIP address of the user who participated in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9a08-144"><strong>Rôle</strong></span><span class="sxs-lookup"><span data-stu-id="c9a08-144"><strong>Role</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9a08-145">Rôle (par exemple, présentateur) joué par le participant à la conférence.</span><span class="sxs-lookup"><span data-stu-id="c9a08-145">Role (for example, Presenter) played by the conference participant.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9a08-146"><strong>Connectivité</strong></span><span class="sxs-lookup"><span data-stu-id="c9a08-146"><strong>Connectivity</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9a08-147">Connectivité réseau (généralement Depuis interne ou Depuis externe) du participant.</span><span class="sxs-lookup"><span data-stu-id="c9a08-147">Network connectivity (typically From Internal or From External) for the participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9a08-148">Heure d’arrivée</span><span class="sxs-lookup"><span data-stu-id="c9a08-148">Join time</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9a08-149">Date et heure auxquelles le participant a rejoint la conférence.</span><span class="sxs-lookup"><span data-stu-id="c9a08-149">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9a08-150"><strong>Heure de départ</strong></span><span class="sxs-lookup"><span data-stu-id="c9a08-150"><strong>Leave time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9a08-151">Date et heure auxquelles le participant a quitté la conférence.</span><span class="sxs-lookup"><span data-stu-id="c9a08-151">Date and time that the participant left the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9a08-152"><strong>Agent utilisateur</strong></span><span class="sxs-lookup"><span data-stu-id="c9a08-152"><strong>User agent</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9a08-153">Identifiant du logiciel utilisé par le point de terminaison du participant.</span><span class="sxs-lookup"><span data-stu-id="c9a08-153">Identifier for the software used by the participant’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9a08-154"><strong>Rapports de diagnostic</strong></span><span class="sxs-lookup"><span data-stu-id="c9a08-154"><strong>Diagnostic reports</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9a08-p104">Fournit des informations de diagnostic et de résolution des problèmes, notamment les codes de réponse SIP, les en-têtes de diagnostic, les temps de connexion à la conférence et les ID de diagnostic des sessions qui ont échoué.</span><span class="sxs-lookup"><span data-stu-id="c9a08-p104">Provides diagnostic and troubleshooting information. Including SIP response codes, diagnostic headers, conference join times, and diagnostic IDs for failed sessions.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c9a08-157">Le tableau suivant répertorie les informations fournies dans la section modalités de la Conférence du rapport Détails de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="c9a08-157">The following table lists the information provided in the Conference Modalities section of the Conference Detail Report.</span></span>

### <a name="conference-modalities-metrics"></a><span data-ttu-id="c9a08-158">Mesures des modalités de conférence</span><span class="sxs-lookup"><span data-stu-id="c9a08-158">Conference Modalities Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9a08-159">Nom</span><span class="sxs-lookup"><span data-stu-id="c9a08-159">Name</span></span></th>
<th><span data-ttu-id="c9a08-160">Est-il possible d’effectuer un tri sur cet élément ?</span><span class="sxs-lookup"><span data-stu-id="c9a08-160">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="c9a08-161">Description</span><span class="sxs-lookup"><span data-stu-id="c9a08-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9a08-162"><strong>Utilisateur</strong></span><span class="sxs-lookup"><span data-stu-id="c9a08-162"><strong>User</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9a08-163">Adresse SIP de l’utilisateur qui a participé à la conférence.</span><span class="sxs-lookup"><span data-stu-id="c9a08-163">SIP address of the user who participated in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9a08-164"><strong>Heure d’arrivée</strong></span><span class="sxs-lookup"><span data-stu-id="c9a08-164"><strong>Join time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9a08-165">Date et heure auxquelles le participant a rejoint la conférence.</span><span class="sxs-lookup"><span data-stu-id="c9a08-165">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9a08-166"><strong>Heure de départ</strong></span><span class="sxs-lookup"><span data-stu-id="c9a08-166"><strong>Leave time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9a08-167">Date et heure auxquelles un participant a quitté la conférence.</span><span class="sxs-lookup"><span data-stu-id="c9a08-167">Date and time that a participant left the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9a08-168"><strong>URI du serveur de conférence</strong></span><span class="sxs-lookup"><span data-stu-id="c9a08-168"><strong>Conferencing server URI</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9a08-169">URI du serveur de conférence utilisé dans la conférence.</span><span class="sxs-lookup"><span data-stu-id="c9a08-169">URI for the Conferencing server used in the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9a08-170"><strong>Rapports de diagnostic</strong></span><span class="sxs-lookup"><span data-stu-id="c9a08-170"><strong>Diagnostic reports</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c9a08-p105">Fournit des informations de diagnostic et de résolution des problèmes, notamment les codes de réponse SIP, les en-têtes de diagnostic, les temps de connexion à la conférence et les ID de diagnostic des sessions qui ont échoué.</span><span class="sxs-lookup"><span data-stu-id="c9a08-p105">Provides diagnostic and troubleshooting information. Including SIP response codes, diagnostic headers, conference join times, and diagnostic IDs for failed sessions.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c9a08-173">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c9a08-173">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

