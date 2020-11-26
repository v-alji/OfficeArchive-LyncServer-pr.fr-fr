---
title: 'Lync Server 2013 : afficher les informations de plan de numérotation'
description: 'Lync Server 2013 : afficher les informations de plan de numérotation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View dial plan information
ms:assetid: 25ed0112-a8a7-418a-8c2c-580081be692a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687997(v=OCS.15)
ms:contentKeyID: 49733587
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b4473302b182b8de4ea6aad12d7993cb5d442b7e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423392"
---
# <a name="view-dial-plan-information-in-lync-server-2013"></a><span data-ttu-id="2d439-103">Afficher les informations de plan de numérotation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2d439-103">View dial plan information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2d439-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2d439-104">

<span> </span></span></span>

<span data-ttu-id="2d439-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="2d439-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="2d439-106">Pour afficher des informations pour un plan de numérotation existant, suivez les étapes de la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="2d439-106">To view information for an existing dial plan, perform the steps in the following procedure.</span></span> <span data-ttu-id="2d439-107">Pour créer un nouveau plan de numérotation, reportez-vous à [la rubrique créer un plan de numérotation dans Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="2d439-107">If you want to create a new dial plan, see [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span></span>

<div>

## <a name="to-view-information-about-a-dial-plan-from-lync-server-control-panel"></a><span data-ttu-id="2d439-108">Pour afficher des informations sur un plan de numérotation via le panneau de configuration de Lync Server</span><span class="sxs-lookup"><span data-stu-id="2d439-108">To view information about a dial plan from Lync Server Control Panel</span></span>

1.  <span data-ttu-id="2d439-109">Connectez-vous à l’ordinateur en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre du rôle CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="2d439-109">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="2d439-110">Pour plus d’informations, reportez-vous à la section [délégation des autorisations de configuration dans Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="2d439-110">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="2d439-111">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2d439-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="2d439-112">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2d439-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="2d439-113">Dans la barre de navigation de gauche, cliquez sur **Routage des communications vocales**, puis sur **Plan de numérotation**.</span><span class="sxs-lookup"><span data-stu-id="2d439-113">In the left navigation bar, click **Voice Routing** and then click **Dial Plan**.</span></span>

4.  <span data-ttu-id="2d439-114">Dans la page **Plan de numérotation**, double-cliquez sur le nom d’un plan de numérotation.</span><span class="sxs-lookup"><span data-stu-id="2d439-114">On the **Dial Plan** page, double-click a dial plan name.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2d439-115">Vous pouvez afficher des informations pour un seul plan de numérotation à la fois.</span><span class="sxs-lookup"><span data-stu-id="2d439-115">You can view information for only one dial plan at a time.</span></span>

    
    </div>

</div>

<div>

## <a name="to-view-dial-plans-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="2d439-116">Pour afficher les plans de numérotation à l’aide des cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2d439-116">To view dial plans by using Windows PowerShell cmdlets</span></span>

  - <span data-ttu-id="2d439-117">Les plans de numérotation peuvent être affichés à l’aide de l’interface de ligne de commande Windows PowerShell et de l’applet de commande **Get-CsDialPlan** .</span><span class="sxs-lookup"><span data-stu-id="2d439-117">Dial plans can be viewed by using the Windows PowerShell command-line interface and the **Get-CsDialPlan** cmdlet.</span></span> <span data-ttu-id="2d439-118">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2d439-118">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="2d439-119">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="2d439-119">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>
    
    <span data-ttu-id="2d439-120">Pour afficher des informations sur l’ensemble de vos plans de numérotation, tapez la commande suivante dans Lync Server Management Shell, puis appuyez sur entrée :</span><span class="sxs-lookup"><span data-stu-id="2d439-120">To view information about all your dial plans, type the following command in the Lync Server Management Shell, and then press ENTER:</span></span>
    
        Get-CsDialPlan
    
    <span data-ttu-id="2d439-121">Cette commande renvoie des informations similaires à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="2d439-121">That command will return information similar to this:</span></span>
    
        Identity                 : Global
        Description              :
        DialinConferencingRegion :
        NormalizationRules       : {Description=;
                                   Pattern=^(\d+)$;Translation=$1;Name=
                                   KeepAll;IsInternalExtension=False}
        CountryCode              :
        State                    :
        City                     :
        ExternalAccessPrefix     :
        SimpleName               : DefaultProfile
        OptimizeDeviceDialing    : False

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2d439-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d439-122">See Also</span></span>


[<span data-ttu-id="2d439-123">Créer un plan de numérotation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2d439-123">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)  
[<span data-ttu-id="2d439-124">Modification d’un plan de numérotation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2d439-124">Modify a dial plan in Lync Server 2013</span></span>](lync-server-2013-modify-a-dial-plan.md)  
  

<span data-ttu-id="2d439-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2d439-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

