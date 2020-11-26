---
title: 'Lync Server 2013 : activation ou désactivation d’un appareil de conférence'
description: 'Lync Server 2013 : activation ou désactivation d’un appareil de conférence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable a conferencing device
ms:assetid: d5140e38-d015-4706-9bde-cf2fa748c36b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994070(v=OCS.15)
ms:contentKeyID: 51803981
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 761bc19536c889cced68ff586753f6800df0da59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437573"
---
# <a name="enable-or-disable-a-conferencing-device-in-lync-server-2013"></a><span data-ttu-id="92367-103">Activer ou désactiver un appareil de conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="92367-103">Enable or disable a conferencing device in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="92367-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="92367-104">

<span> </span></span></span>

<span data-ttu-id="92367-105">_**Dernière modification de la rubrique :** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="92367-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="92367-106">Activez et désactivez un appareil de conférence à l’aide de l’applet de passe **Enable-CsMeetingRoom** et de l’applet **de passe CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="92367-106">Enable and disable a conferencing device by using the **Enable-CsMeetingRoom** cmdlet and the **Disable-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="92367-107">Ces applets de commande peuvent être exécutées à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="92367-107">These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="92367-108">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="92367-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>


<div>

## <a name="enabling-a-conferencing-device"></a><span data-ttu-id="92367-109">Activation d’un appareil de conférence</span><span class="sxs-lookup"><span data-stu-id="92367-109">Enabling a Conferencing Device</span></span>

  - <span data-ttu-id="92367-110">Pour activer un appareil de conférence, vous pouvez utiliser l’applet de passe **Enable-CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="92367-110">To enable a conferencing device, use the **Enable-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="92367-111">Dans le cadre de l’activation d’un appareil de conférence, vous devez inclure a) l’identité de l’appareil de conférence, b) le pool d’inscriptions dans lequel le compte de la salle sera hébergé et c) l’adresse SIP à attribuer à ce compte.</span><span class="sxs-lookup"><span data-stu-id="92367-111">When enabling a conferencing device, you must include a) the conferencing device identity, b) the Registrar pool where the room account will be homed, and c) the SIP address to be assigned to that account.</span></span>
    
        Enable-CsMeetingRoom -Identity "Redmond Conferencing device" -RegistrarPool "atl-cs-001.litwareinc.com" -SipAddress "sip:RedmondMeetingRoom@litwareinc.com"

</div>

<div>

## <a name="disabling-a-conferencing-device"></a><span data-ttu-id="92367-112">Désactivation d’un appareil de conférence</span><span class="sxs-lookup"><span data-stu-id="92367-112">Disabling a Conferencing Device</span></span>

  - <span data-ttu-id="92367-113">Pour désactiver un appareil de conférence, vous pouvez utiliser l’applet de vue **Disable-CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="92367-113">To disable a conferencing device, use the **Disable-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="92367-114">Veillez à spécifier l’identité de l’appareil de conférence à désactiver :</span><span class="sxs-lookup"><span data-stu-id="92367-114">Make sure that you specify the identity of the conferencing device to be disabled:</span></span>
    
        Disable-CsMeetingRoom -Identity "sip:RedmondMeetingRoom@litwareinc.com"

</div>

<span data-ttu-id="92367-115">Pour plus d’informations, consultez les rubriques d’aide de l’applet de connexion [Enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) et de l’applet de connexion [Disable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Disable-CsMeetingRoom) .</span><span class="sxs-lookup"><span data-stu-id="92367-115">For details, see the Help topics for the [Enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) cmdlet and the [Disable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Disable-CsMeetingRoom) cmdlet.</span></span>

<span data-ttu-id="92367-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="92367-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

