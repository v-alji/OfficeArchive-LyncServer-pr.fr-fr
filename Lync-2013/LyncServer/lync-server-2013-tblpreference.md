---
title: 'Lync Server 2013 : tblPreference'
description: 'Lync Server 2013 : tblPreference.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPreference
ms:assetid: f94eb128-f782-42ff-a568-ed3529573bc8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615052(v=OCS.15)
ms:contentKeyID: 48185913
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 86e8b81a6af93e9bf1d7673e54492579a1bed08e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441374"
---
# <a name="tblpreference-in-lync-server-2013"></a><span data-ttu-id="24a9e-103">tblPreference dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="24a9e-103">tblPreference in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="24a9e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="24a9e-104">

<span> </span></span></span>

<span data-ttu-id="24a9e-105">_**Dernière modification de la rubrique :** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="24a9e-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="24a9e-106">tblPreference contient les préférences client de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="24a9e-106">tblPreference contains the users’ client preferences.</span></span> <span data-ttu-id="24a9e-107">Il est généralement utilisé par les clients antérieurs à Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="24a9e-107">This is generally used by clients previous to Lync 2013.</span></span>

### <a name="columns"></a><span data-ttu-id="24a9e-108">Celles</span><span class="sxs-lookup"><span data-stu-id="24a9e-108">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24a9e-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="24a9e-109">Column</span></span></th>
<th><span data-ttu-id="24a9e-110">Type</span><span class="sxs-lookup"><span data-stu-id="24a9e-110">Type</span></span></th>
<th><span data-ttu-id="24a9e-111">Description</span><span class="sxs-lookup"><span data-stu-id="24a9e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24a9e-112">prefLabel</span><span class="sxs-lookup"><span data-stu-id="24a9e-112">prefLabel</span></span></p></td>
<td><p><span data-ttu-id="24a9e-113">nvarchar (255), pas null</span><span class="sxs-lookup"><span data-stu-id="24a9e-113">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="24a9e-114">Étiquette avec un format tel que : &lt; URI SIP utilisateur &gt; | nom d’utilisateur. &lt; option définie &gt; .</span><span class="sxs-lookup"><span data-stu-id="24a9e-114">Label with a format such as: &lt;user sip uri&gt;|username.&lt;preference set&gt;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24a9e-115">prefSeqID</span><span class="sxs-lookup"><span data-stu-id="24a9e-115">prefSeqID</span></span></p></td>
<td><p><span data-ttu-id="24a9e-116">ent, non null</span><span class="sxs-lookup"><span data-stu-id="24a9e-116">int, not null</span></span></p></td>
<td><p><span data-ttu-id="24a9e-117">Un numéro séquentiel (par étiquette) à des fins de contrôle de version.</span><span class="sxs-lookup"><span data-stu-id="24a9e-117">A sequential number (per label) for versioning purposes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24a9e-118">prefContent</span><span class="sxs-lookup"><span data-stu-id="24a9e-118">prefContent</span></span></p></td>
<td><p><span data-ttu-id="24a9e-119">nvarchar (max)</span><span class="sxs-lookup"><span data-stu-id="24a9e-119">nvarchar (max)</span></span></p></td>
<td><p><span data-ttu-id="24a9e-120">Contenu encodé.</span><span class="sxs-lookup"><span data-stu-id="24a9e-120">Encoded content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24a9e-121">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="24a9e-121">lastModifiedBy</span></span></p></td>
<td><p><span data-ttu-id="24a9e-122">ent, non null</span><span class="sxs-lookup"><span data-stu-id="24a9e-122">int, not null</span></span></p></td>
<td><p><span data-ttu-id="24a9e-123">ID de l’objet principal qui a mis à jour la préférence.</span><span class="sxs-lookup"><span data-stu-id="24a9e-123">ID of the principal that updated the preference.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="24a9e-124">Clé</span><span class="sxs-lookup"><span data-stu-id="24a9e-124">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24a9e-125">Colonne</span><span class="sxs-lookup"><span data-stu-id="24a9e-125">Column</span></span></th>
<th><span data-ttu-id="24a9e-126">Description</span><span class="sxs-lookup"><span data-stu-id="24a9e-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24a9e-127">&lt;prefLabel, prefSeqID&gt;</span><span class="sxs-lookup"><span data-stu-id="24a9e-127">&lt;prefLabel, prefSeqID&gt;</span></span></p></td>
<td><p><span data-ttu-id="24a9e-128">Clé primaire.</span><span class="sxs-lookup"><span data-stu-id="24a9e-128">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="24a9e-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="24a9e-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

