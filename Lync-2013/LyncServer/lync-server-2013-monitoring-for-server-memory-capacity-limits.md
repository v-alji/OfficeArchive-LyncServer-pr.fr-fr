---
title: 'Lync Server 2013 : surveillance des limites de capacité de mémoire du serveur'
description: 'Lync Server 2013 : surveillance des limites de capacité de mémoire du serveur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring for server memory capacity limits
ms:assetid: 1697ea71-6fcf-480d-b4e9-cd79f94d247e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh689982(v=OCS.15)
ms:contentKeyID: 48183506
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6561908af2c8f2f7b5fb9e347cc6247f7ca6642e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425429"
---
# <a name="monitoring-for-server-memory-capacity-limits-in-lync-server-2013"></a><span data-ttu-id="369f8-103">Surveiller les limites de capacité de mémoire serveur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="369f8-103">Monitoring for server memory capacity limits in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="369f8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="369f8-104">

<span> </span></span></span>

<span data-ttu-id="369f8-105">_**Dernière modification de la rubrique :** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="369f8-105">_**Topic Last Modified:** 2016-12-08_</span></span>

    Some information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<div>


> [!WARNING]  
> <span data-ttu-id="369f8-106">Les informations dans cette rubrique faisant référence à la planification de la capacité uniquement aux clients mobiles Lync 2010 et au service de mobilité (MCX).</span><span class="sxs-lookup"><span data-stu-id="369f8-106">The information in this topic that refers to Capacity Planning pertains only to Lync 2010 Mobile clients and the Mobility Service (Mcx).</span></span> <span data-ttu-id="369f8-107">La planification de la capacité de l’API Web de communications unifiées (UCWA), qui est utilisée par les clients mobiles Lync 2013, est fournie par l’outil de planification de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="369f8-107">Capacity Planning for the Unified Communications Web API (UCWA), used by the Lync 2013 Mobile clients, is provided by the Lync Server 2013, Planning Tool.</span></span>



</div>

<span data-ttu-id="369f8-108">Deux compteurs de performance de mobilité peuvent vous aider à déterminer votre utilisation actuelle et vous aider à planifier la capacité du service de mobilité Lync Server 2013 (MCX), ainsi que l’utilisation de la mémoire pour UCWA.</span><span class="sxs-lookup"><span data-stu-id="369f8-108">Two mobility performance counters can help you to determine your current usage and help you plan capacity for the Lync Server 2013 Mobility Service (Mcx), as well as to monitor memory usage for UCWA.</span></span> <span data-ttu-id="369f8-109">Pour celle-ci, la catégorie de compteurs est **LS:WEB – UCWA**.</span><span class="sxs-lookup"><span data-stu-id="369f8-109">For UCWA, the counter category is **LS:WEB – UCWA**.</span></span> <span data-ttu-id="369f8-110">Pour le service de mobilité (Mcx), les compteurs se trouvent dans la catégorie **LS:WEB - Service de communication mobile**.</span><span class="sxs-lookup"><span data-stu-id="369f8-110">For the Mobility Service (Mcx), the counters are under the category **LS:WEB - Mobile Communication Service**.</span></span> <span data-ttu-id="369f8-111">Les compteurs à surveiller sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="369f8-111">The counters to monitor are:</span></span>

  - <span data-ttu-id="369f8-112">**Nombre de sessions actives avec abonnements actifs aux informations de présence**, qui correspond au nombre actuel de points de terminaison enregistrés par l’intermédiaire de l’API UCWA ou du service de mobilité (Mcx) dont les abonnements aux informations de présence sont actifs (nombre d’utilisateurs mobiles toujours connectés) ;</span><span class="sxs-lookup"><span data-stu-id="369f8-112">**Currently Active Session Count with Active Presence Subscriptions**, which is the current number of endpoints registered through UCWA or the Mobility Service (Mcx) that have active presence subscriptions (number of always-connected mobile users)</span></span>

  - <span data-ttu-id="369f8-113">**Nombre de sessions actives**, qui correspond au nombre actuel de points de terminaison enregistrés par l’intermédiaire de l’API UCWA ou du service de mobilité.</span><span class="sxs-lookup"><span data-stu-id="369f8-113">**Currently Active Session Count**, which is the current number of endpoints registered through UCWA or the Mobility Service</span></span>

