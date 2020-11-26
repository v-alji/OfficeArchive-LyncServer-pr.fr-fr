---
title: Configuration requise pour l’équilibreur de charge matérielle pour Lync Server 2013
description: Configuration requise pour le système d’équilibrage de charge matérielle de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardware load balancer requirements
ms:assetid: 32891268-2059-43d0-adf4-af4ff1e9ce66
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ656815(v=OCS.15)
ms:contentKeyID: 49287208
ms.date: 05/11/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69cbf79c1fd7551dfd428c23ed22c924d0805c43
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427718"
---
# <a name="hardware-load-balancer-requirements-for-lync-server-2013"></a><span data-ttu-id="d9198-103">Configuration requise pour l’équilibreur de charge matérielle pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d9198-103">Hardware load balancer requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d9198-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d9198-104">

<span> </span></span></span>

<span data-ttu-id="d9198-105">_**Dernière modification de la rubrique :** 2015-05-11_</span><span class="sxs-lookup"><span data-stu-id="d9198-105">_**Topic Last Modified:** 2015-05-11_</span></span>

<span data-ttu-id="d9198-106">La topologie de périphérie consolidée de Lync Server 2013 est optimisée pour l’équilibrage de charge DNS pour les nouveaux déploiements qui se fédère principalement avec d’autres organisations à l’aide de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d9198-106">The Lync Server 2013 scaled consolidated Edge topology is optimized for DNS load balancing for new deployments federating primarily with other organizations using Lync Server.</span></span> <span data-ttu-id="d9198-107">S’il est nécessaire de disposer d’une haute disponibilité pour l’un des scénarios suivants, un équilibreur de charge matérielle doit être utilisé sur les pools de serveurs Edge pour les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d9198-107">If high availability is required for any of the following scenarios, a hardware load balancer must be used on Edge Server pools for the following:</span></span>

  - <span data-ttu-id="d9198-108">Fédération avec des organisations qui utilisent Office Communications Server 2007 R2 ou Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="d9198-108">Federation with organizations using Office Communications Server 2007 R2 or Office Communications Server 2007</span></span>

  - <span data-ttu-id="d9198-109">Messagerie unifiée Exchange pour les utilisateurs distants utilisant la messagerie unifiée Exchange antérieure à Exchange 2010 avec SP1</span><span class="sxs-lookup"><span data-stu-id="d9198-109">Exchange UM for remote users using Exchange UM prior to Exchange 2010 with SP1</span></span>

  - <span data-ttu-id="d9198-110">Connectivité avec les utilisateurs de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="d9198-110">Connectivity to public IM users</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d9198-p102">L’utilisation de l’équilibrage de charge DNS sur une interface et de l’équilibrage de charge matérielle sur l’autre n’est pas prise en charge. Sur les deux interfaces, vous devez utiliser l’équilibrage de charge matérielle ou l’équilibrage de charge DNS.</span><span class="sxs-lookup"><span data-stu-id="d9198-p102">Using DNS load balancing on one interface and hardware load balancing on the other is not supported. You must use hardware load balancing for both interfaces or DNS load balancing for both.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="d9198-p103">Si vous utilisez un équilibreur de la charge matérielle, celui qui est déployé pour les connexions au réseau interne doit être configuré pour équilibrer uniquement la charge liée au trafic en direction de serveurs exécutant le service d’accès Edge et le service Edge A/V. Il ne peut pas équilibrer la charge du trafic vers le service Edge de conférence web ou le service de proxy XMPP interne.</span><span class="sxs-lookup"><span data-stu-id="d9198-p103">If you are using a hardware load balancer, the load balancer deployed for connections with the internal network must be configured to load balance only the traffic to servers running the Access Edge service and the A/V Edge service. It cannot load balance the traffic to the internal Web Conferencing Edge service or the internal XMPP Proxy service.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="d9198-115">La traduction d’adresses réseau (DSR) direct Server n’est pas prise en charge avec Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d9198-115">The direct server return (DSR) NAT is not supported with Lync Server 2013.</span></span>



</div>

