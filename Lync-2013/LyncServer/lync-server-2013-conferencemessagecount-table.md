---
title: 'Lync Server 2013 : Table ConferenceMessageCount'
description: 'Tableau Lync Server 2013 : ConferenceMessageCount'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceMessageCount table
ms:assetid: 78569dbf-5217-42fa-ba1a-4380f56e2a3d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398590(v=OCS.15)
ms:contentKeyID: 48184570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 271b654c09ab1aef194eb613e660de208aea1534
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434451"
---
# <a name="conferencemessagecount-table-in-lync-server-2013"></a><span data-ttu-id="b665a-103">Table ConferenceMessageCount dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b665a-103">ConferenceMessageCount table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b665a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b665a-104">

<span> </span></span></span>

<span data-ttu-id="b665a-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="b665a-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="b665a-106">Chaque enregistrement de cette table représente un utilisateur au sein d’une conférence par messagerie instantanée et inclut le nombre de messages envoyés par cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b665a-106">Each record in this table represents one user in one IM conference and includes the number of messages sent by that user.</span></span> <span data-ttu-id="b665a-107">Chaque conférence est représentée par plusieurs enregistrements dans ce tableau ; un enregistrement pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b665a-107">Each conference is represented by multiple records in this table; one record for each user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b665a-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="b665a-108">Column</span></span></th>
<th><span data-ttu-id="b665a-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="b665a-109">Data Type</span></span></th>
<th><span data-ttu-id="b665a-110">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="b665a-110">Key/Index</span></span></th>
<th><span data-ttu-id="b665a-111">Détails</span><span class="sxs-lookup"><span data-stu-id="b665a-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b665a-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="b665a-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b665a-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="b665a-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="b665a-114">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="b665a-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="b665a-115">Durée de l’instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="b665a-115">Time of conference instance.</span></span> <span data-ttu-id="b665a-116">Utilisé conjointement avec <strong>SessionIdSeq</strong> pour identifier de manière unique une instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="b665a-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="b665a-117">Pour plus d’informations, voir le <a href="lync-server-2013-conferences-table.md">tableau conférences dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b665a-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b665a-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="b665a-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="b665a-119">int</span><span class="sxs-lookup"><span data-stu-id="b665a-119">int</span></span></p></td>
<td><p><span data-ttu-id="b665a-120">Etranger principal</span><span class="sxs-lookup"><span data-stu-id="b665a-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="b665a-121">Numéro d’identification pour identifier l’instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="b665a-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="b665a-122">Utilisé conjointement avec <strong>SessionIdTime</strong> pour identifier de manière unique une instance de conférence.</span><span class="sxs-lookup"><span data-stu-id="b665a-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="b665a-123">Pour plus d’informations, voir le <a href="lync-server-2013-conferences-table.md">tableau conférences dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b665a-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b665a-124"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="b665a-124"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="b665a-125">int</span><span class="sxs-lookup"><span data-stu-id="b665a-125">int</span></span></p></td>
<td><p><span data-ttu-id="b665a-126">Externes</span><span class="sxs-lookup"><span data-stu-id="b665a-126">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b665a-127">Numéro unique identifiant cet utilisateur, référencé dans la <a href="lync-server-2013-users-table.md">table utilisateurs de Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="b665a-127">Unique number identifying this user, referenced from the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b665a-128"><strong>MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="b665a-128"><strong>MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="b665a-129">type</span><span class="sxs-lookup"><span data-stu-id="b665a-129">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b665a-130">Nombre de messages envoyés par cet utilisateur au cours de cette conférence.</span><span class="sxs-lookup"><span data-stu-id="b665a-130">The number of messages sent by this user during this conference.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b665a-131">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b665a-131">


</div>

<span> </span>

</div>

</div>

</span></span></div>

