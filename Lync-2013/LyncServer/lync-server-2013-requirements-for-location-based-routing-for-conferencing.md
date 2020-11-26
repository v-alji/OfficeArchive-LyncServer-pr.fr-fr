---
title: 'Lync Server 2013 : configuration requise pour le routage Location-Based pour les conférences'
description: 'Lync Server 2013 : configuration requise pour le routage Location-Based pour les conférences.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Requirements for Location-Based Routing for conferencing
ms:assetid: 766d9286-2c34-4faf-bb3e-f0ca478a70cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362806(v=OCS.15)
ms:contentKeyID: 56335085
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbaa1af2690c3148d2ecfb173b13be288a21d80f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442662"
---
# <a name="requirements-for-location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="46878-103">Configuration requise pour le routage de Location-Based pour les conférences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46878-103">Requirements for Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="46878-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="46878-104">

<span> </span></span></span>

<span data-ttu-id="46878-105">_**Dernière modification de la rubrique :** 2013-07-19_</span><span class="sxs-lookup"><span data-stu-id="46878-105">_**Topic Last Modified:** 2013-07-19_</span></span>

<span data-ttu-id="46878-106">Voici les exigences requises pour l’installation et la configuration de l’application de conférence de routage Location-Based :</span><span class="sxs-lookup"><span data-stu-id="46878-106">The following are the requirements needed for the installation and configuration of the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="46878-107">La mise à jour cumulative 2 Lync Server 2013 doit être déployée sur tous les serveurs ou pools de votre topologie.</span><span class="sxs-lookup"><span data-stu-id="46878-107">Lync Server 2013 Cumulative Update 2 must be deployed on all servers or pools in your topology.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="46878-108">Si une mise à jour cumulative 2 ou une version ultérieure de Lync Server 2013 n’est pas installée sur un serveur ou un pool Lync dans votre topologie, il est possible de garantir le routage Location-Based de routage des réunions Lync.</span><span class="sxs-lookup"><span data-stu-id="46878-108">If a Lync server or pool in your topology does not have Lync Server 2013 Cumulative Update 2 or higher installed, then enforcement of Location-Based Routing of Lync meetings cannot be guaranteed.</span></span>



