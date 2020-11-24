---
title: 'Lync Server 2013 : détails de l’affichage QoE'
description: 'Lync Server 2013 : détails de l’affichage QoE.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: QoE view details
ms:assetid: 6a658318-a317-4546-a44c-a9c473d8e86a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688081(v=OCS.15)
ms:contentKeyID: 49733677
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b20eb083295a5f3d3ecb5be7a8c96d9c4b7cfab2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394521"
---
# <a name="qoe-view-details-in-lync-server-2013"></a><span data-ttu-id="e22a6-103">Détails de l’affichage QoE dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e22a6-103">QoE view details in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e22a6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e22a6-104">

<span> </span></span></span>

<span data-ttu-id="e22a6-105">_**Dernière modification de la rubrique :** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="e22a6-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="e22a6-106">Les vues couvrent les cas les plus courants de retour de données à partir de la base de données SQL QoE.</span><span class="sxs-lookup"><span data-stu-id="e22a6-106">Views cover the most common scenarios for returning data from the QoE SQL database.</span></span> <span data-ttu-id="e22a6-107">Il est recommandé d’utiliser des affichages pour créer des rapports personnalisés plutôt que d’accéder directement aux tables de la base de données. en effet, les vues sont plus susceptibles de garantir la compatibilité descendante avec les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e22a6-107">It is recommended views used for building custom reports instead of directly accessing the database tables; that’s because views are more likely to maintain backwards compatibility with future releases.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e22a6-108">Nom de la vue</span><span class="sxs-lookup"><span data-stu-id="e22a6-108">View Name</span></span></th>
<th><span data-ttu-id="e22a6-109">Description</span><span class="sxs-lookup"><span data-stu-id="e22a6-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e22a6-110"><a href="lync-server-2013-audiostreamdetail-view.md">Affichage AudioStreamDetail dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e22a6-110"><a href="lync-server-2013-audiostreamdetail-view.md">AudioStreamDetail view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e22a6-111">Stocke les informations relatives à chaque flux audio dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="e22a6-111">Stores information about each audio stream in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e22a6-112"><a href="lync-server-2013-medialine-view.md">Affichage MediaLine dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e22a6-112"><a href="lync-server-2013-medialine-view.md">MediaLine view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e22a6-113">Stocke les informations relatives à chaque ligne multimédia dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="e22a6-113">Stores information about each media line in the database.</span></span> <span data-ttu-id="e22a6-114">Une seule session audio contient généralement une ligne multimédia audio.</span><span class="sxs-lookup"><span data-stu-id="e22a6-114">One audio session typically contains one audio media line.</span></span> <span data-ttu-id="e22a6-115">Une session audio et vidéo (A/V) contient généralement une seule ligne de médias audio et une seule ligne de média vidéo. Toutefois, la session peut contenir deux lignes de média vidéo si un appareil de conférence est utilisé ou si la vue Galerie est utilisée.</span><span class="sxs-lookup"><span data-stu-id="e22a6-115">One audio and video (A/V) session typically contains one audio media line and one video media line; however, the session might contain two video media lines if a conferencing device is used or if Gallery View is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e22a6-116"><a href="lync-server-2013-networkconfigurationsettings-view.md">Affichage NetworkConfigurationSettings dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e22a6-116"><a href="lync-server-2013-networkconfigurationsettings-view.md">NetworkConfigurationSettings view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e22a6-117">Stocke des informations sur la configuration du réseau.</span><span class="sxs-lookup"><span data-stu-id="e22a6-117">Stores information about the network configuration.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e22a6-118"><a href="lync-server-2013-session-view.md">Affichage de session dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e22a6-118"><a href="lync-server-2013-session-view.md">Session view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e22a6-119">Stocke les informations sur les sessions contenant des enregistrements dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="e22a6-119">Stores information about sessions that have records in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e22a6-120"><a href="lync-server-2013-useragent-view.md">Affichage UserAgent dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e22a6-120"><a href="lync-server-2013-useragent-view.md">UserAgent view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e22a6-121">Stocke les informations sur les agents utilisateur impliqués dans les sessions contenant des enregistrements dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="e22a6-121">Stores information about the user agents that have been involved in sessions that have records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e22a6-122"><a href="lync-server-2013-videostreamdetail-view.md">Affichage VideoStreamDetail dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="e22a6-122"><a href="lync-server-2013-videostreamdetail-view.md">VideoStreamDetail view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="e22a6-123">Stocke des informations sur chaque flux vidéo dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="e22a6-123">Stores information about each video stream in the database.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e22a6-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e22a6-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

