---
title: 'Lync Server 2013 : rapports de diagnostic d’appel'
description: 'Lync Server 2013 : rapports de diagnostic d’appel.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Diagnostic Reports
ms:assetid: 8d362dd9-a119-4601-a3b4-3e7ed0aaa92e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615013(v=OCS.15)
ms:contentKeyID: 48184794
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6acc41585414e134eebde1635729b470c7f3472c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394800"
---
# <a name="call-diagnostic-reports-in-lync-server-2013"></a><span data-ttu-id="12e61-103">Rapports de diagnostic des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="12e61-103">Call Diagnostic Reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="12e61-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="12e61-104">

<span> </span></span></span>

<span data-ttu-id="12e61-105">_**Dernière modification de la rubrique :** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="12e61-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="12e61-106">Les rapports de diagnostic des appels fournissent des informations récapitulatives et des données de diagnostic relatives aux sessions P2P et de conférence ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="12e61-106">The Call Diagnostic Reports provide summary information and diagnostic data for failed peer-to-peer and conferencing sessions.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="12e61-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="12e61-107">In This Section</span></span>

  - <span data-ttu-id="12e61-108">[Rapport de synthèse de diagnostic des appels dans Lync Server 2013](lync-server-2013-call-diagnostic-summary-report.md)   Fournit un récapitulatif global des sessions d’égal à égal et de conférences.</span><span class="sxs-lookup"><span data-stu-id="12e61-108">[Call Diagnostic Summary Report in Lync Server 2013](lync-server-2013-call-diagnostic-summary-report.md)   Provides an overall summary of failed peer-to-peer sessions and conference sessions.</span></span> <span data-ttu-id="12e61-109">Les sessions P2P sont des sessions impliquant seulement deux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="12e61-109">Peer-to-peer sessions are sessions that involve just two participants.</span></span> <span data-ttu-id="12e61-110">Les sessions de conférence impliquent trois participants ou plus.</span><span class="sxs-lookup"><span data-stu-id="12e61-110">Conferencing sessions involve three or more participants.</span></span>

  - <span data-ttu-id="12e61-111">[Rapport de diagnostic d’activité d’égal à égal dans Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md)   Fournit une vue de tendance globale des sessions d’égal à égal en échec.</span><span class="sxs-lookup"><span data-stu-id="12e61-111">[Peer-to-Peer Activity Diagnostic Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md)   Provides an overall trend view of failed peer-to-peer sessions.</span></span> <span data-ttu-id="12e61-112">Une session P2P implique uniquement deux participants.</span><span class="sxs-lookup"><span data-stu-id="12e61-112">A peer-to-peer session involves just two participants.</span></span>

  - <span data-ttu-id="12e61-113">[Rapport de diagnostic de conférence dans Lync Server 2013](lync-server-2013-conference-diagnostic-report.md)   Fournit une vue d’ensemble des tendances des sessions de conférence et des vues de tendance en échec pour chaque modalité de conférence.</span><span class="sxs-lookup"><span data-stu-id="12e61-113">[Conference Diagnostic Report in Lync Server 2013](lync-server-2013-conference-diagnostic-report.md)   Provides an overall trend view of failed conferencing sessions and trend views for each conference modality.</span></span> <span data-ttu-id="12e61-114">Les sessions de conférence impliquent au moins trois participants.</span><span class="sxs-lookup"><span data-stu-id="12e61-114">Conferencing sessions involve at least three participants.</span></span>

  - <span data-ttu-id="12e61-115">[Rapport sur les principaux échecs dans Lync Server 2013](lync-server-2013-top-failures-report.md)   Dresse la liste des erreurs les plus fréquentes et leurs tendances dans le temps.</span><span class="sxs-lookup"><span data-stu-id="12e61-115">[Top Failures Report in Lync Server 2013](lync-server-2013-top-failures-report.md)   Provides a list of the most frequent failures and their trends over time.</span></span>

  - <span data-ttu-id="12e61-116">[Rapport de distribution des échecs dans Lync Server 2013](lync-server-2013-failure-distribution-report.md)   Fournit une analyse des sessions ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="12e61-116">[Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md)   Provides an analysis of failed sessions.</span></span>

  - <span data-ttu-id="12e61-117">[Rapport de liste des échecs dans Lync Server 2013](lync-server-2013-failure-list-report.md)   Fournit des informations détaillées sur les participants individuels impliqués dans une conférence en échec.</span><span class="sxs-lookup"><span data-stu-id="12e61-117">[Failure List Report in Lync Server 2013](lync-server-2013-failure-list-report.md)   Provides detailed information about the individual participants involved in a failed conference.</span></span>

  - <span data-ttu-id="12e61-118">[Rapport de diagnostic dans Lync Server 2013](lync-server-2013-diagnostic-report.md)   Fournit des informations de diagnostic et de dépannage (y compris les codes de réponse SIP et les en-têtes et ID de diagnostic) pour les échecs de session.</span><span class="sxs-lookup"><span data-stu-id="12e61-118">[Diagnostic Report in Lync Server 2013](lync-server-2013-diagnostic-report.md)   Provides diagnostic and troubleshooting information (including SIP response codes and diagnostic headers and IDs) for failed sessions.</span></span>

<span data-ttu-id="12e61-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="12e61-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

