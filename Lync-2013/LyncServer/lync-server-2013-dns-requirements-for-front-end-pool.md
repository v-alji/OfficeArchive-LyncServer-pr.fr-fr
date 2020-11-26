---
title: 'Lync Server 2013 : Enregistrements DNS requis pour le pool frontal'
description: 'Lync Server 2013 : configuration requise pour le service DNS pour le pool frontal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pool
ms:assetid: 02d2aa6b-9e01-437b-a2df-00590280150d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398082(v=OCS.15)
ms:contentKeyID: 48183249
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bfce90eccb8c8dff94d4122c96c4ca68ea9150f1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437825"
---
# <a name="dns-requirements-for-front-end-pool-in-lync-server-2013"></a><span data-ttu-id="55ebb-103">Enregistrements DNS requis pour le pool frontal dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="55ebb-103">DNS requirements for Front End pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="55ebb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="55ebb-104">

<span> </span></span></span>

<span data-ttu-id="55ebb-105">_**Dernière modification de la rubrique :** 2012-11-07_</span><span class="sxs-lookup"><span data-stu-id="55ebb-105">_**Topic Last Modified:** 2012-11-07_</span></span>

<span data-ttu-id="55ebb-106">Pour effectuer cette procédure, vous devez être connecté au serveur ou au domaine au minimum en tant que membre du groupe administrateurs de domaine ou membre du groupe DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="55ebb-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="55ebb-107">Vous devez configurer les enregistrements DNS (Domain Name System) requis avant de publier votre topologie dans le générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="55ebb-107">You need to configure the required Domain Name System (DNS) records prior to publishing your topology in Topology Builder.</span></span> <span data-ttu-id="55ebb-108">De plus, certains noms de domaine complets (FQDN) utilisés dans la configuration d’un déploiement de Lync Server 2013 sont logiques et non des noms de domaine complets de serveur physique ; c’est pourquoi une configuration DNS supplémentaire est requise avant la publication.</span><span class="sxs-lookup"><span data-stu-id="55ebb-108">Additionally, some of the fully qualified domain names (FQDNs) used in the configuration of a Lync Server 2013 deployment are logical and not physical server FQDNs, so additional DNS configuration is required prior to publishing.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="55ebb-109">Lync Server 2013 ne prend pas en charge les domaines à mention unique.</span><span class="sxs-lookup"><span data-stu-id="55ebb-109">Lync Server 2013 does not support single-labeled domains.</span></span> <span data-ttu-id="55ebb-110">Par exemple, une forêt avec un domaine racine appelé <STRONG>contoso. local</STRONG> est prise en charge, mais un domaine racine nommé <STRONG>local</STRONG> n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="55ebb-110">For example, a forest with a root domain named <STRONG>contoso.local</STRONG> is supported, but a root domain named <STRONG>local</STRONG> is not supported.</span></span> <span data-ttu-id="55ebb-111">Pour plus d’informations, reportez-vous à l’article 300684 de la base de connaissances Microsoft, intitulé « informations sur la configuration de Windows pour les domaines avec les noms DNS en une seule étiquette », <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=300684"> https://go.microsoft.com/fwlink/p/?linkid=3052&amp kbid = 300684</A>.</span><span class="sxs-lookup"><span data-stu-id="55ebb-111">For details, see Microsoft Knowledge Base article 300684, “Information about configuring Windows for domains with single-label DNS names,” at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=300684">https://go.microsoft.com/fwlink/p/?linkid=3052&amp;kbid=300684</A>.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="55ebb-112">Le nom spécifié doit être identique au nom de l’ordinateur configuré sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="55ebb-112">The name you specify must be identical to the computer name configured on the server.</span></span> <span data-ttu-id="55ebb-113">Par défaut, le nom de l’ordinateur d’un ordinateur qui n’est pas joint à un domaine est un nom court qui n’est pas un nom de domaine complet.</span><span class="sxs-lookup"><span data-stu-id="55ebb-113">By default the computer name of a computer that is not joined to a domain is a short name, not an FQDN.</span></span> <span data-ttu-id="55ebb-114">Le générateur de topologie utilise des noms de domaine complets plutôt que des noms courts.</span><span class="sxs-lookup"><span data-stu-id="55ebb-114">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="55ebb-115"><STRONG>Utilisez uniquement les caractères standard</STRONG> (y compris A – z, a-z, 0 à 9 et les traits d’Union) lors de l’affectation des noms de domaine complets des serveurs exécutant Lync Server, des serveurs Edge et des pools.</span><span class="sxs-lookup"><span data-stu-id="55ebb-115"><STRONG>Use only standard characters</STRONG> (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your servers running Lync Server, Edge Servers, and pools.</span></span> <span data-ttu-id="55ebb-116">N’utilisez ni caractère Unicode ni trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="55ebb-116">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="55ebb-117">Les caractères non standard dans un nom de domaine complet ne sont généralement pas pris en charge par les autorités de certification DNS et publiques externes (lorsque le nom de domaine complet doit être attribué à l’SN dans le certificat).</span><span class="sxs-lookup"><span data-stu-id="55ebb-117">Nonstandard characters in an FQDN are often not supported by external DNS and public certification authorities (CAs) (when the FQDN must be assigned to the SN in the certificate).</span></span>



