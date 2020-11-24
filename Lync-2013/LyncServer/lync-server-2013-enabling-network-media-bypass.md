---
title: 'Lync Server 2013 : activation du contournement de média réseau'
description: 'Lync Server 2013 : activation du contournement de média réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling network media bypass
ms:assetid: 95c4fa06-49d3-41ac-acdc-7dcda66e5508
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182552(v=OCS.15)
ms:contentKeyID: 48184846
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1218376903aa42e1ea55205e3a9e8d16aade9a3a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394713"
---
# <a name="enabling-network-media-bypass-in-lync-server-2013"></a><span data-ttu-id="a966c-103">Activation du contournement de média réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a966c-103">Enabling network media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a966c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a966c-104">

<span> </span></span></span>

<span data-ttu-id="a966c-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="a966c-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="a966c-106">Les paramètres de contournement de média s’appliquent globalement dans le déploiement de Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a966c-106">Media bypass settings apply globally across a Microsoft Lync Server 2013 deployment.</span></span> <span data-ttu-id="a966c-107">Bypass Media accepte les appels pour ignorer le serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="a966c-107">Media bypass allows calls to bypass the Mediation Server.</span></span> <span data-ttu-id="a966c-108">Pour plus d’informations sur l’utilisation du contournement du contenu multimédia, voir [planification d’une dérivation multimédia dans Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) dans la section planification.</span><span class="sxs-lookup"><span data-stu-id="a966c-108">For details about when to use Media bypass, see [Planning for media bypass in Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) in the Planning section.</span></span>

<span data-ttu-id="a966c-109">Vous pouvez activer et configurer le contournement multimédia à partir du panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a966c-109">You can enable and configure media bypass from the Lync Server Control Panel.</span></span>

<div>

## <a name="to-enable-and-configure-media-bypass"></a><span data-ttu-id="a966c-110">Pour activer et configurer le contournement multimédia</span><span class="sxs-lookup"><span data-stu-id="a966c-110">To enable and configure media bypass</span></span>

1.  <span data-ttu-id="a966c-111">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="a966c-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="a966c-112">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a966c-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="a966c-113">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="a966c-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="a966c-114">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis sur **Global**.</span><span class="sxs-lookup"><span data-stu-id="a966c-114">In the left navigation bar, click **Network Configuration** and then click **Global**.</span></span>

4.  <span data-ttu-id="a966c-115">Dans la page **Global** , cliquez sur configuration **globale** .</span><span class="sxs-lookup"><span data-stu-id="a966c-115">On the **Global** page, click the **Global** configuration.</span></span> <span data-ttu-id="a966c-116">Il n’y a toujours qu’une seule configuration et elle est toujours nommée global.</span><span class="sxs-lookup"><span data-stu-id="a966c-116">There is always only one configuration, and it is always named Global.</span></span>

5.  <span data-ttu-id="a966c-117">Dans le menu **édition** , cliquez sur **afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="a966c-117">On the **Edit** menu, click **View details**.</span></span>

6.  <span data-ttu-id="a966c-118">Dans la page **modifier le paramètre global** , activez la case à cocher **activer le contournement du contenu multimédia** .</span><span class="sxs-lookup"><span data-stu-id="a966c-118">On the **Edit Global Setting** page, click the **Enable media bypass** check box.</span></span>

