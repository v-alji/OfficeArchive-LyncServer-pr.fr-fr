---
title: 'Affichage Lync Server 2013 : ProgressReport'
description: 'Affichage Lync Server 2013 : ProgressReport'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ProgressReport view
ms:assetid: b49f3fc7-0e2f-498f-8505-aaaf54e435f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721857(v=OCS.15)
ms:contentKeyID: 49733790
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b95086012f254499644e778e43cafdf70ffc8f9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436852"
---
# <a name="progressreport-view-in-lync-server-2013"></a><span data-ttu-id="02f7b-103">Affichage ProgressReport dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="02f7b-103">ProgressReport view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="02f7b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="02f7b-104">

<span> </span></span></span>

<span data-ttu-id="02f7b-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="02f7b-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="02f7b-106">L’affichage ProgressReport stocke les informations sur les sessions terminées.</span><span class="sxs-lookup"><span data-stu-id="02f7b-106">The ProgressReport view stores information about completed sessions.</span></span> <span data-ttu-id="02f7b-107">Les rapports de progression seront écrits uniquement pour les appels et les sessions que Lync Server 2013 détermine peut être utile à des fins de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="02f7b-107">Progress reports will be written only for calls and sessions that Lync Server 2013 determines might be useful for diagnostic purposes.</span></span> <span data-ttu-id="02f7b-108">Cet affichage a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="02f7b-108">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="02f7b-109">Les champs ErrorTime, ErrorReportSeq et ProgressReportSeq ne font pas nécessairement référence aux erreurs, mais aux messages indiquant l’état des appels ou des messages.</span><span class="sxs-lookup"><span data-stu-id="02f7b-109">The ErrorTime, ErrorReportSeq and ProgressReportSeq fields don’t necessarily refer to errors but to messages that indicate the status of calls or messages.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02f7b-110">Colonne</span><span class="sxs-lookup"><span data-stu-id="02f7b-110">Column</span></span></th>
<th><span data-ttu-id="02f7b-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="02f7b-111">Data Type</span></span></th>
<th><span data-ttu-id="02f7b-112">Détails</span><span class="sxs-lookup"><span data-stu-id="02f7b-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02f7b-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="02f7b-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="02f7b-114">DateHeure</span><span class="sxs-lookup"><span data-stu-id="02f7b-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="02f7b-115">L’heure de l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="02f7b-115">Time of error occurred.</span></span> <span data-ttu-id="02f7b-116">Utilisé conjointement avec ErrorReportSeq pour identifier de manière unique une erreur.</span><span class="sxs-lookup"><span data-stu-id="02f7b-116">Used in conjunction with ErrorReportSeq to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02f7b-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="02f7b-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="02f7b-118">int</span><span class="sxs-lookup"><span data-stu-id="02f7b-118">int</span></span></p></td>
<td><p><span data-ttu-id="02f7b-119">Numéro d’identification pour identifier l’erreur.</span><span class="sxs-lookup"><span data-stu-id="02f7b-119">ID number to identify the error.</span></span> <span data-ttu-id="02f7b-120">Utilisé conjointement avec ErrorTime pour identifier de manière unique une erreur.</span><span class="sxs-lookup"><span data-stu-id="02f7b-120">Used in conjunction with ErrorTime to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02f7b-121"><strong>ProgressReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="02f7b-121"><strong>ProgressReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="02f7b-122">int</span><span class="sxs-lookup"><span data-stu-id="02f7b-122">int</span></span></p></td>
<td><p><span data-ttu-id="02f7b-123">ID pour identifier le rapport de progression.</span><span class="sxs-lookup"><span data-stu-id="02f7b-123">ID to identify the progress report.</span></span> <span data-ttu-id="02f7b-124">Permet de distinguer les rapports de progression d’un même rapport d’erreur.</span><span class="sxs-lookup"><span data-stu-id="02f7b-124">Used to distinguish progress reports of the same error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02f7b-125"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="02f7b-125"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="02f7b-126">int</span><span class="sxs-lookup"><span data-stu-id="02f7b-126">int</span></span></p></td>
<td><p><span data-ttu-id="02f7b-127">ID de diagnostic du rapport d’erreur.</span><span class="sxs-lookup"><span data-stu-id="02f7b-127">Diagnostic ID for the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02f7b-128"><strong>Source</strong></span><span class="sxs-lookup"><span data-stu-id="02f7b-128"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="02f7b-129">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="02f7b-129">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="02f7b-130">Nom du serveur à l’origine de l’erreur (si le rapport a été envoyé à partir d’un composant serveur).</span><span class="sxs-lookup"><span data-stu-id="02f7b-130">Name of server that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02f7b-131"><strong>Application</strong></span><span class="sxs-lookup"><span data-stu-id="02f7b-131"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="02f7b-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="02f7b-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="02f7b-133">Nom de l’application à l’origine de l’erreur (si le rapport a été envoyé à partir d’un composant serveur).</span><span class="sxs-lookup"><span data-stu-id="02f7b-133">Name of application that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02f7b-134"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="02f7b-134"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="02f7b-135">identificateur</span><span class="sxs-lookup"><span data-stu-id="02f7b-135">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="02f7b-136">Identifiant unique permettant de corréler les informations de connexion aux différents composants participant à une conférence.</span><span class="sxs-lookup"><span data-stu-id="02f7b-136">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02f7b-137"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="02f7b-137"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="02f7b-138">int</span><span class="sxs-lookup"><span data-stu-id="02f7b-138">int</span></span></p></td>
<td><p><span data-ttu-id="02f7b-139">Durée (en millisecondes) requise pour un composant spécifique pour participer à une conférence.</span><span class="sxs-lookup"><span data-stu-id="02f7b-139">Time (in milliseconds) required for a specific component to join a conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02f7b-140"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="02f7b-140"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="02f7b-141">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="02f7b-141">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="02f7b-142">Informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="02f7b-142">Additional error information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="02f7b-143">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="02f7b-143">


</div>

<span> </span>

</div>

</div>

</span></span></div>