<span data-ttu-id="369f8-114">Si la différence entre les compteurs **Nombre de sessions actives avec abonnements actifs aux informations de présence** et **Nombre de sessions actives** reste minime au fil du temps, cela signifie que la plupart des utilisateurs d’appareils mobiles disposent d’un appareil toujours connecté, tel qu’un appareil mobile Android ou Nokia (pour Mcx uniquement).</span><span class="sxs-lookup"><span data-stu-id="369f8-114">If the difference between **Currently Active Session Count with Active Presence Subscriptions** and **Currently Active Session Count** is small over time, this means that most mobile device users have an always-connected device, such as an Android or Nokia mobile device (for Mcx only).</span></span> <span data-ttu-id="369f8-115">Les appareils UCWA toujours connectés incluent des appareils Apple et Android exécutant des clients mobiles Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="369f8-115">UCWA always-connected devices include Apple and Android devices running Lync 2013 Mobile clients).</span></span> <span data-ttu-id="369f8-116">Si le compteur **Nombre de sessions actives** est beaucoup plus élevé que le compteur **Nombre de sessions actives avec abonnements actifs aux informations de présence**, cela indique qu’un nombre plus élevé d’utilisateurs emploient un appareil à points de terminaison en arrière-plan, tel qu’un appareil Apple iOS ou Windows Phone sous Mcx.</span><span class="sxs-lookup"><span data-stu-id="369f8-116">If **Currently Active Session Count** is much higher than **Currently Active Session Count with Active Presence Subscriptions**, this indicates that more users are using a background endpoint device, such as an Apple iOS device or Windows Phone under Mcx.</span></span> <span data-ttu-id="369f8-117">(Windows Phone est le seul client mobile Lync 2013 qui s’inscrira comme suit).</span><span class="sxs-lookup"><span data-stu-id="369f8-117">(Windows Phone is the only Lync 2013 Mobile client that will register as this).</span></span>

<span data-ttu-id="369f8-118">Vous devez définir une limite sur le **nombre de sessions actives avec abonnements de présence actives** et compteurs de performance **actuellement nombre de sessions actives** en fonction de votre utilisation prévue, des résultats de la planification de la capacité et d’une analyse continue du service de mobilité et des autres compteurs de serveur front-end.</span><span class="sxs-lookup"><span data-stu-id="369f8-118">You should set a limit on the **Currently Active Session Count with Active Presence Subscriptions** and **Currently Active Session Count** performance counters based on your expected usage, capacity planning results, and ongoing monitoring of Mobility Service and other Front End Server counters.</span></span> <span data-ttu-id="369f8-119">Les limites que vous définissez doivent vous permettre d’évaluer la capacité des serveurs et de déclencher des alertes quand celle-ci est dépassée.</span><span class="sxs-lookup"><span data-stu-id="369f8-119">The limits you set should enable you to evaluate server capacity and raise alerts when capacity is exceeded.</span></span>

<span data-ttu-id="369f8-120">Pour déterminer les limites appropriées, vous devez d’abord déterminer la quantité de mémoire disponible sur le serveur frontal pour le service de mobilité.</span><span class="sxs-lookup"><span data-stu-id="369f8-120">To determine the appropriate limits, you need to first determine how much memory is available on the Front End Server for the Mobility Service.</span></span> <span data-ttu-id="369f8-121">Surveillez les compteurs afin de déterminer le besoin de prévoir une capacité supplémentaire à l’aide de la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="369f8-121">Monitor the counters to determine when you need to plan for extra capacity, according to the following formula:</span></span>