7.  <span data-ttu-id="a966c-119">Sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="a966c-119">Select one of the following options:</span></span>
    
      - <span data-ttu-id="a966c-120">**Contournement permanent**   Sélectionnez cette option pour essayer la dérivation multimédia sur tous les appels.</span><span class="sxs-lookup"><span data-stu-id="a966c-120">**Always bypass**   Select this option to attempt media bypass on all calls.</span></span> <span data-ttu-id="a966c-121">Cette option n’est pas disponible si le contrôle d’admission des appels (CAC) est activé.</span><span class="sxs-lookup"><span data-stu-id="a966c-121">This option will be unavailable if call admission control (CAC) is enabled.</span></span> <span data-ttu-id="a966c-122">Si le CAC n’est pas activé, sélectionnez cette option dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a966c-122">If CAC is not enabled, select this option in the following situations:</span></span>
        
          - <span data-ttu-id="a966c-123">Le contrôle de la bande passante n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a966c-123">There is no need for bandwidth control.</span></span>
        
          - <span data-ttu-id="a966c-124">Il n’est pas nécessaire de disposer d’une configuration précise pour déterminer le moment où un contournement se produit.</span><span class="sxs-lookup"><span data-stu-id="a966c-124">There is no need for fine-grained configuration to determine when bypass should happen.</span></span>
        
          - <span data-ttu-id="a966c-125">Il existe une connectivité complète entre les passerelles et les clients.</span><span class="sxs-lookup"><span data-stu-id="a966c-125">There is full connectivity between gateways and clients.</span></span>
    
      - <span data-ttu-id="a966c-126">**Utiliser la configuration des sites et des régions**   Si le CAC est activé, cette option est activée par défaut et ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="a966c-126">**Use sites and region configuration**   If CAC is enabled, this option is selected by default and cannot be changed.</span></span> <span data-ttu-id="a966c-127">Lorsque cette option est sélectionnée, les sites et les régions de configuration réseau sont utilisés pour déterminer à quel moment une dérivation de média est possible.</span><span class="sxs-lookup"><span data-stu-id="a966c-127">When this option is selected, network configuration sites and regions will be used to determine when media bypass is possible.</span></span> <span data-ttu-id="a966c-128">Si vous sélectionnez cette option, vous pouvez choisir d’activer le contournement pour les sites qui ne sont pas mappés.</span><span class="sxs-lookup"><span data-stu-id="a966c-128">If you select this option, you can choose to enable bypass for sites that are not mapped.</span></span> <span data-ttu-id="a966c-129">Activez la case à cocher **activer le contournement pour les sites non mappés** uniquement si vous avez un ou plusieurs sites de grande taille associés à la même région qui n’ont pas de contraintes de bande passante (par exemple, un site central de grande taille) et si des sites de succursales sont également associés à la même région qui comporte des contraintes de bande passante.</span><span class="sxs-lookup"><span data-stu-id="a966c-129">Click the **Enable bypass for non-mapped sites** check box only if you have one or more large sites associated with the same region that do not have bandwidth constraints (for example, a large central site) and you also have some branch sites associated with the same region that do have bandwidth constraints.</span></span> <span data-ttu-id="a966c-130">Lorsque vous activez le contournement pour les sites non mappés, la configuration est simplifiée, car vous spécifiez uniquement les sous-réseaux associés aux sites de succursale plutôt que d’indiquer tous les sous-réseaux associés à tous les sites.</span><span class="sxs-lookup"><span data-stu-id="a966c-130">When you enable bypass for non-mapped sites, configuration is streamlined because you specify only the subnets associated with the branch sites rather than needing to specify all subnets associated with all sites.</span></span> <span data-ttu-id="a966c-131">Nous vous recommandons de ne pas activer la case à cocher **activer le contournement pour les sites non mappés** si le CAC est activé.</span><span class="sxs-lookup"><span data-stu-id="a966c-131">We recommend that you do not select the **Enable bypass for non-mapped sites** check box if CAC is enabled.</span></span>

8.  <span data-ttu-id="a966c-132">Cliquez sur **valider** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="a966c-132">Click **Commit** to save your changes.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a966c-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a966c-133">See Also</span></span>


[<span data-ttu-id="a966c-134">Désactivation de la contournement de média réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a966c-134">Disabling network media bypass in Lync Server 2013</span></span>](lync-server-2013-disabling-network-media-bypass.md)  


[<span data-ttu-id="a966c-135">Options de contournement global de médias dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a966c-135">Global media bypass options in Lync Server 2013</span></span>](lync-server-2013-global-media-bypass-options.md)  


[<span data-ttu-id="a966c-136">Planification de la déviation du trafic multimédia dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a966c-136">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="a966c-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a966c-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

