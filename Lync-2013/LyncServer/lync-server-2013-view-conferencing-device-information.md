---
title: 'Lync Server 2013 : afficher les informations de périphérique de conférence'
description: 'Lync Server 2013 : afficher des informations sur l’appareil de conférence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View conferencing device information
ms:assetid: 838bdbf8-8b68-4eb6-8fa3-45bfd5b0b1cd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994043(v=OCS.15)
ms:contentKeyID: 51803954
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9bbbdcecbc15ef59b2b9e22ffd2b28ff745d67a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443369"
---
# <a name="view-conferencing-device-information-in-lync-server-2013"></a><span data-ttu-id="e0c99-103">Afficher les informations de périphérique de conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0c99-103">View conferencing device information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e0c99-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e0c99-104">

<span> </span></span></span>

<span data-ttu-id="e0c99-105">_**Dernière modification de la rubrique :** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="e0c99-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="e0c99-106">Vous pouvez afficher des informations sur les appareils de conférence configurés pour une utilisation au sein de votre organisation à l’aide de Windows PowerShell et de l’applet **de passe Get-CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="e0c99-106">You can view information about the conferencing devices configured for use in your organization by using Windows PowerShell and the **Get-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="e0c99-107">Exécutez l’applet de commande **Get-CsMeetingRoom** à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e0c99-107">Run the **Get-CsMeetingRoom** cmdlet from either the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e0c99-108">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="e0c99-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<span data-ttu-id="e0c99-109">Si vous utilisez l’applet de passe **Get-CsMeetingRoom** sans aucun paramètre, elle renvoie des informations sur tous vos périphériques de conférence.</span><span class="sxs-lookup"><span data-stu-id="e0c99-109">If you use the **Get-CsMeetingRoom** cmdlet without any parameters, it returns information about all your conferencing devices.</span></span> <span data-ttu-id="e0c99-110">Les paramètres facultatifs permettent de filtrer les informations de différentes manières.</span><span class="sxs-lookup"><span data-stu-id="e0c99-110">Optional parameters provide different ways for you to filter information.</span></span> <span data-ttu-id="e0c99-111">Pour plus d’informations, consultez la section paramètres de [Get-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingRoom).</span><span class="sxs-lookup"><span data-stu-id="e0c99-111">For details, see the Parameters section of [Get-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingRoom).</span></span>

<div>


<div>

## <a name="viewing-information-about-all-your-conferencing-devices"></a><span data-ttu-id="e0c99-112">Affichage d’informations sur tous vos périphériques de conférence</span><span class="sxs-lookup"><span data-stu-id="e0c99-112">Viewing Information about All Your Conferencing Devices</span></span>

  - <span data-ttu-id="e0c99-113">Pour afficher les détails de tous vos appareils de conférence, tapez la commande suivante dans Lync Server Management Shell, puis appuyez sur entrée :</span><span class="sxs-lookup"><span data-stu-id="e0c99-113">To view details about all your conferencing devices, type the following command in the Lync Server Management Shell, and then press Enter:</span></span>
    
        Get-CsMeetingRoom
    
    <span data-ttu-id="e0c99-114">Cette applet de commande renvoie des informations similaires à ce qui suit pour chaque appareil de conférence.</span><span class="sxs-lookup"><span data-stu-id="e0c99-114">This cmdlet returns information similar to the following for each conferencing device.</span></span> <span data-ttu-id="e0c99-115">Notez que l’exemple ci-après illustre les informations que vous verrez lors de l’exécution de cette cmdlet :</span><span class="sxs-lookup"><span data-stu-id="e0c99-115">Note that this example shows only some of the information that you’ll see when you run this cmdlet:</span></span>
    
        ContactOptionFlags                : 64
        OwnerUrn                          : urn:device:roomsystem
        OriginatorSid                     :
        SamAccountName                    : room12129
        UserPrincipalName                 : room1219@litwareinc.com
        FirstName                         : 
        LastName                          :
        WindowsEmailAddress               :
        Sid                               : S-1-5-21-2831376166-2963252556-2165051629-1257
        LineServerURI                     :
        AudioVideoDisabled                : False
        IPPBXSoftPhoneRoutingEnabled      : False
        RemoteCallControlTelephonyEnabled : False
        PrivateLine                       :
        AcpInfo                           : {}
        HostedVoiceMail                   :
        DisplayName                       : Room 1219

</div>

<div>

## <a name="viewing-information-about-a-specific-conferencing-device"></a><span data-ttu-id="e0c99-116">Affichage d’informations sur un appareil de conférence spécifique</span><span class="sxs-lookup"><span data-stu-id="e0c99-116">Viewing Information about a Specific Conferencing Device</span></span>

  - <span data-ttu-id="e0c99-117">Pour afficher des informations pour un appareil de conférence spécifique, incluez le paramètre Identity suivi de l’identité de l’appareil de conférence (en général, le nom d’affichage Active Directory).</span><span class="sxs-lookup"><span data-stu-id="e0c99-117">To view information for a specific conferencing device, include the Identity parameter followed by the conferencing device identity (typically, the Active Directory display name).</span></span> <span data-ttu-id="e0c99-118">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e0c99-118">For example:</span></span>
    
        Get-CsMeetingRoom -Identity "Room 1219"

</div>

<span data-ttu-id="e0c99-119">Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de connexion [Get-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingRoom) .</span><span class="sxs-lookup"><span data-stu-id="e0c99-119">For details, see the Help topic for the [Get-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingRoom) cmdlet.</span></span>

<span data-ttu-id="e0c99-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e0c99-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

