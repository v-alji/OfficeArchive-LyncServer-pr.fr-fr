---
title: 'Lync Server 2013 : compteurs de performances de mobilité'
description: 'Lync Server 2013 : compteurs de performance mobilité.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mobility performance counters
ms:assetid: d18ed85a-673d-4695-aa3f-ac83a38ab90a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690046(v=OCS.15)
ms:contentKeyID: 48185441
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 922288f6c026f088d651dc61afdcb6ba04fed30a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425555"
---
# <a name="mobility-performance-counters-in-lync-server-2013"></a><span data-ttu-id="faeae-103">Compteurs de performance de mobilité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="faeae-103">Mobility performance counters in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="faeae-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="faeae-104">

<span> </span></span></span>

<span data-ttu-id="faeae-105">_**Dernière modification de la rubrique :** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="faeae-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="faeae-106">Les tableaux suivants répertorient les noms et descriptions des compteurs de performance que vous pouvez utiliser pour surveiller les serveurs exécutant l’API Unified Communications Web API (UCWA) et le service de mobilité MCX de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="faeae-106">The following tables list the names and descriptions of performance counters that you can use to monitor servers running the Unified Communications Web API (UCWA) and the Lync Server 2013 Mcx Mobility Service.</span></span>

<span data-ttu-id="faeae-107">Le nom de la catégorie pour les compteurs dans le tableau UCWA est **LS:WEB – UCWA**.</span><span class="sxs-lookup"><span data-stu-id="faeae-107">The category name for the counters in the UCWA table is **LS:WEB – UCWA**.</span></span>

<span data-ttu-id="faeae-108">Le nom de la catégorie pour les compteurs dans le tableau Service de mobilité Mcx est **LS:WEB - Mobile Communication Service**.</span><span class="sxs-lookup"><span data-stu-id="faeae-108">The category name for the counters in the Mcx Mobility Service table is **LS:WEB - Mobile Communication Service**.</span></span>

<div>

