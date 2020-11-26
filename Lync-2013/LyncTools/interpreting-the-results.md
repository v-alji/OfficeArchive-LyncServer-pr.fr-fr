---
title: Interprétation des résultats
description: Interprétation des résultats.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Interpreting the Results
ms:assetid: dd7f199f-7075-4d88-bb84-49a7e05eb593
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945608(v=OCS.15)
ms:contentKeyID: 51541433
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b8342a1ec1e15e42852fc5293f87342e98587a60
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443173"
---
# <a name="interpreting-the-results"></a><span data-ttu-id="b20df-103">Interprétation des résultats</span><span class="sxs-lookup"><span data-stu-id="b20df-103">Interpreting the Results</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b20df-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b20df-104">

<span> </span></span></span>

<span data-ttu-id="b20df-105">_**Dernière modification de la rubrique :** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="b20df-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="b20df-106">L’outil de stress et de performance de Lync Server 2013 (LyncPerfTool.exe) comporte de nombreux compteurs qui vous permettent de comprendre ce que le client effectue et s’il rencontre des problèmes.</span><span class="sxs-lookup"><span data-stu-id="b20df-106">The Lync Server 2013 Stress and Performance Tool (LyncPerfTool.exe) has many counters that you can use to understand what the client is doing and whether it is encountering issues.</span></span>

<div>

## <a name="client-counters"></a><span data-ttu-id="b20df-107">Compteurs clients</span><span class="sxs-lookup"><span data-stu-id="b20df-107">Client Counters</span></span>

<span data-ttu-id="b20df-108">Chaque instance de LyncPerfTool.exe en cours d’exécution dispose d’une instance distincte des compteurs.</span><span class="sxs-lookup"><span data-stu-id="b20df-108">Each instance of LyncPerfTool.exe that is running has a separate instance of the counters.</span></span> <span data-ttu-id="b20df-109">Chaque instance est nommée par son ID de processus.</span><span class="sxs-lookup"><span data-stu-id="b20df-109">Each instance is named by its process ID.</span></span>

<span data-ttu-id="b20df-110">Si les clients sont surchargés, des problèmes peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="b20df-110">If the clients are overloaded, issues can occur.</span></span> <span data-ttu-id="b20df-111">Pour éviter ce problème, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b20df-111">To prevent these issues, do the following:</span></span>

1.  <span data-ttu-id="b20df-112">Surveiller le processeur et l’utilisation de la mémoire sur les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="b20df-112">Monitor the CPU and the memory usage on the client computers.</span></span> <span data-ttu-id="b20df-113">Si le processeur est toujours supérieur à 90%, réduisez le nombre d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b20df-113">If the CPU is consistently above 90 percent, reduce the number of users.</span></span>

2.  <span data-ttu-id="b20df-114">Si l’encombrement mémoire est élevé, vous risquez de rencontrer des problèmes si le fichier de la page n’est pas assez grand.</span><span class="sxs-lookup"><span data-stu-id="b20df-114">If the memory footprint is high, you could run into issues if the page file is not big enough.</span></span> <span data-ttu-id="b20df-115">Assurez-vous que la mémoire de validation n’atteint pas la limite de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b20df-115">Verify that the Commit Charge is not hitting the limit on the computer.</span></span> <span data-ttu-id="b20df-116">Si vous utilisez des limites de mémoire, envisagez d’augmenter la taille de fichier de la page ou de réduire le nombre d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b20df-116">If you are running into memory limits, consider increasing the page file size or reducing the number of users</span></span>

<span data-ttu-id="b20df-117">Les tableaux suivants répertorient les principaux compteurs de performances de LyncPerfTool.</span><span class="sxs-lookup"><span data-stu-id="b20df-117">The following tables list the key LyncPerfTool performance counters.</span></span>

