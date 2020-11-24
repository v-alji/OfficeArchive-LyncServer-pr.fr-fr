---
title: 'Lync Server 2013 : Planification de capacité pour le parcage d’appel'
description: 'Lync Server 2013 : planification de la capacité pour le parc d’appels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning for Call Park
ms:assetid: 75520310-760a-4b1b-bcc1-4d724d13f87a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg416493(v=OCS.15)
ms:contentKeyID: 48184529
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 053a6dabad9d10540e84e9e4f43de09057c295f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395161"
---
# <a name="capacity-planning-for-call-park-in-lync-server-2013"></a><span data-ttu-id="a1da5-103">Planification de capacité pour le parcage d’appel dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a1da5-103">Capacity planning for Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a1da5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a1da5-104">

<span> </span></span></span>

<span data-ttu-id="a1da5-105">_**Dernière modification de la rubrique :** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="a1da5-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<div id="sectionSection0" class="section">

<span data-ttu-id="a1da5-106">Le tableau suivant décrit le modèle d’utilisateur de parc d’appels que vous pouvez utiliser comme base pour les exigences de planification de capacité.</span><span class="sxs-lookup"><span data-stu-id="a1da5-106">The following table describes the Call Park user model that you can use as the basis for capacity planning requirements.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a1da5-107">Gardez à l’esprit que pour la planification de la capacité de reprise après sinistre, chaque pool d’un pool couplé doit être en mesure de gérer les charges de travail des services de parc d’appels dans les deux pools.</span><span class="sxs-lookup"><span data-stu-id="a1da5-107">Keep in mind that, for disaster recovery capacity planning, each pool of a paired pool should be able to handle the workloads for Call Park services in both pools.</span></span>



</div>

### <a name="call-park-user-model"></a><span data-ttu-id="a1da5-108">Modèle utilisateur de parcage d’appel</span><span class="sxs-lookup"><span data-stu-id="a1da5-108">Call Park User Model</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a1da5-109">Mesure</span><span class="sxs-lookup"><span data-stu-id="a1da5-109">Metric</span></span></th>
<th><span data-ttu-id="a1da5-110">Par pool frontal (avec 8 serveurs frontaux)</span><span class="sxs-lookup"><span data-stu-id="a1da5-110">Per Front End pool (with 8 Front End Servers)</span></span></th>
<th><span data-ttu-id="a1da5-111">Par serveur Standard Edition</span><span class="sxs-lookup"><span data-stu-id="a1da5-111">Per Standard Edition server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1da5-112">Taux de parcage</span><span class="sxs-lookup"><span data-stu-id="a1da5-112">Park rate</span></span></p></td>
<td><p><span data-ttu-id="a1da5-113">8 par minute</span><span class="sxs-lookup"><span data-stu-id="a1da5-113">8 per minute</span></span></p></td>
<td><p><span data-ttu-id="a1da5-114">1 par minute</span><span class="sxs-lookup"><span data-stu-id="a1da5-114">1 per minute</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1da5-115">Taux d’appels parqués récupérés</span><span class="sxs-lookup"><span data-stu-id="a1da5-115">Retrieve parked call rate</span></span></p></td>
<td><p><span data-ttu-id="a1da5-116">8 par minute</span><span class="sxs-lookup"><span data-stu-id="a1da5-116">8 per minute</span></span></p></td>
<td><p><span data-ttu-id="a1da5-117">1 par minute</span><span class="sxs-lookup"><span data-stu-id="a1da5-117">1 per minute</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1da5-118">Durée moyenne de parcage</span><span class="sxs-lookup"><span data-stu-id="a1da5-118">Average park duration</span></span></p></td>
<td><p><span data-ttu-id="a1da5-119">60 secondes</span><span class="sxs-lookup"><span data-stu-id="a1da5-119">60 seconds</span></span></p></td>
<td><p><span data-ttu-id="a1da5-120">60 secondes</span><span class="sxs-lookup"><span data-stu-id="a1da5-120">60 seconds</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a1da5-121">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a1da5-121">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

