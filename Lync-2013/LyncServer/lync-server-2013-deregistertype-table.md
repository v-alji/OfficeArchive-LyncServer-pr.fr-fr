---
title: 'Lync Server 2013 : Table DeRegisterType'
description: 'Tableau Lync Server 2013 : DeRegisterType'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DeRegisterType table
ms:assetid: 09148118-6209-4fd7-a494-99118689a245
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398142(v=OCS.15)
ms:contentKeyID: 48183346
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: afad63c2abeba3e91565e07dac75d0ac6c96ca3a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429558"
---
# <a name="deregistertype-table-in-lync-server-2013"></a><span data-ttu-id="58083-103">Table DeRegisterType dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="58083-103">DeRegisterType table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="58083-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="58083-104">

<span> </span></span></span>

<span data-ttu-id="58083-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="58083-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="58083-106">La table DeRegisterType est une table statique qui stocke la liste de types de déregistreurs d’utilisateurs possibles, par exemple « client lancé », « inscription expirée » ou « le client a cessé de répondre ».</span><span class="sxs-lookup"><span data-stu-id="58083-106">The DeRegisterType table is a static table that stores the list of possible user de-registers types, such as ‘client initiated’, ‘registration expired’, or ‘client stopped responding.’</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="58083-107">Colonne</span><span class="sxs-lookup"><span data-stu-id="58083-107">Column</span></span></th>
<th><span data-ttu-id="58083-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="58083-108">Data Type</span></span></th>
<th><span data-ttu-id="58083-109">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="58083-109">Key/Index</span></span></th>
<th><span data-ttu-id="58083-110">Détails</span><span class="sxs-lookup"><span data-stu-id="58083-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58083-111"><strong>DeRegisterTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="58083-111"><strong>DeRegisterTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="58083-112">tinyint</span><span class="sxs-lookup"><span data-stu-id="58083-112">tinyint</span></span></p></td>
<td><p><span data-ttu-id="58083-113">Principal</span><span class="sxs-lookup"><span data-stu-id="58083-113">Primary</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58083-114"><strong>DeRegisterReason</strong></span><span class="sxs-lookup"><span data-stu-id="58083-114"><strong>DeRegisterReason</strong></span></span></p></td>
<td><p><span data-ttu-id="58083-115">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="58083-115">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="58083-116">Valeurs autorisées :</span><span class="sxs-lookup"><span data-stu-id="58083-116">Allowed values:</span></span></p>
<ul>
<li><p><span data-ttu-id="58083-117">0--Inconnu</span><span class="sxs-lookup"><span data-stu-id="58083-117">0 -- Unknown</span></span></p></li>
<li><p><span data-ttu-id="58083-118">1--le client a démarré la suppression</span><span class="sxs-lookup"><span data-stu-id="58083-118">1 -- Client Initiated Deregistration</span></span></p></li>
<li><p><span data-ttu-id="58083-119">2--inscription expirée</span><span class="sxs-lookup"><span data-stu-id="58083-119">2 -- Registration Expired</span></span></p></li>
<li><p><span data-ttu-id="58083-120">3-client bloqué</span><span class="sxs-lookup"><span data-stu-id="58083-120">3 – Client crashed</span></span></p></li>
<li><p><span data-ttu-id="58083-121">4--attributs utilisateur modifiés</span><span class="sxs-lookup"><span data-stu-id="58083-121">4 -- User Attributes Changed</span></span></p></li>
<li><p><span data-ttu-id="58083-122">5 – Bureau d’enregistrement préféré modifié</span><span class="sxs-lookup"><span data-stu-id="58083-122">5 – Preferred Registrar Changed</span></span></p></li>
<li><p><span data-ttu-id="58083-123">6--client hérité en mode de survie</span><span class="sxs-lookup"><span data-stu-id="58083-123">6 -- Legacy Client In Survival Mode</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="58083-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="58083-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

