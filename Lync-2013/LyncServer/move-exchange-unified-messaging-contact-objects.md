---
title: Déplacer les objets de contact de la messagerie unifiée Exchange
description: Déplacer les objets de contact de la messagerie unifiée Exchange.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Move Exchange Unified Messaging Contact objects
ms:assetid: 35c7e987-41b5-4798-b617-3303f20e52e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688022(v=OCS.15)
ms:contentKeyID: 49733612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e3353427f407523a8778585d27201355714a3085
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438443"
---
# <a name="move-exchange-unified-messaging-contact-objects"></a><span data-ttu-id="80299-103">Déplacer les objets de contact de la messagerie unifiée Exchange</span><span class="sxs-lookup"><span data-stu-id="80299-103">Move Exchange Unified Messaging Contact objects</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="80299-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="80299-104">

<span> </span></span></span>

<span data-ttu-id="80299-105">_**Dernière modification de la rubrique :** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="80299-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="80299-106">Pour migrer des objets de contact de standard automatique (AA) et d’accès d’abonné (SA) vers le nouveau déploiement Lync Server 2013, vous devez d’abord déplacer les objets du déploiement d’Office Communications Server 2007 R2 hérités vers le nouveau déploiement Lync Server 2013 à l’aide des applets de technologie **Get-CsExUmContact** et **Move-CsExUmContact** .</span><span class="sxs-lookup"><span data-stu-id="80299-106">To migrate Auto Attendant (AA) and Subscriber Access (SA) contact objects to the new Lync Server 2013 deployment, you first move the objects from the legacy Office Communications Server 2007 R2 deployment to the new the Lync Server 2013 deployment using the **Get-CsExUmContact** and **Move-CsExUmContact** cmdlets.</span></span> <span data-ttu-id="80299-107">Sur le serveur Exchange, vous devez exécuter le script Windows PowerShell **exchucutil** pour effectuer les actions suivantes pour le pool Lync qui vient d’être déployé :</span><span class="sxs-lookup"><span data-stu-id="80299-107">On the Exchange Server, you then run the **ExchUCUtil** Windows PowerShell script to do the following for the newly deployed Lync pool:</span></span>

  - <span data-ttu-id="80299-108">Ajoutez-le aux passerelles IP de messagerie unifiée.</span><span class="sxs-lookup"><span data-stu-id="80299-108">Add it to the Unified Messaging IP gateways.</span></span>

  - <span data-ttu-id="80299-109">Ajoutez-le au groupe de recherche de messagerie unifiée.</span><span class="sxs-lookup"><span data-stu-id="80299-109">Add it to the Unified Messaging hunt groups.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="80299-110">Pour pouvoir utiliser les applets de commande <STRONG>Get-CsExUmContact</STRONG> et <STRONG>Move-CsExUmContact</STRONG> , vous devez être membre du groupe RTCUniversalUserAdmins et disposer de l’autorisation d’unité d’organisation (UO) pour l’unité d’organisation où les objets de contacts sont stockés.</span><span class="sxs-lookup"><span data-stu-id="80299-110">In order to use the <STRONG>Get-CsExUmContact</STRONG> and <STRONG>Move-CsExUmContact</STRONG> cmdlets, you must be a member of the RTCUniversalUserAdmins group and have organizational unit (OU) permission to the OU where the contacts objects are stored.</span></span> <span data-ttu-id="80299-111">L’autorisation d’UO peut être accordée à l’aide de l’applet de commande <STRONG>Grant-OUPermission</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="80299-111">OU permission can be granted using the <STRONG>Grant-OUPermission</STRONG> cmdlet.</span></span>



</div>

<div>

## <a name="to-move-contact-objects-by-using-the-lync-server-management-shell"></a><span data-ttu-id="80299-112">Pour déplacer des objets de contact à l’aide de Lync Server Management Shell</span><span class="sxs-lookup"><span data-stu-id="80299-112">To move contact objects by using the Lync Server Management Shell</span></span>