<span data-ttu-id="b20df-118">**Informations générales**</span><span class="sxs-lookup"><span data-stu-id="b20df-118">**General Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b20df-119"><strong>Compteur de performance</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-119"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="b20df-120"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-120"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b20df-121">Temps passé en minutes</span><span class="sxs-lookup"><span data-stu-id="b20df-121">Time Spent in Minutes</span></span></p></td>
<td><p><span data-ttu-id="b20df-122">Temps passé depuis le démarrage du processus.</span><span class="sxs-lookup"><span data-stu-id="b20df-122">Time spent since the process was started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-123">Points de terminaison actifs</span><span class="sxs-lookup"><span data-stu-id="b20df-123">Active Endpoints</span></span></p></td>
<td><p><span data-ttu-id="b20df-124">Nombre de points de terminaison actuellement connectés au serveur.</span><span class="sxs-lookup"><span data-stu-id="b20df-124">Number of endpoints currently connected to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20df-125">Échecs de connexion</span><span class="sxs-lookup"><span data-stu-id="b20df-125">Failed Logons</span></span></p></td>
<td><p><span data-ttu-id="b20df-126">Nombre total d’échecs de connexion de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b20df-126">Total number of endpoint sign-in failures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-127">Tentatives d’ouverture de session</span><span class="sxs-lookup"><span data-stu-id="b20df-127">Logon Attempts</span></span></p></td>
<td><p><span data-ttu-id="b20df-128">Nombre total de tentatives de connexion de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b20df-128">Total number of endpoint sign-in attempts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20df-129">Points de terminaison déconnectés</span><span class="sxs-lookup"><span data-stu-id="b20df-129">Endpoints Disconnected</span></span></p></td>
<td><p><span data-ttu-id="b20df-130">Nombre total de points de terminaison qui ont été déconnectés.</span><span class="sxs-lookup"><span data-stu-id="b20df-130">Total number of endpoints that have been disconnected.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b20df-131">**Informations de présence**</span><span class="sxs-lookup"><span data-stu-id="b20df-131">**Presence Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b20df-132"><strong>Compteur de performance</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-132"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="b20df-133"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-133"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b20df-134">Appels SetPresence</span><span class="sxs-lookup"><span data-stu-id="b20df-134">SetPresence Calls</span></span></p></td>
<td><p><span data-ttu-id="b20df-135">Nombre total de tentatives de changement de présence.</span><span class="sxs-lookup"><span data-stu-id="b20df-135">Total number of presence change attempts.</span></span> <span data-ttu-id="b20df-136">Pour les différents types de modifications de présence, voir le compteur de performance appels SetPresence (type de présence).</span><span class="sxs-lookup"><span data-stu-id="b20df-136">For different types of presence changes, see the SetPresence (Presence Type) Calls Performance Counter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-137">NNN réponses pour SetPresence</span><span class="sxs-lookup"><span data-stu-id="b20df-137">NNN Responses for SetPresence</span></span></p></td>
<td><p><span data-ttu-id="b20df-138">Nombre total de codes de réponse nnn reçus du serveur.</span><span class="sxs-lookup"><span data-stu-id="b20df-138">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20df-139">Appels GetPresence</span><span class="sxs-lookup"><span data-stu-id="b20df-139">GetPresence Calls</span></span></p></td>
<td><p><span data-ttu-id="b20df-140">Nombre total de tentatives de demande de présence.</span><span class="sxs-lookup"><span data-stu-id="b20df-140">Total number of get presence request attempts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-141">NNN réponses pour GetPresence</span><span class="sxs-lookup"><span data-stu-id="b20df-141">NNN Responses for GetPresence</span></span></p></td>
<td><p><span data-ttu-id="b20df-142">Nombre total de codes de réponse nnn reçus du serveur.</span><span class="sxs-lookup"><span data-stu-id="b20df-142">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b20df-143">**Informations relatives au service de carnet d’adresses**</span><span class="sxs-lookup"><span data-stu-id="b20df-143">**Address Book service Information**</span></span>

