---
title: 'Lync Server 2013 : cmdlets serveur Chat permanent'
description: 'Lync Server 2013 : cmdlets Server chat permanent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Persistent Chat Server cmdlets
ms:assetid: 5aa59edb-db57-406f-9fbd-54bf1a55d31b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204920(v=OCS.15)
ms:contentKeyID: 48184226
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28016031ffd4efdc568999ec0a400d77bf628ba8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394688"
---
# <a name="persistent-chat-server-cmdlets-in-lync-server-2013"></a><span data-ttu-id="9e67e-103">Cmdlets Server chat permanent dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e67e-103">Persistent Chat Server cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9e67e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9e67e-104">

<span> </span></span></span>

<span data-ttu-id="9e67e-105">_**Dernière modification de la rubrique :** 2012-06-27_</span><span class="sxs-lookup"><span data-stu-id="9e67e-105">_**Topic Last Modified:** 2012-06-27_</span></span>

<span data-ttu-id="9e67e-106">Les applets de dialogue de chat permanent vous permettent de gérer et de configurer le service Microsoft Lync Server 2013 permanent chat (auparavant appelé service de conversation de groupe).</span><span class="sxs-lookup"><span data-stu-id="9e67e-106">The Persistent Chat cmdlets enable you to manage and configure the Microsoft Lync Server 2013 Persistent Chat service (formerly known as the Group Chat service).</span></span> <span data-ttu-id="9e67e-107">La conversation permanente permet aux utilisateurs de participer à des sessions de messagerie instantanée en ligne.</span><span class="sxs-lookup"><span data-stu-id="9e67e-107">Persistent Chat enables users to participate in online instant messaging sessions.</span></span> <span data-ttu-id="9e67e-108">Même si ces sessions peuvent avoir lieu en temps réel, le contenu de chaque session est persistant ; Cela signifie que ces conversations peuvent être reprises par quiconque à tout moment.</span><span class="sxs-lookup"><span data-stu-id="9e67e-108">Although these sessions can take place in real time, the content of each session is persistent; that means these conversations can be resumed by anyone at any time.</span></span>

<div>

## <a name="persistent-chat-cmdlets"></a><span data-ttu-id="9e67e-109">Cmdlets de chat permanent</span><span class="sxs-lookup"><span data-stu-id="9e67e-109">Persistent Chat Cmdlets</span></span>

<span data-ttu-id="9e67e-110">Les applets de dialogues de chat permanent vous permettent de gérer et de configurer le service de chat permanent de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9e67e-110">The Persistent Chat cmdlets enable you to manage and configure the Lync Server Persistent Chat service.</span></span>

