---
title: 'Lync Server 2013 : tblADCookie'
description: 'Lync Server 2013 : tblADCookie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblADCookie
ms:assetid: 0a9102c4-47aa-40ea-8a0d-20e72ab09848
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558610(v=OCS.15)
ms:contentKeyID: 48183366
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 41c3dde3730ede07b204a473c7fe0a5ab68054d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394345"
---
# <a name="tbladcookie-in-lync-server-2013"></a><span data-ttu-id="30196-103">tblADCookie dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30196-103">tblADCookie in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="30196-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="30196-104">

<span> </span></span></span>

<span data-ttu-id="30196-105">_**Dernière modification de la rubrique :** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="30196-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="30196-106">tblADCookie contient les cookies de synchronisation LDAP (Lightweight Directory Access Protocol) actuels.</span><span class="sxs-lookup"><span data-stu-id="30196-106">tblADCookie contains the current Lightweight Directory Access Protocol (LDAP) Sync cookies.</span></span>

### <a name="columns"></a><span data-ttu-id="30196-107">Celles</span><span class="sxs-lookup"><span data-stu-id="30196-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30196-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="30196-108">Column</span></span></th>
<th><span data-ttu-id="30196-109">Type</span><span class="sxs-lookup"><span data-stu-id="30196-109">Type</span></span></th>
<th><span data-ttu-id="30196-110">Description</span><span class="sxs-lookup"><span data-stu-id="30196-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30196-111">prinGuid</span><span class="sxs-lookup"><span data-stu-id="30196-111">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="30196-112">GUID, pas null</span><span class="sxs-lookup"><span data-stu-id="30196-112">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="30196-113">GUID principal du domaine qui est surveillé.</span><span class="sxs-lookup"><span data-stu-id="30196-113">Principal GUID of the domain being monitored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30196-114">prinDCHost</span><span class="sxs-lookup"><span data-stu-id="30196-114">prinDCHost</span></span></p></td>
<td><p><span data-ttu-id="30196-115">nvarchar (255)</span><span class="sxs-lookup"><span data-stu-id="30196-115">nvarchar (255)</span></span></p></td>
<td><p><span data-ttu-id="30196-116">Nom de domaine complet (FQDN) du contrôleur de domaine actuel utilisé pour la synchronisation des services de domaine Active Directory (AD DS). A une valeur d’information.</span><span class="sxs-lookup"><span data-stu-id="30196-116">Fully qualified domain name (FQDN) of the current domain controller used for Active Directory Domain Services Sync. Has informational value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30196-117">adcContent</span><span class="sxs-lookup"><span data-stu-id="30196-117">adcContent</span></span></p></td>
<td><p><span data-ttu-id="30196-118">image (binaire)</span><span class="sxs-lookup"><span data-stu-id="30196-118">image (binary)</span></span></p></td>
<td><p><span data-ttu-id="30196-119">Cookie de synchronisation Active Directory.</span><span class="sxs-lookup"><span data-stu-id="30196-119">Active Directory Sync cookie.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30196-120">lastUpdated</span><span class="sxs-lookup"><span data-stu-id="30196-120">lastUpdated</span></span></p></td>
<td><p><span data-ttu-id="30196-121">DateHeure</span><span class="sxs-lookup"><span data-stu-id="30196-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="30196-122">Date et heure de la mise à jour de ligne.</span><span class="sxs-lookup"><span data-stu-id="30196-122">Time stamp with the row update time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30196-123">lockedUntil</span><span class="sxs-lookup"><span data-stu-id="30196-123">lockedUntil</span></span></p></td>
<td><p><span data-ttu-id="30196-124">DateHeure</span><span class="sxs-lookup"><span data-stu-id="30196-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="30196-125">Temps nécessaire au verrouillage de la ligne pour les modifications.</span><span class="sxs-lookup"><span data-stu-id="30196-125">Time until the row is locked for changes.</span></span> <span data-ttu-id="30196-126">Il s’agit d’une partie d’un mécanisme de verrouillage de logiciels qui garantit que seul l’un des services de chat effectue la synchronisation Active Directory à la fois.</span><span class="sxs-lookup"><span data-stu-id="30196-126">This is part of a software interlock mechanism that ensures that only one of the chat services does the Active Directory Sync at a time.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="30196-127">Permettent</span><span class="sxs-lookup"><span data-stu-id="30196-127">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30196-128">Colonne (s)</span><span class="sxs-lookup"><span data-stu-id="30196-128">Column(s)</span></span></th>
<th><span data-ttu-id="30196-129">Description</span><span class="sxs-lookup"><span data-stu-id="30196-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30196-130">prinGuid</span><span class="sxs-lookup"><span data-stu-id="30196-130">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="30196-131">Clé primaire.</span><span class="sxs-lookup"><span data-stu-id="30196-131">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30196-132">prinGuid</span><span class="sxs-lookup"><span data-stu-id="30196-132">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="30196-133">Clé étrangère avec recherche dans la table principale. prinGuid.</span><span class="sxs-lookup"><span data-stu-id="30196-133">Foreign key with lookup in Principal.prinGuid table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="30196-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="30196-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

