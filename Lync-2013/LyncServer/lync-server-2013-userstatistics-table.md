---
title: 'Tableau Lync Server 2013 : UserStatistics'
description: 'Tableau Lync Server 2013 : UserStatistics'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserStatistics table
ms:assetid: cfaf803b-1679-4169-92d3-533fad3e56ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721893(v=OCS.15)
ms:contentKeyID: 49733827
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 75b34fa3c34af4cc9cf2cacc6ae7feb4d217114c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436096"
---
# <a name="userstatistics-table-in-lync-server-2013"></a><span data-ttu-id="8d6e0-103">Table UserStatistics dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8d6e0-103">UserStatistics table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8d6e0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8d6e0-104">

<span> </span></span></span>

<span data-ttu-id="8d6e0-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="8d6e0-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="8d6e0-106">La table UserStatistics est une table de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8d6e0-106">The UserStatistics table is a supporting table.</span></span> <span data-ttu-id="8d6e0-107">Chaque enregistrement de la table stocke des informations sur l’utilisation individuelle du système par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8d6e0-107">Each record in the table stores information about an individual user’s usage of the system.</span></span> <span data-ttu-id="8d6e0-108">Ce tableau a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8d6e0-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8d6e0-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="8d6e0-109">Column</span></span></th>
<th><span data-ttu-id="8d6e0-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="8d6e0-110">Data Type</span></span></th>
<th><span data-ttu-id="8d6e0-111">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="8d6e0-111">Key/Index</span></span></th>
<th><span data-ttu-id="8d6e0-112">Détails</span><span class="sxs-lookup"><span data-stu-id="8d6e0-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d6e0-113"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="8d6e0-113"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="8d6e0-114">int</span><span class="sxs-lookup"><span data-stu-id="8d6e0-114">int</span></span></p></td>
<td><p><span data-ttu-id="8d6e0-115">Principal</span><span class="sxs-lookup"><span data-stu-id="8d6e0-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="8d6e0-116">Numéro unique identifiant cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8d6e0-116">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d6e0-117"><strong>LastLogInTime</strong></span><span class="sxs-lookup"><span data-stu-id="8d6e0-117"><strong>LastLogInTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8d6e0-118">DateHeure</span><span class="sxs-lookup"><span data-stu-id="8d6e0-118">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8d6e0-119">Dernière connexion de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8d6e0-119">Last time the user logged in.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d6e0-120"><strong>LastConfOrganizedTime</strong></span><span class="sxs-lookup"><span data-stu-id="8d6e0-120"><strong>LastConfOrganizedTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8d6e0-121">DateHeure</span><span class="sxs-lookup"><span data-stu-id="8d6e0-121">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8d6e0-122">Dernière organisation d’une conférence.</span><span class="sxs-lookup"><span data-stu-id="8d6e0-122">Last time the user organized a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d6e0-123"><strong>LastCallOrganizerCallFailureTime</strong></span><span class="sxs-lookup"><span data-stu-id="8d6e0-123"><strong>LastCallOrganizerCallFailureTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8d6e0-124">DateHeure</span><span class="sxs-lookup"><span data-stu-id="8d6e0-124">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8d6e0-125">Dernière fois que l’utilisateur a rencontré un échec de l’appel.</span><span class="sxs-lookup"><span data-stu-id="8d6e0-125">Last time the user experienced a call failure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d6e0-126"><strong>LastConfOrganizerCallFailureTime</strong></span><span class="sxs-lookup"><span data-stu-id="8d6e0-126"><strong>LastConfOrganizerCallFailureTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8d6e0-127">DateHeure</span><span class="sxs-lookup"><span data-stu-id="8d6e0-127">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8d6e0-128">Dernière fois que l’utilisateur a rencontré un appel d’organisateur en tant qu’organisateur de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="8d6e0-128">Last time the user experienced a call failure as a conference organizer.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8d6e0-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8d6e0-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

