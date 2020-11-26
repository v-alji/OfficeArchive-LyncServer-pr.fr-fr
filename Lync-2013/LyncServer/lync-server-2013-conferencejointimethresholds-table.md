---
title: 'Tableau Lync Server 2013 : ConferenceJoinTimeThresholds'
description: 'Tableau Lync Server 2013 : ConferenceJoinTimeThresholds'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceJoinTimeThresholds table
ms:assetid: 3944d724-bdd8-4d1c-a2af-933ee8141529
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204809(v=OCS.15)
ms:contentKeyID: 48183855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e38c8b99f444e16309882b6a8885d166fdceb9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434458"
---
# <a name="conferencejointimethresholds-table-in-lync-server-2013"></a><span data-ttu-id="b4425-103">Table ConferenceJoinTimeThresholds dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b4425-103">ConferenceJoinTimeThresholds table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b4425-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b4425-104">

<span> </span></span></span>

<span data-ttu-id="b4425-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="b4425-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="b4425-106">La table ConferenceJoinTimeThresholds contient les limites de classification utilisées par le rapport de synthèse des heures de participation à la Conférence.</span><span class="sxs-lookup"><span data-stu-id="b4425-106">The ConferenceJoinTimeThresholds table contains the classification boundaries used by the Conference Join Time Summary Report.</span></span> <span data-ttu-id="b4425-107">Le rapport Résumé de l’heure de la Conférence résume le temps nécessaire pour que les utilisateurs puissent rejoindre une conférence ; ces valeurs d’heure sont communiquées tant en moyenne qu’à l’une des catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="b4425-107">The Conference Join Time Summary Report summarizes the amount time required for users to successfully join a conference; these time values are reported both as an average and in one of the following categories:</span></span>

  - <span data-ttu-id="b4425-108">Moins de 2 secondes.</span><span class="sxs-lookup"><span data-stu-id="b4425-108">Less than 2 seconds.</span></span>

  - <span data-ttu-id="b4425-109">Entre 2 secondes et 5 secondes.</span><span class="sxs-lookup"><span data-stu-id="b4425-109">Between 2 second and 5 seconds.</span></span>

  - <span data-ttu-id="b4425-110">Entre 5 et 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="b4425-110">Between 5 seconds and 10 seconds.</span></span>

  - <span data-ttu-id="b4425-111">Plus de 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="b4425-111">More than 10 seconds.</span></span>

<span data-ttu-id="b4425-112">La table ConferenceJoinTimeThresholds contient les valeurs de classification 2 secondes, 5 secondes et 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="b4425-112">The ConferenceJoinTimeThresholds table contains the classification values 2 seconds, 5 seconds, and 10 seconds.</span></span>

<span data-ttu-id="b4425-113">Ce tableau a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b4425-113">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4425-114">Colonne</span><span class="sxs-lookup"><span data-stu-id="b4425-114">Column</span></span></th>
<th><span data-ttu-id="b4425-115">Type de données</span><span class="sxs-lookup"><span data-stu-id="b4425-115">Data Type</span></span></th>
<th><span data-ttu-id="b4425-116">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="b4425-116">Key/Index</span></span></th>
<th><span data-ttu-id="b4425-117">Détails</span><span class="sxs-lookup"><span data-stu-id="b4425-117">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4425-118"><strong>ThresholdId</strong></span><span class="sxs-lookup"><span data-stu-id="b4425-118"><strong>ThresholdId</strong></span></span></p></td>
<td><p><span data-ttu-id="b4425-119">int</span><span class="sxs-lookup"><span data-stu-id="b4425-119">int</span></span></p></td>
<td><p><span data-ttu-id="b4425-120">Principal</span><span class="sxs-lookup"><span data-stu-id="b4425-120">Primary</span></span></p></td>
<td><p><span data-ttu-id="b4425-121">Identificateur unique de la classification.</span><span class="sxs-lookup"><span data-stu-id="b4425-121">Unique identifier for the classification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4425-122"><strong>ThresholdValue</strong></span><span class="sxs-lookup"><span data-stu-id="b4425-122"><strong>ThresholdValue</strong></span></span></p></td>
<td><p><span data-ttu-id="b4425-123">int</span><span class="sxs-lookup"><span data-stu-id="b4425-123">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b4425-124">Limite supérieure de la classification.</span><span class="sxs-lookup"><span data-stu-id="b4425-124">Upper limit for the classification.</span></span> <span data-ttu-id="b4425-125">Les valeurs autorisées sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b4425-125">Allowed values are:</span></span></p>
<ol>
<li><p><span data-ttu-id="b4425-126">2</span><span class="sxs-lookup"><span data-stu-id="b4425-126">2</span></span></p></li>
<li><p><span data-ttu-id="b4425-127">5</span><span class="sxs-lookup"><span data-stu-id="b4425-127">5</span></span></p></li>
<li><p><span data-ttu-id="b4425-128">0,10</span><span class="sxs-lookup"><span data-stu-id="b4425-128">10</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table><span data-ttu-id="b4425-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b4425-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

