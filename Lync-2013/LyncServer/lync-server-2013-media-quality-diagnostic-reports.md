---
title: 'Lync Server 2013 : rapports de diagnostic de qualité multimédia'
description: 'Lync Server 2013 : rapports de diagnostic de qualité multimédia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media Quality Diagnostic Reports
ms:assetid: ea61428e-a1d5-4189-aae6-3db19ddc5cf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615044(v=OCS.15)
ms:contentKeyID: 48185935
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2e346d0f9b8997158cb926ad830d5477950e846d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395204"
---
# <a name="media-quality-diagnostic-reports-in-lync-server-2013"></a><span data-ttu-id="8d508-103">Rapports de diagnostic de qualité multimédia dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8d508-103">Media Quality Diagnostic Reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8d508-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8d508-104">

<span> </span></span></span>

<span data-ttu-id="8d508-105">_**Dernière modification de la rubrique :** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="8d508-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="8d508-106">Les rapports de diagnostic de la qualité des médias fournissent des informations sur la qualité des appels, ainsi que des informations de diagnostic et de résolution des problèmes pour les appels ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="8d508-106">The Media Quality Diagnostic Reports provide information about call quality, and diagnostic and troubleshooting information for failed calls.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="8d508-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="8d508-107">In This Section</span></span>

  - <span data-ttu-id="8d508-108">[Rapport synthèse qualité multimédia dans Lync Server 2013](lync-server-2013-media-quality-summary-report.md)   Fournit des données de qualité globales pour différents types de points de terminaison, notamment les appels d’égal à égal voix d’entreprise, les appels de conférences vocaux d’entreprise et les appels reposant, au moins en partie, sur le réseau téléphonique public commuté (RTC).</span><span class="sxs-lookup"><span data-stu-id="8d508-108">[Media Quality Summary Report in Lync Server 2013](lync-server-2013-media-quality-summary-report.md)   Provides overall quality data for different endpoint types, including Enterprise Voice peer-to-peer calls, Enterprise Voice conference calls, and calls that rely, at least in part, on the public switched telephone network (PSTN).</span></span>

  - <span data-ttu-id="8d508-109">[Rapport de comparaison de qualité multimédia dans Lync Server 2013](lync-server-2013-media-quality-comparison-report.md)   Fournit une comparaison des valeurs de qualité d’appel pour différents types d’appels audio (par exemple, les appels passés via un réseau sans fil et les appels effectués sur une connexion câblée).</span><span class="sxs-lookup"><span data-stu-id="8d508-109">[Media Quality Comparison Report in Lync Server 2013](lync-server-2013-media-quality-comparison-report.md)   Provides a comparison of call quality values for different types of audio calls (for example, calls made over a wireless network vs. calls made across a wired connection).</span></span>

  - <span data-ttu-id="8d508-110">[Rapport sur les performances du serveur dans Lync Server 2013](lync-server-2013-server-performance-report.md)   Affiche la liste des serveurs ayant rencontré le plus de problèmes, en fonction des mesures de ces métriques de qualité clé en matière de dégradation, de perte de paquets et de gigue.</span><span class="sxs-lookup"><span data-stu-id="8d508-110">[Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md)   Lists the servers that have experienced the most problems, based on measurements of such key quality metrics as degradation, packet loss, and jitter.</span></span>

  - <span data-ttu-id="8d508-111">[Rapport d’emplacement dans Lync Server 2013](lync-server-2013-location-report.md)   Fournit une liste des emplacements réseau et un résumé de la qualité de média des appels qui se produisent à chaque emplacement.</span><span class="sxs-lookup"><span data-stu-id="8d508-111">[Location Report in Lync Server 2013](lync-server-2013-location-report.md)   Provides a list of network locations and a summary of the media quality of the calls that occur at each location.</span></span> <span data-ttu-id="8d508-112">En raison des objectifs de ce rapport, les emplacements sont basés sur les sous-réseaux IP.</span><span class="sxs-lookup"><span data-stu-id="8d508-112">For purposes of this report, locations are based on IP subnets.</span></span>

  - <span data-ttu-id="8d508-113">[Rapport sur les appareils dans Lync Server 2013](lync-server-2013-device-report.md)   Fournit un récapitulatif des appareils qui sont utilisés pour les appels voix entreprise et qui inclut la qualité média moyenne des appels par appareil.</span><span class="sxs-lookup"><span data-stu-id="8d508-113">[Device Report in Lync Server 2013](lync-server-2013-device-report.md)   Provides a summary of devices that are used for Enterprise Voice calls and it includes the average media quality of the calls by device.</span></span>

  - <span data-ttu-id="8d508-114">[Rapport de liste d’appels dans Lync Server 2013](lync-server-2013-call-list-report.md)   Fournit des informations détaillées sur les appels téléphoniques passés ou reçus au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8d508-114">[Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md)   Provides detailed information about phone calls made or received within your organization.</span></span>

  - <span data-ttu-id="8d508-115">[Rapport Détails des appels dans Lync Server 2013](lync-server-2013-call-detail-report.md)   Fournit des informations détaillées sur les appels téléphoniques passés ou reçus au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8d508-115">[Call Detail Report in Lync Server 2013](lync-server-2013-call-detail-report.md)   Provides detailed information about phone calls made from or received within your organization.</span></span>

  - <span data-ttu-id="8d508-116">[Rapport de tendances de la qualité multimédia du serveur dans Lync Server 2013](lync-server-2013-server-media-quality-trend-report.md)   Permet de comparer graphiquement de 5 serveurs au niveau de la qualité d’appel, comme le volume des appels, le pourcentage d’appels médiocre, la perte de paquets et l’instabilité.</span><span class="sxs-lookup"><span data-stu-id="8d508-116">[Server Media Quality Trend Report in Lync Server 2013](lync-server-2013-server-media-quality-trend-report.md)   Provides a way for you to graphically compare up to 5 servers on Quality of Experience metrics such as call volume, poor call percentage, packet loss, and jitter.</span></span>

  - <span data-ttu-id="8d508-117">[Rapport de distribution des métriques de qualité multimédia dans Lync Server 2013](lync-server-2013-media-quality-metrics-distribution-report.md)   Fournit un graphique montrant les valeurs de distribution pour une métrique de qualité d’acquisition, comme le scintillement ou la perte de paquets.</span><span class="sxs-lookup"><span data-stu-id="8d508-117">[The Media Quality Metrics Distribution Report in Lync Server 2013](lync-server-2013-media-quality-metrics-distribution-report.md)   Provides a graph that shows the distribution values for a Quality of Experience metric such as jitter or packet loss.</span></span>

  - <span data-ttu-id="8d508-118">[Rapport de tendance d’emplacement dans Lync Server 2013](lync-server-2013-location-trend-report.md)   Fournit des informations de tendance de qualité d’appel pour les emplacements réseau.</span><span class="sxs-lookup"><span data-stu-id="8d508-118">[Location Trend Report in Lync Server 2013](lync-server-2013-location-trend-report.md)   Provides call quality trend information for network locations.</span></span>

<span data-ttu-id="8d508-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8d508-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

