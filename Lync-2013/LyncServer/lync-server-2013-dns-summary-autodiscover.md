---
title: 'Serveur Lync Server 2013 : Résumé DNS-découverte automatique'
description: 'Serveur Lync Server 2013 : Résumé DNS-découverte automatique.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Autodiscover
ms:assetid: b336a2ae-0e58-4b74-b606-aedbbd411587
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945644(v=OCS.15)
ms:contentKeyID: 51541504
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eef9bd6a2489561145718c7bbf2f710ab0b1f248
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429041"
---
# <a name="dns-summary---autodiscover-in-lync-server-2013"></a><span data-ttu-id="76bf2-103">DNS Summary-découverte automatique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="76bf2-103">DNS summary - Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="76bf2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="76bf2-104">

<span> </span></span></span>

<span data-ttu-id="76bf2-105">_**Dernière modification de la rubrique :** 2013-02-13_</span><span class="sxs-lookup"><span data-stu-id="76bf2-105">_**Topic Last Modified:** 2013-02-13_</span></span>

<span data-ttu-id="76bf2-106">La découverte automatique est un service flexible qui accepte les communications via HTTP ou HTTPs.</span><span class="sxs-lookup"><span data-stu-id="76bf2-106">Autodiscover is a flexible service in that it will accept communication over HTTP or HTTPS.</span></span> <span data-ttu-id="76bf2-107">Pour ce faire, le système de noms de domaine (DNS) et les certificats utilisés par les serveurs qui hébergent le service de découverte automatique doivent être correctement configurés.</span><span class="sxs-lookup"><span data-stu-id="76bf2-107">To accomplish this, the domain name system (DNS) and the certificates used by servers that host the Autodiscover service must be configured correctly.</span></span> <span data-ttu-id="76bf2-108">Les exigences en matière de certificats sont décrites dans [synthèse des certificats-découverte automatique dans Lync Server 2013](lync-server-2013-certificate-summary-autodiscover.md).</span><span class="sxs-lookup"><span data-stu-id="76bf2-108">Certificate requirements are covered in [Certificate summary - Autodiscover in Lync Server 2013](lync-server-2013-certificate-summary-autodiscover.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="76bf2-109">La logique de recherche DNS pour les clients du serveur Lync utilise un ordre de résolution spécifique.</span><span class="sxs-lookup"><span data-stu-id="76bf2-109">DNS lookup logic for the Lync Server clients uses a specific order of resolution.</span></span> <span data-ttu-id="76bf2-110">Vous devez toujours inclure le lyncdiscoverinternal. &lt; Domain &gt; et lyncdiscover. &lt; Domain &gt; de votre DNS.</span><span class="sxs-lookup"><span data-stu-id="76bf2-110">You should always include both the lyncdiscoverinternal.&lt;domain&gt; and the lyncdiscover.&lt;domain&gt; in your DNS.</span></span> <span data-ttu-id="76bf2-111">À l’exception du lyncdiscoverinternal. &lt; &gt; l’enregistrement du domaine entraîne l’échec de la connexion des clients internes aux services prévus ou la réception d’une réponse de découverte automatique incorrecte.</span><span class="sxs-lookup"><span data-stu-id="76bf2-111">Excluding the lyncdiscoverinternal.&lt;domain&gt; record will cause internal clients to fail to connect to the intended services or receive the incorrect Autodiscover response.</span></span>



</div>

### <a name="internal-dns-records"></a><span data-ttu-id="76bf2-112">Enregistrements DNS internes</span><span class="sxs-lookup"><span data-stu-id="76bf2-112">Internal DNS Records</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="76bf2-113">Type d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="76bf2-113">Record type</span></span></th>
<th><span data-ttu-id="76bf2-114">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="76bf2-114">Host name</span></span></th>
<th><span data-ttu-id="76bf2-115">Résolu en</span><span class="sxs-lookup"><span data-stu-id="76bf2-115">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76bf2-116">CNAME</span><span class="sxs-lookup"><span data-stu-id="76bf2-116">CNAME</span></span></p></td>
<td><p><span data-ttu-id="76bf2-117">Lyncdiscoverinternal. &lt; nom de domaine interne&gt;</span><span class="sxs-lookup"><span data-stu-id="76bf2-117">Lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
<td><p><span data-ttu-id="76bf2-118">Nom de domaine complet (FQDN) des services Web internes de votre pool de Director, si vous en avez un ou pour votre pool frontal si vous n’avez pas de directeur.</span><span class="sxs-lookup"><span data-stu-id="76bf2-118">Internal Web Services FQDN for your Director pool, if you have one, or for your Front End pool if you do not have a Director.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76bf2-119">A (hôte, si IPv6, AAAA)</span><span class="sxs-lookup"><span data-stu-id="76bf2-119">A (host, if IPv6, AAAA)</span></span></p></td>
<td><p><span data-ttu-id="76bf2-120">lyncdiscoverinternal. &lt; nom de domaine interne&gt;</span><span class="sxs-lookup"><span data-stu-id="76bf2-120">lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
<td><p><span data-ttu-id="76bf2-121">Adresse IP des services Web internes (adresse IP virtuelle) si vous utilisez un équilibreur de charge, si vous en avez un, ou si vous n’avez pas de réalisateur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="76bf2-121">Internal Web Services IP address (virtual IP (VIP) address if you use a load balancer) of your Director pool, if you have one, or of your Front End pool if you do not have a Director.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="76bf2-122">Vous devez créer un des enregistrements DNS externes suivants :</span><span class="sxs-lookup"><span data-stu-id="76bf2-122">You need to create one of the following external DNS records:</span></span>

### <a name="external-dns-records"></a><span data-ttu-id="76bf2-123">Enregistrements DNS externes</span><span class="sxs-lookup"><span data-stu-id="76bf2-123">External DNS Records</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="76bf2-124">Type d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="76bf2-124">Record type</span></span></th>
<th><span data-ttu-id="76bf2-125">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="76bf2-125">Host name</span></span></th>
<th><span data-ttu-id="76bf2-126">Résolu en</span><span class="sxs-lookup"><span data-stu-id="76bf2-126">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76bf2-127">CNAME</span><span class="sxs-lookup"><span data-stu-id="76bf2-127">CNAME</span></span></p></td>
<td><p><span data-ttu-id="76bf2-128">lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="76bf2-128">lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="76bf2-129">Nom de domaine complet des services Web externes pour votre pool de directeurs, le cas échéant, ou pour votre pool frontal si vous n’avez pas de directeur.</span><span class="sxs-lookup"><span data-stu-id="76bf2-129">External Web Services FQDN for your Director pool, if you have one, or for your Front End pool if you do not have a Director.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76bf2-130">A (hôte, si IPv6, AAAA)</span><span class="sxs-lookup"><span data-stu-id="76bf2-130">A (host, if IPv6, AAAA)</span></span></p></td>
<td><p><span data-ttu-id="76bf2-131">lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="76bf2-131">lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="76bf2-132">Adresse IP externe ou publique du proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="76bf2-132">External or public IP address of the reverse proxy.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="76bf2-133">Le trafic externe traverse le proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="76bf2-133">External traffic goes through the reverse proxy.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="76bf2-134">Les clients d’appareils mobiles ne prennent pas en charge plusieurs certificats SSL (Secure Sockets Layer) provenant de différents domaines.</span><span class="sxs-lookup"><span data-stu-id="76bf2-134">Mobile device clients do not support multiple Secure Sockets Layer (SSL) certificates from different domains.</span></span> <span data-ttu-id="76bf2-135">Par conséquent, la redirection CNAMe vers différents domaines n’est pas prise en charge sur HTTPs.</span><span class="sxs-lookup"><span data-stu-id="76bf2-135">Therefore, CNAME redirection to different domains is not supported over HTTPS.</span></span> <span data-ttu-id="76bf2-136">Par exemple, un enregistrement CNAMe DNS pour lyncdiscover.contoso.com qui redirige vers une adresse de director.contoso.net n’est pas pris en charge sur HTTPs.</span><span class="sxs-lookup"><span data-stu-id="76bf2-136">For example, a DNS CNAME record for lyncdiscover.contoso.com that redirects to an address of director.contoso.net is not supported over HTTPS.</span></span> <span data-ttu-id="76bf2-137">Dans le cas d’une telle topologie, un client d’appareil mobile doit utiliser HTTP pour la première demande, de sorte que la redirection CNAMe soit résolue via HTTP.</span><span class="sxs-lookup"><span data-stu-id="76bf2-137">In such a topology, a mobile device client needs to use HTTP for the first request, so that the CNAME redirection is resolved over HTTP.</span></span> <span data-ttu-id="76bf2-138">Les requêtes suivantes utilisent alors HTTPs.</span><span class="sxs-lookup"><span data-stu-id="76bf2-138">Subsequent requests then use HTTPS.</span></span> <span data-ttu-id="76bf2-139">Pour prendre en charge ce scénario, vous devez configurer votre proxy inverse avec une règle de publication Web pour le port 80 (HTTP).</span><span class="sxs-lookup"><span data-stu-id="76bf2-139">To support this scenario, you need to configure your reverse proxy with a web publishing rule for port 80 (HTTP).</span></span> <span data-ttu-id="76bf2-140">Pour plus d’informations, reportez-vous à la section « pour créer une règle de publication Web pour le port 80 » dans <A href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">configuration du proxy inverse pour la mobilité dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="76bf2-140">For details, see "To create a web publishing rule for port 80" in <A href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Configuring the reverse proxy for mobility in Lync Server 2013</A>.</span></span> <span data-ttu-id="76bf2-141">La redirection CNAMe vers le même domaine est prise en charge sur HTTPs.</span><span class="sxs-lookup"><span data-stu-id="76bf2-141">CNAME redirection to the same domain is supported over HTTPS.</span></span> <span data-ttu-id="76bf2-142">Dans ce cas, le certificat du domaine de destination couvre le domaine d’origine.</span><span class="sxs-lookup"><span data-stu-id="76bf2-142">In this case, the destination domain's certificate covers the originating domain.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="76bf2-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76bf2-143">See Also</span></span>


[<span data-ttu-id="76bf2-144">Configuration du proxy inverse pour la mobilité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="76bf2-144">Configuring the reverse proxy for mobility in Lync Server 2013</span></span>](lync-server-2013-configuring-the-reverse-proxy-for-mobility.md)  


[<span data-ttu-id="76bf2-145">Résumé du certificat-découverte automatique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="76bf2-145">Certificate summary - Autodiscover in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-autodiscover.md)  
  

<span data-ttu-id="76bf2-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="76bf2-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