## <a name="performance-counters-for-ucwa"></a><span data-ttu-id="faeae-109">Compteurs de performances pour UCWA</span><span class="sxs-lookup"><span data-stu-id="faeae-109">Performance Counters for UCWA</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="faeae-110">Compteur</span><span class="sxs-lookup"><span data-stu-id="faeae-110">Counter</span></span></th>
<th><span data-ttu-id="faeae-111">Description</span><span class="sxs-lookup"><span data-stu-id="faeae-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faeae-112">Active Application Count</span><span class="sxs-lookup"><span data-stu-id="faeae-112">Active Application Count</span></span></p></td>
<td><p><span data-ttu-id="faeae-113">Nombre d’applications en cours</span><span class="sxs-lookup"><span data-stu-id="faeae-113">The current number of applications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-114">Active Application Sharing Modality Count</span><span class="sxs-lookup"><span data-stu-id="faeae-114">Active Application Sharing Modality Count</span></span></p></td>
<td><p><span data-ttu-id="faeae-115">Nombre actuel de modalités de partage d’applications</span><span class="sxs-lookup"><span data-stu-id="faeae-115">The current number of Application Sharing modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-116">Active Audio Modality Count</span><span class="sxs-lookup"><span data-stu-id="faeae-116">Active Audio Modality Count</span></span></p></td>
<td><p><span data-ttu-id="faeae-117">Nombre actuel de modalités audio</span><span class="sxs-lookup"><span data-stu-id="faeae-117">The current number of Audio modality</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-118">Active Data Collaboration Modality Count</span><span class="sxs-lookup"><span data-stu-id="faeae-118">Active Data Collaboration Modality Count</span></span></p></td>
<td><p><span data-ttu-id="faeae-119">Nombre actuel de modalités de collaboration de données</span><span class="sxs-lookup"><span data-stu-id="faeae-119">The current number of Data Collaboration modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-120">Active Directory Photo Get Latency (ms)</span><span class="sxs-lookup"><span data-stu-id="faeae-120">Active Directory Photo Get Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="faeae-121">Ce compteur montre le temps moyen (en millisecondes) nécessaire pour récupérer une photo du répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="faeae-121">This counter shows the average time (in milliseconds) to retrieve a photo from active directory</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-122">Active Messaging Modality Count</span><span class="sxs-lookup"><span data-stu-id="faeae-122">Active Messaging Modality Count</span></span></p></td>
<td><p><span data-ttu-id="faeae-123">Nombre actuel de modalités de messagerie</span><span class="sxs-lookup"><span data-stu-id="faeae-123">The current number of Messaging modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-124">Active Panoramic Video Modality Count</span><span class="sxs-lookup"><span data-stu-id="faeae-124">Active Panoramic Video Modality Count</span></span></p></td>
<td><p><span data-ttu-id="faeae-125">Nombre actuel de modalités de vidéo panoramique</span><span class="sxs-lookup"><span data-stu-id="faeae-125">The current number of Panoramic Video modality</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-126">Active Pending Get Count</span><span class="sxs-lookup"><span data-stu-id="faeae-126">Active Pending Get Count</span></span></p></td>
<td><p><span data-ttu-id="faeae-127">Nombre de gets actifs en attente ; connexions au serveur conservées depuis longtemps</span><span class="sxs-lookup"><span data-stu-id="faeae-127">The number of currently active pending gets; long-held connections to the server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-128">Active Session Count</span><span class="sxs-lookup"><span data-stu-id="faeae-128">Active Session Count</span></span></p></td>
<td><p><span data-ttu-id="faeae-129">Nombre actuel de points de terminaison enregistrés dans UCWA par application et le total</span><span class="sxs-lookup"><span data-stu-id="faeae-129">The current number of endpoints registered in UCWA per application and total</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-130">Active User Instance Count</span><span class="sxs-lookup"><span data-stu-id="faeae-130">Active User Instance Count</span></span></p></td>
<td><p><span data-ttu-id="faeae-131">Nombre d’instances utilisateur en cours</span><span class="sxs-lookup"><span data-stu-id="faeae-131">The current number of user instances</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-132">Active User Instances without Application</span><span class="sxs-lookup"><span data-stu-id="faeae-132">Active User Instances without Application</span></span></p></td>
<td><p><span data-ttu-id="faeae-133">Nombre d’instances utilisateur en cours sans application</span><span class="sxs-lookup"><span data-stu-id="faeae-133">The current number of user instances without application</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-134">Active Video Modality Count</span><span class="sxs-lookup"><span data-stu-id="faeae-134">Active Video Modality Count</span></span></p></td>
<td><p><span data-ttu-id="faeae-135">Nombre actuel de modalités vidéo</span><span class="sxs-lookup"><span data-stu-id="faeae-135">The current number of Video modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-136">Application Creation Requests Received/Second</span><span class="sxs-lookup"><span data-stu-id="faeae-136">Application Creation Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="faeae-137">Taux par seconde de demandes de création d’application reçues</span><span class="sxs-lookup"><span data-stu-id="faeae-137">The per second rate of received application creation requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-138">AS MCU Join Failures</span><span class="sxs-lookup"><span data-stu-id="faeae-138">AS MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="faeae-139">Nombre d’échecs de connexion au service MCU AS</span><span class="sxs-lookup"><span data-stu-id="faeae-139">The number of AS MCU Join Failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-140">AV MCU Join Failures</span><span class="sxs-lookup"><span data-stu-id="faeae-140">AV MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="faeae-141">Nombre d’échecs de connexion au service MCU audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="faeae-141">The number of AV MCU Join Failures</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-142">Average Application Startup Time (ms)</span><span class="sxs-lookup"><span data-stu-id="faeae-142">Average Application Startup Time (ms)</span></span></p></td>
<td><p><span data-ttu-id="faeae-143">Délai de démarrage moyen de l’application en millisecondes</span><span class="sxs-lookup"><span data-stu-id="faeae-143">The average application startup time in Milliseconds</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-144">Average Lifetime for Session (ms)</span><span class="sxs-lookup"><span data-stu-id="faeae-144">Average Lifetime for Session (ms)</span></span></p></td>
<td><p><span data-ttu-id="faeae-145">Durée de vie moyenne pour une session en millisecondes</span><span class="sxs-lookup"><span data-stu-id="faeae-145">The average lifetime for a session in milliseconds</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-146">Data MCU Join Failures</span><span class="sxs-lookup"><span data-stu-id="faeae-146">Data MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="faeae-147">Nombre d’échecs de connexion au service MCU de données</span><span class="sxs-lookup"><span data-stu-id="faeae-147">The number of Data MCU Join Failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-148">Exchange Contact Search Latency (ms)</span><span class="sxs-lookup"><span data-stu-id="faeae-148">Exchange Contact Search Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="faeae-149">Ce compteur affiche le temps moyen (en millisecondes) nécessaire pour rechercher des contacts dans Exchange</span><span class="sxs-lookup"><span data-stu-id="faeae-149">This counter shows the average time (in milliseconds) to search contact in Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-150">Exchange HD Photo Get Latency (ms)</span><span class="sxs-lookup"><span data-stu-id="faeae-150">Exchange HD Photo Get Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="faeae-151">Ce compteur affiche le temps moyen (en millisecondes) nécessaire pour récupérer une photo HD d’Exchange</span><span class="sxs-lookup"><span data-stu-id="faeae-151">This counter shows the average time (in milliseconds) to retrieve a photo from Exchange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-152">HTTP 4xx Responses/Second</span><span class="sxs-lookup"><span data-stu-id="faeae-152">HTTP 4xx Responses/Second</span></span></p></td>
<td><p><span data-ttu-id="faeae-153">Taux de réponses avec un code 4xx HTTP par seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-153">The per second rate of responses with HTTP 4xx code</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-154">HTTP 5xx Responses/Second</span><span class="sxs-lookup"><span data-stu-id="faeae-154">HTTP 5xx Responses/Second</span></span></p></td>
<td><p><span data-ttu-id="faeae-155">Taux de réponses avec un code 5xx HTTP par seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-155">The per second rate of responses with HTTP 5xx code</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-156">IM MCU Join Failures</span><span class="sxs-lookup"><span data-stu-id="faeae-156">IM MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="faeae-157">Nombre d’échecs de connexion au service MCU de messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="faeae-157">The number of IM MCU Join Failures</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-158">Number of Active Directory Photo Get Failures</span><span class="sxs-lookup"><span data-stu-id="faeae-158">Number of Active Directory Photo Get Failures</span></span></p></td>
<td><p><span data-ttu-id="faeae-159">Nombre d’échecs de récupération de photos du répertoire actif</span><span class="sxs-lookup"><span data-stu-id="faeae-159">The total number of failures to retrieve photos from Active Directory</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-160">Number of Contact Search failures</span><span class="sxs-lookup"><span data-stu-id="faeae-160">Number of Contact Search failures</span></span></p></td>
<td><p><span data-ttu-id="faeae-161">Nombre total d’échecs de recherche de contacts dans Exchange</span><span class="sxs-lookup"><span data-stu-id="faeae-161">The total number of failures to search contacts in Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-162">Number of Deserialization Failures</span><span class="sxs-lookup"><span data-stu-id="faeae-162">Number of Deserialization Failures</span></span></p></td>
<td><p><span data-ttu-id="faeae-163">Nombre total d’échecs de désérialisation</span><span class="sxs-lookup"><span data-stu-id="faeae-163">The total number of deserialization failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-164">Nombre d’échecs de photo HD</span><span class="sxs-lookup"><span data-stu-id="faeae-164">Number of HD Photo Get Failures</span></span></p></td>
<td><p><span data-ttu-id="faeae-165">Nombre total d’échecs de récupération de photos HD depuis Exchange</span><span class="sxs-lookup"><span data-stu-id="faeae-165">The total number of failures to retrieve HD photos from Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-166">Over The Maximum Subscriptions Per Application</span><span class="sxs-lookup"><span data-stu-id="faeae-166">Over The Maximum Subscriptions Per Application</span></span></p></td>
<td><p><span data-ttu-id="faeae-167">Nombre de requêtes d’abonnement dépassant le nombre maximal autorisé par application</span><span class="sxs-lookup"><span data-stu-id="faeae-167">The number of Subscription requests over the maximum allowed per application</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-168">Over The Maximum Subscriptions Per Batch</span><span class="sxs-lookup"><span data-stu-id="faeae-168">Over The Maximum Subscriptions Per Batch</span></span></p></td>
<td><p><span data-ttu-id="faeae-169">Nombre de requêtes d’abonnement dépassant le nombre maximal autorisé par lot</span><span class="sxs-lookup"><span data-stu-id="faeae-169">The number of Subscription requests over the maximum allowed per batch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-170">Presence Subscription Failures</span><span class="sxs-lookup"><span data-stu-id="faeae-170">Presence Subscription Failures</span></span></p></td>
<td><p><span data-ttu-id="faeae-171">Nombre d’échecs d’abonnement de présence</span><span class="sxs-lookup"><span data-stu-id="faeae-171">The number of failures to subscribe presence</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-172">Registering Endpoint Failures</span><span class="sxs-lookup"><span data-stu-id="faeae-172">Registering Endpoint Failures</span></span></p></td>
<td><p><span data-ttu-id="faeae-173">Nombre d’échecs d’enregistrement de points de terminaison</span><span class="sxs-lookup"><span data-stu-id="faeae-173">The number of failures to register endpoints</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-174">Requests Received/Second</span><span class="sxs-lookup"><span data-stu-id="faeae-174">Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="faeae-175">Taux de demandes reçues par seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-175">The per second rate of received requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-176">Requests Succeeded/Second</span><span class="sxs-lookup"><span data-stu-id="faeae-176">Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="faeae-177">Taux de demandes réussies par seconde (codes de réponse 2xx/3xx HTTP)</span><span class="sxs-lookup"><span data-stu-id="faeae-177">The per second rate of successful requests (HTTP 2xx/3xx response codes)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-178">Succeeded Create Application Requests/Second</span><span class="sxs-lookup"><span data-stu-id="faeae-178">Succeeded Create Application Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="faeae-179">Taux de demandes de création d’application réussies par seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-179">The per second rate of successful application creation requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-180">Timed Out Pending Get Count</span><span class="sxs-lookup"><span data-stu-id="faeae-180">Timed Out Pending Get Count</span></span></p></td>
<td><p><span data-ttu-id="faeae-181">Nombre de gets en attente ayant expiré</span><span class="sxs-lookup"><span data-stu-id="faeae-181">The number of pending gets that timed out</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-182">Total Application Creation Requests Received</span><span class="sxs-lookup"><span data-stu-id="faeae-182">Total Application Creation Requests Received</span></span></p></td>
<td><p><span data-ttu-id="faeae-183">Nombre total de demandes de création d’application reçues depuis le démarrage du service</span><span class="sxs-lookup"><span data-stu-id="faeae-183">The total number of application creation requests received since the service was started</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-184">Total HTTP 4xx Responses</span><span class="sxs-lookup"><span data-stu-id="faeae-184">Total HTTP 4xx Responses</span></span></p></td>
<td><p><span data-ttu-id="faeae-185">Nombre total de réponses 4xx HTTP</span><span class="sxs-lookup"><span data-stu-id="faeae-185">The total number of HTTP 4xx responses</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-186">Total HTTP 5xx Responses</span><span class="sxs-lookup"><span data-stu-id="faeae-186">Total HTTP 5xx Responses</span></span></p></td>
<td><p><span data-ttu-id="faeae-187">Nombre total de réponses 5xx HTTP</span><span class="sxs-lookup"><span data-stu-id="faeae-187">The total number of HTTP 5xx responses</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-188">Total Requests Received on the Command Channel</span><span class="sxs-lookup"><span data-stu-id="faeae-188">Total Requests Received on the Command Channel</span></span></p></td>
<td><p><span data-ttu-id="faeae-189">Nombre total de demandes reçues sur le canal de commande</span><span class="sxs-lookup"><span data-stu-id="faeae-189">The total number of requests received on the command channel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-190">Total Requests Succeeded</span><span class="sxs-lookup"><span data-stu-id="faeae-190">Total Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="faeae-191">Nombre total de demandes réussies</span><span class="sxs-lookup"><span data-stu-id="faeae-191">The total number of requests that succeeded</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-192">Total Sessions Initiated</span><span class="sxs-lookup"><span data-stu-id="faeae-192">Total Sessions Initiated</span></span></p></td>
<td><p><span data-ttu-id="faeae-193">Nombre total de sessions initiées depuis le démarrage du service</span><span class="sxs-lookup"><span data-stu-id="faeae-193">The total number of sessions that were initiated since the service was started</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-194">Total Sessions Terminated Because of Idle Timeout</span><span class="sxs-lookup"><span data-stu-id="faeae-194">Total Sessions Terminated Because of Idle Timeout</span></span></p></td>
<td><p><span data-ttu-id="faeae-195">Nombre total de sessions terminées en raison d’un délai d’expiration d’inactivité</span><span class="sxs-lookup"><span data-stu-id="faeae-195">The total number of sessions that were terminated because of user idle timeout</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-196">Total Throttled Applications</span><span class="sxs-lookup"><span data-stu-id="faeae-196">Total Throttled Applications</span></span></p></td>
<td><p><span data-ttu-id="faeae-197">Nombre d’applications limitées</span><span class="sxs-lookup"><span data-stu-id="faeae-197">The number of throttled applications</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div id="sectionSection1" class="section">

