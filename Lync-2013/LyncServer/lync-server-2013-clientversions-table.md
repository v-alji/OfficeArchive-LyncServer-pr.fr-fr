---
title: 'Lync Server 2013 : Table ClientVersions'
description: 'Tableau Lync Server 2013 : ClientVersions'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ClientVersions table
ms:assetid: 542316cf-a6db-4d52-ab28-8bf6d27a3b48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398356(v=OCS.15)
ms:contentKeyID: 48184176
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 81cf7147b7e36148901580983cf66176b574f815
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434759"
---
# <a name="clientversions-table-in-lync-server-2013"></a><span data-ttu-id="9343d-103">Table ClientVersions dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9343d-103">ClientVersions table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9343d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9343d-104">

<span> </span></span></span>

<span data-ttu-id="9343d-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="9343d-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="9343d-106">La table ClientVersions est une table qui contient une liste des différents types de clients et différentes versions ayant participé à des sessions enregistrées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="9343d-106">The ClientVersions table is a supporting table that stores a list of the various client types and versions that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="9343d-107">Chaque enregistrement de la table représente une version du client.</span><span class="sxs-lookup"><span data-stu-id="9343d-107">Each record in the table represents one client version.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9343d-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="9343d-108">Column</span></span></th>
<th><span data-ttu-id="9343d-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="9343d-109">Data Type</span></span></th>
<th><span data-ttu-id="9343d-110">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="9343d-110">Key/Index</span></span></th>
<th><span data-ttu-id="9343d-111">Détails</span><span class="sxs-lookup"><span data-stu-id="9343d-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9343d-112"><strong>VersionId</strong></span><span class="sxs-lookup"><span data-stu-id="9343d-112"><strong>VersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="9343d-113"><strong>int</strong></span><span class="sxs-lookup"><span data-stu-id="9343d-113"><strong>int</strong></span></span></p></td>
<td><p><span data-ttu-id="9343d-114">Principal</span><span class="sxs-lookup"><span data-stu-id="9343d-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="9343d-115">Numéro unique identifiant ce type et version de client.</span><span class="sxs-lookup"><span data-stu-id="9343d-115">Unique number identifying this client type and version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9343d-116"><strong>Version</strong></span><span class="sxs-lookup"><span data-stu-id="9343d-116"><strong>Version</strong></span></span></p></td>
<td><p><span data-ttu-id="9343d-117"><strong>nvarchar(256)</strong></span><span class="sxs-lookup"><span data-stu-id="9343d-117"><strong>nvarchar(256)</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9343d-118">Nom de la version.</span><span class="sxs-lookup"><span data-stu-id="9343d-118">Version name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9343d-119"><strong>TypeClient</strong></span><span class="sxs-lookup"><span data-stu-id="9343d-119"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="9343d-120">int</span><span class="sxs-lookup"><span data-stu-id="9343d-120">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9343d-121">Spécifie le type de client utilisé dans la session.</span><span class="sxs-lookup"><span data-stu-id="9343d-121">Specifies the type of client used in the session.</span></span> <span data-ttu-id="9343d-122">Pour plus d’informations, voir la <a href="lync-server-2013-useragentdef-table.md">table UserAgentDef dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="9343d-122">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="9343d-123">Ce champ a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9343d-123">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9343d-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9343d-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

