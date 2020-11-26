---
title: 'Lync Server 2013 : cmdlets de routage statique'
description: 'Lync Server 2013 : cmdlets de routage statique.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Static routing cmdlets
ms:assetid: 71d5e0cd-8412-4383-818a-95b851a4da4b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg416492(v=OCS.15)
ms:contentKeyID: 48184496
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 33fd251f63111cebb9297287252e666a7e10f0e1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423686"
---
# <a name="static-routing-cmdlets-in-lync-server-2013"></a><span data-ttu-id="d75a7-103">Cmdlets de routage statique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d75a7-103">Static routing cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d75a7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d75a7-104">

<span> </span></span></span>

<span data-ttu-id="d75a7-105">_**Dernière modification de la rubrique :** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="d75a7-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="d75a7-106">Les itinéraires statiques permettent aux administrateurs de prédéterminer les itinéraires réseau pris par les messages SIP.</span><span class="sxs-lookup"><span data-stu-id="d75a7-106">With static routes, administrators can predetermine the network routes taken by SIP messages.</span></span> <span data-ttu-id="d75a7-107">Lorsqu’un message est reçu par un serveur, le serveur vérifie l’adresse du message, puis transfère le message au serveur du tronçon suivant préconfiguré par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="d75a7-107">When a message is received by a server, the server checks the message address and then forwards the message to the next hop server preconfigured by an administrator.</span></span> <span data-ttu-id="d75a7-108">S’il est configuré correctement, les itinéraires statiques permettent de garantir l’exactitude et la précision de la remise des messages, et le préentendement minimal placé sur les serveurs.</span><span class="sxs-lookup"><span data-stu-id="d75a7-108">If configured correctly, static routes help ensure timely, and accurate, delivery of messages, and with minimal overheard placed on servers.</span></span>

<div>

## <a name="static-routing-cmdlets"></a><span data-ttu-id="d75a7-109">Cmdlets de routage statique</span><span class="sxs-lookup"><span data-stu-id="d75a7-109">Static Routing Cmdlets</span></span>

<span data-ttu-id="d75a7-110">Sauf disposition contraire du support technique de Microsoft, les itinéraires statiques configurés pour Microsoft Lync Server 2013 doivent être créés à l’aide de l’applet [de commande New-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="d75a7-110">Unless otherwise instructed by Microsoft support personnel, static routes configured for Microsoft Lync Server 2013 should be created using the [New-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15)) cmdlet.</span></span> <span data-ttu-id="d75a7-111">Après la création d’un itinéraire, vous pouvez utiliser les applets de CsStaticRoutingConfiguration pour ajouter cet itinéraire à une collection de routage statique.</span><span class="sxs-lookup"><span data-stu-id="d75a7-111">After a route has been created, you can then use the CsStaticRoutingConfiguration cmdlets to add that route to a static routing collection.</span></span>

<span data-ttu-id="d75a7-112">**Routage statique**</span><span class="sxs-lookup"><span data-stu-id="d75a7-112">**Static Routing**</span></span>

  - <span></span>  
    <span data-ttu-id="d75a7-113">[Get-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg398130(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d75a7-113">[Get-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg398130(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="d75a7-114">[New-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg413041(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d75a7-114">[New-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg413041(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="d75a7-115">[Remove-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg412932(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d75a7-115">[Remove-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg412932(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="d75a7-116">[Set-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg425895(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d75a7-116">[Set-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg425895(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="d75a7-117">[New-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d75a7-117">[New-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="d75a7-118">[Get-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398754(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d75a7-118">[Get-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398754(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="d75a7-119">[Nouveau-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg425811(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d75a7-119">[New-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg425811(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="d75a7-120">[Remove-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398668(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d75a7-120">[Remove-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398668(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="d75a7-121">[Set-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398724(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d75a7-121">[Set-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398724(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="d75a7-122">[Nouveau-CsSipProxyCustom](https://technet.microsoft.com/library/Gg425904(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d75a7-122">[New-CsSipProxyCustom](https://technet.microsoft.com/library/Gg425904(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="d75a7-123">[Nouveau-CsSipProxyRealm](https://technet.microsoft.com/library/Gg413084(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d75a7-123">[New-CsSipProxyRealm](https://technet.microsoft.com/library/Gg413084(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="d75a7-124">[Nouveau-CsSipProxyTCP](https://technet.microsoft.com/library/Gg425745(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d75a7-124">[New-CsSipProxyTCP](https://technet.microsoft.com/library/Gg425745(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="d75a7-125">[Nouveau-CsSipProxyTLS](https://technet.microsoft.com/library/Gg398629(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d75a7-125">[New-CsSipProxyTLS](https://technet.microsoft.com/library/Gg398629(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="d75a7-126">[Nouveau-CsSipProxyTransport](https://technet.microsoft.com/library/Gg398489(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d75a7-126">[New-CsSipProxyTransport](https://technet.microsoft.com/library/Gg398489(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="d75a7-127">[Nouveau-CsSipProxyUseDefault](https://technet.microsoft.com/library/Gg398274(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d75a7-127">[New-CsSipProxyUseDefault](https://technet.microsoft.com/library/Gg398274(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="d75a7-128">[Nouveau-CsSipProxyUseDefaultCert](https://technet.microsoft.com/library/Gg425858(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d75a7-128">[New-CsSipProxyUseDefaultCert](https://technet.microsoft.com/library/Gg425858(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="d75a7-129">[Nouveau-CsIssuedCertId](https://technet.microsoft.com/library/Gg425814(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d75a7-129">[New-CsIssuedCertId](https://technet.microsoft.com/library/Gg425814(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d75a7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d75a7-130">See Also</span></span>


[<span data-ttu-id="d75a7-131">Blog Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="d75a7-131">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="d75a7-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d75a7-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

