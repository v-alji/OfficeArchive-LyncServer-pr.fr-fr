---
title: 'Lync Server 2013 : affichage des informations de liaison de la zone réseau'
description: 'Lync Server 2013 : affichage des informations sur les liens de la région réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network region link information
ms:assetid: 7b6b2ea2-83d8-4376-afb2-70e5d2cf6444
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688102(v=OCS.15)
ms:contentKeyID: 49733701
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0134ded9942ebda91050c1f7b0bbcfef018451a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446204"
---
# <a name="viewing-network-region-link-information-in-lync-server-2013"></a><span data-ttu-id="a66cb-103">Affichage des informations sur les liens de région réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a66cb-103">Viewing network region link information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a66cb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a66cb-104">

<span> </span></span></span>

<span data-ttu-id="a66cb-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="a66cb-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="a66cb-106">Vous pouvez afficher les liens entre deux régions réseau dans le cadre du contrôle d’admission des appels (CAC).</span><span class="sxs-lookup"><span data-stu-id="a66cb-106">You can view links between two network regions as part of call admission control (CAC).</span></span> <span data-ttu-id="a66cb-107">Les régions d’un réseau sont liées par le biais de la connectivité du réseau étendu (WAN) physique.</span><span class="sxs-lookup"><span data-stu-id="a66cb-107">Regions within a network are linked through physical wide area network (WAN) connectivity.</span></span> <span data-ttu-id="a66cb-108">Vous pouvez utiliser le panneau de configuration de Lync Server pour afficher un lien existant entre deux zones du réseau.</span><span class="sxs-lookup"><span data-stu-id="a66cb-108">You can use the Lync Server Control Panel to view an existing link between two network regions.</span></span> <span data-ttu-id="a66cb-109">Pour plus d’informations sur la création ou la modification d’un lien de région réseau, voir [configurer les liens de région réseau dans Lync Server 2013](lync-server-2013-configuring-network-region-links.md).</span><span class="sxs-lookup"><span data-stu-id="a66cb-109">For details about creating or modifying network region link, see [Configuring network region links in Lync Server 2013](lync-server-2013-configuring-network-region-links.md).</span></span>

<div>

## <a name="to-view-a-network-region-link-in-lync-server-control-panel"></a><span data-ttu-id="a66cb-110">Pour afficher un lien de région réseau dans le panneau de configuration de Lync Server</span><span class="sxs-lookup"><span data-stu-id="a66cb-110">To view a network region link in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="a66cb-111">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="a66cb-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="a66cb-112">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a66cb-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="a66cb-113">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="a66cb-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="a66cb-114">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis sur **liaison de région**.</span><span class="sxs-lookup"><span data-stu-id="a66cb-114">In the left navigation bar, click **Network Configuration** and then click **Region Link**.</span></span>

4.  <span data-ttu-id="a66cb-115">Dans la page de liaison de la **zone** , cliquez sur le lien de la région que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="a66cb-115">On the **Region Link** page, click the region link that you want to view.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a66cb-116">Vous pouvez uniquement afficher des informations sur un lien de région à la fois.</span><span class="sxs-lookup"><span data-stu-id="a66cb-116">You can only view information about one region link at a time.</span></span>

    
    </div>

5.  <span data-ttu-id="a66cb-117">Dans le menu **édition** , cliquez sur **afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="a66cb-117">From the **Edit** menu, select **Show details**.</span></span>

</div>

<div>

## <a name="viewing-network-region-link-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="a66cb-118">Affichage d’informations sur les liaisons de région réseau à l’aide d’applets de requête Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a66cb-118">Viewing Network Region Link Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="a66cb-119">Vous pouvez afficher les liens de région réseau à l’aide de Windows PowerShell et de l’applet **de requête get-CsNetworkRegionLink** .</span><span class="sxs-lookup"><span data-stu-id="a66cb-119">You can view network region links by using Windows PowerShell and the **Get-CsNetworkRegionLink** cmdlet.</span></span> <span data-ttu-id="a66cb-120">Vous pouvez exécuter cette applet de commande sur Lync Server 2013 Management Shell ou à partir d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a66cb-120">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="a66cb-121">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="a66cb-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-region-link-information"></a><span data-ttu-id="a66cb-122">Pour afficher les informations sur le lien dans la région réseau</span><span class="sxs-lookup"><span data-stu-id="a66cb-122">To view network region link information</span></span>

  - <span data-ttu-id="a66cb-123">Pour afficher des informations sur tous les liens de votre région réseau, tapez la commande suivante dans Lync Server Management Shell, puis appuyez sur entrée :</span><span class="sxs-lookup"><span data-stu-id="a66cb-123">To view information about all your network region links, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkRegionLink
    
    <span data-ttu-id="a66cb-124">Cette commande renvoie le type d’informations suivant :</span><span class="sxs-lookup"><span data-stu-id="a66cb-124">This command returns information similar to the following:</span></span>
    
        Identity            : NorthwestToCalifornia
        BWPolicyProfileID   :
        NetworkRegionLinkID : NorthwestToCalifornia
        NetworkRegionID1    : Pacific Northwest
        NetworkRegionID2    : California

</div>

<span data-ttu-id="a66cb-125">Pour plus d’informations, consultez la rubrique [Get-CsNetworkRegionLink](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink).</span><span class="sxs-lookup"><span data-stu-id="a66cb-125">For details, see [Get-CsNetworkRegionLink](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a66cb-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a66cb-126">See Also</span></span>


[<span data-ttu-id="a66cb-127">Configuration de liens de site réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a66cb-127">Configuring network site links in Lync Server 2013</span></span>](lync-server-2013-configuring-network-site-links.md)  
  

<span data-ttu-id="a66cb-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a66cb-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

