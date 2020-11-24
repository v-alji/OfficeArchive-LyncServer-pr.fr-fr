---
title: 'Lync Server 2013 : rapports QoE'
description: 'Lync Server 2013 : rapports QoE.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: QoE reports
ms:assetid: 49c827af-b8dd-4c6e-b0dc-b4bc6d60e9a3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720913(v=OCS.15)
ms:contentKeyID: 63969601
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 55965d246b7f0ddd71eaeeec99d218eaf8819c2e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394525"
---
# <a name="qoe-reports-in-lync-server-2013"></a><span data-ttu-id="64620-103">Rapports QoE dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64620-103">QoE reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="64620-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="64620-104">

<span> </span></span></span>

<span data-ttu-id="64620-105">_**Dernière modification de la rubrique :** 2014-05-01_</span><span class="sxs-lookup"><span data-stu-id="64620-105">_**Topic Last Modified:** 2014-05-01_</span></span>

<div>

## <a name="qoe-summarytrend-reports"></a><span data-ttu-id="64620-106">Rapport de synthèse</span><span class="sxs-lookup"><span data-stu-id="64620-106">QoE summary/trend reports</span></span>

<span data-ttu-id="64620-107">Les rapports de synthèse/tendances QoE permettent de rechercher les heures d’utilisation du PIC et d’examiner la qualité du média pendant ces périodes pour vous assurer que les ressources réseau de votre organisation sont suffisantes.</span><span class="sxs-lookup"><span data-stu-id="64620-107">The QoE summary/trends reports are useful for finding the peak usage times of day and examining the media quality during those times to help assure that your organization's network resources are sufficient.</span></span> <span data-ttu-id="64620-108">Votre organisation peut également utiliser les nombreux filtres disponibles dans le rapport pour isoler les numéros de performance de certains emplacements, types de clients et de périphériques, et de serveurs.</span><span class="sxs-lookup"><span data-stu-id="64620-108">Your organization can also use the many filters available in the report to isolate performance numbers for certain locations, client and device types, and servers.</span></span>

<span data-ttu-id="64620-109">Les rapports de synthèse/tendance sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="64620-109">QoE summary/trend reports consist of:</span></span>

  - <span data-ttu-id="64620-110">Rapport synthèse sur les communications UNIFIÉes/rapport de tendance</span><span class="sxs-lookup"><span data-stu-id="64620-110">UC-to-UC Summary/Trend Report</span></span>

  - <span data-ttu-id="64620-111">Rapport de synthèse PSTN/tendance</span><span class="sxs-lookup"><span data-stu-id="64620-111">PSTN Summary/Trend Report</span></span>

  - <span data-ttu-id="64620-112">Rapport de synthèse de conférence/tendance</span><span class="sxs-lookup"><span data-stu-id="64620-112">Conference Summary/Trend Report</span></span>

</div>

<div>

## <a name="qoe-performance-reports"></a><span data-ttu-id="64620-113">Rapports sur les performances QoE</span><span class="sxs-lookup"><span data-stu-id="64620-113">QoE performance reports</span></span>

<span data-ttu-id="64620-114">Rapports sur les performances de QoE fournissent des détails sur les trois rapports qui se concentrent sur les performances QoE des serveurs de médiation, des serveurs de conférence A/V et des emplacements de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="64620-114">QoE performance reports provide details about the three reports that concentrate on the QoE performance of Mediation Servers, A/V Conferencing Servers, and endpoint locations.</span></span>

</div>

<div>

## <a name="mediation-server-performance-report"></a><span data-ttu-id="64620-115">Rapport de performances du serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="64620-115">Mediation server performance report</span></span>

<span data-ttu-id="64620-116">Le rapport sur les performances du serveur de médiation recense les métriques accomplies par une ou plusieurs médiation pendant la période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="64620-116">The Mediation Server Performance report lists the metrics achieved by one or more Mediation during the specified time period.</span></span> <span data-ttu-id="64620-117">Les métriques pour la jambe Unified Communications (UC) à médiation Server leg et la direction serveur à passerelle de médiation de chaque appel sont communiquées séparément.</span><span class="sxs-lookup"><span data-stu-id="64620-117">The metrics for the unified communications (UC)-to-Mediation Server leg and the Mediation Server-to-Gateway leg of each call are reported separately.</span></span> <span data-ttu-id="64620-118">Utilisez ce rapport pour comparer le volume et les performances des divers serveurs de médiation de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="64620-118">Use this report to compare the volume and performance of your organization's various Mediation Servers.</span></span>

