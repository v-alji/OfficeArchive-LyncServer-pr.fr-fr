---
title: Empêcher les nouvelles connexions à Lync Server pour la maintenance du serveur
description: Evitez de nouvelles connexions à Lync Server pour la maintenance du serveur.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prevent new connections to Lync Server for server maintenance
ms:assetid: 22b27adf-a590-43bd-9306-a5789ae108d7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520964(v=OCS.15)
ms:contentKeyID: 48183625
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd676467cdd6b5bb430f972e48c2f3a53f3f6f14
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436896"
---
# <a name="prevent-new-connections-to-lync-server-2013-for-server-maintenance"></a><span data-ttu-id="85d5f-103">Empêcher les nouvelles connexions à Lync Server 2013 pour la maintenance du serveur</span><span class="sxs-lookup"><span data-stu-id="85d5f-103">Prevent new connections to Lync Server 2013 for server maintenance</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85d5f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85d5f-104">

<span> </span></span></span>

<span data-ttu-id="85d5f-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="85d5f-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="85d5f-106">Lync Server vous permet de mettre un serveur hors connexion (par exemple, pour appliquer des mises à jour logicielles ou matérielles) sans perte de service aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="85d5f-106">Lync Server enables you to take a server offline (for example, to apply software or hardware upgrades) without any loss of service to users.</span></span>

<span data-ttu-id="85d5f-107">Lorsque vous spécifiez l’option permettant d’éviter de nouvelles connexions ou appels vers un serveur d’un pool, il cesse de prendre de nouvelles connexions et appels dès que vous implémentez cette option.</span><span class="sxs-lookup"><span data-stu-id="85d5f-107">When you specify the option to prevent new connections or calls to a server in a pool, it stops taking any new connections and calls as soon as you implement this option.</span></span> <span data-ttu-id="85d5f-108">Ces nouvelles connexions et appels sont routés par le biais d’autres serveurs du pool.</span><span class="sxs-lookup"><span data-stu-id="85d5f-108">These new connections and calls are routed through other servers in the pool.</span></span> <span data-ttu-id="85d5f-109">Un serveur qui empêche de nouvelles connexions autorise la poursuite de ses sessions sur les connexions existantes jusqu’à ce qu’il se termine de façon naturelle.</span><span class="sxs-lookup"><span data-stu-id="85d5f-109">A server that is preventing new connections allows its sessions on existing connections to continue until they naturally end.</span></span> <span data-ttu-id="85d5f-110">Lorsque toutes les sessions existantes sont terminées, le serveur est prêt à être déconnecté.</span><span class="sxs-lookup"><span data-stu-id="85d5f-110">When all existing sessions have ended, the server is ready to be taken offline.</span></span>

<span data-ttu-id="85d5f-111">Lorsque vous interdisez de nouvelles connexions à un serveur frontal, certains services et fonctionnalités Lync Server dépendent de l’équilibrage de charge DNS pour s’assurer qu’elle fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="85d5f-111">When you prevent new connections to a Front End Server, some Lync Server features and services rely on DNS load balancing to ensure that it functions properly.</span></span> <span data-ttu-id="85d5f-112">Si vous n’utilisez pas l’équilibrage de charge DNS sur le pool, les connexions par le biais de ces services ne peuvent pas être redirigées vers d’autres serveurs au cours de la période pendant laquelle le serveur empêche les nouvelles connexions et, par conséquent, lorsque le serveur est hors connexion, des sessions et des appels peuvent être interrompus.</span><span class="sxs-lookup"><span data-stu-id="85d5f-112">If you are not using DNS load balancing on the pool, connections through these services may not be re-routed to other servers during the period that the server is preventing new connections, and thus when the server is taken offline some sessions and calls may be interrupted.</span></span> <span data-ttu-id="85d5f-113">Les fonctionnalités qui dépendent de l’équilibrage de charge DNS pour s’assurer que cette option fonctionne correctement sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="85d5f-113">The features that rely on DNS load balancing to ensure that this option operates properly are as follows:</span></span>

  - <span data-ttu-id="85d5f-114">Intendant</span><span class="sxs-lookup"><span data-stu-id="85d5f-114">Attendant</span></span>

  - <span data-ttu-id="85d5f-115">application d’annonce de conférence</span><span class="sxs-lookup"><span data-stu-id="85d5f-115">Conferencing Announcement application</span></span>

  - <span data-ttu-id="85d5f-116">application Response Group</span><span class="sxs-lookup"><span data-stu-id="85d5f-116">Response Group application</span></span>

  - <span data-ttu-id="85d5f-117">application d’annonce</span><span class="sxs-lookup"><span data-stu-id="85d5f-117">Announcement application</span></span>

  - <span data-ttu-id="85d5f-118">application de parcage d’appel</span><span class="sxs-lookup"><span data-stu-id="85d5f-118">Call Park application</span></span>