<span data-ttu-id="b20df-144">Cette catégorie inclut des compteurs permettant de surveiller les téléchargements de fichiers du service de carnet d’adresses et les demandes de service de requête sur le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b20df-144">This category includes counters used to monitor Address Book service (ABS) file downloads and Address Book Web Query service requests.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b20df-145"><strong>Compteur de performance</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-145"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="b20df-146"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-146"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b20df-147">Tentatives de téléchargements de fichiers complets/Delta de ABS</span><span class="sxs-lookup"><span data-stu-id="b20df-147">ABS Full/Delta File Downloads Attempted</span></span></p></td>
<td><p><span data-ttu-id="b20df-148">Nombre total de demandes de téléchargement de fichiers complets ou Delta.</span><span class="sxs-lookup"><span data-stu-id="b20df-148">Total number of full or delta file download requests attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-149">Réussite des téléchargements de fichiers complets/Delta</span><span class="sxs-lookup"><span data-stu-id="b20df-149">ABS Full/Delta File Downloads Succeeded</span></span></p></td>
<td><p><span data-ttu-id="b20df-150">Nombre total de demandes de téléchargement de fichiers complets ou Delta.</span><span class="sxs-lookup"><span data-stu-id="b20df-150">Total number of full or delta file download requests attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20df-151">Compteurs liés au service de requête Web dans le carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="b20df-151">Address Book Web Query service related counters</span></span></p></td>
<td><p><span data-ttu-id="b20df-152">Compteurs liés au téléchargement du fichier du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b20df-152">Address book file download related counters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-153">Tentatives d’appels WS WS</span><span class="sxs-lookup"><span data-stu-id="b20df-153">ABS WS Calls attempted</span></span></p></td>
<td><p><span data-ttu-id="b20df-154">Nombre total de demandes de service de requête Web dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b20df-154">Total number of Address Book Web Query service requests attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20df-155">Appels WS WS réussis</span><span class="sxs-lookup"><span data-stu-id="b20df-155">ABS WS Calls Succeeded</span></span></p></td>
<td><p><span data-ttu-id="b20df-156">Nombre total de demandes de service de requête Web de carnet d’adresses qui renvoient un code de réponse réussi.</span><span class="sxs-lookup"><span data-stu-id="b20df-156">Total number of Address Book Web Query service requests that returned a successful response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-157">Échecs des services d’ABS WS</span><span class="sxs-lookup"><span data-stu-id="b20df-157">ABS WS Calls Failed</span></span></p></td>
<td><p><span data-ttu-id="b20df-158">Nombre total de demandes de service de requête Web de carnet d’adresses qui renvoient un code de réponse d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b20df-158">Total number of Address Book Web Query service requests that returned an error response code.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b20df-159">**Informations de liste de distribution (DL)**</span><span class="sxs-lookup"><span data-stu-id="b20df-159">**Distribution List (DL) Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b20df-160"><strong>Compteur de performance</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-160"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="b20df-161"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-161"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b20df-162">Appels essayés</span><span class="sxs-lookup"><span data-stu-id="b20df-162">Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="b20df-163">Nombre total de demandes de service Web d’extension de liste de distribution (DLX) effectuées.</span><span class="sxs-lookup"><span data-stu-id="b20df-163">Total number of distribution list expansion (DLX) web service requests attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-164">Appels réussis</span><span class="sxs-lookup"><span data-stu-id="b20df-164">Calls Succeeded</span></span></p></td>
<td><p><span data-ttu-id="b20df-165">Nombre total de demandes de service Web DLX ayant renvoyé un code de réponse réussi.</span><span class="sxs-lookup"><span data-stu-id="b20df-165">Total number of DLX web service requests that returned a successful response code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20df-166">Appels en échec</span><span class="sxs-lookup"><span data-stu-id="b20df-166">Calls Failed</span></span></p></td>
<td><p><span data-ttu-id="b20df-167">Nombre total de demandes de service Web DLX qui renvoient un code de réponse d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b20df-167">Total number of DLX web service requests that returned an error response code.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b20df-168">**Informations de base sur VoIP**</span><span class="sxs-lookup"><span data-stu-id="b20df-168">**VoIP Basic Information**</span></span>