<span data-ttu-id="64620-119">Pour chaque serveur de médiation (et pour chaque tronçon d’appel), le rapport affiche les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="64620-119">For each Mediation Server (and for each call leg), the report displays the following:</span></span>

  - <span data-ttu-id="64620-120">Nombre d'appels</span><span class="sxs-lookup"><span data-stu-id="64620-120">Number of calls</span></span>

  - <span data-ttu-id="64620-121">Perte de paquets</span><span class="sxs-lookup"><span data-stu-id="64620-121">Packet Loss</span></span>

  - <span data-ttu-id="64620-122">Durée de l’aller-retour</span><span class="sxs-lookup"><span data-stu-id="64620-122">Round Trip Time</span></span>

  - <span data-ttu-id="64620-123">Jitter</span><span class="sxs-lookup"><span data-stu-id="64620-123">Jitter</span></span>

  - <span data-ttu-id="64620-124">Note moyenne d’opinion de conversation (MOS)</span><span class="sxs-lookup"><span data-stu-id="64620-124">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="64620-125">Envoi d’un MOS</span><span class="sxs-lookup"><span data-stu-id="64620-125">Sending MOS</span></span>

  - <span data-ttu-id="64620-126">Ecouter le MOS</span><span class="sxs-lookup"><span data-stu-id="64620-126">Listening MOS</span></span>

  - <span data-ttu-id="64620-127">MOS du réseau</span><span class="sxs-lookup"><span data-stu-id="64620-127">Network MOS</span></span>

  - <span data-ttu-id="64620-128">Baisse de la dégradation du réseau</span><span class="sxs-lookup"><span data-stu-id="64620-128">Network MOS Degradation</span></span>

  - <span data-ttu-id="64620-129">Retour d’écho</span><span class="sxs-lookup"><span data-stu-id="64620-129">Echo Return</span></span>

  - <span data-ttu-id="64620-130">Niveau du signal</span><span class="sxs-lookup"><span data-stu-id="64620-130">Signal Level</span></span>

</div>

<div>

## <a name="av-conferencing-server-performance-report"></a><span data-ttu-id="64620-131">Rapport de performances du serveur de conférence A/V</span><span class="sxs-lookup"><span data-stu-id="64620-131">A/V conferencing server performance report</span></span>

<span data-ttu-id="64620-132">Le rapport sur les performances du serveur de conférence A/V fournit des listes de mesures obtenues par un ou plusieurs serveurs de conférence A/V pendant la période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="64620-132">The A/V Conferencing Server Performance report provides lists of metrics achieved by one or more A/V Conferencing Servers during the specified time period.</span></span> <span data-ttu-id="64620-133">Ce rapport peut être utilisé pour comparer le volume et les performances des différents serveurs de conférence A/V de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="64620-133">This report can be used to compare the volume and performance of your organization’s various A/V Conferencing Servers.</span></span> <span data-ttu-id="64620-134">Votre organisation peut également isoler le rapport pour afficher uniquement l’interface utilisateur de types de clients spécifiques, tels que les clients Lync ou les clients PSTN.</span><span class="sxs-lookup"><span data-stu-id="64620-134">Your organization can also isolate the report to show only the experience for specific client types, such as Lync clients or PSTN clients.</span></span>