1.  <span data-ttu-id="80299-113">Ouvrez Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="80299-113">Open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="80299-114">Pour chaque liste inscrite avec la messagerie unifiée Exchange (où pool1.contoso.net est un pool à partir du déploiement d’Office Communications Server 2007 R2 et pool2.contoso.net est le pool du déploiement de Lync Server 2013) sur la ligne de commande, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="80299-114">For each pool registered with Exchange UM (where pool1.contoso.net is a pool from the Office Communications Server 2007 R2 deployment and pool2.contoso.net is the pool from the Lync Server 2013 deployment) at the command line, type the following:</span></span>
    
        Get-CsExUmContact -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsExUmContact -Target pool02.contoso.net
    
    <span data-ttu-id="80299-115">Pour vérifier que les objets de contact sont déplacés, exécutez l’applet de contrôle **Get-CsExumContact** et vérifiez que **RegistrarPool** est désormais dirigé vers le nouveau pool.</span><span class="sxs-lookup"><span data-stu-id="80299-115">To verify that the contact objects are moved, run the **Get-CsExumContact** cmdlet and confirm that **RegistrarPool** is now pointing to the new pool.</span></span>

</div>

<div>

## <a name="to-run-the-exchucutil-windows-powershell-script"></a><span data-ttu-id="80299-116">Pour exécuter le script Windows PowerShell ExchUCUtil</span><span class="sxs-lookup"><span data-stu-id="80299-116">To run the ExchUCUtil Windows PowerShell script</span></span>

1.  <span data-ttu-id="80299-117">Ouvrez une session sur le serveur de messagerie unifiée Exchange en tant qu’utilisateur disposant des privilèges d’administrateur de l’organisation Exchange.</span><span class="sxs-lookup"><span data-stu-id="80299-117">Log on to the Exchange UM Server as a user with Exchange Organization Administrator privileges.</span></span>

2.  <span data-ttu-id="80299-118">Accédez au script Windows PowerShell ExchUCUtil.</span><span class="sxs-lookup"><span data-stu-id="80299-118">Navigate to the ExchUCUtil Windows PowerShell script.</span></span>
    
    <span data-ttu-id="80299-119">Dans Exchange 2007, ExchUCUtil.ps1 se trouve à : **% Program Files% \\ Microsoft \\ Exchange Server \\ scripts \\ExchUCUtil.ps1**</span><span class="sxs-lookup"><span data-stu-id="80299-119">In Exchange 2007, ExchUCUtil.ps1 is located at: **%Program Files%\\Microsoft\\Exchange Server\\Scripts\\ExchUCUtil.ps1**</span></span>
    
    <span data-ttu-id="80299-120">Dans Exchange 2010, ExchUCUtil.ps1 se trouve à : **% Program Files% \\ Microsoft \\ Exchange Server \\ v14 \\ scripts \\ExchUCUtil.ps1**</span><span class="sxs-lookup"><span data-stu-id="80299-120">In Exchange 2010, ExchUCUtil.ps1 is located at: **%Program Files%\\Microsoft\\Exchange Server\\V14\\Scripts\\ExchUCUtil.ps1**</span></span>

3.  <span data-ttu-id="80299-121">Si Exchange est déployé dans une seule forêt, tapez :</span><span class="sxs-lookup"><span data-stu-id="80299-121">If Exchange is deployed in a single forest, type:</span></span>
    
        exchucutil.ps1
    
    <span data-ttu-id="80299-122">Ou, si Exchange est déployé dans plusieurs forêts, tapez :</span><span class="sxs-lookup"><span data-stu-id="80299-122">Or, if Exchange is deployed in multiple forests, type:</span></span>
    
        exchucutil.ps1 -Forest:" <forest FQDN>"
    
    <span data-ttu-id="80299-123">où FQDN de forêt spécifie la forêt dans laquelle Lync Server 2013 est déployé.</span><span class="sxs-lookup"><span data-stu-id="80299-123">where forest FQDN specifies the forest in which Lync Server 2013 is deployed.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="80299-124">Assurez-vous de redémarrer le service <STRONG>frontal de Lync Server</STRONG> (rtcsrv.exe) <EM>après avoir</EM> exécuté exchucutil.ps1.</span><span class="sxs-lookup"><span data-stu-id="80299-124">Be sure to restart the <STRONG>Lync Server Front-End</STRONG> service (rtcsrv.exe) <EM>after</EM> you run exchucutil.ps1.</span></span> <span data-ttu-id="80299-125">Dans le cas contraire, Lync Server 2013 ne détectera pas la messagerie unifiée dans la topologie.</span><span class="sxs-lookup"><span data-stu-id="80299-125">Otherwise, Lync Server 2013 will not detect Unified Messaging in the topology.</span></span>

    
    <span data-ttu-id="80299-126"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="80299-126"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