<span data-ttu-id="9e67e-111">**Cmdlets de chat permanent**</span><span class="sxs-lookup"><span data-stu-id="9e67e-111">**Persistent Chat Cmdlets**</span></span>

  - <span data-ttu-id="9e67e-112">[Get-CsAdPrincipal](https://technet.microsoft.com/library/JJ205326(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-112">[Get-CsAdPrincipal](https://technet.microsoft.com/library/JJ205326(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="9e67e-113">[Set-CsPersistentChatActiveServer](https://technet.microsoft.com/library/JJ205065(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-113">[Set-CsPersistentChatActiveServer](https://technet.microsoft.com/library/JJ205065(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="9e67e-114">[Get-CsPersistentChatAddin](https://technet.microsoft.com/library/JJ204670(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-114">[Get-CsPersistentChatAddin](https://technet.microsoft.com/library/JJ204670(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-115">[New-CsPersistentChatAddin](https://technet.microsoft.com/library/JJ204641(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-115">[New-CsPersistentChatAddin](https://technet.microsoft.com/library/JJ204641(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-116">[Remove-CsPersistentChatAddin](https://technet.microsoft.com/library/JJ205350(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-116">[Remove-CsPersistentChatAddin](https://technet.microsoft.com/library/JJ205350(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-117">[Set-CsPersistentChatAddin](https://technet.microsoft.com/library/JJ204721(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-117">[Set-CsPersistentChatAddin](https://technet.microsoft.com/library/JJ204721(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="9e67e-118">[Get-CsPersistentChatCategory](https://technet.microsoft.com/library/JJ204771(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-118">[Get-CsPersistentChatCategory](https://technet.microsoft.com/library/JJ204771(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-119">[New-CsPersistentChatCategory](https://technet.microsoft.com/library/JJ204803(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-119">[New-CsPersistentChatCategory](https://technet.microsoft.com/library/JJ204803(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-120">[Remove-CsPersistentChatCategory](https://technet.microsoft.com/library/JJ204660(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-120">[Remove-CsPersistentChatCategory](https://technet.microsoft.com/library/JJ204660(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-121">[Set-CsPersistentChatCategory](https://technet.microsoft.com/library/JJ204952(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-121">[Set-CsPersistentChatCategory](https://technet.microsoft.com/library/JJ204952(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="9e67e-122">[Get-CsPersistentChatComplianceConfiguration](https://technet.microsoft.com/library/JJ204625(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-122">[Get-CsPersistentChatComplianceConfiguration](https://technet.microsoft.com/library/JJ204625(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-123">[New-CsPersistentChatComplianceConfiguration](https://technet.microsoft.com/library/JJ205163(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-123">[New-CsPersistentChatComplianceConfiguration](https://technet.microsoft.com/library/JJ205163(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-124">[Remove-CsPersistentChatComplianceConfiguration](https://technet.microsoft.com/library/JJ204767(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-124">[Remove-CsPersistentChatComplianceConfiguration](https://technet.microsoft.com/library/JJ204767(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-125">[Set-CsPersistentChatComplianceConfiguration](https://technet.microsoft.com/library/JJ204949(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-125">[Set-CsPersistentChatComplianceConfiguration](https://technet.microsoft.com/library/JJ204949(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="9e67e-126">[Get-CsPersistentChatConfiguration](https://technet.microsoft.com/library/JJ205140(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-126">[Get-CsPersistentChatConfiguration](https://technet.microsoft.com/library/JJ205140(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-127">[New-CsPersistentChatConfiguration](https://technet.microsoft.com/library/JJ205330(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-127">[New-CsPersistentChatConfiguration](https://technet.microsoft.com/library/JJ205330(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-128">[Remove-CsPersistentChatConfiguration](https://technet.microsoft.com/library/JJ204927(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-128">[Remove-CsPersistentChatConfiguration](https://technet.microsoft.com/library/JJ204927(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-129">[Set-CsPersistentChatConfiguration](https://technet.microsoft.com/library/JJ205122(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-129">[Set-CsPersistentChatConfiguration](https://technet.microsoft.com/library/JJ205122(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="9e67e-130">[Export-CsPersistentChatData](https://technet.microsoft.com/library/JJ205378(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-130">[Export-CsPersistentChatData](https://technet.microsoft.com/library/JJ205378(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-131">[Import-CsPersistentChatData](https://technet.microsoft.com/library/JJ204709(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-131">[Import-CsPersistentChatData](https://technet.microsoft.com/library/JJ204709(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="9e67e-132">[Get-CsPersistentChatEligiblePrincipal](https://technet.microsoft.com/library/JJ204891(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-132">[Get-CsPersistentChatEligiblePrincipal](https://technet.microsoft.com/library/JJ204891(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="9e67e-133">[Get-CsPersistentChatEndpoint](https://technet.microsoft.com/library/JJ204764(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-133">[Get-CsPersistentChatEndpoint](https://technet.microsoft.com/library/JJ204764(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-134">[New-CsPersistentChatEndpoint](https://technet.microsoft.com/library/JJ204811(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-134">[New-CsPersistentChatEndpoint](https://technet.microsoft.com/library/JJ204811(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-135">[Remove-CsPersistentChatEndpoint](https://technet.microsoft.com/library/JJ204626(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-135">[Remove-CsPersistentChatEndpoint](https://technet.microsoft.com/library/JJ204626(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="9e67e-136">[Remove-CsPersistentChatMessage](https://technet.microsoft.com/library/JJ204668(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-136">[Remove-CsPersistentChatMessage](https://technet.microsoft.com/library/JJ204668(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-137">[Test-CsPersistentChatMessage](https://technet.microsoft.com/library/JJ204656(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-137">[Test-CsPersistentChatMessage](https://technet.microsoft.com/library/JJ204656(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="9e67e-138">[Get-CsPersistentChatPolicy](https://technet.microsoft.com/library/JJ204673(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-138">[Get-CsPersistentChatPolicy](https://technet.microsoft.com/library/JJ204673(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-139">[Grant-CsPersistentChatPolicy](https://technet.microsoft.com/library/JJ204907(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-139">[Grant-CsPersistentChatPolicy](https://technet.microsoft.com/library/JJ204907(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-140">[New-CsPersistentChatPolicy](https://technet.microsoft.com/library/JJ205396(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-140">[New-CsPersistentChatPolicy](https://technet.microsoft.com/library/JJ205396(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-141">[Remove-CsPersistentChatPolicy](https://technet.microsoft.com/library/JJ205301(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-141">[Remove-CsPersistentChatPolicy](https://technet.microsoft.com/library/JJ205301(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-142">[Set-CsPersistentChatPolicy](https://technet.microsoft.com/library/JJ205192(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-142">[Set-CsPersistentChatPolicy](https://technet.microsoft.com/library/JJ205192(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="9e67e-143">[Clear-CsPersistentChatRoom](https://technet.microsoft.com/library/JJ204976(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-143">[Clear-CsPersistentChatRoom](https://technet.microsoft.com/library/JJ204976(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-144">[Get-CsPersistentChatRoom](https://technet.microsoft.com/library/JJ205123(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-144">[Get-CsPersistentChatRoom](https://technet.microsoft.com/library/JJ205123(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-145">[New-CsPersistentChatRoom](https://technet.microsoft.com/library/JJ205166(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-145">[New-CsPersistentChatRoom](https://technet.microsoft.com/library/JJ205166(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-146">[Remove-CsPersistentChatRoom](https://technet.microsoft.com/library/JJ204639(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-146">[Remove-CsPersistentChatRoom](https://technet.microsoft.com/library/JJ204639(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-147">[Set-CsPersistentChatRoom](https://technet.microsoft.com/library/JJ204801(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-147">[Set-CsPersistentChatRoom](https://technet.microsoft.com/library/JJ204801(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="9e67e-148">[Get-CsPersistentChatState](https://technet.microsoft.com/library/JJ204915(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-148">[Get-CsPersistentChatState](https://technet.microsoft.com/library/JJ204915(v=OCS.15))</span></span>

  - <span data-ttu-id="9e67e-149">[Set-CsPersistentChatState](https://technet.microsoft.com/library/JJ205109(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="9e67e-149">[Set-CsPersistentChatState](https://technet.microsoft.com/library/JJ205109(v=OCS.15))</span></span>

<span data-ttu-id="9e67e-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9e67e-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

