---
title: 'Lync Server 2013 : Table Dialog'
description: 'Tableau de boîte de dialogue Lync Server 2013 :'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dialog table
ms:assetid: 4d93424f-9072-43f5-83c2-3d539e3e9ca6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398313(v=OCS.15)
ms:contentKeyID: 48184068
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7ae93b8ca9f1146b7dc164803f27cbeeadc66777
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429202"
---
# <a name="dialog-table-in-lync-server-2013"></a><span data-ttu-id="67d27-103">Table Dialog dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67d27-103">Dialog table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="67d27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="67d27-104">

<span> </span></span></span>

<span data-ttu-id="67d27-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="67d27-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="67d27-106">Le tableau de boîte de dialogue est une table de prise en charge. chaque enregistrement représente une boîte de dialogue SIP (Session Initiation Protocol).</span><span class="sxs-lookup"><span data-stu-id="67d27-106">The Dialog table is a supporting table; each record represents one Session Initiation Protocol (SIP) dialog.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67d27-107"><strong>Colonne</strong></span><span class="sxs-lookup"><span data-stu-id="67d27-107"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="67d27-108"><strong>Type de données</strong></span><span class="sxs-lookup"><span data-stu-id="67d27-108"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="67d27-109"><strong>Clé/Index</strong></span><span class="sxs-lookup"><span data-stu-id="67d27-109"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="67d27-110"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="67d27-110"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67d27-111"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="67d27-111"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="67d27-112">DateHeure</span><span class="sxs-lookup"><span data-stu-id="67d27-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="67d27-113">Principal</span><span class="sxs-lookup"><span data-stu-id="67d27-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="67d27-114">Temps pendant lequel l’agent de qualité d’excellence reçoit le premier rapport de l’appelant ou du destinataire.</span><span class="sxs-lookup"><span data-stu-id="67d27-114">Time when the Quality of Excellence (QoE) agent receives the first report from either caller or callee.</span></span> <span data-ttu-id="67d27-115">Utilisé conjointement avec SessionSeq pour identifier une session de manière unique.</span><span class="sxs-lookup"><span data-stu-id="67d27-115">Used in conjunction with SessionSeq to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67d27-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="67d27-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="67d27-117">int</span><span class="sxs-lookup"><span data-stu-id="67d27-117">int</span></span></p></td>
<td><p><span data-ttu-id="67d27-118">Principal</span><span class="sxs-lookup"><span data-stu-id="67d27-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="67d27-119">Numéro séquentiel pour différencier les sessions lorsqu’elles ont la même ConferenceDateTime.</span><span class="sxs-lookup"><span data-stu-id="67d27-119">Sequence number to differentiate sessions when they have the same ConferenceDateTime.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67d27-120"><strong>DialogID</strong></span><span class="sxs-lookup"><span data-stu-id="67d27-120"><strong>DialogID</strong></span></span></p></td>
<td><p><span data-ttu-id="67d27-121">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="67d27-121">varchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67d27-122">ID de boîte de dialogue globalement unique.</span><span class="sxs-lookup"><span data-stu-id="67d27-122">Dialog ID which is globally unique.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67d27-123"><strong>DialogIDChecksum</strong></span><span class="sxs-lookup"><span data-stu-id="67d27-123"><strong>DialogIDChecksum</strong></span></span></p></td>
<td><p><span data-ttu-id="67d27-124">int</span><span class="sxs-lookup"><span data-stu-id="67d27-124">int</span></span></p></td>
<td><p><span data-ttu-id="67d27-125">index</span><span class="sxs-lookup"><span data-stu-id="67d27-125">index</span></span></p></td>
<td><p><span data-ttu-id="67d27-126">Checksum de l’ID de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="67d27-126">Checksum of the Dialog ID.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="67d27-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="67d27-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

