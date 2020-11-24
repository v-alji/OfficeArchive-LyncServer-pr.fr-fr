---
title: 'Lync Server 2013 : Table Conferences'
description: 'Tableau Lync Server 2013 : conférences.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferences table
ms:assetid: c3da6271-b3c6-4898-894f-10456ec794d0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412964(v=OCS.15)
ms:contentKeyID: 48185340
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e0d8c61e795dc0c8f9843b871d7e4efd1bec571
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394781"
---
# <a name="conferences-table-in-lync-server-2013"></a><span data-ttu-id="cd66d-103">Table Conferences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd66d-103">Conferences table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cd66d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cd66d-104">

<span> </span></span></span>

<span data-ttu-id="cd66d-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="cd66d-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="cd66d-106">Chaque enregistrement de cette table contient les détails des appels sur une conférence.</span><span class="sxs-lookup"><span data-stu-id="cd66d-106">Each record in this table contains call details about one conference.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cd66d-107">Colonne</span><span class="sxs-lookup"><span data-stu-id="cd66d-107">Column</span></span></th>
<th><span data-ttu-id="cd66d-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="cd66d-108">Data Type</span></span></th>
<th><span data-ttu-id="cd66d-109">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="cd66d-109">Key/Index</span></span></th>
<th><span data-ttu-id="cd66d-110">Détails</span><span class="sxs-lookup"><span data-stu-id="cd66d-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd66d-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="cd66d-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="cd66d-112">DateHeure</span><span class="sxs-lookup"><span data-stu-id="cd66d-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="cd66d-113">Principal</span><span class="sxs-lookup"><span data-stu-id="cd66d-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="cd66d-114">Temps d’acquisition de la demande de conférence par l’agent CDR.</span><span class="sxs-lookup"><span data-stu-id="cd66d-114">Time that the conference request was captured by the CDR agent.</span></span> <span data-ttu-id="cd66d-115">Utilisé uniquement comme clé primaire pour identifier de manière unique une instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="cd66d-115">Used only as a primary key to uniquely identify a conference instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd66d-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="cd66d-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="cd66d-117">int</span><span class="sxs-lookup"><span data-stu-id="cd66d-117">int</span></span></p></td>
<td><p><span data-ttu-id="cd66d-118">Principal</span><span class="sxs-lookup"><span data-stu-id="cd66d-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="cd66d-119">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="cd66d-119">ID number to identify the session.</span></span> <span data-ttu-id="cd66d-120">Utilisé conjointement avec <strong>SessionIdTime</strong> pour identifier de manière unique une instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="cd66d-120">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> *</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd66d-121"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="cd66d-121"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="cd66d-122">int</span><span class="sxs-lookup"><span data-stu-id="cd66d-122">int</span></span></p></td>
<td><p><span data-ttu-id="cd66d-123">Externes</span><span class="sxs-lookup"><span data-stu-id="cd66d-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="cd66d-124">URI de conférence.</span><span class="sxs-lookup"><span data-stu-id="cd66d-124">Conference URI.</span></span> <span data-ttu-id="cd66d-125">Pour plus d’informations, voir la <a href="lync-server-2013-conferenceuris-table.md">table ConferenceUris dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cd66d-125">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd66d-126"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="cd66d-126"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="cd66d-127">identificateur</span><span class="sxs-lookup"><span data-stu-id="cd66d-127">uniqueidentifier</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="cd66d-128">Utile pour les conférences récurrentes ; chaque instance d’une conférence périodique a le même <strong>ConferenceUri</strong>, mais aura un autre <strong>ConfInstance</strong>.</span><span class="sxs-lookup"><span data-stu-id="cd66d-128">Useful for recurring conferences; each instance of a recurring conference has the same <strong>ConferenceUri</strong>, but will have a different <strong>ConfInstance</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd66d-129"><strong>ConferenceStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="cd66d-129"><strong>ConferenceStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="cd66d-130">DateHeure</span><span class="sxs-lookup"><span data-stu-id="cd66d-130">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="cd66d-131">Heure de début de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="cd66d-131">Conference start time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd66d-132"><strong>ConferenceEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="cd66d-132"><strong>ConferenceEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="cd66d-133">DateHeure</span><span class="sxs-lookup"><span data-stu-id="cd66d-133">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="cd66d-134">Heure de début de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="cd66d-134">Conference start time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd66d-135"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="cd66d-135"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="cd66d-136">int</span><span class="sxs-lookup"><span data-stu-id="cd66d-136">int</span></span></p></td>
<td><p><span data-ttu-id="cd66d-137">Externes</span><span class="sxs-lookup"><span data-stu-id="cd66d-137">Foreign</span></span></p></td>
<td><p><span data-ttu-id="cd66d-138">Numéro d’identification identifiant le regroupement dans lequel la Conférence a été capturée.</span><span class="sxs-lookup"><span data-stu-id="cd66d-138">ID number to identify the pool in which the conference was captured.</span></span> <span data-ttu-id="cd66d-139">Pour plus d’informations, voir la <a href="lync-server-2013-pools-table.md">table pools dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cd66d-139">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd66d-140"><strong>OrganizerId</strong></span><span class="sxs-lookup"><span data-stu-id="cd66d-140"><strong>OrganizerId</strong></span></span></p></td>
<td><p><span data-ttu-id="cd66d-141">Ent</span><span class="sxs-lookup"><span data-stu-id="cd66d-141">Int</span></span></p></td>
<td><p><span data-ttu-id="cd66d-142">Externes</span><span class="sxs-lookup"><span data-stu-id="cd66d-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="cd66d-143">Numéro d’identification identifiant l’URI organisateur de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="cd66d-143">ID number to identify the organizer URI of this conference.</span></span> <span data-ttu-id="cd66d-144">Pour plus d’informations, consultez le <a href="lync-server-2013-users-table.md">tableau utilisateurs dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cd66d-144">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd66d-145"><strong>Indication</strong></span><span class="sxs-lookup"><span data-stu-id="cd66d-145"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="cd66d-146">type</span><span class="sxs-lookup"><span data-stu-id="cd66d-146">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="cd66d-147">Masque binaire qui contient les attributs de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="cd66d-147">A bit mask that contains Conference Attributes.</span></span> <span data-ttu-id="cd66d-148">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="cd66d-148">Possible values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="cd66d-149">0X01</span><span class="sxs-lookup"><span data-stu-id="cd66d-149">0X01</span></span></p></li>
<li><p><span data-ttu-id="cd66d-150">Synthetic</span><span class="sxs-lookup"><span data-stu-id="cd66d-150">Synthetic</span></span></p></li>
<li><p><span data-ttu-id="cd66d-151">Transaction</span><span class="sxs-lookup"><span data-stu-id="cd66d-151">Transaction</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd66d-152"><strong>Formé</strong></span><span class="sxs-lookup"><span data-stu-id="cd66d-152"><strong>Processed</strong></span></span></p></td>
<td><p><span data-ttu-id="cd66d-153">bit</span><span class="sxs-lookup"><span data-stu-id="cd66d-153">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="cd66d-154">Champ interne utilisé par le service de surveillance.</span><span class="sxs-lookup"><span data-stu-id="cd66d-154">Internal field used by the Monitoring service.</span></span></p>
<p><span data-ttu-id="cd66d-155">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cd66d-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd66d-156">\* Pour la plupart des sessions, SessionIdSeq aura la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="cd66d-156">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="cd66d-157">S’il s’agit d’une session à partir de la même heure, le SessionIdSeq d’une personne sera 1, et pour l’autre, sera égale à 2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="cd66d-157">If two sessions start at exactly the same time, the SessionIdSeq for one will be 1, and for the other will be 2, and so on.</span></span>

<span data-ttu-id="cd66d-158"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cd66d-158"></div>

<span> </span>

</div>

</div>

</span></span></div>

