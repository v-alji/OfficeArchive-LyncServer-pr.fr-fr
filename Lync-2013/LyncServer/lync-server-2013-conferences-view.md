---
title: 'Lync Server 2013 : vue conférences'
description: 'Lync Server 2013 : vue conférences.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferences view
ms:assetid: c0e5c4db-c135-401f-9296-e9a49f6499a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721871(v=OCS.15)
ms:contentKeyID: 49733803
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dee7fbb7c839c351fc9c81716a5800a678980549
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434423"
---
# <a name="conferences-view-in-lync-server-2013"></a><span data-ttu-id="cee85-103">Affichage conférences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cee85-103">Conferences view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cee85-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cee85-104">

<span> </span></span></span>

<span data-ttu-id="cee85-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="cee85-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="cee85-106">L’affichage conférences stocke les informations relatives aux conférences.</span><span class="sxs-lookup"><span data-stu-id="cee85-106">The Conferences View stores information about the conferences.</span></span> <span data-ttu-id="cee85-107">Cet affichage a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cee85-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cee85-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="cee85-108">Column</span></span></th>
<th><span data-ttu-id="cee85-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="cee85-109">Data Type</span></span></th>
<th><span data-ttu-id="cee85-110">Détails</span><span class="sxs-lookup"><span data-stu-id="cee85-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cee85-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="cee85-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="cee85-112">DateHeure</span><span class="sxs-lookup"><span data-stu-id="cee85-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="cee85-113">Durée de la demande de session.</span><span class="sxs-lookup"><span data-stu-id="cee85-113">Time of session request.</span></span> <span data-ttu-id="cee85-114">Utilisé conjointement avec SessionIdSeq pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="cee85-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="cee85-115">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cee85-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cee85-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="cee85-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="cee85-117">int</span><span class="sxs-lookup"><span data-stu-id="cee85-117">int</span></span></p></td>
<td><p><span data-ttu-id="cee85-118">IDENTIFIant de la session.</span><span class="sxs-lookup"><span data-stu-id="cee85-118">ID number to identify the session.</span></span> <span data-ttu-id="cee85-119">Utilisé conjointement avec SessionIdTime pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="cee85-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="cee85-120">Pour plus d’informations, voir le <a href="lync-server-2013-dialogs-table.md">tableau des boîtes de dialogue dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cee85-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cee85-121"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="cee85-121"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="cee85-122">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="cee85-122">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="cee85-123">URI de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="cee85-123">URI for the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cee85-124"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="cee85-124"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="cee85-125">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cee85-125">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cee85-126">Type de l’URI de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="cee85-126">Type of the conference URI.</span></span> <span data-ttu-id="cee85-127">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cee85-127">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cee85-128"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="cee85-128"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="cee85-129">identificateur</span><span class="sxs-lookup"><span data-stu-id="cee85-129">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="cee85-130">Utilisé pour les conférences récurrentes.</span><span class="sxs-lookup"><span data-stu-id="cee85-130">Used for recurring conferences.</span></span> <span data-ttu-id="cee85-131">Chaque instance d’une conférence périodique a le même ConferenceUri qu’une autre ConfInstance.</span><span class="sxs-lookup"><span data-stu-id="cee85-131">Each instance of a recurring conference has the same ConferenceUri but a different ConfInstance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cee85-132"><strong>ConferenceStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="cee85-132"><strong>ConferenceStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="cee85-133">DateHeure</span><span class="sxs-lookup"><span data-stu-id="cee85-133">datetime</span></span></p></td>
<td><p><span data-ttu-id="cee85-134">Heure de début de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="cee85-134">Starting time for the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cee85-135"><strong>ConferenceEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="cee85-135"><strong>ConferenceEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="cee85-136">DateHeure</span><span class="sxs-lookup"><span data-stu-id="cee85-136">datetime</span></span></p></td>
<td><p><span data-ttu-id="cee85-137">Heure de fin de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="cee85-137">Ending time for the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cee85-138"><strong>OrganizerUri</strong></span><span class="sxs-lookup"><span data-stu-id="cee85-138"><strong>OrganizerUri</strong></span></span></p></td>
<td><p><span data-ttu-id="cee85-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="cee85-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="cee85-140">URI de l’utilisateur qui a organisé la Conférence.</span><span class="sxs-lookup"><span data-stu-id="cee85-140">URI of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cee85-141"><strong>OrganizerType</strong></span><span class="sxs-lookup"><span data-stu-id="cee85-141"><strong>OrganizerType</strong></span></span></p></td>
<td><p><span data-ttu-id="cee85-142">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cee85-142">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cee85-143">Type d’URI de l’utilisateur qui a organisé la Conférence.</span><span class="sxs-lookup"><span data-stu-id="cee85-143">Type of URI of the user who organized the conference.</span></span> <span data-ttu-id="cee85-144">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cee85-144">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cee85-145"><strong>OrganizerTenant</strong></span><span class="sxs-lookup"><span data-stu-id="cee85-145"><strong>OrganizerTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="cee85-146">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cee85-146">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cee85-147">Client de l’utilisateur qui a organisé la Conférence.</span><span class="sxs-lookup"><span data-stu-id="cee85-147">Tenant of the user who organized the conference.</span></span> <span data-ttu-id="cee85-148">Pour plus d’informations, voir la <a href="lync-server-2013-tenants-table.md">table locataires dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cee85-148">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cee85-149"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="cee85-149"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="cee85-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cee85-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cee85-151">Nom de domaine complet du pool ayant hébergé la Conférence.</span><span class="sxs-lookup"><span data-stu-id="cee85-151">Fully qualified domain name of the pool that hosted the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cee85-152"><strong>Indication</strong></span><span class="sxs-lookup"><span data-stu-id="cee85-152"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="cee85-153">type</span><span class="sxs-lookup"><span data-stu-id="cee85-153">smallint</span></span></p></td>
<td><p><span data-ttu-id="cee85-154">Masque binaire qui contient les attributs de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="cee85-154">Bit mask that contains Conference Attributes.</span></span> <span data-ttu-id="cee85-155">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="cee85-155">Possible values are:</span></span></p>
<p><span data-ttu-id="cee85-156">0X01 – transaction synthétique</span><span class="sxs-lookup"><span data-stu-id="cee85-156">0X01 – Synthetic Transaction</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="cee85-157">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cee85-157">


</div>

<span> </span>

</div>

</div>

</span></span></div>

