---
title: 'Lync Server 2013 : Location-Based routage des conférences'
description: 'Lync Server 2013 : Location-Based routage de conférences.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location-Based Routing for conferencing
ms:assetid: e1acb1ba-0ed2-4abf-8a7b-1ca3049e95e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362849(v=OCS.15)
ms:contentKeyID: 56335087
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 979c835e03bbf87c9a9bf86b030cb9a8f4e138e0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426542"
---
# <a name="location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="51001-103">Routage de Location-Based pour les conférences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51001-103">Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="51001-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="51001-104">

<span> </span></span></span>

<span data-ttu-id="51001-105">_**Dernière modification de la rubrique :** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="51001-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="51001-106">Location-Based le routage permet de limiter le routage des appels entre les points de terminaison VoIP et les points de terminaison RTC en fonction de l’emplacement des parties de l’appel.</span><span class="sxs-lookup"><span data-stu-id="51001-106">Location-Based Routing makes it possible to restrict the routing of calls between VoIP endpoints and PSTN endpoints based on the location of the parties in the call.</span></span> <span data-ttu-id="51001-107">Avec la mise à jour cumulative 2 de Lync Server 2013, les règles de routage de Location-Based peuvent être appliquées lors de réunions Lync (par exemple, des conférences) pour empêcher le contournement du numéro RTC.</span><span class="sxs-lookup"><span data-stu-id="51001-107">With Cumulative Update 2 of Lync Server 2013, Location-Based Routing rules can be enforced on Lync meetings (i.e. conferences) to prevent PSTN toll bypass.</span></span> <span data-ttu-id="51001-108">L’application surveille une conférence active et applique Location-Based restrictions de routage en fonction de l’emplacement des utilisateurs qui participent.</span><span class="sxs-lookup"><span data-stu-id="51001-108">The application monitors an active conference and enforces Location-Based Routing restrictions based on the location of users participating.</span></span> <span data-ttu-id="51001-109">L’application de conférence de routage de Location-Based permet en outre d’appliquer des restrictions de routage de Location-Based aux transferts de conseils liés aux points de terminaison RTC.</span><span class="sxs-lookup"><span data-stu-id="51001-109">The Location-Based Routing Conferencing application additionally enables the enforcement of Location-Based Routing restrictions to consultative transfers involving PSTN endpoints.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="51001-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="51001-110">In This Section</span></span>

  - [<span data-ttu-id="51001-111">Vue d’ensemble du routage de Location-Based pour les conférences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51001-111">Overview of Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-overview-of-location-based-routing-for-conferencing.md)

  - [<span data-ttu-id="51001-112">Routage par emplacement et transferts d’appels de consultation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51001-112">Location-Based Routing and consultative call transfers in Lync Server 2013</span></span>](lync-server-2013-location-based-routing-and-consultative-call-transfers.md)

  - [<span data-ttu-id="51001-113">Configuration requise pour le routage de Location-Based pour les conférences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51001-113">Requirements for Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-requirements-for-location-based-routing-for-conferencing.md)

  - [<span data-ttu-id="51001-114">Configuration du routage géodépendant pour les conférences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51001-114">Configuration of Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-configuration-of-location-based-routing-for-conferencing.md)

<span data-ttu-id="51001-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="51001-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

