---
title: 'Lync Server 2013 : Table Mcus'
description: 'Table Lync Server 2013 : MCU.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mcus table
ms:assetid: 271b7963-8fd8-4d92-a701-1a62aaf895ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425742(v=OCS.15)
ms:contentKeyID: 48183674
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b0b5d0bcbebb5efc1d767776b4581b18d9f2ed18
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425744"
---
# <a name="mcus-table-in-lync-server-2013"></a><span data-ttu-id="df217-103">Table Mcus dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df217-103">Mcus table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="df217-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="df217-104">

<span> </span></span></span>

<span data-ttu-id="df217-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="df217-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="df217-106">La table MCU est une table de support.</span><span class="sxs-lookup"><span data-stu-id="df217-106">The Mcus table is a supporting table.</span></span> <span data-ttu-id="df217-107">Chaque enregistrement stocke les informations relatives à un service de conférence.</span><span class="sxs-lookup"><span data-stu-id="df217-107">Each record stores information about one conferencing service.</span></span> <span data-ttu-id="df217-108">Il peut s’agir du service de conférence par messagerie instantanée et du service de conférence téléphonique (qui s’exécutent sous forme de processus sur les serveurs frontaux), du service de conférence Web et du service de conférence A/V.</span><span class="sxs-lookup"><span data-stu-id="df217-108">These can include the IM Conferencing service and the Telephony Conferencing service (which run as processes on front-end servers), and the Web Conferencing service and A/V Conferencing service.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="df217-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="df217-109">Column</span></span></th>
<th><span data-ttu-id="df217-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="df217-110">Data Type</span></span></th>
<th><span data-ttu-id="df217-111">Clé/Index</span><span class="sxs-lookup"><span data-stu-id="df217-111">Key/Index</span></span></th>
<th><span data-ttu-id="df217-112">Détails</span><span class="sxs-lookup"><span data-stu-id="df217-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df217-113"><strong>McuId</strong></span><span class="sxs-lookup"><span data-stu-id="df217-113"><strong>McuId</strong></span></span></p></td>
<td><p><span data-ttu-id="df217-114">int</span><span class="sxs-lookup"><span data-stu-id="df217-114">int</span></span></p></td>
<td><p><span data-ttu-id="df217-115">Principal</span><span class="sxs-lookup"><span data-stu-id="df217-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="df217-116">Numéro unique identifiant ce serveur de conférence.</span><span class="sxs-lookup"><span data-stu-id="df217-116">Unique number identifying this conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df217-117"><strong>McuUri</strong></span><span class="sxs-lookup"><span data-stu-id="df217-117"><strong>McuUri</strong></span></span></p></td>
<td><p><span data-ttu-id="df217-118">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="df217-118">nvarchar(450)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df217-119"><strong>McuTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="df217-119"><strong>McuTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="df217-120">inyint</span><span class="sxs-lookup"><span data-stu-id="df217-120">inyint</span></span></p></td>
<td><p> <span data-ttu-id="df217-121">Externes</span><span class="sxs-lookup"><span data-stu-id="df217-121">Foreign</span></span></p></td>
<td><p><span data-ttu-id="df217-122">Le type de serveur de conférence, tel que conf : chat (pour les messages instantanés) ou conf : audio-vidéo.</span><span class="sxs-lookup"><span data-stu-id="df217-122">Conferencing server type, such as conf:chat (for IMs) or conf:audio-video.</span></span> <span data-ttu-id="df217-123">Pour plus d’informations, voir la <a href="lync-server-2013-uritypes-table.md">table UriTypes dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="df217-123">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="df217-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="df217-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

