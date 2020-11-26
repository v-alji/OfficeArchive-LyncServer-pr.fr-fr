---
title: 'Lync Server 2013 : Démarrez ou arrêtez Lync Server services'
description: 'Lync Server 2013 : Démarrez ou arrêtez les services serveur Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Start or stop Lync Server 2013 services
ms:assetid: 1c70b4ec-9de5-4f7a-a3c9-c0eb76710505
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520958(v=OCS.15)
ms:contentKeyID: 48183554
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d6e6520cbf6fda38676beab984c2d006061b019
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423679"
---
# <a name="start-or-stop-lync-server-2013-services"></a><span data-ttu-id="9c715-103">Démarrer ou arrêter les services Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c715-103">Start or stop Lync Server 2013 services</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9c715-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9c715-104">

<span> </span></span></span>

<span data-ttu-id="9c715-105">_**Dernière modification de la rubrique :** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="9c715-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="9c715-106">Vous pouvez utiliser le panneau de configuration de Lync Server pour démarrer ou arrêter l’exécution de tous les services Lync Server 2013 sur un ordinateur spécifique ou pour démarrer ou arrêter un service spécifique.</span><span class="sxs-lookup"><span data-stu-id="9c715-106">You can use Lync Server Control Panel to start or stop all the Lync Server 2013 services running on a specific computer or to start or stop a specific service.</span></span>

<div>

## <a name="to-start-or-stop-all-lync-server-services-on-a-computer"></a><span data-ttu-id="9c715-107">Pour démarrer ou arrêter tous les services Lync Server sur un ordinateur</span><span class="sxs-lookup"><span data-stu-id="9c715-107">To start or stop all Lync Server services on a computer</span></span>

1.  <span data-ttu-id="9c715-108">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsServerAdministrator ou CsAdministrator, connectez-vous à n’importe quel ordinateur se trouve sur le réseau sur lequel vous avez déployé Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9c715-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span> <span data-ttu-id="9c715-109">Vous pouvez déterminer si vous avez reçu le rôle CsServerAdministrator ou CsAdministrator RBAC en exécutant une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="9c715-109">You can determine whether you have been assigned the CsServerAdministrator or the CsAdministrator RBAC role by running a command similar to the following:</span></span>
    
        Get-CsAdminRoleAssignment -Identity "kenmyer"

2.  <span data-ttu-id="9c715-110">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9c715-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="9c715-111">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="9c715-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="9c715-112">Dans la barre de navigation de gauche, cliquez sur **Topology** , puis sur **Status (statut**).</span><span class="sxs-lookup"><span data-stu-id="9c715-112">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="9c715-113">Dans la page **État** , triez ou effectuez une recherche dans la liste selon vos besoins pour trouver l’ordinateur exécutant les services que vous voulez démarrer ou arrêter, puis cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="9c715-113">On the **Status** page, sort or search through the list as needed to find the computer that is running the services you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="9c715-114">Cliquez sur **action**.</span><span class="sxs-lookup"><span data-stu-id="9c715-114">Click **Action**.</span></span>

6.  <span data-ttu-id="9c715-115">Cliquez sur **Démarrer tout le service** ou **arrêter tous les services**.</span><span class="sxs-lookup"><span data-stu-id="9c715-115">Click **Start All services** or **Stop All services**.</span></span>

</div>

<div>

## <a name="to-start-or-stop-a-specific-service"></a><span data-ttu-id="9c715-116">Pour démarrer ou arrêter un service spécifique</span><span class="sxs-lookup"><span data-stu-id="9c715-116">To start or stop a specific service</span></span>

1.  <span data-ttu-id="9c715-117">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="9c715-117">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="9c715-118">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9c715-118">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="9c715-119">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="9c715-119">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="9c715-120">Dans la barre de navigation de gauche, cliquez sur **Topology** , puis sur **Status (statut**).</span><span class="sxs-lookup"><span data-stu-id="9c715-120">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="9c715-121">Dans la page **État** , triez ou effectuez une recherche dans la liste selon vos besoins pour trouver l’ordinateur exécutant le service que vous voulez démarrer ou arrêter, puis cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="9c715-121">On the **Status** page, sort or search through the list as needed to find the computer that is running the service you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="9c715-122">Cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="9c715-122">Click **Properties**.</span></span>

6.  <span data-ttu-id="9c715-123">Triez la liste des services, si nécessaire, puis cliquez sur le service que vous voulez démarrer ou arrêter.</span><span class="sxs-lookup"><span data-stu-id="9c715-123">Sort the list of services, if necessary, and click the service you want to start or stop.</span></span>

7.  <span data-ttu-id="9c715-124">Cliquez sur **action**.</span><span class="sxs-lookup"><span data-stu-id="9c715-124">Click **Action**.</span></span>

8.  <span data-ttu-id="9c715-125">Cliquez sur **Démarrer le service** ou arrêter le **service**.</span><span class="sxs-lookup"><span data-stu-id="9c715-125">Click **Start service** or **Stop service**.</span></span>

9.  <span data-ttu-id="9c715-126">Cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="9c715-126">Click **Close**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9c715-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c715-127">See Also</span></span>


[<span data-ttu-id="9c715-128">Empêcher les sessions pour les services dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c715-128">Prevent sessions for services in Lync Server 2013</span></span>](lync-server-2013-prevent-sessions-for-services.md)  


[<span data-ttu-id="9c715-129">Gestion de la topologie Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c715-129">Managing the Lync Server 2013 topology</span></span>](lync-server-2013-managing-the-lync-server-topology.md)  
  

<span data-ttu-id="9c715-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9c715-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

