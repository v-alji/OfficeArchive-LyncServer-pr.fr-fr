---
title: 'Lync Server 2013 : Résumé des enregistrements DNS - Serveur Edge consolidé mis à l’échelle, équilibrage de charge DNS avec des adresses IP publiques'
description: 'Serveur Lync Server 2013 : système de synthèse de la mise à l’échelle de l’application DNS'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Scaled consolidated edge, DNS load balancing with public IP addresses
ms:assetid: dc8f096a-a0a4-4f71-8930-88ff8fc089d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205319(v=OCS.15)
ms:contentKeyID: 48185594
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ca88043b76365508ea00ca840e9a9fdcb0e270be
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429013"
---
# <a name="dns-summary---scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="ee77b-103">Résumé des enregistrements DNS - Serveur Edge consolidé mis à l’échelle, équilibrage de charge DNS avec des adresses IP publiques dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee77b-103">DNS summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee77b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee77b-104">

<span> </span></span></span>

<span data-ttu-id="ee77b-105">_**Dernière modification de la rubrique :** 2017-03-09_</span><span class="sxs-lookup"><span data-stu-id="ee77b-105">_**Topic Last Modified:** 2017-03-09_</span></span>

<span data-ttu-id="ee77b-106">Les exigences d’enregistrements DNS pour l’accès distant à Lync Server 2013 sont assez simples comparées à celles des certificats et des ports.</span><span class="sxs-lookup"><span data-stu-id="ee77b-106">DNS record requirements for remote access to Lync Server 2013 are fairly straightforward compared to those for certificates and ports.</span></span> <span data-ttu-id="ee77b-107">De plus, de nombreux enregistrements sont facultatifs, en fonction de la configuration des clients exécutant Lync 2013 et de la possibilité d’activer la Fédération.</span><span class="sxs-lookup"><span data-stu-id="ee77b-107">Also, many records are optional, depending on how you configure clients running Lync 2013 and whether you enable federation.</span></span>

