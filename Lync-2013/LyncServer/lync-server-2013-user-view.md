---
title: 'Vue utilisateur de Lync Server 2013 :'
description: 'Vue utilisateur de Lync Server 2013 :'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User view
ms:assetid: 796f77e6-1da6-4969-b18b-3537209a1fe4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688100(v=OCS.15)
ms:contentKeyID: 49733699
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aa606887e8050a51f1e5a87656bb74a7cd58bbc3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439159"
---
# <a name="user-view-in-lync-server-2013"></a><span data-ttu-id="8585f-103">Affichage utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8585f-103">User view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8585f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8585f-104">

<span> </span></span></span>

<span data-ttu-id="8585f-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="8585f-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="8585f-106">L’affichage utilisateur stocke les informations sur les utilisateurs qui ont participé à des appels ou des sessions ayant des enregistrements dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="8585f-106">The User view stores information about users who have been involved in calls or sessions that have records in the database.</span></span> <span data-ttu-id="8585f-107">Cet affichage a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8585f-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8585f-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="8585f-108">Column</span></span></th>
<th><span data-ttu-id="8585f-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="8585f-109">Data Type</span></span></th>
<th><span data-ttu-id="8585f-110">Détails</span><span class="sxs-lookup"><span data-stu-id="8585f-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8585f-111">UserId</span><span class="sxs-lookup"><span data-stu-id="8585f-111">UserId</span></span></p></td>
<td><p><span data-ttu-id="8585f-112">int</span><span class="sxs-lookup"><span data-stu-id="8585f-112">int</span></span></p></td>
<td><p><span data-ttu-id="8585f-113">Numéro unique identifiant cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8585f-113">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8585f-114">UserUri</span><span class="sxs-lookup"><span data-stu-id="8585f-114">UserUri</span></span></p></td>
<td><p><span data-ttu-id="8585f-115">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="8585f-115">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="8585f-116">URI de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8585f-116">Uri of the user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8585f-117">TenantKey</span><span class="sxs-lookup"><span data-stu-id="8585f-117">TenantKey</span></span></p></td>
<td><p><span data-ttu-id="8585f-118">identificateur</span><span class="sxs-lookup"><span data-stu-id="8585f-118">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="8585f-119">Client de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8585f-119">Tenant of user.</span></span> <span data-ttu-id="8585f-120">Pour plus d’informations, voir la <a href="lync-server-2013-tenants-table.md">table locataires dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8585f-120">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8585f-121">UriType</span><span class="sxs-lookup"><span data-stu-id="8585f-121">UriType</span></span></p></td>
<td><p><span data-ttu-id="8585f-122">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="8585f-122">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8585f-123">Type d’URI de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8585f-123">Type of user URI.</span></span> <span data-ttu-id="8585f-124">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8585f-124">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8585f-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8585f-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

