---
title: 'Lync Server 2013 : Table ErrorDef'
description: 'Tableau Lync Server 2013 : ErrorDef'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorDef table
ms:assetid: 6acf3b86-da61-4923-9812-300db6f66dec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398503(v=OCS.15)
ms:contentKeyID: 48184403
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e58980a671b54007012bbbf6780e24c162aebe00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428537"
---
# <a name="errordef-table-in-lync-server-2013"></a><span data-ttu-id="ce725-103">Table ErrorDef dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce725-103">ErrorDef table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ce725-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ce725-104">

<span> </span></span></span>

<span data-ttu-id="ce725-105">_**Dernière modification de la rubrique :** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="ce725-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="ce725-106">La table ErrorDef stocke des informations sur chaque type d’erreur pouvant se produire.</span><span class="sxs-lookup"><span data-stu-id="ce725-106">The ErrorDef table stores information about each type of error that may occur.</span></span> <span data-ttu-id="ce725-107">Chaque enregistrement correspond à un type d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ce725-107">Each record is one type of error.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce725-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="ce725-108">Column</span></span></th>
<th><span data-ttu-id="ce725-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce725-109">Data Type</span></span></th>
<th><span data-ttu-id="ce725-110">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="ce725-110">Key/Index</span></span></th>
<th><span data-ttu-id="ce725-111">Détails</span><span class="sxs-lookup"><span data-stu-id="ce725-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce725-112"><strong>ErrorId</strong></span><span class="sxs-lookup"><span data-stu-id="ce725-112"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="ce725-113">int</span><span class="sxs-lookup"><span data-stu-id="ce725-113">int</span></span></p></td>
<td><p><span data-ttu-id="ce725-114">Principal</span><span class="sxs-lookup"><span data-stu-id="ce725-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="ce725-115">Numéro d’identification unique identifiant ce type d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ce725-115">Unique ID number identifying this type of error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce725-116"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="ce725-116"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="ce725-117">int</span><span class="sxs-lookup"><span data-stu-id="ce725-117">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ce725-118">Code de réponse SIP standard associé à cette erreur.</span><span class="sxs-lookup"><span data-stu-id="ce725-118">Standard SIP response code associated with this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce725-119"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="ce725-119"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="ce725-120">int</span><span class="sxs-lookup"><span data-stu-id="ce725-120">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ce725-121">ID de diagnostic Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ce725-121">Microsoft Diagnostic ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce725-122"><strong>CallTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="ce725-122"><strong>CallTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="ce725-123">Ent</span><span class="sxs-lookup"><span data-stu-id="ce725-123">Int</span></span></p></td>
<td><p><span data-ttu-id="ce725-124">Externes</span><span class="sxs-lookup"><span data-stu-id="ce725-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ce725-125">Type de l’appel.</span><span class="sxs-lookup"><span data-stu-id="ce725-125">Type of the call.</span></span> <span data-ttu-id="ce725-126">Pour plus d’informations, voir la <a href="lync-server-2013-calltype-table.md">table CallType dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="ce725-126">See the <a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce725-127"><strong>RequestType</strong></span><span class="sxs-lookup"><span data-stu-id="ce725-127"><strong>RequestType</strong></span></span></p></td>
<td><p><span data-ttu-id="ce725-128">varbinary (33)</span><span class="sxs-lookup"><span data-stu-id="ce725-128">varbinary(33)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ce725-129">Type de requête ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="ce725-129">Type of request that failed.</span></span></p>
<p><span data-ttu-id="ce725-130">Vous pouvez convertir ces données en format texte à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="ce725-130">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(RequestType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce725-131"><strong>Indiquez</strong></span><span class="sxs-lookup"><span data-stu-id="ce725-131"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="ce725-132">varbinary (257)</span><span class="sxs-lookup"><span data-stu-id="ce725-132">varbinary(257)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ce725-133">Type de contenu de la requête qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="ce725-133">Content type of the request that failed.</span></span></p>
<p><span data-ttu-id="ce725-134">Vous pouvez convertir ces données en format texte à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="ce725-134">This data can be converted to text format by using this syntaxt:</span></span></p>
<p><code>cast(cast(ContentType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ce725-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ce725-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

