---
title: 'Lync Server 2013 : configuration du routage géodépendant pour les conférences'
description: 'Lync Server 2013 : configuration du routage Location-Based pour les conférences.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration of Location-Based Routing for conferencing
ms:assetid: d8c708cc-a1b1-48b1-808c-a64df15f7701
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362846(v=OCS.15)
ms:contentKeyID: 56335088
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a87f9c799e565f64b0dd30ce025a4e7a3174625
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395160"
---
# <a name="configuration-of-location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="e81c1-103">Configuration du routage géodépendant pour les conférences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e81c1-103">Configuration of Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e81c1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e81c1-104">

<span> </span></span></span>

<span data-ttu-id="e81c1-105">_**Dernière modification de la rubrique :** 2013-09-11_</span><span class="sxs-lookup"><span data-stu-id="e81c1-105">_**Topic Last Modified:** 2013-09-11_</span></span>

<span data-ttu-id="e81c1-106">L’application de conférence de routage de Location-Based repose sur la configuration de l' Location-Based routage Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e81c1-106">The Location-Based Routing Conferencing application relies on the configuration of Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="e81c1-107">Les configurations principales suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="e81c1-107">The main configurations are the following:</span></span>

  - <span data-ttu-id="e81c1-108">L’emplacement des participants rejoignant une réunion est déterminé sur la base de leur site réseau.</span><span class="sxs-lookup"><span data-stu-id="e81c1-108">The location of participants joining a meeting is determined based on their network site.</span></span> <span data-ttu-id="e81c1-109">Un site réseau et ses sous-réseaux associés doivent être définis dans Lync Server afin de mettre en œuvre le routage Location-Based.</span><span class="sxs-lookup"><span data-stu-id="e81c1-109">A network site and its associated network subnets must be defined in Lync Server in order to enforce Location-Based Routing.</span></span>

  - <span data-ttu-id="e81c1-110">Pour appliquer Location-Based le routage des réunions, les participants de Lync doivent être activés pour le routage Location-Based.</span><span class="sxs-lookup"><span data-stu-id="e81c1-110">To enforce Location-Based Routing of meetings, Lync participants must be enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="e81c1-111">Pour faire en sorte que Location-Based le routage de points de terminaison RTC qui rejoint des réunions, le Trunk SIP utilisé pour connecter les points de terminaison PSTN doit être configuré pour le routage de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="e81c1-111">To enforce Location-Based Routing of PSTN endpoints joining meetings, the SIP trunk used to connect the PSTN endpoints must be configured for Location-Based Routing.</span></span>

<span data-ttu-id="e81c1-112">Pour plus d’informations sur le déploiement et la configuration de Lync Server 2013 Location-Based le routage, consultez la rubrique Configuration du [routage en fonction](lync-server-2013-configuring-location-based-routing.md)de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="e81c1-112">For additional information on deploying and configuring Lync Server 2013 Location-Based Routing, please refer Configuring [Location-Based Routing](lync-server-2013-configuring-location-based-routing.md).</span></span>

<div>

## <a name="enabling-the-location-based-routing-conferencing-application"></a><span data-ttu-id="e81c1-113">Activation de l’application de conférence de routage Location-Based</span><span class="sxs-lookup"><span data-stu-id="e81c1-113">Enabling the Location-Based Routing Conferencing Application</span></span>

<span data-ttu-id="e81c1-114">L’application de conférence de routage Location-Based est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="e81c1-114">The Location-Based Routing Conferencing application is disabled by default.</span></span> <span data-ttu-id="e81c1-115">Avant d’activer cette application, vous devez déterminer la priorité adaptée à affecter à l’application.</span><span class="sxs-lookup"><span data-stu-id="e81c1-115">Before enabling this application, you need to determine the right priority to assign for the application.</span></span> <span data-ttu-id="e81c1-116">Pour déterminer cette priorité, exécutez l’applet de commande suivante dans Lync Server Management Shell :</span><span class="sxs-lookup"><span data-stu-id="e81c1-116">To determine this priority, run the following cmdlet in Lync Server Management Shell:</span></span>

```powershell
Get-CsServerApplication -Identity Service:Registrar:<Pool FQDN>
```

<span data-ttu-id="e81c1-117">Dans cette applet de \<Pool FQDN\> demande, est le pool dans lequel l’application de conférence de routage Location-Based doit être activée.</span><span class="sxs-lookup"><span data-stu-id="e81c1-117">In this cmdlet, \<Pool FQDN\> is the pool in which the Location-Based Routing Conferencing application is to be enabled.</span></span>

