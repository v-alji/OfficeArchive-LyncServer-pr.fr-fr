---
title: Vérifier les informations de topologie
description: Vérifiez les informations de topologie.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify topology information
ms:assetid: aa4c424e-f87c-4be6-8df6-a0cd193b11fc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205151(v=OCS.15)
ms:contentKeyID: 48185046
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2ed41cd95fffdca629e710dcf443631d0c74c69e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440117"
---
# <a name="verify-topology-information"></a><span data-ttu-id="b4e9f-103">Vérifier les informations de topologie</span><span class="sxs-lookup"><span data-stu-id="b4e9f-103">Verify topology information</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b4e9f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b4e9f-104">

<span> </span></span></span>

<span data-ttu-id="b4e9f-105">_**Dernière modification de la rubrique :** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="b4e9f-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="b4e9f-106">La première étape de vérification réussie du publipostage consiste à afficher les informations sur la topologie Office Communications Server 2007 R2 que vous avez fusionnées avec Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b4e9f-106">The first step in verifying the merge completed successfully is to view the Office Communications Server 2007 R2 topology information that you merged with Lync Server 2013.</span></span> <span data-ttu-id="b4e9f-107">Dans le générateur de topologie, le nœud **BackCompatSite** affiche le nom de domaine complet (FQDN) de chaque pool et serveur Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="b4e9f-107">In Topology Builder, the **BackCompatSite** node displays the fully qualified domain name (FQDN) of each Office Communications Server 2007 R2 pool and server that you merged.</span></span>

<div>

## <a name="to-view-backcompatsite-in-topology-builder"></a><span data-ttu-id="b4e9f-108">Pour afficher BackCompatSite dans le générateur de topologie</span><span class="sxs-lookup"><span data-stu-id="b4e9f-108">To view BackCompatSite in Topology Builder</span></span>

1.  <span data-ttu-id="b4e9f-109">Dans votre environnement Office Communications Server 2007 R2, ouvrez l’outil d’administration Office Communications Server 2007 R2 et notez les noms de domaine complets des pools et serveurs hérités.</span><span class="sxs-lookup"><span data-stu-id="b4e9f-109">In your Office Communications Server 2007 R2 environment, open the Office Communications Server 2007 R2 administrative tool and note the FQDNs of the legacy pools and servers.</span></span>

2.  <span data-ttu-id="b4e9f-110">Dans votre environnement Lync Server 2013, ouvrez le générateur de topologie et développez le nœud **BackCompatSite** .</span><span class="sxs-lookup"><span data-stu-id="b4e9f-110">In your Lync Server 2013 environment, open Topology Builder and then expand the **BackCompatSite** node.</span></span>

3.  <span data-ttu-id="b4e9f-111">Vérifiez que les noms de domaine complets des pools et des serveurs que vous fusionnez sont affichés.</span><span class="sxs-lookup"><span data-stu-id="b4e9f-111">Verify that the FQDNs for the pools and servers that you merge are displayed.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b4e9f-112">Aucune information n’apparaît dans <STRONG>BackCompatSite</STRONG> pour les rôles serveur colocalisés sur un serveur frontal ou un serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="b4e9f-112">You do not see any information in <STRONG>BackCompatSite</STRONG> for server roles that are collocated on a Front End Server or Standard Edition server.</span></span> <span data-ttu-id="b4e9f-113">Seuls les rôles de serveur requis pour l’interopérabilité entre Office Communications Server 2007 R2 et Lync Server 2013 sont affichés.</span><span class="sxs-lookup"><span data-stu-id="b4e9f-113">Only server roles that are required for interoperability between Office Communications Server 2007 R2 and Lync Server 2013 are shown.</span></span>

    
    </div>

<span data-ttu-id="b4e9f-114">![Boîte de dialogue BackCompatSite de générateur de topologie](images/JJ205243.62751c76-f018-4c6d-bb48-c61ef8974d31(OCS.15).jpg "Boîte de dialogue BackCompatSite de générateur de topologie")</span><span class="sxs-lookup"><span data-stu-id="b4e9f-114">![Topology Builder BackCompatSite dialog box](images/JJ205243.62751c76-f018-4c6d-bb48-c61ef8974d31(OCS.15).jpg "Topology Builder BackCompatSite dialog box")</span></span>

<span data-ttu-id="b4e9f-115">Vous pouvez également utiliser le panneau de configuration de Lync Server 2013 pour afficher votre topologie fusionnée.</span><span class="sxs-lookup"><span data-stu-id="b4e9f-115">You can also use Lync Server 2013 Control Panel to view your merged topology.</span></span> <span data-ttu-id="b4e9f-116">Dans Lync Server 2013 panneau de configuration, vous pouvez voir chaque nom de domaine complet (FQDN) de serveur, nom de domaine complet (FQDN) du pool et nom de site pour votre topologie fusionnée.</span><span class="sxs-lookup"><span data-stu-id="b4e9f-116">In Lync Server 2013 Control Panel, you can see each server FQDN, pool FQDN, and site name for your merged topology.</span></span> <span data-ttu-id="b4e9f-117">Les serveurs fusionnés portent le nom de **site** **BackCompatSite**.</span><span class="sxs-lookup"><span data-stu-id="b4e9f-117">Merged servers have a **Site** name of **BackCompatSite**.</span></span>

