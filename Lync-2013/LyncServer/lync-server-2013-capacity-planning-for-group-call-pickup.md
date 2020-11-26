---
title: 'Lync Server 2013 : planification de la capacité pour le prélèvement d’appels de groupe'
description: 'Lync Server 2013 : planification de la capacité pour le prélèvement d’appels de groupe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning for Group Call Pickup
ms:assetid: 0d654a19-6cf0-4118-903d-ec2c4e519253
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ984297(v=OCS.15)
ms:contentKeyID: 51476680
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12648c57d1036a0ed27c60ef6399bf570c5dcd3d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435571"
---
# <a name="capacity-planning-for-group-call-pickup-in-lync-server-2013"></a><span data-ttu-id="edce4-103">Planification de la capacité pour le prélèvement d’appels de groupe dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="edce4-103">Capacity planning for Group Call Pickup in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="edce4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="edce4-104">

<span> </span></span></span>

<span data-ttu-id="edce4-105">_**Dernière modification de la rubrique :** 2013-02-12_</span><span class="sxs-lookup"><span data-stu-id="edce4-105">_**Topic Last Modified:** 2013-02-12_</span></span>

<div id="sectionSection0" class="section">

<span data-ttu-id="edce4-106">Le tableau suivant décrit le modèle d’utilisateur de capture d’appel de groupe que vous pouvez utiliser comme base pour les exigences de planification de capacité.</span><span class="sxs-lookup"><span data-stu-id="edce4-106">The following table describes the Group Call Pickup user model that you can use as the basis for capacity planning requirements.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="edce4-107">Le prélèvement d’appels de groupe est basé sur l’application de parc d’appels.</span><span class="sxs-lookup"><span data-stu-id="edce4-107">Group Call Pickup is based on the Call Park application.</span></span> <span data-ttu-id="edce4-108">N’oubliez pas que, pour la planification de la capacité de reprise après sinistre, chaque pool d’un pool couplé doit être en mesure de gérer les charges de travail pour les services de parking d’appel, y compris le regroupement des appels de groupe, dans les deux pools.</span><span class="sxs-lookup"><span data-stu-id="edce4-108">Keep in mind that, for disaster recovery capacity planning, each pool of a paired pool should be able to handle the workloads for Call Park services, including Group Call Pickup, in both pools.</span></span>



</div>

### <a name="group-call-pickup-user-model"></a><span data-ttu-id="edce4-109">Modèle utilisateur de cueillette d’appel de groupe</span><span class="sxs-lookup"><span data-stu-id="edce4-109">Group Call Pickup User Model</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="edce4-110">Mesure</span><span class="sxs-lookup"><span data-stu-id="edce4-110">Metric</span></span></th>
<th><span data-ttu-id="edce4-111">Par pool frontal (avec 8 serveurs frontaux)</span><span class="sxs-lookup"><span data-stu-id="edce4-111">Per Front End pool (with 8 Front End Servers)</span></span></th>
<th><span data-ttu-id="edce4-112">Par serveur Standard Edition</span><span class="sxs-lookup"><span data-stu-id="edce4-112">Per Standard Edition server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edce4-113">Nombre recommandé d’utilisateurs par groupe</span><span class="sxs-lookup"><span data-stu-id="edce4-113">Recommended number of users per group</span></span></p></td>
<td><p><span data-ttu-id="edce4-114">50</span><span class="sxs-lookup"><span data-stu-id="edce4-114">50</span></span></p></td>
<td><p><span data-ttu-id="edce4-115">50</span><span class="sxs-lookup"><span data-stu-id="edce4-115">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edce4-116">Nombre recommandé de groupes</span><span class="sxs-lookup"><span data-stu-id="edce4-116">Recommended number of groups</span></span></p></td>
<td><p><span data-ttu-id="edce4-117">500</span><span class="sxs-lookup"><span data-stu-id="edce4-117">500</span></span></p></td>
<td><p><span data-ttu-id="edce4-118">60</span><span class="sxs-lookup"><span data-stu-id="edce4-118">60</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edce4-119">Nombre maximum d’utilisateurs par pool autorisé pour la prise d’appel de groupe</span><span class="sxs-lookup"><span data-stu-id="edce4-119">Maximum number of users per pool enabled for Group Call Pickup</span></span></p></td>
<td><p><span data-ttu-id="edce4-120">25 000</span><span class="sxs-lookup"><span data-stu-id="edce4-120">25,000</span></span></p></td>
<td><p><span data-ttu-id="edce4-121">3 000</span><span class="sxs-lookup"><span data-stu-id="edce4-121">3,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edce4-122">Rapport maximal entre le nombre d’appels entrants et le nombre total d’utilisateurs autorisé pour la prise d’appel de groupe par pool et par minute</span><span class="sxs-lookup"><span data-stu-id="edce4-122">Maximum rate of incoming calls to total users enabled for Group Call Pickup per pool per minute</span></span></p></td>
<td><p><span data-ttu-id="edce4-123">500</span><span class="sxs-lookup"><span data-stu-id="edce4-123">500</span></span></p></td>
<td><p><span data-ttu-id="edce4-124">60</span><span class="sxs-lookup"><span data-stu-id="edce4-124">60</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edce4-125">Taux maximal d’appels récupérés par les utilisateurs avec la prise d’appel de groupe par pool et par minute</span><span class="sxs-lookup"><span data-stu-id="edce4-125">Maximum rate of calls retrieved by users with Group Call Pickup per pool per minute</span></span></p></td>
<td><p><span data-ttu-id="edce4-126">200</span><span class="sxs-lookup"><span data-stu-id="edce4-126">200</span></span></p></td>
<td><p><span data-ttu-id="edce4-127">1,25</span><span class="sxs-lookup"><span data-stu-id="edce4-127">25</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <UL>
> <LI>
> <P><span data-ttu-id="edce4-128">Pour les pools front-end possédant moins de huit serveurs frontaux, calculez les métriques de manière linéaire.</span><span class="sxs-lookup"><span data-stu-id="edce4-128">For Front End pools that have fewer than eight Front End Servers, calculate the metrics linearly.</span></span> <span data-ttu-id="edce4-129">Par exemple, si votre pool frontal comporte un serveur frontal, calculez le chargement maximum comme 1/8 de valeurs affichées dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="edce4-129">For example, if your Front End pool has one Front End Server, calculate the maximum load as 1/8 of the values shown in the table.</span></span></P>
> <LI>
> <P><span data-ttu-id="edce4-130">Vous pouvez augmenter ou diminuer le nombre d’utilisateurs par groupe et le nombre de groupes recommandés tant que vous ne dépassez pas le nombre d’utilisateurs maximal par pool.</span><span class="sxs-lookup"><span data-stu-id="edce4-130">You can increase or decrease the recommended number of users per group and number of groups as long as you do not exceed the maximum number of users per pool.</span></span> <span data-ttu-id="edce4-131">Par exemple, votre serveur édition standard peut avoir des groupes 120 avec 25 utilisateurs par groupe, car le nombre d’utilisateurs activés pour la capture d’appels de groupe est toujours au maximum au niveau du modèle utilisateur (c’est-à-dire, 120 3 000 groupes).</span><span class="sxs-lookup"><span data-stu-id="edce4-131">For example, your Standard Edition server can have 120 groups with 25 users per group because the number of users enabled for Group Call Pickup is still within the user model maximum (that is, 120 groups times 25 users is 3,000 users enabled for Group Call Pickup).</span></span></P></LI></UL><span data-ttu-id="edce4-132">



</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="edce4-132">



</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

