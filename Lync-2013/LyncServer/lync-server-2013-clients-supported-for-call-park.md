---
title: 'Lync Server 2013 : Clients pris en charge pour le parcage d’appel'
description: 'Lync Server 2013 : clients pris en charge pour le parc d’appels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Clients supported for Call Park
ms:assetid: c236d2ba-9d83-418c-9cbc-92541f115fb0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412958(v=OCS.15)
ms:contentKeyID: 48185320
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a923f0e62c246a12b811628d578ab571f4f13e36
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434780"
---
# <a name="clients-supported-for-call-park-in-lync-server-2013"></a><span data-ttu-id="f19c1-103">Clients pris en charge pour le parcage d’appel dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f19c1-103">Clients supported for Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f19c1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f19c1-104">

<span> </span></span></span>

<span data-ttu-id="f19c1-105">_**Dernière modification de la rubrique :** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="f19c1-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<span data-ttu-id="f19c1-106">Cette section identifie les clients qui peuvent être utilisés pour parcr les appels et les clients qui peuvent être utilisés pour récupérer les appels en stationnement.</span><span class="sxs-lookup"><span data-stu-id="f19c1-106">This section identifies the clients that can be used to park calls and the clients that can be used to retrieve parked calls.</span></span>

<div>

## <a name="clients-supported-for-parking-calls"></a><span data-ttu-id="f19c1-107">Clients pris en charge pour le parcage d’appel</span><span class="sxs-lookup"><span data-stu-id="f19c1-107">Clients Supported for Parking Calls</span></span>

<span data-ttu-id="f19c1-108">Les appels de n’importe quel téléphone IP, PBX (autocommutateur privé), PSTN (réseau téléphonique commuté) ou mobile peuvent être parqués.</span><span class="sxs-lookup"><span data-stu-id="f19c1-108">Calls from any IP, private branch exchange (PBX), public switched telephone network (PSTN), or mobile phone can be parked.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f19c1-p101">Seuls les appels audio peuvent être parqués. Aucun parcage pour les messages instantanés et les conférences n’est possible.</span><span class="sxs-lookup"><span data-stu-id="f19c1-p101">Only audio calls can be parked. Instant messages and conferences cannot be parked.</span></span>



</div>

<span data-ttu-id="f19c1-111">Les clients suivants peuvent utiliser le parc d’appels pour les appels de parc :</span><span class="sxs-lookup"><span data-stu-id="f19c1-111">The following clients can use Call Park to park calls:</span></span>

  - <span data-ttu-id="f19c1-112">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="f19c1-112">Lync 2013</span></span>

  - <span data-ttu-id="f19c1-113">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="f19c1-113">Lync 2010</span></span>

  - <span data-ttu-id="f19c1-114">Lync 2010 attendant</span><span class="sxs-lookup"><span data-stu-id="f19c1-114">Lync 2010 Attendant</span></span>

  - <span data-ttu-id="f19c1-115">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="f19c1-115">Lync Phone Edition</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f19c1-116">Les téléphones mobiles ne peuvent pas utiliser le parc d’appels pour Park.</span><span class="sxs-lookup"><span data-stu-id="f19c1-116">Mobile phones cannot use Call Park to park calls.</span></span>



</div>

</div>

<div>

## <a name="clients-supported-for-retrieving-calls"></a><span data-ttu-id="f19c1-117">Clients pris en charge pour la récupération des appels</span><span class="sxs-lookup"><span data-stu-id="f19c1-117">Clients Supported for Retrieving Calls</span></span>

<span data-ttu-id="f19c1-p102">Les plages d’orbites sont configurées en tant que blocs de postes virtuels (postes sans utilisateur ou téléphone attribué). Lorsque vous configurez des orbites sous la forme de postes virtuels, les téléphones mobiles et PSTN ne peuvent pas récupérer des appels parqués.</span><span class="sxs-lookup"><span data-stu-id="f19c1-p102">Orbit ranges are configured as blocks of virtual extensions (extensions without an assigned user or phone). When you configure orbits as virtual extensions, mobile phones and PSTN phones cannot retrieve parked calls.</span></span>

<span data-ttu-id="f19c1-120">Les utilisateurs fédérés ne peuvent pas récupérer des appels parqués.</span><span class="sxs-lookup"><span data-stu-id="f19c1-120">Federated users cannot retrieve parked calls.</span></span>

<span data-ttu-id="f19c1-121">Les clients suivants peuvent récupérer les appels qui sont au parking sur le parc d’appels :</span><span class="sxs-lookup"><span data-stu-id="f19c1-121">The following clients can retrieve calls that are parked on Call Park:</span></span>

  - <span data-ttu-id="f19c1-122">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="f19c1-122">Lync 2013</span></span>

  - <span data-ttu-id="f19c1-123">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="f19c1-123">Lync 2010</span></span>

  - <span data-ttu-id="f19c1-124">Lync 2010 attendant</span><span class="sxs-lookup"><span data-stu-id="f19c1-124">Lync 2010 Attendant</span></span>

  - <span data-ttu-id="f19c1-125">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="f19c1-125">Lync Phone Edition</span></span>

  - <span data-ttu-id="f19c1-126">Téléphones de partie commune IP</span><span class="sxs-lookup"><span data-stu-id="f19c1-126">IP common area phones</span></span>

  - <span data-ttu-id="f19c1-127">Téléphones non IP connectés à l’infrastructure 2013 du serveur Lync, y compris les téléphones portables et les téléphones PBX (Private Branch Exchange)</span><span class="sxs-lookup"><span data-stu-id="f19c1-127">Non-IP phones that are connected to the Lync Server 2013 infrastructure, including common area phones and private branch exchange (PBX) phones</span></span>

<span data-ttu-id="f19c1-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f19c1-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

