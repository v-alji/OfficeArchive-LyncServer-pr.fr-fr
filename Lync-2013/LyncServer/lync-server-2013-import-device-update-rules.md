---
title: 'Lync Server 2013 : importer les règles de mise à jour de périphériques'
description: 'Lync Server 2013 : importez des règles de mise à jour de périphériques.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Import Device Update rules
ms:assetid: 919e9c87-912b-4bc9-92e7-5998fc2e0bf0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994056(v=OCS.15)
ms:contentKeyID: 51803967
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a7b936a4b7be96332343e8f96134d5ba1b879be
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394900"
---
# <a name="import-device-update-rules-in-lync-server-2013"></a><span data-ttu-id="722bf-103">Importer des règles de mise à jour de périphériques dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="722bf-103">Import Device Update rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="722bf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="722bf-104">

<span> </span></span></span>

<span data-ttu-id="722bf-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="722bf-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="722bf-106">Les règles de mise à jour d’appareils peuvent être importées uniquement à l’aide de Windows PowerShell et de l’applet **de cmdlet Import-CsDeviceUpdate** .</span><span class="sxs-lookup"><span data-stu-id="722bf-106">Device update rules can be imported only by using Windows PowerShell and the **Import-CsDeviceUpdate** cmdlet.</span></span> <span data-ttu-id="722bf-107">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="722bf-107">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="722bf-108">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="722bf-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>


<div>

## <a name="to-import-device-update-rules-to-a-single-web-server"></a><span data-ttu-id="722bf-109">Pour importer des règles de mise à jour de périphériques sur un serveur Web unique</span><span class="sxs-lookup"><span data-stu-id="722bf-109">To import device update rules to a single web server</span></span>

  - <span data-ttu-id="722bf-110">La commande suivante importe les règles de mise à jour de l’appareil sur le serveur Web atl-cs-001.litwareinc.com :</span><span class="sxs-lookup"><span data-stu-id="722bf-110">The following command imports device update rules to the Web server atl-cs-001.litwareinc.com:</span></span>
    
        Import-CsDeviceUpdate -Identity "service:WebServer:atl-cs-001.litwareinc.com" -FileName C:\Updates\UCUpdates.cab

</div>

<div>

## <a name="to-import-device-update-rules-to-all-your-web-servers"></a><span data-ttu-id="722bf-111">Pour importer des règles de mise à jour de périphériques sur tous vos serveurs Web</span><span class="sxs-lookup"><span data-stu-id="722bf-111">To import device update rules to all your web servers</span></span>

  - <span data-ttu-id="722bf-112">Dans cet exemple, les règles de mise à jour d’appareil sont importées sur tous les serveurs Web déployés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="722bf-112">In this example, device update rules are imported to all the Web servers deployed in your organization.</span></span> <span data-ttu-id="722bf-113">Pour que cette commande fonctionne, les \\ \\ mises à jour de ATL-FS-001.litwareinc.com de dossiers \\ doivent être partagées et disponibles pour tous les serveurs Web.</span><span class="sxs-lookup"><span data-stu-id="722bf-113">For this command to work, the folder \\\\atl-fs-001.litwareinc.com\\Updates must be shared and available to all the Web servers.</span></span>
    
        Get-CsService -WebServer | ForEach-Object {Import-CsDeviceUpdate -Identity $_.Identity -FileName \\atl-fs-001.litwareinc.com\Updates\UCUpdates.cab}

</div>

<span data-ttu-id="722bf-114">Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de connexion [Import-CsDeviceUpdate](https://docs.microsoft.com/powershell/module/skype/Import-CsDeviceUpdate) .</span><span class="sxs-lookup"><span data-stu-id="722bf-114">For details, see the Help topic for the [Import-CsDeviceUpdate](https://docs.microsoft.com/powershell/module/skype/Import-CsDeviceUpdate) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="722bf-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="722bf-115">See Also</span></span>


[<span data-ttu-id="722bf-116">Afficher des informations sur les règles de mise à jour des appareils dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="722bf-116">View information about Device Update rules in Lync Server 2013</span></span>](lync-server-2013-view-information-about-device-update-rules.md)  
[<span data-ttu-id="722bf-117">Approuver une règle de mise à jour d’appareil dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="722bf-117">Approve a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-approve-a-device-update-rule.md)  
  

<span data-ttu-id="722bf-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="722bf-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