<span data-ttu-id="b20df-169">Les compteurs de performance indiqués ci-dessous indiquent les numéros de tous les appels voix sur IP (VoIP), y compris les appels vers le serveur de médiation, le serveur de conférence A/V, le serveur Edge, l’application Response Group et le standard automatique des conférences, lorsque ces scénarios sont activés.</span><span class="sxs-lookup"><span data-stu-id="b20df-169">The performance counters listed below report numbers for all Voice over IP (VoIP) calls, including calls to Mediation Server, A/V Conferencing Server, Edge Server, Response Group application, and Conference Auto Attendant, when these scenarios are enabled.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b20df-170"><strong>Compteur de performance</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-170"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="b20df-171"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-171"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b20df-172">Appels actifs</span><span class="sxs-lookup"><span data-stu-id="b20df-172">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="b20df-173">Nombre total d’appels vocaux entrants/sortants actuellement en cours.</span><span class="sxs-lookup"><span data-stu-id="b20df-173">Total number of incoming/outgoing voice calls ongoing currently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-174">Appels interrompus</span><span class="sxs-lookup"><span data-stu-id="b20df-174">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="b20df-175">Nombre total d’appels vocaux entrants/sortants déjà terminés.</span><span class="sxs-lookup"><span data-stu-id="b20df-175">Total number of incoming/outgoing voice calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20df-176">Appels refusés</span><span class="sxs-lookup"><span data-stu-id="b20df-176">Calls Declined</span></span></p></td>
<td><p><span data-ttu-id="b20df-177">Nombre total d’appels vocaux entrants refusés.</span><span class="sxs-lookup"><span data-stu-id="b20df-177">Total number of incoming voice calls declined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-178">Tentatives d’appels entrants/sortants</span><span class="sxs-lookup"><span data-stu-id="b20df-178">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="b20df-179">Nombre total d’appels vocaux entrants/sortants.</span><span class="sxs-lookup"><span data-stu-id="b20df-179">Total number of incoming/outgoing voice calls attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20df-180">Appels entrants/sortants établis</span><span class="sxs-lookup"><span data-stu-id="b20df-180">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="b20df-181">Nombre total d’appels vocaux entrants/sortants établis.</span><span class="sxs-lookup"><span data-stu-id="b20df-181">Total number of incoming/outgoing voice calls established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-182">Appels reçus NNN</span><span class="sxs-lookup"><span data-stu-id="b20df-182">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="b20df-183">Nombre total de codes de réponse nnn reçus du serveur.</span><span class="sxs-lookup"><span data-stu-id="b20df-183">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20df-184">Taux de passe VoIP (%)</span><span class="sxs-lookup"><span data-stu-id="b20df-184">VoIP Pass Rate (%)</span></span></p></td>
<td><p><span data-ttu-id="b20df-185">Nombre total d’appels passés/nombre total d’appels tentés.</span><span class="sxs-lookup"><span data-stu-id="b20df-185">Total calls established/Total calls attempted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b20df-186">**Informations de l’appel service de Response Group**</span><span class="sxs-lookup"><span data-stu-id="b20df-186">**Response Group service Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b20df-187"><strong>Compteur de performance</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-187"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="b20df-188"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-188"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b20df-189">Appels actifs</span><span class="sxs-lookup"><span data-stu-id="b20df-189">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="b20df-190">Nombre total d’appels actifs vers l’application Response Group.</span><span class="sxs-lookup"><span data-stu-id="b20df-190">Total number of active calls to the Response Group application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-191">Appels essayés</span><span class="sxs-lookup"><span data-stu-id="b20df-191">Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="b20df-192">Nombre total d’appels tentés.</span><span class="sxs-lookup"><span data-stu-id="b20df-192">Total number of calls attempted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b20df-193">**Informations sur les appels de messagerie instantanée**</span><span class="sxs-lookup"><span data-stu-id="b20df-193">**Instant Messaging (IM) Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b20df-194"><strong>Compteur de performance</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-194"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="b20df-195"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-195"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b20df-196">Appels actifs</span><span class="sxs-lookup"><span data-stu-id="b20df-196">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="b20df-197">Nombre total d’appels de messages instantanés entrants et sortants.</span><span class="sxs-lookup"><span data-stu-id="b20df-197">Total number of ongoing incoming/outgoing instant messaging calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-198">Appels interrompus</span><span class="sxs-lookup"><span data-stu-id="b20df-198">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="b20df-199">Nombre total d’appels entrants/sortants de messagerie instantanée déjà terminés.</span><span class="sxs-lookup"><span data-stu-id="b20df-199">Total number of incoming/outgoing instant messaging calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20df-200">Appels reçus NNN</span><span class="sxs-lookup"><span data-stu-id="b20df-200">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="b20df-201">Nombre total de codes de réponse nnn reçus du serveur.</span><span class="sxs-lookup"><span data-stu-id="b20df-201">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-202">Messages INSTANTANÉs reçus/envoyés</span><span class="sxs-lookup"><span data-stu-id="b20df-202">IM Messages Received/Sent</span></span></p></td>
<td><p><span data-ttu-id="b20df-203">Nombre total de messages reçus ou envoyés pour toutes les sessions.</span><span class="sxs-lookup"><span data-stu-id="b20df-203">Total number of messages received or sent for all sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20df-204">Tentatives d’appels entrants/sortants</span><span class="sxs-lookup"><span data-stu-id="b20df-204">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="b20df-205">Nombre total d’appels entrants/sortants de messages instantanés.</span><span class="sxs-lookup"><span data-stu-id="b20df-205">Total number of incoming/outgoing instant messaging calls attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-206">Appels entrants/sortants établis</span><span class="sxs-lookup"><span data-stu-id="b20df-206">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="b20df-207">Nombre total d’appels entrants/sortants de messages instantanés établis.</span><span class="sxs-lookup"><span data-stu-id="b20df-207">Total number of incoming/outgoing instant message calls established.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b20df-208">**Informations sur les appels de partage d’application**</span><span class="sxs-lookup"><span data-stu-id="b20df-208">**App Sharing Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b20df-209"><strong>Compteur de performance</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-209"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="b20df-210"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-210"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b20df-211">Appels actifs</span><span class="sxs-lookup"><span data-stu-id="b20df-211">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="b20df-212">Nombre total d’appels de partage d’application entrants ou sortants.</span><span class="sxs-lookup"><span data-stu-id="b20df-212">Total number of ongoing incoming/outgoing application sharing calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-213">Appels interrompus</span><span class="sxs-lookup"><span data-stu-id="b20df-213">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="b20df-214">Nombre total d’appels de partage d’application entrants/sortants déjà terminés.</span><span class="sxs-lookup"><span data-stu-id="b20df-214">Total number of incoming/outgoing application sharing calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20df-215">Appels reçus NNN</span><span class="sxs-lookup"><span data-stu-id="b20df-215">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="b20df-216">Nombre total de codes de réponse nnn reçus du serveur.</span><span class="sxs-lookup"><span data-stu-id="b20df-216">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-217">Tentatives d’appels entrants/sortants</span><span class="sxs-lookup"><span data-stu-id="b20df-217">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="b20df-218">Nombre total d’appels entrants/sortants de partage d’application.</span><span class="sxs-lookup"><span data-stu-id="b20df-218">Total number of incoming/outgoing application sharing calls attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20df-219">Appels entrants/sortants établis</span><span class="sxs-lookup"><span data-stu-id="b20df-219">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="b20df-220">Nombre total d’appels de partage d’application entrants/sortants établis.</span><span class="sxs-lookup"><span data-stu-id="b20df-220">Total number of incoming/outgoing application sharing calls established.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b20df-221">**Informations sur les appels CAA**</span><span class="sxs-lookup"><span data-stu-id="b20df-221">**CAA Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b20df-222"><strong>Compteur de performance</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-222"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="b20df-223"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-223"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b20df-224">Appels actifs</span><span class="sxs-lookup"><span data-stu-id="b20df-224">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="b20df-225">Nombre total d’appels entrants/sortants de réseau téléphonique commuté (RTC) actuellement en cours.</span><span class="sxs-lookup"><span data-stu-id="b20df-225">Total number of incoming/outgoing public switched telephone network (PSTN) calls ongoing currently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-226">Appels interrompus</span><span class="sxs-lookup"><span data-stu-id="b20df-226">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="b20df-227">Nombre total d’appels RTC entrants/sortants déjà terminés.</span><span class="sxs-lookup"><span data-stu-id="b20df-227">Total number of incoming/outgoing PSTN calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20df-228">Tentatives d’appels entrants/sortants</span><span class="sxs-lookup"><span data-stu-id="b20df-228">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="b20df-229">Nombre total d’appels RTC entrants et sortants.</span><span class="sxs-lookup"><span data-stu-id="b20df-229">Total number of incoming/outgoing PSTN calls attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-230">Appels entrants/sortants établis</span><span class="sxs-lookup"><span data-stu-id="b20df-230">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="b20df-231">Nombre total d’appels RTC entrants/sortants établis.</span><span class="sxs-lookup"><span data-stu-id="b20df-231">Total number of incoming/outgoing PSTN calls established.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b20df-232">**Informations sur la Conférence**</span><span class="sxs-lookup"><span data-stu-id="b20df-232">**Conference Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b20df-233"><strong>Compteur de performance</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-233"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="b20df-234"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-234"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b20df-235">Conférences de messagerie instantanée actives</span><span class="sxs-lookup"><span data-stu-id="b20df-235">Active Instant Messaging Conferences</span></span></p></td>
<td><p><span data-ttu-id="b20df-236">Nombre total de conférences de messagerie instantanée en cours.</span><span class="sxs-lookup"><span data-stu-id="b20df-236">Total number of ongoing instant messaging conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-237">Conférences audio/vidéo actives</span><span class="sxs-lookup"><span data-stu-id="b20df-237">Active Audio/Video Conferences</span></span></p></td>
<td><p><span data-ttu-id="b20df-238">Nombre total de conférences audio/vidéo (A/V) en cours.</span><span class="sxs-lookup"><span data-stu-id="b20df-238">Total number of ongoing audio/video (A/V) conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20df-239">Conférences de partage d’application actives</span><span class="sxs-lookup"><span data-stu-id="b20df-239">Active Application Sharing Conferences</span></span></p></td>
<td><p><span data-ttu-id="b20df-240">Nombre total de conférences de partage d’application en cours.</span><span class="sxs-lookup"><span data-stu-id="b20df-240">Total number of ongoing application sharing conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-241">Nombre de participants</span><span class="sxs-lookup"><span data-stu-id="b20df-241">Number of Participants</span></span></p></td>
<td><p><span data-ttu-id="b20df-242">Nombre total de participants actuellement connectés aux conférences.</span><span class="sxs-lookup"><span data-stu-id="b20df-242">Total number of participants currently connected to conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20df-243">Échec de la planification de conférences</span><span class="sxs-lookup"><span data-stu-id="b20df-243">Conference Schedule Failure</span></span></p></td>
<td><p><span data-ttu-id="b20df-244">Nombre total d’échecs lors de la planification d’une conférence.</span><span class="sxs-lookup"><span data-stu-id="b20df-244">Total number of failures while trying to schedule a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-245">Participer à une conférence téléphonique</span><span class="sxs-lookup"><span data-stu-id="b20df-245">Join Conference Failure</span></span></p></td>
<td><p><span data-ttu-id="b20df-246">Nombre total d’échecs lors d’une tentative de connexion à une conférence.</span><span class="sxs-lookup"><span data-stu-id="b20df-246">Total number of failures while trying to connect to a conference.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b20df-247">**Compteurs du client UCWA**</span><span class="sxs-lookup"><span data-stu-id="b20df-247">**UCWA Client Counters**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b20df-248"><strong>Compteur de performance</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-248"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="b20df-249"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="b20df-249"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b20df-250">Nombre total de jointures IMMCU réussies</span><span class="sxs-lookup"><span data-stu-id="b20df-250">Total Number of IMMCU Joins Succeeded</span></span></p></td>
<td><p><span data-ttu-id="b20df-251">Nombre total de conférences de messagerie instantanée jointes.</span><span class="sxs-lookup"><span data-stu-id="b20df-251">Total number of instant messaging conferences joined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20df-252">Nombre total de jointures DMCU réussies</span><span class="sxs-lookup"><span data-stu-id="b20df-252">Total Number of DMCU Joins Succeeded</span></span></p></td>
<td><p><span data-ttu-id="b20df-253">Nombre total de conférences A/V jointes.</span><span class="sxs-lookup"><span data-stu-id="b20df-253">Total number of A/V conferences joined.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b20df-254">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b20df-254">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

