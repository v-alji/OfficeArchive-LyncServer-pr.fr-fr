---
title: 'Lync Server 2013 : Remarques sur la migration et la coexistence pour IPv6'
description: 'Lync Server 2013 : considérations de migration et de coexistence pour IPv6.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration and coexistence considerations for IPv6
ms:assetid: 8c769c4f-c8a9-4cbf-9080-beee3be9848a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205068(v=OCS.15)
ms:contentKeyID: 48184751
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e8618cc14ff3c2467ea41df34e39f5094d1206dc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394985"
---
# <a name="migration-and-coexistence-considerations-for-ipv6-in-lync-server-2013"></a><span data-ttu-id="51586-103">Remarques sur la migration et la coexistence pour IPv6 dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51586-103">Migration and coexistence considerations for IPv6 in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="51586-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="51586-104">

<span> </span></span></span>

<span data-ttu-id="51586-105">_**Dernière modification de la rubrique :** 2012-06-14_</span><span class="sxs-lookup"><span data-stu-id="51586-105">_**Topic Last Modified:** 2012-06-14_</span></span>

<span data-ttu-id="51586-106">Le protocole IP version 6 (IPv6) n’est pas pris en charge sur Lync Server 2010 ou Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="51586-106">IP version 6 (IPv6) is not supported on Lync Server 2010 or Office Communications Server.</span></span> <span data-ttu-id="51586-107">Dans le cadre de la phase de test, vous pouvez tester le coexistence de Lync Server 2010 et de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="51586-107">For piloting purposes, you can test Lync Server 2010 and Lync Server 2013 dual-stack coexistence.</span></span> <span data-ttu-id="51586-108">Nous vous recommandons d’effectuer la mise à niveau de tous les pools pour un site central vers Lync Server 2013 avant d’activer le protocole IPv6 (réseau à double pile) pour tous les pools.</span><span class="sxs-lookup"><span data-stu-id="51586-108">We recommend that all pools for a given central site are upgraded to Lync Server 2013 before you enable IPv6 (dual-stack network) for any of the pools.</span></span> <span data-ttu-id="51586-109">Si vous devez configurer un pool uniquement pour IPv6, nous recommandons que vous configuriez un pool IPv6 uniquement dans votre environnement de laboratoire pour le test.</span><span class="sxs-lookup"><span data-stu-id="51586-109">If you need to configure a pool for IPv6 only, we recommend that you set up an IPv6-only pool in your lab environment for testing.</span></span>

<span data-ttu-id="51586-110">Les scénarios suivants sont pris en charge pendant la migration et la coexistence :</span><span class="sxs-lookup"><span data-stu-id="51586-110">The following scenarios are supported during migration and coexistence:</span></span>

  - <span data-ttu-id="51586-111">Lync Server 2013, Lync Server 2010 et les pools Office Communications Server 2007 R2 en mode IPv4, coexistence de Lync Server 2013 en mode double pile.</span><span class="sxs-lookup"><span data-stu-id="51586-111">Lync Server 2013, Lync Server 2010, and Office Communications Server 2007 R2 pools in IPv4 mode, coexisting with Lync Server 2013 in dual-stack mode.</span></span>

  - <span data-ttu-id="51586-112">Pool Lync Server 2013 en mode IPv6 uniquement, si le pool IPv6 uniquement est silo.</span><span class="sxs-lookup"><span data-stu-id="51586-112">Lync Server 2013 pool in IPv6-only mode, if the IPv6-only pool is siloed.</span></span>

<span data-ttu-id="51586-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="51586-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