<span data-ttu-id="d9198-116">Pour savoir si votre équilibreur de charge matérielle prend en charge les fonctionnalités nécessaires requises par Lync Server 2013, voir « partenaires d’équilibrage de charge Lync Server 2010 » à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=202452](https://go.microsoft.com/fwlink/p/?linkid=202452) .</span><span class="sxs-lookup"><span data-stu-id="d9198-116">To determine whether your hardware load balancer supports the necessary features required by Lync Server 2013, see "Lync Server 2010 Load Balancer Partners" at [https://go.microsoft.com/fwlink/p/?linkId=202452](https://go.microsoft.com/fwlink/p/?linkid=202452).</span></span>

<div>

## <a name="hardware-load-balancer-requirements-for-edge-servers-running-the-av-edge-service"></a><span data-ttu-id="d9198-117">Configuration requise pour l’équilibreur de la charge matérielle des serveurs Edge exécutant le service Edge A/V</span><span class="sxs-lookup"><span data-stu-id="d9198-117">Hardware Load Balancer Requirements for Edge Servers Running the A/V Edge Service</span></span>

<span data-ttu-id="d9198-118">Vous trouverez ci-après les exigences relatives à l’équilibrage de charge matérielle pour les serveurs Edge exécutant le service Edge A/V :</span><span class="sxs-lookup"><span data-stu-id="d9198-118">Following are the hardware load balancer requirements for Edge Servers running the A/V Edge service:</span></span>

  - <span data-ttu-id="d9198-p104">Désactivez le nagling TCP pour les ports 443 interne et externe. Le nagling est le processus qui consiste à combiner plusieurs petits paquets en un seul paquet plus volumineux afin de rendre la transmission plus efficace.</span><span class="sxs-lookup"><span data-stu-id="d9198-p104">Turn off TCP nagling for both internal and external ports 443. Nagling is the process of combining several small packets into a single, larger packet for more efficient transmission.</span></span>

  - <span data-ttu-id="d9198-121">Désactivez le nagling TCP pour la plage de ports externes 50 000 – 59 999.</span><span class="sxs-lookup"><span data-stu-id="d9198-121">Turn off TCP nagling for external port range 50,000 – 59,999.</span></span>

  - <span data-ttu-id="d9198-122">N’utilisez pas NAT sur le pare-feu interne ou externe.</span><span class="sxs-lookup"><span data-stu-id="d9198-122">Do not use NAT on the internal or external firewall.</span></span>

  - <span data-ttu-id="d9198-123">L’interface interne Edge doit être située sur un autre réseau que l’interface externe du serveur Edge et le routage entre ces derniers doit être désactivé.</span><span class="sxs-lookup"><span data-stu-id="d9198-123">The edge internal interface must be on a different network than the Edge Server external interface and routing between them must be disabled.</span></span>

  - <span data-ttu-id="d9198-124">L’interface externe du serveur de périphérie exécutant le service Edge A/V doit utiliser les adresses IP routables publiquement et aucune traduction NAT ou de port sur les adresses IP externes du bord.</span><span class="sxs-lookup"><span data-stu-id="d9198-124">The external interface of the Edge Server running the A/V Edge Service must use publicly routable IP addresses and no NAT or port translation on any of the edge external IP addresses.</span></span>

</div>

<div>

## <a name="hardware-load-balancer-requirements"></a><span data-ttu-id="d9198-125">Configuration requise pour l’équilibreur de charge matérielle</span><span class="sxs-lookup"><span data-stu-id="d9198-125">Hardware Load Balancer Requirements</span></span>

<span data-ttu-id="d9198-126">Les exigences d’affinité basées sur les cookies sont considérablement réduites dans Lync Server 2013 pour les services Web.</span><span class="sxs-lookup"><span data-stu-id="d9198-126">Cookie-based affinity requirements are greatly reduced in Lync Server 2013 for Web services.</span></span> <span data-ttu-id="d9198-127">Si vous déployez Lync Server 2013 et ne conservera aucun serveur frontal ou pool frontal de Lync Server 2010, vous n’avez pas besoin d’une persistance basée sur les cookies.</span><span class="sxs-lookup"><span data-stu-id="d9198-127">If you are deploying Lync Server 2013 and will not retain any Lync Server 2010 Front End Servers or Front End pools, you do not need cookie-based persistence.</span></span> <span data-ttu-id="d9198-128">Toutefois, si vous conservez temporairement ou définitivement tout serveur frontal ou pool frontal de Lync Server 2010, vous utiliserez quand même le niveau de persistance de cookie tel qu’il sera déployé et configuré pour Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d9198-128">However, if you will temporarily or permanently retain any Lync Server 2010 Front End Servers or Front End pools, you still use cookie-based persistence as it is deployed and configured for Lync Server 2010.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d9198-129"><STRONG>Si vous décidez d’utiliser l’affinité basée sur les cookies même si votre déploiement n’en a pas besoin</STRONG>, aucun impact négatif n’en résultera.</span><span class="sxs-lookup"><span data-stu-id="d9198-129"><STRONG>If you decide to use cookie-based affinity even though your deployment does not require it</STRONG>, there is no negative impact to doing so.</span></span>



</div>

<span data-ttu-id="d9198-130">Pour les déploiements qui **nʼutiliseront pas** lʼaffinité basée sur les cookies :</span><span class="sxs-lookup"><span data-stu-id="d9198-130">For deployments that **will not use** cookie-based affinity:</span></span>

  - <span data-ttu-id="d9198-p106">Dans la règle de publication du proxy inverse pour le port 4443, définissez **Forward host header** sur True afin de vous assurer que lʼURL dʼorigine est envoyée.</span><span class="sxs-lookup"><span data-stu-id="d9198-p106">On the reverse proxy publishing rule for port 4443, set **Forward host header** to True. This will ensure that the original URL is forwarded.</span></span>

<span data-ttu-id="d9198-133">Pour des déploiements qui **utiliseront** lʼaffinité basée sur les cookies :</span><span class="sxs-lookup"><span data-stu-id="d9198-133">For deployments that **will use** cookie-based affinity:</span></span>

  - <span data-ttu-id="d9198-p107">Dans la règle de publication du proxy inverse pour le port 4443, définissez **Forward host header** sur True afin de vous assurer que lʼURL dʼorigine est envoyée.</span><span class="sxs-lookup"><span data-stu-id="d9198-p107">On the reverse proxy publishing rule for port 4443, set **Forward host header** to True. This will ensure that the original URL is forwarded.</span></span>

  - <span data-ttu-id="d9198-136">Le cookie de l’équilibreur de la charge matérielle NE DOIT PAS être marqué httpOnly</span><span class="sxs-lookup"><span data-stu-id="d9198-136">Hardware load balancer cookie MUST NOT be marked httpOnly</span></span>

  - <span data-ttu-id="d9198-137">Le cookie de l’équilibreur de la charge matérielle NE DOIT PAS inclure d’heure d’expiration</span><span class="sxs-lookup"><span data-stu-id="d9198-137">Hardware load balancer cookie MUST NOT have an expiration time</span></span>

  - <span data-ttu-id="d9198-138">Le cookie de l’équilibreur de la charge matérielle DOIT être nommé **MS-WSMAN** (Il s’agit de la valeur attendue par les services web et elle ne peut pas être modifiée)</span><span class="sxs-lookup"><span data-stu-id="d9198-138">Hardware load balancer cookie MUST be named **MS-WSMAN** (This is the value that the Web services expect, and cannot be changed)</span></span>

  - <span data-ttu-id="d9198-p108">Le cookie de l’équilibreur de la charge matérielle DOIT être défini dans chaque réponse HTTP pour laquelle la requête HTTP entrante ne possédait pas de cookie, qu’une réponse HTTP précédente ait déjà obtenu ou non un cookie sur cette même connexion TCP. Si l’équilibreur de la charge optimise l’insertion de cookies afin qu’elle se produise une seule fois par connexion TCP, cette optimisation NE DOIT PAS être utilisée</span><span class="sxs-lookup"><span data-stu-id="d9198-p108">Hardware load balancer cookie MUST be set in every HTTP response for which the incoming HTTP request did not have a cookie, regardless of whether a previous HTTP response on that same TCP connection had already obtained a cookie. If the load balancer optimizes cookie insert to only occur once per TCP connection, that optimization MUST NOT be used</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d9198-141">Les configurations standard du programme d’équilibrage de la charge matérielle utilisent l’affinité adresse source et une durée de vie de session de 20 minutes, qui convient aux clients Lync Server et Lync 2013, car l’état de session est maintenu par le biais de l’utilisation du client et/ou de l’interaction avec l’application.</span><span class="sxs-lookup"><span data-stu-id="d9198-141">Typical hardware load balancer configurations use source-address affinity and a 20 min. TCP session lifetime, which is fine for Lync Server and Lync 2013 clients because session state is maintained through client usage and/or and application interaction.</span></span>



</div>

<span data-ttu-id="d9198-142">Si vous déployez des appareils mobiles, votre équilibreur de la charge matérielle doit être capable d’équilibrer la charge d’une requête individuelle au sein d’une session TCP (en effet, vous devez être en mesure d’équilibrer la charge d’une requête individuelle en fonction de l’adresse IP cible).</span><span class="sxs-lookup"><span data-stu-id="d9198-142">If you are deploying mobile devices, your hardware load balancer must be able to load balance individual request within a TCP session (in effect, you must be able to load balance an individual request based on the target IP address).</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="d9198-p109">Les programmes d’équilibrage de la charge matérielle F5 possèdent une fonctionnalité appelée OneConnect qui permet de veiller à ce que la charge de chaque requête au sein d’une connexion TCP soit individuellement équilibrée. Si vous déployez des appareils mobiles, veillez à ce que le fournisseur de votre équilibreur de la charge matérielle prenne en charge la même fonctionnalité. Les dernières applications pour mobile iOS d’Apple requièrent la version 1.2 de TLS (Transport Layer Security). F5 fournit les paramètres spécifiques pour cela.</span><span class="sxs-lookup"><span data-stu-id="d9198-p109">F5 hardware load balancers have a feature called OneConnect that ensures each request within a TCP connection is individually load balanced. If you are deploying mobile devices, ensure your hardware load balancer vendor supports the same functionality. The latest Apple iOS mobile apps require Transport Layer Security (TLS) version 1.2. F5 provides specific settings for this.</span></span><BR><span data-ttu-id="d9198-147">Pour plus d’informations sur les équilibreurs de charge matérielle tiers, voir <A href="https://go.microsoft.com/fwlink/p/?linkid=230700">https://go.microsoft.com/fwlink/p/?linkId=230700</A></span><span class="sxs-lookup"><span data-stu-id="d9198-147">For details on third party hardware load balancers, see <A href="https://go.microsoft.com/fwlink/p/?linkid=230700">https://go.microsoft.com/fwlink/p/?linkId=230700</A></span></span>



</div>

<span data-ttu-id="d9198-148">La configuration requise de l’équilibreur de la charge matérielle des services web du directeur et du pool de serveurs frontaux est la suivante :</span><span class="sxs-lookup"><span data-stu-id="d9198-148">Following are the hardware load balancer requirements for Director and Front End pool Web Services:</span></span>

  - <span data-ttu-id="d9198-149">Pour les VIP de services Web internes, définissez \_ persistance de l’adresse source (port interne 80, 443) sur le système d’équilibrage de la charge matérielle.</span><span class="sxs-lookup"><span data-stu-id="d9198-149">For internal Web Services VIPs, set Source\_addr persistence (internal port 80, 443) on the hardware load balancer.</span></span> <span data-ttu-id="d9198-150">Pour Lync Server 2013, la \_ persistance de l’adresse source indique que plusieurs connexions venant d’une seule adresse IP sont toujours envoyées à un serveur pour conserver l’état de la session.</span><span class="sxs-lookup"><span data-stu-id="d9198-150">For Lync Server 2013, Source\_addr persistence means that multiple connections coming from a single IP address are always sent to one server to maintain session state.</span></span>

  - <span data-ttu-id="d9198-151">Utilisez un délai d’inactivité TCP de 1 800 secondes.</span><span class="sxs-lookup"><span data-stu-id="d9198-151">Use TCP idle timeout of 1800 seconds.</span></span>

  - <span data-ttu-id="d9198-p111">Sur le pare-feu situé entre le proxy inverse et l’équilibreur de la charge matérielle du pool du tronçon suivant, créez une règle autorisant le trafic https: sur le port 4443, entre le proxy inverse et l’équilibreur de la charge matérielle. L’équilibreur de la charge matérielle doit être configuré pour écouter sur les ports 80, 443 et 4443.</span><span class="sxs-lookup"><span data-stu-id="d9198-p111">On the firewall between the reverse proxy and the next hop pool’s hardware load balancer, create a rule to allow https: traffic on port 4443, from the reverse proxy to the hardware load balancer. The hardware load balancer must be configured to listen on ports 80, 443, and 4443.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d9198-154">Pour en savoir plus sur la configuration de l’équilibrage de charge matérielle, consultez l’article <A href="lync-server-2013-port-summary-scaled-consolidated-edge-with-hardware-load-balancers.md">Résumé du port-frontière consolidée avec des équilibreurs de charge matérielle dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="d9198-154">For further reading on configuration of the hardware load balancer, please review <A href="lync-server-2013-port-summary-scaled-consolidated-edge-with-hardware-load-balancers.md">Port summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</A>.</span></span>



</div>

</div>

<div>

## <a name="summary-of-hardware-load-balancer-affinity-requirements"></a><span data-ttu-id="d9198-155">Synthèse des conditions requises en termes d’affinité pour l’équilibreur de la charge matérielle</span><span class="sxs-lookup"><span data-stu-id="d9198-155">Summary of Hardware Load Balancer Affinity Requirements</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9198-156">Emplacement du client/de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="d9198-156">Client/user location</span></span></th>
<th><span data-ttu-id="d9198-157">Conditions requises en matière d’affinité pour le nom de domaine complet des services web externes</span><span class="sxs-lookup"><span data-stu-id="d9198-157">External web services FQDN affinity requirements</span></span></th>
<th><span data-ttu-id="d9198-158">Conditions requises en matière d’affinité pour le nom de domaine complet des services web internes</span><span class="sxs-lookup"><span data-stu-id="d9198-158">Internal web services FQDN affinity requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9198-159">Lync Web App (utilisateurs internes et externes)</span><span class="sxs-lookup"><span data-stu-id="d9198-159">Lync Web App (internal and external users)</span></span></p>
<p><span data-ttu-id="d9198-160">Appareil mobile (utilisateurs internes et externes)</span><span class="sxs-lookup"><span data-stu-id="d9198-160">Mobile device (internal and external users)</span></span></p></td>
<td><p><span data-ttu-id="d9198-161">Aucune affinité</span><span class="sxs-lookup"><span data-stu-id="d9198-161">No affinity</span></span></p></td>
<td><p><span data-ttu-id="d9198-162">Affinité des adresses sources</span><span class="sxs-lookup"><span data-stu-id="d9198-162">Source address affinity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9198-163">Lync Web App (utilisateurs externes uniquement)</span><span class="sxs-lookup"><span data-stu-id="d9198-163">Lync Web App (external users only)</span></span></p>
<p><span data-ttu-id="d9198-164">Appareil mobile (utilisateurs internes et externes)</span><span class="sxs-lookup"><span data-stu-id="d9198-164">Mobile device (internal and external users)</span></span></p></td>
<td><p><span data-ttu-id="d9198-165">Aucune affinité</span><span class="sxs-lookup"><span data-stu-id="d9198-165">No affinity</span></span></p></td>
<td><p><span data-ttu-id="d9198-166">Affinité des adresses sources</span><span class="sxs-lookup"><span data-stu-id="d9198-166">Source address affinity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9198-167">Lync Web App (utilisateurs internes uniquement)</span><span class="sxs-lookup"><span data-stu-id="d9198-167">Lync Web App (internal users only)</span></span></p>
<p><span data-ttu-id="d9198-168">Appareil mobile (non déployé)</span><span class="sxs-lookup"><span data-stu-id="d9198-168">Mobile device (not deployed)</span></span></p></td>
<td><p><span data-ttu-id="d9198-169">Aucune affinité</span><span class="sxs-lookup"><span data-stu-id="d9198-169">No affinity</span></span></p></td>
<td><p><span data-ttu-id="d9198-170">Affinité des adresses sources</span><span class="sxs-lookup"><span data-stu-id="d9198-170">Source address affinity</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="port-monitoring-for-hardware-load-balancers"></a><span data-ttu-id="d9198-171">Surveillance des ports pour les programmes d’équilibrage de la charge matérielle</span><span class="sxs-lookup"><span data-stu-id="d9198-171">Port Monitoring for Hardware Load Balancers</span></span>

<span data-ttu-id="d9198-172">Vous définissez la surveillance des ports sur les équilibreurs de la charge matérielle pour déterminer si des services spécifiques ne sont plus disponibles suite à des échecs matériel ou de communication.</span><span class="sxs-lookup"><span data-stu-id="d9198-172">You define port monitoring on the hardware load balancers to determine when specific services are no longer available due to hardware or communications failure.</span></span> <span data-ttu-id="d9198-173">Par exemple, si le service serveur frontal (RTCSRV) s’arrête en raison d’un dysfonctionnement du serveur frontal ou du pool frontal, la surveillance de HLB doit également arrêter la réception du trafic sur les services Web.</span><span class="sxs-lookup"><span data-stu-id="d9198-173">For example, if the Front End Server service (RTCSRV) stops because the Front End Server or Front End pool fails, the HLB monitoring should also stop receiving traffic on the Web Services.</span></span> <span data-ttu-id="d9198-174">Vous implémentez la surveillance des ports sur le programme d’équilibrage de la charge matérielle pour surveiller les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d9198-174">You implement port monitoring on the HLB to monitor the following:</span></span>

### <a name="front-end-server-user-pool--hlb-internal-interface"></a><span data-ttu-id="d9198-175">Pool d’utilisateurs du serveur frontal-interface interne HLB</span><span class="sxs-lookup"><span data-stu-id="d9198-175">Front End Server User Pool – HLB Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9198-176">IP/Port virtuel</span><span class="sxs-lookup"><span data-stu-id="d9198-176">Virtual IP/Port</span></span></th>
<th><span data-ttu-id="d9198-177">Port de nœud</span><span class="sxs-lookup"><span data-stu-id="d9198-177">Node Port</span></span></th>
<th><span data-ttu-id="d9198-178">Nœud Ordinateur/Écran</span><span class="sxs-lookup"><span data-stu-id="d9198-178">Node Machine/Monitor</span></span></th>
<th><span data-ttu-id="d9198-179">Profil de persistance</span><span class="sxs-lookup"><span data-stu-id="d9198-179">Persistence Profile</span></span></th>
<th><span data-ttu-id="d9198-180">Remarques</span><span class="sxs-lookup"><span data-stu-id="d9198-180">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9198-181">&lt;&gt;site Web de pool-int_mco_443_vs</span><span class="sxs-lookup"><span data-stu-id="d9198-181">&lt;pool&gt;web-int_mco_443_vs</span></span></p>
<p><span data-ttu-id="d9198-182">443</span><span class="sxs-lookup"><span data-stu-id="d9198-182">443</span></span></p></td>
<td><p><span data-ttu-id="d9198-183">443</span><span class="sxs-lookup"><span data-stu-id="d9198-183">443</span></span></p></td>
<td><p><span data-ttu-id="d9198-184">Serveur frontal</span><span class="sxs-lookup"><span data-stu-id="d9198-184">Front End</span></span></p>
<p><span data-ttu-id="d9198-185">5061</span><span class="sxs-lookup"><span data-stu-id="d9198-185">5061</span></span></p></td>
<td><p><span data-ttu-id="d9198-186">Source</span><span class="sxs-lookup"><span data-stu-id="d9198-186">Source</span></span></p></td>
<td><p><span data-ttu-id="d9198-187">HTTPS</span><span class="sxs-lookup"><span data-stu-id="d9198-187">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9198-188">&lt;&gt;site Web de pool-int_mco_80_vs</span><span class="sxs-lookup"><span data-stu-id="d9198-188">&lt;pool&gt;web-int_mco_80_vs</span></span></p>
<p><span data-ttu-id="d9198-189">80</span><span class="sxs-lookup"><span data-stu-id="d9198-189">80</span></span></p></td>
<td><p><span data-ttu-id="d9198-190">80</span><span class="sxs-lookup"><span data-stu-id="d9198-190">80</span></span></p></td>
<td><p><span data-ttu-id="d9198-191">Serveur frontal</span><span class="sxs-lookup"><span data-stu-id="d9198-191">Front End</span></span></p>
<p><span data-ttu-id="d9198-192">5061</span><span class="sxs-lookup"><span data-stu-id="d9198-192">5061</span></span></p></td>
<td><p><span data-ttu-id="d9198-193">Source</span><span class="sxs-lookup"><span data-stu-id="d9198-193">Source</span></span></p></td>
<td><p><span data-ttu-id="d9198-194">HTTP</span><span class="sxs-lookup"><span data-stu-id="d9198-194">HTTP</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="front-end-server-user-pool--hlb-external-interface"></a><span data-ttu-id="d9198-195">Pool d’utilisateurs du serveur frontal-interface externe HLB</span><span class="sxs-lookup"><span data-stu-id="d9198-195">Front End Server User Pool – HLB External Interface</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9198-196">IP/Port virtuel</span><span class="sxs-lookup"><span data-stu-id="d9198-196">Virtual IP/Port</span></span></th>
<th><span data-ttu-id="d9198-197">Port de nœud</span><span class="sxs-lookup"><span data-stu-id="d9198-197">Node Port</span></span></th>
<th><span data-ttu-id="d9198-198">Nœud Ordinateur/Écran</span><span class="sxs-lookup"><span data-stu-id="d9198-198">Node Machine/Monitor</span></span></th>
<th><span data-ttu-id="d9198-199">Profil de persistance</span><span class="sxs-lookup"><span data-stu-id="d9198-199">Persistence Profile</span></span></th>
<th><span data-ttu-id="d9198-200">Remarques</span><span class="sxs-lookup"><span data-stu-id="d9198-200">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9198-201">&lt;web_mco_443_vs de réserve &gt;</span><span class="sxs-lookup"><span data-stu-id="d9198-201">&lt;pool&gt;web_mco_443_vs</span></span></p>
<p><span data-ttu-id="d9198-202">443</span><span class="sxs-lookup"><span data-stu-id="d9198-202">443</span></span></p></td>
<td><p><span data-ttu-id="d9198-203">4443</span><span class="sxs-lookup"><span data-stu-id="d9198-203">4443</span></span></p></td>
<td><p><span data-ttu-id="d9198-204">Serveur frontal</span><span class="sxs-lookup"><span data-stu-id="d9198-204">Front End</span></span></p>
<p><span data-ttu-id="d9198-205">5061</span><span class="sxs-lookup"><span data-stu-id="d9198-205">5061</span></span></p></td>
<td><p><span data-ttu-id="d9198-206">Aucune</span><span class="sxs-lookup"><span data-stu-id="d9198-206">None</span></span></p></td>
<td><p><span data-ttu-id="d9198-207">HTTPS</span><span class="sxs-lookup"><span data-stu-id="d9198-207">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9198-208">&lt;web_mco_80_vs de réserve &gt;</span><span class="sxs-lookup"><span data-stu-id="d9198-208">&lt;pool&gt;web_mco_80_vs</span></span></p>
<p><span data-ttu-id="d9198-209">80</span><span class="sxs-lookup"><span data-stu-id="d9198-209">80</span></span></p></td>
<td><p><span data-ttu-id="d9198-210">8080</span><span class="sxs-lookup"><span data-stu-id="d9198-210">8080</span></span></p></td>
<td><p><span data-ttu-id="d9198-211">Serveur frontal</span><span class="sxs-lookup"><span data-stu-id="d9198-211">Front End</span></span></p>
<p><span data-ttu-id="d9198-212">5061</span><span class="sxs-lookup"><span data-stu-id="d9198-212">5061</span></span></p></td>
<td><p><span data-ttu-id="d9198-213">Aucune</span><span class="sxs-lookup"><span data-stu-id="d9198-213">None</span></span></p></td>
<td><p><span data-ttu-id="d9198-214">HTTP</span><span class="sxs-lookup"><span data-stu-id="d9198-214">HTTP</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d9198-215">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d9198-215">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

