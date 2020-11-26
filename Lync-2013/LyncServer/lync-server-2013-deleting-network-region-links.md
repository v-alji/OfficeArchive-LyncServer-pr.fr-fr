---
title: 'Lync Server 2013 : suppression de liens de région réseau'
description: 'Lync Server 2013 : suppression de liens de région réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting network region links
ms:assetid: 839273cd-d23f-4b38-84e6-d2dc972f49cd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688114(v=OCS.15)
ms:contentKeyID: 49733712
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5a17c1ec64460e0f7cb447597f94aadd7fd2a9ca
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430286"
---
# <a name="deleting-network-region-links-in-lync-server-2013"></a><span data-ttu-id="e74e4-103">Supprimer des liens de région réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e74e4-103">Deleting network region links in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e74e4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e74e4-104">

<span> </span></span></span>

<span data-ttu-id="e74e4-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="e74e4-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="e74e4-106">Vous pouvez configurer des liens entre deux régions réseau dans le cadre de la commande d’admission des appels (CAC).</span><span class="sxs-lookup"><span data-stu-id="e74e4-106">You can configure links between two network regions as part of call admission control (CAC).</span></span> <span data-ttu-id="e74e4-107">Les régions d’un réseau sont liées par le biais de la connectivité du réseau étendu (WAN) physique.</span><span class="sxs-lookup"><span data-stu-id="e74e4-107">Regions within a network are linked through physical wide area network (WAN) connectivity.</span></span> <span data-ttu-id="e74e4-108">Le panneau de configuration de Lync Server vous permet de supprimer un lien existant entre deux zones du réseau.</span><span class="sxs-lookup"><span data-stu-id="e74e4-108">You can use the Lync Server Control Panel to delete an existing link between two network regions.</span></span> <span data-ttu-id="e74e4-109">Pour plus d’informations sur la création ou la modification du lien de région de réseau, voir [configuration de liens de région réseau dans Lync Server 2013](lync-server-2013-configuring-network-region-links.md)</span><span class="sxs-lookup"><span data-stu-id="e74e4-109">For details about creating or modifying network region link, see [Configuring network region links in Lync Server 2013](lync-server-2013-configuring-network-region-links.md)</span></span>

<div>

## <a name="to-delete-a-network-region-link"></a><span data-ttu-id="e74e4-110">Pour supprimer un lien de zone réseau</span><span class="sxs-lookup"><span data-stu-id="e74e4-110">To delete a network region link</span></span>

1.  <span data-ttu-id="e74e4-111">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="e74e4-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e74e4-112">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e74e4-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e74e4-113">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e74e4-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="e74e4-114">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis sur **liaison de région**.</span><span class="sxs-lookup"><span data-stu-id="e74e4-114">In the left navigation bar, click **Network Configuration** and then click **Region Link**.</span></span>

4.  <span data-ttu-id="e74e4-115">Dans la page de liaison de la **zone** , cliquez sur le lien dans la région que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="e74e4-115">On the **Region Link** page, click the region link that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e74e4-116">Vous pouvez supprimer plusieurs liens vers une région à la fois.</span><span class="sxs-lookup"><span data-stu-id="e74e4-116">You can delete more than one region link at a time.</span></span> <span data-ttu-id="e74e4-117">Pour cela, appuyez sur CTRL et sélectionnez les liens de plusieurs régions tout en maintenant la touche CTRL enfoncée.</span><span class="sxs-lookup"><span data-stu-id="e74e4-117">To do this, press CTRL and select multiple region links while holding down the CTRL key.</span></span> <span data-ttu-id="e74e4-118">Pour sélectionner tous les liens de région, cliquez sur <STRONG>Sélectionner tout</STRONG> dans le menu <STRONG>Edition</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="e74e4-118">Or, to select all region links, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="e74e4-119">Dans le menu **modifier** , sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="e74e4-119">From the **Edit** menu, select **Delete**.</span></span>

6.  <span data-ttu-id="e74e4-120">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e74e4-120">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e74e4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e74e4-121">See Also</span></span>


[<span data-ttu-id="e74e4-122">Configuration de liens de région réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e74e4-122">Configuring network region links in Lync Server 2013</span></span>](lync-server-2013-configuring-network-region-links.md)  
  

<span data-ttu-id="e74e4-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e74e4-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

