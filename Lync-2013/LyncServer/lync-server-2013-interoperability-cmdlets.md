---
title: 'Lync Server 2013 : cmdlets d’interopérabilité'
description: 'Lync Server 2013 : cmdlets d’interopérabilité.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Interoperability cmdlets
ms:assetid: 18444a0b-7b66-4540-a262-775ea10b3b7d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204714(v=OCS.15)
ms:contentKeyID: 48183527
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 50a8bfca7621b76072cce8c68b15e5cc7e3468c4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426780"
---
# <a name="interoperability-cmdlets-in-lync-server-2013"></a><span data-ttu-id="90954-103">Cmdlets d’interopérabilité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="90954-103">Interoperability cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="90954-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="90954-104">

<span> </span></span></span>

<span data-ttu-id="90954-105">_**Dernière modification de la rubrique :** 2012-06-27_</span><span class="sxs-lookup"><span data-stu-id="90954-105">_**Topic Last Modified:** 2012-06-27_</span></span>

<span data-ttu-id="90954-106">Les applets de demande d’interopérabilité permettent de configurer l’authentification et l’autorisation de serveur à serveur entre Microsoft Lync Server 2013 et d’autres produits serveur tels que Microsoft Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="90954-106">The interoperability cmdlets are used to configure server-to-server authentication and authorization between Microsoft Lync Server 2013 and other server products such as Microsoft Exchange Server 2013.</span></span> <span data-ttu-id="90954-107">L’authentification et l’autorisation serveur à serveur permettent à ces serveurs d’échanger et de partager des données en toute transparence.</span><span class="sxs-lookup"><span data-stu-id="90954-107">Server-to-server authentication and authorization enables these servers to seamless exchange and share data.</span></span>

<div>

## <a name="interoperability-cmdlets"></a><span data-ttu-id="90954-108">Cmdlets d’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="90954-108">Interoperability Cmdlets</span></span>

<span data-ttu-id="90954-109">La liste suivante répertorie les applets de commande qui s’associent directement à la configuration et à la gestion de l’interopérabilité entre Microsoft Lync Server 2013 et d’autres produits serveur :</span><span class="sxs-lookup"><span data-stu-id="90954-109">The following is a list of cmdlets that relate directly to configuring and managing interoperability between Microsoft Lync Server 2013 and other server products:</span></span>

<span data-ttu-id="90954-110">**Cmdlets d’interopérabilité**</span><span class="sxs-lookup"><span data-stu-id="90954-110">**Interoperability Cmdlets**</span></span>

  - <span data-ttu-id="90954-111">[Get-CsOAuthConfiguration](https://technet.microsoft.com/library/JJ205155(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="90954-111">[Get-CsOAuthConfiguration](https://technet.microsoft.com/library/JJ205155(v=OCS.15))</span></span>

  - <span data-ttu-id="90954-112">[Set-CsOAuthConfiguration](https://technet.microsoft.com/library/JJ204841(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="90954-112">[Set-CsOAuthConfiguration](https://technet.microsoft.com/library/JJ204841(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="90954-113">[Get-CsOAuthServer](https://technet.microsoft.com/library/JJ205238(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="90954-113">[Get-CsOAuthServer](https://technet.microsoft.com/library/JJ205238(v=OCS.15))</span></span>

  - <span data-ttu-id="90954-114">[New-CsOAuthServer](https://technet.microsoft.com/library/JJ205206(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="90954-114">[New-CsOAuthServer](https://technet.microsoft.com/library/JJ205206(v=OCS.15))</span></span>

  - <span data-ttu-id="90954-115">[Remove-CsOAuthServer](https://technet.microsoft.com/library/JJ205408(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="90954-115">[Remove-CsOAuthServer](https://technet.microsoft.com/library/JJ205408(v=OCS.15))</span></span>

  - <span data-ttu-id="90954-116">[Set-CsOAuthServer](https://technet.microsoft.com/library/JJ204896(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="90954-116">[Set-CsOAuthServer](https://technet.microsoft.com/library/JJ204896(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="90954-117">[Get-CsPartnerApplication](https://technet.microsoft.com/library/JJ205128(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="90954-117">[Get-CsPartnerApplication](https://technet.microsoft.com/library/JJ205128(v=OCS.15))</span></span>

  - <span data-ttu-id="90954-118">[New-CsPartnerApplication](https://technet.microsoft.com/library/JJ204628(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="90954-118">[New-CsPartnerApplication](https://technet.microsoft.com/library/JJ204628(v=OCS.15))</span></span>

  - <span data-ttu-id="90954-119">[Remove-CsPartnerApplication](https://technet.microsoft.com/library/JJ204820(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="90954-119">[Remove-CsPartnerApplication](https://technet.microsoft.com/library/JJ204820(v=OCS.15))</span></span>

  - <span data-ttu-id="90954-120">[Set-CsPartnerApplication](https://technet.microsoft.com/library/JJ204755(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="90954-120">[Set-CsPartnerApplication](https://technet.microsoft.com/library/JJ204755(v=OCS.15))</span></span>

<span data-ttu-id="90954-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="90954-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