</div>

<span data-ttu-id="55ebb-118">Avant d’activer la topologie après le déploiement de celle-ci, vérifiez que les enregistrements DNS et Active Directory suivants sont créés (à mesure que vous avez besoin de fonctionnalités spécifiques dictées) :</span><span class="sxs-lookup"><span data-stu-id="55ebb-118">Prior to operating the topology after it has been deployed, ensure that the following Active Directory and DNS records are created (as your needs for specific features dictate):</span></span>

  - <span data-ttu-id="55ebb-119">Chaque rôle de serveur existant dans la topologie est publié en tant qu’objet Active Directory (si vous rejoignez l’ordinateur au domaine).</span><span class="sxs-lookup"><span data-stu-id="55ebb-119">Each server role that will exist in the topology is published as an Active Directory object (joining the computer to the domain will accomplish this).</span></span>

  - <span data-ttu-id="55ebb-120">Un enregistrement DNS A existe pour chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="55ebb-120">A DNS A Record exists for each server.</span></span>

  - <span data-ttu-id="55ebb-121">Un enregistrement SRV DNS existe pour chaque domaine SIP si vous envisagez d’utiliser l’ouverture de session automatique pour les clients sous la forme d’une \_ sipinternaltls \_ TCP. \<SIP domain\></span><span class="sxs-lookup"><span data-stu-id="55ebb-121">A DNS SRV Record exists for each SIP domain if you plan to use automatic logon for clients in the form of \_sipinternaltls\_tcp.\<SIP domain\>.</span></span> <span data-ttu-id="55ebb-122">Si vous allez utiliser la configuration manuelle pour les clients, cet enregistrement n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="55ebb-122">If you will use manual configuration for clients, this record is not necessary.</span></span>

  - <span data-ttu-id="55ebb-123">Un enregistrement DNS A pour chaque URL simple configurée qui comporte généralement quatre éléments : réunion, Dial, LWA et Scheduler.</span><span class="sxs-lookup"><span data-stu-id="55ebb-123">A DNS A Record for each configured simple URL, of which there are typically four: meet, dialin, lwa, and scheduler.</span></span> <span data-ttu-id="55ebb-124">De plus, il existe une URL simple d’administration, qui est une URL spéciale pour l’accès au panneau de configuration de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="55ebb-124">Additionally, there is the admin simple URL which is a special URL for access to the Lync Server 2013 Control Panel.</span></span>

  - <span data-ttu-id="55ebb-125">Le serveur exécutant SQL Server doit être joint au domaine et joignable par l’ordinateur à partir duquel le générateur de topologie publie.</span><span class="sxs-lookup"><span data-stu-id="55ebb-125">The server running SQL Server must be joined to the domain, and reachable by the computer that Topology Builder is publishing from.</span></span>

