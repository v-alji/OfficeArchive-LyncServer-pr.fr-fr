---
title: 'Lync Server 2013 : conditions DNS requises pour les pools frontaux'
description: 'Lync Server 2013 : conditions DNS requises pour les pools frontaux.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pools
ms:assetid: ba28919c-fbbe-4c54-8bf9-2b0cd3fa39c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412910(v=OCS.15)
ms:contentKeyID: 48185228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c0369e82bd8ed2ea63e2156728b41f9942b0148
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429069"
---
# <a name="dns-requirements-for-front-end-pools-in-lync-server-2013"></a><span data-ttu-id="25961-103">Conditions DNS requises pour les pools frontaux dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25961-103">DNS requirements for Front End pools in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="25961-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="25961-104">

<span> </span></span></span>

<span data-ttu-id="25961-105">_**Rubrique dernière modification :** 11/11/2012_</span><span class="sxs-lookup"><span data-stu-id="25961-105">_**Topic Last Modified:** 2012-11-07_</span></span>

<span data-ttu-id="25961-106">Cette section décrit les enregistrements DNS (Domain Name System) requis pour le déploiement de pools frontaux.</span><span class="sxs-lookup"><span data-stu-id="25961-106">This section describes the Domain Name System (DNS) records that are required for deployment of Front End pools.</span></span>

<div>

## <a name="dns-records-for-front-end-pools"></a><span data-ttu-id="25961-107">Enregistrements DNS pour les pools frontaux</span><span class="sxs-lookup"><span data-stu-id="25961-107">DNS Records for Front End Pools</span></span>

<span data-ttu-id="25961-108">Le tableau suivant spécifie les exigences DNS requises pour un déploiement de pool frontal Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="25961-108">The following table specifies DNS requirements for a Lync Server 2013 Front End pool deployment.</span></span>

### <a name="dns-requirements-for-a-front-end-pool"></a><span data-ttu-id="25961-109">Conditions DNS requises pour un pool frontal</span><span class="sxs-lookup"><span data-stu-id="25961-109">DNS Requirements for a Front End Pool</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="25961-110">Scénario de déploiement</span><span class="sxs-lookup"><span data-stu-id="25961-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="25961-111">Enregistrement DNS requis</span><span class="sxs-lookup"><span data-stu-id="25961-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25961-112">Groupe frontal avec plusieurs serveurs frontaux et équilibrage de la charge matérielle (que l’équilibrage de charge DNS soit également déployé sur ce pool)</span><span class="sxs-lookup"><span data-stu-id="25961-112">Front End pool with multiple Front End Servers and a hardware load balancer (whether or not DNS load balancing is also deployed on that pool)</span></span></p></td>
<td><p><span data-ttu-id="25961-113">Lors de l’utilisation de l’équilibrage de charge DNS et d’un équilibrage de charge matérielle, vous devez utiliser les enregistrements Hôte (A).</span><span class="sxs-lookup"><span data-stu-id="25961-113">When using both DNS load balancing and a hardware load balancer, you need to Host (A) records.</span></span> <span data-ttu-id="25961-114">Créez un enregistrement A interne qui résout le nom de domaine complet (FQDN) du pool frontal pour l’équilibrage de charge du DNS.</span><span class="sxs-lookup"><span data-stu-id="25961-114">Create an internal A record that resolves the fully qualified domain name (FQDN) of the Front End pool for DNS load balancing.</span></span> <span data-ttu-id="25961-115">Créez un enregistrement hôte interne (A) pour les services web internes à l’adresse IP virtuelle (VIP) de l’équilibreur de charge.</span><span class="sxs-lookup"><span data-stu-id="25961-115">Create an internal host (A) record for the internal Web services to the virtual IP (VIP) address of the load balancer.</span></span> <span data-ttu-id="25961-116">Vous devez utiliser le nom des services web internes, tel que défini dans le Générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="25961-116">You must use the internal Web services name as defined in Topology Builder.</span></span></p>
<p><span data-ttu-id="25961-117">Par exemple, si vous utilisez à la fois l’équilibrage de charge DNS et l’équilibrage de charge matérielle, vous avez un enregistrement A pour chaque serveur frontal dans un pool pour l’équilibrage de charge DNS, et un enregistrement A pour les services Web internes pointant vers l’adresse IP virtuelle du balanceur de charge matérielle :</span><span class="sxs-lookup"><span data-stu-id="25961-117">For example, if you use both DNS load balancing and hardware load balancing, you would have an A record for each Front End Server in a pool for DNS load balancing, and an A record for the internal Web services pointing to the virtual IP of the hardware load balancer:</span></span></p>
<ul>
<li><p><span data-ttu-id="25961-118">Équilibrage de charge DNS : Pool01.contoso.net IP du pool 10.10.10.5</span><span class="sxs-lookup"><span data-stu-id="25961-118">DNS load balancing:   Pool01.contoso.net   IP Address of pool   10.10.10.5</span></span></p>
<div>

