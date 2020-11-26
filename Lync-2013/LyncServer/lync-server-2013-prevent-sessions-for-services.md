---
title: 'Lync Server 2013 : empêcher les sessions pour les services'
description: 'Lync Server 2013 : bloquer les sessions pour les services.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prevent sessions for services
ms:assetid: 977dcc5c-2aac-48ef-86a1-a8d47b4d9e74
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182553(v=OCS.15)
ms:contentKeyID: 48184866
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 846a9da5330c3e64f61c27dfadd883f0c43a0ffa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436901"
---
# <a name="prevent-sessions-for-services-in-lync-server-2013"></a><span data-ttu-id="8a229-103">Empêcher les sessions pour les services dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8a229-103">Prevent sessions for services in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8a229-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8a229-104">

<span> </span></span></span>

<span data-ttu-id="8a229-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="8a229-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="8a229-106">Le panneau de configuration de Lync Server vous permet d’empêcher les nouvelles sessions de tous les services Lync Server 2013 en cours d’exécution sur un ordinateur spécifique ou d’empêcher de nouvelles sessions pour un service 2013 serveur Lync spécifique.</span><span class="sxs-lookup"><span data-stu-id="8a229-106">You can use Lync Server Control Panel to prevent new sessions for all the Lync Server 2013 services running on a specific computer or to prevent new sessions for a specific Lync Server 2013 service.</span></span>

<div>

## <a name="to-prevent-new-sessions-for-all-lync-server-services-on-a-computer"></a><span data-ttu-id="8a229-107">Pour empêcher de nouvelles sessions pour tous les services Lync Server sur un ordinateur</span><span class="sxs-lookup"><span data-stu-id="8a229-107">To prevent new sessions for all Lync Server services on a computer</span></span>

1.  <span data-ttu-id="8a229-108">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsServerAdministrator ou CsAdministrator, connectez-vous à n’importe quel ordinateur se trouve sur le réseau sur lequel vous avez déployé Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8a229-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="8a229-109">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8a229-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="8a229-110">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8a229-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="8a229-111">Dans la barre de navigation de gauche, cliquez sur **Topology** , puis sur **Status (statut**).</span><span class="sxs-lookup"><span data-stu-id="8a229-111">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="8a229-112">Dans la page **État** , triez ou effectuez une recherche dans la liste selon vos besoins pour trouver l’ordinateur exécutant les services pour lesquels vous voulez éviter de nouvelles sessions, puis cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="8a229-112">On the **Status** page, sort or search through the list as needed to find the computer that is running the services for which you want to prevent new sessions, and then click it.</span></span>

5.  <span data-ttu-id="8a229-113">Cliquez sur **action**.</span><span class="sxs-lookup"><span data-stu-id="8a229-113">Click **Action**.</span></span>

6.  <span data-ttu-id="8a229-114">Cliquez sur **empêcher de nouvelles sessions pour tous les services**.</span><span class="sxs-lookup"><span data-stu-id="8a229-114">Click **Prevent new sessions for all services**.</span></span>

</div>

<div>

## <a name="to-prevent-new-sessions-for-a-specific-service"></a><span data-ttu-id="8a229-115">Pour empêcher de nouvelles sessions pour un service spécifique</span><span class="sxs-lookup"><span data-stu-id="8a229-115">To prevent new sessions for a specific service</span></span>

1.  <span data-ttu-id="8a229-116">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsServerAdministrator ou CsAdministrator, connectez-vous à n’importe quel ordinateur se trouve sur le réseau sur lequel vous avez déployé Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8a229-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="8a229-117">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8a229-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="8a229-118">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8a229-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="8a229-119">Dans la barre de navigation de gauche, cliquez sur **Topology** , puis sur **Status (statut**).</span><span class="sxs-lookup"><span data-stu-id="8a229-119">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="8a229-120">Dans la page **État** , triez ou effectuez une recherche dans la liste selon vos besoins pour trouver l’ordinateur exécutant le service que vous voulez démarrer ou arrêter, puis cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="8a229-120">On the **Status** page, sort or search through the list as needed to find the computer that is running the service you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="8a229-121">Cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="8a229-121">Click **Properties**.</span></span>

6.  <span data-ttu-id="8a229-122">Triez la liste des services, si nécessaire, puis cliquez sur le service pour lequel vous souhaitez éviter de nouvelles sessions.</span><span class="sxs-lookup"><span data-stu-id="8a229-122">Sort the list of services, if necessary, and click the service for which you want to prevent new sessions.</span></span>

7.  <span data-ttu-id="8a229-123">Cliquez sur **action**.</span><span class="sxs-lookup"><span data-stu-id="8a229-123">Click **Action**.</span></span>

8.  <span data-ttu-id="8a229-124">Cliquez sur **empêcher de nouvelles sessions pour le service**.</span><span class="sxs-lookup"><span data-stu-id="8a229-124">Click **Prevent new sessions for service**.</span></span>

9.  <span data-ttu-id="8a229-125">Cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="8a229-125">Click **Close**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8a229-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a229-126">See Also</span></span>


[<span data-ttu-id="8a229-127">Gestion de la topologie Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8a229-127">Managing the Lync Server 2013 topology</span></span>](lync-server-2013-managing-the-lync-server-topology.md)  
  

<span data-ttu-id="8a229-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8a229-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

