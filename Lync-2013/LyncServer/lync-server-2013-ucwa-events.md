---
title: 'Lync Server 2013 : événements UCWA'
description: 'Lync Server 2013 : événements UCWA.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UCWA events
ms:assetid: 26cb409d-f4e4-43c7-873f-b694702d491d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945621(v=OCS.15)
ms:contentKeyID: 51541461
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8104ce9c7533350f40ce194e1cde205bc3692792
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440464"
---
# <a name="ucwa-events-in-lync-server-2013"></a><span data-ttu-id="45352-103">Événements adUCWA dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="45352-103">UCWA events in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="45352-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="45352-104">

<span> </span></span></span>

<span data-ttu-id="45352-105">_**Dernière modification de la rubrique :** 2013-02-15_</span><span class="sxs-lookup"><span data-stu-id="45352-105">_**Topic Last Modified:** 2013-02-15_</span></span>

    The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="45352-106">Lync Server 2013 utilise l’API UCWA (Unified Communications Web API) à diverses fins, en accédant à Microsoft Exchange pour les recherches de contacts pour la mise à jour de la présence pour les clients mobiles.</span><span class="sxs-lookup"><span data-stu-id="45352-106">Lync Server 2013 uses the Unified Communications Web API (UCWA) for a number of purposes, from accessing Microsoft Exchange for contact searches to updating presence for mobile clients.</span></span>

