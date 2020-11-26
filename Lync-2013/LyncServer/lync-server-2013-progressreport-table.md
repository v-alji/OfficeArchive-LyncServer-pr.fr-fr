---
title: 'Lync Server 2013 : Table ProgressReport'
description: 'Tableau Lync Server 2013 : ProgressReport'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ProgressReport table
ms:assetid: 38e5f060-5e9b-4185-87b2-7ef61c4bb75f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425864(v=OCS.15)
ms:contentKeyID: 48183847
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d36ee2ab75410ea2462da4b647ef5b45afefb1bb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436866"
---
# <a name="progressreport-table-in-lync-server-2013"></a><span data-ttu-id="8d555-103">Table ProgressReport dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8d555-103">ProgressReport table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8d555-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8d555-104">

<span> </span></span></span>

<span data-ttu-id="8d555-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="8d555-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="8d555-106">Les rapports de progression sont basés sur les données chargées par le client dans la base de données une fois l’appel ou la session terminée.</span><span class="sxs-lookup"><span data-stu-id="8d555-106">Progress reports are based on data uploaded by the client to the database after a call or session is completed.</span></span> <span data-ttu-id="8d555-107">Les rapports de progression seront écrits uniquement pour les appels et les sessions que Lync Server 2013 détermine peut être utile à des fins de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="8d555-107">Progress reports will be written only for calls and sessions that Lync Server 2013 determines might be useful for diagnostic purposes.</span></span>

