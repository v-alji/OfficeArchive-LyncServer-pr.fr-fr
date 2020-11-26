---
title: 'Lync Server 2013 : affichage des informations de région réseau'
description: 'Lync Server 2013 : affichage des informations relatives à la région du réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network region information
ms:assetid: 665740d0-a3ed-460f-8337-5ed945f90589
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688076(v=OCS.15)
ms:contentKeyID: 49733672
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 225cafc392b9b9d0c23f3882d530ad6d2b59f165
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446275"
---
# <a name="viewing-network-region-information-in-lync-server-2013"></a><span data-ttu-id="6d6a0-103">Affichage des informations de région réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6d6a0-103">Viewing network region information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6d6a0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6d6a0-104">

<span> </span></span></span>

<span data-ttu-id="6d6a0-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="6d6a0-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="6d6a0-106">Une région réseau interconnecte diverses parties d’un réseau à plusieurs zones géographiques.</span><span class="sxs-lookup"><span data-stu-id="6d6a0-106">A network region interconnects various parts of a network across multiple geographic areas.</span></span> <span data-ttu-id="6d6a0-107">Chaque région du réseau doit être associée à un site central.</span><span class="sxs-lookup"><span data-stu-id="6d6a0-107">Every network region must be associated with a central site.</span></span> <span data-ttu-id="6d6a0-108">Le site central est le site du centre de données sur lequel le service de stratégie de bande passante de contrôle d’admission des appels (CAC) est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6d6a0-108">The central site is the data center site on which the call admission control (CAC) bandwidth policy service is running.</span></span> <span data-ttu-id="6d6a0-109">Vous pouvez utiliser le panneau de configuration de Lync Server pour afficher les régions du réseau.</span><span class="sxs-lookup"><span data-stu-id="6d6a0-109">You can use Lync Server Control Panel to view network regions.</span></span> <span data-ttu-id="6d6a0-110">Les régions réseau incluent des paramètres qui déterminent si d’autres chemins d’accès via Internet sont autorisés pour les connexions audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="6d6a0-110">Network regions include settings that determine whether alternate paths through the Internet are allowed for audio and video connections.</span></span> <span data-ttu-id="6d6a0-111">Utilisez cette rubrique pour afficher les régions réseau existantes.</span><span class="sxs-lookup"><span data-stu-id="6d6a0-111">Use this topic to view existing network regions.</span></span> <span data-ttu-id="6d6a0-112">Pour plus d’informations sur la création ou la modification de régions réseau existantes, voir [création ou modification des régions réseau dans Lync Server 2013](lync-server-2013-creating-or-modifying-network-regions.md).</span><span class="sxs-lookup"><span data-stu-id="6d6a0-112">For details about creating or modifying existing network regions, see [Creating or modifying network regions in Lync Server 2013](lync-server-2013-creating-or-modifying-network-regions.md).</span></span>

<div>

## <a name="to-view-information-about-a-network-region-with-lync-server-control-panel"></a><span data-ttu-id="6d6a0-113">Pour afficher des informations sur une région réseau avec le panneau de configuration de Lync Server</span><span class="sxs-lookup"><span data-stu-id="6d6a0-113">To view information about a network region with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="6d6a0-114">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="6d6a0-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="6d6a0-115">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6d6a0-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="6d6a0-116">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6d6a0-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="6d6a0-117">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis cliquez sur **région**.</span><span class="sxs-lookup"><span data-stu-id="6d6a0-117">In the left navigation bar, click **Network Configuration** and then click **Region**.</span></span>

4.  <span data-ttu-id="6d6a0-118">Dans la page **zone** , cliquez sur la zone que vous voulez afficher.</span><span class="sxs-lookup"><span data-stu-id="6d6a0-118">On the **Region** page, click the region you want to view.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="6d6a0-119">Vous ne pouvez afficher qu’une région à la fois.</span><span class="sxs-lookup"><span data-stu-id="6d6a0-119">You can only view one region at a time.</span></span>

    
    </div>

5.  <span data-ttu-id="6d6a0-120">Dans le menu **Edition**, cliquez sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="6d6a0-120">On the **Edit** menu, click **Show details**.</span></span>

</div>

<div>

## <a name="viewing-network-region-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="6d6a0-121">Affichage des informations de région du réseau à l’aide des cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6d6a0-121">Viewing Network Region Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="6d6a0-122">Vous pouvez afficher les informations relatives à la région du réseau à l’aide de Windows PowerShell et de l’applet **de requête get-CsNetworkRegion** .</span><span class="sxs-lookup"><span data-stu-id="6d6a0-122">You can view network region information by using Windows PowerShell and the **Get-CsNetworkRegion** cmdlet.</span></span> <span data-ttu-id="6d6a0-123">Vous pouvez exécuter cette applet de commande sur Lync Server 2013 Management Shell ou à partir d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6d6a0-123">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="6d6a0-124">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="6d6a0-124">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-region-information"></a><span data-ttu-id="6d6a0-125">Pour afficher les informations relatives aux régions du réseau</span><span class="sxs-lookup"><span data-stu-id="6d6a0-125">To view network region information</span></span>

  - <span data-ttu-id="6d6a0-126">Pour afficher des informations sur toutes les régions de votre réseau, tapez la commande suivante dans Lync Server Management Shell, puis appuyez sur entrée :</span><span class="sxs-lookup"><span data-stu-id="6d6a0-126">To view information about all your network regions, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkRegion
    
    <span data-ttu-id="6d6a0-127">Vous obtiendrez des indications semblables à ceci :</span><span class="sxs-lookup"><span data-stu-id="6d6a0-127">That will return information similar to this:</span></span>
    
        Identity         : Pacific Northwest
        Description      :
        BypassID         : 3b232b84-2c1d-4da2-8181-e9330bafebe9
        CentralSite      : Site:Redmond1
        BWAlternatePaths : {BWPolicyModality=Audio;AlternatePath=True, 
                           BWPolicyModality=Video;AlternatePath=True}
        NetworkRegionID  : Pacific Northwest

</div>

<span data-ttu-id="6d6a0-128">Pour plus d’informations, consultez la rubrique d’aide de l’applet de passe [Get-CsNetworkRegion](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink) .</span><span class="sxs-lookup"><span data-stu-id="6d6a0-128">For more information, see the help topic for the [Get-CsNetworkRegion](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6d6a0-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d6a0-129">See Also</span></span>


[<span data-ttu-id="6d6a0-130">Création ou modification des régions réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6d6a0-130">Creating or modifying network regions in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-regions.md)  
[<span data-ttu-id="6d6a0-131">Supprimer des zones réseau existantes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6d6a0-131">Deleting existing network regions in Lync Server 2013</span></span>](lync-server-2013-deleting-existing-network-regions.md)  
  

<span data-ttu-id="6d6a0-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6d6a0-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