### <a name="performance-counters-for-mcx-mobility-service"></a><span data-ttu-id="faeae-198">Compteurs de performances pour le service de mobilité Mcx</span><span class="sxs-lookup"><span data-stu-id="faeae-198">Performance Counters for Mcx Mobility Service</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="faeae-199">Compteur</span><span class="sxs-lookup"><span data-stu-id="faeae-199">Counter</span></span></th>
<th><span data-ttu-id="faeae-200">Description</span><span class="sxs-lookup"><span data-stu-id="faeae-200">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faeae-201">Durée de vie moyenne d’une session en millisecondes</span><span class="sxs-lookup"><span data-stu-id="faeae-201">Average Lifetime for a Session in Milliseconds</span></span></p></td>
<td><p><span data-ttu-id="faeae-202">Durée de vie moyenne pour une session en millisecondes</span><span class="sxs-lookup"><span data-stu-id="faeae-202">The average lifetime for a session in milliseconds</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-203">Abonnements actuels aux notifications push</span><span class="sxs-lookup"><span data-stu-id="faeae-203">Current Push Notification Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="faeae-p101">Nombre actuel d’abonnements de notification push. Ce chiffre, associé au Nombre de sessions actuellement actives, représente le sous-ensemble de sessions actuellement actives enregistrées pour les appareils Windows Mobile ou iPhone.</span><span class="sxs-lookup"><span data-stu-id="faeae-p101">The current number of push notification subscriptions. This number, in conjunction with Currently Active Session Count, represents the subset of currently active sessions that are registered for Windows Mobile or iPhone devices.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-206">Nombre d’interrogations réseau expirées actuellement actives</span><span class="sxs-lookup"><span data-stu-id="faeae-206">Currently Active Network Timeout Poll Count</span></span></p></td>
<td><p><span data-ttu-id="faeae-207">Nombre d’interrogations réseau dont le délai d’attente a expiré</span><span class="sxs-lookup"><span data-stu-id="faeae-207">The number of network polls that timed out</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-208">Nombre d’interrogations actuellement actives</span><span class="sxs-lookup"><span data-stu-id="faeae-208">Currently Active Poll Count</span></span></p></td>
<td><p><span data-ttu-id="faeae-209">Nombre d’interrogations actuellement actives (longues connexions au serveur)</span><span class="sxs-lookup"><span data-stu-id="faeae-209">The number of currently active polls (long-held connections to the server)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-210">Nombre de sessions actuellement actives</span><span class="sxs-lookup"><span data-stu-id="faeae-210">Currently Active Session Count</span></span></p></td>
<td><p><span data-ttu-id="faeae-211">Nombre actuel de points de terminaison enregistrés dans le service de mobilité</span><span class="sxs-lookup"><span data-stu-id="faeae-211">Current number of endpoints registered in the Mobility Service</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-212">Nombre de sessions actuellement actives avec abonnements de présence actifs</span><span class="sxs-lookup"><span data-stu-id="faeae-212">Currently Active Session Count with Active Presence Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="faeae-213">Nombre de sessions actuellement actives avec abonnements de présence actifs</span><span class="sxs-lookup"><span data-stu-id="faeae-213">The number of currently active sessions with active presence subscriptions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-214">Demandes de notifications push ayant échoué/seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-214">Push Notification Requests Failed/Second</span></span></p></td>
<td><p><span data-ttu-id="faeae-215">Taux de notifications push ayant échoué par seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-215">The per second rate of failed push notifications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-216">Demandes de notifications push réussies/seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-216">Push Notification Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="faeae-217">Taux de notifications push ayant réussi par seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-217">The per second rate of successful push notifications</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-218">Demandes de notifications push limitées/seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-218">Push Notification Requests Throttled/Second</span></span></p></td>
<td><p><span data-ttu-id="faeae-219">Taux de notifications push ayant été limitées par seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-219">The per second rate of throttled push notifications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-220">Demandes de notifications push/seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-220">Push Notification Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="faeae-221">Taux de notifications push envoyées par seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-221">The per second rate of sent push notifications</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-222">Demandes ayant échoué/seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-222">Requests Failed/Second</span></span></p></td>
<td><p><span data-ttu-id="faeae-223">Taux de demandes ayant échoué par seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-223">The per second rate of failed requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-224">Demandes reçues/seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-224">Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="faeae-225">Taux de demandes reçues par seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-225">The per second rate of received requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-226">Demandes rejetées/seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-226">Requests Rejected/Second</span></span></p></td>
<td><p><span data-ttu-id="faeae-227">Taux de demandes rejetées par seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-227">The per second rate of rejected requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-228">Demandes réussies/seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-228">Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="faeae-229">Taux de demandes réussies par seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-229">The per second rate of successful requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-230">Demandes de lancement de session réussies/seconde</span><span class="sxs-lookup"><span data-stu-id="faeae-230">Succeeded Initiate Session Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="faeae-p102">Taux de demandes Get Location réussies par seconde. Les demandes de lancement de session consomment le plus de puissance de traitement sur le serveur. La charge maximale prise en charge est de 12 par seconde. La capacité à soutenir ces charges dépend des autres charges imposées sur le serveur. Le lancement d’une session signifie généralement la connexion d’un utilisateur ayant été déconnecté depuis un laps de temps étendu.</span><span class="sxs-lookup"><span data-stu-id="faeae-p102">The per second rate of successful Get Location requests. Requests to initiate a session consume the most CPU on the server. Peak supported load is 12/second. Sustainability depends on other loads on the server. Initiate a session typically means a sign-in for a user that has been signed out for an extended period of time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-236">Nombre total d’appels vocaux entrants refusés</span><span class="sxs-lookup"><span data-stu-id="faeae-236">Total Declined Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="faeae-237">Nombre total d’appels vocaux entrants ayant été refusés</span><span class="sxs-lookup"><span data-stu-id="faeae-237">The total number of inbound voice calls that were declined</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-238">Nombre total d’appels vocaux entrants ayant échoué</span><span class="sxs-lookup"><span data-stu-id="faeae-238">Total Failed Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="faeae-239">Nombre total d’appels vocaux entrants ayant échoué</span><span class="sxs-lookup"><span data-stu-id="faeae-239">The total number of inbound voice calls that failed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-240">Nombre total d’appels vocaux sortants ayant échoué</span><span class="sxs-lookup"><span data-stu-id="faeae-240">Total Failed Outbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="faeae-241">Nombre total d’appels vocaux sortants ayant échoué</span><span class="sxs-lookup"><span data-stu-id="faeae-241">The total number of outbound voice calls that failed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-242">Nombre total de sessions terminées par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="faeae-242">Total number of sessions terminated by user</span></span></p></td>
<td><p><span data-ttu-id="faeae-243">Nombre total de sessions auxquelles les utilisateurs ont mis fin</span><span class="sxs-lookup"><span data-stu-id="faeae-243">The total number of sessions terminated by users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-244">Nombre total de demandes de notifications push</span><span class="sxs-lookup"><span data-stu-id="faeae-244">Total Push Notification Requests</span></span></p></td>
<td><p><span data-ttu-id="faeae-245">Nombre total de demandes de notifications push</span><span class="sxs-lookup"><span data-stu-id="faeae-245">The total number of push notification requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-246">Nombre total de demandes de notifications push ayant échoué</span><span class="sxs-lookup"><span data-stu-id="faeae-246">Total Push Notification Requests Failed</span></span></p></td>
<td><p><span data-ttu-id="faeae-247">Nombre total de demandes de notifications push ayant échoué</span><span class="sxs-lookup"><span data-stu-id="faeae-247">The total number of push notification requests that failed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-248">Nombre total de demandes de notifications push réussies</span><span class="sxs-lookup"><span data-stu-id="faeae-248">Total Push Notification Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="faeae-249">Nombre total de demandes de notifications push ayant réussi</span><span class="sxs-lookup"><span data-stu-id="faeae-249">The total number of push notification requests that were successful</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-250">Nombre total de demandes de notifications push limitées</span><span class="sxs-lookup"><span data-stu-id="faeae-250">Total Push Notification Requests Throttled</span></span></p></td>
<td><p><span data-ttu-id="faeae-251">Nombre total de demandes de notifications push ayant limitées</span><span class="sxs-lookup"><span data-stu-id="faeae-251">The total number of push notification requests that were throttled</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-252">Nombre total de demandes ayant échoué</span><span class="sxs-lookup"><span data-stu-id="faeae-252">Total Requests Failed</span></span></p></td>
<td><p><span data-ttu-id="faeae-253">Nombre total de demandes ayant échoué</span><span class="sxs-lookup"><span data-stu-id="faeae-253">The total number of requests that failed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-254">Nombre total de demandes reçues sur le canal de commande</span><span class="sxs-lookup"><span data-stu-id="faeae-254">Total Requests received on the Command Channel</span></span></p></td>
<td><p><span data-ttu-id="faeae-255">Nombre total de demandes reçues sur le canal de commande</span><span class="sxs-lookup"><span data-stu-id="faeae-255">The total number of requests received on the command channel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-256">Nombre total de demandes rejetées</span><span class="sxs-lookup"><span data-stu-id="faeae-256">Total Requests Rejected</span></span></p></td>
<td><p><span data-ttu-id="faeae-257">Nombre total de demandes ayant été rejetées</span><span class="sxs-lookup"><span data-stu-id="faeae-257">The total number of requests that were rejected</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-258">Nombre total de demandes réussies</span><span class="sxs-lookup"><span data-stu-id="faeae-258">Total Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="faeae-259">Nombre total de demandes effectuées au service de mobilité et ayant réussi</span><span class="sxs-lookup"><span data-stu-id="faeae-259">The total number of requests made to the Mobility Service that succeeded</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-260">Total de sessions initiées</span><span class="sxs-lookup"><span data-stu-id="faeae-260">Total Session Initiated Count</span></span></p></td>
<td><p><span data-ttu-id="faeae-261">Nombre total de sessions qui ont été initiées depuis le démarrage du service de mobilité</span><span class="sxs-lookup"><span data-stu-id="faeae-261">The total number of sessions that were initiated since the Mobility Service was started</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-262">Total des sessions terminées pour inactivité utilisateur</span><span class="sxs-lookup"><span data-stu-id="faeae-262">Total Sessions Terminated Because of User Idle Timeout</span></span></p></td>
<td><p><span data-ttu-id="faeae-263">Nombre total de sessions terminées en raison d’un délai d’expiration d’inactivité</span><span class="sxs-lookup"><span data-stu-id="faeae-263">The total number of sessions that were terminated because of user idle timeout</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faeae-264">Nombre total d’appels vocaux entrants réussis</span><span class="sxs-lookup"><span data-stu-id="faeae-264">Total Successful Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="faeae-265">Nombre total d’appels vocaux entrants ayant été réussis</span><span class="sxs-lookup"><span data-stu-id="faeae-265">The total number of inbound voice calls that were successful</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faeae-266">Nombre total d’appels vocaux sortants réussis</span><span class="sxs-lookup"><span data-stu-id="faeae-266">Total Successful Outbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="faeae-267">Nombre total d’appels vocaux sortants ayant été réussis</span><span class="sxs-lookup"><span data-stu-id="faeae-267">The total number of outbound voice calls that were successful</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="faeae-268">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="faeae-268">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

