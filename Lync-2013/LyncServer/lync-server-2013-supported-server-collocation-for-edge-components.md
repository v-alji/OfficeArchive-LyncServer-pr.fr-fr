---
title: 'Lync Server 2013 : Colocalisation de serveur prise en charge pour les composants Edge'
description: 'Lync Server 2013 : prise en charge de la colocalisation du serveur pour les composants Edge.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported server collocation for edge components
ms:assetid: 435c4dd8-36af-4b71-9b88-3ffcf0fc5c65
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425934(v=OCS.15)
ms:contentKeyID: 48183978
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7bf253e5210e077ca62b3d00f7f130d54d8392a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423637"
---
# <a name="supported-server-collocation-for-edge-components-in-lync-server-2013"></a><span data-ttu-id="e415d-103">Colocalisation de serveur prise en charge pour les composants Edge dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e415d-103">Supported server collocation for edge components in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e415d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e415d-104">

<span> </span></span></span>

<span data-ttu-id="e415d-105">_**Dernière modification de la rubrique :** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="e415d-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="e415d-106">Service Edge d’accès, service Edge de conférence Web, service Edge A/V et service proxy XMPP.</span><span class="sxs-lookup"><span data-stu-id="e415d-106">The Access Edge service, Web Conferencing Edge service, A/V Edge service and XMPP Proxy service are collocated on the Edge Servers.</span></span> <span data-ttu-id="e415d-107">Les serveurs suivants fournissent les fonctions requises pour l’accès des utilisateurs externes et doivent être déployées en tant que serveurs dédiés :</span><span class="sxs-lookup"><span data-stu-id="e415d-107">The following servers provide functions needed for external user access and must be deployed as dedicated servers:</span></span>

  - <span data-ttu-id="e415d-108">serveur Edge</span><span class="sxs-lookup"><span data-stu-id="e415d-108">Edge Server</span></span>

  - <span data-ttu-id="e415d-109">Director (facultatif)</span><span class="sxs-lookup"><span data-stu-id="e415d-109">Director (Optional)</span></span>

  - <span data-ttu-id="e415d-110">Proxy inverse</span><span class="sxs-lookup"><span data-stu-id="e415d-110">Reverse proxy</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="e415d-111">Il n’est pas nécessaire de dédier le proxy inverse au service Lync Server 2013 uniquement.</span><span class="sxs-lookup"><span data-stu-id="e415d-111">The reverse proxy does not need to be dedicated to serving only Lync Server 2013.</span></span> <span data-ttu-id="e415d-112">Par exemple, vous pouvez fournir des services pour publier les services Web de Lync Server et fournir simultanément un site Web publié pour un autre site Web qui n’est pas du tout porteur sur Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e415d-112">For example, you can provide services to publish the Lync Server Web services, and concurrently provide a published Web site for another Web site that has no bearing on Lync Server at all.</span></span> <span data-ttu-id="e415d-113">Si vous disposez déjà d’un serveur proxy inverse dans le réseau de périmètre pour prendre en charge d’autres services, vous pouvez l’utiliser pour Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e415d-113">If you already have a reverse proxy server in the perimeter network to support other services, you can use it for Lync Server 2013.</span></span>



<span data-ttu-id="e415d-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e415d-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

