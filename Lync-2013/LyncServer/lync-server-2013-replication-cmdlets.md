---
title: 'Lync Server 2013 : cmdlets de réplication'
description: 'Lync Server 2013 : cmdlets de réplication.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Replication cmdlets
ms:assetid: e0c49601-d2a3-45a1-b05c-26c7ff820708
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415677(v=OCS.15)
ms:contentKeyID: 48185527
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b253176101de61a07630ec141a318dd114776392
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395069"
---
# <a name="replication-cmdlets-in-lync-server-2013"></a><span data-ttu-id="27013-103">Cmdlets de réplication dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27013-103">Replication cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="27013-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="27013-104">

<span> </span></span></span>

<span data-ttu-id="27013-105">_**Dernière modification de la rubrique :** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="27013-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="27013-106">Les applets de contrôle de réplication vous permettent de surveiller et de gérer la réplication de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="27013-106">The replication cmdlets provide a way for you to both monitor and manage Lync Server replication.</span></span> <span data-ttu-id="27013-107">Vous pouvez utiliser ces applets de applet pour configurer les paramètres de réplication. pour surveiller la progression de la réplication ; pour forcer manuellement la réplication sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="27013-107">You can use these cmdlets to configure replication settings; to monitor replication progress; and to manually force replication on a server.</span></span>

<div>

## <a name="replication-cmdlets"></a><span data-ttu-id="27013-108">Cmdlets de réplication</span><span class="sxs-lookup"><span data-stu-id="27013-108">Replication Cmdlets</span></span>

<span data-ttu-id="27013-109">Voici une liste des applets de commande qui concernent directement la gestion de la réplication :</span><span class="sxs-lookup"><span data-stu-id="27013-109">The following is a list of cmdlets that relate directly to managing replication:</span></span>

<span data-ttu-id="27013-110">**Duplication**</span><span class="sxs-lookup"><span data-stu-id="27013-110">**Replication**</span></span>

  - <span></span>  
    <span data-ttu-id="27013-111">[Debug-CsInterPoolReplication](https://technet.microsoft.com/library/JJ619185(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="27013-111">[Debug-CsInterPoolReplication](https://technet.microsoft.com/library/JJ619185(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="27013-112">[Invoke-CsManagementStoreReplication](https://technet.microsoft.com/library/Gg413060(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="27013-112">[Invoke-CsManagementStoreReplication](https://technet.microsoft.com/library/Gg413060(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="27013-113">[Get-CsManagementStoreReplicationStatus](https://technet.microsoft.com/library/Gg399052(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="27013-113">[Get-CsManagementStoreReplicationStatus](https://technet.microsoft.com/library/Gg399052(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="27013-114">[Enable-CsReplica](https://technet.microsoft.com/library/Gg425965(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="27013-114">[Enable-CsReplica](https://technet.microsoft.com/library/Gg425965(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="27013-115">[Test-CsReplica](https://technet.microsoft.com/library/JJ205289(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="27013-115">[Test-CsReplica](https://technet.microsoft.com/library/JJ205289(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="27013-116">[Get-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg398548(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="27013-116">[Get-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg398548(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="27013-117">[Nouveau-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg399059(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="27013-117">[New-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg399059(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="27013-118">[Remove-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg425738(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="27013-118">[Remove-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg425738(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="27013-119">[Set-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg398540(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="27013-119">[Set-CsUserReplicatorConfiguration](https://technet.microsoft.com/library/Gg398540(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="27013-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27013-120">See Also</span></span>


[<span data-ttu-id="27013-121">Blog Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="27013-121">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="27013-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="27013-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