<span data-ttu-id="85d5f-119">Pour plus d’informations sur l’équilibrage de charge DNS, voir [équilibrage de charge DNS dans Lync Server 2013](lync-server-2013-dns-load-balancing.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="85d5f-119">For details about DNS load balancing, see [DNS load balancing in Lync Server 2013](lync-server-2013-dns-load-balancing.md) in the Planning documentation.</span></span>

<span data-ttu-id="85d5f-120">Outre qu’il n’est pas possible d’empêcher les nouvelles connexions de tous les services sur un serveur exécutant Lync Server, vous pouvez également éviter de nouvelles connexions pour les services Lync Server individuels.</span><span class="sxs-lookup"><span data-stu-id="85d5f-120">In addition to preventing new connections for all services on a server running Lync Server, you can also prevent new connections for individual Lync Server services.</span></span> <span data-ttu-id="85d5f-121">Par exemple, cette méthode est utile dans le cas où vous devez appliquer une mise à jour du serveur Lync qui ne nécessite pas l’arrêt de l’intégralité du serveur.</span><span class="sxs-lookup"><span data-stu-id="85d5f-121">For example, this method is useful in a situation where you need to apply a Lync Server update that does not require the whole server to be shut down.</span></span> <span data-ttu-id="85d5f-122">Notez que lorsque vous interdisez les connexions d’un service, vous devez sélectionner un service tel qu’il est groupé et affiché dans la liste des services Windows.</span><span class="sxs-lookup"><span data-stu-id="85d5f-122">Note that when you prevent connections for one service, you must select a service as it is grouped and displayed in the Windows list of services.</span></span> <span data-ttu-id="85d5f-123">Par exemple, le service Lync Server Front-End et l’agent de collection de données pour la surveillance sont des services Lync Server distincts, mais dans la liste des services Windows, ils sont consolidés et affichés comme le service frontal de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="85d5f-123">For example, the Lync Server Front-End service and the data collection agent for Monitoring are separate Lync Server services, but in the Windows services list they are consolidated and shown as the Lync Server Front End service.</span></span> <span data-ttu-id="85d5f-124">Vous pouvez empêcher de nouvelles connexions pour le service frontal de Lync Server, mais vous ne pouvez pas empêcher les nouvelles connexions de ces deux services Lync Server sous-jacents séparément.</span><span class="sxs-lookup"><span data-stu-id="85d5f-124">You can prevent new connections for the Lync Server Front End service, but you cannot prevent new connections for these two individual underlying Lync Server services separately.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="85d5f-125">Lorsque vous définissez un serveur pour empêcher les nouvelles connexions, puis que vous redémarrez le serveur, par défaut, le serveur commence immédiatement à accepter de nouvelles connexions après son démarrage.</span><span class="sxs-lookup"><span data-stu-id="85d5f-125">When you set a server to prevent new connections, and then restart the server, by default the server will immediately begin accepting new connections after it starts.</span></span> <span data-ttu-id="85d5f-126">Pour éviter ce problème, configurez le serveur de façon à ce qu’il ne s’interrompe qu’après le redémarrage du serveur.</span><span class="sxs-lookup"><span data-stu-id="85d5f-126">To prevent this, set the server to only pause and resume manually, before you restart the server.</span></span>



</div>

<div>

## <a name="to-prevent-new-connections-to-lync-server"></a><span data-ttu-id="85d5f-127">Pour éviter de nouvelles connexions à Lync Server :</span><span class="sxs-lookup"><span data-stu-id="85d5f-127">To prevent new connections to Lync Server:</span></span>

1.  <span data-ttu-id="85d5f-128">Connectez-vous à l’ordinateur local en tant que membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="85d5f-128">Log on to the local computer as a member of the Administrators group.</span></span>

2.  <span data-ttu-id="85d5f-129">Ouvrez la console enfichable Services : cliquez sur **Démarrer**, pointez sur **tous les programmes**, sur **Outils d’administration**, puis cliquez sur **services**.</span><span class="sxs-lookup"><span data-stu-id="85d5f-129">Open the Services snap-in console: Click **Start**, point to **All Programs**, point to **Administrative Tools**, and then click **Services**.</span></span>

3.  <span data-ttu-id="85d5f-130">Dans la liste, double-cliquez sur le service Windows Server Lync pour lequel vous voulez empêcher les nouvelles connexions.</span><span class="sxs-lookup"><span data-stu-id="85d5f-130">In the list, double-click the Lync Server Windows service to which you want to prevent new connections.</span></span>

4.  <span data-ttu-id="85d5f-131">Dans la boîte de dialogue Propriétés, sous **État du service : démarré**, cliquez sur **suspendre**.</span><span class="sxs-lookup"><span data-stu-id="85d5f-131">In the Properties dialog box, under **Service status: Started**, click **Pause**.</span></span>

5.  <span data-ttu-id="85d5f-132">Si vous le souhaitez, mais que vous avez le choix, en regard de **type de démarrage**, cliquez sur **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="85d5f-132">Optionally, but recommended, next to **Startup type**, click **Manual**.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="85d5f-133">Lorsque vous définissez un serveur pour empêcher les nouvelles connexions, puis que vous redémarrez le serveur, par défaut, le serveur commence immédiatement à accepter de nouvelles connexions après son démarrage.</span><span class="sxs-lookup"><span data-stu-id="85d5f-133">When you set a server to prevent new connections, and then restart the server, by default the server will immediately begin accepting new connections after it starts.</span></span> <span data-ttu-id="85d5f-134">Pour éviter ce problème, configurez le serveur de façon à ce qu’il ne s’interrompe qu’après le redémarrage du serveur.</span><span class="sxs-lookup"><span data-stu-id="85d5f-134">To prevent this, set the server to only pause and resume manually, before you restart the server.</span></span>

    
    </div>

6.  <span data-ttu-id="85d5f-135">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="85d5f-135">When you are finished, click **OK**.</span></span>

<span data-ttu-id="85d5f-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85d5f-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

