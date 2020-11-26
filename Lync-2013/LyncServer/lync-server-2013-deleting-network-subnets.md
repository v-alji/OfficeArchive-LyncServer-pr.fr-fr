---
title: 'Lync Server 2013 : suppression de sous-réseaux réseau'
description: 'Lync Server 2013 : suppression de sous-réseaux réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting network subnets
ms:assetid: c1850f38-40a3-48c9-b6f1-f181c5e63b6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721873(v=OCS.15)
ms:contentKeyID: 49733806
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6635ec99b68c4ceb10d1cda343fef35c951bf152
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430279"
---
# <a name="deleting-network-subnets-in-lync-server-2013"></a><span data-ttu-id="d6901-103">Supprimer des sous-réseaux réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6901-103">Deleting network subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d6901-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d6901-104">

<span> </span></span></span>

<span data-ttu-id="d6901-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="d6901-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="d6901-106">Vous pouvez utiliser la procédure suivante pour supprimer un sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="d6901-106">You can use the following procedure to delete a subnet.</span></span> <span data-ttu-id="d6901-107">Dans le panneau de configuration de Lync Server, vous pouvez créer, modifier ou supprimer un sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="d6901-107">From the Lync Server Control Panel, you can create, modify, or delete a network subnet.</span></span> <span data-ttu-id="d6901-108">Pour plus d’informations sur la création et la modification de sous-réseaux réseau, voir [créer ou modifier des sous-réseaux dans Lync Server 2013](lync-server-2013-create-or-modify-network-subnets.md).</span><span class="sxs-lookup"><span data-stu-id="d6901-108">For details on creating or modifying network subnets, see [Create or modify network subnets in Lync Server 2013](lync-server-2013-create-or-modify-network-subnets.md).</span></span>

<span data-ttu-id="d6901-109">Dans la plupart des déploiements de Microsoft Lync Server 2013 sur lequel est implémenté le contrôle d’admission des appels, il existe généralement un grand nombre de sous-réseaux.</span><span class="sxs-lookup"><span data-stu-id="d6901-109">In most deployments of Microsoft Lync Server 2013 where call admission control (CAC) is implemented, there will typically be a large number of subnets.</span></span> <span data-ttu-id="d6901-110">Pour cette raison, il est souvent préférable de configurer les sous-réseaux à partir de Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="d6901-110">Because of this, it is often best to configure subnets from the Lync Server Management Shell.</span></span> <span data-ttu-id="d6901-111">À partir de là, vous pouvez appeler **New-CsNetworkSubnet** conjointement avec l’applet de cmdlet Windows PowerShell **Import-CSV**.</span><span class="sxs-lookup"><span data-stu-id="d6901-111">From there you can call **New-CsNetworkSubnet** in conjunction with the Windows PowerShell cmdlet **Import-CSV**.</span></span> <span data-ttu-id="d6901-112">L’utilisation conjointe de ces applets de passe vous permet de lire les paramètres de sous-réseau à partir d’un fichier de valeurs séparées par des virgules (. csv) et de créer plusieurs sous-réseaux en même temps.</span><span class="sxs-lookup"><span data-stu-id="d6901-112">By using these cmdlets together, you can read in subnet settings from a comma-separated values (.csv) file and create multiple subnets at the same time.</span></span> <span data-ttu-id="d6901-113">Pour obtenir des exemples sur la façon de créer des sous-réseaux à partir d’un fichier. csv, voir [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span><span class="sxs-lookup"><span data-stu-id="d6901-113">For examples of how to create subnets from a .csv file, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<div>

## <a name="to-delete-a-network-subnet"></a><span data-ttu-id="d6901-114">Pour supprimer un sous-réseau du réseau</span><span class="sxs-lookup"><span data-stu-id="d6901-114">To delete a network subnet</span></span>

1.  <span data-ttu-id="d6901-115">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="d6901-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="d6901-116">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d6901-116">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d6901-117">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d6901-117">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d6901-118">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis sur **sous-réseau**.</span><span class="sxs-lookup"><span data-stu-id="d6901-118">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="d6901-119">Dans la page de **sous-réseau** , cliquez sur le sous-réseau que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="d6901-119">On the **Subnet** page, click the subnet that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d6901-120">Vous pouvez supprimer plusieurs sous-réseaux à la fois.</span><span class="sxs-lookup"><span data-stu-id="d6901-120">You can delete more than one subnet at a time.</span></span> <span data-ttu-id="d6901-121">Pour cela, appuyez sur CTRL et sélectionnez plusieurs sous-réseaux tout en maintenant la touche CTRL enfoncée.</span><span class="sxs-lookup"><span data-stu-id="d6901-121">To do this, press CTRL and select multiple subnets while holding down the CTRL key.</span></span> <span data-ttu-id="d6901-122">Pour sélectionner tous les sous-réseaux, cliquez sur <STRONG>tout sélectionner</STRONG> dans le menu <STRONG>Edition</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="d6901-122">Or, to select all subnets, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="d6901-123">Dans le menu **modifier** , cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="d6901-123">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="d6901-124">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6901-124">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d6901-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6901-125">See Also</span></span>


[<span data-ttu-id="d6901-126">Créer ou modifier des sous-réseaux réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6901-126">Create or modify network subnets in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-network-subnets.md)  
  

<span data-ttu-id="d6901-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d6901-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

