---
title: 'Affichage Lync Server 2013 : VoIPDetails'
description: 'Affichage Lync Server 2013 : VoIPDetails'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VoIPDetails view
ms:assetid: 14c44736-71ba-4fc5-82c7-1df65bf6261c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687973(v=OCS.15)
ms:contentKeyID: 49733561
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ecd34be0c8568eef29d773f088e8503a8065743
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446183"
---
# <a name="voipdetails-view-in-lync-server-2013"></a><span data-ttu-id="6ba76-103">Affichage VoIPDetails dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ba76-103">VoIPDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6ba76-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6ba76-104">

<span> </span></span></span>

<span data-ttu-id="6ba76-105">_**Dernière modification de la rubrique :** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="6ba76-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="6ba76-106">Le mode VoIPDetails stocke des informations sur les sessions d’égal à égal, où au moins un utilisateur est un utilisateur VoIP.</span><span class="sxs-lookup"><span data-stu-id="6ba76-106">The VoIPDetails view stores information about peer-to-peer sessions, where at least one user is a VoIP user.</span></span> <span data-ttu-id="6ba76-107">Cet affichage a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6ba76-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6ba76-108">Le mode VoIPDetails contient toutes les colonnes de la <A href="lync-server-2013-sessiondetails-view.md">vue SessionDetails dans Lync Server 2013</A> , en plus des colonnes répertoriées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6ba76-108">The VoIPDetails view contains all of the columns in the <A href="lync-server-2013-sessiondetails-view.md">SessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ba76-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="6ba76-109">Column</span></span></th>
<th><span data-ttu-id="6ba76-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="6ba76-110">Data Type</span></span></th>
<th><span data-ttu-id="6ba76-111">Détails</span><span class="sxs-lookup"><span data-stu-id="6ba76-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ba76-112"><strong>FromPhone</strong></span><span class="sxs-lookup"><span data-stu-id="6ba76-112"><strong>FromPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="6ba76-113">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="6ba76-113">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="6ba76-114">URI du téléphone de l’utilisateur qui a démarré la session.</span><span class="sxs-lookup"><span data-stu-id="6ba76-114">Phone URI of the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ba76-115"><strong>À la une</strong></span><span class="sxs-lookup"><span data-stu-id="6ba76-115"><strong>ToPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="6ba76-116">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="6ba76-116">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="6ba76-117">URI de téléphone de l’utilisateur qui a rejoint la session.</span><span class="sxs-lookup"><span data-stu-id="6ba76-117">Phone URI of the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ba76-118"><strong>DisconnectedByUri</strong></span><span class="sxs-lookup"><span data-stu-id="6ba76-118"><strong>DisconnectedByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="6ba76-119">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="6ba76-119">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="6ba76-120">URI de l’utilisateur qui a déconnecté la session.</span><span class="sxs-lookup"><span data-stu-id="6ba76-120">URI of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ba76-121"><strong>DisconnectedByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="6ba76-121"><strong>DisconnectedByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="6ba76-122">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6ba76-122">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6ba76-123">Type d’URI de l’utilisateur qui a déconnecté la session.</span><span class="sxs-lookup"><span data-stu-id="6ba76-123">Type of URI of the user who disconnected the session.</span></span> <span data-ttu-id="6ba76-124">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="6ba76-124">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ba76-125"><strong>DisconnectedByTenant</strong></span><span class="sxs-lookup"><span data-stu-id="6ba76-125"><strong>DisconnectedByTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="6ba76-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6ba76-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6ba76-127">Client de l’utilisateur qui a déconnecté la session.</span><span class="sxs-lookup"><span data-stu-id="6ba76-127">Tenant of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ba76-128"><strong>DisconnectedByPhone</strong></span><span class="sxs-lookup"><span data-stu-id="6ba76-128"><strong>DisconnectedByPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="6ba76-129">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="6ba76-129">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="6ba76-130">URI de téléphone de l’utilisateur qui a déconnecté la session.</span><span class="sxs-lookup"><span data-stu-id="6ba76-130">Phone URI of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ba76-131"><strong>FromMediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="6ba76-131"><strong>FromMediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="6ba76-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6ba76-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6ba76-133">Serveur de médiation utilisé par l’utilisateur qui a démarré la session.</span><span class="sxs-lookup"><span data-stu-id="6ba76-133">Mediation Server used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ba76-134"><strong>ToMediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="6ba76-134"><strong>ToMediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="6ba76-135">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6ba76-135">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6ba76-136">Serveur de médiation utilisé par l’utilisateur ayant rejoint la session.</span><span class="sxs-lookup"><span data-stu-id="6ba76-136">Mediation Server used by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ba76-137"><strong>FromGateway</strong></span><span class="sxs-lookup"><span data-stu-id="6ba76-137"><strong>FromGateway</strong></span></span></p></td>
<td><p><span data-ttu-id="6ba76-138">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6ba76-138">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6ba76-139">Passerelle utilisée par l’utilisateur qui a démarré la session.</span><span class="sxs-lookup"><span data-stu-id="6ba76-139">Gateway used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ba76-140"><strong>ToGateway</strong></span><span class="sxs-lookup"><span data-stu-id="6ba76-140"><strong>ToGateway</strong></span></span></p></td>
<td><p><span data-ttu-id="6ba76-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6ba76-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6ba76-142">Passerelle utilisée par l’utilisateur ayant rejoint la session.</span><span class="sxs-lookup"><span data-stu-id="6ba76-142">Gateway used by the user who joined the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6ba76-143">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6ba76-143">


</div>

<span> </span>

</div>

</div>

</span></span></div>