> [!WARNING]  
> <span data-ttu-id="25961-119">Chaque serveur frontal aura également un enregistrement A distinct :</span><span class="sxs-lookup"><span data-stu-id="25961-119">Each Front End Server will also have a distinct A record:</span></span>


</div>
<ol>
<li><p><span data-ttu-id="25961-120">FE01.contoso.net 10.10.10.1</span><span class="sxs-lookup"><span data-stu-id="25961-120">FE01.contoso.net    10.10.10.1</span></span></p></li>
<li><p><span data-ttu-id="25961-121">FE02.contoso.net 10.10.10.2</span><span class="sxs-lookup"><span data-stu-id="25961-121">FE02.contoso.net    10.10.10.2</span></span></p></li>
<li><p><span data-ttu-id="25961-122">FE03.contoso.net 10.10.10.3</span><span class="sxs-lookup"><span data-stu-id="25961-122">FE03.contoso.net    10.10.10.3</span></span></p></li>
<li><p><span data-ttu-id="25961-123">FE04.contoso.net 10.10.10.4</span><span class="sxs-lookup"><span data-stu-id="25961-123">FE04.contoso.net    10.10.10.4</span></span></p></li>
</ol></li>
<li><p><span data-ttu-id="25961-124">Équilibrage de charge matérielle : WebInternal.contoso.net IP de vip HLB 192.168.10.5</span><span class="sxs-lookup"><span data-stu-id="25961-124">Hardware load balancing:   WebInternal.contoso.net   IP Address of HLB VIP   192.168.10.5</span></span></p></li>
</ul>
<p><span data-ttu-id="25961-125">Tout le trafic, à l’exception du trafic HTTP/HTTPS, utilisera Pool01.contoso.net enregistrement.</span><span class="sxs-lookup"><span data-stu-id="25961-125">All traffic except for HTTP/HTTPS traffic will use the Pool01.contoso.net record.</span></span> <span data-ttu-id="25961-126">Le trafic HTTP/HTTPS utilise l’adresse des services web internes définie 192.168.10.5</span><span class="sxs-lookup"><span data-stu-id="25961-126">HTTP/HTTPS traffic will use the defined internal Web services address of 192.168.10.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25961-127">Pool frontal avec équilibrage de charge DNS déployé</span><span class="sxs-lookup"><span data-stu-id="25961-127">Front End pool with DNS load balancing deployed</span></span></p></td>
<td><p><span data-ttu-id="25961-128">Un jeu d’enregistrements A internes qui résolvent le nom de source de données (FQDN) du pool sur l’adresse IP de chaque serveur du pool.</span><span class="sxs-lookup"><span data-stu-id="25961-128">A set of internal A records that resolve the FQDN of the pool to the IP address of each server in the pool.</span></span> <span data-ttu-id="25961-129">Un enregistrement A doit être enregistré pour chaque serveur du pool.</span><span class="sxs-lookup"><span data-stu-id="25961-129">There must one A record for each server in the pool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25961-130">Pool frontal avec équilibrage de charge DNS déployé</span><span class="sxs-lookup"><span data-stu-id="25961-130">Front End pool with DNS load balancing deployed</span></span></p></td>
<td><p><span data-ttu-id="25961-131">Un jeu d’enregistrements A internes qui résolvent le nom de source de données (FQDN) de chaque serveur du pool sur l’adresse IP de ce serveur.</span><span class="sxs-lookup"><span data-stu-id="25961-131">A set of internal A records that resolve the FQDN of each server in the pool to the IP address of that server.</span></span> <span data-ttu-id="25961-132">Pour plus d’informations, consultez la documentation Planification de l’équilibrage de charge <a href="lync-server-2013-dns-load-balancing.md">DNS dans Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="25961-132">For details, see <a href="lync-server-2013-dns-load-balancing.md">DNS load balancing in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25961-133">Pool frontal avec un serveur frontal unique et une base de données principale dédiée, mais sans équilibrage de charge</span><span class="sxs-lookup"><span data-stu-id="25961-133">Front End pool with a single Front End Server and a dedicated back-end database but no load balancer</span></span></p></td>
<td><p><span data-ttu-id="25961-134">Enregistrement A interne qui résout le nom de bord du nom de bord (FQDN) du pool frontal sur l’adresse IP du serveur frontal d’entreprise édition unique.</span><span class="sxs-lookup"><span data-stu-id="25961-134">An internal A record that resolves the FQDN of the Front End pool to the IP address of the single Enterprise Edition Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25961-135">Connectez-vous automatique au client</span><span class="sxs-lookup"><span data-stu-id="25961-135">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="25961-136">Pour chaque domaine SIP pris en charge, un enregistrement SRV pour _sipinternaltls._tcp. &lt; domain &gt; over port 5061 that maps to the FQDN of the Front End pool that authenticates and redirects client requests for sign-in.</span><span class="sxs-lookup"><span data-stu-id="25961-136">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Front End pool that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="25961-137">Pour plus d’informations, consultez la exigences DNS pour la signature automatique du client dans <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="25961-137">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25961-138">Découverte du service web de mise à jour des appareils par les appareils de communications unifiées</span><span class="sxs-lookup"><span data-stu-id="25961-138">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="25961-139">Enregistrement A interne avec le nom ucupdates-r2. &lt; Domaine SIP résolu à l’adresse IP du pool frontal qui héberge le service web De mise à jour &gt; des appareils.</span><span class="sxs-lookup"><span data-stu-id="25961-139">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Front End pool that hosts the Device Update Web service.</span></span> <span data-ttu-id="25961-140">Dans la situation où un appareil de UC est allumé, mais qu’un utilisateur ne s’est jamais connecté à l’appareil, l’enregistrement A permet à l’appareil de découvrir le pool frontal hébergeant le service web De mise à jour des appareils et d’obtenir des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="25961-140">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the Front End pool hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="25961-141">Dans le cas contraire, les appareils obtiennent ces informations même si une provision à bande s’offre à vous la première fois qu’un utilisateur se connecte.</span><span class="sxs-lookup"><span data-stu-id="25961-141">Otherwise, devices obtain this information though in-band provisioning the first time a user logs in.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="25961-142">Si vous avez déjà déployé un service web de mise à jour de l’appareil dans Lync Server 2010, vous avez déjà créé un enregistrement A interne avec le nom « ucupdates ». &lt; Domaine &gt; SIP.</span><span class="sxs-lookup"><span data-stu-id="25961-142">If you have an existing deployment of Device Update Web service in Lync Server 2010, you have already created an internal A record with the name ucupdates.&lt;SIP domain&gt;.</span></span> <span data-ttu-id="25961-143">Pour Microsoft Office Communications Server 2007 R2, vous devez créer un enregistrement DNS A supplémentaire avec le nom ucupdates-r2. &lt; Domaine &gt; SIP.</span><span class="sxs-lookup"><span data-stu-id="25961-143">For Microsoft Office Communications Server 2007 R2, you must create an additional DNS A record with the name ucupdates-r2.&lt;SIP domain&gt;.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25961-144">Proxy inverse pour prendre en charge le trafic HTTP</span><span class="sxs-lookup"><span data-stu-id="25961-144">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="25961-145">Enregistrement A externe qui résout le FQDN de la batterie de serveurs web externe sur l’adresse IP externe du proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="25961-145">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="25961-146">Les clients et appareils de lauc utilisent cet enregistrement pour se connecter au proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="25961-146">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="25961-147">Pour plus d’informations, voir <a href="lync-server-2013-determine-dns-requirements.md">Déterminer les exigences DNS pour Lync Server 2013</a> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="25961-147">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="25961-148">Le tableau suivant montre un exemple des enregistrements DNS requis pour le FQDN de la batterie de serveurs web interne.</span><span class="sxs-lookup"><span data-stu-id="25961-148">The following table shows an example of the DNS records required for the internal web farm FQDN.</span></span>

