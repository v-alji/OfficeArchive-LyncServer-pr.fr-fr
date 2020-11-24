---
title: 'Lync Server 2013 : affichage des informations de profil de la stratégie de bande passante réseau'
description: 'Lync Server 2013 : affichage des informations de profil de la stratégie de bande passante réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network bandwidth policy profile information
ms:assetid: eed453fc-04e9-4971-959c-6fad54bf1c96
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721931(v=OCS.15)
ms:contentKeyID: 49733866
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c72a3533ae6f49f91db91b2c3b515c0b5153ec27
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394481"
---
# <a name="viewing-network-bandwidth-policy-profile-information-in-lync-server-2013"></a><span data-ttu-id="9a46d-103">Affichage des informations de profil de la stratégie de bande passante réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a46d-103">Viewing network bandwidth policy profile information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9a46d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9a46d-104">

<span> </span></span></span>

<span data-ttu-id="9a46d-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="9a46d-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="9a46d-106">Dans le cadre du contrôle d’admission des appels (CAC), une stratégie de bande passante est utilisée pour définir des limitations de bande passante pour certaines modalités.</span><span class="sxs-lookup"><span data-stu-id="9a46d-106">As part of call admission control (CAC), a bandwidth policy is used to define bandwidth limitations for certain modalities.</span></span> <span data-ttu-id="9a46d-107">Dans Microsoft Lync Server 2013, seules les modalités d’audio et de vidéo peuvent être affectées par des limitations de bande passante.</span><span class="sxs-lookup"><span data-stu-id="9a46d-107">In Microsoft Lync Server 2013, only audio and video modalities can be assigned bandwidth limitations.</span></span> <span data-ttu-id="9a46d-108">Vous pouvez définir les limites générales de bande passante et les limites de session.</span><span class="sxs-lookup"><span data-stu-id="9a46d-108">You can set overall bandwidth limitations and session limitations.</span></span> <span data-ttu-id="9a46d-109">Vous pouvez utiliser le panneau de configuration de Lync Server pour créer, modifier ou supprimer un profil de conteneur pour ces stratégies.</span><span class="sxs-lookup"><span data-stu-id="9a46d-109">You can use the Lync Server Control Panel to create, modify, or delete a container profile for these policies.</span></span> <span data-ttu-id="9a46d-110">Chaque profil de stratégie de bande passante peut être associé à un ou plusieurs sites réseau.</span><span class="sxs-lookup"><span data-stu-id="9a46d-110">Each bandwidth policy profile can be associated with one or more network sites.</span></span> <span data-ttu-id="9a46d-111">Pour afficher le profil d’une stratégie de bande passante, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="9a46d-111">Use the following procedures to view a bandwidth policy profile.</span></span> <span data-ttu-id="9a46d-112">Pour créer ou modifier un profil de stratégie de bande passante, reportez-vous à [la rubrique création ou modification des profils de stratégie de bande passante dans Lync Server 2013](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="9a46d-112">To create or modify a bandwidth policy profile, see [Creating or modifying bandwidth policy profiles in Lync Server 2013](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md).</span></span>

<div>

## <a name="to-view-a-bandwidth-policy-profile"></a><span data-ttu-id="9a46d-113">Pour afficher un profil de stratégie de bande passante</span><span class="sxs-lookup"><span data-stu-id="9a46d-113">To view a bandwidth policy profile</span></span>

1.  <span data-ttu-id="9a46d-114">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="9a46d-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="9a46d-115">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9a46d-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="9a46d-116">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="9a46d-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="9a46d-117">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis sur **stratégie de bande passante**.</span><span class="sxs-lookup"><span data-stu-id="9a46d-117">In the left navigation bar, click **Network Configuration** and then click **Bandwidth Policy**.</span></span>

4.  <span data-ttu-id="9a46d-118">Dans la page **stratégie de bande passante** , cliquez sur le profil de la stratégie de bande passante que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="9a46d-118">On the **Bandwidth Policy** page, click the bandwidth policy profile that you want to view.</span></span>

5.  <span data-ttu-id="9a46d-119">Dans le menu **Edition**, cliquez sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="9a46d-119">On the **Edit** menu, click **Show details**.</span></span>

</div>

<div>

## <a name="viewing-network-bandwidth-policy-profile-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="9a46d-120">Affichage des informations de profil de la stratégie de bande passante du réseau à l’aide des cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9a46d-120">Viewing Network Bandwidth Policy Profile Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="9a46d-121">Les profils de bande passante réseau peuvent être affichés à l’aide de Windows PowerShell et de l’applet de connexion Get-CsNetworkBandwidthPolicyProfile.</span><span class="sxs-lookup"><span data-stu-id="9a46d-121">Network bandwidth profiles can be viewed by using Windows PowerShell and the Get-CsNetworkBandwidthPolicyProfile cmdlet.</span></span> <span data-ttu-id="9a46d-122">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9a46d-122">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="9a46d-123">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="9a46d-123">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-bandwidth-policy-profile-information"></a><span data-ttu-id="9a46d-124">Pour afficher les informations de profil de la stratégie de bande passante réseau</span><span class="sxs-lookup"><span data-stu-id="9a46d-124">To view network bandwidth policy profile information</span></span>

  - <span data-ttu-id="9a46d-125">Pour afficher des informations sur tous les profils de stratégie de bande passante réseau, tapez la commande suivante dans Lync Server Management Shell, puis appuyez sur entrée :</span><span class="sxs-lookup"><span data-stu-id="9a46d-125">To view information about all your network bandwidth policy profiles, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkBandwidthPolicyProfile
    
    <span data-ttu-id="9a46d-126">Vous obtiendrez des indications semblables à ceci :</span><span class="sxs-lookup"><span data-stu-id="9a46d-126">That will return information similar to this:</span></span>
    
        Identity          : RedmondBandwidthPolicy
        BWPolicy          : {BWLimit=200;BWSessionLimit=200;
                            BWPolicyModality=Audio, 
                            BWLimit=1400;BWSessionLimit=500;
                            BWPolicyModality=Video}
        BWPolicyProfileID : RedmondBandwidthPolicy
        Description       :

</div>

<span data-ttu-id="9a46d-127">Pour plus d’informations, consultez la rubrique d’aide de l’applet de passe [Get-CsNetworkBandwidthPolicyProfile](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile) .</span><span class="sxs-lookup"><span data-stu-id="9a46d-127">For more information, see the help topic for the [Get-CsNetworkBandwidthPolicyProfile](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9a46d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a46d-128">See Also</span></span>


[<span data-ttu-id="9a46d-129">Création ou modification des profils de stratégie de bande passante dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a46d-129">Creating or modifying bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md)  
[<span data-ttu-id="9a46d-130">Supprimer des profils de stratégie de bande passante réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a46d-130">Deleting network bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-deleting-network-bandwidth-policy-profiles.md)  


[<span data-ttu-id="9a46d-131">Configurer le contrôle d’admission des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a46d-131">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)  
  

<span data-ttu-id="9a46d-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9a46d-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

