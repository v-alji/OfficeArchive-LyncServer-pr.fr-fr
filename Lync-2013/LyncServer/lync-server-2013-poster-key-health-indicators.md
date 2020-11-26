---
title: 'Lync Server 2013 : affiche : indicateurs d’intégrité clés'
description: 'Lync Server 2013 : affiche : indicateurs d’intégrité clés.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Poster: Key Health Indicators'
ms:assetid: 8367dccf-adaa-4a0b-a4ed-bc9570cc5e24
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn593599(v=OCS.15)
ms:contentKeyID: 61084873
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9962d1764d5d2c664bb8415261344d9b48c81149
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424234"
---
# <a name="key-health-indicators-in-lync-server-2013"></a><span data-ttu-id="ba86d-103">Principaux indicateurs d’intégrité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba86d-103">Key Health Indicators in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ba86d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ba86d-104">

<span> </span></span></span>

<span data-ttu-id="ba86d-105">_**Dernière modification de la rubrique :** 2014-02-10_</span><span class="sxs-lookup"><span data-stu-id="ba86d-105">_**Topic Last Modified:** 2014-02-10_</span></span>

<span data-ttu-id="ba86d-106">Cet article est un complément des [indicateurs d’intégrité clés : la base de la mise à jour des afficheurs Lync Servers sains](https://go.microsoft.com/fwlink/?linkid=391838) que vous pouvez télécharger à partir du centre de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="ba86d-106">This article is a companion to the [Key Health Indicators: The Foundation for Maintaining Healthy Lync Servers](https://go.microsoft.com/fwlink/?linkid=391838) poster, which you can download from the Download Center.</span></span>

<span data-ttu-id="ba86d-107">![Affiche décrivant le dépannage à l’aide de données KHI](images/Dn594589.b6fe82bd-d70f-4c1f-a812-b615ac5fa7d7(OCS.15).jpg "Affiche décrivant le dépannage à l’aide de données KHI")</span><span class="sxs-lookup"><span data-stu-id="ba86d-107">![Poster describing troubleshooting using KHI data](images/Dn594589.b6fe82bd-d70f-4c1f-a812-b615ac5fa7d7(OCS.15).jpg "Poster describing troubleshooting using KHI data")</span></span>

<span data-ttu-id="ba86d-108">Vous pouvez utiliser cette affiche pour en savoir plus sur les indicateurs de performance clés (KHIs), les compteurs de performance avec des seuils visant à révéler des problèmes d’utilisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ba86d-108">You can use this poster to learn about Key Health Indicators (KHIs), performance counters with thresholds aimed at revealing user experience issues.</span></span> <span data-ttu-id="ba86d-109">La collecte des données KHI est généralement la première étape de l’implémentation de la méthodologie de qualité des appels (CQM), qui vise à garantir une qualité audio optimale pour les utilisateurs de Lync.</span><span class="sxs-lookup"><span data-stu-id="ba86d-109">Gathering KHI data is usually the first step to implementing the Call Quality Methodology (CQM), which is focused on ensuring a quality audio experience for Lync users.</span></span>

<span data-ttu-id="ba86d-110">Si vous avez des questions sur l’utilisation de CQM, vous pouvez transmettre vos questions à cqmfeedback@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="ba86d-110">If you have questions about how to use CQM, you can submit your questions to cqmfeedback@microsoft.com.</span></span>

<span data-ttu-id="ba86d-111">L’affiche décrit les domaines suivants :</span><span class="sxs-lookup"><span data-stu-id="ba86d-111">The poster explains the following areas:</span></span>

  - <span data-ttu-id="ba86d-112">Que sont les indicateurs d’intégrité clés ?</span><span class="sxs-lookup"><span data-stu-id="ba86d-112">What are Key Health Indicators?</span></span>

  - <span data-ttu-id="ba86d-113">Pour collecter des données KHI</span><span class="sxs-lookup"><span data-stu-id="ba86d-113">To Collect KHI Data</span></span>

  - <span data-ttu-id="ba86d-114">Flux de correction pour tous les rôles de serveur</span><span class="sxs-lookup"><span data-stu-id="ba86d-114">Remediation Flow for all Server Roles</span></span>

  - <span data-ttu-id="ba86d-115">Glossaire</span><span class="sxs-lookup"><span data-stu-id="ba86d-115">Glossary</span></span>

  - <span data-ttu-id="ba86d-116">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="ba86d-116">Front-end Servers</span></span>

  - <span data-ttu-id="ba86d-117">Serveur SQL principal</span><span class="sxs-lookup"><span data-stu-id="ba86d-117">Backend SQL Servers</span></span>

  - <span data-ttu-id="ba86d-118">serveurs de médiation</span><span class="sxs-lookup"><span data-stu-id="ba86d-118">Mediation Servers</span></span>

  - <span data-ttu-id="ba86d-119">serveurs Edge</span><span class="sxs-lookup"><span data-stu-id="ba86d-119">Edge Servers</span></span>

<span id="WhatIs"></span>

<div>

## <a name="what-are-key-health-indicators"></a><span data-ttu-id="ba86d-120">Que sont les indicateurs d’intégrité clés ?</span><span class="sxs-lookup"><span data-stu-id="ba86d-120">What are Key Health Indicators?</span></span>

<span data-ttu-id="ba86d-121">Les indicateurs de performance clés sont des compteurs de performance avec des seuils visant à révéler des problèmes d’utilisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ba86d-121">Key Health Indicators are performance counters with thresholds aimed at revealing user experience issues.</span></span> <span data-ttu-id="ba86d-122">La collecte des données KHI est généralement la première étape de l’implémentation de la méthodologie de qualité des appels (CQM), qui vise à garantir une qualité audio optimale pour les utilisateurs de Lync.</span><span class="sxs-lookup"><span data-stu-id="ba86d-122">Gathering KHI data is usually the first step to implementing the Call Quality Methodology (CQM), which is focused on ensuring a quality audio experience for Lync users.</span></span>

<span data-ttu-id="ba86d-123">Les KHIs sont utilisés en plus des solutions de surveillance Lync standard (par exemple, System Center Operations Manager, transactions synthétiques, serveur de surveillance) et non au lieu de ces solutions.</span><span class="sxs-lookup"><span data-stu-id="ba86d-123">KHIs are used in addition to standard Lync Monitoring Solutions (e.g. System Center Operations Manager, Synthetic Transactions, Monitoring Server) and not instead of those solutions.</span></span>

<span data-ttu-id="ba86d-124">Recueillez les compteurs de performance KHI et remplissez la feuille de calcul KHI qui accompagne le Guide réseau pour créer une carte de performance qui vous aidera à déterminer l’état du serveur d’un déploiement Lync.</span><span class="sxs-lookup"><span data-stu-id="ba86d-124">Collect the KHI performance counters and populate the KHI spreadsheet accompanying the Networking Guide to produce a scorecard that will help you determine the server health of a Lync deployment.</span></span> <span data-ttu-id="ba86d-125">Une fois rempli, il vous guide dans la réparation de l’environnement et fournit des renseignements supplémentaires aux autres parties prenantes.</span><span class="sxs-lookup"><span data-stu-id="ba86d-125">Once populated, it guides you in repairing the environment and gives additional insight to other stakeholders.</span></span> <span data-ttu-id="ba86d-126">Évaluez KHIs sur une base mensuelle et intégrez-le dans les processus opérationnels en cours de déploiement.</span><span class="sxs-lookup"><span data-stu-id="ba86d-126">Evaluate KHIs on a monthly basis and incorporate them into any deployment’s ongoing operational processes.</span></span>

<span data-ttu-id="ba86d-127">Téléchargez le [Guide du réseau Lync Server](https://go.microsoft.com/fwlink/p/?linkid=390677) pour afficher la liste complète des KHIs et obtenir les feuilles de calcul associées.</span><span class="sxs-lookup"><span data-stu-id="ba86d-127">Download the [Lync Server Networking Guide](https://go.microsoft.com/fwlink/p/?linkid=390677) to see the full list of KHIs and to get the related spreadsheets.</span></span>

</div>

<span id="ToCollect"></span>

<div>

## <a name="to-collect-khi-data"></a><span data-ttu-id="ba86d-128">Pour collecter des données KHI</span><span class="sxs-lookup"><span data-stu-id="ba86d-128">To Collect KHI Data</span></span>

1.  <span data-ttu-id="ba86d-129">Exécutez le script KHI inclus dans le Guide du réseau Lync Server sur chaque serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="ba86d-129">Run the KHI script included with the Lync Server Networking Guide on each Lync Server.</span></span> <span data-ttu-id="ba86d-130">Cela permet de créer un collecteur de données dans le moniteur de performance et de le nommer KHI.</span><span class="sxs-lookup"><span data-stu-id="ba86d-130">This will create a Data Collector inside of Performance Monitor and name it KHI.</span></span> <span data-ttu-id="ba86d-131">Par défaut, les données sont interrogées toutes les 15 secondes.</span><span class="sxs-lookup"><span data-stu-id="ba86d-131">By default, data will be polled every 15 seconds.</span></span>

2.  <span data-ttu-id="ba86d-132">Avant le début de la journée de votre entreprise, accédez à chaque serveur Lync et démarrez le collecteur de données KHI.</span><span class="sxs-lookup"><span data-stu-id="ba86d-132">Before the start of your company's business day, go to each Lync Server and start the KHI Data Collector.</span></span>

3.  <span data-ttu-id="ba86d-133">À la fin de cette journée, arrêtez le collecteur de données KHI et copiez les données dans un emplacement central.</span><span class="sxs-lookup"><span data-stu-id="ba86d-133">At the end of that day, stop the KHI Data Collector and copy the data to a central location.</span></span>

4.  <span data-ttu-id="ba86d-134">Après avoir utilisé le moniteur de performance pour remplir la feuille de calcul KHI incluse dans le téléchargement du Guide du réseau Lync Server, comparez les résultats aux cibles recommandées.</span><span class="sxs-lookup"><span data-stu-id="ba86d-134">After using Performance Monitor to fill in the KHI spreadsheet included with the Lync Server Networking Guide download, compare the results to the recommended targets.</span></span>

</div>

<span id="Remidiation"></span>

<div>

## <a name="remediation-flow-for-all-server-roles"></a><span data-ttu-id="ba86d-135">Flux de correction pour tous les rôles de serveur</span><span class="sxs-lookup"><span data-stu-id="ba86d-135">Remediation Flow for all Server Roles</span></span>

<span data-ttu-id="ba86d-136">Pour chaque serveur dans votre implémentation Lync, commencez par vérifier que les performances du composant et celles du serveur du serveur sont au niveau le plus souhaité.</span><span class="sxs-lookup"><span data-stu-id="ba86d-136">For each server in your Lync implementation, begin by verifying that the server’s component health and system performance is at or above the desired level.</span></span> <span data-ttu-id="ba86d-137">Après cela, vous devez examiner les indicateurs relatifs au rôle du serveur dans l’implémentation globale de Lync.</span><span class="sxs-lookup"><span data-stu-id="ba86d-137">Only after that should you look at the indicators relating to the server’s role in the overall Lync implementation.</span></span>

<span data-ttu-id="ba86d-138">Commencez par collecter les données de performances KHI pour tous les serveurs.</span><span class="sxs-lookup"><span data-stu-id="ba86d-138">Begin by collecting KHI Performance Data for all servers.</span></span> <span data-ttu-id="ba86d-139">Pour chacun des rôles système (détails abordés plus loin dans ce document), déterminez si les composants système de base répondent aux cibles recommandées.</span><span class="sxs-lookup"><span data-stu-id="ba86d-139">For each of the system roles (details discussed later in this document) determine whether the basic system components meet the recommended targets.</span></span> <span data-ttu-id="ba86d-140">Si ce n’est pas le cas, assurez-vous d’apporter une correction aux performances du système, puis recollectez les données KHI et assurez-vous que l’état du système s’applique aux mesures spécifiques au rôle du serveur dans l’implémentation Lync.</span><span class="sxs-lookup"><span data-stu-id="ba86d-140">If they do not, remediate the system performance then re-collect KHI data and ensure system health before looking at the metrics specific to the server’s role in the Lync implementation.</span></span> <span data-ttu-id="ba86d-141">L’intégrité des composants de tous les rôles est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="ba86d-141">Component health for all roles is defined as:</span></span>

  - <span data-ttu-id="ba86d-142">Taux d’utilisation UC \< 80%</span><span class="sxs-lookup"><span data-stu-id="ba86d-142">CPU Utilization \< 80%</span></span>

  - <span data-ttu-id="ba86d-143">Moyenne. écriture de \< 10 ms</span><span class="sxs-lookup"><span data-stu-id="ba86d-143">Avg. Disk Write \< 10 ms</span></span>

  - <span data-ttu-id="ba86d-144">Moyenne. Disk lu \< 10 ms</span><span class="sxs-lookup"><span data-stu-id="ba86d-144">Avg. Disk Read \< 10 ms</span></span>

  - <span data-ttu-id="ba86d-145">Mémoire disponible de \> 20% au total Mo</span><span class="sxs-lookup"><span data-stu-id="ba86d-145">Available memory \>20% System Total MB</span></span>

  - <span data-ttu-id="ba86d-146">Longueur de la file d’attente réseau \< 2</span><span class="sxs-lookup"><span data-stu-id="ba86d-146">Network Queue Length \< 2</span></span>

  - <span data-ttu-id="ba86d-147">Paquets ignorés (en entrée/sortie) = 0</span><span class="sxs-lookup"><span data-stu-id="ba86d-147">Discarded Packets (in / out) = 0</span></span>

</div>

<span id="Glossary"></span>

<div>

## <a name="glossary"></a><span data-ttu-id="ba86d-148">Glossaire</span><span class="sxs-lookup"><span data-stu-id="ba86d-148">Glossary</span></span>

<span data-ttu-id="ba86d-149">Les termes et sigles suivants sont utilisés dans cet affiche :</span><span class="sxs-lookup"><span data-stu-id="ba86d-149">The following terms and acronyms are used in this poster:</span></span>

<span data-ttu-id="ba86d-150">AS MCU = unité de contrôle de partage d’application multipoint</span><span class="sxs-lookup"><span data-stu-id="ba86d-150">AS MCU = Application Sharing Multi-point Control Unit</span></span>

<span data-ttu-id="ba86d-151">AV MCU = audio/vidéo MCU</span><span class="sxs-lookup"><span data-stu-id="ba86d-151">AV MCU = Audio/Video MCU</span></span>

<span data-ttu-id="ba86d-152">Messagerie instantanée MCU = MCU</span><span class="sxs-lookup"><span data-stu-id="ba86d-152">IM MCU = Instant Messaging MCU</span></span>

<span data-ttu-id="ba86d-153">UCWA = API Web de communications unifiées</span><span class="sxs-lookup"><span data-stu-id="ba86d-153">UCWA = Unified Communications Web API</span></span>

<span data-ttu-id="ba86d-154">Clavier AV = traversée de l’audio/vidéo via Edge</span><span class="sxs-lookup"><span data-stu-id="ba86d-154">AV Edge = Traversal of audio/video via edge</span></span>

<span data-ttu-id="ba86d-155">Authentification AV = authentification audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="ba86d-155">AV Auth = Audio/Video Authentication</span></span>

<span data-ttu-id="ba86d-156">Pile SIP = application de base SIP de Lync</span><span class="sxs-lookup"><span data-stu-id="ba86d-156">SIP Stack = Contains Lync’s core SIP implementation</span></span>

<span data-ttu-id="ba86d-157">Proxy de données = utilisé pour les conférences de périphériques</span><span class="sxs-lookup"><span data-stu-id="ba86d-157">Data Proxy = Used for edge conferencing</span></span>

<span data-ttu-id="ba86d-158">LySS = service de stockage Lync</span><span class="sxs-lookup"><span data-stu-id="ba86d-158">LySS = Lync Storage Service</span></span>

</div>

<span id="Front"></span>

<div>

## <a name="front-end-servers"></a><span data-ttu-id="ba86d-159">Serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="ba86d-159">Front-end Servers</span></span>

<span data-ttu-id="ba86d-160">Les cibles KHI suivantes sont spécifiques aux serveurs frontaux en plus de l’état d’intégrité des composants de base :</span><span class="sxs-lookup"><span data-stu-id="ba86d-160">The following recommended KHI targets are specific to front-end servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ba86d-161">Zone fonctionnelle</span><span class="sxs-lookup"><span data-stu-id="ba86d-161">Functional area</span></span></th>
<th><span data-ttu-id="ba86d-162">Mesures cibles</span><span class="sxs-lookup"><span data-stu-id="ba86d-162">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba86d-163">AS/AV/IM MCU</span><span class="sxs-lookup"><span data-stu-id="ba86d-163">AS/AV/IM MCU</span></span></p></td>
<td><p><span data-ttu-id="ba86d-164">État d’intégrité du MCU &lt; 2</span><span class="sxs-lookup"><span data-stu-id="ba86d-164">MCU Health State &lt;2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba86d-165">Composants Web</span><span class="sxs-lookup"><span data-stu-id="ba86d-165">Web Components</span></span></p></td>
<td><p><span data-ttu-id="ba86d-166">Temporisation de l’extension de liste de distribution &lt; 0</span><span class="sxs-lookup"><span data-stu-id="ba86d-166">Distribution List expansion AD timeouts &lt;0</span></span></p>
<p><span data-ttu-id="ba86d-167">Échecs de ABWQ = 0</span><span class="sxs-lookup"><span data-stu-id="ba86d-167">ABWQ failures = 0</span></span></p>
<p><span data-ttu-id="ba86d-168">Échecs de LIS = 0</span><span class="sxs-lookup"><span data-stu-id="ba86d-168">LIS failures = 0</span></span></p>
<p><span data-ttu-id="ba86d-169">Erreurs d’authentification &lt; 1/s</span><span class="sxs-lookup"><span data-stu-id="ba86d-169">Authentication Errors &lt; 1/sec</span></span></p>
<p><span data-ttu-id="ba86d-170">Demandes d’ASP.NET V4 rejetées = 0</span><span class="sxs-lookup"><span data-stu-id="ba86d-170">ASP.NET v4 Requests Rejected = 0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba86d-171">Pile SIP</span><span class="sxs-lookup"><span data-stu-id="ba86d-171">SIP Stack</span></span></p></td>
<td><p><span data-ttu-id="ba86d-172">Moyenne. traitement de messages entrants &lt; 1 s</span><span class="sxs-lookup"><span data-stu-id="ba86d-172">Avg. Incoming Message Processing &lt; 1 sec</span></span></p>
<p><span data-ttu-id="ba86d-173">Les &lt; réponses entrantes ont été supprimées. &lt;</span><span class="sxs-lookup"><span data-stu-id="ba86d-173">Incoming Responses Dropped &lt; 1/sec Incoming Requests Dropped &lt; 1/sec</span></span></p>
<p><span data-ttu-id="ba86d-174">Latence de la file d’attente &lt; 100 ms</span><span class="sxs-lookup"><span data-stu-id="ba86d-174">Queue Latency &lt; 100 ms</span></span></p>
<p><span data-ttu-id="ba86d-175">Latence de sproc &lt; 100 ms</span><span class="sxs-lookup"><span data-stu-id="ba86d-175">Sproc Latency &lt; 100 ms</span></span></p>
<p><span data-ttu-id="ba86d-176">Demandes de limitation = 0</span><span class="sxs-lookup"><span data-stu-id="ba86d-176">Throttled Requests = 0</span></span></p>
<p><span data-ttu-id="ba86d-177">Erreurs d’authentification &lt; 1/s</span><span class="sxs-lookup"><span data-stu-id="ba86d-177">Authentication Errors &lt; 1/sec</span></span></p>
<p><span data-ttu-id="ba86d-178">Messages entrants expirés &lt; 2</span><span class="sxs-lookup"><span data-stu-id="ba86d-178">Incoming Messages Timed Out &lt; 2</span></span></p>
<p><span data-ttu-id="ba86d-179">Moyenne de messages entrants : &lt; 1 seconde</span><span class="sxs-lookup"><span data-stu-id="ba86d-179">Avg. Incoming Message Hold &lt; 1 sec</span></span></p>
<p><span data-ttu-id="ba86d-180">Connexions à contrôle de flux &lt; 2</span><span class="sxs-lookup"><span data-stu-id="ba86d-180">Flow Controlled Connections &lt; 2</span></span></p>
<p><span data-ttu-id="ba86d-181">Moyenne. décalage de la file d’attente &lt; 2 s</span><span class="sxs-lookup"><span data-stu-id="ba86d-181">Avg. Out Queue Delay &lt; 2 sec</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba86d-182">LySS</span><span class="sxs-lookup"><span data-stu-id="ba86d-182">LySS</span></span></p></td>
<td><p><span data-ttu-id="ba86d-183">% d’espace utilisé par la base de services de stockage &lt; 80</span><span class="sxs-lookup"><span data-stu-id="ba86d-183">% of space used by Storage Service DB &lt; 80</span></span></p>
<p><span data-ttu-id="ba86d-184"># échecs de réplication de réplica = 0</span><span class="sxs-lookup"><span data-stu-id="ba86d-184"># of replica replication failures = 0</span></span></p>
<p><span data-ttu-id="ba86d-185"># des événements de perte de données = 0</span><span class="sxs-lookup"><span data-stu-id="ba86d-185"># of data loss events = 0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba86d-186">SQL</span><span class="sxs-lookup"><span data-stu-id="ba86d-186">SQL</span></span></p></td>
<td><p><span data-ttu-id="ba86d-187">Durée de vie de la page &gt; 300 s.</span><span class="sxs-lookup"><span data-stu-id="ba86d-187">Page life expectancy &gt; 300 Sec.</span></span></p>
<p><span data-ttu-id="ba86d-188">Demandes de lot/s &lt; 2500</span><span class="sxs-lookup"><span data-stu-id="ba86d-188">Batch requests / sec &lt; 2500</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="BackEnd"></span>

<div>

## <a name="backend-sql-servers"></a><span data-ttu-id="ba86d-189">Serveur SQL principal</span><span class="sxs-lookup"><span data-stu-id="ba86d-189">Backend SQL Servers</span></span>

<span data-ttu-id="ba86d-190">Les cibles KHI suivantes sont spécifiques aux serveurs SQL Server en plus de l’intégrité des composants de base :</span><span class="sxs-lookup"><span data-stu-id="ba86d-190">The following recommended KHI targets are specific to SQL servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ba86d-191">Zone fonctionnelle</span><span class="sxs-lookup"><span data-stu-id="ba86d-191">Functional area</span></span></th>
<th><span data-ttu-id="ba86d-192">Mesures cibles</span><span class="sxs-lookup"><span data-stu-id="ba86d-192">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba86d-193">SQL</span><span class="sxs-lookup"><span data-stu-id="ba86d-193">SQL</span></span></p></td>
<td><p><span data-ttu-id="ba86d-194">Durée de vie de la page &gt; 300 s.</span><span class="sxs-lookup"><span data-stu-id="ba86d-194">Page life expectancy &gt; 300 Sec.</span></span></p>
<p><span data-ttu-id="ba86d-195">Demandes de lot/s &lt; 2500</span><span class="sxs-lookup"><span data-stu-id="ba86d-195">Batch requests / sec &lt; 2500</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="Mediation"></span>

<div>

## <a name="mediation-servers"></a><span data-ttu-id="ba86d-196">serveurs de médiation</span><span class="sxs-lookup"><span data-stu-id="ba86d-196">Mediation Servers</span></span>

<span data-ttu-id="ba86d-197">Les cibles KHI suivantes sont spécifiques aux serveurs de médiation en plus de l’intégrité des composants de base :</span><span class="sxs-lookup"><span data-stu-id="ba86d-197">The following recommended KHI targets are specific to mediation servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ba86d-198">Zone fonctionnelle</span><span class="sxs-lookup"><span data-stu-id="ba86d-198">Functional area</span></span></th>
<th><span data-ttu-id="ba86d-199">Mesures cibles</span><span class="sxs-lookup"><span data-stu-id="ba86d-199">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba86d-200">Service de médiation Server</span><span class="sxs-lookup"><span data-stu-id="ba86d-200">Mediation Server Service</span></span></p></td>
<td><p><span data-ttu-id="ba86d-201">Chargement de l’index d’échec de l’appel = 0</span><span class="sxs-lookup"><span data-stu-id="ba86d-201">Load Call Failure Index = 0</span></span></p>
<p><span data-ttu-id="ba86d-202">Appels en échec en raison de proxy &lt; 10</span><span class="sxs-lookup"><span data-stu-id="ba86d-202">Failed Calls due to Proxy &lt;10</span></span></p>
<p><span data-ttu-id="ba86d-203">Appels en échec en raison de la passerelle &lt; 10</span><span class="sxs-lookup"><span data-stu-id="ba86d-203">Failed Calls due to Gateway &lt;10</span></span></p>
<p><span data-ttu-id="ba86d-204">Appels (en sortie ou en sortie) rejetés = 0</span><span class="sxs-lookup"><span data-stu-id="ba86d-204">Calls (in or out) rejected = 0</span></span></p>
<p><span data-ttu-id="ba86d-205">Les candidats de médias ont manquant = 0</span><span class="sxs-lookup"><span data-stu-id="ba86d-205">Media Candidates missing = 0</span></span></p>
<p><span data-ttu-id="ba86d-206">Échecs de vérification de la connectivité média = 0</span><span class="sxs-lookup"><span data-stu-id="ba86d-206">Media Connectivity Check Failures = 0</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="Edge"></span>

<div>

## <a name="edge-servers"></a><span data-ttu-id="ba86d-207">serveurs Edge</span><span class="sxs-lookup"><span data-stu-id="ba86d-207">Edge Servers</span></span>

<span data-ttu-id="ba86d-208">Les cibles KHI suivantes sont spécifiques aux serveurs Edge, en plus de l’état d’intégrité des composants de base :</span><span class="sxs-lookup"><span data-stu-id="ba86d-208">The following recommended KHI targets are specific to edge servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ba86d-209">Zone fonctionnelle</span><span class="sxs-lookup"><span data-stu-id="ba86d-209">Functional area</span></span></th>
<th><span data-ttu-id="ba86d-210">Mesures cibles</span><span class="sxs-lookup"><span data-stu-id="ba86d-210">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba86d-211">Authentification AV</span><span class="sxs-lookup"><span data-stu-id="ba86d-211">AV Auth</span></span></p></td>
<td><p><span data-ttu-id="ba86d-212">Demandes incorrectes &lt; 20/s</span><span class="sxs-lookup"><span data-stu-id="ba86d-212">Bad Requests &lt; 20/sec</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba86d-213">Bordure AV</span><span class="sxs-lookup"><span data-stu-id="ba86d-213">AV Edge</span></span></p></td>
<td><p><span data-ttu-id="ba86d-214">Échecs d’authentification &lt; 20/s</span><span class="sxs-lookup"><span data-stu-id="ba86d-214">Auth. Failures &lt;20/sec</span></span></p>
<p><span data-ttu-id="ba86d-215">Échecs d’attribution &lt; 20/s</span><span class="sxs-lookup"><span data-stu-id="ba86d-215">Allocation Failures &lt;20/sec</span></span></p>
<p><span data-ttu-id="ba86d-216">Paquets déposés &lt; 300/s</span><span class="sxs-lookup"><span data-stu-id="ba86d-216">Packets Dropped &lt;300/sec</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba86d-217">Proxy de données</span><span class="sxs-lookup"><span data-stu-id="ba86d-217">Data Proxy</span></span></p></td>
<td><p><span data-ttu-id="ba86d-218">Connexions serveur limitées &lt; 3</span><span class="sxs-lookup"><span data-stu-id="ba86d-218">Throttled Server connections &lt; 3</span></span></p>
<p><span data-ttu-id="ba86d-219">Le système est en limitation &lt; 1</span><span class="sxs-lookup"><span data-stu-id="ba86d-219">System is Throttling &lt;1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba86d-220">Pile SIP</span><span class="sxs-lookup"><span data-stu-id="ba86d-220">SIP Stack</span></span></p></td>
<td><p><span data-ttu-id="ba86d-221">Connexions en dépassement de limite &lt;</span><span class="sxs-lookup"><span data-stu-id="ba86d-221">Connections over limit dropped &lt; 1</span></span></p>
<p><span data-ttu-id="ba86d-222">Le délai d’envoi est écoulé &lt; 10</span><span class="sxs-lookup"><span data-stu-id="ba86d-222">Sends timed out &lt;10</span></span></p>
<p><span data-ttu-id="ba86d-223">Connexion contrôlée par flux &lt; 100</span><span class="sxs-lookup"><span data-stu-id="ba86d-223">Flow Controlled Connections &lt;100</span></span></p>
<p><span data-ttu-id="ba86d-224">Demandes entrantes rejetées &lt; 1/s</span><span class="sxs-lookup"><span data-stu-id="ba86d-224">Incoming requests dropped &lt; 1/sec</span></span></p>
<p><span data-ttu-id="ba86d-225">Moyenne du traitement des messages &lt; 3 s</span><span class="sxs-lookup"><span data-stu-id="ba86d-225">Avg. Message Processing &lt; 3 sec</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ba86d-226">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba86d-226">See Also</span></span>


[<span data-ttu-id="ba86d-227">Guide du réseau Lync Server</span><span class="sxs-lookup"><span data-stu-id="ba86d-227">Lync Server Networking Guide</span></span>](https://go.microsoft.com/fwlink/p/?linkid=390677)  
[<span data-ttu-id="ba86d-228">Principaux indicateurs d’intégrité : notions de base pour la mise à jour des serveurs Lync sains</span><span class="sxs-lookup"><span data-stu-id="ba86d-228">Key Health Indicators: The Foundation for Maintaining Healthy Lync Servers</span></span>](https://go.microsoft.com/fwlink/?linkid=391838)  
[<span data-ttu-id="ba86d-229">Méthodologie de qualité d’appel Lync</span><span class="sxs-lookup"><span data-stu-id="ba86d-229">Lync Call Quality Methodology</span></span>](https://go.microsoft.com/fwlink/?linkid=391841)  
  

<span data-ttu-id="ba86d-230"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ba86d-230"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