</div>

  - <span data-ttu-id="46878-109">Lync Server 2013 Location-Based le routage est une configuration requise pour Location-Based application de conférence de routage.</span><span class="sxs-lookup"><span data-stu-id="46878-109">Lync Server 2013 Location-Based Routing is a pre-requisite for Location-Based Routing Conferencing application.</span></span> <span data-ttu-id="46878-110">Pour plus d’informations sur la configuration du routage de Lync Server 2013 Location-Based, voir [configuration du routage Location-Based](lync-server-2013-configuring-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="46878-110">For further information on configuring Lync Server 2013 Location-Based Routing, please refer to [Configuring Location-Based Routing](lync-server-2013-configuring-location-based-routing.md).</span></span>

  - <span data-ttu-id="46878-111">La configuration requise pour l’application conférences de routage Location-Based est la même que celle de Lync Server 2013 Location-Based routage.</span><span class="sxs-lookup"><span data-stu-id="46878-111">Requirements of Location-Based Routing Conferencing application are the same as the requirements for Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="46878-112">Pour plus d’informations, consultez [planification du routage Location-Based](lync-server-2013-planning-for-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="46878-112">For more information, please refer to [Planning for Location-Based Routing](lync-server-2013-planning-for-location-based-routing.md).</span></span>

<div>

## <a name="supported-servers"></a><span data-ttu-id="46878-113">Serveurs pris en charge</span><span class="sxs-lookup"><span data-stu-id="46878-113">Supported Servers</span></span>

<span data-ttu-id="46878-114">L’application de conférence de routage de Location-Based nécessite que Lync Server 2013 cumulative Update 2 soit déployé sur tous les pools Front-End et les serveurs Standard Edition dans votre topologie.</span><span class="sxs-lookup"><span data-stu-id="46878-114">The Location-Based Routing Conferencing application requires that Lync Server 2013 Cumulative Update 2 is deployed on all Front-End pools and Standard Edition Servers in your topology.</span></span> <span data-ttu-id="46878-115">Si la mise à jour cumulative 2 de Lync Server 2013 n’est pas installée sur certains serveurs Lync dans votre topologie, Location-Based restrictions de routage ne peuvent pas être appliquées entièrement lors de réunions Lync et de transferts d’appels.</span><span class="sxs-lookup"><span data-stu-id="46878-115">If Lync Server 2013 Cumulative Update 2 is not installed on some Lync Servers in your topology, Location-Based Routing restrictions cannot be fully enforced on Lync meetings and consultative call transfers.</span></span>

<span data-ttu-id="46878-116">Le tableau suivant identifie la combinaison de rôles et de versions de serveur prenant en charge le routage Location-Based.</span><span class="sxs-lookup"><span data-stu-id="46878-116">The following table identifies the combination of server roles and versions that support Location-Based Routing.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46878-117">Version de pool frontal</span><span class="sxs-lookup"><span data-stu-id="46878-117">Front-End Pool version</span></span></p></td>
<td><p><span data-ttu-id="46878-118">Version de serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="46878-118">Mediation Server version</span></span></p></td>
<td><p><span data-ttu-id="46878-119">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="46878-119">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46878-120">Mise à jour cumulative 2 de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46878-120">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="46878-121">Mise à jour cumulative 2 de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46878-121">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="46878-122">Oui</span><span class="sxs-lookup"><span data-stu-id="46878-122">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46878-123">Mise à jour cumulative 2 de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46878-123">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="46878-124">Mise à jour cumulative 1 de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46878-124">Lync Server 2013 Cumulative Update 1</span></span></p></td>
<td><p><span data-ttu-id="46878-125">Non</span><span class="sxs-lookup"><span data-stu-id="46878-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46878-126">Mise à jour cumulative 2 de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46878-126">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="46878-127">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="46878-127">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="46878-128">Non</span><span class="sxs-lookup"><span data-stu-id="46878-128">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46878-129">Mise à jour cumulative 2 de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46878-129">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="46878-130">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="46878-130">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="46878-131">Non</span><span class="sxs-lookup"><span data-stu-id="46878-131">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46878-132">Mise à jour cumulative 1 de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46878-132">Lync Server 2013 Cumulative Update 1</span></span></p></td>
<td><p><span data-ttu-id="46878-133">Indifférente</span><span class="sxs-lookup"><span data-stu-id="46878-133">Any</span></span></p></td>
<td><p><span data-ttu-id="46878-134">Non</span><span class="sxs-lookup"><span data-stu-id="46878-134">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46878-135">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="46878-135">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="46878-136">Indifférente</span><span class="sxs-lookup"><span data-stu-id="46878-136">Any</span></span></p></td>
<td><p><span data-ttu-id="46878-137">Non</span><span class="sxs-lookup"><span data-stu-id="46878-137">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46878-138">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="46878-138">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="46878-139">Indifférente</span><span class="sxs-lookup"><span data-stu-id="46878-139">Any</span></span></p></td>
<td><p><span data-ttu-id="46878-140">Non</span><span class="sxs-lookup"><span data-stu-id="46878-140">No</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supported-clients"></a><span data-ttu-id="46878-141">Clients pris en charge</span><span class="sxs-lookup"><span data-stu-id="46878-141">Supported Clients</span></span>

<span data-ttu-id="46878-142">Les clients Lync qui prennent en charge Location-Based le routage des réunions Lync sont les mêmes que ceux prenant en charge le routage Location-Based serveur 2013.</span><span class="sxs-lookup"><span data-stu-id="46878-142">The Lync clients that support Location-Based Routing of Lync meetings are the same clients that support Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="46878-143">Pour plus d’informations, reportez-vous à la [prise en charge du routage Location-Based pour le client et le serveur](lync-server-2013-client-and-server-support-for-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="46878-143">For more information, please refer to [Client and Server Support for Location-Based Routing](lync-server-2013-client-and-server-support-for-location-based-routing.md).</span></span>

</div>

<div>

## <a name="mediation-server-requirements-for-consultative-call-transfers"></a><span data-ttu-id="46878-144">Configuration requise pour le serveur de médiation pour les transferts d’appels</span><span class="sxs-lookup"><span data-stu-id="46878-144">Mediation Server Requirements for Consultative Call Transfers</span></span>

<span data-ttu-id="46878-145">L’application de conférence de routage de Location-Based nécessite le déploiement de serveurs de médiation autonomes pour appliquer des restrictions de routage Location-Based sur les transferts d’appel.</span><span class="sxs-lookup"><span data-stu-id="46878-145">The Location-Based Routing Conferencing application requires deploying stand-alone Mediation Servers in order to enforce Location-Based Routing restrictions on consultative call transfers.</span></span>

<span data-ttu-id="46878-146">Pour faire en sorte qu’il soit nécessaire de mettre en place Location-Based le routage des transferts d’appel, le serveur de médiation doit être associé à un seul homologue du serveur de médiation (PBX, passerelle SIP, etc.) dans les régions réseau où Location-Based routage est requis.</span><span class="sxs-lookup"><span data-stu-id="46878-146">To enforce Location-Based Routing of consultative call transfers, the Mediation Server must be associated with only one Mediation Server peer (i.e. PBX, SIP gateway, etc) in network regions where Location-Based Routing is required.</span></span> <span data-ttu-id="46878-147">Si d’autres homologues du serveur de médiation sont déployés dans la même région réseau, l’homologue du serveur de médiation doit être associé à un serveur de médiation différent.</span><span class="sxs-lookup"><span data-stu-id="46878-147">If additional Mediation Server peers are deployed in the same network region, the Mediation Server peer must be associated with a different Mediation Server .</span></span> <span data-ttu-id="46878-148">Cette obligation est détaillée comme suit :</span><span class="sxs-lookup"><span data-stu-id="46878-148">This Requirement is detailed as follows:</span></span>

  - <span data-ttu-id="46878-149">Serveur de médiation unique par plusieurs homologues du serveur de médiation lorsque le transfert d’appel d’un service de médiation est acheminé vers un serveur de médiation par le biais d’un serveur de médiation configuré avec plusieurs Trunks SIP (par exemple, PBX et passerelles), le transfert d’appel consultatif est bloqué en cas d’annulation du transfert d’appel sur des ISL SIP.</span><span class="sxs-lookup"><span data-stu-id="46878-149">Single Mediation Server per multiple Mediation Server peers When a consultative call transfer is routed to a Mediation Server peer through a Mediation Server that’s configured with multiple SIP trunks to multiple peers (i.e. PBXs and gateways), the consultative call transfer is blocked to prevent PSTN toll bypass if the consultative call transfer is permitted through some SIP trunks but disallowed through other SIP trunks.</span></span>
    
    <span data-ttu-id="46878-150">Par exemple, dans le cas d’un serveur de médiation unique qui dessert un homologue du serveur de médiation de la passerelle RTC et un homologue du serveur de médiation PBX, le comportement suivant est observé :</span><span class="sxs-lookup"><span data-stu-id="46878-150">For example, in the case of a single Mediation Server servicing a PSTN Gateway Mediation Server Peer and a PBX Mediation Server Peer, the following behavior will be observed:</span></span>
    
      - <span data-ttu-id="46878-151">Lorsqu’un utilisateur Lync à partir d’un site donné (par exemple, le site 1) tente de transférer un appel avec un point de terminaison RTC à un utilisateur Lync à partir d’un site différent (par exemple, site 2) par le biais du transfert de consultation, l’appel n’est pas autorisé à éviter le contournement du numéro RTC.</span><span class="sxs-lookup"><span data-stu-id="46878-151">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PSTN endpoint to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed to prevent PSTN toll bypass.</span></span>
    
      - <span data-ttu-id="46878-152">Lorsqu’un utilisateur de Lync à partir d’un site donné (par exemple, le site 1) tente de transférer un appel avec un point de terminaison PBX dans le même site (site 1) pour un utilisateur Lync à partir d’un autre site (par exemple, site 2) via le transfert de consultation, l’appel n’est pas autorisé, même s’il n’est pas en contournement potentiel de péage</span><span class="sxs-lookup"><span data-stu-id="46878-152">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PBX endpoint in the same site (site 1) to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed even if it doesn’t incur in potential PSTN toll bypassing.</span></span>

  - <span data-ttu-id="46878-153">Séparation des serveurs de médiation par le pair du serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="46878-153">Separate Mediation Servers per Mediation Server peer</span></span>
    
    <span data-ttu-id="46878-154">Lorsque le transfert consultatif est ciblé auprès d’un homologue de serveur de médiation, le transfert de la consultation est évalué par rapport à l’homologue du serveur de médiation unique desservi par le serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="46878-154">When a consultative transfer is targeted at a Mediation Server Peer, the consultative transfer will be evaluated against the single Mediation Server Peer serviced by the Mediation Server.</span></span> <span data-ttu-id="46878-155">L’appel sera interdit ou autorisé en fonction de son potentiel dans le cadre du contournement du numéro RTC, quels que soient les autres homologues du site dans le cadre de leur service par des serveurs de médiation distincts.</span><span class="sxs-lookup"><span data-stu-id="46878-155">The call will be disallowed or allowed based in its potential to incur in PSTN toll bypass regardless of all other Mediations Server Peers in the site as they’re serviced by separate Mediation Servers.</span></span>
    
    <span data-ttu-id="46878-156">Par exemple, dans le cas d’un serveur de médiation distinct prenant en service un homologue de serveur de médiation de passerelle RTC et un homologue de serveur de médiation PBX, le comportement suivant est observé :</span><span class="sxs-lookup"><span data-stu-id="46878-156">For example, in the case of a separate Mediation Servers servicing a PSTN Gateway Mediation Server Peer and a PBX Mediation Server Peer, the following behavior will be observed:</span></span>
    
      - <span data-ttu-id="46878-157">Lorsqu’un utilisateur Lync à partir d’un site donné (par exemple, le site 1) tente de transférer un appel avec un point de terminaison RTC à un utilisateur Lync à partir d’un site différent (par exemple, site 2) par le biais du transfert de consultation, l’appel n’est pas autorisé à éviter le contournement du numéro RTC.</span><span class="sxs-lookup"><span data-stu-id="46878-157">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PSTN endpoint to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed to prevent PSTN toll bypass.</span></span>
    
      - <span data-ttu-id="46878-158">Lorsqu’un utilisateur Lync à partir d’un site donné (par exemple, le site 1) tente de transférer un appel avec un point de terminaison PBX au sein d’un même site (site 1) pour un utilisateur Lync à partir d’un site différent (par exemple, site 2) par le biais d’un transfert de consultation, l’appel n’est pas soumis à un problème de péage RTC potentiel.</span><span class="sxs-lookup"><span data-stu-id="46878-158">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PBX endpoint in the same site (site 1) to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be allowed as it doesn’t incur in potential PSTN toll bypassing.</span></span>

</div>

<div>

## <a name="capabilities-not-supported-by-the-location-based-routing-conferencing-application"></a><span data-ttu-id="46878-159">Fonctionnalités non prises en charge par l’application de conférence de routage Location-Based</span><span class="sxs-lookup"><span data-stu-id="46878-159">Capabilities Not Supported by the Location-Based Routing Conferencing Application</span></span>

<span data-ttu-id="46878-160">Les fonctionnalités suivantes ne sont pas prises en charge par l’application de conférence de routage Location-Based :</span><span class="sxs-lookup"><span data-stu-id="46878-160">The following capabilities are not supported by the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="46878-161">Conférence rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="46878-161">Dial-in conferencing.</span></span> <span data-ttu-id="46878-162">Location-Based routage ne peut pas être appliqué pour la Conférence rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="46878-162">Location-Based Routing cannot be enforced for Dial-in conferencing.</span></span> <span data-ttu-id="46878-163">Toute demande d’accès à une conférence donnée n’est pas limitée par Location-Based routage, même si l’organisateur de la Conférence est un utilisateur de Lync activé pour le routage Location-Based.</span><span class="sxs-lookup"><span data-stu-id="46878-163">Any dial-in request to a given conference will not be restricted by Location-Based Routing even if the conference organizer is a Lync user enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="46878-164">Nous vous conseillons de ne pas mettre en place des numéros d’accès aux conférences dans les régions où Location-Based restrictions de routage doivent être appliquées.</span><span class="sxs-lookup"><span data-stu-id="46878-164">It’s recommended not to provision conferencing access numbers in regions where Location-Based Routing restrictions need to be enforced.</span></span>

<span data-ttu-id="46878-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="46878-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

