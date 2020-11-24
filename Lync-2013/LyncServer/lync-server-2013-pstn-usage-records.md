---
title: 'Lync Server 2013 : Enregistrements d’utilisation RTC'
description: 'Lync Server 2013 : enregistrements d’utilisation RTC.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN usage records
ms:assetid: b5f624aa-abe8-455b-a8e3-c228be230463
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412878(v=OCS.15)
ms:contentKeyID: 48185188
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f8ff428dc2fa5cf8cf0f10e37f0f79c38d70d70
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394577"
---
# <a name="pstn-usage-records-in-lync-server-2013"></a><span data-ttu-id="7ee58-103">Enregistrements d’utilisation RTC dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7ee58-103">PSTN usage records in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7ee58-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7ee58-104">

<span> </span></span></span>

<span data-ttu-id="7ee58-105">_**Dernière modification de la rubrique :** 2012-09-23_</span><span class="sxs-lookup"><span data-stu-id="7ee58-105">_**Topic Last Modified:** 2012-09-23_</span></span>

<span data-ttu-id="7ee58-106">La planification des enregistrements d’utilisation PSTN consiste principalement à répertorier toutes les autorisations d’appel actuellement en vigueur dans votre organisation, du PDG aux travailleurs temporaires, consultants et subordonnés.</span><span class="sxs-lookup"><span data-stu-id="7ee58-106">Planning PSTN usage records consists mainly of listing all the call permissions that are currently in force in your organization, from the CEO to temporary workers, consultants, and contingent staff.</span></span> <span data-ttu-id="7ee58-107">Ce processus donne également la possibilité de revérifier les autorisations d’appel existantes et de les modifier.</span><span class="sxs-lookup"><span data-stu-id="7ee58-107">This process also provides an opportunity to reexamine existing call permissions and revise them.</span></span> <span data-ttu-id="7ee58-108">Vous pouvez créer des enregistrements d’utilisation RTC uniquement pour les autorisations d’appel qui s’appliquent aux utilisateurs vocaux de votre entreprise, mais une meilleure prise en charge peut être de créer des enregistrements d’utilisation RTC pour toutes les autorisations d’appel, qu’il n’y ait peut-être pas pour l’instant ou non applicable au groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7ee58-108">You can create PSTN usage records only for those call permissions that apply to your anticipated Enterprise Voice users, but a better long-range solution might be to create PSTN usage records for all call permissions, regardless of whether some may not currently apply to the group of users to be enabled for Enterprise Voice.</span></span> <span data-ttu-id="7ee58-109">Si les autorisations d’appel changent ou que de nouveaux utilisateurs avec des autorisations d’appel différentes sont ajoutés, vous aurez déjà créé les enregistrements d’utilisation PSTN requis.</span><span class="sxs-lookup"><span data-stu-id="7ee58-109">If call permissions change or new users with different call permissions are added, you will have already created the required PSTN usage records.</span></span>

<span data-ttu-id="7ee58-110">Le tableau ci-dessous présente un exemple d’utilisation PSTN standard :</span><span class="sxs-lookup"><span data-stu-id="7ee58-110">The following table shows a typical PSTN usage table.</span></span>

### <a name="pstn-usage-records"></a><span data-ttu-id="7ee58-111">Enregistrements d’utilisation PSTN</span><span class="sxs-lookup"><span data-stu-id="7ee58-111">PSTN Usage Records</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ee58-112">Attribut de téléphone</span><span class="sxs-lookup"><span data-stu-id="7ee58-112">Phone attribute</span></span></th>
<th><span data-ttu-id="7ee58-113">Description</span><span class="sxs-lookup"><span data-stu-id="7ee58-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ee58-114">Local</span><span class="sxs-lookup"><span data-stu-id="7ee58-114">Local</span></span></p></td>
<td><p><span data-ttu-id="7ee58-115">Appels locaux</span><span class="sxs-lookup"><span data-stu-id="7ee58-115">Local calls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ee58-116">Long-Distance</span><span class="sxs-lookup"><span data-stu-id="7ee58-116">Long-Distance</span></span></p></td>
<td><p><span data-ttu-id="7ee58-117">Appels longue distance</span><span class="sxs-lookup"><span data-stu-id="7ee58-117">Long distance calls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ee58-118">International</span><span class="sxs-lookup"><span data-stu-id="7ee58-118">International</span></span></p></td>
<td><p><span data-ttu-id="7ee58-119">Appels internationaux</span><span class="sxs-lookup"><span data-stu-id="7ee58-119">International calls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ee58-120">Delhi</span><span class="sxs-lookup"><span data-stu-id="7ee58-120">Delhi</span></span></p></td>
<td><p><span data-ttu-id="7ee58-121">Employés à temps plein à Delhi</span><span class="sxs-lookup"><span data-stu-id="7ee58-121">Delhi full-time employees</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ee58-122">Redmond</span><span class="sxs-lookup"><span data-stu-id="7ee58-122">Redmond</span></span></p></td>
<td><p><span data-ttu-id="7ee58-123">Employés à temps plein à Redmond</span><span class="sxs-lookup"><span data-stu-id="7ee58-123">Redmond full-time employees</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ee58-124">RedmondTemps</span><span class="sxs-lookup"><span data-stu-id="7ee58-124">RedmondTemps</span></span></p></td>
<td><p><span data-ttu-id="7ee58-125">Employés temporaires à Redmond</span><span class="sxs-lookup"><span data-stu-id="7ee58-125">Redmond temporary employees</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ee58-126">Zurich</span><span class="sxs-lookup"><span data-stu-id="7ee58-126">Zurich</span></span></p></td>
<td><p><span data-ttu-id="7ee58-127">Employés à temps plein à Zurich</span><span class="sxs-lookup"><span data-stu-id="7ee58-127">Zurich full-time employees</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7ee58-p102">Les enregistrements d’utilisation PSTN n’effectuent aucune action par eux-mêmes. Pour qu’ils fonctionnent, vous devez les associer aux éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7ee58-p102">By themselves, PSTN usage records do not do anything. For them to work, you must associate them with the following:</span></span>

  - <span data-ttu-id="7ee58-130">des stratégies de voix, affectées aux utilisateurs ;</span><span class="sxs-lookup"><span data-stu-id="7ee58-130">Voice policies, which are assigned to users.</span></span>

  - <span data-ttu-id="7ee58-131">des itinéraires, affectés aux numéros de téléphone.</span><span class="sxs-lookup"><span data-stu-id="7ee58-131">Routes, which are assigned to phone numbers.</span></span>

<span data-ttu-id="7ee58-132">Pour plus d’informations sur les stratégies et les itinéraires vocaux, voir [stratégies vocales dans Lync server 2013](lync-server-2013-voice-policies.md) et [itinéraires vocaux dans Lync Server 2013](lync-server-2013-voice-routes.md).</span><span class="sxs-lookup"><span data-stu-id="7ee58-132">For details about voice policies and routes, see [Voice policies in Lync Server 2013](lync-server-2013-voice-policies.md) and [Voice routes in Lync Server 2013](lync-server-2013-voice-routes.md).</span></span> <span data-ttu-id="7ee58-133">Pour plus d’informations sur la création et la configuration de celles-ci, reportez-vous à la rubrique [Configuration des itinéraires vocaux pour les appels sortants dans Lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).</span><span class="sxs-lookup"><span data-stu-id="7ee58-133">For details about how to create and configure them, see [Configuring voice routes for outbound calls in Lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).</span></span>

<span data-ttu-id="7ee58-134"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7ee58-134"></div>

<span> </span>

</div>

</div>

</span></span></div>