<span data-ttu-id="ee77b-108">Pour plus d’informations sur les exigences DNS de Lync 2013, voir [déterminer les exigences DNS pour Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ee77b-108">For details about Lync 2013 DNS requirements, see [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="ee77b-109">Pour plus d’informations sur la configuration de la configuration automatique de clients 2013 Lync si le DNS avec fractionnement n’est pas configuré, voir la section « Configuration automatique sans le service DNS partagé » dans [déterminer les exigences DNS pour Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ee77b-109">For details about configuring automatic configuration of Lync 2013 clients if split-brain DNS is not configured, see the "Automatic Configuration without Split Brain DNS" section in [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="ee77b-110">Le tableau suivant contient un résumé des enregistrements DNS requis pour la prise en charge de la topologie de périphérie unique consolidée illustrée dans la figure unique.</span><span class="sxs-lookup"><span data-stu-id="ee77b-110">The following table contains a summary of the DNS records that are required to support the single consolidated edge topology shown in the Single Consolidated Edge Topology figure.</span></span> <span data-ttu-id="ee77b-111">Notez que certains enregistrements DNS sont requis uniquement pour la configuration automatique de clients 2013 Lync.</span><span class="sxs-lookup"><span data-stu-id="ee77b-111">Note that certain DNS records are required only for automatic configuration of Lync 2013 clients.</span></span> <span data-ttu-id="ee77b-112">Si vous envisagez d’utiliser des objets de stratégie de groupe pour configurer des clients Lync, les enregistrements associés ne sont pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="ee77b-112">If you plan to use group policy objects (GPOs) to configure Lync clients, the associated records are not necessary.</span></span>

<div>

## <a name="important-edge-server-network-adapter-requirements"></a><span data-ttu-id="ee77b-113">IMPORTANT : configuration requise pour les cartes réseau du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="ee77b-113">IMPORTANT: Edge Server Network Adapter Requirements</span></span>

<span data-ttu-id="ee77b-114">Pour éviter les problèmes de routage, assurez-vous qu’il y a au moins deux cartes réseau dans vos serveurs Edge et que la passerelle par défaut est définie uniquement sur l’adaptateur réseau associé à l’interface externe.</span><span class="sxs-lookup"><span data-stu-id="ee77b-114">To avoid routing issues, verify that there are at least two network adapters in your Edge Servers and that the default gateway is set only on the network adapter associated with the external interface.</span></span> <span data-ttu-id="ee77b-115">Par exemple, comme illustré dans la figure dans le scénario d’arête consolidée ajusté [, l’équilibrage de charge DNS avec des adresses IP publiques dans Lync Server 2013](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md) , la passerelle par défaut pointe vers le pare-feu externe.</span><span class="sxs-lookup"><span data-stu-id="ee77b-115">For example, as shown in the Scaled Consolidated Edge Scenario figure in [Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md) , the default gateway would point to the external firewall.</span></span>

<span data-ttu-id="ee77b-116">Vous pouvez configurer deux cartes réseau sur chacun de votre serveur Edge comme suit :</span><span class="sxs-lookup"><span data-stu-id="ee77b-116">You can configure two network adapters in each of your Edge Server as follows:</span></span>

  - <span data-ttu-id="ee77b-117">**Carte réseau 1-nœud 1 (interface interne)**</span><span class="sxs-lookup"><span data-stu-id="ee77b-117">**Network adapter 1 - Node 1 (Internal Interface)**</span></span>
    
    <span data-ttu-id="ee77b-118">Interface interne avec 172.25.33.10 attribué.</span><span class="sxs-lookup"><span data-stu-id="ee77b-118">Internal interface with 172.25.33.10 assigned.</span></span>
    
    <span data-ttu-id="ee77b-119">Aucune passerelle par défaut n’est définie.</span><span class="sxs-lookup"><span data-stu-id="ee77b-119">No default gateway is defined.</span></span>
    
    <span data-ttu-id="ee77b-120">Assurez-vous qu’il existe un itinéraire du réseau contenant l’interface interne latérale vers tout réseau qui contient des serveurs exécutant Lync Server 2013 ou des clients Lync Server 2013 (par exemple, de 172.25.33.0 à 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="ee77b-120">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="ee77b-121">**Carte réseau 1-nœud 2 (interface interne)**</span><span class="sxs-lookup"><span data-stu-id="ee77b-121">**Network adapter 1 - Node 2 (Internal Interface)**</span></span>
    
    <span data-ttu-id="ee77b-122">Interface interne avec 172.25.33.11 attribué.</span><span class="sxs-lookup"><span data-stu-id="ee77b-122">Internal interface with 172.25.33.11 assigned.</span></span>
    
    <span data-ttu-id="ee77b-123">Aucune passerelle par défaut n’est définie.</span><span class="sxs-lookup"><span data-stu-id="ee77b-123">No default gateway is defined.</span></span>
    
    <span data-ttu-id="ee77b-124">Assurez-vous qu’il existe un itinéraire du réseau contenant l’interface interne latérale vers tout réseau qui contient des serveurs exécutant Lync Server 2013 ou des clients Lync Server 2013 (par exemple, de 172.25.33.0 à 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="ee77b-124">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="ee77b-125">**Carte réseau 2-nœud 1 (interface externe)**</span><span class="sxs-lookup"><span data-stu-id="ee77b-125">**Network adapter 2 Node 1 (External Interface)**</span></span>
    
    <span data-ttu-id="ee77b-126">Trois adresses IP privées sont attribuées à cette carte réseau (par exemple, 131.107.155.10 pour le service Edge d’Access 131.107.155.20 pour le service Edge de conférence Web, 131.107.155.30 pour les services Edge A/V.</span><span class="sxs-lookup"><span data-stu-id="ee77b-126">Three private IP addresses are assigned to this network adapter, for example 131.107.155.10 for Access Edge service, 131.107.155.20 for Web Conferencing Edge service, 131.107.155.30 for A/V Edge service.</span></span>
    
    <span data-ttu-id="ee77b-127">L’adresse IP publique du service Edge d’accès est principale avec passerelle par défaut définie sur le routeur public (131.107.155.1).</span><span class="sxs-lookup"><span data-stu-id="ee77b-127">The Access Edge service public IP address is primary with default gateway set to the public router (131.107.155.1).</span></span>
    
    <span data-ttu-id="ee77b-128">Les adresses IP privées des services Edge et de service de conférence Web sont des adresses IP supplémentaires dans la section **avancé** des propriétés de **protocole IP version 4 (TCP/IPv4)** et **protocole Internet (TCP/IPv6)** des propriétés de connexion de la **zone locale** dans Windows Server.</span><span class="sxs-lookup"><span data-stu-id="ee77b-128">Web Conferencing Edge service and A/V Edge service private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ee77b-129">Il est possible, mais déconseillé, d’utiliser une seule adresse IP pour les trois interfaces de service Edge.</span><span class="sxs-lookup"><span data-stu-id="ee77b-129">It is possible, though not recommended, to use a single IP address for all three Edge service interfaces.</span></span> <span data-ttu-id="ee77b-130">Même si cela enregistre les adresses IP, il est nécessaire de disposer d’un numéro de port différent pour chaque service.</span><span class="sxs-lookup"><span data-stu-id="ee77b-130">Though this does save IP addresses, it requires different port numbers for each service.</span></span> <span data-ttu-id="ee77b-131">Le numéro de port par défaut est 443/TCP, ce qui permet à la plupart des pare-feu distants d’autoriser le trafic.</span><span class="sxs-lookup"><span data-stu-id="ee77b-131">The default port number is 443/TCP, which ensures that most remote firewalls will allow the traffic.</span></span> <span data-ttu-id="ee77b-132">Le fait de remplacer les valeurs de port par (par exemple) 5061/TCP pour le service Edge d’accès, 444/TCP pour le service Edge de conférence Web et 443/TCP pour le service Edge A/V, peut poser des problèmes pour les utilisateurs distants dans lesquels un pare-feu est derrière n’autorise pas le trafic de 5061/TCP et 444/TCP.</span><span class="sxs-lookup"><span data-stu-id="ee77b-132">Changing the port values to (for example) 5061/TCP for the Access Edge service, 444/TCP for the Web Conferencing Edge service and 443/TCP for the A/V Edge service might cause problems for remote users where a firewall that they are behind does not allow the traffic over 5061/TCP and 444/TCP.</span></span> <span data-ttu-id="ee77b-133">Par ailleurs, trois adresses IP distinctes simplifient la résolution des problèmes en raison de la possibilité de filtrer sur l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="ee77b-133">Additionally, three distinct IP addresses makes troubleshooting easier due to being able to filter on IP address.</span></span>

    
    </div>

  - <span data-ttu-id="ee77b-134">**Carte réseau 2-nœud 2 (interface externe)**</span><span class="sxs-lookup"><span data-stu-id="ee77b-134">**Network adapter 2 Node 2 (External Interface)**</span></span>
    
    <span data-ttu-id="ee77b-135">Trois adresses IP privées sont attribuées à cette carte réseau (par exemple, 131.107.155.11 pour le service Edge d’Access 131.107.155.21 pour le service Edge de conférence Web, 131.107.155.31 pour les services Edge A/V.</span><span class="sxs-lookup"><span data-stu-id="ee77b-135">Three private IP addresses are assigned to this network adapter, for example 131.107.155.11 for Access Edge service, 131.107.155.21 for Web Conferencing Edge service, 131.107.155.31 for A/V Edge service.</span></span>
    
    <span data-ttu-id="ee77b-136">L’adresse IP publique du service Edge d’accès est principale avec passerelle par défaut définie sur le routeur public (131.107.155.1).</span><span class="sxs-lookup"><span data-stu-id="ee77b-136">The Access Edge service public IP address is primary with default gateway set to the public router (131.107.155.1).</span></span>
    
    <span data-ttu-id="ee77b-137">Les adresses IP privées des services Edge et de service de conférence Web sont des adresses IP supplémentaires dans la section **avancé** des propriétés de **protocole IP version 4 (TCP/IPv4)** et **protocole Internet (TCP/IPv6)** des propriétés de connexion de la **zone locale** dans Windows Server.</span><span class="sxs-lookup"><span data-stu-id="ee77b-137">Web Conferencing Edge service and A/V Edge service private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="ee77b-138">La configuration du serveur Edge avec deux cartes réseau est l’une des deux options suivantes.</span><span class="sxs-lookup"><span data-stu-id="ee77b-138">Configuring the Edge Server with two network adapters is one of two options.</span></span> <span data-ttu-id="ee77b-139">L’autre option consiste à utiliser une carte réseau pour le côté interne et trois cartes réseau pour le côté externe du serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="ee77b-139">The other option is to use one network adapter for the internal side and three network adapters for the external side of the Edge Server.</span></span> <span data-ttu-id="ee77b-140">Le principal avantage de cette option est une carte réseau distincte par service de serveur Edge et une collection de données plus concise lorsque le dépannage est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ee77b-140">The main benefit of this option is a distinct network adapter per Edge Server service, and potentially more concise data collection when troubleshooting is necessary</span></span>



</div>

### <a name="dns-records-required-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-example"></a><span data-ttu-id="ee77b-141">Enregistrements DNS requis pour l’équilibrage de charge DNS à l’échelle, avec les adresses IP publiques (par exemple)</span><span class="sxs-lookup"><span data-stu-id="ee77b-141">DNS Records Required for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee77b-142">Emplacement/TYPE/port</span><span class="sxs-lookup"><span data-stu-id="ee77b-142">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="ee77b-143">Nom de domaine complet/enregistrement DNS</span><span class="sxs-lookup"><span data-stu-id="ee77b-143">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="ee77b-144">IP address/FQDN</span><span class="sxs-lookup"><span data-stu-id="ee77b-144">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="ee77b-145">Cartes sur/Commentaires</span><span class="sxs-lookup"><span data-stu-id="ee77b-145">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee77b-146">DNS/A externe</span><span class="sxs-lookup"><span data-stu-id="ee77b-146">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="ee77b-147">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ee77b-147">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ee77b-148">131.107.155.10 et 131.107.155.11</span><span class="sxs-lookup"><span data-stu-id="ee77b-148">131.107.155.10 and 131.107.155.11</span></span></p></td>
<td><p><span data-ttu-id="ee77b-149">Accès à l’interface externe du service Edge d’accès (contoso) si nécessaire pour tous les domaines SIP sur lesquels Lync a activé les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="ee77b-149">Access Edge service external interface (Contoso) Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee77b-150">DNS/A externe</span><span class="sxs-lookup"><span data-stu-id="ee77b-150">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="ee77b-151">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ee77b-151">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ee77b-152">131.107.155.20 et 131.107.155.21</span><span class="sxs-lookup"><span data-stu-id="ee77b-152">131.107.155.20 and 131.107.155.21</span></span></p></td>
<td><p><span data-ttu-id="ee77b-153">Interface externe du service de conférence Web</span><span class="sxs-lookup"><span data-stu-id="ee77b-153">Web Conferencing Edge service external interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee77b-154">DNS/A externe</span><span class="sxs-lookup"><span data-stu-id="ee77b-154">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="ee77b-155">av.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ee77b-155">av.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ee77b-156">131.107.155.30 et 131.107.155.31</span><span class="sxs-lookup"><span data-stu-id="ee77b-156">131.107.155.30 and 131.107.155.31</span></span></p></td>
<td><p><span data-ttu-id="ee77b-157">Interface externe du service A/V Edge</span><span class="sxs-lookup"><span data-stu-id="ee77b-157">A/V Edge service external interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee77b-158">DNS/SRV/443 externes</span><span class="sxs-lookup"><span data-stu-id="ee77b-158">External DNS/SRV/443</span></span></p></td>
<td><p><span data-ttu-id="ee77b-159">_sip._tls.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ee77b-159">_sip._tls.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ee77b-160">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ee77b-160">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ee77b-161">Interface externe du service Edge d’accès.</span><span class="sxs-lookup"><span data-stu-id="ee77b-161">Access Edge service external interface.</span></span> <span data-ttu-id="ee77b-162">Requis pour la configuration automatique de clients 2013 et Lync 2010 pour une utilisation externe.</span><span class="sxs-lookup"><span data-stu-id="ee77b-162">Required for automatic configuration of Lync 2013 and Lync 2010 clients to work externally.</span></span> <span data-ttu-id="ee77b-163">Répétez cette opération pour tous les domaines SIP pour lesquels Lync est compatible avec les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ee77b-163">Repeat as necessary for all SIP domains with Lync enabled users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee77b-164">DNS/SRV/5061 externes</span><span class="sxs-lookup"><span data-stu-id="ee77b-164">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="ee77b-165">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ee77b-165">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ee77b-166">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ee77b-166">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ee77b-167">Interface externe du service d’accès Edge requise pour la détection automatique de DNS des partenaires fédérés connus sous le nom de « domaine SIP autorisé » (appelé Fédération avancée dans les versions précédentes).</span><span class="sxs-lookup"><span data-stu-id="ee77b-167">Access Edge service external interface Required for automatic DNS discovery of federated partners known as “Allowed SIP Domain” (called enhanced federation in previous releases).</span></span> <span data-ttu-id="ee77b-168">Répétez cette opération pour tous les domaines SIP pour lesquels Lync est compatible avec les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ee77b-168">Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee77b-169">DNS interne/A</span><span class="sxs-lookup"><span data-stu-id="ee77b-169">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="ee77b-170">lsedge.contoso.net</span><span class="sxs-lookup"><span data-stu-id="ee77b-170">lsedge.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="ee77b-171">172.25.33.10 et 172.25.33.11</span><span class="sxs-lookup"><span data-stu-id="ee77b-171">172.25.33.10 and 172.25.33.11</span></span></p></td>
<td><p><span data-ttu-id="ee77b-172">Interface interne consolidée Edge</span><span class="sxs-lookup"><span data-stu-id="ee77b-172">Consolidated Edge internal interface</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="records-required-for-federation"></a><span data-ttu-id="ee77b-173">Enregistrements requis pour la Fédération</span><span class="sxs-lookup"><span data-stu-id="ee77b-173">Records Required for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee77b-174">Emplacement/TYPE/port</span><span class="sxs-lookup"><span data-stu-id="ee77b-174">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="ee77b-175">FQDN</span><span class="sxs-lookup"><span data-stu-id="ee77b-175">FQDN</span></span></th>
<th><span data-ttu-id="ee77b-176">Enregistrement d’adresse IP/nom de domaine complet</span><span class="sxs-lookup"><span data-stu-id="ee77b-176">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="ee77b-177">Cartes sur/Commentaires</span><span class="sxs-lookup"><span data-stu-id="ee77b-177">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee77b-178">DNS/SRV/5061 externes</span><span class="sxs-lookup"><span data-stu-id="ee77b-178">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="ee77b-179">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ee77b-179">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ee77b-180">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ee77b-180">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ee77b-181">L’interface externe du service d’accès Edge SIP doit être requise pour la découverte automatique du DNS de votre Fédération par le biais d’autres partenaires de Fédération potentiels, et elle est appelée « domaines SIP autorisés » (appelé Fédération avancée dans les versions précédentes).</span><span class="sxs-lookup"><span data-stu-id="ee77b-181">SIP Access Edge service external interface Required for automatic DNS discovery of your federation to other potential federation partners, and is known as “Allowed SIP Domains” (called enhanced federation in previous releases).</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="ee77b-182">Répétez cette opération pour tous les domaines SIP avec des utilisateurs compatibles Lync et des clients mobiles Microsoft Lync qui utilisent le service de notifications d’émission ou le service de notifications de transmission d’Apple.</span><span class="sxs-lookup"><span data-stu-id="ee77b-182">Repeat as necessary for all SIP domains with Lync enabled users and Microsoft Lync Mobile clients that use either the Push Notification Service or the Apple Push Notification service</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="ee77b-183">DNS Summary pour le protocole de messagerie et de présence extensible</span><span class="sxs-lookup"><span data-stu-id="ee77b-183">DNS Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee77b-184">Emplacement/TYPE/port</span><span class="sxs-lookup"><span data-stu-id="ee77b-184">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="ee77b-185">FQDN</span><span class="sxs-lookup"><span data-stu-id="ee77b-185">FQDN</span></span></th>
<th><span data-ttu-id="ee77b-186">Enregistrement d’adresse IP/nom de domaine complet</span><span class="sxs-lookup"><span data-stu-id="ee77b-186">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="ee77b-187">Cartes sur/Commentaires</span><span class="sxs-lookup"><span data-stu-id="ee77b-187">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee77b-188">DNS externe/SRV/5269</span><span class="sxs-lookup"><span data-stu-id="ee77b-188">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="ee77b-189">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ee77b-189">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ee77b-190">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ee77b-190">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ee77b-191">Interface externe du proxy XMPP du service Edge d’accès ou du pool Edge. Répétez cette opération pour tous les domaines SIP internes avec Lync pour les utilisateurs pour lesquels le contact avec les contacts XMPP est autorisé via la configuration de la stratégie d’accès externe par le biais d’une stratégie globale, d’une stratégie de site à l’emplacement de l’utilisateur ou d’une stratégie utilisateur appliquée à l’utilisateur Lync.</span><span class="sxs-lookup"><span data-stu-id="ee77b-191">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="ee77b-192">Un domaine XMPP autorisé doit également être configuré dans la stratégie partenaires fédérés de XMPP.</span><span class="sxs-lookup"><span data-stu-id="ee77b-192">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="ee77b-193">Pour plus d’informations, voir rubriques supplémentaires dans la <strong>section Voir aussi</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee77b-193">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee77b-194">DNS/A externe</span><span class="sxs-lookup"><span data-stu-id="ee77b-194">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="ee77b-195">xmpp.contoso.com (par exemple)</span><span class="sxs-lookup"><span data-stu-id="ee77b-195">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="ee77b-196">Adresse IP du service Edge d’accès sur votre serveur Edge ou pool d’hébergement de proxy XMPP</span><span class="sxs-lookup"><span data-stu-id="ee77b-196">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="ee77b-197">Pointe vers le service Edge d’accès ou le pool Edge qui héberge le service proxy XMPP.</span><span class="sxs-lookup"><span data-stu-id="ee77b-197">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="ee77b-198">En général, l’enregistrement SRV que vous créez pointe vers cet enregistrement hôte (A ou AAAA).</span><span class="sxs-lookup"><span data-stu-id="ee77b-198">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ee77b-199">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee77b-199">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

