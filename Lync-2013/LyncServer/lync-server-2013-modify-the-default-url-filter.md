---
title: 'Lync Server 2013 : modifiez le filtre d’URL par défaut'
description: 'Lync Server 2013 : modifiez le filtre d’URL par défaut.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify the default URL filter
ms:assetid: 80a472b3-054e-45a6-80fc-9ee2bda28ee6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182544(v=OCS.15)
ms:contentKeyID: 48184653
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 079fcc83cd9041f99f1d14663ad51e86f6c23619
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445707"
---
# <a name="modify-the-default-url-filter-in-lync-server-2013"></a><span data-ttu-id="476ad-103">Modifier le filtre d’URL par défaut dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="476ad-103">Modify the default URL filter in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="476ad-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="476ad-104">

<span> </span></span></span>

<span data-ttu-id="476ad-105">_**Dernière modification de la rubrique :** 2012-06-26_</span><span class="sxs-lookup"><span data-stu-id="476ad-105">_**Topic Last Modified:** 2012-06-26_</span></span>

<span data-ttu-id="476ad-106">À l’aide du filtre de messagerie instantanée, Lync Server 2013 fournit un filtre d’URL global qui bloque les URL spécifiques contenues dans les conversations de messagerie instantanée entre les utilisateurs tout au long du déploiement de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="476ad-106">By using the instant messaging (IM) filter, Lync Server 2013 provides a global URL filter that blocks specific URLs contained in IM conversations among users throughout your Lync Server 2013 deployment.</span></span> <span data-ttu-id="476ad-107">Le panneau de configuration de Lync Server vous permet d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="476ad-107">By using Lync Server Control Panel, you can do the following:</span></span>

  - <span data-ttu-id="476ad-108">Bloquer tout ou un sous-ensemble d’URL dans des conversations par messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="476ad-108">Block all or a subset of URLs in instant message conversations.</span></span>

  - <span data-ttu-id="476ad-109">Autoriser toutes les URL.</span><span class="sxs-lookup"><span data-stu-id="476ad-109">Allow all URLs.</span></span> <span data-ttu-id="476ad-110">En option, vous pouvez créer une note insérée au début de chaque message instantané contenant une URL.</span><span class="sxs-lookup"><span data-stu-id="476ad-110">As an option, you can create a notice that is inserted at the beginning of each instant message that contains a URL.</span></span>

  - <span data-ttu-id="476ad-111">Autorisez des URL spécifiques et incluez un avertissement dans chaque message instantané contenant une URL.</span><span class="sxs-lookup"><span data-stu-id="476ad-111">Allow specific URLs and include a warning with each instant message that contains a URL.</span></span>

<span data-ttu-id="476ad-112">De plus, vous pouvez choisir de bloquer les URL qui contiennent des types de fichiers spécifiques, ou bloquer uniquement les URL Internet en autorisant les URL qui se trouvent dans la zone Intranet local du serveur : les URL intranet, qui passent par le serveur.</span><span class="sxs-lookup"><span data-stu-id="476ad-112">In addition, you can choose to block URLs that contain specific file types, or block only Internet URLs by allowing URLs that are within the server’s local intranet zone — intranet URLs — to pass through the server.</span></span> <span data-ttu-id="476ad-113">Pour plus d’informations sur le filtrage d’URL, voir [configuration du transfert de fichiers et du filtrage d’URL pour la messagerie instantanée dans Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span><span class="sxs-lookup"><span data-stu-id="476ad-113">For details about URL filtering, see [Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="476ad-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="476ad-114">See Also</span></span>


[<span data-ttu-id="476ad-115">Configuration du transfert de fichiers et du filtrage d’URL pour la messagerie instantanée dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="476ad-115">Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013</span></span>](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)  
[<span data-ttu-id="476ad-116">Créer un filtre de transfert de fichiers dans Lync Server 2013 pour un site spécifique</span><span class="sxs-lookup"><span data-stu-id="476ad-116">Create a new file transfer filter in Lync Server 2013 for a specific site</span></span>](lync-server-2013-create-a-new-file-transfer-filter-for-a-specific-site.md)  
[<span data-ttu-id="476ad-117">Créer un nouveau filtre d’URL dans Lync Server 2013 pour gérer les liens hypertexte dans les conversations par messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="476ad-117">Create a new URL filter in Lync Server 2013 to handle hyperlinks in IM conversations</span></span>](lync-server-2013-create-a-new-url-filter-to-handle-hyperlinks-in-im-conversations.md)  
[<span data-ttu-id="476ad-118">Modifier le filtre de transfert de fichiers par défaut dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="476ad-118">Modify the default file transfer filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-file-transfer-filter.md)  
  

<span data-ttu-id="476ad-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="476ad-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

