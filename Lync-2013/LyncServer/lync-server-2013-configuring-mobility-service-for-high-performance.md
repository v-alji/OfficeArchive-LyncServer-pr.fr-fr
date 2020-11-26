---
title: 'Lync Server 2013 : configuration d’un service de mobilité pour des performances élevées'
description: 'Lync Server 2013 : configuration d’un service de mobilité pour des performances optimales.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Mobility Service for high performance
ms:assetid: c2b8aadb-cffb-49f0-ba7a-e8541a1ff475
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690042(v=OCS.15)
ms:contentKeyID: 48185332
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4732d9f6a92c383a105a6f0d7162c9b6c798de24
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432883"
---
# <a name="configuring-mobility-service-for-high-performance-in-lync-server-2013"></a><span data-ttu-id="3f440-103">Configuration d’un service de mobilité pour des performances élevées dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f440-103">Configuring Mobility Service for high performance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f440-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f440-104">

<span> </span></span></span>

<span data-ttu-id="3f440-105">_**Dernière modification de la rubrique :** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="3f440-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3f440-106">Cette rubrique s’applique uniquement au service de mobilité Lync Server 2013 (MCX) et ne s’applique pas à l’API Unified Communications Web API (UCWA), comme il est fourni dans les mises à jour cumulatives de Lync Server 2013:2013 février.</span><span class="sxs-lookup"><span data-stu-id="3f440-106">This topic applies only to the Lync Server 2013 Mobility Service (Mcx), and does not apply to Unified Communications Web API (UCWA), as delivered in the Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

<span data-ttu-id="3f440-107">Lorsque vous installez le service de mobilité (MCX) sur Internet Information Services (IIS) 7,5, le programme d’installation de service de mobilité configure certains paramètres de performance sur le serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="3f440-107">When you install the Mobility Service (Mcx) on Internet Information Services (IIS) 7.5, the Mobility Service installer configures some performance settings on the Front End Server.</span></span> <span data-ttu-id="3f440-108">Nous vous recommandons d’utiliser les services Internet (IIS) 7.5 pour la mobilité.</span><span class="sxs-lookup"><span data-stu-id="3f440-108">We recommend that you use IIS 7.5 for mobility.</span></span> <span data-ttu-id="3f440-109">Ceux-ci affectent la quantité maximale de demandes utilisateur simultanées et la quantité maximale de threads autorisés pour le service de mobilité.</span><span class="sxs-lookup"><span data-stu-id="3f440-109">The settings affect the maximum number of concurrent user requests and the maximum number of threads that are allowed for the Mobility Service.</span></span>

<span data-ttu-id="3f440-110">Voici les paramètres de performances :</span><span class="sxs-lookup"><span data-stu-id="3f440-110">Here are the performance settings:</span></span>

<div>

## <a name="settings-for-mcx-on-iis-75"></a><span data-ttu-id="3f440-111">Paramètres pour Mcx sur IIS 7.5</span><span class="sxs-lookup"><span data-stu-id="3f440-111">Settings for Mcx on IIS 7.5</span></span>

1.  <span data-ttu-id="3f440-112">**maxConcurrentThreadsPerCPU** est fixé sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="3f440-112">**maxConcurrentThreadsPerCPU** is set to zero (0).</span></span>

2.  <span data-ttu-id="3f440-113">**maxConcurrentRequestsPerCPU** est fixé sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="3f440-113">**maxConcurrentRequestsPerCPU** is set to zero (0).</span></span>

3.  <span data-ttu-id="3f440-114">Le modèle de processus ASP.NET est AutoConfig (pour les services Internet (IIS) 7.5 uniquement).</span><span class="sxs-lookup"><span data-stu-id="3f440-114">ASP.NET process model is set to AutoConfig (for IIS 7.5 only).</span></span>

4.  <span data-ttu-id="3f440-115">La limite de file d’attente HTTP.sys a la valeur 1 000 (par défaut).</span><span class="sxs-lookup"><span data-stu-id="3f440-115">HTTP.sys queue limit is set to 1,000 (by default).</span></span>

<span data-ttu-id="3f440-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f440-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

