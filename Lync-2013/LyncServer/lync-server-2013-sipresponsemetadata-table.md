---
title: 'Tableau Lync Server 2013 : SIPResponseMetaData'
description: 'Tableau Lync Server 2013 : SIPResponseMetaData'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SIPResponseMetaData table
ms:assetid: cf723737-4a75-4352-829b-f4954aa59716
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205294(v=OCS.15)
ms:contentKeyID: 48185510
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 402cff331f81a9b46028d76de69deeaace8d5ae1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444622"
---
# <a name="sipresponsemetadata-table-in-lync-server-2013"></a><span data-ttu-id="0ef4d-103">Table SIPResponseMetaData dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ef4d-103">SIPResponseMetaData table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0ef4d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0ef4d-104">

<span> </span></span></span>

<span data-ttu-id="0ef4d-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="0ef4d-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="0ef4d-106">Le SIPResponseMetaDataTable contient une liste des codes de réponse SIP et la classification et la définition de chacun de ces codes.</span><span class="sxs-lookup"><span data-stu-id="0ef4d-106">The SIPResponseMetaDataTable contains a list of SIP response codes and the classification and definition of each of those codes.</span></span> <span data-ttu-id="0ef4d-107">Ces codes sont générés en réponse à des événements affectant des périphériques SIP et des sessions de communication SIP ; par exemple, le code de réponse 403 est généré lorsqu’un périphérique SIP envoie une demande, mais que le serveur décline la demande.</span><span class="sxs-lookup"><span data-stu-id="0ef4d-107">These codes are generated in response to events affecting SIP devices and SIP communication sessions; for example, the response code 403 is generated when a SIP device makes a request, but the server declines to honor that request.</span></span>

<span data-ttu-id="0ef4d-108">Ce tableau a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ef4d-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ef4d-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="0ef4d-109">Column</span></span></th>
<th><span data-ttu-id="0ef4d-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="0ef4d-110">Data Type</span></span></th>
<th><span data-ttu-id="0ef4d-111">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="0ef4d-111">Key/Index</span></span></th>
<th><span data-ttu-id="0ef4d-112">Détails</span><span class="sxs-lookup"><span data-stu-id="0ef4d-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ef4d-113"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="0ef4d-113"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="0ef4d-114">int</span><span class="sxs-lookup"><span data-stu-id="0ef4d-114">int</span></span></p></td>
<td><p><span data-ttu-id="0ef4d-115">Principal</span><span class="sxs-lookup"><span data-stu-id="0ef4d-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="0ef4d-116">Valeur numérique qui représente le code de réponse SIP.</span><span class="sxs-lookup"><span data-stu-id="0ef4d-116">Numeric value that represents the SIP response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ef4d-117"><strong>Cours</strong></span><span class="sxs-lookup"><span data-stu-id="0ef4d-117"><strong>Class</strong></span></span></p></td>
<td><p><span data-ttu-id="0ef4d-118">int</span><span class="sxs-lookup"><span data-stu-id="0ef4d-118">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ef4d-119">Classification générale du code de réponse.</span><span class="sxs-lookup"><span data-stu-id="0ef4d-119">General classification for the response code.</span></span> <span data-ttu-id="0ef4d-120">Les classifications sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0ef4d-120">Classifications include:</span></span></p>
<ul>
<li><p><span data-ttu-id="0ef4d-121">1 – réponses d’information</span><span class="sxs-lookup"><span data-stu-id="0ef4d-121">1 – Informational Responses</span></span></p></li>
<li><p><span data-ttu-id="0ef4d-122">2 – réponses réussies</span><span class="sxs-lookup"><span data-stu-id="0ef4d-122">2 – Successful Responses</span></span></p></li>
<li><p><span data-ttu-id="0ef4d-123">3 – réponses de redirection</span><span class="sxs-lookup"><span data-stu-id="0ef4d-123">3 – Redirection Responses</span></span></p></li>
<li><p><span data-ttu-id="0ef4d-124">4 – réponses d’échec client</span><span class="sxs-lookup"><span data-stu-id="0ef4d-124">4 – Client Failure Responses</span></span></p></li>
<li><p><span data-ttu-id="0ef4d-125">5 réponses aux échecs sur le serveur</span><span class="sxs-lookup"><span data-stu-id="0ef4d-125">5 -- Server Failure Responses</span></span></p></li>
<li><p><span data-ttu-id="0ef4d-126">6-réponse d’échec globale</span><span class="sxs-lookup"><span data-stu-id="0ef4d-126">6 – Global Failure Response</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ef4d-127"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="0ef4d-127"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="0ef4d-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0ef4d-128">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0ef4d-129">Description du code de réponse SIP.</span><span class="sxs-lookup"><span data-stu-id="0ef4d-129">Description of the SIP response code.</span></span> <span data-ttu-id="0ef4d-130">Par exemple, le code de réponse 181 contient la description suivante :</span><span class="sxs-lookup"><span data-stu-id="0ef4d-130">For example, response code 181 has the following description:</span></span></p>
<p><span data-ttu-id="0ef4d-131">Appel en cours de transfert</span><span class="sxs-lookup"><span data-stu-id="0ef4d-131">Call Is Being Forwarded</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0ef4d-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0ef4d-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