<span data-ttu-id="8d555-108">Les champs ErrorTime, ErrorReportSeq et ProgressReportSeq ne font pas nécessairement référence aux erreurs, mais aux messages indiquant l’état des appels ou des messages.</span><span class="sxs-lookup"><span data-stu-id="8d555-108">The ErrorTime, ErrorReportSeq and ProgressReportSeq fields don’t necessarily refer to errors but to messages that indicate the status of calls or messages.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8d555-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="8d555-109">Column</span></span></th>
<th><span data-ttu-id="8d555-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="8d555-110">Data Type</span></span></th>
<th><span data-ttu-id="8d555-111">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="8d555-111">Key/Index</span></span></th>
<th><span data-ttu-id="8d555-112">Détails</span><span class="sxs-lookup"><span data-stu-id="8d555-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d555-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="8d555-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8d555-114">DateHeure</span><span class="sxs-lookup"><span data-stu-id="8d555-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="8d555-115">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="8d555-115">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="8d555-116">Date et heure du rapport d’erreur de progression contenant ce rapport de progression.</span><span class="sxs-lookup"><span data-stu-id="8d555-116">Date and time of the progress error report that contains this progress report.</span></span> <span data-ttu-id="8d555-117">Pour plus d’informations, voir la <a href="lync-server-2013-errorreport-table.md">table errorreport dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8d555-117">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d555-118"><strong>ErrorId</strong></span><span class="sxs-lookup"><span data-stu-id="8d555-118"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="8d555-119">int</span><span class="sxs-lookup"><span data-stu-id="8d555-119">int</span></span></p></td>
<td><p><span data-ttu-id="8d555-120">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="8d555-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="8d555-121">Numéro d’identification utilisé conjointement avec ErrorTime, ProgressReportSeq pour identifier de façon unique un rapport de progression.</span><span class="sxs-lookup"><span data-stu-id="8d555-121">ID number used in conjunction with ErrorTime, ProgressReportSeq to uniquely identify a progress report.</span></span> <span data-ttu-id="8d555-122">Pour plus d’informations, voir la <a href="lync-server-2013-errorreport-table.md">table errorreport dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8d555-122">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d555-123"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="8d555-123"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="8d555-124">int</span><span class="sxs-lookup"><span data-stu-id="8d555-124">int</span></span></p></td>
<td><p><span data-ttu-id="8d555-125">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="8d555-125">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="8d555-126">Numéro identifiant le rapport d’erreur.</span><span class="sxs-lookup"><span data-stu-id="8d555-126">ID number that identifies the error report.</span></span> <span data-ttu-id="8d555-127">ErrorReporSeq est utilisé en conjonction avec ErrorTime pour identifier de manière unique un rapport d’erreur.</span><span class="sxs-lookup"><span data-stu-id="8d555-127">ErrorReporSeq is used in conjunction with ErrorTime to uniquely identify an error report.</span></span> <span data-ttu-id="8d555-128">Pour plus d’informations, voir la <a href="lync-server-2013-errorreport-table.md">table errorreport dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8d555-128">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information</span></span></p>
<p><span data-ttu-id="8d555-129">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8d555-129">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d555-130"><strong>ProgressReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="8d555-130"><strong>ProgressReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="8d555-131">int</span><span class="sxs-lookup"><span data-stu-id="8d555-131">int</span></span></p></td>
<td><p><span data-ttu-id="8d555-132">Principal</span><span class="sxs-lookup"><span data-stu-id="8d555-132">Primary</span></span></p></td>
<td><p><span data-ttu-id="8d555-133">Numéro d’identification pour identifier le rapport de progression.</span><span class="sxs-lookup"><span data-stu-id="8d555-133">ID number to identify the progress report.</span></span> <span data-ttu-id="8d555-134">Utilisé conjointement avec ErrorTime et ErrorReportSeq pour identifier de manière unique un rapport de progression.</span><span class="sxs-lookup"><span data-stu-id="8d555-134">Used in conjunction with ErrorTime and ErrorReportSeq to uniquely identify a progress report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d555-135"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="8d555-135"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="8d555-136">int</span><span class="sxs-lookup"><span data-stu-id="8d555-136">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8d555-137">ID de diagnostic du rapport de progression.</span><span class="sxs-lookup"><span data-stu-id="8d555-137">Diagnostic ID of the progress report.</span></span></p>
<p><span data-ttu-id="8d555-138">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8d555-138">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d555-139"><strong>SourceId</strong></span><span class="sxs-lookup"><span data-stu-id="8d555-139"><strong>SourceId</strong></span></span></p></td>
<td><p><span data-ttu-id="8d555-140">int</span><span class="sxs-lookup"><span data-stu-id="8d555-140">int</span></span></p></td>
<td><p><span data-ttu-id="8d555-141">Externes</span><span class="sxs-lookup"><span data-stu-id="8d555-141">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8d555-142">Serveur ayant envoyé le rapport d’erreur (si le rapport a été envoyé à partir d’un composant serveur).</span><span class="sxs-lookup"><span data-stu-id="8d555-142">Server that sent the error report (if the report was sent from a server component).</span></span> <span data-ttu-id="8d555-143">Pour plus d’informations, voir le <a href="lync-server-2013-servers-table.md">tableau des serveurs dans Lync Server 2013</a> . Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8d555-143">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d555-144"><strong>ApplicationId</strong></span><span class="sxs-lookup"><span data-stu-id="8d555-144"><strong>ApplicationId</strong></span></span></p></td>
<td><p><span data-ttu-id="8d555-145">int</span><span class="sxs-lookup"><span data-stu-id="8d555-145">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8d555-146">Le processus serveur Lync dont le rapport est sujet.</span><span class="sxs-lookup"><span data-stu-id="8d555-146">The Lync Server process that the report is about.</span></span> <span data-ttu-id="8d555-147">Pour plus d’informations, consultez le tableau de l’application.</span><span class="sxs-lookup"><span data-stu-id="8d555-147">See the Application Table for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d555-148"><strong>Détails</strong></span><span class="sxs-lookup"><span data-stu-id="8d555-148"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="8d555-149">image</span><span class="sxs-lookup"><span data-stu-id="8d555-149">image</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8d555-150">Détails du rapport de progression, enregistrés au format binaire pour économiser de l’espace. Il est possible de convertir les données au format texte à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="8d555-150">Progress report details, stored in binary format to save space.This data can be converted to text format using this syntax:</span></span></p>
<p><span data-ttu-id="8d555-151">Cast (de type « detail ») As varchar (max))</span><span class="sxs-lookup"><span data-stu-id="8d555-151">cast(cast(Detail as varbinary(max)) as varchar(max))</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d555-152"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="8d555-152"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="8d555-153">Identificateur</span><span class="sxs-lookup"><span data-stu-id="8d555-153">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8d555-154">Identificateur unique qui met en corrélation les informations de connexion aux différents composants impliqués dans une conférence.</span><span class="sxs-lookup"><span data-stu-id="8d555-154">Unique identifier that correlates join time information for the different components involved in a conference.</span></span></p>
<p><span data-ttu-id="8d555-155">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8d555-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d555-156"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="8d555-156"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8d555-157">int</span><span class="sxs-lookup"><span data-stu-id="8d555-157">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8d555-158">Durée (en millisecondes) d’un composant spécifique pour participer à une conférence.</span><span class="sxs-lookup"><span data-stu-id="8d555-158">Time (in milliseconds) for a specific component to join a conference.</span></span></p>
<p><span data-ttu-id="8d555-159">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8d555-159">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8d555-160">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8d555-160">


</div>

<span> </span>

</div>

</div>

</span></span></div>

