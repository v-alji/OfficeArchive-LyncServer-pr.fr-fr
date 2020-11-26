---
title: 'Lync Server 2013 : Table Tenants'
description: 'Table Lync Server 2013 : clients'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Tenants table
ms:assetid: c1b070c1-2c59-4ca9-910b-43f673f97fda
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412950(v=OCS.15)
ms:contentKeyID: 48185309
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 96025dfd9fb42a6083f7f3daca98e243f01a8516
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441283"
---
# <a name="tenants-table-in-lync-server-2013"></a><span data-ttu-id="68f84-103">Table Tenants dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68f84-103">Tenants table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="68f84-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="68f84-104">

<span> </span></span></span>

<span data-ttu-id="68f84-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="68f84-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="68f84-106">La table clients est une table de prise en charge qui stocke une liste des différents clients.</span><span class="sxs-lookup"><span data-stu-id="68f84-106">The Tenants table is a supporting table that stores a list of the various tenants.</span></span> <span data-ttu-id="68f84-107">Chaque enregistrement de la table représente un client.</span><span class="sxs-lookup"><span data-stu-id="68f84-107">Each record in the table represents one tenant.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="68f84-108">Dans le cadre d’un déploiement local, le CDR utilise l’ID de locataire intégré pour indiquer un type d’authentification différent, tel que la connectivité de messagerie instantanée publique, fédéré et anonyme.</span><span class="sxs-lookup"><span data-stu-id="68f84-108">In on-premises deployment, CDR uses the build-in Tenant ID to indicate different authentication type, such as public IM connectivity, Federated and Anonymous.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68f84-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="68f84-109">Column</span></span></th>
<th><span data-ttu-id="68f84-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="68f84-110">Data Type</span></span></th>
<th><span data-ttu-id="68f84-111">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="68f84-111">Key/Index</span></span></th>
<th><span data-ttu-id="68f84-112">Détails</span><span class="sxs-lookup"><span data-stu-id="68f84-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="68f84-113"><strong>IDClient</strong></span><span class="sxs-lookup"><span data-stu-id="68f84-113"><strong>TenantId</strong></span></span></p></td>
<td><p><span data-ttu-id="68f84-114">int</span><span class="sxs-lookup"><span data-stu-id="68f84-114">int</span></span></p></td>
<td><p><span data-ttu-id="68f84-115">Principal</span><span class="sxs-lookup"><span data-stu-id="68f84-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="68f84-116">Numéro unique identifiant cet ID de client.</span><span class="sxs-lookup"><span data-stu-id="68f84-116">Unique number identifying this Tenant ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68f84-117"><strong>TenantKey</strong></span><span class="sxs-lookup"><span data-stu-id="68f84-117"><strong>TenantKey</strong></span></span></p></td>
<td><p><span data-ttu-id="68f84-118">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="68f84-118">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="68f84-119">Valeurs autorisées :</span><span class="sxs-lookup"><span data-stu-id="68f84-119">Allowed values:</span></span></p>
<ul>
<li><p><span data-ttu-id="68f84-120">00000000-0000-0000-0000-000000000000-entreprise</span><span class="sxs-lookup"><span data-stu-id="68f84-120">00000000-0000-0000-0000-000000000000 – Enterprise</span></span></p></li>
<li><p><span data-ttu-id="68f84-121">00000000-0000-0000-0000-000000000001-Federated</span><span class="sxs-lookup"><span data-stu-id="68f84-121">00000000-0000-0000-0000-000000000001 – Federated</span></span></p></li>
<li><p><span data-ttu-id="68f84-122">00000000-0000-0000-0000-000000000002-anonyme</span><span class="sxs-lookup"><span data-stu-id="68f84-122">00000000-0000-0000-0000-000000000002 – Anonymous</span></span></p></li>
<li><p><span data-ttu-id="68f84-123">00000000-0000-0000-0000-000000000003-connectivité PIC (Public IM Connectivity)</span><span class="sxs-lookup"><span data-stu-id="68f84-123">00000000-0000-0000-0000-000000000003 – Public IM connectivity</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="68f84-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="68f84-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