<span data-ttu-id="55ebb-126">Le tableau suit les architectures de référence présentées dans la section Planning.</span><span class="sxs-lookup"><span data-stu-id="55ebb-126">The table follows the reference architectures presented in the Planning section.</span></span> <span data-ttu-id="55ebb-127">Pour plus d’informations, reportez-vous à la rubrique [scénarios d’accès des utilisateurs externes dans Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="55ebb-127">For details, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) in the Planning documentation.</span></span>

<div id="sectionSection0" class="section">

### <a name="dns-records-required-for-the-front-end-pool"></a><span data-ttu-id="55ebb-128">Enregistrements DNS requis pour le pool frontal</span><span class="sxs-lookup"><span data-stu-id="55ebb-128">DNS Records Required for the Front End pool</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55ebb-129">Emplacement</span><span class="sxs-lookup"><span data-stu-id="55ebb-129">Location</span></span></th>
<th><span data-ttu-id="55ebb-130">Type</span><span class="sxs-lookup"><span data-stu-id="55ebb-130">Type</span></span></th>
<th><span data-ttu-id="55ebb-131">FQDN</span><span class="sxs-lookup"><span data-stu-id="55ebb-131">FQDN</span></span></th>
<th><span data-ttu-id="55ebb-132">Cartes sur/Commentaires</span><span class="sxs-lookup"><span data-stu-id="55ebb-132">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55ebb-133">DNS interne</span><span class="sxs-lookup"><span data-stu-id="55ebb-133">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="55ebb-134">A</span><span class="sxs-lookup"><span data-stu-id="55ebb-134">A</span></span></p></td>
<td><p><span data-ttu-id="55ebb-135">pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="55ebb-135">pool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="55ebb-136">Pool01 (équilibrage de charge DNS).</span><span class="sxs-lookup"><span data-stu-id="55ebb-136">Pool01 (DNS load balancing).</span></span> <span data-ttu-id="55ebb-137">Il est nécessaire de disposer d’un enregistrement DNS A pour l’adresse IP de chaque serveur frontal au sein du pool et de mapper le nom de domaine complet du pool.</span><span class="sxs-lookup"><span data-stu-id="55ebb-137">Requires a DNS A record for the IP address of each Front End Server within the pool, mapping to the pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55ebb-138">DNS interne</span><span class="sxs-lookup"><span data-stu-id="55ebb-138">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="55ebb-139">A</span><span class="sxs-lookup"><span data-stu-id="55ebb-139">A</span></span></p></td>
<td><p><span data-ttu-id="55ebb-140">pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="55ebb-140">pool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="55ebb-141">Pool01 (adresse IP virtuelle de l’équilibrage de charge matérielle).</span><span class="sxs-lookup"><span data-stu-id="55ebb-141">Pool01 (virtual IP (VIP) of hardware load balancer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55ebb-142">DNS interne</span><span class="sxs-lookup"><span data-stu-id="55ebb-142">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="55ebb-143">A</span><span class="sxs-lookup"><span data-stu-id="55ebb-143">A</span></span></p></td>
<td><p><span data-ttu-id="55ebb-144">fe01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="55ebb-144">fe01.contoso.net</span></span></p>
<p><span data-ttu-id="55ebb-145">fe02.contoso.net</span><span class="sxs-lookup"><span data-stu-id="55ebb-145">fe02.contoso.net</span></span></p>
<p><span data-ttu-id="55ebb-146">fe03.contoso.net</span><span class="sxs-lookup"><span data-stu-id="55ebb-146">fe03.contoso.net</span></span></p>
<p><span data-ttu-id="55ebb-147">…</span><span class="sxs-lookup"><span data-stu-id="55ebb-147">…</span></span></p></td>
<td><p><span data-ttu-id="55ebb-148">Serveur frontal Pool01 (nœud 1).</span><span class="sxs-lookup"><span data-stu-id="55ebb-148">Pool01 Front End Server (NODE 1).</span></span></p>
<p><span data-ttu-id="55ebb-149">Serveur frontal Pool01 (nœud 2).</span><span class="sxs-lookup"><span data-stu-id="55ebb-149">Pool01 Front End Server (NODE 2).</span></span></p>
<p><span data-ttu-id="55ebb-150">Serveur frontal Pool01 (nœud 3).</span><span class="sxs-lookup"><span data-stu-id="55ebb-150">Pool01 Front End Server (NODE 3).</span></span></p>
<p><span data-ttu-id="55ebb-151">…</span><span class="sxs-lookup"><span data-stu-id="55ebb-151">…</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55ebb-152">DNS interne</span><span class="sxs-lookup"><span data-stu-id="55ebb-152">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="55ebb-153">A</span><span class="sxs-lookup"><span data-stu-id="55ebb-153">A</span></span></p></td>
<td><p><span data-ttu-id="55ebb-154">fe02.contoso.net</span><span class="sxs-lookup"><span data-stu-id="55ebb-154">fe02.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="55ebb-155">Serveur frontal Pool01 (nœud 2).</span><span class="sxs-lookup"><span data-stu-id="55ebb-155">Pool01 Front End Server (NODE 2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55ebb-156">DNS interne</span><span class="sxs-lookup"><span data-stu-id="55ebb-156">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="55ebb-157">A</span><span class="sxs-lookup"><span data-stu-id="55ebb-157">A</span></span></p></td>
<td><p><span data-ttu-id="55ebb-158">lsweb.contoso.net</span><span class="sxs-lookup"><span data-stu-id="55ebb-158">lsweb.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="55ebb-159">Pool01 (VIP) pour le trafic Web de client à serveur.</span><span class="sxs-lookup"><span data-stu-id="55ebb-159">Pool01 (VIP) for client-to-server web traffic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55ebb-160">DNS interne</span><span class="sxs-lookup"><span data-stu-id="55ebb-160">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="55ebb-161">A</span><span class="sxs-lookup"><span data-stu-id="55ebb-161">A</span></span></p></td>
<td><p><span data-ttu-id="55ebb-162">sqlbe.contoso.net</span><span class="sxs-lookup"><span data-stu-id="55ebb-162">sqlbe.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="55ebb-163">Serveur principal Pool01 exécutant SQL Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="55ebb-163">Pool01 Back End Server running SQL Server 2008 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55ebb-164">DNS interne</span><span class="sxs-lookup"><span data-stu-id="55ebb-164">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="55ebb-165">A</span><span class="sxs-lookup"><span data-stu-id="55ebb-165">A</span></span></p></td>
<td><p><span data-ttu-id="55ebb-166">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="55ebb-166">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="55ebb-167">Requis pour Lync Phone Edition ou l’ouverture de session automatique de clients sans enregistrements DNS SRV, et pour une concordance de domaine stricte.</span><span class="sxs-lookup"><span data-stu-id="55ebb-167">Required for Lync Phone Edition, or automatic logon of clients without DNS SRV records, and for strict domain matching.</span></span> <span data-ttu-id="55ebb-168">Ce n’est pas obligatoire dans tous les cas.</span><span class="sxs-lookup"><span data-stu-id="55ebb-168">Not required in all cases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55ebb-169">DNS interne</span><span class="sxs-lookup"><span data-stu-id="55ebb-169">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="55ebb-170">A</span><span class="sxs-lookup"><span data-stu-id="55ebb-170">A</span></span></p></td>
<td><p><span data-ttu-id="55ebb-171">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="55ebb-171">sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="55ebb-172">Suppose un deuxième domaine SIP.</span><span class="sxs-lookup"><span data-stu-id="55ebb-172">Assumes a second SIP domain.</span></span> <span data-ttu-id="55ebb-173">Requis pour Lync Phone Edition, l’ouverture de session automatique de clients sans enregistrements DNS SRV et pour une concordance de domaine stricte.</span><span class="sxs-lookup"><span data-stu-id="55ebb-173">Required for Lync Phone Edition, automatic logon of clients without DNS SRV records, and for strict domain matching.</span></span> <span data-ttu-id="55ebb-174">Ce n’est pas obligatoire dans tous les cas.</span><span class="sxs-lookup"><span data-stu-id="55ebb-174">Not required in all cases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55ebb-175">DNS interne</span><span class="sxs-lookup"><span data-stu-id="55ebb-175">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="55ebb-176">A</span><span class="sxs-lookup"><span data-stu-id="55ebb-176">A</span></span></p></td>
<td><p><span data-ttu-id="55ebb-177">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="55ebb-177">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="55ebb-178">URL simple pour les conférences rendez-vous publiées en interne-serveur frontal (ou directeur, le cas échéant) répond aux requêtes d’URL simples.</span><span class="sxs-lookup"><span data-stu-id="55ebb-178">Simple URL for dial-in conferencing published internally – Front End Server (or Director, if installed) responds to simple URL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55ebb-179">DNS interne</span><span class="sxs-lookup"><span data-stu-id="55ebb-179">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="55ebb-180">A</span><span class="sxs-lookup"><span data-stu-id="55ebb-180">A</span></span></p></td>
<td><p><span data-ttu-id="55ebb-181">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="55ebb-181">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="55ebb-182">URL simple pour les conférences publiées en interne-serveur frontal (ou réalisateur, le cas échéant) répond aux requêtes d’URL simples.</span><span class="sxs-lookup"><span data-stu-id="55ebb-182">Simple URL for conferences published internally – Front End Server (or Director, if installed) responds to simple URL queries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55ebb-183">DNS interne</span><span class="sxs-lookup"><span data-stu-id="55ebb-183">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="55ebb-184">A</span><span class="sxs-lookup"><span data-stu-id="55ebb-184">A</span></span></p></td>
<td><p><span data-ttu-id="55ebb-185">admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="55ebb-185">admin.contoso.com</span></span></p>
<p><span data-ttu-id="55ebb-186">administrateur</span><span class="sxs-lookup"><span data-stu-id="55ebb-186">admin</span></span></p></td>
<td><p><span data-ttu-id="55ebb-187">Enregistrement facultatif, URL simple pour le panneau de configuration de Lync Server 2013 publié en interne (ou Director, s’il est installé) répond aux requêtes d’URL simples.</span><span class="sxs-lookup"><span data-stu-id="55ebb-187">Optional record, simple URL for Lync Server 2013 Control Panel published internally - Front End Server (or Director, if installed) responds to simple URL queries.</span></span> <span data-ttu-id="55ebb-188">Nom d’hôte uniquement (il n’y a pas de nom de domaine) recommandé.</span><span class="sxs-lookup"><span data-stu-id="55ebb-188">Host name only (no domain name) is recommended.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="55ebb-189">VIP = adresse IP virtuelle pour le système d’équilibrage de la charge matérielle</span><span class="sxs-lookup"><span data-stu-id="55ebb-189">VIP = Virtual IP address for hardware load balancer</span></span>



</div>

</div>

<div>

## <a name="dns-srv-records-for-the-front-end-pool"></a><span data-ttu-id="55ebb-190">Enregistrements SRV DNS pour le pool frontal</span><span class="sxs-lookup"><span data-stu-id="55ebb-190">DNS SRV Records for the Front End pool</span></span>


<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55ebb-191">Emplacement</span><span class="sxs-lookup"><span data-stu-id="55ebb-191">Location</span></span></th>
<th><span data-ttu-id="55ebb-192">Type</span><span class="sxs-lookup"><span data-stu-id="55ebb-192">Type</span></span></th>
<th><span data-ttu-id="55ebb-193">FQDN</span><span class="sxs-lookup"><span data-stu-id="55ebb-193">FQDN</span></span></th>
<th><span data-ttu-id="55ebb-194">Nom de domaine complet cible</span><span class="sxs-lookup"><span data-stu-id="55ebb-194">Target FQDN</span></span></th>
<th><span data-ttu-id="55ebb-195">Port</span><span class="sxs-lookup"><span data-stu-id="55ebb-195">Port</span></span></th>
<th><span data-ttu-id="55ebb-196">Cartes sur/Commentaires</span><span class="sxs-lookup"><span data-stu-id="55ebb-196">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55ebb-197">DNS interne</span><span class="sxs-lookup"><span data-stu-id="55ebb-197">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="55ebb-198">SRV</span><span class="sxs-lookup"><span data-stu-id="55ebb-198">SRV</span></span></p></td>
<td><p><span data-ttu-id="55ebb-199">_sipinternaltls _sipinternaltls._tcp. contoso. com</span><span class="sxs-lookup"><span data-stu-id="55ebb-199">_sipinternaltls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="55ebb-200">pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="55ebb-200">pool01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="55ebb-201">5061</span><span class="sxs-lookup"><span data-stu-id="55ebb-201">5061</span></span></p></td>
<td><p><span data-ttu-id="55ebb-202">Requis pour la configuration automatique des clients 2013 Lync pour fonctionner en interne.</span><span class="sxs-lookup"><span data-stu-id="55ebb-202">Required for automatic configuration of Lync 2013 clients to work internally.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55ebb-203">DNS interne</span><span class="sxs-lookup"><span data-stu-id="55ebb-203">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="55ebb-204">SRV</span><span class="sxs-lookup"><span data-stu-id="55ebb-204">SRV</span></span></p></td>
<td><p><span data-ttu-id="55ebb-205">_sipinternaltls _sipinternaltls._tcp. fabrikam. com</span><span class="sxs-lookup"><span data-stu-id="55ebb-205">_sipinternaltls._tcp.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="55ebb-206">pool01.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="55ebb-206">pool01.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="55ebb-207">5061</span><span class="sxs-lookup"><span data-stu-id="55ebb-207">5061</span></span></p></td>
<td><p><span data-ttu-id="55ebb-208">Requis pour la configuration automatique des clients 2013 Lync pour fonctionner en interne.</span><span class="sxs-lookup"><span data-stu-id="55ebb-208">Required for automatic configuration of Lync 2013 clients to work internally.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55ebb-209">DNS interne</span><span class="sxs-lookup"><span data-stu-id="55ebb-209">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="55ebb-210">SRV</span><span class="sxs-lookup"><span data-stu-id="55ebb-210">SRV</span></span></p></td>
<td><p><span data-ttu-id="55ebb-211">_ntp._udp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="55ebb-211">_ntp._udp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="55ebb-212">dc01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="55ebb-212">dc01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="55ebb-213">123</span><span class="sxs-lookup"><span data-stu-id="55ebb-213">123</span></span></p></td>
<td><p><span data-ttu-id="55ebb-214">Source d’horloge réseau (NTP) requise pour les appareils exécutant Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="55ebb-214">Network Time Protocol (NTP) source required for devices running Lync Phone Edition.</span></span> <span data-ttu-id="55ebb-215">En interne, cela doit pointer sur le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="55ebb-215">Internally, this should point to the domain controller.</span></span> <span data-ttu-id="55ebb-216">Si le contrôleur de domaine n’est pas défini, il essaiera d’utiliser le serveur NTP time.windows.com.</span><span class="sxs-lookup"><span data-stu-id="55ebb-216">If the domain controller is not defined, it will try to use the NTP server time.windows.com.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="55ebb-217">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="55ebb-217">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