<span data-ttu-id="45352-p101">L’API UCWA écrit les enregistrements liés aux opérations en tant qu’événements de type information, avertissement ou erreur. Le tableau suivant décrit les événements pouvant être écrits par les composants de l’API UCWA.</span><span class="sxs-lookup"><span data-stu-id="45352-p101">UCWA will write records of operational behavior as event types Informational, Warning, and Error. The following table describes the events that can be written by the UCWA components.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45352-109">ID d’événement</span><span class="sxs-lookup"><span data-stu-id="45352-109">Event ID</span></span></th>
<th><span data-ttu-id="45352-110">Type d’événement</span><span class="sxs-lookup"><span data-stu-id="45352-110">Event Type</span></span></th>
<th><span data-ttu-id="45352-111">Résumé</span><span class="sxs-lookup"><span data-stu-id="45352-111">Summary</span></span></th>
<th><span data-ttu-id="45352-112">Cause et résolution</span><span class="sxs-lookup"><span data-stu-id="45352-112">Cause and Resolution</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45352-113">20001</span><span class="sxs-lookup"><span data-stu-id="45352-113">20001</span></span></p></td>
<td><p><span data-ttu-id="45352-114">Information</span><span class="sxs-lookup"><span data-stu-id="45352-114">Informational</span></span></p></td>
<td><p><span data-ttu-id="45352-115">API UCWA initialisée</span><span class="sxs-lookup"><span data-stu-id="45352-115">UCWA initialized</span></span></p></td>
<td><p><span data-ttu-id="45352-116">N/A</span><span class="sxs-lookup"><span data-stu-id="45352-116">N/A</span></span></p>
<p><span data-ttu-id="45352-117">N/A</span><span class="sxs-lookup"><span data-stu-id="45352-117">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45352-118">20002</span><span class="sxs-lookup"><span data-stu-id="45352-118">20002</span></span></p></td>
<td><p><span data-ttu-id="45352-119">Erreur</span><span class="sxs-lookup"><span data-stu-id="45352-119">Error</span></span></p></td>
<td><p><span data-ttu-id="45352-120">L’API UCWA a rencontré une exception inattendue pendant son initialisation.</span><span class="sxs-lookup"><span data-stu-id="45352-120">UCWA encountered an unexpected exception during initialization</span></span></p></td>
<td><p><span data-ttu-id="45352-121">Une erreur inattendue s’est produite pendant l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="45352-121">An unexpected error has occurred during initialization</span></span></p>
<p><span data-ttu-id="45352-122">Examinez les détails de l’exception dans l’entrée correspondante du journal des événements pour déterminer la cause possible.</span><span class="sxs-lookup"><span data-stu-id="45352-122">Examine the exception details in the associated event log entry to determine the possible cause</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45352-123">20003</span><span class="sxs-lookup"><span data-stu-id="45352-123">20003</span></span></p></td>
<td><p><span data-ttu-id="45352-124">Erreur</span><span class="sxs-lookup"><span data-stu-id="45352-124">Error</span></span></p></td>
<td><p><span data-ttu-id="45352-125">L’API UCWA a rencontré une exception non traitée.</span><span class="sxs-lookup"><span data-stu-id="45352-125">UCWA encountered an unhandled exception</span></span></p></td>
<td><p><span data-ttu-id="45352-126">Une exception non traitée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="45352-126">An unhandled exception happened</span></span></p>
<p><span data-ttu-id="45352-p102">Redémarrez le serveur. Si le problème persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="45352-p102">Restart the server. If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45352-129">20004</span><span class="sxs-lookup"><span data-stu-id="45352-129">20004</span></span></p></td>
<td><p><span data-ttu-id="45352-130">Erreur</span><span class="sxs-lookup"><span data-stu-id="45352-130">Error</span></span></p></td>
<td><p><span data-ttu-id="45352-131">Impossible d’accéder à Exchange pour la photo HD</span><span class="sxs-lookup"><span data-stu-id="45352-131">Cannot access Exchange for HD photo</span></span></p></td>
<td><p><span data-ttu-id="45352-132">La connexion à Exchange n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="45352-132">Connection to Exchange is not available</span></span></p>
<p><span data-ttu-id="45352-133">Vérifiez que la connexion à Exchange est disponible.</span><span class="sxs-lookup"><span data-stu-id="45352-133">Make sure the connection to Exchange is available</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45352-134">20005</span><span class="sxs-lookup"><span data-stu-id="45352-134">20005</span></span></p></td>
<td><p><span data-ttu-id="45352-135">Information</span><span class="sxs-lookup"><span data-stu-id="45352-135">Informational</span></span></p></td>
<td><p><span data-ttu-id="45352-136">Récupération de l’échec de l’accès à Exchange pour la photo HD</span><span class="sxs-lookup"><span data-stu-id="45352-136">Recovered from failing to access Exchange for HD photo</span></span></p></td>
<td><p><span data-ttu-id="45352-137">N/A</span><span class="sxs-lookup"><span data-stu-id="45352-137">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45352-138">20006</span><span class="sxs-lookup"><span data-stu-id="45352-138">20006</span></span></p></td>
<td><p><span data-ttu-id="45352-139">Erreur</span><span class="sxs-lookup"><span data-stu-id="45352-139">Error</span></span></p></td>
<td><p><span data-ttu-id="45352-140">Impossible d’accéder à Exchange pour la recherche de contact</span><span class="sxs-lookup"><span data-stu-id="45352-140">Cannot access Exchange for contact search</span></span></p></td>
<td><p><span data-ttu-id="45352-141">La connexion à Exchange n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="45352-141">Connection to Exchange is not available</span></span></p>
<p><span data-ttu-id="45352-142">Vérifiez que la connexion à Exchange est disponible.</span><span class="sxs-lookup"><span data-stu-id="45352-142">Make sure the connection to Exchange is available</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45352-143">20007</span><span class="sxs-lookup"><span data-stu-id="45352-143">20007</span></span></p></td>
<td><p><span data-ttu-id="45352-144">Information</span><span class="sxs-lookup"><span data-stu-id="45352-144">Informational</span></span></p></td>
<td><p><span data-ttu-id="45352-145">Récupération de l’échec de la recherche de contact dans Exchange</span><span class="sxs-lookup"><span data-stu-id="45352-145">Recovered from failing to search contact in Exchange</span></span></p></td>
<td><p><span data-ttu-id="45352-146">N/A</span><span class="sxs-lookup"><span data-stu-id="45352-146">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45352-147">20008</span><span class="sxs-lookup"><span data-stu-id="45352-147">20008</span></span></p></td>
<td><p><span data-ttu-id="45352-148">Avertissement</span><span class="sxs-lookup"><span data-stu-id="45352-148">Warning</span></span></p></td>
<td><p><span data-ttu-id="45352-149">Tentative de souscription à un nombre d’abonnements aux informations de présence supérieur au nombre autorisé par application</span><span class="sxs-lookup"><span data-stu-id="45352-149">Attempt to subscribe more than the allowed presence subscriptions per application</span></span></p></td>
<td><p><span data-ttu-id="45352-150">Tentative de souscription à un nombre d’abonnements aux informations de présence supérieur au nombre autorisé par application</span><span class="sxs-lookup"><span data-stu-id="45352-150">Attempt to subscribe more than the allowed presence subscriptions per application</span></span></p>
<p><span data-ttu-id="45352-151">Vérifiez si les clients possèdent des abonnements superflus.</span><span class="sxs-lookup"><span data-stu-id="45352-151">Check the clients for unnecessary subscriptions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45352-152">20009</span><span class="sxs-lookup"><span data-stu-id="45352-152">20009</span></span></p></td>
<td><p><span data-ttu-id="45352-153">Avertissement</span><span class="sxs-lookup"><span data-stu-id="45352-153">Warning</span></span></p></td>
<td><p><span data-ttu-id="45352-154">Tentative de souscription à un nombre d’abonnements aux informations de présence supérieur au nombre autorisé par lot</span><span class="sxs-lookup"><span data-stu-id="45352-154">Attempt to subscribe more than the allowed presence subscriptions per batch</span></span></p></td>
<td><p><span data-ttu-id="45352-155">Tentative de souscription à un nombre d’abonnements aux informations de présence supérieur au nombre autorisé par lot</span><span class="sxs-lookup"><span data-stu-id="45352-155">Attempt to subscribe more than the allowed presence subscriptions per batch</span></span></p>
<p><span data-ttu-id="45352-156">Vérifiez si les clients possèdent des abonnements superflus.</span><span class="sxs-lookup"><span data-stu-id="45352-156">Check the clients for unnecessary subscriptions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45352-157">20010</span><span class="sxs-lookup"><span data-stu-id="45352-157">20010</span></span></p></td>
<td><p><span data-ttu-id="45352-158">Erreur</span><span class="sxs-lookup"><span data-stu-id="45352-158">Error</span></span></p></td>
<td><p><span data-ttu-id="45352-159">Impossible de récupérer les données de la bande entrante</span><span class="sxs-lookup"><span data-stu-id="45352-159">Cannot retrieve inband data</span></span></p></td>
<td><p><span data-ttu-id="45352-160">Impossible de récupérer les données de la bande entrante</span><span class="sxs-lookup"><span data-stu-id="45352-160">Cannot retrieve inband data</span></span></p>
<p><span data-ttu-id="45352-161">Si le problème persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="45352-161">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45352-162">20011</span><span class="sxs-lookup"><span data-stu-id="45352-162">20011</span></span></p></td>
<td><p><span data-ttu-id="45352-163">Erreur</span><span class="sxs-lookup"><span data-stu-id="45352-163">Error</span></span></p></td>
<td><p><span data-ttu-id="45352-164">Impossible de s’abonner aux informations de présence</span><span class="sxs-lookup"><span data-stu-id="45352-164">Cannot subscribe presence</span></span></p></td>
<td><p><span data-ttu-id="45352-165">Impossible de s’abonner aux informations de présence</span><span class="sxs-lookup"><span data-stu-id="45352-165">Cannot subscribe presence</span></span></p>
<p><span data-ttu-id="45352-166">Si le problème persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="45352-166">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45352-167">20012</span><span class="sxs-lookup"><span data-stu-id="45352-167">20012</span></span></p></td>
<td><p><span data-ttu-id="45352-168">Erreur</span><span class="sxs-lookup"><span data-stu-id="45352-168">Error</span></span></p></td>
<td><p><span data-ttu-id="45352-169">Échec de l’enregistrement du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="45352-169">Failed to register endpoint</span></span></p></td>
<td><p><span data-ttu-id="45352-170">Échec de l’enregistrement du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="45352-170">Failed to register endpoint</span></span></p>
<p><span data-ttu-id="45352-171">Si le problème persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="45352-171">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45352-172">20013</span><span class="sxs-lookup"><span data-stu-id="45352-172">20013</span></span></p></td>
<td><p><span data-ttu-id="45352-173">Erreur</span><span class="sxs-lookup"><span data-stu-id="45352-173">Error</span></span></p></td>
<td><p><span data-ttu-id="45352-174">Le MCU de messagerie instantanée n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="45352-174">IM MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="45352-175">Le MCU de messagerie instantanée n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="45352-175">IM MCU is unavailable</span></span></p>
<p><span data-ttu-id="45352-176">Vérifiez si le MCU de messagerie instantanée est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="45352-176">See whether IM MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45352-177">20014</span><span class="sxs-lookup"><span data-stu-id="45352-177">20014</span></span></p></td>
<td><p><span data-ttu-id="45352-178">Information</span><span class="sxs-lookup"><span data-stu-id="45352-178">Informational</span></span></p></td>
<td><p><span data-ttu-id="45352-179">Récupération de l’échec de la connexion au MCU de messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="45352-179">Recovered from failing to connect to IM MCU</span></span></p></td>
<td><p><span data-ttu-id="45352-180">N/A</span><span class="sxs-lookup"><span data-stu-id="45352-180">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45352-181">20015</span><span class="sxs-lookup"><span data-stu-id="45352-181">20015</span></span></p></td>
<td><p><span data-ttu-id="45352-182">Erreur</span><span class="sxs-lookup"><span data-stu-id="45352-182">Error</span></span></p></td>
<td><p><span data-ttu-id="45352-183">Le MCU AV n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="45352-183">AV MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="45352-184">Le MCU AV n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="45352-184">AV MCU is unavailable</span></span></p>
<p><span data-ttu-id="45352-185">Vérifiez si le MCU AV est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="45352-185">See whether AV MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45352-186">20016</span><span class="sxs-lookup"><span data-stu-id="45352-186">20016</span></span></p></td>
<td><p><span data-ttu-id="45352-187">Information</span><span class="sxs-lookup"><span data-stu-id="45352-187">Informational</span></span></p></td>
<td><p><span data-ttu-id="45352-188">Récupération de l’échec de la connexion au MCU AV</span><span class="sxs-lookup"><span data-stu-id="45352-188">Recovered from failing to connect to AV MCU</span></span></p></td>
<td><p><span data-ttu-id="45352-189">N/A</span><span class="sxs-lookup"><span data-stu-id="45352-189">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45352-190">20017</span><span class="sxs-lookup"><span data-stu-id="45352-190">20017</span></span></p></td>
<td><p><span data-ttu-id="45352-191">Erreur</span><span class="sxs-lookup"><span data-stu-id="45352-191">Error</span></span></p></td>
<td><p><span data-ttu-id="45352-192">Le MCU AS n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="45352-192">AS MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="45352-193">Le MCU AS n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="45352-193">AS MCU is unavailable</span></span></p>
<p><span data-ttu-id="45352-194">Vérifiez si le MCU AS est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="45352-194">See whether AS MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45352-195">20018</span><span class="sxs-lookup"><span data-stu-id="45352-195">20018</span></span></p></td>
<td><p><span data-ttu-id="45352-196">Information</span><span class="sxs-lookup"><span data-stu-id="45352-196">Informational</span></span></p></td>
<td><p><span data-ttu-id="45352-197">Récupération de l’échec de la connexion au MCU AS</span><span class="sxs-lookup"><span data-stu-id="45352-197">Recovered from failing to connect to AS MCU</span></span></p></td>
<td><p><span data-ttu-id="45352-198">N/A</span><span class="sxs-lookup"><span data-stu-id="45352-198">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45352-199">20019</span><span class="sxs-lookup"><span data-stu-id="45352-199">20019</span></span></p></td>
<td><p><span data-ttu-id="45352-200">Erreur</span><span class="sxs-lookup"><span data-stu-id="45352-200">Error</span></span></p></td>
<td><p><span data-ttu-id="45352-201">Le MCU de données n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="45352-201">Data MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="45352-202">Le MCU de données n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="45352-202">Data MCU is unavailable</span></span></p>
<p><span data-ttu-id="45352-203">Vérifiez si le MCU de données est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="45352-203">See whether Data MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45352-204">20020</span><span class="sxs-lookup"><span data-stu-id="45352-204">20020</span></span></p></td>
<td><p><span data-ttu-id="45352-205">Information</span><span class="sxs-lookup"><span data-stu-id="45352-205">Informational</span></span></p></td>
<td><p><span data-ttu-id="45352-206">Récupération de l’échec de la connexion au MCU de données</span><span class="sxs-lookup"><span data-stu-id="45352-206">Recovered from failing to connect to Data MCU</span></span></p></td>
<td><p><span data-ttu-id="45352-207">N/A</span><span class="sxs-lookup"><span data-stu-id="45352-207">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45352-208">20021</span><span class="sxs-lookup"><span data-stu-id="45352-208">20021</span></span></p></td>
<td><p><span data-ttu-id="45352-209">Erreur</span><span class="sxs-lookup"><span data-stu-id="45352-209">Error</span></span></p></td>
<td><p><span data-ttu-id="45352-210">Impossible de rejoindre le MCU de messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="45352-210">Cannot join IM MCU</span></span></p></td>
<td><p><span data-ttu-id="45352-211">Impossible de rejoindre le MCU de messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="45352-211">Cannot join IM MCU</span></span></p>
<p><span data-ttu-id="45352-212">Vérifiez si le MCU de messagerie instantanée est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="45352-212">See whether IM MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45352-213">20022</span><span class="sxs-lookup"><span data-stu-id="45352-213">20022</span></span></p></td>
<td><p><span data-ttu-id="45352-214">Erreur</span><span class="sxs-lookup"><span data-stu-id="45352-214">Error</span></span></p></td>
<td><p><span data-ttu-id="45352-215">Impossible de rejoindre le MCU AV</span><span class="sxs-lookup"><span data-stu-id="45352-215">Cannot join AV MCU</span></span></p></td>
<td><p><span data-ttu-id="45352-216">Impossible de rejoindre le MCU AV</span><span class="sxs-lookup"><span data-stu-id="45352-216">Cannot join AV MCU</span></span></p>
<p><span data-ttu-id="45352-217">Vérifiez si le MCU AV est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="45352-217">See whether AV MCU is running</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45352-218">20023</span><span class="sxs-lookup"><span data-stu-id="45352-218">20023</span></span></p></td>
<td><p><span data-ttu-id="45352-219">Erreur</span><span class="sxs-lookup"><span data-stu-id="45352-219">Error</span></span></p></td>
<td><p><span data-ttu-id="45352-220">Impossible de rejoindre le MCU AS</span><span class="sxs-lookup"><span data-stu-id="45352-220">Cannot join AS MCU</span></span></p></td>
<td><p><span data-ttu-id="45352-221">Impossible de rejoindre le MCU AS</span><span class="sxs-lookup"><span data-stu-id="45352-221">Cannot join AS MCU</span></span></p>
<p><span data-ttu-id="45352-222">Vérifiez si le MCU AS est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="45352-222">See whether AS MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45352-223">20024</span><span class="sxs-lookup"><span data-stu-id="45352-223">20024</span></span></p></td>
<td><p><span data-ttu-id="45352-224">Erreur</span><span class="sxs-lookup"><span data-stu-id="45352-224">Error</span></span></p></td>
<td><p><span data-ttu-id="45352-225">Impossible de rejoindre le MCU de données</span><span class="sxs-lookup"><span data-stu-id="45352-225">Cannot join Data MCU</span></span></p></td>
<td><p><span data-ttu-id="45352-226">Impossible de rejoindre le MCU de données</span><span class="sxs-lookup"><span data-stu-id="45352-226">Cannot join Data MCU</span></span></p>
<p><span data-ttu-id="45352-227">Vérifiez si le MCU de données est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="45352-227">See whether Data MCU is running</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45352-228">20025</span><span class="sxs-lookup"><span data-stu-id="45352-228">20025</span></span></p></td>
<td><p><span data-ttu-id="45352-229">Erreur</span><span class="sxs-lookup"><span data-stu-id="45352-229">Error</span></span></p></td>
<td><p><span data-ttu-id="45352-230">Impossible d’accéder à Active Directory pour la photo</span><span class="sxs-lookup"><span data-stu-id="45352-230">Cannot access active directory for photo</span></span></p></td>
<td><p><span data-ttu-id="45352-231">La connexion à Active Directory n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="45352-231">Connection to active directory is not available</span></span></p>
<p><span data-ttu-id="45352-232">Vérifiez que la connexion à Active Directory est disponible.</span><span class="sxs-lookup"><span data-stu-id="45352-232">Make sure the connection to active directory is available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45352-233">20026</span><span class="sxs-lookup"><span data-stu-id="45352-233">20026</span></span></p></td>
<td><p><span data-ttu-id="45352-234">Information</span><span class="sxs-lookup"><span data-stu-id="45352-234">Informational</span></span></p></td>
<td><p><span data-ttu-id="45352-235">Récupération de l’échec de l’accès à Active Directory pour la photo</span><span class="sxs-lookup"><span data-stu-id="45352-235">Recovered from failing to access active directory for photo</span></span></p></td>
<td><p><span data-ttu-id="45352-236">N/A</span><span class="sxs-lookup"><span data-stu-id="45352-236">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45352-237">20027</span><span class="sxs-lookup"><span data-stu-id="45352-237">20027</span></span></p></td>
<td><p><span data-ttu-id="45352-238">Avertissement</span><span class="sxs-lookup"><span data-stu-id="45352-238">Warning</span></span></p></td>
<td><p><span data-ttu-id="45352-239">Impossible d’effectuer la désérialisation</span><span class="sxs-lookup"><span data-stu-id="45352-239">Cannot deserialize</span></span></p></td>
<td><p><span data-ttu-id="45352-240">Impossible d’effectuer la désérialisation</span><span class="sxs-lookup"><span data-stu-id="45352-240">Cannot deserialize</span></span></p>
<p><span data-ttu-id="45352-241">Si le problème persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="45352-241">If the problem persists contact product support</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="45352-242">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="45352-242">


</div>

<span> </span>

</div>

</div>

</span></span></div>