<span data-ttu-id="369f8-122">Mémoire totale utilisée par le service de mobilité MCX (Mo) = 164 + (400 + 134)/1024 le \* **nombre de sessions actives avec les abonnements de présence actives** + 400/1024 \* ( **Currently Active Session Count with Active Presence Subscriptions\*\*\*\*nombre de sessions actives** )</span><span class="sxs-lookup"><span data-stu-id="369f8-122">Total memory used by the Mcx Mobility Service (MB) = 164 + (400 + 134) / 1024 \* **Currently Active Session Count with Active Presence Subscriptions** + 400 / 1024 \* (**Currently Active Session Count** – **Currently Active Session Count with Active Presence Subscriptions**)</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="369f8-123">Le calculateur de capacités de Microsoft Lync Server 2010 est une feuille de calcul préremplie avec toutes les formules permettant à un planificateur de déterminer quelles sont les conditions requises pour les serveurs, y compris le processeur, la mémoire et le disque dur.</span><span class="sxs-lookup"><span data-stu-id="369f8-123">The Microsoft Lync Server 2010 Capacity Calculator is a spreadsheet that is prepopulated with all of the formulas that enable a planner to determine what the requirements will be for the servers, including CPU, memory, and hard drive.</span></span> <span data-ttu-id="369f8-124">Vous pouvez télécharger la feuille de calcul et un document associé à l’adresse suivante : <A href="https://go.microsoft.com/fwlink/p/?linkid=212657">https://go.microsoft.com/fwlink/p/?LinkID=212657</A></span><span class="sxs-lookup"><span data-stu-id="369f8-124">You can download the spreadsheet and an associated document at: <A href="https://go.microsoft.com/fwlink/p/?linkid=212657">https://go.microsoft.com/fwlink/p/?LinkID=212657</A></span></span>



</div>

<span data-ttu-id="369f8-125">Le serveur frontal doit disposer de suffisamment de mémoire pour prendre en charge le service de mobilité dans les situations de basculement.</span><span class="sxs-lookup"><span data-stu-id="369f8-125">The Front End Server needs enough available memory to support the Mobility Service in failover situations.</span></span> <span data-ttu-id="369f8-126">Vous pouvez contrôler la quantité de mémoire disponible sur le serveur frontal en utilisant le compteur de **mémoire \\ Mo disponibles** ou en utilisant l’équation mentionnée plus haut, afin de planifier la quantité de mémoire que le service de mobilité devrait utiliser.</span><span class="sxs-lookup"><span data-stu-id="369f8-126">You can monitor the current available memory on the Front End Server by using the **Memory\\Available Mbytes** counter, or by using the equation mentioned earlier, to plan for the amount of memory that you expect the Mobility Service to use.</span></span>

<span data-ttu-id="369f8-127">Si le volume de mémoire disponible sur le serveur frontal est inférieur à 1 500 Mo lorsque vous planifiez le nombre d’utilisateurs de mobilité attendus, vous devez ajouter davantage de matériel pour la prise en charge du service de mobilité.</span><span class="sxs-lookup"><span data-stu-id="369f8-127">If the amount of memory available on the Front End Server is lower than 1,500 MB when you plan for the expected number of mobility users, you need to add more hardware to support the Mobility Service.</span></span> <span data-ttu-id="369f8-128">Pour plus d’informations, reportez-vous à la rubrique [surveillance de mobilité pour les performances dans Lync Server 2013](lync-server-2013-monitoring-mobility-for-performance.md) dans la documentation sur les opérations.</span><span class="sxs-lookup"><span data-stu-id="369f8-128">For more details, see [Monitoring mobility for performance in Lync Server 2013](lync-server-2013-monitoring-mobility-for-performance.md) in the Operations documentation.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="369f8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="369f8-129">See Also</span></span>


[<span data-ttu-id="369f8-130">Surveiller la mobilité des performances dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="369f8-130">Monitoring mobility for performance in Lync Server 2013</span></span>](lync-server-2013-monitoring-mobility-for-performance.md)  
  

<span data-ttu-id="369f8-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="369f8-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

