---
title: 'Lync Server 2013 : affichage des informations relatives au site réseau'
description: 'Lync Server 2013 : affichage des informations relatives au site réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network site information
ms:assetid: 24a97d98-b168-4016-81bf-c2c478092b87
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687996(v=OCS.15)
ms:contentKeyID: 49733586
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b46dc91510cb5ff737977871470033374573ba8c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440401"
---
# <a name="viewing-network-site-information-in-lync-server-2013"></a><span data-ttu-id="f9d4d-103">Affichage des informations sur le site réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9d4d-103">Viewing network site information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f9d4d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f9d4d-104">

<span> </span></span></span>

<span data-ttu-id="f9d4d-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="f9d4d-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="f9d4d-106">Les sites réseau sont les bureaux ou les emplacements configurés dans chaque région d’un contrôle d’admission des appels (CAC) ou un déploiement 9-1-1 amélioré.</span><span class="sxs-lookup"><span data-stu-id="f9d4d-106">Network sites are the offices or locations configured within each region of a call admission control (CAC) or Enhanced 9-1-1 deployment.</span></span> <span data-ttu-id="f9d4d-107">Vous pouvez consulter les informations relatives à un site réseau dans Lync Server 2013 Control Panel ou Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="f9d4d-107">You can view network site information in either Lync Server 2013 Control Panel or Lync Server Management Shell .</span></span> <span data-ttu-id="f9d4d-108">Pour plus d’informations sur la création et la modification de sites réseau, voir [création ou modification de sites réseau dans Lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md).</span><span class="sxs-lookup"><span data-stu-id="f9d4d-108">For details about creating or modifying network sites, see [Creating or modifying network sites in Lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md).</span></span>

<div>

## <a name="to-view-network-site-information-in-lync-server-control-panel"></a><span data-ttu-id="f9d4d-109">Pour afficher les informations de site réseau dans le panneau de configuration de Lync Server</span><span class="sxs-lookup"><span data-stu-id="f9d4d-109">To view network site information in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="f9d4d-110">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="f9d4d-110">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="f9d4d-111">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f9d4d-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f9d4d-112">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="f9d4d-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f9d4d-113">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis cliquez sur **site**.</span><span class="sxs-lookup"><span data-stu-id="f9d4d-113">In the left navigation bar, click **Network Configuration** and then click **Site**.</span></span>

4.  <span data-ttu-id="f9d4d-114">Sur la page du **site** , cliquez sur le site que vous voulez afficher.</span><span class="sxs-lookup"><span data-stu-id="f9d4d-114">On the **Site** page, click the site that you want to view.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f9d4d-115">Vous ne pouvez afficher que les informations relatives à un site à la fois.</span><span class="sxs-lookup"><span data-stu-id="f9d4d-115">You can only view information for one site at a time.</span></span>

    
    </div>

5.  <span data-ttu-id="f9d4d-116">Dans le menu **Edition**, cliquez sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="f9d4d-116">On the **Edit** menu, click **Show details**.</span></span>

</div>

<div>

## <a name="viewing-network-site-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="f9d4d-117">Affichage des informations sur le site réseau à l’aide des cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9d4d-117">Viewing Network Site Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="f9d4d-118">Vous pouvez afficher les informations sur le site réseau à l’aide de Windows PowerShell et de l’applet de connexion Get-CsNetworkSite.</span><span class="sxs-lookup"><span data-stu-id="f9d4d-118">You can view network site information by using Windows PowerShell and the Get-CsNetworkSite cmdlet.</span></span> <span data-ttu-id="f9d4d-119">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f9d4d-119">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="f9d4d-120">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="f9d4d-120">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-site-information"></a><span data-ttu-id="f9d4d-121">Pour afficher les informations relatives au site réseau</span><span class="sxs-lookup"><span data-stu-id="f9d4d-121">To view network site information</span></span>

  - <span data-ttu-id="f9d4d-122">Pour afficher des informations sur tous les sites de votre réseau, tapez la commande suivante dans Lync Server Management Shell, puis appuyez sur entrée :</span><span class="sxs-lookup"><span data-stu-id="f9d4d-122">To view information about all your network sites, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkSite
    
    <span data-ttu-id="f9d4d-123">Vous obtiendrez des indications semblables à ceci :</span><span class="sxs-lookup"><span data-stu-id="f9d4d-123">That will return information similar to this:</span></span>
    
        Identity          : Redmond
        NetworkSiteID     : Redmond
        Description       :
        NetworkRegionID   : Pacific Northwest
        BypassID          : 3b232b84-2c1d-4da2-8181-e9330bafebe9
        BWPolicyProfileID :
        LocationPolicy    :

</div>

<span data-ttu-id="f9d4d-124">Pour plus d’informations, consultez la rubrique d’aide de l’applet de passe [Get-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSite) .</span><span class="sxs-lookup"><span data-stu-id="f9d4d-124">For more information, see the help topic for the [Get-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSite) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f9d4d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9d4d-125">See Also</span></span>


[<span data-ttu-id="f9d4d-126">Création ou modification de sites réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9d4d-126">Creating or modifying network sites in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-sites.md)  
[<span data-ttu-id="f9d4d-127">Suppression d’un site réseau existant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9d4d-127">Deleting an existing network site in Lync Server 2013</span></span>](lync-server-2013-deleting-an-existing-network-site.md)  
  

<span data-ttu-id="f9d4d-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f9d4d-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

