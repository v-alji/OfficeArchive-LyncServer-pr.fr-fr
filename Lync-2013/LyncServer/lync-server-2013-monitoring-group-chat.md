---
title: 'Lync Server 2013 : surveillance des discussions de groupe'
description: 'Lync Server 2013 : surveillance des discussions de groupe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring group chat
ms:assetid: bddcf0be-ebf3-46bc-90c7-2576877734fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720924(v=OCS.15)
ms:contentKeyID: 63969648
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 625e45f455e8dba50a5fa64240b62cb010623d16
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425422"
---
# <a name="monitoring-group-chat-in-lync-server-2013"></a><span data-ttu-id="34154-103">Surveiller la discussion de groupe dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="34154-103">Monitoring group chat in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="34154-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="34154-104">

<span> </span></span></span>

<span data-ttu-id="34154-105">_**Dernière modification de la rubrique :** 2014-08-04_</span><span class="sxs-lookup"><span data-stu-id="34154-105">_**Topic Last Modified:** 2014-08-04_</span></span>

<span data-ttu-id="34154-106">Nous vous recommandons vivement d’exécuter le [programme d’installation de mise à jour de serveur cumulative](https://support.microsoft.com/kb/968802) le plus récent disponible sur le centre de téléchargement Microsoft pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="34154-106">We highly recommend running the most recent [Cumulative Server Update Installer](https://support.microsoft.com/kb/968802) available on the Microsoft Download Center for performance improvements.</span></span>

<span data-ttu-id="34154-107">En supposant que vous exécutez la dernière mise à jour cumulative, utilisez le tableau de test de stress suivant pour déterminer si vos serveurs de discussion de groupe s’exécutent de manière optimale.</span><span class="sxs-lookup"><span data-stu-id="34154-107">Assuming you are running latest cumulative update, use the following stress test table for metrics to understand if your Group Chat Servers are running at optimal health.</span></span>

### <a name="test-environment-and-user-model"></a><span data-ttu-id="34154-108">Environnement de test et modèle utilisateur</span><span class="sxs-lookup"><span data-stu-id="34154-108">Test environment and user model</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34154-109">Trois serveurs de discussion de groupe dans une liste de discussion de groupe, chacun avec 8 Go de mémoire et 8 processeurs.</span><span class="sxs-lookup"><span data-stu-id="34154-109">Three Group Chat Servers in a Group Chat pool, each with 8 GB memory and 8 processors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34154-110">Deux serveurs frontaux de Lync Server 2013 dans l’édition Enterprise.</span><span class="sxs-lookup"><span data-stu-id="34154-110">Two Lync Server 2013 Front Ends in Enterprise Edition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34154-111">60 000 utilisateurs simultanés sur trois serveurs de discussion de groupe.</span><span class="sxs-lookup"><span data-stu-id="34154-111">60,000 concurrent users across three Group Chat Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34154-112">canaux 25 000 hébergés par une liste de discussion de groupe.</span><span class="sxs-lookup"><span data-stu-id="34154-112">25,000 channels hosted by Group Chat Pool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34154-113">Taille du canal :</span><span class="sxs-lookup"><span data-stu-id="34154-113">Channel Size:</span></span></p>
<ul>
<li><p><span data-ttu-id="34154-114">Taille du petit canal : 30</span><span class="sxs-lookup"><span data-stu-id="34154-114">Small Channel Size: 30</span></span></p></li>
<li><p><span data-ttu-id="34154-115">Taille du canal moyen : 150</span><span class="sxs-lookup"><span data-stu-id="34154-115">Medium Channel Size: 150</span></span></p></li>
<li><p><span data-ttu-id="34154-116">Grande taille de canal : 2500</span><span class="sxs-lookup"><span data-stu-id="34154-116">Large Channel Size: 2500</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34154-117">Nombre de canaux :</span><span class="sxs-lookup"><span data-stu-id="34154-117">Channel Count:</span></span></p>
<ul>
<li><p><span data-ttu-id="34154-118">Nombre de petits canaux : 24 000</span><span class="sxs-lookup"><span data-stu-id="34154-118">Number small channels: 24,000</span></span></p></li>
<li><p><span data-ttu-id="34154-119">Canaux de moyenne numérique 800</span><span class="sxs-lookup"><span data-stu-id="34154-119">Number medium channels 800</span></span></p></li>
<li><p><span data-ttu-id="34154-120">Nombre de canaux de grande taille 24</span><span class="sxs-lookup"><span data-stu-id="34154-120">Number large channels 24</span></span></p></li>
<li><p><span data-ttu-id="34154-121">Nombre total de canaux 24 824</span><span class="sxs-lookup"><span data-stu-id="34154-121">Total Channels 24,824</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34154-122">Canaux d’invitation :</span><span class="sxs-lookup"><span data-stu-id="34154-122">Invite channels:</span></span></p>
<ul>
<li><p><span data-ttu-id="34154-123">La moitié des canaux étaient des canaux d’invitation</span><span class="sxs-lookup"><span data-stu-id="34154-123">Half the channels were invite channels</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34154-124">Nombre de canaux qu’un utilisateur rejoint :</span><span class="sxs-lookup"><span data-stu-id="34154-124">Number of channels a user joins:</span></span></p>
<ul>
<li><p><span data-ttu-id="34154-125">Petites : 12</span><span class="sxs-lookup"><span data-stu-id="34154-125">Small: 12</span></span></p></li>
<li><p><span data-ttu-id="34154-126">Moyenne : 2</span><span class="sxs-lookup"><span data-stu-id="34154-126">Medium: 2</span></span></p></li>
<li><p><span data-ttu-id="34154-127">Grande : 1</span><span class="sxs-lookup"><span data-stu-id="34154-127">Large: 1</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34154-128">Taux de participation :</span><span class="sxs-lookup"><span data-stu-id="34154-128">Join rate:</span></span></p>
<ul>
<li><p><span data-ttu-id="34154-129">10 au total/par seconde, 3,33 secondes par serveur</span><span class="sxs-lookup"><span data-stu-id="34154-129">10 total/second, 3.33/second per server</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34154-130">Taux de connexion :</span><span class="sxs-lookup"><span data-stu-id="34154-130">Logout rate:</span></span></p>
<ul>
<li><p><span data-ttu-id="34154-131">10 au total/par seconde, 3,33 secondes par serveur</span><span class="sxs-lookup"><span data-stu-id="34154-131">10 total/second, 3.33/second per server</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34154-132">Taux de conversation :</span><span class="sxs-lookup"><span data-stu-id="34154-132">Chat rate:</span></span></p>
<ul>
<li><p><span data-ttu-id="34154-133">20 au total/par seconde, 6.66/seconde par serveur</span><span class="sxs-lookup"><span data-stu-id="34154-133">20 total/second, 6.66/second per server</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <span data-ttu-id="34154-134">Les numéros de compteurs de performance suivants peuvent varier en fonction du matériel utilisé.</span><span class="sxs-lookup"><span data-stu-id="34154-134">The following performance counter numbers will likely vary when different hardware specifications or user profiles are used.</span></span>



</div>

### <a name="performance-counter-to-be-monitored"></a><span data-ttu-id="34154-135">Compteur de performance à surveiller</span><span class="sxs-lookup"><span data-stu-id="34154-135">Performance counter to be monitored</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34154-136">Compteur de performance</span><span class="sxs-lookup"><span data-stu-id="34154-136">Performance Counter</span></span></th>
<th><span data-ttu-id="34154-137">Seuil</span><span class="sxs-lookup"><span data-stu-id="34154-137">Thresholds</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34154-138">Processus (ChannelService)- &gt; % temps processeur</span><span class="sxs-lookup"><span data-stu-id="34154-138">Process(ChannelService)-&gt;%Processor Time</span></span></p></td>
<td><p><span data-ttu-id="34154-139">Min : 0</span><span class="sxs-lookup"><span data-stu-id="34154-139">Min: 0</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="34154-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="34154-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

