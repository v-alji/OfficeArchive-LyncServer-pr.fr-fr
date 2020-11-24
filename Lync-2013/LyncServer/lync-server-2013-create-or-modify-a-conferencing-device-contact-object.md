---
title: 'Lync Server 2013 : création ou modification d’un objet de contact de périphérique de conférence'
description: 'Lync Server 2013 : création ou modification d’un objet de contact d’appareil de conférence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a conferencing device Contact object
ms:assetid: 62ed64be-379c-417d-9453-511881cf5604
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994035(v=OCS.15)
ms:contentKeyID: 51803945
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 853ee1c7dfda2fda99431b8cc1a5210a51f39a4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394377"
---
# <a name="create-or-modify-a-conferencing-device-contact-object-in-lync-server-2013"></a><span data-ttu-id="59c17-103">Créer ou modifier un objet de contact de l’appareil de conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="59c17-103">Create or modify a conferencing device Contact object in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="59c17-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="59c17-104">

<span> </span></span></span>

<span data-ttu-id="59c17-105">_**Dernière modification de la rubrique :** 2013-10-02_</span><span class="sxs-lookup"><span data-stu-id="59c17-105">_**Topic Last Modified:** 2013-10-02_</span></span>

<span data-ttu-id="59c17-106">Pour créer un objet de salle de conférence, commencez par créer un compte d’utilisateur Active Directory pour représenter l’appareil.</span><span class="sxs-lookup"><span data-stu-id="59c17-106">To create a conferencing room object, first create an Active Directory user account to represent the device.</span></span> <span data-ttu-id="59c17-107">Vous pouvez ensuite utiliser l’applet de passe **Enable-CsMeetingRoom** pour permettre au compte de fonctionner en tant qu’appareil de conférence.</span><span class="sxs-lookup"><span data-stu-id="59c17-107">Then, use the **Enable-CsMeetingRoom** cmdlet to enable that account to function as a conferencing device.</span></span> <span data-ttu-id="59c17-108">Si vous devez modifier les propriétés d’un appareil de conférence existant, utilisez l’applet de passe **Set-CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="59c17-108">If you need to change the properties of an existing conferencing device, use the **Set-CsMeetingRoom** cmdlet.</span></span>

<span data-ttu-id="59c17-109">Ces applets de commande peuvent être exécutées à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="59c17-109">These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="59c17-110">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="59c17-110">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>


<div>

## <a name="creating-a-conferencing-device"></a><span data-ttu-id="59c17-111">Création d’un périphérique de conférence</span><span class="sxs-lookup"><span data-stu-id="59c17-111">Creating a Conferencing Device</span></span>

  - <span data-ttu-id="59c17-112">Une fois que vous avez créé le compte d’utilisateur Active Directory qui représente le nouvel appareil de conférence, activez-le à l’aide de l’applet de contrôle **Enable-CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="59c17-112">After you create the Active Directory user account that represents the new conferencing device, enable it by using the **Enable-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="59c17-113">N’oubliez pas d’inclure a) l’identité de l’appareil de conférence, b) du pool de bureaux d’enregistrement dans lequel le compte de la salle sera hébergé et l’adresse SIP doit être attribuée à ce compte.</span><span class="sxs-lookup"><span data-stu-id="59c17-113">Be sure to include a) the conferencing device identity, b) the registrar pool where the room account will be homed, and c) the SIP address to be assigned to that account.</span></span> <span data-ttu-id="59c17-114">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="59c17-114">For example:</span></span>
    
        Enable-CsMeetingRoom -Identity "Redmond Conferencing device" -RegistrarPool "atl-cs-001.litwareinc.com" -SipAddress "sip:RedmondMeetingRoom@litwareinc.com"

</div>

<div>

## <a name="modifying-a-conferencing-device"></a><span data-ttu-id="59c17-115">Modification d’un appareil de conférence</span><span class="sxs-lookup"><span data-stu-id="59c17-115">Modifying a Conferencing Device</span></span>

  - <span data-ttu-id="59c17-116">Pour modifier les valeurs de propriétés d’un appareil de conférence existant, utilisez l’applet de passe **Set-CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="59c17-116">To modify the property values of an existing conferencing device, use the **Set-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="59c17-117">Par exemple, la commande suivante met à jour le numéro de téléphone (LineUri) associé à un appareil de conférence :</span><span class="sxs-lookup"><span data-stu-id="59c17-117">For example, the following command updates the phone number (LineUri) associated with a conferencing device:</span></span>
    
        Set-CsMeetingRoom -Identity "Redmond Conferencing device" -LineUri "tel:+12065551219"

</div>

<span data-ttu-id="59c17-118">Pour plus d’informations, consultez les rubriques d’aide de l’applet de connexion [Enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) et de l’applet de connexion [Set-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Set-CsMeetingRoom) .</span><span class="sxs-lookup"><span data-stu-id="59c17-118">For details, see the Help topics for the [Enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) cmdlet and the [Set-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Set-CsMeetingRoom) cmdlet.</span></span>

<span data-ttu-id="59c17-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="59c17-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