<span data-ttu-id="64620-135">Pour chaque serveur de conférence A/V, le rapport affiche les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="64620-135">For each A/V Conferencing Server, the report displays the following:</span></span>

  - <span data-ttu-id="64620-136">Nombre de conférences</span><span class="sxs-lookup"><span data-stu-id="64620-136">Number of conferences</span></span>

  - <span data-ttu-id="64620-137">Perte de paquets</span><span class="sxs-lookup"><span data-stu-id="64620-137">Packet Loss</span></span>

  - <span data-ttu-id="64620-138">Durée de l’aller-retour</span><span class="sxs-lookup"><span data-stu-id="64620-138">Round Trip Time</span></span>

  - <span data-ttu-id="64620-139">Jitter</span><span class="sxs-lookup"><span data-stu-id="64620-139">Jitter</span></span>

  - <span data-ttu-id="64620-140">Note moyenne d’opinion de conversation (MOS)</span><span class="sxs-lookup"><span data-stu-id="64620-140">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="64620-141">Envoi d’un MOS</span><span class="sxs-lookup"><span data-stu-id="64620-141">Sending MOS</span></span>

  - <span data-ttu-id="64620-142">Ecouter le MOS</span><span class="sxs-lookup"><span data-stu-id="64620-142">Listening MOS</span></span>

  - <span data-ttu-id="64620-143">MOS du réseau</span><span class="sxs-lookup"><span data-stu-id="64620-143">Network MOS</span></span>

  - <span data-ttu-id="64620-144">Baisse de la dégradation du réseau</span><span class="sxs-lookup"><span data-stu-id="64620-144">Network MOS Degradation</span></span>

  - <span data-ttu-id="64620-145">Retour d’écho</span><span class="sxs-lookup"><span data-stu-id="64620-145">Echo Return</span></span>

  - <span data-ttu-id="64620-146">Niveau du signal</span><span class="sxs-lookup"><span data-stu-id="64620-146">Signal Level</span></span>

</div>

<div>

## <a name="location-based-performance-report"></a><span data-ttu-id="64620-147">Rapport sur les performances de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="64620-147">Location-based performance report</span></span>

<span data-ttu-id="64620-148">Le rapport sur les performances de Location-Based fournit une liste d’emplacements réseau et chaque emplacement indique le nombre d’appels dans chaque gamme de qualité prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="64620-148">The Location-Based Performance report provides a list of network locations and for each location shows the number of calls in each pre-determined range of quality.</span></span> <span data-ttu-id="64620-149">L’objectif de ce rapport est d’offrir une vue d’ensemble de la qualité de médias des appels téléphoniques de votre organisation pour différents emplacements, afin que vous puissiez identifier les emplacements médiocres et voir les différentes notes de qualité multimédia dans les différents emplacements de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="64620-149">The goal of this report is to provide insight into the media quality of the bulk of your organization’s telephone calls for various locations so that you can identify poorly performing locations, and see the different grades of media quality in your organization’s different locations.</span></span>

<span data-ttu-id="64620-150">Lors de l’affichage du rapport, différentes tables de métriques apparaissent : une table pour chaque métrique que votre organisation décide de signaler.</span><span class="sxs-lookup"><span data-stu-id="64620-150">When displaying the report, different tables of metrics appear—one table for each metric your organization decides to report on.</span></span> <span data-ttu-id="64620-151">Pour ce rapport, vous pouvez choisir parmi les mesures suivantes :</span><span class="sxs-lookup"><span data-stu-id="64620-151">You can choose from the following metrics for this report:</span></span>

  - <span data-ttu-id="64620-152">Note moyenne d’opinion de conversation (MOS)</span><span class="sxs-lookup"><span data-stu-id="64620-152">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="64620-153">MOS du réseau</span><span class="sxs-lookup"><span data-stu-id="64620-153">Network MOS</span></span>

  - <span data-ttu-id="64620-154">Baisse de la dégradation du réseau</span><span class="sxs-lookup"><span data-stu-id="64620-154">Network MOS Degradation</span></span>

  - <span data-ttu-id="64620-155">Envoi d’un MOS</span><span class="sxs-lookup"><span data-stu-id="64620-155">Sending MOS</span></span>

  - <span data-ttu-id="64620-156">Ecouter le MOS</span><span class="sxs-lookup"><span data-stu-id="64620-156">Listening MOS</span></span>

  - <span data-ttu-id="64620-157">Perte de paquets</span><span class="sxs-lookup"><span data-stu-id="64620-157">Packet Loss</span></span>

  - <span data-ttu-id="64620-158">Jitter</span><span class="sxs-lookup"><span data-stu-id="64620-158">Jitter</span></span>

  - <span data-ttu-id="64620-159">Latence</span><span class="sxs-lookup"><span data-stu-id="64620-159">Latency</span></span>

<span data-ttu-id="64620-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="64620-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

