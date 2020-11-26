---
title: 'Lync Server 2013 : gestion du contrôle d’admission des appels'
description: 'Lync Server 2013 : gestion du contrôle d’admission des appels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing call admission control
ms:assetid: b0bd4783-6f47-408d-b010-2e30f9bc1770
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721851(v=OCS.15)
ms:contentKeyID: 49733784
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0a1c01bff6d1dce48dea314b6704cc0f5ff7d6b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425961"
---
# <a name="managing-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="2ea69-103">Gestion du contrôle d’admission des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ea69-103">Managing call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2ea69-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2ea69-104">

<span> </span></span></span>

<span data-ttu-id="2ea69-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="2ea69-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="2ea69-106">Le contrôle d’admission des appels détermine, en fonction de la bande passante réseau disponible, si des sessions de communication en temps réel, telles que des appels vocaux ou vidéo, peuvent être établies.</span><span class="sxs-lookup"><span data-stu-id="2ea69-106">Call admission control (CAC) determines, based on available network bandwidth, whether to allow real-time communications sessions such as voice or video calls to be established.</span></span> <span data-ttu-id="2ea69-107">Utilisez les procédures suivantes pour gérer différentes fonctionnalités CAC pour votre environnement Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2ea69-107">Use the following procedures to manage different CAC features for your Lync Server 2013 environment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2ea69-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="2ea69-108">In This Section</span></span>

  - [<span data-ttu-id="2ea69-109">Activation du contrôle d’admission des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ea69-109">Enabling call admission control in Lync Server 2013</span></span>](lync-server-2013-enabling-call-admission-control.md)

  - [<span data-ttu-id="2ea69-110">Gestion des profils de stratégie de bande passante réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ea69-110">Managing network bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-managing-network-bandwidth-policy-profiles.md)

  - [<span data-ttu-id="2ea69-111">Régions réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ea69-111">Network regions in Lync Server 2013</span></span>](lync-server-2013-network-regions.md)

  - [<span data-ttu-id="2ea69-112">Itinéraires de région réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ea69-112">Network region routes in Lync Server 2013</span></span>](lync-server-2013-network-region-routes.md)

  - [<span data-ttu-id="2ea69-113">Contrôle d’admission des appels pour les sites dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ea69-113">Call admission control for sites in Lync Server 2013</span></span>](lync-server-2013-call-admission-control-for-sites.md)

  - [<span data-ttu-id="2ea69-114">Activation et désactivation de la contournement multimédia dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ea69-114">Enabling and disabling media bypass in Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-media-bypass.md)

  - [<span data-ttu-id="2ea69-115">Liaison des régions réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ea69-115">Linking network regions in Lync Server 2013</span></span>](lync-server-2013-linking-network-regions.md)

  - [<span data-ttu-id="2ea69-116">Gestion des sous-réseaux réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ea69-116">Managing network subnets in Lync Server 2013</span></span>](lync-server-2013-managing-network-subnets.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2ea69-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ea69-117">See Also</span></span>


[<span data-ttu-id="2ea69-118">Vue d’ensemble du contrôle d’admission des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ea69-118">Overview of call admission control in Lync Server 2013</span></span>](lync-server-2013-overview-of-call-admission-control.md)  
  

<span data-ttu-id="2ea69-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2ea69-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