</div>

<div>

## <a name="to-view-the-merged-topology-in-lync-server-2013-control-panel"></a><span data-ttu-id="b4e9f-118">Pour afficher la topologie fusionnée dans Lync Server 2013 panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="b4e9f-118">To view the merged topology in Lync Server 2013 Control Panel</span></span>

1.  <span data-ttu-id="b4e9f-119">Ouvrez le panneau de configuration de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b4e9f-119">Open Lync Server 2013 Control Panel.</span></span>

2.  <span data-ttu-id="b4e9f-120">Cliquez sur **Topology**.</span><span class="sxs-lookup"><span data-stu-id="b4e9f-120">Click **Topology**.</span></span>

3.  <span data-ttu-id="b4e9f-121">Dans l’onglet **statut** , assurez-vous que les serveurs et les pools fusionnés apparaissent en recherchant **BackCompatSite** dans la colonne **site** .</span><span class="sxs-lookup"><span data-stu-id="b4e9f-121">On the **Status** tab, verify that servers and pools you merged appear by looking for **BackCompatSite** in the **Site** column.</span></span>

<span data-ttu-id="b4e9f-122">![Panneau de configuration de Lync Server avec topologie fusionnée](images/JJ205151.f986ddd4-2040-454d-9389-7f6154b59cc9(OCS.15).jpg "Panneau de configuration de Lync Server avec topologie fusionnée")</span><span class="sxs-lookup"><span data-stu-id="b4e9f-122">![Lync Server Control Panel showing merged topology](images/JJ205151.f986ddd4-2040-454d-9389-7f6154b59cc9(OCS.15).jpg "Lync Server Control Panel showing merged topology")</span></span>

<span data-ttu-id="b4e9f-123">Pour afficher des détails supplémentaires sur un pool fusionné, utilisez l’applet de passe **Get-CsPool** .</span><span class="sxs-lookup"><span data-stu-id="b4e9f-123">To see more detail about a merged pool, use the **Get-CsPool** cmdlet.</span></span> <span data-ttu-id="b4e9f-124">Outre les informations disponibles dans le générateur de topologie et le panneau de configuration de Lync Server 2013, cette applet de commande affiche les services qui s’exécutent sur le pool Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b4e9f-124">In addition to the information that is available in Topology Builder and Lync Server 2013 Control Panel, this cmdlet displays the services that run on the Lync Server 2013 pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b4e9f-125">Lorsque vous publiez la topologie après avoir exécuté l’Assistant fusion dans le générateur de topologie, les annuaires de conférences sont fusionnés avec Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b4e9f-125">When you publish the topology after running the Merge wizard in Topology Builder, conference directories are merged to Lync Server 2013.</span></span> <span data-ttu-id="b4e9f-126">Les annuaires de conférences peuvent être vérifiés en exécutant l’applet de passe <STRONG>Get-CsConferenceDirectory</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="b4e9f-126">Conference directories can be verified by running the <STRONG>Get-CsConferenceDirectory</STRONG> cmdlet.</span></span>



</div>

</div>

<div>

## <a name="to-view-services-on-a-merged-pool"></a><span data-ttu-id="b4e9f-127">Pour afficher les services d’un pool fusionné</span><span class="sxs-lookup"><span data-stu-id="b4e9f-127">To view services on a merged pool</span></span>

1.  <span data-ttu-id="b4e9f-128">Ouvrez Lync Server 2013 Management Shell.</span><span class="sxs-lookup"><span data-stu-id="b4e9f-128">Open the Lync Server 2013 Management Shell.</span></span>

2.  <span data-ttu-id="b4e9f-129">Dans la ligne de commande, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b4e9f-129">At the command line, type the following:</span></span>
    
        Get-CsPool [-Identity <FQDN of the pool>]
    
    <span data-ttu-id="b4e9f-130">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b4e9f-130">For example:</span></span>
    
        Get-CsPool -Identity pool02.contoso.net

</div>

<div>

## <a name="to-verify-conference-directories-merged"></a><span data-ttu-id="b4e9f-131">Pour vérifier la fusion des répertoires de conférences</span><span class="sxs-lookup"><span data-stu-id="b4e9f-131">To verify conference directories merged</span></span>

1.  <span data-ttu-id="b4e9f-132">Ouvrez Lync Server 2013 Management Shell.</span><span class="sxs-lookup"><span data-stu-id="b4e9f-132">Open the Lync Server 2013 Management Shell.</span></span>

2.  <span data-ttu-id="b4e9f-133">Dans la ligne de commande, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b4e9f-133">At the command line, type the following:</span></span>
    
        Get-CsConferenceDirectory

3.  <span data-ttu-id="b4e9f-134">Vérifiez que tous les répertoires de conférences du pool ou du serveur que vous fusionnez se trouvent désormais dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b4e9f-134">Verify that all the conference directories for the pool or server you are merging are now in Lync Server 2013.</span></span>

<span data-ttu-id="b4e9f-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b4e9f-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

