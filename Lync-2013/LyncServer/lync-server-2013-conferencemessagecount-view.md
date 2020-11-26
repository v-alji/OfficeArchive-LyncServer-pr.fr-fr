---
title: 'Affichage Lync Server 2013 : ConferenceMessageCount'
description: 'Affichage Lync Server 2013 : ConferenceMessageCount'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceMessageCount view
ms:assetid: 8ee3ee95-fb78-4d4e-bcdd-6ce5a0a23b44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688129(v=OCS.15)
ms:contentKeyID: 49733727
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 212d6e1a346253809fb70806424350cc7fc0dfe2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434430"
---
# <a name="conferencemessagecount-view-in-lync-server-2013"></a><span data-ttu-id="bbf5e-103">Affichage ConferenceMessageCount dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bbf5e-103">ConferenceMessageCount view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bbf5e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bbf5e-104">

<span> </span></span></span>

<span data-ttu-id="bbf5e-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="bbf5e-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="bbf5e-106">Le mode ConferenceMessageCount stocke les informations sur le nombre de messages envoyés par un utilisateur à une conférence.</span><span class="sxs-lookup"><span data-stu-id="bbf5e-106">The ConferenceMessageCount view stores information about how many messages were sent by a user to a conference.</span></span> <span data-ttu-id="bbf5e-107">Cet affichage a été présenté dans Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bbf5e-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bbf5e-108">Le mode ConferenceMessageCount contient toutes les colonnes de la <A href="lync-server-2013-conferencesessiondetails-view.md">vue ConferenceSessionDetails dans Lync Server 2013</A> , en plus des colonnes répertoriées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="bbf5e-108">The ConferenceMessageCount view contains all of the columns in the <A href="lync-server-2013-conferencesessiondetails-view.md">ConferenceSessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bbf5e-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="bbf5e-109">Column</span></span></th>
<th><span data-ttu-id="bbf5e-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="bbf5e-110">Data Type</span></span></th>
<th><span data-ttu-id="bbf5e-111">Détails</span><span class="sxs-lookup"><span data-stu-id="bbf5e-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbf5e-112"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="bbf5e-112"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="bbf5e-113">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="bbf5e-113">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="bbf5e-114">URI de l’utilisateur qui a envoyé le message.</span><span class="sxs-lookup"><span data-stu-id="bbf5e-114">URI of the user who sent the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbf5e-115"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="bbf5e-115"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="bbf5e-116">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="bbf5e-116">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="bbf5e-117">Type d’URI de l’utilisateur qui a envoyé les messages.</span><span class="sxs-lookup"><span data-stu-id="bbf5e-117">Type of URI of the user who sent the messages.</span></span> <span data-ttu-id="bbf5e-118">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="bbf5e-118">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbf5e-119"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="bbf5e-119"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="bbf5e-120">identificateur</span><span class="sxs-lookup"><span data-stu-id="bbf5e-120">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="bbf5e-121">Client de l’utilisateur qui a envoyé les messages.</span><span class="sxs-lookup"><span data-stu-id="bbf5e-121">Tenant of user who sent the messages.</span></span> <span data-ttu-id="bbf5e-122">Pour plus d’informations, voir la <a href="lync-server-2013-tenants-table.md">table locataires dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="bbf5e-122">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbf5e-123"><strong>UserMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="bbf5e-123"><strong>UserMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="bbf5e-124">type</span><span class="sxs-lookup"><span data-stu-id="bbf5e-124">smallint</span></span></p></td>
<td><p><span data-ttu-id="bbf5e-125">Nombre de messages envoyés par l’utilisateur au cours de la session de conférence.</span><span class="sxs-lookup"><span data-stu-id="bbf5e-125">Number of messages sent by the user during the conference session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="bbf5e-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bbf5e-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

