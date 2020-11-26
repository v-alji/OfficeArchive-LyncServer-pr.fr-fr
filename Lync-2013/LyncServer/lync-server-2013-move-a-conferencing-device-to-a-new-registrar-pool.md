---
title: 'Lync Server 2013 : déplacer un appareil de conférence vers un nouveau pool d’inscriptions'
description: 'Lync Server 2013 : déplacer un appareil de conférence vers un nouveau pool d’inscriptions.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Move a conferencing device to a new Registrar pool
ms:assetid: 26e02ca3-e881-4f90-8bf0-b13649108100
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994025(v=OCS.15)
ms:contentKeyID: 51803934
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 852e6c53ce86129a25e5831d54b1afb2c87828d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425289"
---
# <a name="move-a-conferencing-device-to-a-new-registrar-pool-in-lync-server-2013"></a><span data-ttu-id="237e4-103">Déplacer un appareil de conférence vers un nouveau pool d’inscriptions dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="237e4-103">Move a conferencing device to a new Registrar pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="237e4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="237e4-104">

<span> </span></span></span>

<span data-ttu-id="237e4-105">_**Dernière modification de la rubrique :** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="237e4-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="237e4-106">Déplacez un appareil de conférence d’un pool d’inscriptions vers un autre à l’aide de l’applet de **passe Move-CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="237e4-106">Move a conferencing device from one Registrar pool to another by using the **Move-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="237e4-107">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="237e4-107">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="237e4-108">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="237e4-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>


<div>

## <a name="moving-a-conferencing-device-to-a-new-registrar-pool"></a><span data-ttu-id="237e4-109">Déplacement d’un appareil de conférence vers un nouveau pool d’inscriptions</span><span class="sxs-lookup"><span data-stu-id="237e4-109">Moving a Conferencing Device to a New Registrar Pool</span></span>

  - <span data-ttu-id="237e4-110">Pour déplacer un appareil de conférence, vous devez spécifier l’identité de la salle à déplacer, puis définir le paramètre Target sur le nom de domaine complet (FQDN) du pool d’inscriptions vers lequel l’appareil sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="237e4-110">To move a conferencing device, you must specify the identity of the room to be moved, and then set the Target parameter to the fully qualified domain name (FQDN) of the Registrar pool the device will be moved to.</span></span> <span data-ttu-id="237e4-111">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="237e4-111">For example:</span></span>
    
        Move-CsMeetingRoom -Target "atl-cs-001.litwareinc.com" -Identity "Room 14"

</div>

<span data-ttu-id="237e4-112">Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de connexion [Move-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Move-CsMeetingRoom) .</span><span class="sxs-lookup"><span data-stu-id="237e4-112">For details, see the Help topic for the [Move-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Move-CsMeetingRoom) cmdlet.</span></span>

<span data-ttu-id="237e4-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="237e4-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