### <a name="example-dns-records-for-internal-web-farm-fqdn"></a><span data-ttu-id="25961-149">Exemples d’enregistrements DNS pour le FQDN de batterie de serveurs web internes</span><span class="sxs-lookup"><span data-stu-id="25961-149">Example DNS Records for Internal Web Farm FQDN</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="25961-150">FQDN de batterie de serveurs web interne</span><span class="sxs-lookup"><span data-stu-id="25961-150">Internal web farm FQDN</span></span></th>
<th><span data-ttu-id="25961-151">FQDN du pool</span><span class="sxs-lookup"><span data-stu-id="25961-151">Pool FQDN</span></span></th>
<th><span data-ttu-id="25961-152">DNS A record(s)</span><span class="sxs-lookup"><span data-stu-id="25961-152">DNS A record(s)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25961-153">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="25961-153">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="25961-154">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="25961-154">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="25961-155">Enregistrement DNS A pour la ee-pool.contoso.com qui résout l’adresse VIP de l’équilibreur de charge utilisé par les serveurs frontaux.</span><span class="sxs-lookup"><span data-stu-id="25961-155">DNS A record for the ee-pool.contoso.com that resolves to the VIP address of the load balancer used by the Front End Servers.</span></span></p>
<p><span data-ttu-id="25961-156">Enregistrement DNS A pour les webcon.contoso.com résoudre à l’adresse VIP de l’équilibreur de charge utilisé par les serveurs frontaux.</span><span class="sxs-lookup"><span data-stu-id="25961-156">DNS A record for webcon.contoso.com that resolves to the VIP address of the load balancer used by the Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25961-157">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="25961-157">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="25961-158">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="25961-158">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="25961-159">Enregistrement DNS A pour ee-pool.contoso.com qui résout l’adresse IP virtuelle (VIP) de l’équilibreur de charge utilisé par les serveurs frontaux Enterprise Edition du pool frontal.</span><span class="sxs-lookup"><span data-stu-id="25961-159">DNS A record for ee-pool.contoso.com that resolves to the virtual IP (VIP) address of the load balancer used by the Enterprise Edition Front End Servers in the Front End pool.</span></span></p>
<p><span data-ttu-id="25961-160">Notez que si vous utilisez l’équilibrage de charge DNS sur ce pool, votre pool frontal et votre batterie de serveurs web interne ne peuvent pas avoir le même nom de source de données (FQDN).</span><span class="sxs-lookup"><span data-stu-id="25961-160">Note that if you are using DNS load balancing on this pool, your Front End pool and internal web farm cannot have the same FQDN.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="25961-161">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="25961-161">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