<span data-ttu-id="e81c1-118">Ce cmdlet renverra la liste des applications hébergées par Lync Server et la valeur Priority (priorité) pour chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="e81c1-118">This cmdlet will return the list of the applications hosted by Lync Server and the priority value for each of them.</span></span> <span data-ttu-id="e81c1-119">La Location-Based application de conférence de routage doit être attribuée à une valeur de priorité plus grande que l’application « UdcAgent » et inférieure aux applications « DefaultRouting », « ExumRouting » et « OutboundRouting ».</span><span class="sxs-lookup"><span data-stu-id="e81c1-119">The Location-Based Routing Conferencing application needs to be assigned a priority value larger than the “UdcAgent” application and smaller than the “DefaultRouting”, “ExumRouting” and “OutboundRouting” applications.</span></span> <span data-ttu-id="e81c1-120">Nous vous recommandons d’affecter à la Location-Based application de routage une valeur de priorité qui est un point plus élevé que la valeur de priorité de l’application « UdcAgent ».</span><span class="sxs-lookup"><span data-stu-id="e81c1-120">We recommend that you assign the Location-Based Routing Conferencing application a priority value that is one point higher than the priority value of the “UdcAgent” application.</span></span>

<span data-ttu-id="e81c1-121">Par exemple, si l’application « UdcAgent » a une valeur de priorité de « 2 », l’application « DefaultRouting » a une valeur de priorité de « 9 », l’application « ExumRouting » a une valeur de priorité de « 9 » et l’application « OutboundRouting » a une valeur de priorité de « 10 », alors vous devez attribuer à la Location-Based l’application de routage de routage.</span><span class="sxs-lookup"><span data-stu-id="e81c1-121">For example, if the “UdcAgent” application has a priority value of “2”, the “DefaultRouting” application has a priority value of “8”, the “ExumRouting” application has a priority value of “9” and the “OutboundRouting” application has a priority value of “10” then you should assign the Location-Based Routing Conferencing application a priority value of “3”.</span></span> <span data-ttu-id="e81c1-122">Ainsi, la priorité des applications est définie dans l’ordre suivant : autres applications (priorités : 0 à 1), « UdcAgent » (priorité : 2), application de conférence avec routage géodépendant (priorité : 3), autres applications (priorités : 4 à 8), « DefaultRouting » (priorité : 9), « ExumRouting » (priorité : 10) et « OutboundRouting » (priorité : 11).</span><span class="sxs-lookup"><span data-stu-id="e81c1-122">Doing so would place the priority of the applications in the following order: Other applications (Priorities: 0 to 1), “UdcAgent” (Priority: 2), Location-Based Routing Conferencing application (Priority: 3), other applications (Priorities: 4 to 8), “DefaultRouting” (Priority: 9), “ExumRouting” (Priority: 10) and “OutboundRouting” (Priority: 11).</span></span>

<span data-ttu-id="e81c1-123">Une fois que vous avez trouvé la valeur de priorité correcte pour l’application de conférence de routage Location-Based, tapez l’applet de commande suivante pour chaque pool Front-End ou un serveur Standard Edition sur lequel les utilisateurs ont activé le routage Location-Based :</span><span class="sxs-lookup"><span data-stu-id="e81c1-123">After you find the correct priority value for the Location-Based Routing Conferencing application, type the following cmdlet for each Front-End pool or Standard Edition Server that homes users enabled for Location-Based Routing:</span></span>

```powershell
New-CsServerApplication -Identity Service:Registrar:<Pool FQDN>/LBRouting -Priority <Application Priority> -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

<span data-ttu-id="e81c1-124">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e81c1-124">For example:</span></span>

```powershell
New-CsServerApplication -Identity Service:Registrar:LS2013CU2LBRPool.contoso.com/LBRouting -Priority 3 -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

<span data-ttu-id="e81c1-125">Après avoir utilisé cette applet de demande, redémarrez tous les serveurs frontaux dans le pool ou les serveurs Standard Edition sur lesquels l’application de conférence de routage Location-Based est activée.</span><span class="sxs-lookup"><span data-stu-id="e81c1-125">After using this cmdlet, restart all Front End servers in the pool or the Standard Edition Servers where the Location-Based Routing Conferencing application has been enabled.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="e81c1-126">Location-Based le routage des mises en œuvre vers des conférences ou des transferts de consultation ne seront pas appliqués tant que tous les serveurs frontaux dans les pools applicables ou les serveurs Standard Edition n’ont pas été redémarrés.</span><span class="sxs-lookup"><span data-stu-id="e81c1-126">Location-Based Routing enforcements to conferences or consultative transfers won’t be enforced until all the Front End Servers in the applicable pools or the Standard Edition Servers are restarted.</span></span>



</div>

<span data-ttu-id="e81c1-127">Lorsque l’application de conférence de routage de Location-Based est activée et que tous les serveurs Lync en vigueur ont été redémarrés, toutes les conférences organisées par les utilisateurs de Lync activées pour le routage Location-Based seront surveillées de façon à éviter le contournement du numéro RTC</span><span class="sxs-lookup"><span data-stu-id="e81c1-127">Once the Location-Based Routing Conferencing application has been successfully enabled and all applicable Lync servers have been restarted, all conferences organized by Lync users enabled for Location-Based Routing will be monitored to prevent PSTN toll bypass</span></span>

<span data-ttu-id="e81c1-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e81c1-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

