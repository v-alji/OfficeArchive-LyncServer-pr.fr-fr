---
title: 'Lync Server 2013 : suppression des profils de stratégie de bande passante réseau'
description: 'Lync Server 2013 : suppression des profils de stratégie de bande passante réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting network bandwidth policy profiles
ms:assetid: 4d6beda8-6aa5-4d5e-8a07-363598f0e0c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688050(v=OCS.15)
ms:contentKeyID: 49733643
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69f460d9620158d1857dae41e0033f6d36078868
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430300"
---
# <a name="deleting-network-bandwidth-policy-profiles-in-lync-server-2013"></a><span data-ttu-id="a18cc-103">Supprimer des profils de stratégie de bande passante réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a18cc-103">Deleting network bandwidth policy profiles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a18cc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a18cc-104">

<span> </span></span></span>

<span data-ttu-id="a18cc-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="a18cc-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="a18cc-106">Dans le cadre du contrôle d’admission des appels (CAC), une stratégie de bande passante est utilisée pour définir des limitations de bande passante pour certaines modalités.</span><span class="sxs-lookup"><span data-stu-id="a18cc-106">As part of call admission control (CAC), a bandwidth policy is used to define bandwidth limitations for certain modalities.</span></span> <span data-ttu-id="a18cc-107">Dans Microsoft Lync Server 2013, seules les modalités d’audio et de vidéo peuvent être affectées par des limitations de bande passante.</span><span class="sxs-lookup"><span data-stu-id="a18cc-107">In Microsoft Lync Server 2013, only audio and video modalities can be assigned bandwidth limitations.</span></span> <span data-ttu-id="a18cc-108">Vous pouvez définir les limites générales de bande passante et les limites de session.</span><span class="sxs-lookup"><span data-stu-id="a18cc-108">You can set overall bandwidth limitations and session limitations.</span></span> <span data-ttu-id="a18cc-109">Vous pouvez utiliser le panneau de configuration de Lync Server pour créer, modifier ou supprimer un profil de conteneur pour ces stratégies.</span><span class="sxs-lookup"><span data-stu-id="a18cc-109">You can use the Lync Server Control Panel to create, modify, or delete a container profile for these policies.</span></span> <span data-ttu-id="a18cc-110">Utilisez les procédures suivantes pour supprimer un profil de stratégie de bande passante réseau.</span><span class="sxs-lookup"><span data-stu-id="a18cc-110">Use the following procedures to delete a network bandwidth policy profiles.</span></span> <span data-ttu-id="a18cc-111">Pour plus d’informations sur la création et la modification d’un profil de stratégie de bande passante réseau, voir [création ou modification des profils de stratégie de bande passante dans Lync Server 2013](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="a18cc-111">For details on creating or modifying a network bandwidth policy profile, see [Creating or modifying bandwidth policy profiles in Lync Server 2013](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md).</span></span>

<div>

## <a name="to-delete-a-bandwidth-policy-profile"></a><span data-ttu-id="a18cc-112">Pour supprimer un profil de stratégie de bande passante</span><span class="sxs-lookup"><span data-stu-id="a18cc-112">To delete a bandwidth policy profile</span></span>

1.  <span data-ttu-id="a18cc-113">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="a18cc-113">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="a18cc-114">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a18cc-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="a18cc-115">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="a18cc-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="a18cc-116">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis sur **stratégie de bande passante**.</span><span class="sxs-lookup"><span data-stu-id="a18cc-116">In the left navigation bar, click **Network Configuration** and then click **Bandwidth Policy**.</span></span>

4.  <span data-ttu-id="a18cc-117">Dans la page **stratégie de bande passante** , cliquez sur le profil de la stratégie de bande passante que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="a18cc-117">On the **Bandwidth Policy** page, click the bandwidth policy profile that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a18cc-118">Vous pouvez supprimer plusieurs profils à la fois.</span><span class="sxs-lookup"><span data-stu-id="a18cc-118">You can delete more than one profile at a time.</span></span> <span data-ttu-id="a18cc-119">Pour cela, appuyez sur CTRL et sélectionnez plusieurs profils tout en maintenant la touche CTRL enfoncée.</span><span class="sxs-lookup"><span data-stu-id="a18cc-119">To do this, press CTRL and select multiple profiles while holding down the CTRL key.</span></span> <span data-ttu-id="a18cc-120">Pour sélectionner tous les profils, dans le menu <STRONG>Edition</STRONG> , cliquez sur <STRONG>Sélectionner tout</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="a18cc-120">Or, to select all profiles, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="a18cc-121">Dans le menu **modifier** , cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="a18cc-121">On the **Edit** menu, click **Delete**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="a18cc-122">Vous ne pouvez pas supprimer un profil de stratégie de bande passante associé à un site réseau.</span><span class="sxs-lookup"><span data-stu-id="a18cc-122">You cannot delete a bandwidth policy profile that is associated with a network site.</span></span> <span data-ttu-id="a18cc-123">Vous devez d’abord supprimer l’Association au site du réseau avant de pouvoir supprimer le profil.</span><span class="sxs-lookup"><span data-stu-id="a18cc-123">You must first remove the association with the network site before you can delete the profile.</span></span> <span data-ttu-id="a18cc-124">Pour plus d’informations sur la modification du site réseau, voir <A href="lync-server-2013-creating-or-modifying-network-sites.md">création ou modification des sites réseau dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="a18cc-124">For details about how to modify the network site, see <A href="lync-server-2013-creating-or-modifying-network-sites.md">Creating or modifying network sites in Lync Server 2013</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a18cc-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a18cc-125">See Also</span></span>


[<span data-ttu-id="a18cc-126">Création ou modification des profils de stratégie de bande passante dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a18cc-126">Creating or modifying bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md)  
[<span data-ttu-id="a18cc-127">Affichage des informations de profil de la stratégie de bande passante réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a18cc-127">Viewing network bandwidth policy profile information in Lync Server 2013</span></span>](lync-server-2013-viewing-network-bandwidth-policy-profile-information.md)  


[<span data-ttu-id="a18cc-128">Configurer le contrôle d’admission des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a18cc-128">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)  
[<span data-ttu-id="a18cc-129">Remove-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="a18cc-129">Remove-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkBandwidthPolicyProfile)  
  

<span data-ttu-id="a18cc-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a18cc-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

